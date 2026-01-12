---
title: Tech:Server admin log
---

## 2026-01-11 

* 23:30 Universal Omega: upgraded os202 to Debian Trixie
* 23:20 Universal Omega: upgraded os162 to Debian Trixie
* 23:00 Universal Omega: upgraded os201 to Debian Trixie
* 23:00 Universal Omega: upgraded os191 to Debian Trixie
* 22:20 Universal Omega: upgraded os161 to Debian Trixie
* 22:07 Universal Omega: upgraded ldap171 to Debian Trixie
* 21:47 Universal Omega: upgraded llm191 to Debian Trixie
* 21:16 Reception123: DELETED and DROPPED [https://issue-tracker.miraheze.org/P577](https://issue-tracker.miraheze.org/P577) & [https://issue-tracker.miraheze.org/P578](https://issue-tracker.miraheze.org/P578)
* 21:08 MirahezeLSBot: [somerandomdeveloper@mwtask181] finished deploy of {'versions': '1.44', 'upgrade_extensions': 'RemovePII'} to all - SUCCESS in 29s
* 21:08 MirahezeLSBot: [somerandomdeveloper@mwtask181] starting deploy of {'versions': '1.44', 'upgrade_extensions': 'RemovePII'} to all
* 21:08 MirahezeLSBot: [somerandomdeveloper@test151] finished deploy of {'versions': ['1.44', '1.45'], 'upgrade_extensions': 'RemovePII'} to test151 - SUCCESS in 1s
* 21:08 MirahezeLSBot: [somerandomdeveloper@test151] starting deploy of {'versions': ['1.44', '1.45'], 'upgrade_extensions': 'RemovePII'} to test151
* 19:11 @paladox: reboot puppet181
* 18:59 @paladox: upgrade puppet181 to trixie
* 18:50 Universal Omega: upgraded os151 to Debian Trixie
* 17:30 Universal Omega: upgraded prometheus151 to Debian Trixie
* 17:29 Reception123: DELETED swift containers [https://issue-tracker.miraheze.org/P576](https://issue-tracker.miraheze.org/P576)
* 17:21 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php MirahezeMagic:CheckSwiftContainers --wiki=loginwiki (END - exit=0)
* 15:21 MirahezeLSBot: [paladox@mwtask181] sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/databases.php /srv/mediawiki/1.44/maintenance/run.php /srv/mediawiki/1.44/extensions/MatomoAnalytics/maintenance/DeleteCache.php
* 14:56 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php CreateWiki:DeleteWikis --wiki=loginwiki --delete Reception123 (END - exit=2)
* 13:58 MirahezeLSBot: [paladox@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 29s
* 13:57 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 13:57 MirahezeLSBot: [paladox@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 30s
* 13:56 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 13:56 MirahezeLSBot: [paladox@mwtask181] DEPLOY ABORTED: Non-Zero Exit Code in prep, see output.
* 13:56 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 13:30 MirahezeLSBot: [skye@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 27s
* 13:29 MirahezeLSBot: [skye@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 13:10 MirahezeLSBot: [skye@mwtask181] finished deploy of {'config': True} to all - SUCCESS in 29s
* 13:10 MirahezeLSBot: [skye@mwtask181] starting deploy of {'config': True} to all
* 11:21 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php /srv/mediawiki/1.44/maintenance/extensions/CheckWikiDatabases.php --wiki=loginwiki (END - exit=256)
* 11:21 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php /srv/mediawiki/1.44/maintenance/MirahezeMagic:CheckWikiDatabases.php --wiki=loginwiki (END - exit=256)
* 01:13 MirahezeLSBot: [somerandomdeveloper@test151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php OATHAuth:disableOATHAuthForUser --wiki=metawikibeta SomeRandomDeveloper (END - exit=65280)
* 00:50 Universal Omega: upgraded db172 to Debian Trixie
* 00:00 MirahezeLSBot: [universalomega@bots171] test

## 2026-01-10 

* 23:57 Universal Omega: upgraded bots171 to Debian Trixie
* 23:57 Universal Omega: test
* 21:56 Universal Omega: upgraded mon181 to Debian Trixie
* 21:08 Universal Omega: stop ircecho on mon181 for trixie upgrade to prevent immediately spamming everything.
* 20:46 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php CreateWiki:DeleteWikis --wiki=loginwiki --delete Reception123 (END - exit=2)
* 20:39 Universal Omega: upgraded db182 to Debian Trixie
* 20:10 Universal Omega: downtimed db182 in icinga for trixie upgrade
* 19:47 Universal Omega: upgraded matomo151 to Debian Trixie
* 18:28 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php rebuildtextindex --wiki=dappervolkwiki (END - exit=0)
* 18:27 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php rebuildtextindex --wiki=dappervolkwiki (START)
* 17:15 Reception123: started deletewikis.php
* 16:14 @paladox: delete old ns1 vm replaced by newer one
* 16:05 @paladox: restart  pdns-recursor everywhere
* 15:11 @paladox: reinstall ns1 with trixie (as a new vm to do a different bios setup)
* 11:14 Reception123: re-run delbackups after fixing issue

## 2026-01-09 

* 23:41 MirahezeLSBot: [somerandomdeveloper@mwtask181] finished deploy of {'versions': '1.44', 'upgrade_extensions': 'RemovePII'} to all - SUCCESS in 29s
* 23:40 MirahezeLSBot: [somerandomdeveloper@mwtask181] starting deploy of {'versions': '1.44', 'upgrade_extensions': 'RemovePII'} to all
* 23:40 MirahezeLSBot: [somerandomdeveloper@test151] finished deploy of {'versions': ['1.44', '1.45'], 'upgrade_extensions': 'RemovePII'} to test151 - SUCCESS in 1s
* 23:40 MirahezeLSBot: [somerandomdeveloper@test151] starting deploy of {'versions': ['1.44', '1.45'], 'upgrade_extensions': 'RemovePII'} to test151
* 23:29 MirahezeLSBot: [somerandomdeveloper@test151] finished deploy of {'l10n': True, 'versions': ['1.44', '1.45']} to test151 - SUCCESS in 651s
* 23:28 MirahezeLSBot: [somerandomdeveloper@mwtask181] finished deploy of {'l10n': True, 'versions': '1.44'} to all - SUCCESS in 552s
* 23:19 MirahezeLSBot: [somerandomdeveloper@mwtask181] starting deploy of {'l10n': True, 'versions': '1.44'} to all
* 23:18 MirahezeLSBot: [somerandomdeveloper@mwtask181] finished deploy of {'versions': '1.44', 'upgrade_extensions': 'UploadWizard'} to all - SUCCESS in 29s
* 23:18 MirahezeLSBot: [somerandomdeveloper@test151] starting deploy of {'l10n': True, 'versions': ['1.44', '1.45']} to test151
* 23:18 MirahezeLSBot: [somerandomdeveloper@mwtask181] starting deploy of {'versions': '1.44', 'upgrade_extensions': 'UploadWizard'} to all
* 23:18 MirahezeLSBot: [somerandomdeveloper@test151] finished deploy of {'versions': ['1.44', '1.45'], 'upgrade_extensions': 'UploadWizard'} to test151 - SUCCESS in 2s
* 23:18 MirahezeLSBot: [somerandomdeveloper@test151] starting deploy of {'versions': ['1.44', '1.45'], 'upgrade_extensions': 'UploadWizard'} to test151
* 23:08 MirahezeLSBot: [somerandomdeveloper@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 29s
* 23:08 MirahezeLSBot: [somerandomdeveloper@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 22:46 MirahezeLSBot: [somerandomdeveloper@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 30s
* 22:45 MirahezeLSBot: [somerandomdeveloper@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 20:32 Reception123: (on mwtask181)
* 20:32 Reception123: run delbackups (bash ./delbackups.sh /home/reception/delwikis09012026.txt /srv/mediawiki/w/maintenance/dumpBackup.ph)
* 19:33 MirahezeLSBot: [reception@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php MirahezeMagic:RenameDatabase --wiki=loginwiki --rename --old=attenboroughwiki --new=encyclopediakemowiki --user=Reception123 (END - exit=0)
* 19:16 MirahezeLSBot: [macfan@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 29s
* 19:15 MirahezeLSBot: [macfan@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 15:47 @paladox: reinstall ns2 with debian trixie
* 00:06 MirahezeLSBot: [somerandomdeveloper@test151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php ManageWiki:PopulateNamespaces --wiki=morerandomstuffwikibeta --force (END - exit=0)
* 00:05 MirahezeLSBot: [somerandomdeveloper@test151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php ManageWiki:PopulateNamespaces --wiki=morerandomstuffwikibeta (END - exit=256)
* 00:03 MirahezeLSBot: [somerandomdeveloper@test151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php ManageWiki:PopulateNamespacesWithDefaults --wiki=morerandomstuffwikibeta --overwrite (END - exit=0)
* 00:03 MirahezeLSBot: [somerandomdeveloper@test151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php ManageWiki:PopulateNamespacesWithDefaults --wiki=morerandomstuffwikibeta (END - exit=0)
* 00:00 MirahezeLSBot: [somerandomdeveloper@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 00:00 MirahezeLSBot: [somerandomdeveloper@test151] starting deploy of {'config': True} to test151

## 2026-01-08 

* 23:31 MirahezeLSBot: [somerandomdeveloper@mwtask181] finished deploy of {'versions': '1.44', 'upgrade_extensions': 'Wikibase'} to all - SUCCESS in 43s
* 23:31 MirahezeLSBot: [somerandomdeveloper@mwtask181] starting deploy of {'versions': '1.44', 'upgrade_extensions': 'Wikibase'} to all
* 23:31 MirahezeLSBot: [somerandomdeveloper@test151] finished deploy of {'versions': ['1.44', '1.45'], 'upgrade_extensions': 'Wikibase'} to test151 - SUCCESS in 9s
* 23:31 MirahezeLSBot: [somerandomdeveloper@test151] starting deploy of {'versions': ['1.44', '1.45'], 'upgrade_extensions': 'Wikibase'} to test151
* 21:54 MirahezeLSBot: [macfan@test151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php /srv/mediawiki/1.45/extensions/OATHAuth/maintenance/disableOATHAuthForUser.php --wiki=metawikibeta MacFan4000 (END - exit=0)
* 17:33 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php MirahezeMagic:ResetWiki --wiki=loginwiki --dbname=craighcraftwiki --requester=ZethalMC (END - exit=0)
* 16:10 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php SemanticMediaWiki:setupStore --wiki=wixosswiki (END - exit=0)
* 02:16 MirahezeLSBot: [somerandomdeveloper@mwtask181] sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/deleted.php /srv/mediawiki/1.44/maintenance/run.php sql /home/somerandomdeveloper/userprofile-patches.sql (END - exit=256)
* 01:46 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php CreateWiki:SetContainersAccess --wiki=winterworldwiki (END - exit=0)
* 01:44 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php MirahezeMagic:RenameDatabase --wiki=loginwiki --rename --old=winterwarswiki --new=winterworldwiki --user=Skye (END - exit=0)
* 01:40 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php CreateWiki:SetContainersAccess --wiki=findthetetoswiki (END - exit=0)
* 01:38 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php MirahezeMagic:RenameDatabase --wiki=loginwiki --rename --old=tetowiki --new=findthetetoswiki --user=Skye (END - exit=0)
* 00:29 MirahezeLSBot: [somerandomdeveloper@mwtask181] sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/deleted.php /srv/mediawiki/1.44/maintenance/run.php sql /home/somerandomdeveloper/userprofile-patches.sql (START)
* 00:28 MirahezeLSBot: [somerandomdeveloper@mwtask181] sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/deleted.php /srv/mediawiki/1.44/maintenance/run.php sql /home/somerandomdeveloper/comments-patches.sql (END - exit=256)
* 00:24 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php /srv/mediawiki/1.44/maintenance/initSiteStats.php --wiki=talodwiki --update (END - exit=0)
* 00:24 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php /srv/mediawiki/1.44/maintenance/rebuildall.php --wiki=talodwiki (END - exit=0)

## 2026-01-07 

* 22:41 MirahezeLSBot: [somerandomdeveloper@mwtask181] finished deploy of {'folders': '1.44/extensions/ProofreadPage'} to all - SUCCESS in 31s
* 22:40 SomeRandomDeveloper: removed local patches for T14482
* 22:40 MirahezeLSBot: [somerandomdeveloper@mwtask181] starting deploy of {'folders': '1.44/extensions/ProofreadPage'} to all
* 22:39 MirahezeLSBot: [somerandomdeveloper@test151] finished deploy of {'folders': '1.44/extensions/ProofreadPage,1.45/extensions/ProofreadPage'} to test151 - SUCCESS in 0s
* 22:39 MirahezeLSBot: [somerandomdeveloper@test151] starting deploy of {'folders': '1.44/extensions/ProofreadPage,1.45/extensions/ProofreadPage'} to test151
* 22:36 MirahezeLSBot: [somerandomdeveloper@mwtask181] sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/deleted.php /srv/mediawiki/1.44/maintenance/run.php sql /home/somerandomdeveloper/comments-patches.sql (START)
* 21:42 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php /srv/mediawiki/1.44/maintenance/rebuildall.php --wiki=talodwiki (START)
* 21:42 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php /srv/mediawiki/1.44/maintenance/importDump.php --wiki=talodwiki dump.xml --no-updates (END - exit=0)
* 21:41 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php /srv/mediawiki/1.44/maintenance/importDump.php --wiki=talodwiki dump.xml --no-updates (START)
* 21:10 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php /srv/mediawiki/1.44/maintenance/initSiteStats.php --wiki=talodwiki --update (END - exit=0)
* 21:10 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php /srv/mediawiki/1.44/maintenance/rebuildall.php --wiki=talodwiki (END - exit=2)
* 21:10 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php /srv/mediawiki/1.44/maintenance/rebuildall.php --wiki=talodwiki (START)
* 21:10 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php /srv/mediawiki/1.44/maintenance/importDump.php --wiki=talodwiki dump.xml --no-updates (END - exit=256)
* 21:10 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php /srv/mediawiki/1.44/maintenance/importDump.php --wiki=talodwiki dump.xml --no-updates (START)
* 03:30 MirahezeLSBot: [somerandomdeveloper@mwtask181] sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/databases.php /srv/mediawiki/1.44/maintenance/run.php sql /home/somerandomdeveloper/comments-patches.sql (END - exit=256)

## 2026-01-06 

* 21:56 MirahezeLSBot: [universalomega@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 29s
* 21:55 MirahezeLSBot: [universalomega@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 21:55 MirahezeLSBot: [somerandomdeveloper@test151] finished deploy of {'l10n': True, 'versions': ['1.44', '1.45']} to test151 - SUCCESS in 660s
* 21:47 MirahezeLSBot: [somerandomdeveloper@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 30s
* 21:46 MirahezeLSBot: [somerandomdeveloper@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 21:46 MirahezeLSBot: [somerandomdeveloper@test151] finished deploy of {'pull': 'config', 'config': True} to test151 - SUCCESS in 0s
* 21:46 MirahezeLSBot: [somerandomdeveloper@test151] starting deploy of {'pull': 'config', 'config': True} to test151
* 21:44 SomeRandomDeveloper: deployed local patch for T14757 on beta and prod
* 21:44 MirahezeLSBot: [somerandomdeveloper@test151] starting deploy of {'l10n': True, 'versions': ['1.44', '1.45']} to test151
* 20:30 SomeRandomDeveloper: (using a combined version of the two patches from [https://gerrit.wikimedia.org/r/c/mediawiki/extensions/Comments/+/1221613](https://gerrit.wikimedia.org/r/c/mediawiki/extensions/Comments/+/1221613))
* 20:30 MirahezeLSBot: [somerandomdeveloper@mwtask181] sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/databases.php /srv/mediawiki/1.44/maintenance/run.php sql /home/somerandomdeveloper/comments-patches.sql (START)
* 20:28 MirahezeLSBot: [somerandomdeveloper@mwtask181] finished deploy of {'folders': '1.44/extensions/Comments'} to all - SUCCESS in 29s
* 20:28 MirahezeLSBot: [somerandomdeveloper@mwtask181] starting deploy of {'folders': '1.44/extensions/Comments'} to all
* 18:23 MirahezeLSBot: [universalomega@mwtask181] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php MirahezeMagic:RenameDatabase --wiki=metawiki --old=dpl3wiki --new=dpl4wiki --user=Universal_Omega --rename (END - exit=0)
* 18:16 MirahezeLSBot: [universalomega@mwtask181] finished deploy of {'versions': '1.44', 'upgrade_extensions': 'MirahezeMagic'} to all - SUCCESS in 31s
* 18:16 MirahezeLSBot: [universalomega@mwtask181] starting deploy of {'versions': '1.44', 'upgrade_extensions': 'MirahezeMagic'} to all
* 15:51 @paladox: restarted mariadb and took it out of recovery mode
* 15:50 @paladox: started in recovery mode in  mariadb and dropped repository_commit_corrupt table in phabricator_repository
* 15:47 @paladox: restart db182
* 02:37 Universal Omega: bring phorge back online, but some tasks will still give exceptions if they have an attached commit to them.
* 02:27 Universal Omega: RENAME TABLE repository_commit TO repository_commit_corrupt; (will restore from backup) and place db182 into InnoDB recovery mode for a moment (out of recovery mode now)
* 01:37 Universal Omega: kill phorge and restart db182 from host
* 00:30 @paladox: restart mariadb on db182
* 00:24 @paladox: reboot phorge171
* 00:13 @paladox: upgrade phorge on phorge171
* 00:03 SomeRandomDeveloper: ran "./bin/policy unlock E1 --edit SomeRandomDeveloper" for T13002

## 2026-01-05 

* 23:54 SomeRandomDeveloper: test
* 23:49 SomeRandomDev: test
* 23:12 SomeRandomDeveloper: (the SQL file combines all four userboard patches)
* 23:12 SomeRandomDeveloper: started "sudo -u www-data ~/foreachwikiindblist-parallel /srv/mediawiki/cache/databases.php php /srv/mediawiki/1.44/maintenance/run.php sql /home/somerandomdeveloper/userprofile-patches.sql" on prod
* 23:10 MirahezeLSBot: [somerandomdeveloper@mwtask181] finished deploy of {'versions': '1.44', 'upgrade_extensions': 'SocialProfile'} to all - SUCCESS in 33s
* 23:09 MirahezeLSBot: [somerandomdeveloper@mwtask181] starting deploy of {'versions': '1.44', 'upgrade_extensions': 'SocialProfile'} to all
* 23:08 SomeRandomDeveloper: ran all four SQL patches from < [https://github.com/wikimedia/mediawiki-extensions-SocialProfile/commit/b48bca41319e0b601580c62d4ce603b04f6f7e57](https://github.com/wikimedia/mediawiki-extensions-SocialProfile/commit/b48bca41319e0b601580c62d4ce603b04f6f7e57)> on all beta wikis
* 23:06 MirahezeLSBot: [somerandomdeveloper@test151] finished deploy of {'versions': ['1.44', '1.45'], 'upgrade_extensions': 'SocialProfile'} to test151 - SUCCESS in 21s
* 23:05 MirahezeLSBot: [somerandomdeveloper@test151] starting deploy of {'versions': ['1.44', '1.45'], 'upgrade_extensions': 'SocialProfile'} to test151
* 22:56 SomeRandomDeveloper: ran "sudo -u www-data ~/foreachwikiindblist-parallel /srv/mediawiki/cache/databases.php php /srv/mediawiki/1.45/maintenance/run.php sql /srv/mediawiki/1.44/extensions/Comments/sql/patches/drop-Comment_Vote_IP.sql" on test151
* 22:56 SomeRandomDeveloper: ran "sudo -u www-data ~/foreachwikiindblist-parallel /srv/mediawiki/cache/databases.php php /srv/mediawiki/1.45/maintenance/run.php sql /srv/mediawiki/1.44/extensions/Comments/sql/patches/drop-Comment_IP.sql" on test151
* 22:54 MirahezeLSBot: [somerandomdeveloper@test151] finished deploy of {'folders': '1.44/extensions/Comments,1.45/extensions/Comments'} to test151 - SUCCESS in 0s
* 22:54 MirahezeLSBot: [somerandomdeveloper@test151] starting deploy of {'folders': '1.44/extensions/Comments,1.45/extensions/Comments'} to test151
* 22:12 @paladox: upgraded salt on puppet181
* 21:41 MirahezeLSBot: [somerandomdeveloper@puppet181] Upgraded packages on cloud15: libsodium23
* 21:37 MirahezeLSBot: [somerandomdeveloper@db201] manually upgraded libsodium23 due to T14767
* 21:35 MirahezeLSBot: [somerandomdeveloper@puppet181] Upgraded packages on swiftobject201: libsodium23
* 21:35 MirahezeLSBot: [somerandomdeveloper@puppet181] Upgraded packages on swiftobject181: libsodium23
* 21:35 MirahezeLSBot: [somerandomdeveloper@puppet181] Upgraded packages on swiftproxy171: libsodium23
* 21:34 MirahezeLSBot: [somerandomdeveloper@puppet181] Upgraded packages on swiftobject151: libsodium23
* 21:34 MirahezeLSBot: [somerandomdeveloper@puppet181] Upgraded packages on swiftobject191: libsodium23
* 21:33 MirahezeLSBot: [somerandomdeveloper@puppet181] Upgraded packages on swiftobject161: libsodium23
* 21:33 MirahezeLSBot: [somerandomdeveloper@puppet181] Upgraded packages on swiftproxy161: libsodium23
* 21:33 MirahezeLSBot: [somerandomdeveloper@puppet181] Upgraded packages on swiftobject171: libsodium23
* 21:32 MirahezeLSBot: [somerandomdeveloper@puppet181] Upgraded packages on swiftac171: libsodium23
* 21:32 MirahezeLSBot: [somerandomdeveloper@puppet181] Upgraded packages on test151: libsodium23
* 21:32 MirahezeLSBot: [somerandomdeveloper@puppet181] Upgraded packages on puppet181: libsodium23
* 21:32 MirahezeLSBot: [somerandomdeveloper@puppet181] Upgraded packages on reports171: libsodium23
* 21:31 MirahezeLSBot: [somerandomdeveloper@puppet181] Upgraded packages on rdb151: libsodium23
* 21:31 MirahezeLSBot: [somerandomdeveloper@puppet181] Upgraded packages on ns2: libsodium23
* 21:30 MirahezeLSBot: [somerandomdeveloper@puppet181] Upgraded packages on os202: libsodium23
* 21:30 MirahezeLSBot: [somerandomdeveloper@puppet181] Upgraded packages on os201: libsodium23
* 21:30 MirahezeLSBot: [somerandomdeveloper@puppet181] Upgraded packages on phorge171: libsodium23
* 21:29 MirahezeLSBot: [somerandomdeveloper@puppet181] Upgraded packages on prometheus151: libsodium23
* 21:29 MirahezeLSBot: [somerandomdeveloper@puppet181] Upgraded packages on os191: libsodium23
* 21:29 MirahezeLSBot: [somerandomdeveloper@puppet181] Upgraded packages on os162: libsodium23
* 21:28 MirahezeLSBot: [somerandomdeveloper@puppet181] Upgraded packages on mwtask181: libsodium23
* 21:28 MirahezeLSBot: [somerandomdeveloper@puppet181] Upgraded packages on os161: libsodium23
* 21:28 MirahezeLSBot: [somerandomdeveloper@puppet181] Upgraded packages on os151: libsodium23
* 21:28 MirahezeLSBot: [somerandomdeveloper@puppet181] Upgraded packages on ns1: libsodium23
* 21:27 MirahezeLSBot: [somerandomdeveloper@puppet181] Upgraded packages on mwtask171: libsodium23
* 21:27 MirahezeLSBot: [somerandomdeveloper@puppet181] Upgraded packages on mwtask161: libsodium23
* 21:27 MirahezeLSBot: [somerandomdeveloper@puppet181] Upgraded packages on mw203: libsodium23
* 21:26 MirahezeLSBot: [somerandomdeveloper@puppet181] Upgraded packages on mwtask151: libsodium23
* 21:26 MirahezeLSBot: [somerandomdeveloper@puppet181] Upgraded packages on mw202: libsodium23
* 21:26 MirahezeLSBot: [somerandomdeveloper@puppet181] Upgraded packages on mw201: libsodium23
* 21:26 MirahezeLSBot: [somerandomdeveloper@puppet181] Upgraded packages on mw183: libsodium23
* 21:25 MirahezeLSBot: [somerandomdeveloper@puppet181] Upgraded packages on mw192: libsodium23
* 21:25 MirahezeLSBot: [somerandomdeveloper@puppet181] Upgraded packages on mw173: libsodium23
* 21:25 MirahezeLSBot: [somerandomdeveloper@puppet181] Upgraded packages on mw182: libsodium23
* 21:24 MirahezeLSBot: [somerandomdeveloper@puppet181] Upgraded packages on mw161: libsodium23
* 21:24 MirahezeLSBot: [somerandomdeveloper@puppet181] Upgraded packages on mw162: libsodium23
* 21:24 MirahezeLSBot: [somerandomdeveloper@puppet181] Upgraded packages on mw181: libsodium23
* 21:23 MirahezeLSBot: [somerandomdeveloper@puppet181] Upgraded packages on mw171: libsodium23
* 21:23 MirahezeLSBot: [somerandomdeveloper@puppet181] Upgraded packages on mw191: libsodium23
* 21:23 MirahezeLSBot: [somerandomdeveloper@puppet181] Upgraded packages on mw163: libsodium23
* 21:22 MirahezeLSBot: [somerandomdeveloper@puppet181] Upgraded packages on mw172: libsodium23
* 21:22 MirahezeLSBot: [somerandomdeveloper@puppet181] Upgraded packages on mw151: libsodium23
* 21:22 MirahezeLSBot: [somerandomdeveloper@puppet181] Upgraded packages on mw193: libsodium23
* 21:21 MirahezeLSBot: [somerandomdeveloper@puppet181] Upgraded packages on mw153: libsodium23
* 21:21 MirahezeLSBot: [somerandomdeveloper@puppet181] Upgraded packages on mw152: libsodium23
* 21:21 MirahezeLSBot: [somerandomdeveloper@puppet181] Upgraded packages on mem191: libsodium23
* 21:20 MirahezeLSBot: [somerandomdeveloper@puppet181] Upgraded packages on mon181: libsodium23
* 21:20 MirahezeLSBot: [somerandomdeveloper@puppet181] Upgraded packages on mem201: libsodium23
* 21:20 MirahezeLSBot: [somerandomdeveloper@puppet181] Upgraded packages on mem161: libsodium23
* 21:19 MirahezeLSBot: [somerandomdeveloper@puppet181] Upgraded packages on mem151: libsodium23
* 21:19 MirahezeLSBot: [somerandomdeveloper@puppet181] Upgraded packages on ldap171: libsodium23
* 21:19 MirahezeLSBot: [somerandomdeveloper@puppet181] Upgraded packages on matomo151: libsodium23
* 21:19 MirahezeLSBot: [somerandomdeveloper@puppet181] Upgraded packages on llm191: libsodium23
* 21:18 MirahezeLSBot: [somerandomdeveloper@puppet181] Upgraded packages on mattermost1: libsodium23
* 21:18 MirahezeLSBot: [somerandomdeveloper@puppet181] Upgraded packages on db181: libsodium23
* 21:18 MirahezeLSBot: [somerandomdeveloper@puppet181] Upgraded packages on cp201: libsodium23
* 21:18 MirahezeLSBot: [somerandomdeveloper@puppet181] Upgraded packages on db182: libsodium23
* 21:17 MirahezeLSBot: [somerandomdeveloper@puppet181] Upgraded packages on bots171: libsodium23
* 21:17 MirahezeLSBot: [somerandomdeveloper@puppet181] Upgraded packages on graylog161: libsodium23
* 21:17 MirahezeLSBot: [somerandomdeveloper@puppet181] Upgraded packages on cp171: libsodium23
* 21:16 MirahezeLSBot: [somerandomdeveloper@puppet181] Upgraded packages on eventgate181: libsodium23
* 21:16 MirahezeLSBot: [somerandomdeveloper@puppet181] Upgraded packages on db161: libsodium23
* 21:16 MirahezeLSBot: [somerandomdeveloper@puppet181] Upgraded packages on cloud20: libsodium23
* 21:16 MirahezeLSBot: [somerandomdeveloper@puppet181] Upgraded packages on kafka181: libsodium23
* 21:15 MirahezeLSBot: [somerandomdeveloper@puppet181] Upgraded packages on db172: libsodium23
* 21:15 MirahezeLSBot: [somerandomdeveloper@puppet181] Upgraded packages on db171: libsodium23
* 21:15 MirahezeLSBot: [somerandomdeveloper@puppet181] Upgraded packages on cloud19: libsodium23
* 21:14 MirahezeLSBot: [somerandomdeveloper@puppet181] Upgraded packages on cp191: libsodium23
* 21:14 MirahezeLSBot: [somerandomdeveloper@puppet181] Upgraded packages on db151: libsodium23
* 21:14 MirahezeLSBot: [somerandomdeveloper@puppet181] Upgraded packages on cloud17: libsodium23
* 21:14 MirahezeLSBot: [somerandomdeveloper@puppet181] Upgraded packages on cloud18: libsodium23
* 21:13 MirahezeLSBot: [somerandomdeveloper@puppet181] Upgraded packages on cp161: libsodium23
* 21:13 MirahezeLSBot: [somerandomdeveloper@puppet181] Upgraded packages on changeprop201: libsodium23
* 21:13 MirahezeLSBot: [somerandomdeveloper@puppet181] Upgraded packages on bast161: libsodium23
* 21:12 MirahezeLSBot: [somerandomdeveloper@puppet181] Upgraded packages on db192: libsodium23
* 21:12 MirahezeLSBot: [somerandomdeveloper@puppet181] Upgraded packages on bast181: libsodium23
* 21:12 MirahezeLSBot: [somerandomdeveloper@puppet181] Upgraded packages on cloud16: libsodium23
* 21:03 MirahezeLSBot: [somerandomdeveloper@mwtask181] finished deploy of {'versions': '1.44', 'upgrade_skins': 'Citizen'} to all - SUCCESS in 34s
* 21:03 MirahezeLSBot: [somerandomdeveloper@mwtask181] starting deploy of {'versions': '1.44', 'upgrade_skins': 'Citizen'} to all
* 21:02 MirahezeLSBot: [somerandomdeveloper@test151] finished deploy of {'versions': ['1.44', '1.45'], 'upgrade_skins': 'Citizen'} to test151 - SUCCESS in 2s
* 21:02 MirahezeLSBot: [somerandomdeveloper@test151] starting deploy of {'versions': ['1.44', '1.45'], 'upgrade_skins': 'Citizen'} to test151
* 20:59 MirahezeLSBot: [somerandomdeveloper@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 37s
* 20:58 MirahezeLSBot: [somerandomdeveloper@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 20:58 MirahezeLSBot: [somerandomdeveloper@test151] finished deploy of {'pull': 'config', 'config': True} to test151 - SUCCESS in 1s
* 20:58 MirahezeLSBot: [somerandomdeveloper@test151] starting deploy of {'pull': 'config', 'config': True} to test151
* 20:50 SomeRandomDeveloper: salt-ssh -E 'mw.*' cmd.run 'sudo -u www-data rm -rf /srv/mediawiki/1.44/extensions/QuickSurveys/'
* 20:48 MirahezeLSBot: [somerandomdeveloper@test151] sudo -u www-data rm -rf /srv/mediawiki/1.44/extensions/QuickSurveys/ /srv/mediawiki/1.45/extensions/QuickSurveys/
* 20:48 MirahezeLSBot: [somerandomdeveloper@test151] sudo -u www-data rm -rf /srv/mediawiki-staging/1.44/extensions/QuickSurveys/ /srv/mediawiki-staging/1.45/extensions/QuickSurveys/
* 20:47 MirahezeLSBot: [somerandomdeveloper@mwtask181] sudo -u www-data rm -rf /srv/mediawiki/1.44/extensions/QuickSurveys/
* 20:46 MirahezeLSBot: [somerandomdeveloper@mwtask181] sudo -u www-data rm -rf /srv/mediawiki-staging/1.44/extensions/QuickSurveys/
* 20:41 MirahezeLSBot: [somerandomdeveloper@mwtask181] finished deploy of {'versions': '1.44', 'upgrade_extensions': 'PageSchemas'} to all - SUCCESS in 29s
* 20:40 MirahezeLSBot: [somerandomdeveloper@mwtask181] starting deploy of {'versions': '1.44', 'upgrade_extensions': 'PageSchemas'} to all
* 20:39 MirahezeLSBot: [somerandomdeveloper@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 30s
* 20:39 MirahezeLSBot: [somerandomdeveloper@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 20:39 MirahezeLSBot: [somerandomdeveloper@test151] finished deploy of {'pull': 'config', 'config': True} to test151 - SUCCESS in 0s
* 20:39 MirahezeLSBot: [somerandomdeveloper@test151] starting deploy of {'pull': 'config', 'config': True} to test151
* 13:58 MirahezeLSBot: [paladox@test151] finished deploy of {'l10n': True, 'force_upgrade': True, 'versions': ['1.44', '1.45'], 'upgrade_extensions': 'LdapAuthentication', 'upgrade_skins': 'Femiwiki'} to test151 - SUCCESS in 671s
* 13:47 MirahezeLSBot: [paladox@test151] starting deploy of {'l10n': True, 'force_upgrade': True, 'versions': ['1.44', '1.45'], 'upgrade_extensions': 'LdapAuthentication', 'upgrade_skins': 'Femiwiki'} to test151
* 12:53 MirahezeLSBot: [paladox@test151] finished deploy of {'l10n': True, 'force_upgrade': True, 'versions': ['1.44', '1.45'], 'upgrade_extensions': 'MirahezeMagic'} to test151 - SUCCESS in 425s
* 12:46 MirahezeLSBot: [paladox@test151] starting deploy of {'l10n': True, 'force_upgrade': True, 'versions': ['1.44', '1.45'], 'upgrade_extensions': 'MirahezeMagic'} to test151
* 12:39 MirahezeLSBot: [paladox@test151] starting deploy of {'l10n': True, 'force_upgrade': True, 'versions': ['1.44', '1.45'], 'upgrade_extensions': 'MirahezeMagic'} to test151
* 12:35 MirahezeLSBot: [paladox@test151] DEPLOY ABORTED: Non-Zero Exit Code in prep, see output.
* 12:35 MirahezeLSBot: [paladox@test151] starting deploy of {'l10n': True, 'versions': ['1.44', '1.45'], 'upgrade_extensions': 'MirahezeMagic'} to test151
* 12:34 MirahezeLSBot: [paladox@test151] DEPLOY ABORTED: Non-Zero Exit Code in prep, see output.
* 12:34 MirahezeLSBot: [paladox@test151] starting deploy of {'l10n': True, 'force_upgrade': True, 'versions': ['1.44', '1.45'], 'upgrade_extensions': 'MirahezeMagic'} to test151
* 12:32 MirahezeLSBot: [paladox@mwtask181] finished deploy of {'l10n': True, 'versions': '1.44', 'upgrade_extensions': 'MirahezeMagic'} to all - SUCCESS in 193s
* 12:29 MirahezeLSBot: [paladox@test151] DEPLOY ABORTED: Non-Zero Exit Code in prep, see output.
* 12:29 MirahezeLSBot: [paladox@test151] starting deploy of {'l10n': True, 'versions': ['1.44', '1.45'], 'upgrade_extensions': 'MirahezeMagic'} to test151
* 12:29 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'l10n': True, 'versions': '1.44', 'upgrade_extensions': 'MirahezeMagic'} to all
* 12:28 @paladox: salt-ssh -E "mw.*" cmd.run "rm -r /srv/mediawiki/1.44/extensions/Interwiki"
* 12:26 MirahezeLSBot: [paladox@test151] finished deploy of {'l10n': True, 'versions': ['1.44', '1.45'], 'upgrade_extensions': ['Cargo', 'PageForms']} to test151 - SUCCESS in 186s
* 12:26 MirahezeLSBot: [paladox@mwtask181] finished deploy of {'l10n': True, 'versions': '1.44', 'upgrade_extensions': ['Cargo', 'PageForms']} to all - SUCCESS in 192s
* 12:23 MirahezeLSBot: [paladox@test151] starting deploy of {'l10n': True, 'versions': ['1.44', '1.45'], 'upgrade_extensions': ['Cargo', 'PageForms']} to test151
* 12:23 MirahezeLSBot: [paladox@test151] finished deploy of {'l10n': True, 'versions': ['1.44', '1.45'], 'upgrade_extensions': 'RatePage'} to test151 - SUCCESS in 627s
* 12:23 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'l10n': True, 'versions': '1.44', 'upgrade_extensions': ['Cargo', 'PageForms']} to all
* 12:21 MirahezeLSBot: [paladox@mwtask181] finished deploy of {'l10n': True, 'versions': '1.44', 'upgrade_extensions': 'RatePage'} to all - SUCCESS in 517s
* 12:13 MirahezeLSBot: [paladox@test151] starting deploy of {'l10n': True, 'versions': ['1.44', '1.45'], 'upgrade_extensions': 'RatePage'} to test151
* 12:12 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'l10n': True, 'versions': '1.44', 'upgrade_extensions': 'RatePage'} to all
* 09:10 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php purgeParserCache --wiki=pilgrammedwiki --age=360 (END - exit=0)
* 05:26 MirahezeLSBot: [skye@mwtask171] Finished import for pilgrammedwiki (XML: None; Images: .) (END - exit=0)
* 05:26 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php initSiteStats --wiki=pilgrammedwiki --update (END - exit=0)
* 05:26 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php initSiteStats --wiki=pilgrammedwiki --update (START)
* 05:26 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php importImages --wiki=pilgrammedwiki --sleep=1 '--comment=Importing images from [fandom:pilgrammed-rblx](https://meta.miraheze.org/wiki/fandom:pilgrammed-rblx) ([T14753](https://meta.miraheze.org/wiki/phorge:T14753))' --search-recursively -- . (END - exit=0)
* 03:15 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php importImages --wiki=pilgrammedwiki --sleep=1 '--comment=Importing images from [fandom:pilgrammed-rblx](https://meta.miraheze.org/wiki/fandom:pilgrammed-rblx) ([T14753](https://meta.miraheze.org/wiki/phorge:T14753))' --search-recursively -- . (START)
* 03:15 MirahezeLSBot: [skye@mwtask171] Starting import for pilgrammedwiki (XML: None; Images: .) (START)
* 01:27 MirahezeLSBot: [universalomega@mwtask181] finished deploy of {'force_upgrade': True, 'versions': '1.44', 'upgrade_extensions': 'DynamicPageList4'} to all - SUCCESS in 30s
* 01:26 MirahezeLSBot: [universalomega@mwtask181] starting deploy of {'force_upgrade': True, 'versions': '1.44', 'upgrade_extensions': 'DynamicPageList4'} to all

## 2026-01-04 

* 20:49 MirahezeLSBot: [somerandomdeveloper@test151] finished deploy of {'config': True, 'ignore_time': True} to test151 - SUCCESS in 0s
* 20:49 MirahezeLSBot: [somerandomdeveloper@test151] starting deploy of {'config': True, 'ignore_time': True} to test151
* 20:42 MirahezeLSBot: [somerandomdeveloper@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 20:42 MirahezeLSBot: [somerandomdeveloper@test151] starting deploy of {'config': True} to test151
* 20:06 SomeRandomDeveloper: (T14755)
* 20:06 SomeRandomDeveloper: DROP DATABASE shintowiki; on db181
* 20:04 MirahezeLSBot: [somerandomdeveloper@mwtask181] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php CreateWiki:DeleteWiki --wiki=loginwiki --delete --deletewiki shintowiki (END - exit=0)
* 18:59 MirahezeLSBot: [somerandomdeveloper@test151] finished deploy of {'pull': 'config', 'config': True} to test151 - SUCCESS in 1s
* 18:59 MirahezeLSBot: [somerandomdeveloper@test151] starting deploy of {'pull': 'config', 'config': True} to test151
* 18:53 MirahezeLSBot: [somerandomdeveloper@test151] finished deploy of {'versions': ['1.44', '1.45'], 'upgrade_extensions': 'PageSchemas'} to test151 - SUCCESS in 2s
* 18:53 MirahezeLSBot: [somerandomdeveloper@test151] starting deploy of {'versions': ['1.44', '1.45'], 'upgrade_extensions': 'PageSchemas'} to test151

## 2026-01-03 

* 14:17 MirahezeLSBot: [skye@mwtask171] Finished import for pilgrammedwiki (XML: pilgrammed.xml; Images: None) (END - exit=0)
* 14:17 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php initSiteStats --wiki=pilgrammedwiki --update (END - exit=0)
* 14:17 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php initSiteStats --wiki=pilgrammedwiki --update (START)
* 14:17 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php initEditCount --wiki=pilgrammedwiki (END - exit=0)
* 14:17 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php initEditCount --wiki=pilgrammedwiki (START)
* 14:17 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php rebuildall --wiki=pilgrammedwiki (END - exit=0)
* 13:55 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php rebuildall --wiki=pilgrammedwiki (START)
* 13:55 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php importDump --wiki=pilgrammedwiki --no-updates --username-prefix=fandom:pilgrammed-rblx -- pilgrammed.xml (END - exit=0)
* 13:21 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php importDump --wiki=pilgrammedwiki --no-updates --username-prefix=fandom:pilgrammed-rblx -- pilgrammed.xml (START)
* 13:21 MirahezeLSBot: [skye@mwtask171] Starting import for pilgrammedwiki (XML: pilgrammed.xml; Images: None) (START)
* 12:04 MirahezeLSBot: [somerandomdeveloper@test151] finished deploy of {'versions': '1.45', 'upgrade_extensions': 'MassEditRegex'} to test151 - SUCCESS in 0s
* 12:04 MirahezeLSBot: [somerandomdeveloper@test151] starting deploy of {'versions': '1.45', 'upgrade_extensions': 'MassEditRegex'} to test151
* 02:32 MirahezeLSBot: [skye@mwtask171] Finished import for etohwiki (XML: jtohfandom.xml; Images: None) (END - exit=0)
* 02:32 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php initSiteStats --wiki=etohwiki --update (END - exit=0)
* 02:32 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php initSiteStats --wiki=etohwiki --update (START)
* 02:32 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php initEditCount --wiki=etohwiki (END - exit=0)
* 02:32 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php initEditCount --wiki=etohwiki (START)
* 02:32 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php rebuildall --wiki=etohwiki (END - exit=0)

## 2026-01-02 

* 20:25 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php rebuildall --wiki=etohwiki (START)
* 20:25 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php importDump --wiki=etohwiki --no-updates --username-prefix=fandom:jtoh -- jtohfandom.xml (END - exit=0)
* 17:04 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php importDump --wiki=etohwiki --no-updates --username-prefix=fandom:jtoh -- jtohfandom.xml (START)
* 17:04 MirahezeLSBot: [skye@mwtask171] Starting import for etohwiki (XML: jtohfandom.xml; Images: None) (START)
* 12:40 MirahezeLSBot: [skye@mwtask171] Finished import for etohwiki (XML: None; Images: .) (END - exit=0)
* 12:40 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php initSiteStats --wiki=etohwiki --update (END - exit=0)
* 12:40 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php initSiteStats --wiki=etohwiki --update (START)
* 12:40 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php importImages --wiki=etohwiki --sleep=1 '--comment=Importing images from [fandom:jtoh](https://meta.miraheze.org/wiki/fandom:jtoh) ([T14709](https://meta.miraheze.org/wiki/phorge:T14709))' --search-recursively -- . (END - exit=0)
* 11:59 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php deleteArchivedRevisions --wiki=etohwiki --delete (END - exit=0)
* 11:57 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php deleteOldRevisions --wiki=etohwiki --delete (END - exit=0)
* 11:18 MirahezeLSBot: [skye@mwtask171] Finished import for etohwiki (XML: Juke.xml; Images: None) (END - exit=1)
* 11:18 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php importDump --wiki=etohwiki --no-updates --username-prefix=fandom:jtoh -- Juke.xml (END - exit=1)
* 11:18 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php importDump --wiki=etohwiki --no-updates --username-prefix=fandom:jtoh -- Juke.xml (START)
* 11:18 MirahezeLSBot: [skye@mwtask171] Starting import for etohwiki (XML: Juke.xml; Images: None) (START)
* 10:55 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php nukeNS --wiki=etohwiki --ns=829 --all --delete (END - exit=0)
* 10:55 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php nukeNS --wiki=etohwiki --ns=829 --all --delete (START)
* 10:54 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php nukeNS --wiki=etohwiki --ns=828 --all --delete (END - exit=0)
* 10:54 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php nukeNS --wiki=etohwiki --ns=828 --all --delete (START)
* 10:53 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php nukeNS --wiki=etohwiki --ns=15 --all --delete (END - exit=0)
* 10:53 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php nukeNS --wiki=etohwiki --ns=15 --all --delete (START)
* 10:52 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php nukeNS --wiki=etohwiki --ns=14 --all --delete (END - exit=0)
* 10:51 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php nukeNS --wiki=etohwiki --ns=14 --all --delete (START)
* 10:51 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php nukeNS --wiki=etohwiki --ns=12 --all --delete (END - exit=0)
* 10:51 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php nukeNS --wiki=etohwiki --ns=12 --all --delete (START)
* 10:50 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php nukeNS --wiki=etohwiki --ns=11 --all --delete (END - exit=0)
* 10:50 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php nukeNS --wiki=etohwiki --ns=11 --all --delete (START)
* 10:50 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php nukeNS --wiki=etohwiki --ns=10 --all --delete (END - exit=0)
* 10:50 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php nukeNS --wiki=etohwiki --ns=10 --all --delete (START)
* 10:50 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php nukeNS --wiki=etohwiki --ns=9 --all --delete (END - exit=0)
* 10:50 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php nukeNS --wiki=etohwiki --ns=9 --all --delete (START)
* 10:47 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php nukeNS --wiki=etohwiki --ns=8 --all --delete (END - exit=0)
* 10:46 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php nukeNS --wiki=etohwiki --ns=8 --all --delete (START)
* 10:46 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php nukeNS --wiki=etohwiki --ns=5 --all --delete (END - exit=0)
* 10:46 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php nukeNS --wiki=etohwiki --ns=5 --all --delete (START)
* 10:45 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php nukeNS --wiki=etohwiki --ns=4 --all --delete (END - exit=0)
* 10:44 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php nukeNS --wiki=etohwiki --ns=4 --all --delete (START)
* 10:44 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php nukeNS --wiki=etohwiki --ns=3 --all --delete (END - exit=0)
* 10:44 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php nukeNS --wiki=etohwiki --ns=3 --all --delete (START)
* 10:44 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php nukeNS --wiki=etohwiki --ns=2 --all --delete (END - exit=0)
* 10:42 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php nukeNS --wiki=etohwiki --ns=2 --all --delete (START)
* 10:41 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php nukeNS --wiki=etohwiki --ns=1 --all --delete (END - exit=0)
* 10:38 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php nukeNS --wiki=etohwiki --ns=1 --all --delete (START)
* 10:38 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php nukeNS --wiki=etohwiki --ns=0 --all --delete (END - exit=0)
* 10:36 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php nukeNS --wiki=etohwiki --ns=0 --all --delete (START)
* 10:11 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php rebuildall --wiki=etohwiki (END - exit=2)
* 09:35 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php rebuildall --wiki=etohwiki (START)
* 06:51 MirahezeLSBot: [skye@mwtask171] Finished import for rexreincarnatedwiki (XML: rexreincarnated.xml; Images: None) (END - exit=0)
* 06:51 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php initSiteStats --wiki=rexreincarnatedwiki --update (END - exit=0)
* 06:51 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php initSiteStats --wiki=rexreincarnatedwiki --update (START)
* 06:51 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php initEditCount --wiki=rexreincarnatedwiki (END - exit=0)
* 06:51 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php initEditCount --wiki=rexreincarnatedwiki (START)
* 06:51 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php rebuildall --wiki=rexreincarnatedwiki (END - exit=0)
* 06:11 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php rebuildall --wiki=rexreincarnatedwiki (START)
* 06:11 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php importDump --wiki=rexreincarnatedwiki --no-updates --username-prefix=fandom:rex-reincarnated -- rexreincarnated.xml (END - exit=0)
* 05:27 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php importDump --wiki=rexreincarnatedwiki --no-updates --username-prefix=fandom:rex-reincarnated -- rexreincarnated.xml (START)
* 05:27 MirahezeLSBot: [skye@mwtask171] Starting import for rexreincarnatedwiki (XML: rexreincarnated.xml; Images: None) (START)
* 04:44 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php importImages --wiki=etohwiki --sleep=1 '--comment=Importing images from [fandom:jtoh](https://meta.miraheze.org/wiki/fandom:jtoh) ([T14709](https://meta.miraheze.org/wiki/phorge:T14709))' --search-recursively -- . (START)
* 04:44 MirahezeLSBot: [skye@mwtask171] Starting import for etohwiki (XML: None; Images: .) (START)
* 04:25 MirahezeLSBot: [skye@mwtask171] Finished import for theunofficialoutcomememorieswiki (XML: None; Images: .) (END - exit=1)
* 04:25 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php importImages --wiki=theunofficialoutcomememorieswiki --sleep=1 '--comment=Import images from [fandom:the-unofficial-outcome-memories](https://meta.miraheze.org/wiki/fandom:the-unofficial-outcome-memories) ([T14676](https://meta.miraheze.org/wiki/phorge:T14676))' --search-recursively -- . (END - exit=1)
* 04:16 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php importImages --wiki=theunofficialoutcomememorieswiki --sleep=1 '--comment=Import images from [fandom:the-unofficial-outcome-memories](https://meta.miraheze.org/wiki/fandom:the-unofficial-outcome-memories) ([T14676](https://meta.miraheze.org/wiki/phorge:T14676))' --search-recursively -- . (START)
* 04:16 MirahezeLSBot: [skye@mwtask171] Starting import for theunofficialoutcomememorieswiki (XML: None; Images: .) (START)
* 04:08 MirahezeLSBot: [skye@mwtask171] Finished import for theunofficialoutcomememorieswiki (XML: None; Images: .) (END - exit=-2)
* 04:08 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php importImages --wiki=theunofficialoutcomememorieswiki --sleep=1 '--comment=Import images from [fandom:the-unofficial-outcome-memories](https://meta.miraheze.org/wiki/fandom:the-unofficial-outcome-memories) ([T14676](https://meta.miraheze.org/wiki/phorge:T14676))' --search-recursively -- . (END - exit=-2)
* 03:37 MirahezeLSBot: [skye@mwtask171] Finished import for klep2catswiki (XML: None; Images: .) (END - exit=0)
* 03:37 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php initSiteStats --wiki=klep2catswiki --update (END - exit=0)
* 03:37 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php initSiteStats --wiki=klep2catswiki --update (START)
* 03:37 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php importImages --wiki=klep2catswiki --sleep=1 '--comment=Importing images from [fandom:kleptocats-2](https://meta.miraheze.org/wiki/fandom:kleptocats-2) ([T14706](https://meta.miraheze.org/wiki/phorge:T14706))' --search-recursively -- . (END - exit=0)
* 03:31 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php importImages --wiki=klep2catswiki --sleep=1 '--comment=Importing images from [fandom:kleptocats-2](https://meta.miraheze.org/wiki/fandom:kleptocats-2) ([T14706](https://meta.miraheze.org/wiki/phorge:T14706))' --search-recursively -- . (START)
* 03:31 MirahezeLSBot: [skye@mwtask171] Starting import for klep2catswiki (XML: None; Images: .) (START)
* 03:19 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php importImages --wiki=theunofficialoutcomememorieswiki --sleep=1 '--comment=Import images from [fandom:the-unofficial-outcome-memories](https://meta.miraheze.org/wiki/fandom:the-unofficial-outcome-memories) ([T14676](https://meta.miraheze.org/wiki/phorge:T14676))' --search-recursively -- . (START)
* 03:19 MirahezeLSBot: [skye@mwtask171] Starting import for theunofficialoutcomememorieswiki (XML: None; Images: .) (START)
* 03:03 MirahezeLSBot: [skye@mwtask171] Finished import for lernatelierwiki (XML: None; Images: .) (END - exit=0)
* 03:03 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php initSiteStats --wiki=lernatelierwiki --update (END - exit=0)
* 03:03 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php initSiteStats --wiki=lernatelierwiki --update (START)
* 03:03 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php importImages --wiki=lernatelierwiki --sleep=1 '--comment=Importing images from [http://lernatelier.dsmynas.net/mediawiki/images](http://lernatelier.dsmynas.net/mediawiki/images) ([T14688](https://meta.miraheze.org/wiki/phorge:T14688))' --search-recursively -- . (END - exit=0)
* 02:48 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php importImages --wiki=lernatelierwiki --sleep=1 '--comment=Importing images from [http://lernatelier.dsmynas.net/mediawiki/images](http://lernatelier.dsmynas.net/mediawiki/images) ([T14688](https://meta.miraheze.org/wiki/phorge:T14688))' --search-recursively -- . (START)
* 02:48 MirahezeLSBot: [skye@mwtask171] Starting import for lernatelierwiki (XML: None; Images: .) (START)

## 2026-01-01 

* 00:00 MirahezeLSBot: [www-data@mwtask181] Began automatic backing up

----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:Server_admin_log)**