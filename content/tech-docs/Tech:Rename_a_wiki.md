---
title: Tech:Rename a wiki
---

One should be careful renaming a wiki (database/domain) as it involves many steps and basically anything going wrong can make it impossible for users to login across the entire farm, or worse.

Following directions found [here](http://stackoverflow.com/questions/67093/how-do-i-quickly-rename-a-mysql-database-change-schema-name), I will update to clarify a little.

**Note:** The wiki should probably be made read-only before doing any of this, remember to make it readable after.
* One should create a complete SQL dump of the wiki to be renamed.
   * There are probably multiple ways of doing this, but I used `sudo -i mysqldump nameofwikidb > nameofwikidb.sql` in my home directory, replacing "nameofwikidb" to be the name of the database, including the final "wiki". Note that this (if run in your home directory) creates the SQL dump in your home directory.
* Create an empty database for the new wiki.
   * `sudo -i mysql -e "CREATE DATABASE nameofnewwikidb;"` replacing "nameofnewwikidb" with the target subdomain + wiki.
* Import the SQL dump into the new database.
   * `sudo -i mysql -D nameofnewwikidb -e "SOURCE /path/to/dump.sql;"` replacing the wiki name, path, and file name as appropriate, **but including the `;` at the end of the command**.
* After the new wiki is created, run:
   * `sudo -u www-data php /srv/mediawiki/w/extensions/CreateWiki/maintenance/renameWiki.php --wiki=loginwiki --rename nameofwikidb nameofnewwikidb <user_running_script>`
* Finally, **AFTER YOU ARE VERY CERTAIN ALL OF THE ABOVE WAS DONE CORRECTLY,** you may drop the old database.
   * `sudo -i mysql -e "DROP DATABASE nameofwikidb;"`

### Swift 

**Double check Swift**:
* `. /etc/swift-env.sh`
* `swift list --prefix miraheze-<old_wiki_db>`
If anything shows in the above, for each of them:
* `diff --color <(swift list miraheze-<new_wiki_db>-<zone>) <(swift list miraheze-<old_wiki_db>-<zone>)`
   * <zone> example: `local-public`
If only empty directories or everything looks fine there (files returned by that are now only present on old container, not on the new wiki container), you can remove the old containers with:
* `swift delete miraheze-<old_wiki_db>-<zone>`
* `sudo -u www-data rm -rf /tmp/miraheze-<old_wiki_db>-<zone>`

Finally, run:
* `sudo -u www-data php /srv/mediawiki/w/extensions/CreateWiki/maintenance/setContainersAccess.php --wiki=<new_wiki_db>`

### After rename 

* If there is any configuration on LocalSettings.php change the DB name there as well.

[Category:Technology guidelines and guides](https://meta.miraheze.org/wiki/Category:Technology_guidelines_and_guides)

----
**Source**: [https://meta.miraheze.org/wiki/Tech:Rename_a_wiki](https://meta.miraheze.org/wiki/Tech:Rename_a_wiki)