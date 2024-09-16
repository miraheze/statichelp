---
title: Tech:MariaDB
---

MariaDB<sub>(*reference:* English Wikipedia article: [MariaDB](https://meta.miraheze.org/wiki/w:MariaDB))</sub> is the chosen database software used in production. Currently we run 10.11.x on database servers.

## Configuration 

Database configuration is in [Puppet](/tech-docs/techpuppet.md).

## Master-replica replication 

In 2021, we tried using replication for database backups: see [T5877](https://meta.miraheze.org/wiki/phab:T5877). Due to I/O constraints on the cloud instances, we switched strategies. However, this guide to set up a new replica may be useful in the future.

### Dump data from master to replica 

mariabackup allows you to create a point-in-time dump of the database cluster. In this case, data is streamed to another server (destination) and extracted in `/home/dbcopy/backup-db6-10april`. The destination directory must exist and be writable before the command is executed!

In this example, we're going to clone db12 (c3) to dbbackup1. dbbackup1 is a server running multiple instances of MariaDB (multi-instance setup). First, it is mandatory to raise the soft limit for open files:
`[at the source] ulimit -Sn 1000000 `

Then you can start the mariabackup process:
```
[at the destination] mkdir /home/dbcopy/backup-db12-10january2020
[at the destination] chown -R mysql:mysql /home/dbcopy/backup-db12-10january2020
[at the destination] chmod 0750 /home/dbcopy/backup-db12-10january2020
[at the source] mariabackup --backup --slave-info --safe-slave-backup --stream=xbstream | ssh -i /home/dbcopy/.ssh/id_ed25519 dbcopy@dbbackup1.wikitide.net "mbstream -x -C /home/dbcopy/backup-db12-10january2020/"
```

An alternative (might be faster in some situations):
```
[at the source] mariabackup --open-files-limit=150000 --parallel=2 --backup --slave-info --safe-slave-backup --stream=xbstream | pigz -p 2 | ssh -i /home/dbcopy/.ssh/id_ed25519 dbcopy@dbbackup1.wikitide.net "pigz -dc -p 2 | mbstream -x --parallel=2 --directory=/home/dbcopy/backup-db12-10january2020/"
```
(the directory at the destination **must** be created before, please specify the correct date as well)

At the destination, the backup must be *prepared*, since the data is not consistent yet. You can do this using mariabackup:
```
[again, raise the soft open files limit] ulimit -Sn 1000000
mariabackup --prepare --open-files-limit=900000 --target-dir=/home/dbcopy/backup-db12-10january2020 --use-memory=2G
```

Finally, copy the directory to the appropriate location in /srv:
```
systemctl stop mariadb@c3
rm -rf /srv/mariadb.c3
mv /home/dbcopy/backup-db12-10january2020 /srv/mariadb.c3
chown -R mysql:mysql /srv/mariadb.c3
systemctl start mariadb@c3
```

### Replicate from master 

You need to change `MASTER_HOST`, `MASTER_PASSWORD`, `MASTER_LOG_FILE` and `MASTER_LOG_POS`. Never set up replication without TLS (`MASTER_SSL`) and never disable verification (`MASTER_SSL_VERIFY_SERVER_CERT`).

Look at the `xtrabackup_binlog_info` file for the binlog positions. The first field (e.g. `mysql-bin.000150`) is the value for `MASTER_LOG_FILE`, the second field is `MASTER_LOG_POS` (large digit number). The third field is a [global transaction ID](https://mariadb.com/kb/en/gtid/), but we don't use GTID for replication yet.

```
CHANGE MASTER TO 
   MASTER_HOST="<the db master>.wikitide.net", 
   MASTER_PORT=3306, 
   MASTER_USER="replica",  
   MASTER_PASSWORD="REDACTED", 
   MASTER_LOG_FILE='MYSQLBINLOG',
   MASTER_LOG_POS=POSITION,
   MASTER_SSL=1,
   MASTER_SSL_CA='/etc/ssl/certs/LetsEncrypt.crt',
   MASTER_SSL_VERIFY_SERVER_CERT=1;
START SLAVE;
```

## Revoke Grants / Drop User 

To revoke grants do the following:

* Run `SELECT User,Host FROM mysql.user;`
* Run `SHOW GRANTS FOR <User_column>@<Host_column>;`
* Run `REVOKE <Text_after_`GRANT`_and_before_ON> on <Table> from <User_column>@<Host_column>;`
**Example:**`REVOKE SELECT, PROCESS, REPLICATION CLIENT on *.* from exporter@81.4.127.174;`

To drop a user:
* Run `drop user <User_column>@<Host_column>;`
**Example:**`drop user exporter@81.4.127.174;`

## Restoring Database from a backup 

To restore a database from a .idb file following these steps:

* Follow [Restore backup](https://meta.miraheze.org/wiki/Tech:Bacula#Restoring_a_Backup) first. (Make sure the backup is not a diff rather it needs to be a full backup.)
* Setup mysql on test3 temporarily as we want to avoid using a production db system for this.
* Copy over the .idb files from db4 to test3.
* Create a fake db on test3 "create database testdb".
* Create the table matching the contents of the idb file.
* After creating the table, run "ALTER TABLE table_name DISCARD TABLESPACE;".
* Then copy the .idb file to `/var/lib/mysql/<db>/<table>.idb` (the file name you're copying should match the table name in `/var/lib/mysql/<db>/`).
* After that run "ALTER TABLE table_Name IMPORT TABLESPACE;".
* Now you can generate an sql file and import into db4.

## See also 

* [Restoring mysql tables from ind fpm files and or mysql log bin files](https://dba.stackexchange.com/questions/71596/restoring-mysql-tables-from-ibd-frm-and-mysqllogbin-files)

[Category:Services](https://meta.miraheze.org/wiki/Category:Services)
[Category:Technology guidelines and guides](https://meta.miraheze.org/wiki/Category:Technology_guidelines_and_guides)

----
**Source**: [https://meta.miraheze.org/wiki/Tech:MariaDB](https://meta.miraheze.org/wiki/Tech:MariaDB)