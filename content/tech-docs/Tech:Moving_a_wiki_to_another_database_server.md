---
title: Tech:Moving a wiki to another database server
---

This page provides guidance if you need to move a wiki to another database server (typically relates to disk space issues/imbalances).

Moving a wiki to another database is not complicated provided you have the required rights (Infrastructure Specialists or database-admins).

* Put the wiki you are moving into read-only mode (add a read-only notice if you'd like, especially if it is a large wiki, and it will take time).
   * Example: [https://github.com/miraheze/mw-config/commit/497e5608d95ba148b81133d5c34ce72a046d9c43](https://github.com/miraheze/mw-config/commit/497e5608d95ba148b81133d5c34ce72a046d9c43)
* Connect to the **server on which the database is located** and as **root** execute:
* `mysqldump --single-transaction --routines --triggers nameofwiki | gzip -c | ssh -i /home/dbcopy/.ssh/id_ed25519 dbcopy@db151.wikitide.net 'cat > /home/dbcopy/nameofwiki.sql.gz'`
* `{{ {{note}} }}` Replace "nameofwiki" with the name of the wiki you want to move.
* Open **the target server** and unzip the file.
* `gunzip nameofwiki.sql.gz`
* Execute creation of the new database.
* `mysql -e 'create database nameofwiki;'`
* Import the database.
* ` mysql nameofwiki < nameofwiki.sql`
* Change `wiki_dbcluster` in `metawiki.cw_wikis`.
* Remove read-only mode from the wiki.
* After **you have made sure** that the wiki works on the new database server and that it has been imported correctly, you can drop the database on the initial server.

## Categories

* [Category:Tech](https://meta.miraheze.org/wiki/Category:Tech)
* [Category:Technology guidelines and guides](https://meta.miraheze.org/wiki/Category:Technology_guidelines_and_guides)



----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:Moving_a_wiki_to_another_database_server)**