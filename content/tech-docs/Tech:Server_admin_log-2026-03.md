---
title: Tech:Server admin log/2026-03
---

`{{ {{Server admin log/nav}} }}`

## 2026-03-31 

* 23:42 MirahezeLSBot: [somerandomdeveloper@mwtask181] finished deploy of {'versions': '1.45', 'upgrade_extensions': 'Echo'} to all - SUCCESS in 26s
* 23:42 MirahezeLSBot: [somerandomdeveloper@mwtask181] starting deploy of {'versions': '1.45', 'upgrade_extensions': 'Echo'} to all
* 23:42 MirahezeLSBot: [somerandomdeveloper@test151] finished deploy of {'versions': '1.45', 'upgrade_extensions': 'Echo'} to test151 - SUCCESS in 1s
* 23:42 MirahezeLSBot: [somerandomdeveloper@test151] starting deploy of {'versions': '1.45', 'upgrade_extensions': 'Echo'} to test151
* 23:32 MirahezeLSBot: [somerandomdeveloper@mwtask181] finished deploy of {'versions': '1.45', 'upgrade_extensions': 'OATHAuth'} to all - SUCCESS in 24s
* 23:32 MirahezeLSBot: [somerandomdeveloper@mwtask181] starting deploy of {'versions': '1.45', 'upgrade_extensions': 'OATHAuth'} to all
* 23:32 MirahezeLSBot: [somerandomdeveloper@test151] finished deploy of {'versions': '1.45', 'upgrade_extensions': 'OATHAuth'} to test151 - SUCCESS in 1s
* 23:32 MirahezeLSBot: [somerandomdeveloper@test151] starting deploy of {'versions': '1.45', 'upgrade_extensions': 'OATHAuth'} to test151
* 23:06 MirahezeLSBot: [somerandomdeveloper@mwtask181] sudo -u www-data foreachwikiindblist /tmp/bucket.php /srv/mediawiki/1.45/maintenance/run.php /srv/mediawiki/1.45/extensions/ManageWiki/maintenance/ResetWikiCaches.php
* 23:03 MirahezeLSBot: [somerandomdeveloper@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:GenerateExtensionDatabaseList --wiki=metawiki --extension=bucket --directory=/tmp
* 22:40 SomeRandomDeveloper: trigger binlog purges on db151, db171 and db181 as well
* 22:40 SomeRandomDeveloper: temporarily set slave_connections_needed_for_purge = 0 on db161 and db192 to trigger binlog purging, then undo to match puppet state
* 22:40 SomeRandomDeveloper: ran "SET GLOBAL slave_connections_needed_for_purge = 0;" on db172 ([https://jira.mariadb.org/browse/MDEV-38849](https://jira.mariadb.org/browse/MDEV-38849))
* 22:40 SomeRandomDeveloper: restart logbot on bots171

## 2026-03-30 

* 16:46 MirahezeLSBot: [rhinos@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 23s
* 16:45 MirahezeLSBot: [rhinos@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 07:11 MirahezeLSBot: [petramagna@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 07:11 MirahezeLSBot: [petramagna@test151] starting deploy of {'config': True} to test151
* 00:08 MirahezeLSBot: [petramagna@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 23s
* 00:08 MirahezeLSBot: [petramagna@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all

## 2026-03-29 

* 23:19 MirahezeLSBot: [petramagna@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 23:19 MirahezeLSBot: [petramagna@test151] starting deploy of {'config': True} to test151
* 22:28 MirahezeLSBot: [petramagna@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 22:28 MirahezeLSBot: [petramagna@test151] starting deploy of {'config': True} to test151
* 22:10 MirahezeLSBot: [petramagna@mwtask181] finished deploy of {'versions': '1.45', 'upgrade_extensions': 'MirahezeMagic'} to all - SUCCESS in 24s
* 22:10 MirahezeLSBot: [petramagna@mwtask181] starting deploy of {'versions': '1.45', 'upgrade_extensions': 'MirahezeMagic'} to all
* 22:04 MirahezeLSBot: [petramagna@test151] finished deploy of {'versions': '1.45', 'upgrade_extensions': 'MirahezeMagic'} to test151 - SUCCESS in 0s
* 22:03 MirahezeLSBot: [petramagna@test151] starting deploy of {'versions': '1.45', 'upgrade_extensions': 'MirahezeMagic'} to test151
* 22:01 MirahezeLSBot: [petramagna@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 23s
* 22:00 MirahezeLSBot: [petramagna@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 21:59 MirahezeLSBot: [petramagna@test151] finished deploy of {'pull': 'config', 'config': True} to test151 - SUCCESS in 0s
* 21:59 MirahezeLSBot: [petramagna@test151] starting deploy of {'pull': 'config', 'config': True} to test151
* 19:45 MirahezeLSBot: [petramagna@test151] finished deploy of {'folders': '1.45/extensions/MirahezeMagic'} to test151 - SUCCESS in 0s
* 19:45 MirahezeLSBot: [petramagna@test151] starting deploy of {'folders': '1.45/extensions/MirahezeMagic'} to test151
* 19:45 MirahezeLSBot: [petramagna@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 19:44 MirahezeLSBot: [petramagna@test151] starting deploy of {'config': True} to test151
* 19:27 MirahezeLSBot: [void@puppet181] Upgraded packages on changeprop202: nodejs, libnode115, and nodejs-doc
* 19:27 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask181: nodejs, libnode115, and nodejs-doc
* 19:26 MirahezeLSBot: [void@puppet181] Upgraded packages on mw183: nodejs, libnode115, and nodejs-doc
* 19:26 MirahezeLSBot: [void@puppet181] Upgraded packages on mw203: nodejs, libnode115, and nodejs-doc
* 19:26 MirahezeLSBot: [void@puppet181] Upgraded packages on mw201: nodejs, libnode115, and nodejs-doc
* 19:25 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask171: nodejs, libnode115, and nodejs-doc
* 19:25 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask151: nodejs, libnode115, and nodejs-doc
* 19:25 MirahezeLSBot: [void@puppet181] Upgraded packages on test151: nodejs, libnode115, and nodejs-doc
* 19:25 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask161: nodejs, libnode115, and nodejs-doc
* 19:24 MirahezeLSBot: [void@puppet181] Upgraded packages on mw193: nodejs, libnode115, and nodejs-doc
* 19:24 MirahezeLSBot: [void@puppet181] Upgraded packages on mw182: nodejs, libnode115, and nodejs-doc
* 19:24 MirahezeLSBot: [void@puppet181] Upgraded packages on mw173: nodejs, libnode115, and nodejs-doc
* 19:23 MirahezeLSBot: [void@puppet181] Upgraded packages on mw181: nodejs, libnode115, and nodejs-doc
* 19:23 MirahezeLSBot: [void@puppet181] Upgraded packages on mw202: nodejs, libnode115, and nodejs-doc
* 19:23 MirahezeLSBot: [void@puppet181] Upgraded packages on mw191: nodejs, libnode115, and nodejs-doc
* 19:23 MirahezeLSBot: [void@puppet181] Upgraded packages on mw192: nodejs, libnode115, and nodejs-doc
* 19:22 MirahezeLSBot: [void@puppet181] Upgraded packages on mw163: nodejs, libnode115, and nodejs-doc
* 19:22 MirahezeLSBot: [void@puppet181] Upgraded packages on mw152: nodejs, libnode115, and nodejs-doc
* 19:22 MirahezeLSBot: [void@puppet181] Upgraded packages on mw161: nodejs, libnode115, and nodejs-doc
* 19:21 MirahezeLSBot: [void@puppet181] Upgraded packages on mw153: nodejs, libnode115, and nodejs-doc
* 19:21 MirahezeLSBot: [void@puppet181] Upgraded packages on mw162: nodejs, libnode115, and nodejs-doc
* 19:21 MirahezeLSBot: [void@puppet181] Upgraded packages on mw172: nodejs, libnode115, and nodejs-doc
* 19:21 MirahezeLSBot: [void@puppet181] Upgraded packages on mw171: nodejs, libnode115, and nodejs-doc
* 19:20 MirahezeLSBot: [void@puppet181] Upgraded packages on mw151: nodejs, libnode115, and nodejs-doc
* 19:20 MirahezeLSBot: [void@puppet181] Upgraded packages on eventgate182: nodejs, libnode115, and nodejs-doc
* 11:21 MirahezeLSBot: [petramagna@test151] finished deploy of {'folders': '1.45/extensions/MirahezeMagic'} to test151 - SUCCESS in 0s
* 11:21 MirahezeLSBot: [petramagna@test151] starting deploy of {'folders': '1.45/extensions/MirahezeMagic'} to test151
* 11:14 MirahezeLSBot: [petramagna@test151] finished deploy of {'folders': '1.45/extensions/MirahezeMagic'} to test151 - SUCCESS in 0s
* 11:14 MirahezeLSBot: [petramagna@test151] starting deploy of {'folders': '1.45/extensions/MirahezeMagic'} to test151
* 11:12 MirahezeLSBot: [petramagna@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 11:12 MirahezeLSBot: [petramagna@test151] starting deploy of {'config': True} to test151
* 08:04 MirahezeLSBot: [petramagna@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:ResetWiki --wiki=loginwiki --dbname=scratchwiki --requester=MC_mrjone (END - exit=0)
* 07:43 MirahezeLSBot: [petramagna@test151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php ManageWiki:ModifyGroupPermission --wiki=buckettestwikibeta --group=bureaucrat --addperms=editbucket (END - exit=0)

## 2026-03-28 

* 23:25 MirahezeLSBot: [petramagna@mwtask151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php ManageWiki:ResetWikiCaches --wiki=strinovawiki (END - exit=0)
* 22:31 MirahezeLSBot: [petramagna@mwtask181] finished deploy of {'extension_list': True, 'force_upgrade': True, 'versions': '1.45', 'upgrade_extensions': 'Bucket', 'ignore_time': True} to mwtask151 - SUCCESS in 1s
* 22:31 MirahezeLSBot: [petramagna@mwtask181] starting deploy of {'extension_list': True, 'force_upgrade': True, 'versions': '1.45', 'upgrade_extensions': 'Bucket', 'ignore_time': True} to mwtask151
* 22:24 MirahezeLSBot: [petramagna@mwtask181] finished deploy of {'extension_list': True, 'force_upgrade': True, 'versions': '1.45', 'upgrade_extensions': 'Bucket'} to mwtask151 - SUCCESS in 1s
* 22:24 MirahezeLSBot: [petramagna@mwtask181] starting deploy of {'extension_list': True, 'force_upgrade': True, 'versions': '1.45', 'upgrade_extensions': 'Bucket'} to mwtask151
* 22:09 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask181: libxml-parser-perl
* 22:09 MirahezeLSBot: [void@puppet181] Upgraded packages on test151: libxml-parser-perl
* 22:08 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask171: libxml-parser-perl
* 22:08 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask161: libxml-parser-perl
* 22:08 MirahezeLSBot: [void@puppet181] Upgraded packages on mw203: libxml-parser-perl
* 22:08 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask151: libxml-parser-perl
* 22:07 MirahezeLSBot: [void@puppet181] Upgraded packages on mw202: libxml-parser-perl
* 22:07 MirahezeLSBot: [void@puppet181] Upgraded packages on mw201: libxml-parser-perl
* 22:07 MirahezeLSBot: [void@puppet181] Upgraded packages on mw183: libxml-parser-perl
* 22:07 MirahezeLSBot: [void@puppet181] Upgraded packages on mw193: libxml-parser-perl
* 22:06 MirahezeLSBot: [void@puppet181] Upgraded packages on eventgate182: libxml-parser-perl
* 22:06 MirahezeLSBot: [void@puppet181] Upgraded packages on mw192: libxml-parser-perl
* 22:06 MirahezeLSBot: [void@puppet181] Upgraded packages on mw173: libxml-parser-perl
* 22:06 MirahezeLSBot: [void@puppet181] Upgraded packages on mw182: libxml-parser-perl
* 22:05 MirahezeLSBot: [void@puppet181] Upgraded packages on mw181: libxml-parser-perl
* 22:05 MirahezeLSBot: [void@puppet181] Upgraded packages on mw172: libxml-parser-perl
* 22:05 MirahezeLSBot: [void@puppet181] Upgraded packages on mw163: libxml-parser-perl
* 22:05 MirahezeLSBot: [void@puppet181] Upgraded packages on mw153: libxml-parser-perl
* 22:04 MirahezeLSBot: [void@puppet181] Upgraded packages on mw191: libxml-parser-perl
* 22:04 MirahezeLSBot: [void@puppet181] Upgraded packages on mw162: libxml-parser-perl
* 22:04 MirahezeLSBot: [void@puppet181] Upgraded packages on mw161: libxml-parser-perl
* 22:04 MirahezeLSBot: [void@puppet181] Upgraded packages on mw152: libxml-parser-perl
* 22:03 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud19: libxml-parser-perl
* 22:03 MirahezeLSBot: [void@puppet181] Upgraded packages on mw171: libxml-parser-perl
* 22:03 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud17: libxml-parser-perl
* 22:03 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud20: libxml-parser-perl
* 22:02 MirahezeLSBot: [void@puppet181] Upgraded packages on changeprop202: libxml-parser-perl
* 22:02 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud18: libxml-parser-perl
* 22:02 MirahezeLSBot: [void@puppet181] Upgraded packages on mw151: libxml-parser-perl
* 22:02 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud16: libxml-parser-perl
* 22:02 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud15: libxml-parser-perl
* 22:01 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud21: libxml-parser-perl
* 17:50 MirahezeLSBot: [wwr@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php cleanupTitles --wiki=battlecatswiki (END - exit=0)
* 17:49 MirahezeLSBot: [wwr@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php cleanupTitles --wiki=battlecatswiki (END - exit=33280)
* 17:09 MirahezeLSBot: [wwr@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php purgeParserCache --wiki=bucketwiki (END - exit=256)
* 17:07 MirahezeLSBot: [wwr@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php /srv/mediawiki/1.45/maintenance/Bucket:RefreshAllBuckets.php --wiki=bucketwiki (END - exit=256)
* 17:06 MirahezeLSBot: [wwr@mwtask181] finished deploy of {'pull': 'config', 'config': True, 'extension_list': True, 'force_upgrade': True, 'versions': '1.45', 'upgrade_extensions': 'Bucket'} to all - SUCCESS in 68s
* 17:05 MirahezeLSBot: [wwr@mwtask181] starting deploy of {'pull': 'config', 'config': True, 'extension_list': True, 'force_upgrade': True, 'versions': '1.45', 'upgrade_extensions': 'Bucket'} to all
* 17:04 MirahezeLSBot: [skye@mwtask181] finished deploy of {'versions': '1.45', 'upgrade_extensions': 'Bucket'} to all - SUCCESS in 22s
* 17:04 MirahezeLSBot: [skye@mwtask181] starting deploy of {'versions': '1.45', 'upgrade_extensions': 'Bucket'} to all
* 17:00 MirahezeLSBot: [wwr@mwtask181] starting deploy of {'pull': 'config', 'config': True, 'l10n': True, 'extension_list': True, 'force_upgrade': True, 'versions': '1.45', 'upgrade_extensions': 'Bucket'} to all
* 16:59 MirahezeLSBot: [wwr@mwtask181] starting deploy of {'pull': 'config', 'config': True, 'l10n': True, 'extension_list': True, 'force_upgrade': True, 'versions': '1.45', 'upgrade_extensions': 'Bucket'} to all
* 16:45 MirahezeLSBot: [wwr@mwtask181] finished deploy of {'pull': 'config', 'config': True, 'l10n': True, 'extension_list': True, 'versions': '1.45'} to all - SUCCESS in 122s
* 16:43 MirahezeLSBot: [wwr@mwtask181] starting deploy of {'pull': 'config', 'config': True, 'l10n': True, 'extension_list': True, 'versions': '1.45'} to all
* 16:40 MirahezeLSBot: [wwr@mwtask181] starting deploy of {'pull': 'config', 'config': True, 'l10n': True, 'extension_list': True, 'force_upgrade': True, 'versions': '1.45', 'upgrade_extensions': 'Bucket'} to all
* 16:39 MirahezeLSBot: [wwr@mwtask181] finished deploy of {'config': True} to all - SUCCESS in 23s
* 16:38 MirahezeLSBot: [wwr@mwtask181] starting deploy of {'config': True} to all
* 13:36 MirahezeLSBot: [paladox@mwtask181] finished deploy of {'l10n': True, 'versions': '1.45', 'upgrade_extensions': ['Cargo', 'PageForms']} to all - SUCCESS in 580s
* 13:32 MirahezeLSBot: [paladox@test151] finished deploy of {'l10n': True, 'versions': '1.45', 'upgrade_extensions': ['Cargo', 'PageForms']} to test151 - SUCCESS in 331s
* 13:26 MirahezeLSBot: [paladox@test151] starting deploy of {'l10n': True, 'versions': '1.45', 'upgrade_extensions': ['Cargo', 'PageForms']} to test151
* 13:26 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'l10n': True, 'versions': '1.45', 'upgrade_extensions': ['Cargo', 'PageForms']} to all
* 12:53 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php dumpBackup --wiki=buckettestwikibeta --full (END - exit=0)
* 05:10 MirahezeLSBot: [skye@mwtask181] finished deploy of {'config': True} to all - SUCCESS in 22s
* 05:10 MirahezeLSBot: [skye@mwtask181] starting deploy of {'config': True} to all
* 04:18 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftproxy161: bind9-host, bind9-dnsutils, and bind9-libs
* 04:18 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftproxy171: bind9-host, bind9-dnsutils, and bind9-libs
* 04:18 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject201: bind9-host, bind9-dnsutils, and bind9-libs
* 04:17 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject211: bind9-host, bind9-dnsutils, and bind9-libs
* 04:17 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject191: bind9-host, bind9-dnsutils, and bind9-libs
* 04:17 MirahezeLSBot: [void@puppet181] Upgraded packages on test151: bind9-host, bind9-dnsutils, and bind9-libs
* 04:16 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject181: bind9-host, bind9-dnsutils, and bind9-libs
* 04:16 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject171: bind9-host, bind9-dnsutils, and bind9-libs
* 04:16 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject161: bind9-host, bind9-dnsutils, and bind9-libs
* 04:16 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftac171: bind9-host, bind9-dnsutils, and bind9-libs
* 04:15 MirahezeLSBot: [void@puppet181] Upgraded packages on ns2: bind9-host, bind9-dnsutils, and bind9-libs
* 04:15 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject151: bind9-host, bind9-dnsutils, and bind9-libs
* 04:15 MirahezeLSBot: [void@puppet181] Upgraded packages on rdb191: bind9-host, bind9-dnsutils, and bind9-libs
* 04:15 MirahezeLSBot: [void@puppet181] Upgraded packages on os202: bind9-host, bind9-dnsutils, and bind9-libs
* 04:14 MirahezeLSBot: [void@puppet181] Upgraded packages on reports171: bind9-host, bind9-dnsutils, and bind9-libs
* 04:14 MirahezeLSBot: [void@puppet181] Upgraded packages on puppet181: bind9-host, bind9-dnsutils, and bind9-libs
* 04:14 MirahezeLSBot: [void@puppet181] Upgraded packages on os162: bind9-host, bind9-dnsutils, and bind9-libs
* 04:13 MirahezeLSBot: [void@puppet181] Upgraded packages on prometheus151: bind9-host, bind9-dnsutils, and bind9-libs
* 04:13 MirahezeLSBot: [void@puppet181] Upgraded packages on os191: bind9-host, bind9-dnsutils, and bind9-libs
* 04:13 MirahezeLSBot: [void@puppet181] Upgraded packages on os201: bind9-host, bind9-dnsutils, and bind9-libs
* 04:13 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask181: bind9-host, bind9-dnsutils, and bind9-libs
* 04:12 MirahezeLSBot: [void@puppet181] Upgraded packages on phorge171: bind9-host, bind9-dnsutils, and bind9-libs
* 04:12 MirahezeLSBot: [void@puppet181] Upgraded packages on os151: bind9-host, bind9-dnsutils, and bind9-libs
* 04:12 MirahezeLSBot: [void@puppet181] Upgraded packages on mw201: bind9-host, bind9-dnsutils, and bind9-libs
* 04:12 MirahezeLSBot: [void@puppet181] Upgraded packages on mw202: bind9-host, bind9-dnsutils, and bind9-libs
* 04:11 MirahezeLSBot: [void@puppet181] Upgraded packages on os161: bind9-host, bind9-dnsutils, and bind9-libs
* 04:11 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask171: bind9-host, bind9-dnsutils, and bind9-libs
* 04:11 MirahezeLSBot: [void@puppet181] Upgraded packages on mw203: bind9-host, bind9-dnsutils, and bind9-libs
* 04:11 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask151: bind9-host, bind9-dnsutils, and bind9-libs
* 04:10 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask161: bind9-host, bind9-dnsutils, and bind9-libs
* 04:10 MirahezeLSBot: [void@puppet181] Upgraded packages on ns1: bind9-host, bind9-dnsutils, and bind9-libs
* 04:10 MirahezeLSBot: [void@puppet181] Upgraded packages on mw183: bind9-host, bind9-dnsutils, and bind9-libs
* 04:10 MirahezeLSBot: [void@puppet181] Upgraded packages on mw192: bind9-host, bind9-dnsutils, and bind9-libs
* 04:09 MirahezeLSBot: [void@puppet181] Upgraded packages on mw173: bind9-host, bind9-dnsutils, and bind9-libs
* 04:09 MirahezeLSBot: [void@puppet181] Upgraded packages on mw182: bind9-host, bind9-dnsutils, and bind9-libs
* 04:09 MirahezeLSBot: [void@puppet181] Upgraded packages on mw193: bind9-host, bind9-dnsutils, and bind9-libs
* 04:08 MirahezeLSBot: [void@puppet181] Upgraded packages on mw181: bind9-host, bind9-dnsutils, and bind9-libs
* 04:08 MirahezeLSBot: [void@puppet181] Upgraded packages on mw191: bind9-host, bind9-dnsutils, and bind9-libs
* 04:08 MirahezeLSBot: [void@puppet181] Upgraded packages on mw161: bind9-host, bind9-dnsutils, and bind9-libs
* 04:08 MirahezeLSBot: [void@puppet181] Upgraded packages on mw172: bind9-host, bind9-dnsutils, and bind9-libs
* 04:07 MirahezeLSBot: [void@puppet181] Upgraded packages on mw163: bind9-host, bind9-dnsutils, and bind9-libs
* 04:07 MirahezeLSBot: [void@puppet181] Upgraded packages on mw171: bind9-host, bind9-dnsutils, and bind9-libs
* 04:07 MirahezeLSBot: [void@puppet181] Upgraded packages on mw162: bind9-host, bind9-dnsutils, and bind9-libs
* 04:06 MirahezeLSBot: [void@puppet181] Upgraded packages on mon181: bind9-host, bind9-dnsutils, and bind9-libs
* 04:06 MirahezeLSBot: [void@puppet181] Upgraded packages on mw153: bind9-host, bind9-dnsutils, and bind9-libs
* 04:06 MirahezeLSBot: [void@puppet181] Upgraded packages on mw152: bind9-host, bind9-dnsutils, and bind9-libs
* 04:06 MirahezeLSBot: [void@puppet181] Upgraded packages on mw151: bind9-host, bind9-dnsutils, and bind9-libs
* 04:05 MirahezeLSBot: [void@puppet181] Upgraded packages on mem191: bind9-host, bind9-dnsutils, and bind9-libs
* 04:05 MirahezeLSBot: [void@puppet181] Upgraded packages on mem201: bind9-host, bind9-dnsutils, and bind9-libs
* 04:05 MirahezeLSBot: [void@puppet181] Upgraded packages on llm191: bind9-host, bind9-dnsutils, and bind9-libs
* 04:05 MirahezeLSBot: [void@puppet181] Upgraded packages on kafka182: bind9-host, bind9-dnsutils, and bind9-libs
* 04:04 MirahezeLSBot: [void@puppet181] Upgraded packages on mem151: bind9-host, bind9-dnsutils, and bind9-libs
* 04:04 MirahezeLSBot: [void@puppet181] Upgraded packages on mem161: bind9-host, bind9-dnsutils, and bind9-libs
* 04:04 MirahezeLSBot: [void@puppet181] Upgraded packages on matomo151: bind9-host, bind9-dnsutils, and bind9-libs
* 04:04 MirahezeLSBot: [void@puppet181] Upgraded packages on mattermost2: bind9-host, bind9-dnsutils, and bind9-libs
* 04:03 MirahezeLSBot: [void@puppet181] Upgraded packages on ldap171: bind9-host, bind9-dnsutils, and bind9-libs
* 04:03 MirahezeLSBot: [void@puppet181] Upgraded packages on graylog161: bind9-host, bind9-dnsutils, and bind9-libs
* 04:03 MirahezeLSBot: [void@puppet181] Upgraded packages on cp201: bind9-host, bind9-dnsutils, and bind9-libs
* 04:03 MirahezeLSBot: [void@puppet181] Upgraded packages on eventgate182: bind9-host, bind9-dnsutils, and bind9-libs
* 04:02 MirahezeLSBot: [void@puppet181] Upgraded packages on cp191: bind9-host, bind9-dnsutils, and bind9-libs
* 04:02 MirahezeLSBot: [void@puppet181] Upgraded packages on db201: bind9-host, bind9-dnsutils, and bind9-libs
* 04:02 MirahezeLSBot: [void@puppet181] Upgraded packages on db182: bind9-host, bind9-dnsutils, and bind9-libs
* 04:02 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud20: bind9-host, bind9-dnsutils, and bind9-libs
* 04:01 MirahezeLSBot: [void@puppet181] Upgraded packages on db192: bind9-host, bind9-dnsutils, and bind9-libs
* 04:01 MirahezeLSBot: [void@puppet181] Upgraded packages on db181: bind9-host, bind9-dnsutils, and bind9-libs
* 04:01 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud19: bind9-host, bind9-dnsutils, and bind9-libs
* 04:01 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud16: bind9-host, bind9-dnsutils, and bind9-libs
* 04:00 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud18: bind9-host, bind9-dnsutils, and bind9-libs
* 04:00 MirahezeLSBot: [void@puppet181] Upgraded packages on cp171: bind9-host, bind9-dnsutils, and bind9-libs
* 04:00 MirahezeLSBot: [void@puppet181] Upgraded packages on changeprop202: bind9-host, bind9-dnsutils, and bind9-libs
* 04:00 MirahezeLSBot: [void@puppet181] Upgraded packages on bast181: bind9-host, bind9-dnsutils, and bind9-libs
* 03:59 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud17: bind9-host, bind9-dnsutils, and bind9-libs
* 03:59 MirahezeLSBot: [void@puppet181] Upgraded packages on db161: bind9-host, bind9-dnsutils, and bind9-libs
* 03:59 MirahezeLSBot: [void@puppet181] Upgraded packages on db151: bind9-host, bind9-dnsutils, and bind9-libs
* 03:59 MirahezeLSBot: [void@puppet181] Upgraded packages on db172: bind9-host, bind9-dnsutils, and bind9-libs
* 03:59 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud15: bind9-host, bind9-dnsutils, and bind9-libs
* 03:58 MirahezeLSBot: [void@puppet181] Upgraded packages on db171: bind9-host, bind9-dnsutils, and bind9-libs
* 03:58 MirahezeLSBot: [void@puppet181] Upgraded packages on cp161: bind9-host, bind9-dnsutils, and bind9-libs
* 03:58 MirahezeLSBot: [void@puppet181] Upgraded packages on bots171: bind9-host, bind9-dnsutils, and bind9-libs
* 03:58 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud21: bind9-host, bind9-dnsutils, and bind9-libs
* 03:57 MirahezeLSBot: [void@puppet181] Upgraded packages on bast161: bind9-host, bind9-dnsutils, and bind9-libs
* 03:06 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php /srv/mediawiki/1.45/maintenance/initSiteStats.php --wiki=driveworldwiki --update (END - exit=0)
* 03:06 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php /srv/mediawiki/1.45/maintenance/rebuildall.php --wiki=driveworldwiki (END - exit=0)
* 02:57 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php /srv/mediawiki/1.45/maintenance/rebuildall.php --wiki=driveworldwiki (START)
* 02:57 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php /srv/mediawiki/1.45/maintenance/importDump.php --wiki=driveworldwiki dump.xml --no-updates (END - exit=0)
* 02:40 MirahezeLSBot: [skye@mwtask181] finished deploy of {'config': True} to all - SUCCESS in 23s
* 02:39 MirahezeLSBot: [skye@mwtask181] starting deploy of {'config': True} to all
* 02:36 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php /srv/mediawiki/1.45/maintenance/importDump.php --wiki=driveworldwiki dump.xml --no-updates (START)

## 2026-03-27 

* 22:44 Universal Omega: run bucketuser grants on db181
* 22:44 Universal Omega: run bucketuser grants on db171
* 22:43 Universal Omega: run bucketuser grants on db161
* 22:42 Universal Omega: run bucketuser grants on db151
* 21:37 MirahezeLSBot: [wwr@mwtask181] finished deploy of {'config': True} to all - SUCCESS in 23s
* 21:37 MirahezeLSBot: [wwr@mwtask181] starting deploy of {'config': True} to all
* 21:00 MirahezeLSBot: [wwr@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 21:00 MirahezeLSBot: [wwr@test151] starting deploy of {'config': True} to test151
* 20:48 MirahezeLSBot: [wwr@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 20:48 MirahezeLSBot: [wwr@test151] starting deploy of {'config': True} to test151
* 20:26 Universal Omega: run bucketuser grants on db172
* 20:23 MirahezeLSBot: [macfan@mwtask181] finished deploy of {'pull': 'config', 'config': True, 'force': True} to all - SUCCESS in 19s
* 20:23 MirahezeLSBot: [macfan@mwtask181] starting deploy of {'pull': 'config', 'config': True, 'force': True} to all
* 20:20 MirahezeLSBot: [macfan@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 20:20 MirahezeLSBot: [macfan@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 20:01 Universal Omega: add ldap groups for wwr
* 11:38 MirahezeLSBot: [wwr@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 11:38 MirahezeLSBot: [wwr@test151] starting deploy of {'config': True} to test151
* 11:37 MirahezeLSBot: [wwr@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 11:37 MirahezeLSBot: [wwr@test151] starting deploy of {'config': True} to test151
* 11:36 MirahezeLSBot: [wwr@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 11:36 MirahezeLSBot: [wwr@test151] starting deploy of {'config': True} to test151
* 11:35 MirahezeLSBot: [wwr@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 11:35 MirahezeLSBot: [wwr@test151] starting deploy of {'config': True} to test151

## 2026-03-26 

* 23:04 MirahezeLSBot: [somerandomdeveloper@mwtask181] finished deploy of {'versions': '1.45', 'upgrade_skins': 'Monaco'} to all - SUCCESS in 24s
* 23:03 MirahezeLSBot: [somerandomdeveloper@mwtask181] starting deploy of {'versions': '1.45', 'upgrade_skins': 'Monaco'} to all
* 23:02 MirahezeLSBot: [somerandomdeveloper@test151] finished deploy of {'versions': '1.45', 'upgrade_skins': 'Monaco'} to test151 - SUCCESS in 0s
* 23:02 MirahezeLSBot: [somerandomdeveloper@test151] starting deploy of {'versions': '1.45', 'upgrade_skins': 'Monaco'} to test151
* 22:47 MirahezeLSBot: [wwr@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 22:47 MirahezeLSBot: [wwr@test151] starting deploy of {'config': True} to test151
* 22:29 MirahezeLSBot: [wwr@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 22:29 MirahezeLSBot: [wwr@test151] starting deploy of {'config': True} to test151
* 21:50 MirahezeLSBot: [wwr@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 21:50 MirahezeLSBot: [wwr@test151] starting deploy of {'config': True} to test151
* 21:42 MirahezeLSBot: [wwr@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 21:42 MirahezeLSBot: [wwr@test151] starting deploy of {'config': True} to test151
* 21:41 MirahezeLSBot: [wwr@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 21:41 MirahezeLSBot: [wwr@test151] starting deploy of {'config': True} to test151
* 21:04 Universal Omega: add bucketuser passwords to private puppet
* 20:47 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php /srv/mediawiki/1.45/maintenance/importDump.php --wiki=animatorvsanimationwiki --username-prefix=wikia:animatorvsanimation /home/reception/animatorvsanimation_pages_full.xml (END - exit=0)
* 19:12 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php /srv/mediawiki/1.45/maintenance/importDump.php --wiki=animatorvsanimationwiki --username-prefix=wikia:animatorvsanimation /home/reception/animatorvsanimation_pages_full.xml (START)
* 19:04 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RenameDatabase --wiki=loginwiki --rename --old=rbpwiki --new=resetrblxwiki --user=Reception123 (END - exit=0)
* 19:02 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RenameDatabase --wiki=loginwiki --rename --old=lewthumbriawiki --new=montgriswiki --user=Reception123 (END - exit=0)
* 01:51 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php Bucket:CreateInitialSchemaForBucketIssues --wiki=buckettestwikibeta (END - exit=0)
* 01:44 MirahezeLSBot: [skye@test151] finished deploy of {'versions': '1.45', 'upgrade_extensions': 'Bucket'} to test151 - SUCCESS in 0s
* 01:44 MirahezeLSBot: [skye@test151] starting deploy of {'versions': '1.45', 'upgrade_extensions': 'Bucket'} to test151
* 01:40 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php Bucket:CreateInitialSchemaForBucketIssues --wiki=buckettestwikibeta (END - exit=256)
* 01:38 MirahezeLSBot: [wwr@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 01:38 MirahezeLSBot: [wwr@test151] starting deploy of {'config': True} to test151
* 01:11 MirahezeLSBot: [somerandomdeveloper@mwtask181] finished deploy of {'versions': '1.45', 'upgrade_extensions': 'Bucket'} to all - SUCCESS in 25s
* 01:11 MirahezeLSBot: [somerandomdeveloper@mwtask181] starting deploy of {'versions': '1.45', 'upgrade_extensions': 'Bucket'} to all
* 01:08 MirahezeLSBot: [somerandomdeveloper@test151] DEPLOY ABORTED: Non-Zero Exit Code in prep, see output.
* 01:08 MirahezeLSBot: [somerandomdeveloper@test151] starting deploy of {'versions': '1.45', 'upgrade_extensions': 'Bucket'} to test151
* 00:06 MirahezeLSBot: [oa@mwtask181] finished deploy of {'versions': '1.45', 'upgrade_extensions': 'TableProgressTracking'} to all - SUCCESS in 24s
* 00:06 MirahezeLSBot: [oa@mwtask181] starting deploy of {'versions': '1.45', 'upgrade_extensions': 'TableProgressTracking'} to all

## 2026-03-25 

* 21:49 MirahezeLSBot: [petramagna@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php cleanupTitles --wiki=yotunewiki (END - exit=0)
* 21:30 MirahezeLSBot: [petramagna@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php deleteBatch --wiki=yotunewiki --u=PetraMagna_(Miraheze) --r='Try delete inaccessible page in T15123' pages.txt (END - exit=512)
* 21:30 MirahezeLSBot: [petramagna@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php deleteBatch --wiki=yotunewiki --u=PetraMagna_(Miraheze) --r='Try delete inaccessible page in T15123' pages.txt (START)
* 21:29 MirahezeLSBot: [petramagna@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php deleteBatch --wiki=yotunewiki --u=PetraMagna_(Miraheze) --r=Try delete inaccessible page in T15123 pages.txt (END - exit=512)
* 21:29 MirahezeLSBot: [petramagna@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php deleteBatch --wiki=yotunewiki --u=PetraMagna_(Miraheze) --r=Try delete inaccessible page in T15123 pages.txt (START)
* 21:12 MirahezeLSBot: [universalomega@mwtask181] finished deploy of {'versions': '1.45', 'upgrade_extensions': 'MirahezeMagic'} to all - SUCCESS in 0s
* 21:12 MirahezeLSBot: [universalomega@mwtask181] starting deploy of {'versions': '1.45', 'upgrade_extensions': 'MirahezeMagic'} to all
* 21:06 MirahezeLSBot: [petramagna@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:ResetWiki --wiki=loginwiki --dbname=doorswiki --requester=Crystalite13 (END - exit=0)
* 21:01 MirahezeLSBot: [petramagna@test151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:ResetWiki --wiki=loginwikibeta --dbname=loadouttest5wikibeta --requester=PetraMagna (END - exit=0)
* 20:51 MirahezeLSBot: [universalomega@mwtask181] finished deploy of {'versions': '1.45', 'upgrade_extensions': 'MirahezeMagic'} to all - SUCCESS in 25s
* 20:50 MirahezeLSBot: [universalomega@mwtask181] starting deploy of {'versions': '1.45', 'upgrade_extensions': 'MirahezeMagic'} to all

## 2026-03-24 

* 23:19 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php CreateWiki:DeleteWiki --wiki=loginwikibeta --delete --deletewiki wwrtest5wikibeta (END - exit=0)
* 06:07 MirahezeLSBot: [petramagna@mwtask181] finished deploy of {'versions': '1.45', 'upgrade_extensions': 'TableProgressTracking'} to all - SUCCESS in 24s
* 06:06 MirahezeLSBot: [petramagna@mwtask181] starting deploy of {'versions': '1.45', 'upgrade_extensions': 'TableProgressTracking'} to all
* 06:03 MirahezeLSBot: [petramagna@test151] finished deploy of {'versions': '1.45', 'upgrade_extensions': 'TableProgressTracking'} to test151 - SUCCESS in 0s
* 06:03 MirahezeLSBot: [petramagna@test151] starting deploy of {'versions': '1.45', 'upgrade_extensions': 'TableProgressTracking'} to test151

## 2026-03-23 

* 20:57 MirahezeLSBot: [void@puppet181] Upgraded packages on test151: strongswan-starter, libcharon-extauth-plugins, libcharon-extra-plugins, strongswan-pki, strongswan-libcharon, strongswan-charon, libstrongswan, and libstrongswan-standard-plugins
* 19:19 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php deleteBatch --wiki=wwrtest3wikibeta b.txt --u TheWWRNerdGuy --r Testing deletion (END - exit=0)
* 19:19 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php deleteBatch --wiki=wwrtest3wikibeta b.txt --u TheWWRNerdGuy --r Testing deletion (START)
* 19:19 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php deleteBatch --wiki=wwrtest3wikibeta b.txt --u TheWWRNerdGuy --r Testing deletion (END - exit=0)
* 19:19 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php deleteBatch --wiki=wwrtest3wikibeta b.txt --u TheWWRNerdGuy --r Testing deletion (START)
* 19:17 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php deleteBatch --wiki=wwrtest3wikibeta b.txt --u TheWWRNerdGuy --r Testing deletion (END - exit=0)
* 19:17 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php deleteBatch --wiki=wwrtest3wikibeta b.txt --u TheWWRNerdGuy --r Testing deletion (START)
* 10:30 @posix_memalign: sudo -u www-data foreachwikiindblist /srv/mediawiki/cache/embedvideo.php /srv/mediawiki/1.45/extensions/EmbedVideo/maintenance/BackfillLocalMediaMetadata.php 2>&1 | tee -a logs.txt
* 10:18 MirahezeLSBot: [petramagna@mwtask181] finished deploy of {'versions': '1.45', 'upgrade_extensions': 'EmbedVideo'} to all - SUCCESS in 25s
* 10:17 MirahezeLSBot: [petramagna@mwtask181] starting deploy of {'versions': '1.45', 'upgrade_extensions': 'EmbedVideo'} to all
* 10:04 MirahezeLSBot: [petramagna@test151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php EmbedVideo:BackfillLocalMediaMetadata --wiki=loadouttest5wikibeta (END - exit=0)
* 09:59 MirahezeLSBot: [petramagna@test151] finished deploy of {'versions': '1.45', 'upgrade_extensions': 'EmbedVideo'} to test151 - SUCCESS in 1s
* 09:59 MirahezeLSBot: [petramagna@test151] starting deploy of {'versions': '1.45', 'upgrade_extensions': 'EmbedVideo'} to test151

## 2026-03-22 

* 23:12 MirahezeLSBot: [petramagna@test151] finished deploy of {'folders': '1.45/extensions/CreateWikiLoadout'} to test151 - SUCCESS in 0s
* 23:12 MirahezeLSBot: [petramagna@test151] starting deploy of {'folders': '1.45/extensions/CreateWikiLoadout'} to test151
* 22:19 MirahezeLSBot: [skye@mwtask181] finished deploy of {'versions': '1.45', 'upgrade_extensions': 'PdfHandler'} to all - SUCCESS in 25s
* 22:19 MirahezeLSBot: [skye@mwtask181] starting deploy of {'versions': '1.45', 'upgrade_extensions': 'PdfHandler'} to all
* 21:56 MirahezeLSBot: [petramagna@test151] finished deploy of {'folders': '1.45/extensions/CreateWikiLoadout'} to test151 - SUCCESS in 0s
* 21:56 MirahezeLSBot: [petramagna@test151] starting deploy of {'folders': '1.45/extensions/CreateWikiLoadout'} to test151
* 21:12 MirahezeLSBot: [wwr@test151] finished deploy of {'folders': '1.45/extensions/PdfHandler'} to test151 - SUCCESS in 0s
* 21:12 MirahezeLSBot: [wwr@test151] starting deploy of {'folders': '1.45/extensions/PdfHandler'} to test151
* 21:07 MirahezeLSBot: [wwr@test151] DEPLOY ABORTED: Non-Zero Exit Code in prep, see output.
* 21:07 MirahezeLSBot: [wwr@test151] starting deploy of {'versions': '1.45', 'upgrade_extensions': 'PdfHandler'} to test151
* 20:54 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RenameDatabase --wiki=loginwiki --rename --old=craighcraftwiki --new=raveriswiki --user=Reception123 (END - exit=0)
* 20:41 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RenameDatabase --wiki=loginwiki --rename --old=paranormasightfileswiki --new=paranormasightwiki --user=Reception123 (END - exit=256)
* 20:27 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RenameDatabase --wiki=loginwiki --rename --old=sithempirewiki --new=jediorderwiki --user=Reception123 (END - exit=0)
* 20:16 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RenameDatabase --wiki=loginwiki --rename --old=quicksilvervaultwiki --new=skylanderswikiwiki --user=Reception123 (END - exit=0)
* 11:02 MirahezeLSBot: [blankeclair@mwtask151] Finished import for jonathanbreewiki (XML: None; Images: JBW) (END - exit=0)
* 11:02 MirahezeLSBot: [blankeclair@mwtask151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php initSiteStats --wiki=jonathanbreewiki --update (END - exit=0)
* 11:02 MirahezeLSBot: [blankeclair@mwtask151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php initSiteStats --wiki=jonathanbreewiki --update (START)
* 11:02 MirahezeLSBot: [blankeclair@mwtask151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=jonathanbreewiki --sleep=1 '--comment=Importing images from [https://jonathanbree.fandom.com](https://jonathanbree.fandom.com) ([T15114](https://meta.miraheze.org/wiki/phorge:T15114))' -- JBW (END - exit=0)
* 11:02 MirahezeLSBot: [blankeclair@mwtask151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=jonathanbreewiki --sleep=1 '--comment=Importing images from [https://jonathanbree.fandom.com](https://jonathanbree.fandom.com) ([T15114](https://meta.miraheze.org/wiki/phorge:T15114))' -- JBW (START)
* 11:02 MirahezeLSBot: [blankeclair@mwtask151] Starting import for jonathanbreewiki (XML: None; Images: JBW) (START)
* 11:02 MirahezeLSBot: [blankeclair@mwtask151] Finished import for jonathanbreewiki (XML: None; Images: JBW) (END - exit=1)
* 11:02 MirahezeLSBot: [blankeclair@mwtask151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=jonathanbreewiki --sleep=1 '--comment=Importing images from [https://jonathanbree.fandom.com](https://jonathanbree.fandom.com) ([T15114](https://meta.miraheze.org/wiki/phorge:T15114))' -- JBW (END - exit=1)
* 11:01 MirahezeLSBot: [blankeclair@mwtask151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=jonathanbreewiki --sleep=1 '--comment=Importing images from [https://jonathanbree.fandom.com](https://jonathanbree.fandom.com) ([T15114](https://meta.miraheze.org/wiki/phorge:T15114))' -- JBW (START)
* 11:01 MirahezeLSBot: [blankeclair@mwtask151] Starting import for jonathanbreewiki (XML: None; Images: JBW) (START)
* 11:01 MirahezeLSBot: [blankeclair@mwtask151] Finished import for jonathanbreewiki (XML: None; Images: JBW) (END - exit=1)
* 11:01 MirahezeLSBot: [blankeclair@mwtask151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=jonathanbreewiki --sleep=1 '--comment=Importing images from [https://jonathanbree.fandom.com](https://jonathanbree.fandom.com) ([T15114](https://meta.miraheze.org/wiki/phorge:T15114))' -- JBW (END - exit=1)
* 10:59 MirahezeLSBot: [blankeclair@mwtask151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=jonathanbreewiki --sleep=1 '--comment=Importing images from [https://jonathanbree.fandom.com](https://jonathanbree.fandom.com) ([T15114](https://meta.miraheze.org/wiki/phorge:T15114))' -- JBW (START)
* 10:59 MirahezeLSBot: [blankeclair@mwtask151] Starting import for jonathanbreewiki (XML: None; Images: JBW) (START)
* 10:59 MirahezeLSBot: [blankeclair@mwtask151] Finished import for jonathanbreewiki (XML: None; Images: JBW) (END - exit=1)
* 10:59 MirahezeLSBot: [blankeclair@mwtask151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=jonathanbreewiki --sleep=1 '--comment=Importing images from [https://jonathanbree.fandom.com](https://jonathanbree.fandom.com) ([T15114](https://meta.miraheze.org/wiki/phorge:T15114))' -- JBW (END - exit=1)
* 10:58 MirahezeLSBot: [blankeclair@mwtask151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=jonathanbreewiki --sleep=1 '--comment=Importing images from [https://jonathanbree.fandom.com](https://jonathanbree.fandom.com) ([T15114](https://meta.miraheze.org/wiki/phorge:T15114))' -- JBW (START)
* 10:58 MirahezeLSBot: [blankeclair@mwtask151] Starting import for jonathanbreewiki (XML: None; Images: JBW) (START)
* 10:58 MirahezeLSBot: [blankeclair@mwtask151] Finished import for jonathanbreewiki (XML: None; Images: JBW) (END - exit=1)
* 10:58 MirahezeLSBot: [blankeclair@mwtask151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=jonathanbreewiki --sleep=1 '--comment=Importing images from [https://jonathanbree.fandom.com](https://jonathanbree.fandom.com) ([T15114](https://meta.miraheze.org/wiki/phorge:T15114))' -- JBW (END - exit=1)
* 10:58 MirahezeLSBot: [blankeclair@mwtask151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=jonathanbreewiki --sleep=1 '--comment=Importing images from [https://jonathanbree.fandom.com](https://jonathanbree.fandom.com) ([T15114](https://meta.miraheze.org/wiki/phorge:T15114))' -- JBW (START)
* 10:58 MirahezeLSBot: [blankeclair@mwtask151] Starting import for jonathanbreewiki (XML: None; Images: JBW) (START)
* 10:57 MirahezeLSBot: [blankeclair@mwtask151] Finished import for jonathanbreewiki (XML: None; Images: JBW) (END - exit=1)
* 10:57 MirahezeLSBot: [blankeclair@mwtask151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=jonathanbreewiki --sleep=1 '--comment=Importing images from [https://jonathanbree.fandom.com](https://jonathanbree.fandom.com) ([T15114](https://meta.miraheze.org/wiki/phorge:T15114))' -- JBW (END - exit=1)
* 10:55 MirahezeLSBot: [blankeclair@mwtask151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=jonathanbreewiki --sleep=1 '--comment=Importing images from [https://jonathanbree.fandom.com](https://jonathanbree.fandom.com) ([T15114](https://meta.miraheze.org/wiki/phorge:T15114))' -- JBW (START)
* 10:55 MirahezeLSBot: [blankeclair@mwtask151] Starting import for jonathanbreewiki (XML: None; Images: JBW) (START)
* 10:54 MirahezeLSBot: [blankeclair@mwtask151] Finished import for jonathanbreewiki (XML: None; Images: JBW) (END - exit=1)
* 10:54 MirahezeLSBot: [blankeclair@mwtask151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=jonathanbreewiki --sleep=1 '--comment=Importing images from [https://jonathanbree.fandom.com](https://jonathanbree.fandom.com) ([T15114](https://meta.miraheze.org/wiki/phorge:T15114))' -- JBW (END - exit=1)
* 10:54 MirahezeLSBot: [blankeclair@mwtask151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=jonathanbreewiki --sleep=1 '--comment=Importing images from [https://jonathanbree.fandom.com](https://jonathanbree.fandom.com) ([T15114](https://meta.miraheze.org/wiki/phorge:T15114))' -- JBW (START)
* 10:54 MirahezeLSBot: [blankeclair@mwtask151] Starting import for jonathanbreewiki (XML: None; Images: JBW) (START)
* 10:54 MirahezeLSBot: [blankeclair@mwtask151] Finished import for jonathanbreewiki (XML: None; Images: JBW) (END - exit=1)
* 10:54 MirahezeLSBot: [blankeclair@mwtask151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=jonathanbreewiki --sleep=1 '--comment=Importing images from [https://jonathanbree.fandom.com](https://jonathanbree.fandom.com) ([T15114](https://meta.miraheze.org/wiki/phorge:T15114))' -- JBW (END - exit=1)
* 10:53 MirahezeLSBot: [blankeclair@mwtask151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=jonathanbreewiki --sleep=1 '--comment=Importing images from [https://jonathanbree.fandom.com](https://jonathanbree.fandom.com) ([T15114](https://meta.miraheze.org/wiki/phorge:T15114))' -- JBW (START)
* 10:53 MirahezeLSBot: [blankeclair@mwtask151] Starting import for jonathanbreewiki (XML: None; Images: JBW) (START)
* 10:52 MirahezeLSBot: [blankeclair@mwtask151] Finished import for jonathanbreewiki (XML: None; Images: JBW) (END - exit=1)
* 10:52 MirahezeLSBot: [blankeclair@mwtask151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=jonathanbreewiki --sleep=1 '--comment=Importing images from [https://jonathanbree.fandom.com](https://jonathanbree.fandom.com) ([T15114](https://meta.miraheze.org/wiki/phorge:T15114))' -- JBW (END - exit=1)
* 10:51 MirahezeLSBot: [blankeclair@mwtask151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=jonathanbreewiki --sleep=1 '--comment=Importing images from [https://jonathanbree.fandom.com](https://jonathanbree.fandom.com) ([T15114](https://meta.miraheze.org/wiki/phorge:T15114))' -- JBW (START)
* 10:51 MirahezeLSBot: [blankeclair@mwtask151] Starting import for jonathanbreewiki (XML: None; Images: JBW) (START)
* 10:51 MirahezeLSBot: [blankeclair@mwtask151] Finished import for jonathanbreewiki (XML: None; Images: JBW) (END - exit=1)
* 10:51 MirahezeLSBot: [blankeclair@mwtask151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=jonathanbreewiki --sleep=1 '--comment=Importing images from [https://jonathanbree.fandom.com](https://jonathanbree.fandom.com) ([T15114](https://meta.miraheze.org/wiki/phorge:T15114))' -- JBW (END - exit=1)
* 10:47 MirahezeLSBot: [blankeclair@mwtask151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=jonathanbreewiki --sleep=1 '--comment=Importing images from [https://jonathanbree.fandom.com](https://jonathanbree.fandom.com) ([T15114](https://meta.miraheze.org/wiki/phorge:T15114))' -- JBW (START)
* 10:47 MirahezeLSBot: [blankeclair@mwtask151] Starting import for jonathanbreewiki (XML: None; Images: JBW) (START)
* 10:47 MirahezeLSBot: [blankeclair@mwtask151] Finished import for jonathanbreewiki (XML: None; Images: JBW) (END - exit=1)
* 10:47 MirahezeLSBot: [blankeclair@mwtask151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=jonathanbreewiki --sleep=1 '--comment=Importing images from [https://jonathanbree.fandom.com](https://jonathanbree.fandom.com) ([T15114](https://meta.miraheze.org/wiki/phorge:T15114))' -- JBW (END - exit=1)
* 10:46 MirahezeLSBot: [blankeclair@mwtask151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=jonathanbreewiki --sleep=1 '--comment=Importing images from [https://jonathanbree.fandom.com](https://jonathanbree.fandom.com) ([T15114](https://meta.miraheze.org/wiki/phorge:T15114))' -- JBW (START)
* 10:46 MirahezeLSBot: [blankeclair@mwtask151] Starting import for jonathanbreewiki (XML: None; Images: JBW) (START)
* 10:46 MirahezeLSBot: [blankeclair@mwtask151] Finished import for jonathanbreewiki (XML: None; Images: JBW) (END - exit=1)
* 10:46 MirahezeLSBot: [blankeclair@mwtask151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=jonathanbreewiki --sleep=1 '--comment=Importing images from [https://jonathanbree.fandom.com](https://jonathanbree.fandom.com) ([T15114](https://meta.miraheze.org/wiki/phorge:T15114))' -- JBW (END - exit=1)
* 10:46 MirahezeLSBot: [blankeclair@mwtask151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=jonathanbreewiki --sleep=1 '--comment=Importing images from [https://jonathanbree.fandom.com](https://jonathanbree.fandom.com) ([T15114](https://meta.miraheze.org/wiki/phorge:T15114))' -- JBW (START)
* 10:46 MirahezeLSBot: [blankeclair@mwtask151] Starting import for jonathanbreewiki (XML: None; Images: JBW) (START)
* 10:45 MirahezeLSBot: [blankeclair@mwtask151] Finished import for jonathanbreewiki (XML: None; Images: JBW) (END - exit=1)
* 10:45 MirahezeLSBot: [blankeclair@mwtask151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=jonathanbreewiki --sleep=1 '--comment=Importing images from [https://jonathanbree.fandom.com](https://jonathanbree.fandom.com) ([T15114](https://meta.miraheze.org/wiki/phorge:T15114))' -- JBW (END - exit=1)
* 10:43 MirahezeLSBot: [blankeclair@mwtask151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=jonathanbreewiki --sleep=1 '--comment=Importing images from [https://jonathanbree.fandom.com](https://jonathanbree.fandom.com) ([T15114](https://meta.miraheze.org/wiki/phorge:T15114))' -- JBW (START)
* 10:43 MirahezeLSBot: [blankeclair@mwtask151] Starting import for jonathanbreewiki (XML: None; Images: JBW) (START)
* 10:42 MirahezeLSBot: [blankeclair@mwtask151] Finished import for jonathanbreewiki (XML: None; Images: JBW) (END - exit=1)
* 10:42 MirahezeLSBot: [blankeclair@mwtask151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=jonathanbreewiki --sleep=1 '--comment=Importing images from [https://jonathanbree.fandom.com](https://jonathanbree.fandom.com) ([T15114](https://meta.miraheze.org/wiki/phorge:T15114))' -- JBW (END - exit=1)
* 10:40 MirahezeLSBot: [blankeclair@mwtask151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=jonathanbreewiki --sleep=1 '--comment=Importing images from [https://jonathanbree.fandom.com](https://jonathanbree.fandom.com) ([T15114](https://meta.miraheze.org/wiki/phorge:T15114))' -- JBW (START)
* 10:40 MirahezeLSBot: [blankeclair@mwtask151] Starting import for jonathanbreewiki (XML: None; Images: JBW) (START)
* 10:39 MirahezeLSBot: [blankeclair@mwtask151] Finished import for jonathanbreewiki (XML: None; Images: JBW) (END - exit=1)
* 10:39 MirahezeLSBot: [blankeclair@mwtask151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=jonathanbreewiki --sleep=1 '--comment=Importing images from [https://jonathanbree.fandom.com](https://jonathanbree.fandom.com) ([T15114](https://meta.miraheze.org/wiki/phorge:T15114))' -- JBW (END - exit=1)
* 10:39 MirahezeLSBot: [blankeclair@mwtask151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=jonathanbreewiki --sleep=1 '--comment=Importing images from [https://jonathanbree.fandom.com](https://jonathanbree.fandom.com) ([T15114](https://meta.miraheze.org/wiki/phorge:T15114))' -- JBW (START)
* 10:39 MirahezeLSBot: [blankeclair@mwtask151] Starting import for jonathanbreewiki (XML: None; Images: JBW) (START)
* 10:29 MirahezeLSBot: [blankeclair@mwtask151] Finished import for jonathanbreewiki (XML: None; Images: JBW) (END - exit=1)
* 10:29 MirahezeLSBot: [blankeclair@mwtask151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=jonathanbreewiki --sleep=1 '--comment=Importing images from [https://jonathanbree.fandom.com](https://jonathanbree.fandom.com) ([T15114](https://meta.miraheze.org/wiki/phorge:T15114))' -- JBW (END - exit=1)
* 10:28 MirahezeLSBot: [blankeclair@mwtask151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=jonathanbreewiki --sleep=1 '--comment=Importing images from [https://jonathanbree.fandom.com](https://jonathanbree.fandom.com) ([T15114](https://meta.miraheze.org/wiki/phorge:T15114))' -- JBW (START)
* 10:28 MirahezeLSBot: [blankeclair@mwtask151] Starting import for jonathanbreewiki (XML: None; Images: JBW) (START)
* 10:28 MirahezeLSBot: [blankeclair@mwtask151] Finished import for jonathanbreewiki (XML: None; Images: JBW) (END - exit=1)
* 10:28 MirahezeLSBot: [blankeclair@mwtask151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=jonathanbreewiki --sleep=1 '--comment=Importing images from [https://jonathanbree.fandom.com](https://jonathanbree.fandom.com) ([T15114](https://meta.miraheze.org/wiki/phorge:T15114))' -- JBW (END - exit=1)
* 10:27 MirahezeLSBot: [blankeclair@mwtask151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=jonathanbreewiki --sleep=1 '--comment=Importing images from [https://jonathanbree.fandom.com](https://jonathanbree.fandom.com) ([T15114](https://meta.miraheze.org/wiki/phorge:T15114))' -- JBW (START)
* 10:27 MirahezeLSBot: [blankeclair@mwtask151] Starting import for jonathanbreewiki (XML: None; Images: JBW) (START)
* 10:27 MirahezeLSBot: [blankeclair@mwtask151] Finished import for jonathanbreewiki (XML: None; Images: JBW) (END - exit=1)
* 10:27 MirahezeLSBot: [blankeclair@mwtask151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=jonathanbreewiki --sleep=1 '--comment=Importing images from [https://jonathanbree.fandom.com](https://jonathanbree.fandom.com) (([phorge:T15114|T15114]])' -- JBW (END - exit=1)
* 10:25 MirahezeLSBot: [blankeclair@mwtask151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=jonathanbreewiki --sleep=1 '--comment=Importing images from [https://jonathanbree.fandom.com](https://jonathanbree.fandom.com) (([phorge:T15114|T15114]])' -- JBW (START)
* 10:25 MirahezeLSBot: [blankeclair@mwtask151] Starting import for jonathanbreewiki (XML: None; Images: JBW) (START)
* 10:24 MirahezeLSBot: [blankeclair@mwtask151] Finished import for jonathanbreewiki (XML: None; Images: JBW) (END - exit=1)
* 10:24 MirahezeLSBot: [blankeclair@mwtask151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=jonathanbreewiki --sleep=1 '--comment=Importing images from [https://jonathanbree.fandom.com](https://jonathanbree.fandom.com) (([phorge:T15114|T15114]])' -- JBW (END - exit=1)
* 10:24 MirahezeLSBot: [blankeclair@mwtask151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=jonathanbreewiki --sleep=1 '--comment=Importing images from [https://jonathanbree.fandom.com](https://jonathanbree.fandom.com) (([phorge:T15114|T15114]])' -- JBW (START)
* 10:24 MirahezeLSBot: [blankeclair@mwtask151] Starting import for jonathanbreewiki (XML: None; Images: JBW) (START)
* 10:23 MirahezeLSBot: [blankeclair@mwtask151] Finished import for jonathanbreewiki (XML: None; Images: JBW) (END - exit=1)
* 10:23 MirahezeLSBot: [blankeclair@mwtask151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=jonathanbreewiki --sleep=1 '--comment=Importing images from [https://jonathanbree.fandom.com](https://jonathanbree.fandom.com) (([phorge:T15114|T15114]])' -- JBW (END - exit=1)
* 10:21 MirahezeLSBot: [blankeclair@mwtask151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=jonathanbreewiki --sleep=1 '--comment=Importing images from [https://jonathanbree.fandom.com](https://jonathanbree.fandom.com) (([phorge:T15114|T15114]])' -- JBW (START)
* 10:21 MirahezeLSBot: [blankeclair@mwtask151] Starting import for jonathanbreewiki (XML: None; Images: JBW) (START)
* 10:20 MirahezeLSBot: [blankeclair@mwtask151] Finished import for jonathanbreewiki (XML: None; Images: JBW) (END - exit=1)
* 10:20 MirahezeLSBot: [blankeclair@mwtask151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=jonathanbreewiki --sleep=1 '--comment=Importing images from [https://jonathanbree.fandom.com](https://jonathanbree.fandom.com) (([phorge:T15114|T15114]])' -- JBW (END - exit=1)
* 10:17 MirahezeLSBot: [blankeclair@mwtask151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=jonathanbreewiki --sleep=1 '--comment=Importing images from [https://jonathanbree.fandom.com](https://jonathanbree.fandom.com) (([phorge:T15114|T15114]])' -- JBW (START)
* 10:17 MirahezeLSBot: [blankeclair@mwtask151] Starting import for jonathanbreewiki (XML: None; Images: JBW) (START)
* 10:16 MirahezeLSBot: [blankeclair@mwtask151] Finished import for jonathanbreewiki (XML: None; Images: JBW) (END - exit=1)
* 10:16 MirahezeLSBot: [blankeclair@mwtask151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=jonathanbreewiki --sleep=1 '--comment=Importing images from [https://jonathanbree.fandom.com](https://jonathanbree.fandom.com) (([phorge:T15114|T15114]])' -- JBW (END - exit=1)
* 10:15 MirahezeLSBot: [blankeclair@mwtask151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=jonathanbreewiki --sleep=1 '--comment=Importing images from [https://jonathanbree.fandom.com](https://jonathanbree.fandom.com) (([phorge:T15114|T15114]])' -- JBW (START)
* 10:15 MirahezeLSBot: [blankeclair@mwtask151] Starting import for jonathanbreewiki (XML: None; Images: JBW) (START)
* 10:14 MirahezeLSBot: [blankeclair@mwtask151] Finished import for jonathanbreewiki (XML: None; Images: JBW) (END - exit=1)
* 10:14 MirahezeLSBot: [blankeclair@mwtask151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=jonathanbreewiki --sleep=1 '--comment=Importing images from [https://jonathanbree.fandom.com](https://jonathanbree.fandom.com) (([phorge:T15114|T15114]])' -- JBW (END - exit=1)
* 10:12 MirahezeLSBot: [blankeclair@mwtask151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=jonathanbreewiki --sleep=1 '--comment=Importing images from [https://jonathanbree.fandom.com](https://jonathanbree.fandom.com) (([phorge:T15114|T15114]])' -- JBW (START)
* 10:12 MirahezeLSBot: [blankeclair@mwtask151] Starting import for jonathanbreewiki (XML: None; Images: JBW) (START)
* 10:12 MirahezeLSBot: [blankeclair@mwtask151] Finished import for jonathanbreewiki (XML: None; Images: JBW) (END - exit=1)
* 10:12 MirahezeLSBot: [blankeclair@mwtask151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=jonathanbreewiki --sleep=1 '--comment=Importing images from [https://jonathanbree.fandom.com](https://jonathanbree.fandom.com) (([phorge:T15114|T15114]])' -- JBW (END - exit=1)
* 10:10 MirahezeLSBot: [blankeclair@mwtask151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=jonathanbreewiki --sleep=1 '--comment=Importing images from [https://jonathanbree.fandom.com](https://jonathanbree.fandom.com) (([phorge:T15114|T15114]])' -- JBW (START)
* 10:09 MirahezeLSBot: [blankeclair@mwtask151] Starting import for jonathanbreewiki (XML: None; Images: JBW) (START)
* 10:02 MirahezeLSBot: [blankeclair@mwtask151] Finished import for jonathanbreewiki (XML: None; Images: JBW) (END - exit=1)
* 10:02 MirahezeLSBot: [blankeclair@mwtask151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=jonathanbreewiki --sleep=1 '--comment=Importing images from [https://jonathanbree.fandom.com](https://jonathanbree.fandom.com) (([phorge:T15114|T15114]])' -- JBW (END - exit=1)
* 10:02 MirahezeLSBot: [blankeclair@mwtask151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=jonathanbreewiki --sleep=1 '--comment=Importing images from [https://jonathanbree.fandom.com](https://jonathanbree.fandom.com) (([phorge:T15114|T15114]])' -- JBW (START)
* 10:02 MirahezeLSBot: [blankeclair@mwtask151] Starting import for jonathanbreewiki (XML: None; Images: JBW) (START)
* 10:01 MirahezeLSBot: [blankeclair@mwtask151] Finished import for jonathanbreewiki (XML: None; Images: JBW) (END - exit=1)
* 10:01 MirahezeLSBot: [blankeclair@mwtask151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=jonathanbreewiki --sleep=1 '--comment=Importing images from [https://jonathanbree.fandom.com](https://jonathanbree.fandom.com) (([phorge:T15114|T15114]])' -- JBW (END - exit=1)
* 09:58 MirahezeLSBot: [blankeclair@mwtask151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=jonathanbreewiki --sleep=1 '--comment=Importing images from [https://jonathanbree.fandom.com](https://jonathanbree.fandom.com) (([phorge:T15114|T15114]])' -- JBW (START)
* 09:57 MirahezeLSBot: [blankeclair@mwtask151] Starting import for jonathanbreewiki (XML: None; Images: JBW) (START)

## 2026-03-21 

* 23:10 MirahezeLSBot: [blankeclair@mwtask151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RenameDatabase --wiki=loginwiki --rename --old blinxcateaswiki --new blinxeaswiki --user 'BlankEclair (Miraheze)' (END - exit=0)
* 23:07 MirahezeLSBot: [blankeclair@mwtask151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RenameDatabase --wiki=loginwiki --rename --old tsgwiki --new tsgwikiwiki --user 'BlankEclair (Miraheze)' (END - exit=0)
* 23:03 MirahezeLSBot: [blankeclair@mwtask151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php CirrusSearch:ForceSearchIndex --wiki=waukeepediawiki (END - exit=0)
* 22:58 MirahezeLSBot: [blankeclair@mwtask151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php CirrusSearch:UpdateSearchIndexConfig --wiki=waukeepediawiki (END - exit=0)
* 22:57 BlankEclair: [blankeclair@mwtask151:~/imports]$ curl -X DELETE [https://opensearch-mw.wikitide.net/walkerpediawiki_{content,general}](https://opensearch-mw.wikitide.net/walkerpediawiki_{content,general})
* 22:55 BlankEclair: waukeepediawiki: CREATE DATABASE waukeepediawikicargo;
* 22:42 MirahezeLSBot: [blankeclair@mwtask151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RenameDatabase --wiki=loginwiki --rename --old walkerpediawiki --new waukeepediawiki --user 'BlankEclair (Miraheze)' (END - exit=0)
* 22:25 MirahezeLSBot: [petramagna@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 22:25 MirahezeLSBot: [petramagna@test151] starting deploy of {'config': True} to test151
* 22:23 MirahezeLSBot: [petramagna@test151] finished deploy of {'extension_list': True, 'folders': '1.45/extensions/CreateWikiLoadout', 'versions': '1.45'} to test151 - SUCCESS in 0s
* 22:23 MirahezeLSBot: [petramagna@test151] starting deploy of {'extension_list': True, 'folders': '1.45/extensions/CreateWikiLoadout', 'versions': '1.45'} to test151
* 13:16 MirahezeLSBot: [wwr@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 13:16 MirahezeLSBot: [wwr@test151] starting deploy of {'config': True} to test151
* 13:15 MirahezeLSBot: [wwr@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 13:15 MirahezeLSBot: [wwr@test151] starting deploy of {'config': True} to test151
* 09:13 RhinosF1: bounce ircecho
* 09:11 RhinosF1: bounce logbot & irclogserverbot

## 2026-03-20 

* 21:09 MirahezeLSBot: [wwr@test151] finished deploy of {'folders': '1.45/extensions/Bucket'} to test151 - SUCCESS in 0s
* 21:09 MirahezeLSBot: [wwr@test151] starting deploy of {'folders': '1.45/extensions/Bucket'} to test151
* 20:48 MirahezeLSBot: [wwr@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 20:48 MirahezeLSBot: [wwr@test151] starting deploy of {'config': True} to test151
* 03:54 Universal Omega: destory a user on phorge for [T15110](https://meta.miraheze.org/wiki/phorge:T15110)

## 2026-03-19 

* 22:36 MirahezeLSBot: [somerandomdeveloper@mwtask181] finished deploy of {'force_upgrade': True, 'versions': '1.45', 'upgrade_extensions': 'ThemeToggle'} to all - SUCCESS in 23s
* 22:35 MirahezeLSBot: [somerandomdeveloper@mwtask181] starting deploy of {'force_upgrade': True, 'versions': '1.45', 'upgrade_extensions': 'ThemeToggle'} to all
* 22:35 MirahezeLSBot: [somerandomdeveloper@mwtask181] finished deploy of {'versions': '1.45', 'upgrade_extensions': 'ThemeToggle'} to all - SUCCESS in 0s
* 22:35 MirahezeLSBot: [somerandomdeveloper@mwtask181] starting deploy of {'versions': '1.45', 'upgrade_extensions': 'ThemeToggle'} to all
* 22:35 MirahezeLSBot: [somerandomdeveloper@test151] finished deploy of {'force_upgrade': True, 'versions': '1.45', 'upgrade_extensions': 'ThemeToggle'} to test151 - SUCCESS in 0s
* 22:35 MirahezeLSBot: [somerandomdeveloper@test151] starting deploy of {'force_upgrade': True, 'versions': '1.45', 'upgrade_extensions': 'ThemeToggle'} to test151
* 22:35 MirahezeLSBot: [somerandomdeveloper@test151] finished deploy of {'versions': '1.45', 'upgrade_extensions': 'ThemeToggle'} to test151 - SUCCESS in 0s
* 22:35 MirahezeLSBot: [somerandomdeveloper@test151] starting deploy of {'versions': '1.45', 'upgrade_extensions': 'ThemeToggle'} to test151
* 22:27 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask181: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 22:27 MirahezeLSBot: [void@puppet181] Upgraded packages on mw183: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 22:27 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask151: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 22:26 MirahezeLSBot: [void@puppet181] Upgraded packages on mw202: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 22:26 MirahezeLSBot: [void@puppet181] Upgraded packages on mw182: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 22:26 MirahezeLSBot: [void@puppet181] Upgraded packages on mw203: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 22:25 MirahezeLSBot: [void@puppet181] Upgraded packages on mw192: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 22:25 MirahezeLSBot: [void@puppet181] Upgraded packages on test151: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 22:25 MirahezeLSBot: [void@puppet181] Upgraded packages on mw201: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 22:24 MirahezeLSBot: [void@puppet181] Upgraded packages on mw181: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 22:24 MirahezeLSBot: [void@puppet181] Upgraded packages on mw193: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 22:24 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask161: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 22:24 MirahezeLSBot: [void@puppet181] Upgraded packages on mw191: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 22:23 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask171: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 22:23 MirahezeLSBot: [void@puppet181] Upgraded packages on mw171: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 22:23 MirahezeLSBot: [void@puppet181] Upgraded packages on mw153: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 22:22 MirahezeLSBot: [void@puppet181] Upgraded packages on mw173: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 22:22 MirahezeLSBot: [void@puppet181] Upgraded packages on mw161: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 22:22 MirahezeLSBot: [void@puppet181] Upgraded packages on mw162: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 22:21 MirahezeLSBot: [void@puppet181] Upgraded packages on mw172: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 22:21 MirahezeLSBot: [void@puppet181] Upgraded packages on mw163: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 22:21 MirahezeLSBot: [void@puppet181] Upgraded packages on mw151: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 22:21 MirahezeLSBot: [void@puppet181] Upgraded packages on mw152: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 21:21 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject201: libfreetype6
* 21:21 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject191: libfreetype6
* 21:21 MirahezeLSBot: [void@puppet181] Upgraded packages on test151: libfreetype-dev and libfreetype6
* 21:20 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftproxy161: libfreetype6
* 21:20 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject211: libfreetype6
* 21:20 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftproxy171: libfreetype6
* 21:20 MirahezeLSBot: [void@puppet181] Upgraded packages on ns2: libfreetype6
* 21:19 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject181: libfreetype6
* 21:19 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject171: libfreetype6
* 21:19 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftac171: libfreetype6
* 21:19 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject161: libfreetype6
* 21:18 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject151: libfreetype6
* 21:18 MirahezeLSBot: [void@puppet181] Upgraded packages on rdb191: libfreetype6
* 21:18 MirahezeLSBot: [skye@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php CirrusSearch:ForceSearchIndex --wiki=vanguardswiki (END - exit=0)
* 21:18 MirahezeLSBot: [void@puppet181] Upgraded packages on os202: libfreetype6
* 21:17 MirahezeLSBot: [void@puppet181] Upgraded packages on puppet181: libfreetype6
* 21:17 MirahezeLSBot: [void@puppet181] Upgraded packages on os162: libfreetype6
* 21:17 MirahezeLSBot: [void@puppet181] Upgraded packages on os201: libfreetype6
* 21:17 MirahezeLSBot: [void@puppet181] Upgraded packages on os191: libfreetype6
* 21:17 MirahezeLSBot: [void@puppet181] Upgraded packages on os151: libfreetype6
* 21:16 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask181: libfreetype-dev and libfreetype6
* 21:16 MirahezeLSBot: [void@puppet181] Upgraded packages on reports171: libfreetype6
* 21:16 MirahezeLSBot: [void@puppet181] Upgraded packages on prometheus151: libfreetype6
* 21:16 MirahezeLSBot: [void@puppet181] Upgraded packages on os161: libfreetype6
* 21:15 MirahezeLSBot: [void@puppet181] Upgraded packages on phorge171: libfreetype6
* 21:15 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask171: libfreetype-dev and libfreetype6
* 21:15 MirahezeLSBot: [void@puppet181] Upgraded packages on ns1: libfreetype6
* 21:15 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask161: libfreetype-dev and libfreetype6
* 21:14 MirahezeLSBot: [void@puppet181] Upgraded packages on mw202: libfreetype-dev and libfreetype6
* 21:14 MirahezeLSBot: [void@puppet181] Upgraded packages on mw203: libfreetype-dev and libfreetype6
* 21:14 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask151: libfreetype-dev and libfreetype6
* 21:14 MirahezeLSBot: [void@puppet181] Upgraded packages on mw201: libfreetype-dev and libfreetype6
* 21:13 MirahezeLSBot: [void@puppet181] Upgraded packages on mw183: libfreetype-dev and libfreetype6
* 21:13 MirahezeLSBot: [void@puppet181] Upgraded packages on mw193: libfreetype-dev and libfreetype6
* 21:13 MirahezeLSBot: [void@puppet181] Upgraded packages on mw192: libfreetype-dev and libfreetype6
* 21:13 MirahezeLSBot: [void@puppet181] Upgraded packages on mw182: libfreetype-dev and libfreetype6
* 21:12 MirahezeLSBot: [void@puppet181] Upgraded packages on mw191: libfreetype-dev and libfreetype6
* 21:12 MirahezeLSBot: [void@puppet181] Upgraded packages on mw181: libfreetype-dev and libfreetype6
* 21:12 MirahezeLSBot: [void@puppet181] Upgraded packages on mw173: libfreetype-dev and libfreetype6
* 21:12 MirahezeLSBot: [void@puppet181] Upgraded packages on mw171: libfreetype-dev and libfreetype6
* 21:11 MirahezeLSBot: [void@puppet181] Upgraded packages on mw163: libfreetype-dev and libfreetype6
* 21:11 MirahezeLSBot: [void@puppet181] Upgraded packages on mw172: libfreetype-dev and libfreetype6
* 21:11 MirahezeLSBot: [void@puppet181] Upgraded packages on mon181: libfreetype6
* 21:11 MirahezeLSBot: [void@puppet181] Upgraded packages on mw153: libfreetype-dev and libfreetype6
* 21:10 MirahezeLSBot: [void@puppet181] Upgraded packages on mw162: libfreetype-dev and libfreetype6
* 21:10 MirahezeLSBot: [void@puppet181] Upgraded packages on mw152: libfreetype-dev and libfreetype6
* 21:10 MirahezeLSBot: [skye@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php CirrusSearch:UpdateSearchIndexConfig --wiki=vanguardswiki --startOver (END - exit=0)
* 21:10 MirahezeLSBot: [void@puppet181] Upgraded packages on mw151: libfreetype-dev and libfreetype6
* 21:10 MirahezeLSBot: [void@puppet181] Upgraded packages on mw161: libfreetype-dev and libfreetype6
* 21:09 MirahezeLSBot: [void@puppet181] Upgraded packages on mem191: libfreetype6
* 21:09 MirahezeLSBot: [void@puppet181] Upgraded packages on llm191: libfreetype6
* 21:09 MirahezeLSBot: [void@puppet181] Upgraded packages on mem201: libfreetype6
* 21:09 MirahezeLSBot: [void@puppet181] Upgraded packages on mem161: libfreetype6
* 21:08 MirahezeLSBot: [void@puppet181] Upgraded packages on kafka182: libfreetype6
* 21:08 MirahezeLSBot: [void@puppet181] Upgraded packages on matomo151: libfreetype6
* 21:08 MirahezeLSBot: [void@puppet181] Upgraded packages on ldap171: libfreetype6
* 21:08 MirahezeLSBot: [void@puppet181] Upgraded packages on mem151: libfreetype6
* 21:07 MirahezeLSBot: [void@puppet181] Upgraded packages on mattermost2: libfreetype6
* 21:07 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud20: libfreetype6
* 21:07 MirahezeLSBot: [void@puppet181] Upgraded packages on graylog161: libfreetype6
* 21:07 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud19: libfreetype6
* 21:07 MirahezeLSBot: [void@puppet181] Upgraded packages on db192: libfreetype6
* 21:06 MirahezeLSBot: [void@puppet181] Upgraded packages on eventgate182: libfreetype6
* 21:06 MirahezeLSBot: [void@puppet181] Upgraded packages on db181: libfreetype6
* 21:06 MirahezeLSBot: [void@puppet181] Upgraded packages on cp201: libfreetype6
* 21:06 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud18: libfreetype6
* 21:05 MirahezeLSBot: [void@puppet181] Upgraded packages on cp171: libfreetype6
* 21:05 MirahezeLSBot: [void@puppet181] Upgraded packages on db201: libfreetype6
* 21:05 MirahezeLSBot: [void@puppet181] Upgraded packages on bast181: libfreetype6
* 21:05 MirahezeLSBot: [void@puppet181] Upgraded packages on db182: libfreetype6
* 21:05 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud15: libfreetype6
* 21:04 MirahezeLSBot: [void@puppet181] Upgraded packages on changeprop202: libfreetype6
* 21:04 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud17: libfreetype6
* 21:04 MirahezeLSBot: [void@puppet181] Upgraded packages on db151: libfreetype6
* 21:04 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud21: libfreetype6
* 21:03 MirahezeLSBot: [void@puppet181] Upgraded packages on cp191: libfreetype6
* 21:03 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud16: libfreetype6
* 21:03 MirahezeLSBot: [void@puppet181] Upgraded packages on db172: libfreetype6
* 21:03 MirahezeLSBot: [void@puppet181] Upgraded packages on cp161: libfreetype6
* 21:03 MirahezeLSBot: [void@puppet181] Upgraded packages on db171: libfreetype6
* 21:02 MirahezeLSBot: [void@puppet181] Upgraded packages on bast161: libfreetype6
* 21:02 MirahezeLSBot: [void@puppet181] Upgraded packages on db161: libfreetype6
* 21:02 MirahezeLSBot: [void@puppet181] Upgraded packages on bots171: libfreetype6
* 19:46 MirahezeLSBot: [skye@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 24s
* 19:45 MirahezeLSBot: [skye@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 17:25 MirahezeLSBot: [skye@mwtask181] finished deploy of {'versions': '1.45', 'upgrade_extensions': 'PdfHandler'} to all - SUCCESS in 25s
* 17:25 MirahezeLSBot: [skye@mwtask181] starting deploy of {'versions': '1.45', 'upgrade_extensions': 'PdfHandler'} to all
* 16:02 MirahezeLSBot: [wwr@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 16:02 MirahezeLSBot: [wwr@test151] starting deploy of {'config': True} to test151
* 02:15 MirahezeLSBot: [skye@mwtask181] finished deploy of {'versions': '1.45', 'upgrade_extensions': 'SocialProfile'} to all - SUCCESS in 26s
* 02:14 MirahezeLSBot: [skye@mwtask181] starting deploy of {'versions': '1.45', 'upgrade_extensions': 'SocialProfile'} to all
* 01:48 MirahezeLSBot: [skye@test151] finished deploy of {'versions': '1.45', 'upgrade_extensions': 'SocialProfile'} to test151 - SUCCESS in 1s
* 01:48 MirahezeLSBot: [skye@test151] starting deploy of {'versions': '1.45', 'upgrade_extensions': 'SocialProfile'} to test151
* 00:05 MirahezeLSBot: [somerandomdeveloper@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 25s
* 00:05 MirahezeLSBot: [somerandomdeveloper@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 00:05 MirahezeLSBot: [somerandomdeveloper@test151] finished deploy of {'pull': 'config', 'config': True} to test151 - SUCCESS in 2s
* 00:04 MirahezeLSBot: [somerandomdeveloper@test151] starting deploy of {'pull': 'config', 'config': True} to test151
* 00:01 MirahezeLSBot: [somerandomdeveloper@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 00:01 MirahezeLSBot: [somerandomdeveloper@test151] starting deploy of {'config': True} to test151
* 00:00 MirahezeLSBot: [somerandomdeveloper@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 00:00 MirahezeLSBot: [somerandomdeveloper@test151] starting deploy of {'config': True} to test151

## 2026-03-18 

* 16:20 @paladox: upgrade phorge on phorge171
* 11:08 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php Bucket:RefreshAllBuckets --wiki=buckettestwikibeta (END - exit=0)
* 02:10 MirahezeLSBot: [void@puppet181] Upgraded packages on eventgate182: nodejs, libnode115, and nodejs-doc
* 02:10 MirahezeLSBot: [void@puppet181] Upgraded packages on changeprop202: nodejs, libnode115, and nodejs-doc
* 02:06 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject181: libgstreamer-plugins-base1.0-0, libgstreamer-gl1.0-0, gstreamer1.0-gl, and gstreamer1.0-plugins-base
* 02:05 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject191: libgstreamer-plugins-base1.0-0, libgstreamer-gl1.0-0, gstreamer1.0-gl, and gstreamer1.0-plugins-base
* 02:05 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject201: libgstreamer-plugins-base1.0-0, libgstreamer-gl1.0-0, gstreamer1.0-gl, and gstreamer1.0-plugins-base
* 02:05 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftproxy161: libgstreamer-plugins-base1.0-0, libgstreamer-gl1.0-0, gstreamer1.0-gl, and gstreamer1.0-plugins-base
* 02:05 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftac171: libgstreamer-plugins-base1.0-0, libgstreamer-gl1.0-0, gstreamer1.0-gl, and gstreamer1.0-plugins-base
* 02:04 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject161: libgstreamer-plugins-base1.0-0, libgstreamer-gl1.0-0, gstreamer1.0-gl, and gstreamer1.0-plugins-base
* 02:04 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject171: libgstreamer-plugins-base1.0-0, libgstreamer-gl1.0-0, gstreamer1.0-gl, and gstreamer1.0-plugins-base
* 02:04 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftproxy171: libgstreamer-plugins-base1.0-0, libgstreamer-gl1.0-0, gstreamer1.0-gl, and gstreamer1.0-plugins-base
* 02:04 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject151: libgstreamer-plugins-base1.0-0, libgstreamer-gl1.0-0, gstreamer1.0-gl, and gstreamer1.0-plugins-base
* 02:02 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud18: libgstreamer-plugins-base1.0-0
* 02:02 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud19: libgstreamer-plugins-base1.0-0
* 02:01 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud17: libgstreamer-plugins-base1.0-0
* 02:01 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud20: libgstreamer-plugins-base1.0-0
* 02:01 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud16: libgstreamer-plugins-base1.0-0
* 02:01 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud15: libgstreamer-plugins-base1.0-0
* 02:01 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud21: libgstreamer-plugins-base1.0-0
* 01:59 MirahezeLSBot: [void@puppet181] Upgraded packages on test151: libgstreamer-plugins-base1.0-0, libgstreamer-gl1.0-0, gstreamer1.0-gl, gstreamer1.0-plugins-base, nodejs, libnode115, and nodejs-doc
* 01:57 MirahezeLSBot: [void@puppet181] Upgraded packages on mw202: libgstreamer-plugins-base1.0-0, libgstreamer-gl1.0-0, gstreamer1.0-gl, gstreamer1.0-plugins-base, nodejs, libnode115, and nodejs-doc
* 01:57 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask181: libgstreamer-plugins-base1.0-0, libgstreamer-gl1.0-0, gstreamer1.0-gl, gstreamer1.0-plugins-base, nodejs, libnode115, and nodejs-doc
* 01:56 MirahezeLSBot: [void@puppet181] Upgraded packages on mw183: libgstreamer-plugins-base1.0-0, libgstreamer-gl1.0-0, gstreamer1.0-gl, gstreamer1.0-plugins-base, nodejs, libnode115, and nodejs-doc
* 01:56 MirahezeLSBot: [void@puppet181] Upgraded packages on mw193: libgstreamer-plugins-base1.0-0, libgstreamer-gl1.0-0, gstreamer1.0-gl, gstreamer1.0-plugins-base, nodejs, libnode115, and nodejs-doc
* 01:56 MirahezeLSBot: [void@puppet181] Upgraded packages on mw201: libgstreamer-plugins-base1.0-0, libgstreamer-gl1.0-0, gstreamer1.0-gl, gstreamer1.0-plugins-base, nodejs, libnode115, and nodejs-doc
* 01:56 MirahezeLSBot: [void@puppet181] Upgraded packages on mw192: libgstreamer-plugins-base1.0-0, libgstreamer-gl1.0-0, gstreamer1.0-gl, gstreamer1.0-plugins-base, nodejs, libnode115, and nodejs-doc
* 01:55 MirahezeLSBot: [void@puppet181] Upgraded packages on mw191: libgstreamer-plugins-base1.0-0, libgstreamer-gl1.0-0, gstreamer1.0-gl, gstreamer1.0-plugins-base, nodejs, libnode115, and nodejs-doc
* 01:55 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask171: libgstreamer-plugins-base1.0-0, libgstreamer-gl1.0-0, gstreamer1.0-gl, gstreamer1.0-plugins-base, nodejs, libnode115, and nodejs-doc
* 01:55 MirahezeLSBot: [void@puppet181] Upgraded packages on mw203: libgstreamer-plugins-base1.0-0, libgstreamer-gl1.0-0, gstreamer1.0-gl, gstreamer1.0-plugins-base, nodejs, libnode115, and nodejs-doc
* 01:54 MirahezeLSBot: [void@puppet181] Upgraded packages on mw182: libgstreamer-plugins-base1.0-0, libgstreamer-gl1.0-0, gstreamer1.0-gl, gstreamer1.0-plugins-base, nodejs, libnode115, and nodejs-doc
* 01:54 MirahezeLSBot: [void@puppet181] Upgraded packages on mw173: libgstreamer-plugins-base1.0-0, libgstreamer-gl1.0-0, gstreamer1.0-gl, gstreamer1.0-plugins-base, nodejs, libnode115, and nodejs-doc
* 01:54 MirahezeLSBot: [void@puppet181] Upgraded packages on mw172: libgstreamer-plugins-base1.0-0, libgstreamer-gl1.0-0, gstreamer1.0-gl, gstreamer1.0-plugins-base, nodejs, libnode115, and nodejs-doc
* 01:53 MirahezeLSBot: [void@puppet181] Upgraded packages on mw181: libgstreamer-plugins-base1.0-0, libgstreamer-gl1.0-0, gstreamer1.0-gl, gstreamer1.0-plugins-base, nodejs, libnode115, and nodejs-doc
* 01:53 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask161: libgstreamer-plugins-base1.0-0, libgstreamer-gl1.0-0, gstreamer1.0-gl, gstreamer1.0-plugins-base, nodejs, libnode115, and nodejs-doc
* 01:53 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask151: libgstreamer-plugins-base1.0-0, libgstreamer-gl1.0-0, gstreamer1.0-gl, gstreamer1.0-plugins-base, nodejs, libnode115, and nodejs-doc
* 01:53 MirahezeLSBot: [void@puppet181] Upgraded packages on mw162: libgstreamer-plugins-base1.0-0, libgstreamer-gl1.0-0, gstreamer1.0-gl, gstreamer1.0-plugins-base, nodejs, libnode115, and nodejs-doc
* 01:52 MirahezeLSBot: [void@puppet181] Upgraded packages on mw171: libgstreamer-plugins-base1.0-0, libgstreamer-gl1.0-0, gstreamer1.0-gl, gstreamer1.0-plugins-base, nodejs, libnode115, and nodejs-doc
* 01:52 MirahezeLSBot: [void@puppet181] Upgraded packages on mw163: libgstreamer-plugins-base1.0-0, libgstreamer-gl1.0-0, gstreamer1.0-gl, gstreamer1.0-plugins-base, nodejs, libnode115, and nodejs-doc
* 01:52 MirahezeLSBot: [void@puppet181] Upgraded packages on mw161: libgstreamer-plugins-base1.0-0, libgstreamer-gl1.0-0, gstreamer1.0-gl, gstreamer1.0-plugins-base, nodejs, libnode115, and nodejs-doc
* 01:51 MirahezeLSBot: [void@puppet181] Upgraded packages on mw151: libgstreamer-plugins-base1.0-0, libgstreamer-gl1.0-0, gstreamer1.0-gl, gstreamer1.0-plugins-base, nodejs, libnode115, and nodejs-doc
* 01:51 MirahezeLSBot: [void@puppet181] Upgraded packages on mw153: libgstreamer-plugins-base1.0-0, libgstreamer-gl1.0-0, gstreamer1.0-gl, gstreamer1.0-plugins-base, nodejs, libnode115, and nodejs-doc
* 01:51 MirahezeLSBot: [void@puppet181] Upgraded packages on mw152: libgstreamer-plugins-base1.0-0, libgstreamer-gl1.0-0, gstreamer1.0-gl, gstreamer1.0-plugins-base, nodejs, libnode115, and nodejs-doc

## 2026-03-17 

* 22:27 MirahezeLSBot: [petramagna@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php ManageWiki:PopulateWikiSettings --wiki=metawiki --setting=wgLocaltimezone --sourcelist=/tmp/tzvalues.txt (END - exit=0)
* 22:24 MirahezeLSBot: [petramagna@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php CentralAuth:fixStuckGlobalRename --wiki=polandcuberuwiki --logwiki=metawiki Wither girl02679 Wither02679 (END - exit=0)
* 22:21 MirahezeLSBot: [petramagna@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php ManageWiki:PopulateWikiSettings --wiki=metawiki --setting=wgLocaltimezone --sourcelist=/tmp/tzvalues.txt (END - exit=0)
* 22:21 MirahezeLSBot: [petramagna@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php ManageWiki:PopulateWikiSettings --wiki=metawiki --setting=wgLocaltimezone --sourcelist=~/tzvalues.txt (END - exit=0)
* 22:10 MirahezeLSBot: [petramagna@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php CentralAuth:fixStuckGlobalRename --wiki=zhpolandballwiki --logwiki=metawiki Wither girl02679 Wither02679 (END - exit=0)
* 22:09 MirahezeLSBot: [petramagna@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php CentralAuth:fixStuckGlobalRename --wiki=wikiballwiki --logwiki=metawiki Wither girl02679 Wither02679 (END - exit=0)
* 22:08 MirahezeLSBot: [petramagna@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php CentralAuth:fixStuckGlobalRename --wiki=vexillumwiki --logwiki=metawiki Wither girl02679 Wither02679 (END - exit=0)
* 22:07 MirahezeLSBot: [petramagna@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php CentralAuth:fixStuckGlobalRename --wiki=polandcuberuwiki --logwiki=metawiki Wither girl02679 Wither02679 (END - exit=65280)
* 01:48 MirahezeLSBot: [void@cloud21] Clear ipmi sel (inlet temperature spike from March 13 to March 14)
* 01:46 MirahezeLSBot: [void@phorge171] restart ntp service

## 2026-03-16 

* 00:30 MirahezeLSBot: [paladox@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 24s
* 00:30 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all

## 2026-03-15 

* 19:25 @paladox: reboot phorge171
* 17:11 @paladox: upgrade phorge on phorge171

## 2026-03-14 

* 18:09 MirahezeLSBot: [wwr@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 18:09 MirahezeLSBot: [wwr@test151] starting deploy of {'config': True} to test151
* 14:28 MirahezeLSBot: [pixldev@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 14:28 MirahezeLSBot: [pixldev@test151] starting deploy of {'config': True} to test151
* 13:46 MirahezeLSBot: [wwr@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 13:46 MirahezeLSBot: [wwr@test151] starting deploy of {'config': True} to test151
* 02:57 MirahezeLSBot: [wwr@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 02:57 MirahezeLSBot: [wwr@test151] starting deploy of {'config': True} to test151
* 02:39 MirahezeLSBot: [wwr@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 02:39 MirahezeLSBot: [wwr@test151] starting deploy of {'config': True} to test151
* 02:38 MirahezeLSBot: [wwr@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 02:38 MirahezeLSBot: [wwr@test151] starting deploy of {'config': True} to test151
* 02:25 MirahezeLSBot: [wwr@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 02:25 MirahezeLSBot: [wwr@test151] starting deploy of {'config': True} to test151
* 02:24 MirahezeLSBot: [wwr@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 02:24 MirahezeLSBot: [wwr@test151] starting deploy of {'config': True} to test151
* 02:07 MirahezeLSBot: [wwr@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 02:07 MirahezeLSBot: [wwr@test151] starting deploy of {'config': True} to test151
* 02:06 MirahezeLSBot: [wwr@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 02:06 MirahezeLSBot: [wwr@test151] starting deploy of {'config': True} to test151
* 02:04 MirahezeLSBot: [pixldev@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 02:04 MirahezeLSBot: [pixldev@test151] starting deploy of {'config': True} to test151
* 01:56 MirahezeLSBot: [pixldev@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 01:56 MirahezeLSBot: [pixldev@test151] starting deploy of {'config': True} to test151
* 01:46 MirahezeLSBot: [pixldev@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 01:46 MirahezeLSBot: [pixldev@test151] starting deploy of {'config': True} to test151
* 01:35 MirahezeLSBot: [pixldev@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 01:35 MirahezeLSBot: [pixldev@test151] starting deploy of {'config': True} to test151
* 01:35 MirahezeLSBot: [pixldev@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 01:35 MirahezeLSBot: [pixldev@test151] starting deploy of {'config': True} to test151
* 01:34 MirahezeLSBot: [pixldev@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 01:34 MirahezeLSBot: [pixldev@test151] starting deploy of {'config': True} to test151
* 01:30 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MatomoAnalytics:ModifyMatomo --wiki=wwrtest3wikibeta (END - exit=0)
* 01:24 MirahezeLSBot: [wwr@test151] Finished import for wwrtest3wikibeta (XML: None; Images: ./images/) (END - exit=1)
* 01:24 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=wwrtest3wikibeta --sleep=0 '--comment=Importing images from [https://dev.miraheze.org](https://dev.miraheze.org) ([T15032](https://meta.miraheze.org/wiki/phorge:T15032))' --search-recursively -- ./images/ (END - exit=1)
* 01:23 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=wwrtest3wikibeta --sleep=0 '--comment=Importing images from [https://dev.miraheze.org](https://dev.miraheze.org) ([T15032](https://meta.miraheze.org/wiki/phorge:T15032))' --search-recursively -- ./images/ (START)
* 01:23 MirahezeLSBot: [wwr@test151] Starting import for wwrtest3wikibeta (XML: None; Images: ./images/) (START)
* 01:23 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php initSiteStats --wiki=wwrtest3wikibeta --update (END - exit=0)
* 01:23 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php initEditCount --wiki=wwrtest3wikibeta (END - exit=0)
* 01:16 MirahezeLSBot: [wwr@test151] Finished import for wwrtest3wikibeta (XML: None; Images: ./imports/images/) (END - exit=1)
* 01:16 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=wwrtest3wikibeta --sleep=0 '--comment=Importing images from [https://dev.miraheze.org](https://dev.miraheze.org) ([T15032](https://meta.miraheze.org/wiki/phorge:T15032))' -- ./imports/images/ (END - exit=1)
* 01:16 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=wwrtest3wikibeta --sleep=0 '--comment=Importing images from [https://dev.miraheze.org](https://dev.miraheze.org) ([T15032](https://meta.miraheze.org/wiki/phorge:T15032))' -- ./imports/images/ (START)
* 01:16 MirahezeLSBot: [wwr@test151] Starting import for wwrtest3wikibeta (XML: None; Images: ./imports/images/) (START)
* 01:09 MirahezeLSBot: [pixldev@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 01:09 MirahezeLSBot: [pixldev@test151] starting deploy of {'config': True} to test151
* 00:42 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php CreateWiki:SetContainersAccess --wiki=wwrtest3wikibeta (END - exit=0)
* 00:41 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php CreateWiki:SetContainersAccess --wiki=wwrtest3wikibeta (END - exit=0)
* 00:32 MirahezeLSBot: [wwr@test151] Finished import for wwrtest3wikibeta (XML: None; Images: ./images) (END - exit=1)
* 00:32 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=wwrtest3wikibeta --sleep=0 '--comment=Importing images from [https://dev.miraheze.org](https://dev.miraheze.org) ([T15032](https://meta.miraheze.org/wiki/phorge:T15032))' -- ./images (END - exit=1)
* 00:32 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=wwrtest3wikibeta --sleep=0 '--comment=Importing images from [https://dev.miraheze.org](https://dev.miraheze.org) ([T15032](https://meta.miraheze.org/wiki/phorge:T15032))' -- ./images (START)
* 00:32 MirahezeLSBot: [wwr@test151] Starting import for wwrtest3wikibeta (XML: None; Images: ./images) (START)
* 00:31 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php CreateWiki:SetContainersAccess --wiki=wwrtest3wikibeta (END - exit=0)
* 00:23 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php rebuildall --wiki=wwrtest3wikibeta (END - exit=0)
* 00:04 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php rebuildall --wiki=wwrtest3wikibeta (START)
* 00:01 MirahezeLSBot: [wwr@test151] Finished import for wwrtest3wikibeta (XML: None; Images: ./images) (END - exit=1)
* 00:01 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=wwrtest3wikibeta --sleep=1 '--comment=Importing images from [https://dev.miraheze.org](https://dev.miraheze.org) ([T15032](https://meta.miraheze.org/wiki/phorge:T15032))' -- ./images (END - exit=1)
* 00:01 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=wwrtest3wikibeta --sleep=1 '--comment=Importing images from [https://dev.miraheze.org](https://dev.miraheze.org) ([T15032](https://meta.miraheze.org/wiki/phorge:T15032))' -- ./images (START)
* 00:01 MirahezeLSBot: [wwr@test151] Starting import for wwrtest3wikibeta (XML: None; Images: ./images) (START)
* 00:00 MirahezeLSBot: [wwr@test151] Finished import for wwrtest3wikibeta (XML: None; Images: ./images) (END - exit=1)
* 00:00 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=wwrtest3wikibeta --sleep=0 '--comment=Importing images from [https://dev.miraheze.org](https://dev.miraheze.org) ([T15032](https://meta.miraheze.org/wiki/phorge:T15032))' -- ./images (END - exit=1)
* 00:00 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=wwrtest3wikibeta --sleep=0 '--comment=Importing images from [https://dev.miraheze.org](https://dev.miraheze.org) ([T15032](https://meta.miraheze.org/wiki/phorge:T15032))' -- ./images (START)
* 00:00 MirahezeLSBot: [wwr@test151] Starting import for wwrtest3wikibeta (XML: None; Images: ./images) (START)

## 2026-03-13 

* 23:57 MirahezeLSBot: [wwr@test151] Finished import for wwrtest3wikibeta (XML: None; Images: ./tmp/devwiki/) (END - exit=1)
* 23:57 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=wwrtest3wikibeta --sleep=0 '--comment=Importing images from [https://dev.miraheze.org](https://dev.miraheze.org) ([T15032](https://meta.miraheze.org/wiki/phorge:T15032))' --search-recursively -- ./tmp/devwiki/ (END - exit=1)
* 23:57 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=wwrtest3wikibeta --sleep=0 '--comment=Importing images from [https://dev.miraheze.org](https://dev.miraheze.org) ([T15032](https://meta.miraheze.org/wiki/phorge:T15032))' --search-recursively -- ./tmp/devwiki/ (START)
* 23:57 MirahezeLSBot: [wwr@test151] Starting import for wwrtest3wikibeta (XML: None; Images: ./tmp/devwiki/) (START)
* 23:52 MirahezeLSBot: [wwr@test151] Finished import for wwrtest3wikibeta (XML: ./history.xml; Images: ./tmp/devwiki/) (END - exit=1)
* 23:52 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=wwrtest3wikibeta --sleep=0 '--comment=Importing images from [https://dev.miraheze.org](https://dev.miraheze.org) ([T15032](https://meta.miraheze.org/wiki/phorge:T15032))' --search-recursively -- ./tmp/devwiki/ (END - exit=1)
* 23:52 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=wwrtest3wikibeta --sleep=0 '--comment=Importing images from [https://dev.miraheze.org](https://dev.miraheze.org) ([T15032](https://meta.miraheze.org/wiki/phorge:T15032))' --search-recursively -- ./tmp/devwiki/ (START)
* 23:52 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importDump --wiki=wwrtest3wikibeta --no-updates --username-prefix=mh:dev -- ./history.xml (END - exit=0)
* 23:46 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importDump --wiki=wwrtest3wikibeta --no-updates --username-prefix=mh:dev -- ./history.xml (START)
* 23:46 MirahezeLSBot: [wwr@test151] Starting import for wwrtest3wikibeta (XML: ./history.xml; Images: ./tmp/devwiki/) (START)
* 22:55 MirahezeLSBot: [void@db171] restart sql-backup service
* 22:33 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php createAndPromote --wiki=wwrtest3wikibeta TheWWRNerdGuy --bureaucrat --force --sysop --interface-admin (END - exit=0)
* 22:29 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:ResetWiki --wiki=loginwikibeta --dbname=wwrtest3wikibeta --requester=TheWWRNerdAlt (END - exit=0)
* 19:06 MirahezeLSBot: [paladox@test151] finished deploy of {'l10n': True, 'versions': '1.45', 'upgrade_extensions': 'PageForms'} to test151 - SUCCESS in 315s
* 19:00 MirahezeLSBot: [paladox@test151] starting deploy of {'l10n': True, 'versions': '1.45', 'upgrade_extensions': 'PageForms'} to test151
* 18:59 MirahezeLSBot: [paladox@test151] finished deploy of {'l10n': True, 'versions': '1.45', 'upgrade_extensions': 'Cargo'} to test151 - SUCCESS in 324s
* 18:58 MirahezeLSBot: [paladox@mwtask181] finished deploy of {'l10n': True, 'versions': '1.45', 'upgrade_extensions': 'PageForms'} to all - SUCCESS in 111s
* 18:56 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'l10n': True, 'versions': '1.45', 'upgrade_extensions': 'PageForms'} to all
* 18:56 MirahezeLSBot: [paladox@mwtask181] finished deploy of {'l10n': True, 'versions': '1.45', 'upgrade_extensions': 'Cargo'} to all - SUCCESS in 159s
* 18:53 MirahezeLSBot: [paladox@test151] starting deploy of {'l10n': True, 'versions': '1.45', 'upgrade_extensions': 'Cargo'} to test151
* 18:53 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'l10n': True, 'versions': '1.45', 'upgrade_extensions': 'Cargo'} to all
* 16:03 @paladox: upgrade mariadb-common on mon181
* 15:57 @paladox: upgrade icinga2 on mon181
* 15:52 @paladox: upgrade grafana on mon181
* 02:25 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RemoveCustomDomain --wiki=loginwiki --dbname=stretwikiwiki (END - exit=0)
* 02:25 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RemoveCustomDomain --wiki=loginwiki --dbname=nazarewiki (END - exit=0)
* 02:25 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RemoveCustomDomain --wiki=loginwiki --dbname=truevanillawiki (END - exit=0)
* 02:25 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RemoveCustomDomain --wiki=loginwiki --dbname=redk1ttywiki (END - exit=0)
* 02:25 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RemoveCustomDomain --wiki=loginwiki --dbname=luckbychancewiki (END - exit=0)
* 02:25 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RemoveCustomDomain --wiki=loginwiki --dbname=lostcompasswiki (END - exit=0)
* 02:25 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RemoveCustomDomain --wiki=loginwiki --dbname=lifesprogresswiki (END - exit=0)
* 02:25 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RemoveCustomDomain --wiki=loginwiki --dbname=hymnrowiki (END - exit=0)
* 02:25 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RemoveCustomDomain --wiki=loginwiki --dbname=firetimewiki (END - exit=0)
* 02:25 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RemoveCustomDomain --wiki=loginwiki --dbname=eggnoswiki (END - exit=0)
* 02:25 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RemoveCustomDomain --wiki=loginwiki --dbname=checkcablewiki (END - exit=0)
* 02:25 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RemoveCustomDomain --wiki=loginwiki --dbname=bastionsgwiki (END - exit=0)
* 02:25 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RemoveCustomDomain --wiki=loginwiki --dbname=reactorwiki (END - exit=0)
* 02:25 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RemoveCustomDomain --wiki=loginwiki --dbname=sithempirewiki (END - exit=0)
* 02:25 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RemoveCustomDomain --wiki=loginwiki --dbname=prxpvnewiki (END - exit=0)
* 02:25 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RemoveCustomDomain --wiki=loginwiki --dbname=prisonerlifewiki (END - exit=0)
* 02:25 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RemoveCustomDomain --wiki=loginwiki --dbname=metawiki (END - exit=0)
* 02:25 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RemoveCustomDomain --wiki=loginwiki --dbname=maxcapacitywiki (END - exit=0)
* 02:25 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RemoveCustomDomain --wiki=loginwiki --dbname=lugatwiki (END - exit=0)
* 02:25 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RemoveCustomDomain --wiki=loginwiki --dbname=forestwiki (END - exit=0)
* 02:24 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RemoveCustomDomain --wiki=loginwiki --dbname=dysonsphereprogramwiki (END - exit=0)
* 02:24 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RemoveCustomDomain --wiki=loginwiki --dbname=tucsonemwiki (END - exit=0)
* 02:24 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RemoveCustomDomain --wiki=loginwiki --dbname=bristolstudenthousingcoopwiki (END - exit=0)
* 02:24 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RemoveCustomDomain --wiki=loginwiki --dbname=starworldwiki (END - exit=0)
* 02:24 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RemoveCustomDomain --wiki=loginwiki --dbname=armoredpatrolremasteredwiki (END - exit=0)
* 02:24 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RemoveCustomDomain --wiki=loginwiki --dbname=100acgwiki (END - exit=0)
* 02:15 MirahezeLSBot: [universalomega@bots171] sudo apt purge --autoremove dotnet-sdk-8.0
* 00:46 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject201: linux-libc-dev
* 00:45 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject191: linux-libc-dev
* 00:45 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftproxy171: linux-libc-dev
* 00:45 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject211: linux-libc-dev
* 00:45 MirahezeLSBot: [void@puppet181] Upgraded packages on test151: linux-libc-dev
* 00:44 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftproxy161: linux-libc-dev
* 00:44 MirahezeLSBot: [void@puppet181] Upgraded packages on ns2: linux-libc-dev
* 00:44 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject181: linux-libc-dev
* 00:44 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject171: linux-libc-dev
* 00:43 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject161: linux-libc-dev
* 00:43 MirahezeLSBot: [void@puppet181] Upgraded packages on os191: linux-libc-dev
* 00:43 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftac171: linux-libc-dev
* 00:43 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject151: linux-libc-dev
* 00:43 MirahezeLSBot: [void@puppet181] Upgraded packages on rdb191: linux-libc-dev
* 00:42 MirahezeLSBot: [void@puppet181] Upgraded packages on os202: linux-libc-dev
* 00:42 MirahezeLSBot: [void@puppet181] Upgraded packages on puppet181: linux-libc-dev
* 00:42 MirahezeLSBot: [void@puppet181] Upgraded packages on os201: linux-libc-dev
* 00:40 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask181: linux-libc-dev
* 00:40 MirahezeLSBot: [void@puppet181] Upgraded packages on reports171: linux-libc-dev
* 00:40 MirahezeLSBot: [void@puppet181] Upgraded packages on os161: linux-libc-dev
* 00:40 MirahezeLSBot: [void@puppet181] Upgraded packages on os162: linux-libc-dev
* 00:40 MirahezeLSBot: [void@puppet181] Upgraded packages on prometheus151: linux-libc-dev
* 00:39 MirahezeLSBot: [void@puppet181] Upgraded packages on phorge171: linux-libc-dev
* 00:39 MirahezeLSBot: [void@puppet181] Upgraded packages on os151: linux-libc-dev
* 00:39 MirahezeLSBot: [void@puppet181] Upgraded packages on ns1: linux-libc-dev
* 00:39 MirahezeLSBot: [void@puppet181] Upgraded packages on mw203: linux-libc-dev
* 00:38 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask151: linux-libc-dev
* 00:38 MirahezeLSBot: [void@puppet181] Upgraded packages on mw201: linux-libc-dev
* 00:38 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask161: linux-libc-dev
* 00:38 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask171: linux-libc-dev
* 00:38 MirahezeLSBot: [void@puppet181] Upgraded packages on mw202: linux-libc-dev
* 00:37 MirahezeLSBot: [void@puppet181] Upgraded packages on mw191: linux-libc-dev
* 00:36 MirahezeLSBot: [void@puppet181] Upgraded packages on mw183: linux-libc-dev
* 00:36 MirahezeLSBot: [void@puppet181] Upgraded packages on mw193: linux-libc-dev
* 00:36 MirahezeLSBot: [void@puppet181] Upgraded packages on mw181: linux-libc-dev
* 00:35 MirahezeLSBot: [void@puppet181] Upgraded packages on mw182: linux-libc-dev
* 00:35 MirahezeLSBot: [void@puppet181] Upgraded packages on mw192: linux-libc-dev
* 00:35 MirahezeLSBot: [void@puppet181] Upgraded packages on mw173: linux-libc-dev
* 00:35 MirahezeLSBot: [void@puppet181] Upgraded packages on mw171: linux-libc-dev
* 00:34 MirahezeLSBot: [void@puppet181] Upgraded packages on mw163: linux-libc-dev
* 00:34 MirahezeLSBot: [void@puppet181] Upgraded packages on mw172: linux-libc-dev
* 00:34 MirahezeLSBot: [void@puppet181] Upgraded packages on mw162: linux-libc-dev
* 00:34 MirahezeLSBot: [void@puppet181] Upgraded packages on mw161: linux-libc-dev
* 00:34 MirahezeLSBot: [void@puppet181] Upgraded packages on mw153: linux-libc-dev
* 00:33 MirahezeLSBot: [void@puppet181] Upgraded packages on mw152: linux-libc-dev
* 00:33 MirahezeLSBot: [void@puppet181] Upgraded packages on mem191: linux-libc-dev
* 00:33 MirahezeLSBot: [void@puppet181] Upgraded packages on mon181: linux-libc-dev
* 00:33 MirahezeLSBot: [void@puppet181] Upgraded packages on mw151: linux-libc-dev
* 00:32 MirahezeLSBot: [void@puppet181] Upgraded packages on mem201: linux-libc-dev
* 00:32 MirahezeLSBot: [void@puppet181] Upgraded packages on llm191: linux-libc-dev
* 00:32 MirahezeLSBot: [void@puppet181] Upgraded packages on kafka182: linux-libc-dev
* 00:32 MirahezeLSBot: [void@puppet181] Upgraded packages on mem161: linux-libc-dev
* 00:32 MirahezeLSBot: [void@puppet181] Upgraded packages on mem151: linux-libc-dev
* 00:31 MirahezeLSBot: [void@puppet181] Upgraded packages on matomo151: linux-libc-dev
* 00:31 MirahezeLSBot: [void@puppet181] Upgraded packages on mattermost2: linux-libc-dev
* 00:31 MirahezeLSBot: [void@puppet181] Upgraded packages on ldap171: linux-libc-dev
* 00:31 MirahezeLSBot: [void@puppet181] Upgraded packages on graylog161: linux-libc-dev
* 00:31 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud20: libcpupower1, linux-cpupower, and linux-libc-dev
* 00:30 MirahezeLSBot: [void@puppet181] Upgraded packages on cp191: linux-libc-dev
* 00:30 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud19: libcpupower1, linux-cpupower, and linux-libc-dev
* 00:30 MirahezeLSBot: [void@puppet181] Upgraded packages on eventgate182: linux-libc-dev
* 00:30 MirahezeLSBot: [void@puppet181] Upgraded packages on cp201: linux-libc-dev
* 00:29 MirahezeLSBot: [void@puppet181] Upgraded packages on db201: linux-libc-dev
* 00:29 MirahezeLSBot: [void@puppet181] Upgraded packages on db181: linux-libc-dev
* 00:29 MirahezeLSBot: [void@puppet181] Upgraded packages on db182: linux-libc-dev
* 00:29 MirahezeLSBot: [void@puppet181] Upgraded packages on db192: linux-libc-dev
* 00:28 MirahezeLSBot: [void@puppet181] Upgraded packages on bast181: linux-libc-dev
* 00:28 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud18: libcpupower1, linux-cpupower, and linux-libc-dev
* 00:28 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud17: libcpupower1, linux-cpupower, and linux-libc-dev
* 00:28 MirahezeLSBot: [void@puppet181] Upgraded packages on db161: linux-libc-dev
* 00:28 MirahezeLSBot: [void@puppet181] Upgraded packages on cp171: linux-libc-dev
* 00:27 MirahezeLSBot: [void@puppet181] Upgraded packages on changeprop202: linux-libc-dev
* 00:27 MirahezeLSBot: [void@puppet181] Upgraded packages on db151: linux-libc-dev
* 00:27 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud16: libcpupower1, linux-cpupower, and linux-libc-dev
* 00:27 MirahezeLSBot: [void@puppet181] Upgraded packages on db171: linux-libc-dev
* 00:26 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud21: libcpupower1, linux-cpupower, and linux-libc-dev
* 00:26 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud15: libcpupower1, linux-cpupower, and linux-libc-dev
* 00:26 MirahezeLSBot: [void@puppet181] Upgraded packages on db172: linux-libc-dev
* 00:26 MirahezeLSBot: [void@puppet181] Upgraded packages on bots171: linux-libc-dev
* 00:26 MirahezeLSBot: [void@puppet181] Upgraded packages on cp161: linux-libc-dev
* 00:25 MirahezeLSBot: [void@puppet181] Upgraded packages on bast161: linux-libc-dev

## 2026-03-12 

* 20:51 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php purgeParserCache --wiki=suppressionwiki --age=14400 (END - exit=0)
* 19:47 MirahezeLSBot: [universalomega@bots171] sudo apt purge --autoremove dotnet-sdk-6.0
* 19:24 MirahezeLSBot: [void@kafka182] upgrade package libnetty-java and restart kafka + zookeeper
* 19:07 MirahezeLSBot: [wwr@test151] Finished import for wwrtest3wikibeta (XML: ./tdutr.xml; Images: ./images) (END - exit=0)
* 19:07 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php initSiteStats --wiki=wwrtest3wikibeta --update (END - exit=0)
* 19:07 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php initSiteStats --wiki=wwrtest3wikibeta --update (START)
* 19:07 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php initEditCount --wiki=wwrtest3wikibeta (END - exit=0)
* 19:07 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php initEditCount --wiki=wwrtest3wikibeta (START)
* 19:07 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php rebuildall --wiki=wwrtest3wikibeta (END - exit=0)
* 19:04 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php rebuildall --wiki=wwrtest3wikibeta (START)
* 19:04 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=wwrtest3wikibeta --sleep=0 '--comment=Blowing up db servers with content from [https://tdutr.fandom.com'](https://tdutr.fandom.com') -- ./images (END - exit=0)
* 19:02 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=wwrtest3wikibeta --sleep=0 '--comment=Blowing up db servers with content from [https://tdutr.fandom.com'](https://tdutr.fandom.com') -- ./images (START)
* 19:02 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importDump --wiki=wwrtest3wikibeta --no-updates --username-prefix=fandom:tdutr -- ./tdutr.xml (END - exit=0)
* 18:58 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importDump --wiki=wwrtest3wikibeta --no-updates --username-prefix=fandom:tdutr -- ./tdutr.xml (START)
* 18:58 MirahezeLSBot: [wwr@test151] Starting import for wwrtest3wikibeta (XML: ./tdutr.xml; Images: ./images) (START)

## 2026-03-11 

* 02:55 MirahezeLSBot: [universalomega@mwtask181] finished deploy of {'versions': '1.45', 'upgrade_extensions': 'CreateWiki'} to all - SUCCESS in 26s
* 02:55 MirahezeLSBot: [universalomega@mwtask181] starting deploy of {'versions': '1.45', 'upgrade_extensions': 'CreateWiki'} to all
* 01:40 MirahezeLSBot: [universalomega@test151] finished deploy of {'force_upgrade': True, 'versions': '1.45', 'upgrade_extensions': 'MirahezeMagic'} to test151 - SUCCESS in 0s
* 01:40 MirahezeLSBot: [universalomega@test151] starting deploy of {'force_upgrade': True, 'versions': '1.45', 'upgrade_extensions': 'MirahezeMagic'} to test151
* 01:40 MirahezeLSBot: [universalomega@test151] DEPLOY ABORTED: Non-Zero Exit Code in prep, see output.
* 01:40 MirahezeLSBot: [universalomega@test151] starting deploy of {'versions': '1.45', 'upgrade_extensions': 'MirahezeMagic'} to test151

## 2026-03-10 

* 23:27 MirahezeLSBot: [petramagna@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 23:27 MirahezeLSBot: [petramagna@test151] starting deploy of {'config': True} to test151
* 23:22 MirahezeLSBot: [petramagna@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 23:22 MirahezeLSBot: [petramagna@test151] starting deploy of {'config': True} to test151
* 21:34 MirahezeLSBot: [pixldev@test151] finished deploy of {'force_upgrade': True, 'versions': '1.45', 'upgrade_extensions': 'CreateWiki'} to test151 - SUCCESS in 0s
* 21:34 MirahezeLSBot: [pixldev@test151] starting deploy of {'force_upgrade': True, 'versions': '1.45', 'upgrade_extensions': 'CreateWiki'} to test151
* 21:30 MirahezeLSBot: [pixldev@test151] DEPLOY ABORTED: Non-Zero Exit Code in prep, see output.
* 21:30 MirahezeLSBot: [pixldev@test151] starting deploy of {'force_upgrade': True, 'versions': '1.45', 'upgrade_extensions': 'CreateWiki'} to test151
* 21:28 MirahezeLSBot: [pixldev@test151] DEPLOY ABORTED: Non-Zero Exit Code in prep, see output.
* 21:28 MirahezeLSBot: [pixldev@test151] starting deploy of {'force_upgrade': True, 'versions': '1.45', 'upgrade_extensions': 'CreateWiki'} to test151
* 21:27 MirahezeLSBot: [pixldev@test151] DEPLOY ABORTED: Non-Zero Exit Code in prep, see output.
* 21:27 MirahezeLSBot: [pixldev@test151] starting deploy of {'force_upgrade': True, 'versions': '1.45', 'upgrade_extensions': 'CreateWiki'} to test151
* 21:25 MirahezeLSBot: [pixldev@test151] DEPLOY ABORTED: Non-Zero Exit Code in prep, see output.
* 21:25 MirahezeLSBot: [pixldev@test151] starting deploy of {'force_upgrade': True, 'versions': '1.45', 'upgrade_extensions': 'CreateWiki'} to test151
* 21:19 MirahezeLSBot: [pixldev@test151] finished deploy of {'force_upgrade': True, 'versions': '1.45', 'upgrade_extensions': 'CreateWiki'} to test151 - SUCCESS in 0s
* 21:19 MirahezeLSBot: [pixldev@test151] starting deploy of {'force_upgrade': True, 'versions': '1.45', 'upgrade_extensions': 'CreateWiki'} to test151
* 20:36 MirahezeLSBot: [pixldev@test151] finished deploy of {'world': True, 'folders': '1.45/extensions/CreateWiki', 'versions': '1.45'} to test151 - SUCCESS in 29s
* 20:35 MirahezeLSBot: [pixldev@test151] starting deploy of {'world': True, 'folders': '1.45/extensions/CreateWiki', 'versions': '1.45'} to test151
* 20:22 MirahezeLSBot: [pixldev@test151] finished deploy of {'folders': '1.45/extensions/CreateWiki'} to test151 - SUCCESS in 0s
* 20:22 MirahezeLSBot: [pixldev@test151] starting deploy of {'folders': '1.45/extensions/CreateWiki'} to test151
* 20:18 MirahezeLSBot: [pixldev@test151] finished deploy of {'folders': '1.45/extensions/CreateWiki'} to test151 - SUCCESS in 0s
* 20:18 MirahezeLSBot: [pixldev@test151] starting deploy of {'folders': '1.45/extensions/CreateWiki'} to test151
* 20:14 MirahezeLSBot: [pixldev@test151] finished deploy of {'versions': '1.45', 'upgrade_extensions': 'CreateWiki'} to test151 - SUCCESS in 1s
* 20:14 MirahezeLSBot: [pixldev@test151] starting deploy of {'versions': '1.45', 'upgrade_extensions': 'CreateWiki'} to test151
* 20:09 MirahezeLSBot: [pixldev@test151] finished deploy of {'pull': 'config', 'config': True} to test151 - SUCCESS in 0s
* 20:08 MirahezeLSBot: [pixldev@test151] starting deploy of {'pull': 'config', 'config': True} to test151
* 20:08 MirahezeLSBot: [pixldev@test151] DEPLOY ABORTED: Canary check failed for meta.mirabeta.org@localhost
* 20:08 MirahezeLSBot: [pixldev@test151] starting deploy of {'config': True} to test151
* 20:02 MirahezeLSBot: [pixldev@test151] DEPLOY ABORTED: Canary check failed for meta.mirabeta.org@localhost
* 20:02 MirahezeLSBot: [pixldev@test151] starting deploy of {'config': True} to test151
* 16:54 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RenameDatabase --wiki=loginwikibeta --rename --old=wwrtest2wikibeta --new=wwrtest3wikibeta --user=TheWWRNerdGuy (END - exit=0)
* 16:24 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php CreateWiki:SetContainersAccess --wiki=wwrtest2wikibeta (END - exit=0)
* 16:20 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RenameDatabase --wiki=loginwikibeta --rename --old=wwrtestwikibeta --new=wwrtest2wikibeta --user=TheWWRNerdGuy (END - exit=0)
* 16:17 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RenameDatabase --wiki=loginwikibeta --old=wwrtestwikibeta --new=wwrtest2wikibeta --user=TheWWRNerdGuy (END - exit=0)
* 16:17 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RenameDatabase --wiki=loginwiki --old=wwrtestwikibeta --new=wwrtest2wikibeta --user=TheWWRNerdGuy (END - exit=512)
* 02:21 MirahezeLSBot: [pixldev@test151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php createAndPromote --wiki=metawikibeta PixDeVl --force --custom-groups assistant-steward (END - exit=0)
* 02:20 MirahezeLSBot: [pixldev@test151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php createAndPromote --wiki=metawikibeta PixDeVl --custom-groups assistant-steward (END - exit=256)

## 2026-03-09 

* 23:14 MirahezeLSBot: [universalomega@puppet181] Upgraded packages on mw203: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 23:14 MirahezeLSBot: [universalomega@puppet181] Upgraded packages on mwtask171: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 23:13 MirahezeLSBot: [universalomega@puppet181] Upgraded packages on mw182: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 23:13 MirahezeLSBot: [universalomega@puppet181] Upgraded packages on mw191: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 23:13 MirahezeLSBot: [universalomega@puppet181] Upgraded packages on mw201: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 23:12 MirahezeLSBot: [universalomega@puppet181] Upgraded packages on mwtask181: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 23:12 MirahezeLSBot: [universalomega@puppet181] Upgraded packages on mwtask151: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 23:12 MirahezeLSBot: [universalomega@puppet181] Upgraded packages on mw161: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 23:12 MirahezeLSBot: [universalomega@puppet181] Upgraded packages on mw181: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 23:11 MirahezeLSBot: [universalomega@puppet181] Upgraded packages on mw193: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 23:11 MirahezeLSBot: [universalomega@puppet181] Upgraded packages on mw183: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 23:11 MirahezeLSBot: [universalomega@puppet181] Upgraded packages on mw202: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 23:10 MirahezeLSBot: [universalomega@puppet181] Upgraded packages on mw173: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 23:10 MirahezeLSBot: [universalomega@puppet181] Upgraded packages on mw192: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 23:10 MirahezeLSBot: [universalomega@puppet181] Upgraded packages on mwtask161: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 23:09 MirahezeLSBot: [universalomega@puppet181] Upgraded packages on mw163: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 23:09 MirahezeLSBot: [universalomega@puppet181] Upgraded packages on mw162: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 23:09 MirahezeLSBot: [universalomega@puppet181] Upgraded packages on mw171: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 23:09 MirahezeLSBot: [universalomega@puppet181] Upgraded packages on mw172: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 23:08 MirahezeLSBot: [universalomega@puppet181] Upgraded packages on mw153: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 23:08 MirahezeLSBot: [universalomega@puppet181] Upgraded packages on mw152: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 23:08 MirahezeLSBot: [universalomega@puppet181] Upgraded packages on mw151: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 23:08 MirahezeLSBot: [universalomega@puppet181] Upgraded packages on test151: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 21:58 MirahezeLSBot: [wwr@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 21:58 MirahezeLSBot: [wwr@test151] starting deploy of {'config': True} to test151
* 21:54 MirahezeLSBot: [wwr@test151] finished deploy of {'config': True, 'l10n': True, 'extension_list': True, 'versions': '1.45', 'upgrade_extensions': 'Bucket'} to test151 - SUCCESS in 51s
* 21:53 MirahezeLSBot: [wwr@test151] starting deploy of {'config': True, 'l10n': True, 'extension_list': True, 'versions': '1.45', 'upgrade_extensions': 'Bucket'} to test151
* 21:53 MirahezeLSBot: [wwr@test151] DEPLOY ABORTED: Non-Zero Exit Code in prep, see output.
* 21:53 MirahezeLSBot: [wwr@test151] starting deploy of {'config': True, 'l10n': True, 'extension_list': True, 'versions': '1.45', 'upgrade_extensions': 'Bucket'} to test151
* 21:50 MirahezeLSBot: [wwr@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 21:50 MirahezeLSBot: [wwr@test151] starting deploy of {'config': True} to test151
* 21:40 MirahezeLSBot: [wwr@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 21:40 MirahezeLSBot: [wwr@test151] starting deploy of {'config': True} to test151
* 21:38 MirahezeLSBot: [wwr@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 21:37 MirahezeLSBot: [wwr@test151] starting deploy of {'config': True} to test151
* 21:37 MirahezeLSBot: [wwr@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 21:37 MirahezeLSBot: [wwr@test151] starting deploy of {'config': True} to test151
* 19:12 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php CreateWiki:SetContainersAccess --wiki=diaryofacitygirlwiki (END - exit=0)
* 19:11 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RenameDatabase --wiki=loginwiki --rename --old=thediaryofmaxinewiki --new=diaryofacitygirlwiki --user=MacFan4000 (END - exit=0)
* 19:06 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php CreateWiki:SetContainersAccess --wiki=aerrawiki (END - exit=0)
* 19:06 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RenameDatabase --wiki=loginwiki --rename --old=aerrheawiki --new=aerrawiki --user=MacFan4000 (END - exit=0)
* 18:59 MirahezeLSBot: [skye@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 26s
* 18:58 MirahezeLSBot: [skye@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 18:52 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php CreateWiki:SetContainersAccess --wiki=realmzwiki (END - exit=0)
* 18:50 MacFan4000: rename the cargodb for the same wiki then (db151) DROP DATABASE realmzctionarywikicargo
* 18:34 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RenameDatabase --wiki=loginwiki --rename --old=realmzctionarywiki --new=realmzwiki --user=MacFan4000 (END - exit=0)
* 18:30 MacFan4000: (db151) DROP DATABASE realmzwiki;
* 18:29 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php CreateWiki:DeleteWiki --wiki=loginwiki --delete --deletewiki realmzwiki (END - exit=0)
* 18:04 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php CreateWiki:SetContainersAccess --wiki=sonexemewiki (END - exit=0)
* 18:03 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RenameDatabase --wiki=loginwiki --rename --old=guduwiki --new=sonexemewiki --user=MacFan4000 (END - exit=0)
* 18:00 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RenameDatabase --wiki=loginwiki --rename --old=guruwiki --new=sonexemewiki --user=MacFan4000 (END - exit=256)
* 17:56 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php CreateWiki:SetContainersAccess --wiki=yuriwiki (END - exit=0)
* 17:55 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RenameDatabase --wiki=loginwiki --rename --old=himewiki --new=yuriwiki --user=MacFan4000 (END - exit=0)
* 17:44 Universal Omega: deployed local patch to TSPortal on reports171 and disabled puppet until after 00:00 3/10 UTC for testing PR #62
* 01:54 MirahezeLSBot: [pixldev@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 01:53 MirahezeLSBot: [pixldev@test151] starting deploy of {'config': True} to test151
* 01:52 MirahezeLSBot: [pixldev@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 01:52 MirahezeLSBot: [pixldev@test151] starting deploy of {'config': True} to test151
* 01:41 MirahezeLSBot: [pixldev@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 01:41 MirahezeLSBot: [pixldev@test151] starting deploy of {'config': True} to test151
* 01:39 MirahezeLSBot: [pixldev@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 01:39 MirahezeLSBot: [pixldev@test151] starting deploy of {'config': True} to test151
* 01:21 MirahezeLSBot: [pixldev@test151] finished deploy of {'pull': 'config', 'config': True} to test151 - SUCCESS in 0s
* 01:21 MirahezeLSBot: [pixldev@test151] starting deploy of {'pull': 'config', 'config': True} to test151
* 00:18 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php refreshLinks --wiki=battlenationswiki (END - exit=0)

## 2026-03-08 

* 23:11 MirahezeLSBot: [petramagna@mwtask181] finished deploy of {'versions': '1.45', 'upgrade_extensions': 'RenderBlocking'} to all - SUCCESS in 24s
* 23:10 MirahezeLSBot: [petramagna@mwtask181] starting deploy of {'versions': '1.45', 'upgrade_extensions': 'RenderBlocking'} to all
* 22:01 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php refreshLinks --wiki=battlenationswiki (START)
* 22:01 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php refreshlinks --wiki=battlenationswiki (END - exit=256)
* 22:01 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php refreshlinks --wiki=battlenationswiki (START)
* 21:17 Universal Omega: added reader roles for pixldev and wwr in Graylog
* 21:13 MirahezeLSBot: [somerandomdeveloper@mwtask181] finished deploy of {'versions': '1.45', 'upgrade_extensions': 'Bucket'} to all - SUCCESS in 27s
* 21:13 MirahezeLSBot: [somerandomdeveloper@mwtask181] starting deploy of {'versions': '1.45', 'upgrade_extensions': 'Bucket'} to all
* 21:12 MirahezeLSBot: [somerandomdeveloper@test151] finished deploy of {'versions': '1.45', 'upgrade_extensions': 'Bucket'} to test151 - SUCCESS in 0s
* 21:12 MirahezeLSBot: [somerandomdeveloper@test151] starting deploy of {'versions': '1.45', 'upgrade_extensions': 'Bucket'} to test151
* 21:07 MirahezeLSBot: [somerandomdeveloper@test151] DEPLOY ABORTED: Non-Zero Exit Code in prep, see output.
* 21:07 MirahezeLSBot: [somerandomdeveloper@test151] starting deploy of {'versions': '1.45', 'upgrade_extensions': 'Bucket'} to test151
* 20:35 Universal Omega: created ldap accounts for wwr and pixldev

## 2026-03-07 

* 22:36 MirahezeLSBot: [blankeclair@mwtask181] finished deploy of {'l10n': True, 'versions': '1.45', 'upgrade_extensions': 'ConfirmEdit'} to all - SUCCESS in 120s
* 22:34 MirahezeLSBot: [blankeclair@mwtask181] starting deploy of {'l10n': True, 'versions': '1.45', 'upgrade_extensions': 'ConfirmEdit'} to all
* 20:23 MirahezeLSBot: [paladox@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 23s
* 20:23 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 20:23 MirahezeLSBot: [paladox@test151] DEPLOY ABORTED: Non-Zero Exit Code in prep, see output.
* 20:23 MirahezeLSBot: [paladox@test151] starting deploy of {'pull': 'config', 'config': True} to test151
* 19:37 MirahezeLSBot: [wwr@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 19:37 MirahezeLSBot: [wwr@test151] starting deploy of {'config': True} to test151
* 19:37 MirahezeLSBot: [wwr@test151] DEPLOY ABORTED: Non-Zero Exit Code in prep, see output.
* 19:37 MirahezeLSBot: [wwr@test151] starting deploy of {'l10n': True, 'extension_list': True, 'force_upgrade': True, 'versions': '1.45', 'upgrade_extensions': 'Bucket'} to test151
* 18:51 MirahezeLSBot: [universalomega@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 24s
* 18:51 MirahezeLSBot: [universalomega@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 16:07 MirahezeLSBot: [paladox@mwtask181] finished deploy of {'l10n': True, 'versions': '1.45', 'upgrade_extensions': 'PortableInfobox'} to all - SUCCESS in 543s
* 15:58 MirahezeLSBot: [paladox@test151] finished deploy of {'l10n': True, 'versions': '1.45', 'upgrade_extensions': 'PortableInfobox'} to test151 - SUCCESS in 57s
* 15:58 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'l10n': True, 'versions': '1.45', 'upgrade_extensions': 'PortableInfobox'} to all
* 15:57 MirahezeLSBot: [paladox@test151] starting deploy of {'l10n': True, 'versions': '1.45', 'upgrade_extensions': 'PortableInfobox'} to test151

## 2026-03-06 

* 22:25 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php Bucket:RefreshAllBuckets --wiki=buckettestwikibeta (END - exit=0)
* 05:34 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php refreshLinks --wiki=fischwiki 10300 (END - exit=0)
* 04:28 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php refreshLinks --wiki=fischwiki 10300 (START)
* 04:10 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php refreshLinks --wiki=fischwiki (END - exit=35072)
* 02:43 Universal Omega: sudo apt purge -y cpufrequtils on cloud*
* 02:34 Universal Omega: remove /etc/powerdns/recursor.conf on all servers
* 00:58 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php refreshLinks --wiki=fischwiki (START)

## 2026-03-05 

* 22:43 Skye: (excluding cloud21)
* 22:42 Universal Omega: upgraded cloud* to Proxmox 9/Debian Trixie
* 22:41 MirahezeLSBot: [universalomega@mwtask181] finished deploy of {'pull': 'config', 'config': True, 'force': True} to all - SUCCESS in 18s
* 20:00 MirahezeLSBot: [universalomega@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 15:31 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php ManageWiki:PopulateDefaults --wiki=buckettestwikibeta (END - exit=256)
* 15:30 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php ManageWiki:PopulateNamespacesWithDefaults --wiki=buckettestwikibeta (END - exit=0)
* 13:06 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php ManageWiki:PopulateNamespaces --wiki=buckettestwikibeta --force (END - exit=0)
* 13:05 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php ManageWiki:PopulateNamespaces --wiki=buckettestwikibeta (END - exit=256)
* 00:52 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php shell --wiki=buckettestwikibeta (END - exit=0)

## 2026-03-04 

* 21:45 MirahezeLSBot: [petramagna@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:GenerateMirahezeSitemap --wiki=superstarracerswiki (END - exit=0)
* 18:53 @paladox: created a hack in puppet folder on puppet181
* 06:34 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php CreateWiki:SetContainersAccess --wiki=zeroerawiki (END - exit=0)

## 2026-03-03 

* 15:43 MirahezeLSBot: [petramagna@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php /srv/mediawiki/1.45/extensions/TitleKey/maintenance/rebuildTitleKeys.php --wiki=arcaeawiki (END - exit=0)
* 15:43 MirahezeLSBot: [petramagna@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php /srv/mediawiki/1.45/extensions/TitleKey/maintenance/rebuildTitleKeys.php --wiki=infalsuswiki (END - exit=0)
* 12:53 MirahezeLSBot: [wwr@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 12:53 MirahezeLSBot: [wwr@test151] starting deploy of {'config': True} to test151
* 12:50 MirahezeLSBot: [wwr@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 12:50 MirahezeLSBot: [wwr@test151] starting deploy of {'config': True} to test151
* 10:48 MirahezeLSBot: [wwr@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 10:48 MirahezeLSBot: [wwr@test151] starting deploy of {'config': True} to test151
* 10:32 MirahezeLSBot: [wwr@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 10:31 MirahezeLSBot: [wwr@test151] starting deploy of {'config': True} to test151
* 10:31 MirahezeLSBot: [wwr@test151] finished deploy of {'l10n': True, 'extension_list': True, 'force_upgrade': True, 'versions': '1.45', 'upgrade_extensions': 'Bucket'} to test151 - SUCCESS in 53s
* 10:30 MirahezeLSBot: [wwr@test151] starting deploy of {'l10n': True, 'extension_list': True, 'force_upgrade': True, 'versions': '1.45', 'upgrade_extensions': 'Bucket'} to test151
* 10:30 MirahezeLSBot: [wwr@test151] DEPLOY ABORTED: Non-Zero Exit Code in prep, see output.
* 10:30 MirahezeLSBot: [wwr@test151] starting deploy of {'pull': 'config', 'config': True, 'l10n': True, 'extension_list': True, 'force_upgrade': True, 'versions': '1.45', 'upgrade_extensions': 'Bucket'} to test151
* 01:40 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php Bucket:RefreshAllBuckets --wiki=exttestwikibeta (END - exit=0)
* 01:07 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php Bucket:SetupDBPermission --wiki=exttestwikibeta (END - exit=0)
* 00:48 MirahezeLSBot: [skye@test151] finished deploy of {'folders': '1.45/extensions/Bucket'} to test151 - SUCCESS in 0s
* 00:48 MirahezeLSBot: [skye@test151] starting deploy of {'folders': '1.45/extensions/Bucket'} to test151
* 00:38 MirahezeLSBot: [skye@test151] finished deploy of {'folders': '1.45/extensions/Bucket'} to test151 - SUCCESS in 0s
* 00:38 MirahezeLSBot: [skye@test151] starting deploy of {'folders': '1.45/extensions/Bucket'} to test151
* 00:34 MirahezeLSBot: [skye@test151] finished deploy of {'folders': '1.45/extensions/Bucket'} to test151 - SUCCESS in 0s
* 00:34 MirahezeLSBot: [skye@test151] starting deploy of {'folders': '1.45/extensions/Bucket'} to test151
* 00:01 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php Bucket:SetupDBPermission --wiki=exttestwikibeta (END - exit=0)
* 00:01 MirahezeLSBot: [wwr@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 00:01 MirahezeLSBot: [wwr@test151] starting deploy of {'config': True} to test151

## 2026-03-02 

* 23:43 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php Bucket:SetupDBPermission --wiki=exttestwikibeta (END - exit=0)
* 23:40 MirahezeLSBot: [wwr@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 23:40 MirahezeLSBot: [wwr@test151] starting deploy of {'config': True} to test151
* 23:38 MirahezeLSBot: [skye@test151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php Bucket:SetupDBPermission --wiki=skye2wikibeta (END - exit=0)
* 23:34 MirahezeLSBot: [wwr@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 23:34 MirahezeLSBot: [wwr@test151] starting deploy of {'config': True} to test151
* 23:30 MirahezeLSBot: [wwr@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 23:30 MirahezeLSBot: [wwr@test151] starting deploy of {'config': True} to test151
* 23:28 MirahezeLSBot: [wwr@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 23:28 MirahezeLSBot: [wwr@test151] starting deploy of {'config': True} to test151
* 23:27 MirahezeLSBot: [wwr@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 23:27 MirahezeLSBot: [wwr@test151] starting deploy of {'config': True} to test151
* 23:13 MirahezeLSBot: [wwr@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 23:13 MirahezeLSBot: [wwr@test151] starting deploy of {'config': True} to test151
* 23:12 MirahezeLSBot: [wwr@test151] finished deploy of {'l10n': True, 'extension_list': True, 'force_upgrade': True, 'versions': '1.45', 'upgrade_extensions': 'Bucket'} to test151 - SUCCESS in 242s
* 23:08 MirahezeLSBot: [wwr@test151] starting deploy of {'l10n': True, 'extension_list': True, 'force_upgrade': True, 'versions': '1.45', 'upgrade_extensions': 'Bucket'} to test151
* 22:54 MirahezeLSBot: [wwr@test151] DEPLOY ABORTED: Non-Zero Exit Code in prep, see output.
* 22:51 MirahezeLSBot: [wwr@test151] starting deploy of {'l10n': True, 'extension_list': True, 'force_upgrade': True, 'versions': '1.45', 'upgrade_extensions': 'Bucket'} to test151
* 22:50 MirahezeLSBot: [wwr@test151] finished deploy of {'versions': '1.45', 'upgrade_extensions': 'Bucket'} to test151 - SUCCESS in 0s
* 22:49 MirahezeLSBot: [wwr@test151] starting deploy of {'versions': '1.45', 'upgrade_extensions': 'Bucket'} to test151
* 22:47 MirahezeLSBot: [wwr@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 22:46 MirahezeLSBot: [wwr@test151] starting deploy of {'config': True} to test151
* 22:40 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php createAndPromote --wiki=metawikibeta TheWWRNerdGuy --interface-admin --bureaucrat --sysop --force (END - exit=0)
* 22:33 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php createAndPromote --wiki=metawikibeta TheWWRNerdGuy --interface-admin --force (END - exit=0)
* 20:57 MirahezeLSBot: [skye@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 33s
* 20:57 MirahezeLSBot: [skye@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 19:12 MirahezeLSBot: [skye@mwtask171] Finished import for pokemoninfinitywiki (XML: None; Images: .) (END - exit=0)
* 19:12 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php initSiteStats --wiki=pokemoninfinitywiki --update (END - exit=0)
* 19:12 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php initSiteStats --wiki=pokemoninfinitywiki --update (START)
* 19:12 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=pokemoninfinitywiki --sleep=1 '--comment=Importing images from [https://p-infinity.fandom.com/](https://p-infinity.fandom.com/) ([T15038](https://meta.miraheze.org/wiki/phorge:T15038))' -- . (END - exit=0)
* 16:07 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=pokemoninfinitywiki --sleep=1 '--comment=Importing images from [https://p-infinity.fandom.com/](https://p-infinity.fandom.com/) ([T15038](https://meta.miraheze.org/wiki/phorge:T15038))' -- . (START)
* 16:07 MirahezeLSBot: [skye@mwtask171] Starting import for pokemoninfinitywiki (XML: None; Images: .) (START)

## 2026-03-01 

* 17:41 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php CreateWiki:SetContainersAccess --wiki=icarlywiki (END - exit=0)
* 13:11 @paladox: upgrade phorge on phorge171
* 09:34 MirahezeLSBot: [petramagna@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 27s
* 09:33 MirahezeLSBot: [petramagna@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 09:32 MirahezeLSBot: [petramagna@test151] finished deploy of {'pull': 'config', 'config': True} to test151 - SUCCESS in 0s
* 09:32 MirahezeLSBot: [petramagna@test151] starting deploy of {'pull': 'config', 'config': True} to test151
* 00:00 MirahezeLSBot: [www-data@mwtask181] Began automatic backing up

----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:Server_admin_log/2026-03)**