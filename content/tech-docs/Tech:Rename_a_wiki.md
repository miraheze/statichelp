---
title: Tech:Rename a wiki
---

One should be careful renaming a wiki (database/domain) as it involves many steps and basically anything going wrong can make it impossible for users to login across the entire farm, or worse. Please pay attention to what the scripts output when doing a rename to make sure everything is working properly.

* Start by running `mwscript MirahezeMagic:RenameDatabase loginwiki --rename --old=<old_wiki_db> --new=<new_wiki_db> --user=<user_running_script>`
   * Run without `--rename` to run in dry run mode.
* **AFTER YOU ARE VERY CERTAIN THE ABOVE WAS DONE CORRECTLY,** you may drop the old database. **This is not a requirement to do.**
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
* `mwscript CreateWiki:SetContainersAccess <new_wiki_db>`

### After rename 

* If there is any configuration on LocalSettings.php change the database name there as well.

## Categories

* [Category:Technology guidelines and guides](https://meta.miraheze.org/wiki/Category:Technology_guidelines_and_guides)

----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:Rename_a_wiki)**