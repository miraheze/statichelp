---
title: Tech:Server admin log/2026-06
---

`{{ {{Server admin log/nav}} }}`

## 2026-06-30 

* 21:13 MirahezeLSBot: [somerandomdeveloper@mwtask181] finished deploy of {'versions': '1.45', 'upgrade_extensions': 'Chart'} to all - SUCCESS in 38s
* 21:12 MirahezeLSBot: [somerandomdeveloper@mwtask181] starting deploy of {'versions': '1.45', 'upgrade_extensions': 'Chart'} to all
* 21:12 MirahezeLSBot: [somerandomdeveloper@test151] finished deploy of {'versions': ['1.45', '1.46'], 'upgrade_extensions': 'Chart'} to test151 - SUCCESS in 1s
* 21:12 MirahezeLSBot: [somerandomdeveloper@test151] starting deploy of {'versions': ['1.45', '1.46'], 'upgrade_extensions': 'Chart'} to test151
* 19:10 Reception123: DELETED and DROPPED [https://issue-tracker.miraheze.org/P597](https://issue-tracker.miraheze.org/P597)
* 09:42 MirahezeLSBot: [reception@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:CheckWikiDatabases --wiki=loginwiki --delete (END - exit=256)
* 06:09 Reception123: begin dropping previously deleted wikis
* 06:08 MirahezeLSBot: [reception@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php /srv/mediawiki/1.45/maintenance/MirahezeMagic:CheckWikiDatabases.php --wiki=loginwiki --delete (END - exit=256)
* 04:05 MirahezeLSBot: [reception@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php CreateWiki:DeleteWikis --wiki=loginwiki --delete Reception123 (END - exit=0)

## 2026-06-29 

* 20:49 MirahezeLSBot: [somerandomdeveloper@test151] finished deploy of {'force_upgrade': True, 'versions': ['1.45', '1.46'], 'upgrade_extensions': 'Timeline'} to test151 - SUCCESS in 1s
* 20:49 MirahezeLSBot: [somerandomdeveloper@test151] starting deploy of {'force_upgrade': True, 'versions': ['1.45', '1.46'], 'upgrade_extensions': 'Timeline'} to test151
* 20:49 MirahezeLSBot: [somerandomdeveloper@test151] finished deploy of {'versions': ['1.45', '1.46'], 'upgrade_extensions': 'Timeline'} to test151 - SUCCESS in 1s
* 20:49 MirahezeLSBot: [somerandomdeveloper@test151] starting deploy of {'versions': ['1.45', '1.46'], 'upgrade_extensions': 'Timeline'} to test151
* 20:48 MirahezeLSBot: [somerandomdeveloper@mwtask181] finished deploy of {'versions': '1.45', 'upgrade_extensions': 'Timeline'} to all - SUCCESS in 29s
* 20:48 MirahezeLSBot: [somerandomdeveloper@test151] DEPLOY ABORTED: Non-Zero Exit Code in prep, see output.
* 20:48 MirahezeLSBot: [somerandomdeveloper@test151] starting deploy of {'versions': ['1.45', '1.46'], 'upgrade_extensions': 'Timeline'} to test151
* 20:48 MirahezeLSBot: [somerandomdeveloper@mwtask181] starting deploy of {'versions': '1.45', 'upgrade_extensions': 'Timeline'} to all
* 14:55 MirahezeLSBot: [somerandomdeveloper@test151] finished deploy of {'versions': ['1.45', '1.46'], 'upgrade_extensions': 'CentralAuth'} to test151 - SUCCESS in 1s
* 14:55 MirahezeLSBot: [somerandomdeveloper@test151] starting deploy of {'versions': ['1.45', '1.46'], 'upgrade_extensions': 'CentralAuth'} to test151
* 14:55 MirahezeLSBot: [somerandomdeveloper@mwtask181] finished deploy of {'versions': '1.45', 'upgrade_extensions': 'UrlShortener'} to all - SUCCESS in 25s
* 14:54 MirahezeLSBot: [somerandomdeveloper@mwtask181] starting deploy of {'versions': '1.45', 'upgrade_extensions': 'UrlShortener'} to all
* 14:54 MirahezeLSBot: [somerandomdeveloper@test151] finished deploy of {'versions': ['1.45', '1.46'], 'upgrade_extensions': 'UrlShortener'} to test151 - SUCCESS in 1s
* 14:54 MirahezeLSBot: [somerandomdeveloper@test151] starting deploy of {'versions': ['1.45', '1.46'], 'upgrade_extensions': 'UrlShortener'} to test151
* 13:35 SomeRandomDeveloper: dropped the patches for T15453 and T15401 on prod and upgraded the extension
* 11:14 SomeRandomDeveloper: deploy updated patch for T15587 (again)
* 10:53 SomeRandomDeveloper: deploy updated patch for T15587
* 10:29 MirahezeLSBot: [somerandomdeveloper@mwtask181] finished deploy of {'versions': '1.45', 'upgrade_extensions': 'AbuseFilter'} to all - SUCCESS in 30s
* 10:29 MirahezeLSBot: [somerandomdeveloper@mwtask181] starting deploy of {'versions': '1.45', 'upgrade_extensions': 'AbuseFilter'} to all
* 10:29 MirahezeLSBot: [somerandomdeveloper@test151] finished deploy of {'versions': ['1.45', '1.46'], 'upgrade_extensions': 'AbuseFilter'} to test151 - SUCCESS in 6s
* 10:29 MirahezeLSBot: [somerandomdeveloper@test151] starting deploy of {'versions': ['1.45', '1.46'], 'upgrade_extensions': 'AbuseFilter'} to test151
* 10:18 MirahezeLSBot: [somerandomdeveloper@mwtask181] finished deploy of {'versions': '1.45', 'upgrade_extensions': 'SyntaxHighlight_GeSHi'} to all - SUCCESS in 26s
* 10:17 MirahezeLSBot: [somerandomdeveloper@mwtask181] starting deploy of {'versions': '1.45', 'upgrade_extensions': 'SyntaxHighlight_GeSHi'} to all
* 10:17 MirahezeLSBot: [somerandomdeveloper@test151] finished deploy of {'versions': ['1.45', '1.46'], 'upgrade_extensions': 'SyntaxHighlight_GeSHi'} to test151 - SUCCESS in 2s
* 10:17 MirahezeLSBot: [somerandomdeveloper@test151] starting deploy of {'versions': ['1.45', '1.46'], 'upgrade_extensions': 'SyntaxHighlight_GeSHi'} to test151
* 10:04 SomeRandomDeveloper: deploy patch for T15587 to prod

## 2026-06-28 

* 19:37 @paladox: upgrade phorge on phorge171
* 18:02 SomeRandomDeveloper: deployed patch for T15587 on beta
* 17:26 MirahezeLSBot: [petramagna@test151] finished deploy of {'folders': '1.46/extensions/PortableInfobox', 'ignore_time': True} to test151 - SUCCESS in 0s
* 17:26 MirahezeLSBot: [petramagna@test151] starting deploy of {'folders': '1.46/extensions/PortableInfobox', 'ignore_time': True} to test151
* 17:25 MirahezeLSBot: [petramagna@test151] finished deploy of {'versions': '1.46', 'upgrade_extensions': 'PortableInfobox'} to test151 - SUCCESS in 0s
* 17:25 MirahezeLSBot: [petramagna@test151] starting deploy of {'versions': '1.46', 'upgrade_extensions': 'PortableInfobox'} to test151
* 17:25 MirahezeLSBot: [petramagna@test151] finished deploy of {'versions': ['1.45', '1.46'], 'upgrade_extensions': 'PortableInfobox'} to test151 - SUCCESS in 1s
* 17:25 MirahezeLSBot: [petramagna@test151] starting deploy of {'versions': ['1.45', '1.46'], 'upgrade_extensions': 'PortableInfobox'} to test151
* 17:14 MirahezeLSBot: [reception@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php CreateWiki:DeleteWikis --wiki=loginwiki --delete Reception123 (END - exit=33280)
* 17:14 MirahezeLSBot: [reception@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php CreateWiki:DeleteWikis --wiki=loginwiki --delete Reception123 (END - exit=33280)
* 14:40 MirahezeLSBot: [somerandomdeveloper@mwtask181] finished deploy of {'versions': '1.45', 'upgrade_extensions': 'CommentStreams'} to all - SUCCESS in 28s
* 14:40 MirahezeLSBot: [somerandomdeveloper@mwtask181] starting deploy of {'versions': '1.45', 'upgrade_extensions': 'CommentStreams'} to all
* 14:39 MirahezeLSBot: [somerandomdeveloper@test151] finished deploy of {'versions': ['1.45', '1.46'], 'upgrade_extensions': 'CommentStreams'} to test151 - SUCCESS in 1s
* 14:39 MirahezeLSBot: [somerandomdeveloper@test151] starting deploy of {'versions': ['1.45', '1.46'], 'upgrade_extensions': 'CommentStreams'} to test151

## 2026-06-27 

* 21:26 MirahezeLSBot: [void@puppet181] Upgraded packages on llm191: xserver-xorg-core and xserver-common
* 21:18 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask181: xserver-xorg-core, xserver-common, and xvfb
* 21:18 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask161: xserver-xorg-core, xserver-common, and xvfb
* 21:17 MirahezeLSBot: [void@puppet181] Upgraded packages on mw183: xserver-xorg-core, xserver-common, and xvfb
* 21:17 MirahezeLSBot: [void@puppet181] Upgraded packages on mw202: xserver-xorg-core, xserver-common, and xvfb
* 21:17 MirahezeLSBot: [void@puppet181] Upgraded packages on mw201: xserver-xorg-core, xserver-common, and xvfb
* 21:16 MirahezeLSBot: [void@puppet181] Upgraded packages on mw193: xserver-xorg-core, xserver-common, and xvfb
* 21:16 MirahezeLSBot: [void@puppet181] Upgraded packages on mw203: xserver-xorg-core, xserver-common, and xvfb
* 21:16 MirahezeLSBot: [void@puppet181] Upgraded packages on mw192: xserver-xorg-core, xserver-common, and xvfb
* 21:15 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask171: xserver-xorg-core, xserver-common, and xvfb
* 21:15 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask151: xserver-xorg-core, xserver-common, and xvfb
* 21:15 MirahezeLSBot: [void@puppet181] Upgraded packages on test151: xserver-xorg-core, xserver-common, and xvfb
* 21:14 MirahezeLSBot: [void@puppet181] Upgraded packages on mw182: xserver-xorg-core, xserver-common, and xvfb
* 21:14 MirahezeLSBot: [void@puppet181] Upgraded packages on mw173: xserver-xorg-core, xserver-common, and xvfb
* 21:14 MirahezeLSBot: [void@puppet181] Upgraded packages on mw181: xserver-xorg-core, xserver-common, and xvfb
* 21:13 MirahezeLSBot: [void@puppet181] Upgraded packages on mw191: xserver-xorg-core, xserver-common, and xvfb
* 21:13 MirahezeLSBot: [void@puppet181] Upgraded packages on mw171: xserver-xorg-core, xserver-common, and xvfb
* 21:13 MirahezeLSBot: [void@puppet181] Upgraded packages on mw172: xserver-xorg-core, xserver-common, and xvfb
* 21:12 MirahezeLSBot: [void@puppet181] Upgraded packages on mw161: xserver-xorg-core, xserver-common, and xvfb
* 21:12 MirahezeLSBot: [void@puppet181] Upgraded packages on mw163: xserver-xorg-core, xserver-common, and xvfb
* 21:12 MirahezeLSBot: [void@puppet181] Upgraded packages on mw162: xserver-xorg-core, xserver-common, and xvfb
* 21:11 MirahezeLSBot: [void@puppet181] Upgraded packages on mw151: xserver-xorg-core, xserver-common, and xvfb
* 21:11 MirahezeLSBot: [void@puppet181] Upgraded packages on mw152: xserver-xorg-core, xserver-common, and xvfb
* 21:11 MirahezeLSBot: [void@puppet181] Upgraded packages on mw153: xserver-xorg-core, xserver-common, and xvfb

## 2026-06-26 

* 13:04 MirahezeLSBot: [somerandomdeveloper@mwtask181] finished deploy of {'versions': '1.45', 'upgrade_extensions': 'PageForms'} to all - SUCCESS in 29s
* 13:04 MirahezeLSBot: [somerandomdeveloper@mwtask181] starting deploy of {'versions': '1.45', 'upgrade_extensions': 'PageForms'} to all
* 08:46 MirahezeLSBot: [petramagna@mwtask181] finished deploy of {'config': True, 'force': True} to all - SUCCESS in 19s
* 08:45 MirahezeLSBot: [petramagna@mwtask181] starting deploy of {'config': True, 'force': True} to all
* 08:45 MirahezeLSBot: [petramagna@mwtask181] DEPLOY ABORTED: Canary check failed for publictestwiki.com@localhost
* 08:45 MirahezeLSBot: [petramagna@mwtask181] starting deploy of {'config': True} to all
* 08:37 MirahezeLSBot: [petramagna@mwtask181] finished deploy of {'config': True, 'force': True} to all - SUCCESS in 18s
* 08:37 MirahezeLSBot: [petramagna@mwtask181] starting deploy of {'config': True, 'force': True} to all
* 01:28 SomeRandomDeveloper: sudo salt-ssh -E 'mw(153|152|183|193)' cmd.run 'rm /srv/mediawiki/cache/config-metawiki.php'
* 01:28 SomeRandomDeveloper: sudo salt-ssh -E 'mw(153|152|183|193)' cmd.run 'rm /srv/mediawiki/cache/metawiki.php'
* 00:37 MirahezeLSBot: [somerandomdeveloper@mwtask181] sudo -u www-data /usr/local/bin/foreachwikiindblist /tmp/semanticmediawiki.php /srv/mediawiki/1.45/maintenance/run.php SemanticMediaWiki:setupStore (END - exit=0)
* 00:22 MirahezeLSBot: [somerandomdeveloper@mwtask181] sudo -u www-data /usr/local/bin/foreachwikiindblist /tmp/semanticmediawiki.php /srv/mediawiki/1.45/maintenance/run.php SemanticMediaWiki:setupStore (START)
* 00:20 MirahezeLSBot: [somerandomdeveloper@test151] sudo -u www-data /usr/local/bin/foreachwikiindblist /tmp/semanticmediawiki.php /srv/mediawiki/1.46/maintenance/run.php SemanticMediaWiki:setupStore (END - exit=0)
* 00:20 MirahezeLSBot: [somerandomdeveloper@test151] sudo -u www-data /usr/local/bin/foreachwikiindblist /tmp/semanticmediawiki.php /srv/mediawiki/1.46/maintenance/run.php SemanticMediaWiki:setupStore (START)
* 00:19 MirahezeLSBot: [somerandomdeveloper@test151] sudo -u www-data /usr/local/bin/foreachwikiindblist /tmp/semanticmediawiki.php /srv/mediawiki/1.46/maintenance/run.php MirahezeMagic:GenerateExtensionDatabaseList metawiki --directory=/tmp (END - exit=256)
* 00:19 MirahezeLSBot: [somerandomdeveloper@test151] sudo -u www-data /usr/local/bin/foreachwikiindblist /tmp/semanticmediawiki.php /srv/mediawiki/1.46/maintenance/run.php MirahezeMagic:GenerateExtensionDatabaseList metawiki --directory=/tmp (START)
* 00:13 MirahezeLSBot: [somerandomdeveloper@test151] sudo -u www-data php /srv/mediawiki/1.46/maintenance/run.php SemanticMediaWiki:setupStore --wiki=smwtestwikibeta (END - exit=0)
* 00:12 MirahezeLSBot: [somerandomdeveloper@test151] finished deploy of {'versions': ['1.45', '1.46'], 'upgrade_extensions': 'SemanticMediaWiki'} to test151 - SUCCESS in 1s
* 00:12 MirahezeLSBot: [somerandomdeveloper@test151] starting deploy of {'versions': ['1.45', '1.46'], 'upgrade_extensions': 'SemanticMediaWiki'} to test151
* 00:08 MirahezeLSBot: [somerandomdeveloper@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php SemanticMediaWiki:setupStore --wiki=bluepageswiki (END - exit=0)

## 2026-06-25 

* 23:37 MirahezeLSBot: [somerandomdeveloper@test151] finished deploy of {'force_upgrade': True, 'versions': '1.46', 'upgrade_extensions': 'Bucket'} to test151 - SUCCESS in 1s
* 23:37 MirahezeLSBot: [somerandomdeveloper@test151] starting deploy of {'force_upgrade': True, 'versions': '1.46', 'upgrade_extensions': 'Bucket'} to test151
* 23:23 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject201: libssh2-1t64 and pdns-recursor
* 23:23 MirahezeLSBot: [void@puppet181] Upgraded packages on test151: libssh2-1t64 and pdns-recursor
* 23:23 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftproxy171: libssh2-1t64 and pdns-recursor
* 23:22 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftproxy161: libssh2-1t64 and pdns-recursor
* 23:22 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject191: libssh2-1t64 and pdns-recursor
* 23:22 MirahezeLSBot: [void@puppet181] Upgraded packages on ns2: libssh2-1t64
* 23:21 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject211: libssh2-1t64 and pdns-recursor
* 23:21 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject171: libssh2-1t64 and pdns-recursor
* 23:21 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject181: libssh2-1t64 and pdns-recursor
* 23:20 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject161: libssh2-1t64 and pdns-recursor
* 23:20 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftac171: libssh2-1t64 and pdns-recursor
* 23:20 MirahezeLSBot: [void@puppet181] Upgraded packages on os201: libssh2-1t64 and pdns-recursor
* 23:19 MirahezeLSBot: [void@puppet181] Upgraded packages on os191: libssh2-1t64 and pdns-recursor
* 23:19 MirahezeLSBot: [void@puppet181] Upgraded packages on puppet181: libssh2-1t64 and pdns-recursor
* 23:19 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject151: libssh2-1t64 and pdns-recursor
* 23:18 MirahezeLSBot: [void@puppet181] Upgraded packages on os161: libssh2-1t64 and pdns-recursor
* 23:18 MirahezeLSBot: [void@puppet181] Upgraded packages on os202: libssh2-1t64 and pdns-recursor
* 23:18 MirahezeLSBot: [void@puppet181] Upgraded packages on rdb191: libssh2-1t64 and pdns-recursor
* 23:17 MirahezeLSBot: [void@puppet181] Upgraded packages on os162: libssh2-1t64 and pdns-recursor
* 23:17 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask181: libssh2-1t64 and pdns-recursor
* 23:17 MirahezeLSBot: [void@puppet181] Upgraded packages on reports171: libssh2-1t64 and pdns-recursor
* 23:16 MirahezeLSBot: [void@puppet181] Upgraded packages on prometheus151: libssh2-1t64 and pdns-recursor
* 23:16 MirahezeLSBot: [void@puppet181] Upgraded packages on os151: libssh2-1t64 and pdns-recursor
* 23:16 MirahezeLSBot: [void@puppet181] Upgraded packages on phorge171: libssh2-1t64 and pdns-recursor
* 23:15 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask161: libssh2-1t64 and pdns-recursor
* 23:15 MirahezeLSBot: [void@puppet181] Upgraded packages on ns1: libssh2-1t64
* 23:15 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask171: libssh2-1t64 and pdns-recursor
* 23:15 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask151: libssh2-1t64 and pdns-recursor
* 23:14 MirahezeLSBot: [void@puppet181] Upgraded packages on mw202: libssh2-1t64 and pdns-recursor
* 23:13 MirahezeLSBot: [void@puppet181] Upgraded packages on mw203: libssh2-1t64 and pdns-recursor
* 23:12 MirahezeLSBot: [void@puppet181] Upgraded packages on mw201: libssh2-1t64 and pdns-recursor
* 23:11 MirahezeLSBot: [void@puppet181] Upgraded packages on mw183: libssh2-1t64 and pdns-recursor
* 23:10 MirahezeLSBot: [void@puppet181] Upgraded packages on mw182: libssh2-1t64 and pdns-recursor
* 23:08 MirahezeLSBot: [void@puppet181] Upgraded packages on mw181: libssh2-1t64 and pdns-recursor
* 23:08 MirahezeLSBot: [void@puppet181] Upgraded packages on mw193: libssh2-1t64 and pdns-recursor
* 23:07 MirahezeLSBot: [void@puppet181] Upgraded packages on mw173: libssh2-1t64 and pdns-recursor
* 23:06 MirahezeLSBot: [void@puppet181] Upgraded packages on mw192: libssh2-1t64 and pdns-recursor
* 23:05 MirahezeLSBot: [void@puppet181] Upgraded packages on mw191: libssh2-1t64 and pdns-recursor
* 23:04 MirahezeLSBot: [void@puppet181] Upgraded packages on mw172: libssh2-1t64 and pdns-recursor
* 23:02 MirahezeLSBot: [void@puppet181] Upgraded packages on mw151: libssh2-1t64 and pdns-recursor
* 23:01 MirahezeLSBot: [void@puppet181] Upgraded packages on mw171: libssh2-1t64 and pdns-recursor
* 23:00 MirahezeLSBot: [void@puppet181] Upgraded packages on mem191: libssh2-1t64 and pdns-recursor
* 23:00 MirahezeLSBot: [void@puppet181] Upgraded packages on mw163: libssh2-1t64 and pdns-recursor
* 22:59 MirahezeLSBot: [void@puppet181] Upgraded packages on mw162: libssh2-1t64 and pdns-recursor
* 22:58 MirahezeLSBot: [void@puppet181] Upgraded packages on mw153: libssh2-1t64 and pdns-recursor
* 22:57 MirahezeLSBot: [void@puppet181] Upgraded packages on mon181: libssh2-1t64 and pdns-recursor
* 22:57 MirahezeLSBot: [void@puppet181] Upgraded packages on mw161: libssh2-1t64 and pdns-recursor
* 22:56 MirahezeLSBot: [void@puppet181] Upgraded packages on mw152: libssh2-1t64 and pdns-recursor
* 22:54 MirahezeLSBot: [void@puppet181] Upgraded packages on mem201: libssh2-1t64 and pdns-recursor
* 22:54 MirahezeLSBot: [void@puppet181] Upgraded packages on llm191: libssh2-1t64 and pdns-recursor
* 22:54 MirahezeLSBot: [void@puppet181] Upgraded packages on mem161: libssh2-1t64 and pdns-recursor
* 22:54 MirahezeLSBot: [void@puppet181] Upgraded packages on mem151: libssh2-1t64 and pdns-recursor
* 22:53 MirahezeLSBot: [void@puppet181] Upgraded packages on kafka182: libssh2-1t64 and pdns-recursor
* 22:53 MirahezeLSBot: [void@puppet181] Upgraded packages on matomo151: libssh2-1t64 and pdns-recursor
* 22:53 MirahezeLSBot: [void@puppet181] Upgraded packages on ldap171: libssh2-1t64 and pdns-recursor
* 22:52 MirahezeLSBot: [void@puppet181] Upgraded packages on mattermost2: libssh2-1t64 and pdns-recursor
* 22:52 MirahezeLSBot: [void@puppet181] Upgraded packages on eventgate182: libssh2-1t64 and pdns-recursor
* 22:52 MirahezeLSBot: [void@puppet181] Upgraded packages on db181: libssh2-1t64 and pdns-recursor
* 22:51 MirahezeLSBot: [void@puppet181] Upgraded packages on db161: libssh2-1t64 and pdns-recursor
* 22:51 MirahezeLSBot: [void@puppet181] Upgraded packages on cp171: libssh2-1t64 and pdns-recursor
* 22:51 MirahezeLSBot: [void@puppet181] Upgraded packages on db201: libssh2-1t64 and pdns-recursor
* 22:50 MirahezeLSBot: [void@puppet181] Upgraded packages on graylog161: libssh2-1t64 and pdns-recursor
* 22:50 MirahezeLSBot: [void@puppet181] Upgraded packages on db182: libssh2-1t64 and pdns-recursor
* 22:50 MirahezeLSBot: [void@puppet181] Upgraded packages on db192: libssh2-1t64 and pdns-recursor
* 22:49 MirahezeLSBot: [void@puppet181] Upgraded packages on cp201: libssh2-1t64 and pdns-recursor
* 22:49 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud20: libssh2-1t64 and pdns-recursor
* 22:49 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud18: libssh2-1t64 and pdns-recursor
* 22:48 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud19: libssh2-1t64 and pdns-recursor
* 22:48 MirahezeLSBot: [void@puppet181] Upgraded packages on db171: libssh2-1t64 and pdns-recursor
* 22:48 MirahezeLSBot: [void@puppet181] Upgraded packages on cp161: libssh2-1t64 and pdns-recursor
* 22:48 MirahezeLSBot: [void@puppet181] Upgraded packages on cp191: libssh2-1t64 and pdns-recursor
* 22:47 MirahezeLSBot: [void@puppet181] Upgraded packages on changeprop202: libssh2-1t64 and pdns-recursor
* 22:47 MirahezeLSBot: [void@puppet181] Upgraded packages on db172: libssh2-1t64 and pdns-recursor
* 22:47 MirahezeLSBot: [void@puppet181] Upgraded packages on db151: libssh2-1t64 and pdns-recursor
* 22:46 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud17: libssh2-1t64 and pdns-recursor
* 22:46 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud16: libssh2-1t64 and pdns-recursor
* 22:46 MirahezeLSBot: [void@puppet181] Upgraded packages on bots171: libssh2-1t64 and pdns-recursor
* 22:46 MirahezeLSBot: [void@puppet181] Upgraded packages on bast181: libssh2-1t64 and pdns-recursor
* 22:45 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud21: libssh2-1t64 and pdns-recursor
* 22:45 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud15: libssh2-1t64 and pdns-recursor
* 22:45 MirahezeLSBot: [void@puppet181] Upgraded packages on bast161: libssh2-1t64 and pdns-recursor
* 07:13 MirahezeLSBot: [petramagna@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:AssignImportedEdits --wiki=xyywiki --import-prefix=fandom:xyy --from=OmrpGnWS --to=Schaduw108n (END - exit=0)
* 07:13 MirahezeLSBot: [petramagna@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:AssignImportedEdits --wiki=xyywiki --import-prefix=imported --from=OmrpGnWS --to=Schaduw108n (END - exit=0)
* 07:12 MirahezeLSBot: [petramagna@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:AssignImportedEdits --wiki=xyywiki --import-prefix=imported --from=IsAnmi4 --to=Pancakeanmi (END - exit=0)
* 07:11 MirahezeLSBot: [petramagna@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:AssignImportedEdits --wiki=xyywiki --import-prefix=imported --from='Zhou Kang' --to=Karsten (END - exit=0)
* 07:10 MirahezeLSBot: [petramagna@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:AssignImportedEdits --wiki=xyywiki --import-prefix=imported --from=Zhou_Kang --to=Karsten (END - exit=256)

## 2026-06-24 

* 19:05 MirahezeLSBot: [somerandomdeveloper@mwtask181] sudo -u www-data rm -rf /srv/mediawiki-staging/1.45/extensions/SimpleBlogPage/
* 19:04 MirahezeLSBot: [somerandomdeveloper@test151] finished deploy of {'world': True, 'versions': '1.46'} to test151 - SUCCESS in 22s
* 19:03 MirahezeLSBot: [somerandomdeveloper@test151] starting deploy of {'world': True, 'versions': '1.46'} to test151
* 19:03 MirahezeLSBot: [somerandomdeveloper@test151] finished deploy of {'folders': '1.46/extensions/SimpleBlogPage'} to test151 - SUCCESS in 0s
* 19:03 MirahezeLSBot: [somerandomdeveloper@test151] starting deploy of {'folders': '1.46/extensions/SimpleBlogPage'} to test151
* 19:00 MirahezeLSBot: [somerandomdeveloper@test151] sudo rm -rf /srv/mediawiki-staging/1.45/extensions/SimpleBlogPage/
* 19:00 MirahezeLSBot: [somerandomdeveloper@test151] sudo rm -rf /srv/mediawiki-staging/1.46/extensions/SimpleBlogPage/
* 18:49 MirahezeLSBot: [somerandomdeveloper@test151] finished deploy of {'versions': '1.46', 'upgrade_extensions': ['OOJSPlus', 'SimpleBlogPage']} to test151 - SUCCESS in 1s
* 18:49 MirahezeLSBot: [somerandomdeveloper@test151] starting deploy of {'versions': '1.46', 'upgrade_extensions': ['OOJSPlus', 'SimpleBlogPage']} to test151
* 18:46 MirahezeLSBot: [somerandomdeveloper@test151] DEPLOY ABORTED: Non-Zero Exit Code in prep, see output.
* 18:46 MirahezeLSBot: [somerandomdeveloper@test151] starting deploy of {'world': True, 'versions': '1.46'} to test151
* 18:45 MirahezeLSBot: [somerandomdeveloper@test151] finished deploy of {'folders': '1.46/extensions'} to test151 - SUCCESS in 8s
* 18:45 MirahezeLSBot: [somerandomdeveloper@test151] starting deploy of {'folders': '1.46/extensions'} to test151
* 18:44 MirahezeLSBot: [somerandomdeveloper@test151] DEPLOY ABORTED: Non-Zero Exit Code in prep, see output.
* 18:44 MirahezeLSBot: [somerandomdeveloper@test151] starting deploy of {'world': True, 'force': True, 'versions': '1.46'} to test151
* 18:43 MirahezeLSBot: [somerandomdeveloper@test151] DEPLOY ABORTED: Canary check failed for meta.mirabeta.org@localhost
* 18:43 MirahezeLSBot: [somerandomdeveloper@test151] starting deploy of {'world': True, 'versions': '1.46'} to test151
* 18:16 MirahezeLSBot: [reception@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RenameDatabase --wiki=loginwiki --rename --old=hyperscandevwiki --new=sunpluscoredevwiki --user=Reception123 (END - exit=0)
* 18:13 MirahezeLSBot: [reception@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RenameDatabase --wiki=loginwiki --rename --old=exterminationorderdawnofrobloxiawiki --new=robloxexterminationorderwiki --user=Reception123 (END - exit=0)
* 18:09 MirahezeLSBot: [reception@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RenameDatabase --wiki=loginwiki --rename --old=kratimawiki --new=psaltictheorywiki --user=Reception123 (END - exit=0)
* 18:07 MirahezeLSBot: [reception@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RenameDatabase --wiki=loginwiki --rename --old=pamiejaigewiki --new=jamiepediawiki --user=Reception123 (END - exit=0)
* 18:05 MirahezeLSBot: [reception@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RenameDatabase --wiki=loginwiki --rename --old=evropaeumswiki --new=evropawiki --user=Reception123 (END - exit=0)
* 18:00 MirahezeLSBot: [reception@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RenameDatabase --wiki=loginwiki --rename --old=averseofstorieswiki --new=thelittlegodswiki --user=Reception123 (END - exit=0)
* 17:58 MirahezeLSBot: [reception@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RenameDatabase --wiki=loginwiki --rename --old=q487294wiki --new=thebinarystellararchivewiki --user=Reception123 (END - exit=0)
* 17:56 MirahezeLSBot: [reception@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RenameDatabase --wiki=loginwiki --rename --old=enforgewiki --new=civworldwiki --user=Reception123 (END - exit=0)
* 13:19 MirahezeLSBot: [somerandomdeveloper@test151] finished deploy of {'pull': 'config', 'config': True} to test151 - SUCCESS in 1s
* 13:19 MirahezeLSBot: [somerandomdeveloper@test151] starting deploy of {'pull': 'config', 'config': True} to test151
* 13:18 MirahezeLSBot: [somerandomdeveloper@mwtask181] finished deploy of {'config': True} to all - SUCCESS in 28s
* 13:18 MirahezeLSBot: [somerandomdeveloper@mwtask181] starting deploy of {'config': True} to all
* 12:45 MirahezeLSBot: [petramagna@mwtask181] finished deploy of {'versions': '1.45', 'upgrade_extensions': 'HideSection'} to all - SUCCESS in 26s
* 12:44 MirahezeLSBot: [petramagna@mwtask181] starting deploy of {'versions': '1.45', 'upgrade_extensions': 'HideSection'} to all
* 12:43 MirahezeLSBot: [petramagna@test151] finished deploy of {'versions': ['1.45', '1.46'], 'upgrade_extensions': 'HideSection'} to test151 - SUCCESS in 1s
* 12:43 MirahezeLSBot: [petramagna@test151] starting deploy of {'versions': ['1.45', '1.46'], 'upgrade_extensions': 'HideSection'} to test151
* 09:08 MirahezeLSBot: [petramagna@test151] finished deploy of {'folders': '1.46/extensions/WikiDiscover', 'ignore_time': True} to test151 - SUCCESS in 0s
* 09:08 MirahezeLSBot: [petramagna@test151] starting deploy of {'folders': '1.46/extensions/WikiDiscover', 'ignore_time': True} to test151
* 09:06 MirahezeLSBot: [petramagna@test151] finished deploy of {'versions': ['1.45', '1.46'], 'upgrade_extensions': 'WikiDiscover', 'ignore_time': True} to test151 - SUCCESS in 1s
* 09:06 MirahezeLSBot: [petramagna@test151] starting deploy of {'versions': ['1.45', '1.46'], 'upgrade_extensions': 'WikiDiscover', 'ignore_time': True} to test151
* 08:52 MirahezeLSBot: [petramagna@test151] finished deploy of {'versions': ['1.45', '1.46'], 'upgrade_extensions': 'WikiDiscover'} to test151 - SUCCESS in 1s
* 08:52 MirahezeLSBot: [petramagna@test151] starting deploy of {'versions': ['1.45', '1.46'], 'upgrade_extensions': 'WikiDiscover'} to test151
* 05:03 Reception123: started wiki deletions
* 03:41 MirahezeLSBot: [skye@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 25s
* 03:41 MirahezeLSBot: [skye@test151] finished deploy of {'pull': 'config', 'config': True} to test151 - SUCCESS in 0s
* 03:41 MirahezeLSBot: [skye@test151] starting deploy of {'pull': 'config', 'config': True} to test151
* 03:41 MirahezeLSBot: [skye@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 00:58 TheWWRNerdGuy: this bit got cut off (and so did the quotes from the --r parameter): `|requested]]`
* 00:54 MirahezeLSBot: [wwr@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php deleteBatch --wiki=mariowiki batch.txt --r=[[phorge:T15564
* 00:51 MirahezeLSBot: [wwr@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php deleteBatch --wiki=mariowiki batch.txt --r=[[phorge:T15564
* 00:41 TheWWRNerdGuy: same thing for all namespaces in [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 828, 829]
* 00:39 MirahezeLSBot: [wwr@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php nukeNS --wiki=riskuniversaliswiki --delete --all --ns=4 (END - exit=0)
* 00:39 MirahezeLSBot: [wwr@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php nukeNS --wiki=riskuniversaliswiki --delete --all --ns=4 (START)
* 00:37 MirahezeLSBot: [wwr@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php nukeNS --wiki=riskuniversaliswiki --delete --all --ns=3 (END - exit=0)
* 00:37 MirahezeLSBot: [wwr@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php nukeNS --wiki=riskuniversaliswiki --delete --all --ns=3 (START)
* 00:37 MirahezeLSBot: [wwr@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php nukeNS --wiki=riskuniversaliswiki --delete --all --ns=2 (END - exit=0)
* 00:36 MirahezeLSBot: [wwr@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php nukeNS --wiki=riskuniversaliswiki --delete --all --ns=2 (START)
* 00:36 MirahezeLSBot: [wwr@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php nukeNS --wiki=riskuniversaliswiki --delete --all --ns=1 (END - exit=0)
* 00:36 MirahezeLSBot: [wwr@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php nukeNS --wiki=riskuniversaliswiki --delete --all --ns=1 (START)
* 00:36 MirahezeLSBot: [wwr@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php nukeNS --wiki=riskuniversaliswiki --delete --all --ns=0 (END - exit=0)
* 00:36 MirahezeLSBot: [wwr@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php nukeNS --wiki=riskuniversaliswiki --delete --all --ns=0 (START)

## 2026-06-23 

* 23:14 MirahezeLSBot: [skye@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 26s
* 23:13 MirahezeLSBot: [skye@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 23:13 MirahezeLSBot: [skye@test151] finished deploy of {'pull': 'config', 'config': True} to test151 - SUCCESS in 0s
* 23:13 MirahezeLSBot: [skye@test151] starting deploy of {'pull': 'config', 'config': True} to test151
* 23:13 MirahezeLSBot: [skye@test151] DEPLOY ABORTED: Non-Zero Exit Code in prep, see output.
* 23:13 MirahezeLSBot: [skye@test151] starting deploy of {'pull': 'config', 'config': True} to test151
* 23:12 MirahezeLSBot: [skye@test151] DEPLOY ABORTED: Non-Zero Exit Code in prep, see output.
* 23:12 MirahezeLSBot: [skye@test151] starting deploy of {'pull': 'config', 'config': True} to test151
* 23:05 MirahezeLSBot: [skye@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 23:05 MirahezeLSBot: [skye@test151] starting deploy of {'config': True} to test151
* 20:19 MirahezeLSBot: [void@puppet181] Upgraded packages on os202: python3-urllib3
* 20:19 MirahezeLSBot: [void@puppet181] Upgraded packages on rdb191: python3-urllib3
* 20:18 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftproxy161: python3-urllib3
* 20:18 MirahezeLSBot: [wwr@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php CreateWiki:SetContainersAccess --wiki=rivenvisionwiki (END - exit=0)
* 20:18 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject201: python3-urllib3
* 20:18 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftproxy171: python3-urllib3
* 20:18 MirahezeLSBot: [wwr@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RenameDatabase --wiki=loginwiki --rename --old=funoonvisionwiki --new=rivenvisionwiki --user=TheWWRNerdGuy (END - exit=0)
* 20:17 MirahezeLSBot: [void@puppet181] Upgraded packages on test151: python3-urllib3
* 20:17 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject191: python3-urllib3
* 20:17 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject181: python3-urllib3
* 20:17 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject171: python3-urllib3
* 20:16 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject211: python3-urllib3
* 20:16 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject161: python3-urllib3
* 20:16 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftac171: python3-urllib3
* 20:15 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject151: python3-urllib3
* 20:15 MirahezeLSBot: [void@puppet181] Upgraded packages on ns2: python3-urllib3
* 20:15 MirahezeLSBot: [void@puppet181] Upgraded packages on reports171: python3-urllib3
* 20:15 MirahezeLSBot: [void@puppet181] Upgraded packages on os201: python3-urllib3
* 20:14 MirahezeLSBot: [void@puppet181] Upgraded packages on puppet181: python3-urllib3
* 20:14 MirahezeLSBot: [void@puppet181] Upgraded packages on phorge171: python3-urllib3
* 20:14 MirahezeLSBot: [void@puppet181] Upgraded packages on os162: python3-urllib3
* 20:14 MirahezeLSBot: [void@puppet181] Upgraded packages on os191: python3-urllib3
* 20:13 MirahezeLSBot: [void@puppet181] Upgraded packages on mw202: python3-urllib3
* 20:13 MirahezeLSBot: [void@puppet181] Upgraded packages on os161: python3-urllib3
* 20:13 MirahezeLSBot: [void@puppet181] Upgraded packages on prometheus151: python3-urllib3
* 20:12 MirahezeLSBot: [void@puppet181] Upgraded packages on ns1: python3-urllib3
* 20:12 MirahezeLSBot: [void@puppet181] Upgraded packages on os151: python3-urllib3
* 20:12 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask171: python3-urllib3
* 20:12 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask181: python3-urllib3
* 20:11 MirahezeLSBot: [void@puppet181] Upgraded packages on mw203: python3-urllib3
* 20:11 MirahezeLSBot: [void@puppet181] Upgraded packages on mw201: python3-urllib3
* 20:11 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask151: python3-urllib3
* 20:10 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask161: python3-urllib3
* 20:10 MirahezeLSBot: [void@puppet181] Upgraded packages on mw192: python3-urllib3
* 20:10 MirahezeLSBot: [void@puppet181] Upgraded packages on mw193: python3-urllib3
* 20:09 MirahezeLSBot: [void@puppet181] Upgraded packages on kafka182: python3-urllib3
* 20:09 MirahezeLSBot: [void@puppet181] Upgraded packages on mw191: python3-urllib3
* 20:09 MirahezeLSBot: [void@puppet181] Upgraded packages on mw183: python3-urllib3
* 20:09 MirahezeLSBot: [void@puppet181] Upgraded packages on mw181: python3-urllib3
* 20:08 MirahezeLSBot: [void@puppet181] Upgraded packages on mw182: python3-urllib3
* 20:08 MirahezeLSBot: [void@puppet181] Upgraded packages on mw163: python3-urllib3
* 20:08 MirahezeLSBot: [void@puppet181] Upgraded packages on mw173: python3-urllib3
* 20:07 MirahezeLSBot: [void@puppet181] Upgraded packages on mw172: python3-urllib3
* 20:07 MirahezeLSBot: [void@puppet181] Upgraded packages on mw153: python3-urllib3
* 20:07 MirahezeLSBot: [void@puppet181] Upgraded packages on mw161: python3-urllib3
* 20:06 MirahezeLSBot: [void@puppet181] Upgraded packages on mw171: python3-urllib3
* 20:06 MirahezeLSBot: [void@puppet181] Upgraded packages on mw152: python3-urllib3
* 20:06 MirahezeLSBot: [void@puppet181] Upgraded packages on mem191: python3-urllib3
* 20:06 MirahezeLSBot: [wwr@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php CreateWiki:SetContainersAccess --wiki=vibrancewiki (END - exit=0)
* 20:05 MirahezeLSBot: [void@puppet181] Upgraded packages on mw162: python3-urllib3
* 20:05 MirahezeLSBot: [void@puppet181] Upgraded packages on mon181: python3-urllib3
* 20:05 MirahezeLSBot: [void@puppet181] Upgraded packages on db192: python3-urllib3
* 20:05 MirahezeLSBot: [wwr@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RenameDatabase --wiki=loginwiki --rename --old=thevibrantlandswiki --new=vibrancewiki --user=TheWWRNerdGuy (END - exit=0)
* 20:05 MirahezeLSBot: [void@puppet181] Upgraded packages on db201: python3-urllib3
* 20:04 MirahezeLSBot: [void@puppet181] Upgraded packages on mw151: python3-urllib3
* 20:04 MirahezeLSBot: [void@puppet181] Upgraded packages on llm191: python3-urllib3
* 20:04 MirahezeLSBot: [void@puppet181] Upgraded packages on mem201: python3-urllib3
* 20:03 MirahezeLSBot: [void@puppet181] Upgraded packages on mem161: python3-urllib3
* 20:03 MirahezeLSBot: [void@puppet181] Upgraded packages on mem151: python3-urllib3
* 20:03 MirahezeLSBot: [void@puppet181] Upgraded packages on matomo151: python3-urllib3
* 20:03 MirahezeLSBot: [void@puppet181] Upgraded packages on changeprop202: python3-urllib3
* 20:02 MirahezeLSBot: [void@puppet181] Upgraded packages on ldap171: python3-urllib3
* 20:02 MirahezeLSBot: [void@puppet181] Upgraded packages on mattermost2: python3-urllib3
* 20:02 MirahezeLSBot: [void@puppet181] Upgraded packages on graylog161: python3-urllib3
* 20:02 MirahezeLSBot: [void@puppet181] Upgraded packages on cp171: python3-urllib3
* 20:01 MirahezeLSBot: [void@puppet181] Upgraded packages on cp201: python3-urllib3
* 20:01 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud20: python3-urllib3
* 20:01 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud19: python3-urllib3
* 20:00 MirahezeLSBot: [void@puppet181] Upgraded packages on db181: python3-urllib3
* 20:00 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud16: python3-urllib3
* 20:00 MirahezeLSBot: [void@puppet181] Upgraded packages on cp191: python3-urllib3
* 20:00 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud15: python3-urllib3
* 19:59 MirahezeLSBot: [void@puppet181] Upgraded packages on db182: python3-urllib3
* 19:59 MirahezeLSBot: [wwr@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php CreateWiki:SetContainersAccess --wiki=trenchfallwiki (END - exit=0)
* 19:59 MirahezeLSBot: [void@puppet181] Upgraded packages on bast181: python3-urllib3
* 19:59 MirahezeLSBot: [void@puppet181] Upgraded packages on db161: python3-urllib3
* 19:59 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud18: python3-urllib3
* 19:58 MirahezeLSBot: [wwr@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RenameDatabase --wiki=loginwiki --rename --old=trenchfallofficialwiki --new=trenchfallwiki --user=TheWWRNerdGuy (END - exit=0)
* 19:58 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud17: python3-urllib3
* 19:58 MirahezeLSBot: [void@puppet181] Upgraded packages on eventgate182: python3-urllib3
* 19:58 MirahezeLSBot: [void@puppet181] Upgraded packages on db171: python3-urllib3
* 19:57 MirahezeLSBot: [void@puppet181] Upgraded packages on db151: python3-urllib3
* 19:57 MirahezeLSBot: [void@puppet181] Upgraded packages on bots171: python3-urllib3
* 19:57 MirahezeLSBot: [void@puppet181] Upgraded packages on db172: python3-urllib3
* 19:57 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud21: python3-urllib3
* 19:57 MirahezeLSBot: [void@puppet181] Upgraded packages on cp161: python3-urllib3
* 19:56 MirahezeLSBot: [void@puppet181] Upgraded packages on bast161: python3-urllib3
* 19:44 MirahezeLSBot: [wwr@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php CreateWiki:SetContainersAccess --wiki=dagapyawiki (END - exit=0)
* 19:43 MirahezeLSBot: [wwr@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RenameDatabase --wiki=loginwiki --rename --old=dasopyawiki --new=dagapyawiki --user=TheWWRNerdGuy (END - exit=0)
* 19:26 MirahezeLSBot: [wwr@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php CreateWiki:SetContainersAccess --wiki=newworldswiki (END - exit=0)
* 19:25 MirahezeLSBot: [wwr@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RenameDatabase --wiki=loginwiki --rename --old=newnovawiki --new=newworldswiki --user=TheWWRNerdGuy (END - exit=0)
* 19:19 MirahezeLSBot: [wwr@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php CreateWiki:SetContainersAccess --wiki=jetpunkwiki (END - exit=0)
* 19:18 MirahezeLSBot: [wwr@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RenameDatabase --wiki=loginwiki --rename --old=jetpunkquizwiki --new=jetpunkwiki --user=TheWWRNerdGuy (END - exit=0)
* 19:10 MirahezeLSBot: [wwr@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php CreateWiki:SetContainersAccess --wiki=illwiki (END - exit=0)
* 19:07 MirahezeLSBot: [wwr@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RenameDatabase --wiki=loginwiki --rename --old=ihsawiki --new=illwiki --user=TheWWRNerdGuy (END - exit=0)
* 02:05 MirahezeLSBot: [petramagna@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 02:05 MirahezeLSBot: [petramagna@test151] starting deploy of {'config': True} to test151
* 00:21 MirahezeLSBot: [void@puppet181] Upgraded packages on test151: libswscale8, libavfilter10, libavdevice61, libavformat61, libavcodec61, libavutil59, libpostproc58, libswresample5, and ffmpeg
* 00:02 MirahezeLSBot: [void@puppet181] Upgraded packages on mw203: libswscale8, libavfilter10, libavdevice61, libavformat61, libavcodec61, libavutil59, libpostproc58, libswresample5, and ffmpeg
* 00:02 MirahezeLSBot: [void@puppet181] Upgraded packages on mw193: libswscale8, libavfilter10, libavdevice61, libavformat61, libavcodec61, libavutil59, libpostproc58, libswresample5, and ffmpeg
* 00:01 MirahezeLSBot: [void@puppet181] Upgraded packages on mw183: libswscale8, libavfilter10, libavdevice61, libavformat61, libavcodec61, libavutil59, libpostproc58, libswresample5, and ffmpeg
* 00:01 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask181: libswscale8, libavfilter10, libavdevice61, libavformat61, libavcodec61, libavutil59, libpostproc58, libswresample5, and ffmpeg
* 00:00 MirahezeLSBot: [void@puppet181] Upgraded packages on mw182: libswscale8, libavfilter10, libavdevice61, libavformat61, libavcodec61, libavutil59, libpostproc58, libswresample5, and ffmpeg
* 00:00 MirahezeLSBot: [void@puppet181] Upgraded packages on mw202: libswscale8, libavfilter10, libavdevice61, libavformat61, libavcodec61, libavutil59, libpostproc58, libswresample5, and ffmpeg
* 00:00 MirahezeLSBot: [void@puppet181] Upgraded packages on mw181: libswscale8, libavfilter10, libavdevice61, libavformat61, libavcodec61, libavutil59, libpostproc58, libswresample5, and ffmpeg

## 2026-06-22 

* 23:59 MirahezeLSBot: [void@puppet181] Upgraded packages on mw191: libswscale8, libavfilter10, libavdevice61, libavformat61, libavcodec61, libavutil59, libpostproc58, libswresample5, and ffmpeg
* 23:59 MirahezeLSBot: [void@puppet181] Upgraded packages on mw192: libswscale8, libavfilter10, libavdevice61, libavformat61, libavcodec61, libavutil59, libpostproc58, libswresample5, and ffmpeg
* 23:59 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask161: libswscale8, libavfilter10, libavdevice61, libavformat61, libavcodec61, libavutil59, libpostproc58, libswresample5, and ffmpeg
* 23:58 MirahezeLSBot: [void@puppet181] Upgraded packages on mw171: libswscale8, libavfilter10, libavdevice61, libavformat61, libavcodec61, libavutil59, libpostproc58, libswresample5, and ffmpeg
* 23:58 MirahezeLSBot: [void@puppet181] Upgraded packages on mw201: libswscale8, libavfilter10, libavdevice61, libavformat61, libavcodec61, libavutil59, libpostproc58, libswresample5, and ffmpeg
* 23:58 MirahezeLSBot: [void@puppet181] Upgraded packages on mw173: libswscale8, libavfilter10, libavdevice61, libavformat61, libavcodec61, libavutil59, libpostproc58, libswresample5, and ffmpeg
* 23:57 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask151: libswscale8, libavfilter10, libavdevice61, libavformat61, libavcodec61, libavutil59, libpostproc58, libswresample5, and ffmpeg
* 23:57 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask171: libswscale8, libavfilter10, libavdevice61, libavformat61, libavcodec61, libavutil59, libpostproc58, libswresample5, and ffmpeg
* 23:57 MirahezeLSBot: [void@puppet181] Upgraded packages on mw163: libswscale8, libavfilter10, libavdevice61, libavformat61, libavcodec61, libavutil59, libpostproc58, libswresample5, and ffmpeg
* 23:56 MirahezeLSBot: [void@puppet181] Upgraded packages on mw161: libswscale8, libavfilter10, libavdevice61, libavformat61, libavcodec61, libavutil59, libpostproc58, libswresample5, and ffmpeg
* 23:56 MirahezeLSBot: [void@puppet181] Upgraded packages on mw172: libswscale8, libavfilter10, libavdevice61, libavformat61, libavcodec61, libavutil59, libpostproc58, libswresample5, and ffmpeg
* 23:55 MirahezeLSBot: [void@puppet181] Upgraded packages on mw152: libswscale8, libavfilter10, libavdevice61, libavformat61, libavcodec61, libavutil59, libpostproc58, libswresample5, and ffmpeg
* 23:55 MirahezeLSBot: [void@puppet181] Upgraded packages on mw153: libswscale8, libavfilter10, libavdevice61, libavformat61, libavcodec61, libavutil59, libpostproc58, libswresample5, and ffmpeg
* 23:55 MirahezeLSBot: [void@puppet181] Upgraded packages on mw162: libswscale8, libavfilter10, libavdevice61, libavformat61, libavcodec61, libavutil59, libpostproc58, libswresample5, and ffmpeg
* 23:54 MirahezeLSBot: [void@puppet181] Upgraded packages on mw151: libswscale8, libavfilter10, libavdevice61, libavformat61, libavcodec61, libavutil59, libpostproc58, libswresample5, and ffmpeg
* 19:36 MirahezeLSBot: [wwr@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php createAndPromote --wiki=minecraftminigameswiki MC_mrjone --bureaucrat --sysop --interface-admin --force (END - exit=0)
* 11:43 Reception123: run delbackups (bash ./delbackups.sh /home/reception/tobedeleted22062026.txt /srv/mediawiki/w/maintenance/dumpBackup.php)
* 11:38 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php CreateWiki:DeleteWikis --wiki=loginwiki DRY_RUN (END - exit=0)
* 00:33 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject151: linux-libc-dev and python3-pil
* 00:15 MirahezeLSBot: [void@puppet181] Upgraded packages on ns2: linux-libc-dev
* 00:14 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject201: linux-libc-dev and python3-pil
* 00:14 MirahezeLSBot: [void@puppet181] Upgraded packages on test151: linux-libc-dev, libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, libhttp-daemon-perl, libmagickcore-7.q16-10-extra, and python3-pil
* 00:14 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject191: linux-libc-dev and python3-pil
* 00:13 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftproxy171: linux-libc-dev and python3-pil
* 00:13 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftproxy161: linux-libc-dev and python3-pil
* 00:13 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject211: linux-libc-dev and python3-pil
* 00:12 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject181: linux-libc-dev and python3-pil
* 00:12 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject171: linux-libc-dev and python3-pil
* 00:12 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject161: linux-libc-dev and python3-pil
* 00:12 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftac171: linux-libc-dev and python3-pil
* 00:11 MirahezeLSBot: [void@puppet181] Upgraded packages on os191: linux-libc-dev
* 00:11 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject151: linux-libc-dev and python3-pil
* 00:11 MirahezeLSBot: [void@puppet181] Upgraded packages on os161: linux-libc-dev
* 00:10 MirahezeLSBot: [void@puppet181] Upgraded packages on os201: linux-libc-dev
* 00:10 MirahezeLSBot: [void@puppet181] Upgraded packages on os202: linux-libc-dev
* 00:10 MirahezeLSBot: [void@puppet181] Upgraded packages on rdb191: linux-libc-dev
* 00:09 MirahezeLSBot: [void@puppet181] Upgraded packages on os162: linux-libc-dev
* 00:09 MirahezeLSBot: [void@puppet181] Upgraded packages on prometheus151: linux-libc-dev
* 00:09 MirahezeLSBot: [void@puppet181] Upgraded packages on puppet181: linux-libc-dev
* 00:09 MirahezeLSBot: [void@puppet181] Upgraded packages on reports171: linux-libc-dev
* 00:08 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask181: linux-libc-dev, libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, libhttp-daemon-perl, libmagickcore-7.q16-10-extra, and python3-pil
* 00:08 MirahezeLSBot: [void@puppet181] Upgraded packages on ns1: linux-libc-dev
* 00:08 MirahezeLSBot: [void@puppet181] Upgraded packages on phorge171: linux-libc-dev
* 00:07 MirahezeLSBot: [void@puppet181] Upgraded packages on os151: linux-libc-dev
* 00:07 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask171: linux-libc-dev, libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, libhttp-daemon-perl, libmagickcore-7.q16-10-extra, and python3-pil
* 00:07 MirahezeLSBot: [void@puppet181] Upgraded packages on mw203: linux-libc-dev, libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, libhttp-daemon-perl, libmagickcore-7.q16-10-extra, and python3-pil
* 00:06 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask161: linux-libc-dev, libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, libhttp-daemon-perl, libmagickcore-7.q16-10-extra, and python3-pil
* 00:06 MirahezeLSBot: [void@puppet181] Upgraded packages on mw202: linux-libc-dev, libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, libhttp-daemon-perl, libmagickcore-7.q16-10-extra, and python3-pil
* 00:06 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask151: linux-libc-dev, libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, libhttp-daemon-perl, libmagickcore-7.q16-10-extra, and python3-pil
* 00:05 MirahezeLSBot: [void@puppet181] Upgraded packages on mw201: linux-libc-dev, libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, libhttp-daemon-perl, libmagickcore-7.q16-10-extra, and python3-pil
* 00:05 MirahezeLSBot: [void@puppet181] Upgraded packages on mw192: linux-libc-dev, libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, libhttp-daemon-perl, libmagickcore-7.q16-10-extra, and python3-pil
* 00:04 MirahezeLSBot: [void@puppet181] Upgraded packages on mw193: linux-libc-dev, libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, libhttp-daemon-perl, libmagickcore-7.q16-10-extra, and python3-pil
* 00:04 MirahezeLSBot: [void@puppet181] Upgraded packages on mw183: linux-libc-dev, libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, libhttp-daemon-perl, libmagickcore-7.q16-10-extra, and python3-pil
* 00:03 MirahezeLSBot: [void@puppet181] Upgraded packages on mw182: linux-libc-dev, libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, libhttp-daemon-perl, libmagickcore-7.q16-10-extra, and python3-pil
* 00:03 MirahezeLSBot: [void@puppet181] Upgraded packages on ldap171: linux-libc-dev
* 00:03 MirahezeLSBot: [void@puppet181] Upgraded packages on mw191: linux-libc-dev, libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, libhttp-daemon-perl, libmagickcore-7.q16-10-extra, and python3-pil
* 00:02 MirahezeLSBot: [void@puppet181] Upgraded packages on mw181: linux-libc-dev, libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, libhttp-daemon-perl, libmagickcore-7.q16-10-extra, and python3-pil
* 00:02 MirahezeLSBot: [void@puppet181] Upgraded packages on mem191: linux-libc-dev
* 00:01 MirahezeLSBot: [void@puppet181] Upgraded packages on mw153: linux-libc-dev, libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, libhttp-daemon-perl, libmagickcore-7.q16-10-extra, and python3-pil
* 00:01 MirahezeLSBot: [void@puppet181] Upgraded packages on mw171: linux-libc-dev, libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, libhttp-daemon-perl, libmagickcore-7.q16-10-extra, and python3-pil
* 00:01 MirahezeLSBot: [void@puppet181] Upgraded packages on mw173: linux-libc-dev, libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, libhttp-daemon-perl, libmagickcore-7.q16-10-extra, and python3-pil
* 00:00 MirahezeLSBot: [void@puppet181] Upgraded packages on mw163: linux-libc-dev, libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, libhttp-daemon-perl, libmagickcore-7.q16-10-extra, and python3-pil
* 00:00 MirahezeLSBot: [void@puppet181] Upgraded packages on mw172: linux-libc-dev, libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, libhttp-daemon-perl, libmagickcore-7.q16-10-extra, and python3-pil

## 2026-06-21 

* 23:59 MirahezeLSBot: [void@puppet181] Upgraded packages on mw152: linux-libc-dev, libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, libhttp-daemon-perl, libmagickcore-7.q16-10-extra, and python3-pil
* 23:59 MirahezeLSBot: [void@puppet181] Upgraded packages on mon181: linux-libc-dev
* 23:59 MirahezeLSBot: [void@puppet181] Upgraded packages on mw161: linux-libc-dev, libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, libhttp-daemon-perl, libmagickcore-7.q16-10-extra, and python3-pil
* 23:58 MirahezeLSBot: [void@puppet181] Upgraded packages on mw162: linux-libc-dev, libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, libhttp-daemon-perl, libmagickcore-7.q16-10-extra, and python3-pil
* 23:58 MirahezeLSBot: [void@puppet181] Upgraded packages on mw151: linux-libc-dev, libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, libhttp-daemon-perl, libmagickcore-7.q16-10-extra, and python3-pil
* 23:58 MirahezeLSBot: [void@puppet181] Upgraded packages on mem201: linux-libc-dev
* 23:57 MirahezeLSBot: [void@puppet181] Upgraded packages on llm191: linux-libc-dev
* 23:57 MirahezeLSBot: [void@puppet181] Upgraded packages on mem161: linux-libc-dev
* 23:57 MirahezeLSBot: [void@puppet181] Upgraded packages on matomo151: linux-libc-dev
* 23:57 MirahezeLSBot: [void@puppet181] Upgraded packages on mem151: linux-libc-dev
* 23:56 MirahezeLSBot: [void@puppet181] Upgraded packages on kafka182: linux-libc-dev
* 23:56 MirahezeLSBot: [void@puppet181] Upgraded packages on mattermost2: linux-libc-dev
* 23:56 MirahezeLSBot: [void@puppet181] Upgraded packages on graylog161: linux-libc-dev
* 23:56 MirahezeLSBot: [void@puppet181] Upgraded packages on db201: linux-libc-dev
* 23:55 MirahezeLSBot: [void@puppet181] Upgraded packages on db192: linux-libc-dev
* 23:55 MirahezeLSBot: [void@puppet181] Upgraded packages on db181: linux-libc-dev
* 23:55 MirahezeLSBot: [void@puppet181] Upgraded packages on cp201: linux-libc-dev
* 23:54 MirahezeLSBot: [void@puppet181] Upgraded packages on db182: linux-libc-dev
* 23:54 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud20: linux-libc-dev, libcpupower1, libhttp-daemon-perl, and linux-cpupower
* 23:54 MirahezeLSBot: [void@puppet181] Upgraded packages on eventgate182: linux-libc-dev and libhttp-daemon-perl
* 23:53 MirahezeLSBot: [void@puppet181] Upgraded packages on cp191: linux-libc-dev
* 23:53 MirahezeLSBot: [void@puppet181] Upgraded packages on changeprop202: linux-libc-dev and libhttp-daemon-perl
* 23:53 MirahezeLSBot: [void@puppet181] Upgraded packages on bast181: linux-libc-dev, squid-common, and squid
* 23:52 MirahezeLSBot: [void@puppet181] Upgraded packages on db151: linux-libc-dev
* 23:52 MirahezeLSBot: [void@puppet181] Upgraded packages on db171: linux-libc-dev
* 23:51 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud18: linux-libc-dev, libcpupower1, libhttp-daemon-perl, and linux-cpupower
* 23:51 MirahezeLSBot: [void@puppet181] Upgraded packages on cp161: linux-libc-dev
* 23:51 MirahezeLSBot: [void@puppet181] Upgraded packages on cp171: linux-libc-dev
* 23:51 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud16: linux-libc-dev, libcpupower1, libhttp-daemon-perl, and linux-cpupower
* 23:50 MirahezeLSBot: [void@puppet181] Upgraded packages on db161: linux-libc-dev
* 23:50 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud19: linux-libc-dev, libcpupower1, libhttp-daemon-perl, and linux-cpupower
* 23:50 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud17: linux-libc-dev, libcpupower1, libhttp-daemon-perl, and linux-cpupower
* 23:49 MirahezeLSBot: [void@puppet181] Upgraded packages on bots171: linux-libc-dev and python3-pil
* 23:49 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud15: linux-libc-dev, libcpupower1, libhttp-daemon-perl, and linux-cpupower
* 23:49 MirahezeLSBot: [void@puppet181] Upgraded packages on db172: linux-libc-dev
* 23:49 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud21: linux-libc-dev, libcpupower1, libhttp-daemon-perl, and linux-cpupower
* 23:48 MirahezeLSBot: [void@puppet181] Upgraded packages on bast161: linux-libc-dev, squid-common, and squid
* 12:25 MirahezeLSBot: [wwr@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php createAndPromote --wiki=minecraftminigameswiki MC_mrjone --bureaucrat --sysop --interface-admin --force (END - exit=256)
* 12:13 MirahezeLSBot: [wwr@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php CreateWiki:SetContainersAccess --wiki=minecraftminigameswiki (END - exit=0)
* 12:08 MirahezeLSBot: [wwr@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:ResetWiki --wiki=loginwiki --dbname=minecraftminigameswiki --requester=MC mrjone (END - exit=0)
* 10:58 TheWWRNerdGuy: MediaWiki\Extension\CentralAuth\User\CentralAuthUser::getInstance( User::newFromName( 'FrivolousCreature' ) )->attach( 'dustbunnywiki', 'admin' );

## 2026-06-20 

* 16:07 @paladox: restart mysql on db182 to pick up config change

## 2026-06-19 

* 21:18 MirahezeLSBot: [skye@test151] finished deploy of {'pull': 'config', 'config': True} to test151 - SUCCESS in 0s
* 21:18 MirahezeLSBot: [skye@test151] starting deploy of {'pull': 'config', 'config': True} to test151
* 21:18 MirahezeLSBot: [skye@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 24s
* 21:18 MirahezeLSBot: [skye@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 20:12 MirahezeLSBot: [void@puppet181] Upgraded packages on mon181: libconfig-inifiles-perl
* 20:11 MirahezeLSBot: [void@puppet181] Upgraded packages on db181: libconfig-inifiles-perl
* 20:11 MirahezeLSBot: [void@puppet181] Upgraded packages on db192: libconfig-inifiles-perl
* 20:11 MirahezeLSBot: [void@puppet181] Upgraded packages on db201: libconfig-inifiles-perl
* 20:10 MirahezeLSBot: [void@puppet181] Upgraded packages on db182: libconfig-inifiles-perl
* 20:10 MirahezeLSBot: [void@puppet181] Upgraded packages on reports171: libconfig-inifiles-perl
* 20:10 MirahezeLSBot: [void@puppet181] Upgraded packages on db171: libconfig-inifiles-perl
* 20:10 MirahezeLSBot: [void@puppet181] Upgraded packages on db151: libconfig-inifiles-perl
* 20:10 MirahezeLSBot: [void@puppet181] Upgraded packages on phorge171: libconfig-inifiles-perl
* 20:09 MirahezeLSBot: [void@puppet181] Upgraded packages on db172: libconfig-inifiles-perl
* 20:09 MirahezeLSBot: [void@puppet181] Upgraded packages on db161: libconfig-inifiles-perl
* 18:49 SomeRandomDeveloper: dropped security patches for T15475
* 18:49 MirahezeLSBot: [somerandomdeveloper@mwtask181] finished deploy of {'versions': '1.45', 'upgrade_extensions': 'EmbedVideo'} to all - SUCCESS in 27s
* 18:49 MirahezeLSBot: [somerandomdeveloper@mwtask181] starting deploy of {'versions': '1.45', 'upgrade_extensions': 'EmbedVideo'} to all
* 18:48 MirahezeLSBot: [somerandomdeveloper@test151] finished deploy of {'versions': ['1.45', '1.46'], 'upgrade_extensions': 'EmbedVideo'} to test151 - SUCCESS in 1s
* 18:48 MirahezeLSBot: [somerandomdeveloper@test151] starting deploy of {'versions': ['1.45', '1.46'], 'upgrade_extensions': 'EmbedVideo'} to test151

## 2026-06-18 

* 05:13 MirahezeLSBot: [void@db161] restart sql-backup service

## 2026-06-17 

* 01:23 MirahezeLSBot: [void@puppet181] Upgraded packages on puppet181: gsasl-common and libgsasl18
* 00:25 SomeRandomDeveloper: sudo salt-ssh -E 'mw.*' cmd.run 'rm /srv/mediawiki/cache/polandcuberuwiki.php'
* 00:25 SomeRandomDeveloper: sudo salt-ssh -E 'mw.*' cmd.run 'rm /srv/mediawiki/cache/config-polandcuberuwiki.php'

## 2026-06-16 

* 23:26 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php initSiteStats --wiki=fantendowiki --update (END - exit=0)
* 19:57 @paladox: deploy [https://github.com/miraheze/puppet/pull/4864](https://github.com/miraheze/puppet/pull/4864)
* 14:09 MirahezeLSBot: [skye@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 27s
* 14:09 MirahezeLSBot: [skye@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 14:09 MirahezeLSBot: [skye@test151] finished deploy of {'pull': 'config', 'config': True} to test151 - SUCCESS in 1s
* 14:08 MirahezeLSBot: [skye@test151] starting deploy of {'pull': 'config', 'config': True} to test151

## 2026-06-15 

* 22:14 SomeRandomDeveloper: dropped tcgswiki, teiinfwiki, vvedommelstatewiki, murdermittensrobloxwiki, francoriawiki, eurosfootballwiki, evilspacewiki, andrahistoriaswiki, ahleleleahlelaswikiwiki, margoswiki, nothingknownwiki, aliencodexwiki, starterdexwiki on db161/db171 (some existed on both)
* 21:59 SomeRandomDeveloper: "DROP DATABASE hadeanheavenwiki;" on db161
* 21:21 @paladox: [root@matomo151:/srv/matomo]# ./console  core:update
* 12:05 MirahezeLSBot: [petramagna@mwtask181] finished deploy of {'versions': '1.45', 'upgrade_extensions': 'UrlShortener'} to all - SUCCESS in 25s
* 12:04 MirahezeLSBot: [petramagna@mwtask181] starting deploy of {'versions': '1.45', 'upgrade_extensions': 'UrlShortener'} to all
* 12:03 MirahezeLSBot: [petramagna@test151] finished deploy of {'versions': ['1.45', '1.46'], 'upgrade_extensions': 'UrlShortener'} to test151 - SUCCESS in 1s
* 12:02 MirahezeLSBot: [petramagna@test151] starting deploy of {'versions': ['1.45', '1.46'], 'upgrade_extensions': 'UrlShortener'} to test151
* 11:52 MirahezeLSBot: [petramagna@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 24s
* 11:52 MirahezeLSBot: [petramagna@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 10:11 MirahezeLSBot: [petramagna@mwtask181] finished deploy of {'config': True, 'force': True} to all - SUCCESS in 18s
* 10:11 MirahezeLSBot: [petramagna@mwtask181] starting deploy of {'config': True, 'force': True} to all
* 10:11 MirahezeLSBot: [petramagna@mwtask181] DEPLOY ABORTED: Canary check failed for publictestwiki.com@localhost
* 10:11 MirahezeLSBot: [petramagna@mwtask181] starting deploy of {'config': True} to all
* 10:04 RhinosF1: sudo qm reset 128 on cloud 16 (reset db161)
* 09:51 MirahezeLSBot: [petramagna@mwtask181] finished deploy of {'config': True, 'force': True} to all - SUCCESS in 19s
* 08:41 MirahezeLSBot: [petramagna@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 08:41 MirahezeLSBot: [petramagna@test151] starting deploy of {'config': True} to test151
* 07:19 MirahezeLSBot: [petramagna@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 25s
* 07:18 MirahezeLSBot: [petramagna@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 07:17 MirahezeLSBot: [petramagna@test151] finished deploy of {'pull': 'config', 'config': True} to test151 - SUCCESS in 1s
* 07:17 MirahezeLSBot: [petramagna@test151] starting deploy of {'pull': 'config', 'config': True} to test151

## 2026-06-14 

* 19:02 SomeRandomDeveloper: manually deployed patch for T15477
* 19:01 MirahezeLSBot: [somerandomdeveloper@mwtask181] finished deploy of {'world': True, 'versions': '1.45'} to all - SUCCESS in 218s
* 18:57 MirahezeLSBot: [somerandomdeveloper@mwtask181] starting deploy of {'world': True, 'versions': '1.45'} to all
* 18:55 MirahezeLSBot: [somerandomdeveloper@test151] finished deploy of {'world': True, 'versions': '1.45'} to test151 - SUCCESS in 19s
* 18:55 MirahezeLSBot: [somerandomdeveloper@test151] starting deploy of {'world': True, 'versions': '1.45'} to test151
* 18:52 MirahezeLSBot: [somerandomdeveloper@test151] finished deploy of {'world': True, 'versions': '1.45'} to test151 - SUCCESS in 28s
* 18:52 MirahezeLSBot: [somerandomdeveloper@test151] starting deploy of {'world': True, 'versions': '1.45'} to test151
* 17:19 MirahezeLSBot: [somerandomdeveloper@mwtask181] finished deploy of {'force_upgrade': True, 'versions': '1.45', 'upgrade_extensions': 'CommentStreams'} to all - SUCCESS in 28s
* 17:18 MirahezeLSBot: [somerandomdeveloper@mwtask181] starting deploy of {'force_upgrade': True, 'versions': '1.45', 'upgrade_extensions': 'CommentStreams'} to all
* 17:18 MirahezeLSBot: [somerandomdeveloper@mwtask181] starting deploy of {'force_upgrade': True, 'versions': '1.45', 'upgrade_extensions': 'CommentStreams'} to all
* 17:17 MirahezeLSBot: [somerandomdeveloper@test151] finished deploy of {'force_upgrade': True, 'versions': '1.45', 'upgrade_extensions': 'CommentStreams'} to test151 - SUCCESS in 1s
* 17:17 MirahezeLSBot: [somerandomdeveloper@test151] starting deploy of {'force_upgrade': True, 'versions': '1.45', 'upgrade_extensions': 'CommentStreams'} to test151
* 17:17 MirahezeLSBot: [somerandomdeveloper@test151] finished deploy of {'versions': '1.45', 'upgrade_extensions': 'CommentStreams'} to test151 - SUCCESS in 0s
* 17:17 MirahezeLSBot: [somerandomdeveloper@test151] starting deploy of {'versions': '1.45', 'upgrade_extensions': 'CommentStreams'} to test151
* 17:05 MirahezeLSBot: [somerandomdeveloper@mwtask181] starting deploy of {'force_upgrade': True, 'versions': '1.45', 'upgrade_extensions': 'CommentStreams'} to all
* 17:05 MirahezeLSBot: [somerandomdeveloper@mwtask181] finished deploy of {'versions': '1.45', 'upgrade_extensions': 'CommentStreams'} to all - SUCCESS in 1s
* 17:05 MirahezeLSBot: [somerandomdeveloper@mwtask181] starting deploy of {'versions': '1.45', 'upgrade_extensions': 'CommentStreams'} to all

## 2026-06-13 

* 18:39 MirahezeLSBot: [void@db171] restart sql-backup service
* 12:58 MirahezeLSBot: [wwr@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:ReplaceTextEligible --wiki=pinmasterwiki (END - exit=0)
* 12:05 MirahezeLSBot: [wwr@mwtask181] finished deploy of {'versions': '1.45', 'upgrade_extensions': 'CommentStreams'} to all - SUCCESS in 0s
* 12:05 MirahezeLSBot: [wwr@mwtask181] starting deploy of {'versions': '1.45', 'upgrade_extensions': 'CommentStreams'} to all
* 08:21 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php refreshLinks --wiki=fantendowiki (END - exit=256)
* 01:33 MirahezeLSBot: [somerandomdeveloper@mwtask181] starting deploy of {'versions': '1.45', 'upgrade_extensions': 'CommentStreams'} to all
* 01:26 MirahezeLSBot: [somerandomdeveloper@test151] finished deploy of {'versions': ['1.45', '1.46'], 'upgrade_extensions': 'CommentStreams'} to test151 - SUCCESS in 1s
* 01:26 MirahezeLSBot: [somerandomdeveloper@test151] starting deploy of {'versions': ['1.45', '1.46'], 'upgrade_extensions': 'CommentStreams'} to test151
* 01:25 MirahezeLSBot: [somerandomdeveloper@test151] starting deploy of {'versions': ['1.45', '1.46'], 'upgrade_extensions': 'CommentStreams'} to test151
* 01:08 MirahezeLSBot: [somerandomdeveloper@mwtask181] finished deploy of {'config': True, 'force': True} to all - SUCCESS in 18s
* 01:08 SomeRandomDeveloper: repool c2
* 01:08 MirahezeLSBot: [somerandomdeveloper@mwtask181] starting deploy of {'config': True, 'force': True} to all
* 01:05 MirahezeLSBot: [somerandomdeveloper@mwtask181] finished deploy of {'config': True, 'force': True} to all - SUCCESS in 20s
* 01:04 MirahezeLSBot: [somerandomdeveloper@mwtask181] starting deploy of {'config': True, 'force': True} to all

## 2026-06-12 

* 23:34 MirahezeLSBot: [void@puppet181] Upgraded packages on test151: libjxl0.11 and librabbitmq4
* 23:34 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask161: libjxl0.11 and librabbitmq4
* 23:34 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask181: libjxl0.11 and librabbitmq4
* 23:33 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask171: libjxl0.11 and librabbitmq4
* 23:33 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask151: libjxl0.11 and librabbitmq4
* 23:33 MirahezeLSBot: [void@puppet181] Upgraded packages on mw181: libjxl0.11 and librabbitmq4
* 23:32 MirahezeLSBot: [void@puppet181] Upgraded packages on mw193: libjxl0.11 and librabbitmq4
* 23:32 MirahezeLSBot: [void@puppet181] Upgraded packages on mw203: libjxl0.11 and librabbitmq4
* 23:31 MirahezeLSBot: [void@puppet181] Upgraded packages on mw182: libjxl0.11 and librabbitmq4
* 23:31 MirahezeLSBot: [void@puppet181] Upgraded packages on mw192: libjxl0.11 and librabbitmq4
* 23:30 MirahezeLSBot: [void@puppet181] Upgraded packages on mw201: libjxl0.11 and librabbitmq4
* 23:30 MirahezeLSBot: [void@puppet181] Upgraded packages on mw202: libjxl0.11 and librabbitmq4
* 23:30 MirahezeLSBot: [void@puppet181] Upgraded packages on mw163: libjxl0.11 and librabbitmq4
* 23:29 MirahezeLSBot: [void@puppet181] Upgraded packages on mw171: libjxl0.11 and librabbitmq4
* 23:29 MirahezeLSBot: [void@puppet181] Upgraded packages on mw172: libjxl0.11 and librabbitmq4
* 23:29 MirahezeLSBot: [void@puppet181] Upgraded packages on mw162: libjxl0.11 and librabbitmq4
* 23:28 MirahezeLSBot: [void@puppet181] Upgraded packages on mw191: libjxl0.11 and librabbitmq4
* 23:28 MirahezeLSBot: [void@puppet181] Upgraded packages on mw173: libjxl0.11 and librabbitmq4
* 23:28 MirahezeLSBot: [void@puppet181] Upgraded packages on mw161: libjxl0.11 and librabbitmq4
* 23:27 MirahezeLSBot: [void@puppet181] Upgraded packages on mw152: libjxl0.11 and librabbitmq4
* 23:27 MirahezeLSBot: [void@puppet181] Upgraded packages on mw151: libjxl0.11 and librabbitmq4
* 23:27 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud18: librabbitmq4
* 23:27 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud20: librabbitmq4
* 23:26 MirahezeLSBot: [void@puppet181] Upgraded packages on mw153: libjxl0.11 and librabbitmq4
* 23:26 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud19: librabbitmq4
* 23:26 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud17: librabbitmq4
* 23:25 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud16: librabbitmq4
* 23:25 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud15: librabbitmq4
* 23:25 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud21: librabbitmq4
* 01:21 MirahezeLSBot: [void@puppet181] Upgraded packages on kafka182: libjackson2-core-java and libjackson2-databind-java
* 01:19 MirahezeLSBot: [void@puppet181] Upgraded packages on puppet181: libdbi-perl
* 01:16 MirahezeLSBot: [void@puppet181] Upgraded packages on test151: libinput-bin and libinput10
* 01:16 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask181: libinput-bin and libinput10
* 01:16 MirahezeLSBot: [void@puppet181] Upgraded packages on mw201: libinput-bin and libinput10
* 01:16 MirahezeLSBot: [void@puppet181] Upgraded packages on mw203: libinput-bin and libinput10
* 01:15 MirahezeLSBot: [void@puppet181] Upgraded packages on mw202: libinput-bin and libinput10
* 01:15 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask151: libinput-bin and libinput10
* 01:14 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask171: libinput-bin and libinput10
* 01:14 MirahezeLSBot: [void@puppet181] Upgraded packages on mw193: libinput-bin and libinput10
* 01:14 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask161: libinput-bin and libinput10
* 01:13 MirahezeLSBot: [void@puppet181] Upgraded packages on reports171: libdbi-perl
* 01:13 MirahezeLSBot: [void@puppet181] Upgraded packages on phorge171: libdbi-perl
* 01:13 MirahezeLSBot: [void@puppet181] Upgraded packages on mw192: libinput-bin and libinput10
* 01:13 MirahezeLSBot: [void@puppet181] Upgraded packages on mw183: libinput-bin and libinput10
* 01:12 MirahezeLSBot: [void@puppet181] Upgraded packages on mw182: libinput-bin and libinput10
* 01:12 MirahezeLSBot: [void@puppet181] Upgraded packages on mw181: libinput-bin and libinput10
* 01:12 MirahezeLSBot: [void@puppet181] Upgraded packages on mw191: libinput-bin and libinput10
* 01:11 MirahezeLSBot: [void@puppet181] Upgraded packages on mw161: libinput-bin and libinput10
* 01:11 MirahezeLSBot: [void@puppet181] Upgraded packages on mw163: libinput-bin and libinput10
* 01:10 MirahezeLSBot: [void@puppet181] Upgraded packages on mw152: libinput-bin and libinput10
* 01:10 MirahezeLSBot: [void@puppet181] Upgraded packages on mw171: libinput-bin and libinput10
* 01:10 MirahezeLSBot: [void@puppet181] Upgraded packages on mw173: libinput-bin and libinput10
* 01:10 MirahezeLSBot: [void@puppet181] Upgraded packages on mw172: libinput-bin and libinput10
* 01:09 MirahezeLSBot: [void@puppet181] Upgraded packages on mon181: libdbi-perl
* 01:09 MirahezeLSBot: [void@puppet181] Upgraded packages on mw162: libinput-bin and libinput10
* 01:09 MirahezeLSBot: [void@puppet181] Upgraded packages on db201: libdbi-perl
* 01:08 MirahezeLSBot: [void@puppet181] Upgraded packages on db192: libdbi-perl
* 01:08 MirahezeLSBot: [void@puppet181] Upgraded packages on mw153: libinput-bin and libinput10
* 01:08 MirahezeLSBot: [void@puppet181] Upgraded packages on mw151: libinput-bin and libinput10
* 01:07 MirahezeLSBot: [void@puppet181] Upgraded packages on bast181: libdbi-perl
* 01:07 MirahezeLSBot: [void@puppet181] Upgraded packages on db181: libdbi-perl
* 01:07 MirahezeLSBot: [void@puppet181] Upgraded packages on db161: libdbi-perl
* 01:07 MirahezeLSBot: [void@puppet181] Upgraded packages on db182: libdbi-perl
* 01:06 MirahezeLSBot: [void@puppet181] Upgraded packages on db171: libdbi-perl
* 01:06 MirahezeLSBot: [void@puppet181] Upgraded packages on db151: libdbi-perl
* 01:06 MirahezeLSBot: [void@puppet181] Upgraded packages on db172: libdbi-perl
* 01:05 MirahezeLSBot: [void@puppet181] Upgraded packages on bast161: libdbi-perl
* 01:05 MirahezeLSBot: [void@puppet181] Upgraded packages on mattermost2: libdbi-perl

## 2026-06-11 

* 22:46 MirahezeLSBot: [somerandomdeveloper@mwtask181] finished deploy of {'config': True, 'force': True} to all - SUCCESS in 18s
* 22:46 SomeRandomDeveloper: repool c2
* 22:46 MirahezeLSBot: [somerandomdeveloper@mwtask181] starting deploy of {'config': True, 'force': True} to all
* 22:44 MirahezeLSBot: [somerandomdeveloper@mwtask181] finished deploy of {'config': True, 'force': True} to all - SUCCESS in 20s
* 22:43 MirahezeLSBot: [somerandomdeveloper@mwtask181] starting deploy of {'config': True, 'force': True} to all
* 22:43 MirahezeLSBot: [somerandomdeveloper@mwtask181] DEPLOY ABORTED: Canary check failed for publictestwiki.com@mw151
* 22:43 MirahezeLSBot: [somerandomdeveloper@mwtask181] starting deploy of {'config': True} to all

## 2026-06-10 

* 21:27 MirahezeLSBot: [macfan@test151] finished deploy of {'pull': 'config', 'config': True, 'world': True, 'l10n': True, 'extension_list': True, 'versions': ['1.45', '1.46']} to test151 - SUCCESS in 470s
* 21:23 MirahezeLSBot: [macfan@mwtask181] finished deploy of {'pull': 'config', 'config': True, 'world': True, 'l10n': True, 'extension_list': True, 'versions': '1.45'} to all - SUCCESS in 791s
* 21:19 MirahezeLSBot: [macfan@test151] starting deploy of {'pull': 'config', 'config': True, 'world': True, 'l10n': True, 'extension_list': True, 'versions': ['1.45', '1.46']} to test151
* 21:16 MirahezeLSBot: [macfan@test151] DEPLOY ABORTED: Non-Zero Exit Code in prep, see output.
* 21:10 MirahezeLSBot: [macfan@test151] starting deploy of {'pull': 'config', 'config': True, 'world': True, 'l10n': True, 'extension_list': True, 'versions': ['1.45', '1.46']} to test151
* 21:10 MirahezeLSBot: [macfan@mwtask181] starting deploy of {'pull': 'config', 'config': True, 'world': True, 'l10n': True, 'extension_list': True, 'versions': '1.45'} to all
* 21:06 MirahezeLSBot: [macfan@test151] sudo -u www-data php /srv/mediawiki/1.46/maintenance/run.php ManageWiki:PopulateWikiSettings --wiki=loginwikibeta --setting=egChameleonLayoutFile --remove --all-wikis --execute (END - exit=0)
* 21:06 MirahezeLSBot: [macfan@test151] sudo -u www-data php /srv/mediawiki/1.46/maintenance/run.php ManageWiki:PopulateWikiSettings --wiki=loginwikibeta --setting=egChameleonEnableExternalLinkIcons --remove --all-wikis --execute (END - exit=0)
* 21:05 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php ManageWiki:PopulateWikiSettings --wiki=loginwiki --setting=egChameleonEnableExternalLinkIcons --remove --all-wikis --execute (END - exit=0)
* 21:00 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php ManageWiki:PopulateWikiSettings --wiki=loginwiki --setting=egChameleonLayoutFile --remove --all-wikis --execute (END - exit=0)
* 20:53 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php ManageWiki:ToggleExtension --wiki=loginwiki --name=chameleon --disable --all-wikis --execute (END - exit=0)
* 20:52 MirahezeLSBot: [macfan@test151] sudo -u www-data php /srv/mediawiki/1.46/maintenance/run.php ManageWiki:ToggleExtension --wiki=loginwikibeta --name=chameleon --disable --all-wikis --execute (END - exit=0)
* 20:52 MirahezeLSBot: [macfan@test151] sudo -u www-data php /srv/mediawiki/1.46/maintenance/run.php ManageWiki:ToggleExtension --wiki=loginwiki --name=chameleon --disable --all-wikis --execute (END - exit=512)
* 20:04 MirahezeLSBot: [macfan@test151] DEPLOY ABORTED: Non-Zero Exit Code in prep, see output.
* 20:04 MirahezeLSBot: [macfan@test151] starting deploy of {'pull': 'world', 'world': True, 'versions': '1.46', 'upgrade_skins': 'chameleon'} to test151
* 19:59 MirahezeLSBot: [macfan@test151] DEPLOY ABORTED: Non-Zero Exit Code in prep, see output.
* 19:59 MirahezeLSBot: [macfan@test151] starting deploy of {'pull': 'world', 'world': True, 'versions': '1.46'} to test151
* 07:43 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject201: openssl-provider-legacy, libssl3t64, and openssl
* 07:43 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject191: openssl-provider-legacy, libssl3t64, and openssl
* 07:42 MirahezeLSBot: [void@puppet181] Upgraded packages on test151: libssl-dev, openssl-provider-legacy, libssl3t64, poppler-utils, libpoppler-glib8t64, libpoppler147, and openssl
* 07:42 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftproxy161: openssl-provider-legacy, libssl3t64, and openssl
* 07:41 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftproxy171: openssl-provider-legacy, libssl3t64, and openssl
* 07:41 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject211: openssl-provider-legacy, libssl3t64, and openssl
* 07:41 MirahezeLSBot: [void@puppet181] Upgraded packages on ns2: openssl-provider-legacy, libssl3t64, and openssl
* 07:40 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject181: openssl-provider-legacy, libssl3t64, and openssl
* 07:40 MirahezeLSBot: [void@puppet181] Upgraded packages on os201: openssl-provider-legacy, libssl3t64, and openssl
* 07:39 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject161: openssl-provider-legacy, libssl3t64, and openssl
* 07:39 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject171: openssl-provider-legacy, libssl3t64, and openssl
* 07:39 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftac171: openssl-provider-legacy, libssl3t64, and openssl
* 07:39 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject151: openssl-provider-legacy, libssl3t64, and openssl
* 07:38 MirahezeLSBot: [void@puppet181] Upgraded packages on os202: openssl-provider-legacy, libssl3t64, and openssl
* 07:38 MirahezeLSBot: [void@puppet181] Upgraded packages on rdb191: openssl-provider-legacy, libssl3t64, and openssl
* 07:37 MirahezeLSBot: [void@puppet181] Upgraded packages on puppet181: openssl-provider-legacy, libssl3t64, and openssl
* 07:37 MirahezeLSBot: [void@puppet181] Upgraded packages on os191: openssl-provider-legacy, libssl3t64, and openssl
* 07:37 MirahezeLSBot: [void@puppet181] Upgraded packages on reports171: openssl-provider-legacy, libssl3t64, and openssl
* 07:36 MirahezeLSBot: [void@puppet181] Upgraded packages on os151: openssl-provider-legacy, libssl3t64, and openssl
* 07:36 MirahezeLSBot: [void@puppet181] Upgraded packages on prometheus151: openssl-provider-legacy, libssl3t64, and openssl
* 07:36 MirahezeLSBot: [void@puppet181] Upgraded packages on os162: openssl-provider-legacy, libssl3t64, and openssl
* 07:35 MirahezeLSBot: [void@puppet181] Upgraded packages on phorge171: openssl-provider-legacy, libssl3t64, and openssl
* 07:35 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask181: openssl-provider-legacy, libssl3t64, poppler-utils, libpoppler-glib8t64, libpoppler147, and openssl
* 07:35 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask151: openssl-provider-legacy, libssl3t64, poppler-utils, libpoppler-glib8t64, libpoppler147, and openssl
* 07:34 MirahezeLSBot: [void@puppet181] Upgraded packages on os161: openssl-provider-legacy, libssl3t64, and openssl
* 07:34 MirahezeLSBot: [void@puppet181] Upgraded packages on ns1: openssl-provider-legacy, libssl3t64, and openssl
* 07:34 MirahezeLSBot: [void@puppet181] Upgraded packages on mw203: openssl-provider-legacy, libssl3t64, poppler-utils, libpoppler-glib8t64, libpoppler147, and openssl
* 07:33 MirahezeLSBot: [void@puppet181] Upgraded packages on mw202: openssl-provider-legacy, libssl3t64, poppler-utils, libpoppler-glib8t64, libpoppler147, and openssl
* 07:33 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask161: openssl-provider-legacy, libssl3t64, poppler-utils, libpoppler-glib8t64, libpoppler147, and openssl
* 07:32 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask171: openssl-provider-legacy, libssl3t64, poppler-utils, libpoppler-glib8t64, libpoppler147, and openssl
* 07:32 MirahezeLSBot: [void@puppet181] Upgraded packages on mw201: openssl-provider-legacy, libssl3t64, poppler-utils, libpoppler-glib8t64, libpoppler147, and openssl
* 07:31 MirahezeLSBot: [void@puppet181] Upgraded packages on mw183: openssl-provider-legacy, libssl3t64, poppler-utils, libpoppler-glib8t64, libpoppler147, and openssl
* 07:31 MirahezeLSBot: [void@puppet181] Upgraded packages on mw192: openssl-provider-legacy, libssl3t64, poppler-utils, libpoppler-glib8t64, libpoppler147, and openssl
* 07:31 MirahezeLSBot: [void@puppet181] Upgraded packages on mw181: openssl-provider-legacy, libssl3t64, poppler-utils, libpoppler-glib8t64, libpoppler147, and openssl
* 07:30 MirahezeLSBot: [void@puppet181] Upgraded packages on mw193: openssl-provider-legacy, libssl3t64, poppler-utils, libpoppler-glib8t64, libpoppler147, and openssl
* 07:30 MirahezeLSBot: [void@puppet181] Upgraded packages on mw182: openssl-provider-legacy, libssl3t64, poppler-utils, libpoppler-glib8t64, libpoppler147, and openssl
* 07:29 MirahezeLSBot: [void@puppet181] Upgraded packages on mw191: openssl-provider-legacy, libssl3t64, poppler-utils, libpoppler-glib8t64, libpoppler147, and openssl
* 07:29 MirahezeLSBot: [void@puppet181] Upgraded packages on mw161: openssl-provider-legacy, libssl3t64, poppler-utils, libpoppler-glib8t64, libpoppler147, and openssl
* 07:28 MirahezeLSBot: [void@puppet181] Upgraded packages on mw173: openssl-provider-legacy, libssl3t64, poppler-utils, libpoppler-glib8t64, libpoppler147, and openssl
* 07:28 MirahezeLSBot: [void@puppet181] Upgraded packages on mw163: openssl-provider-legacy, libssl3t64, poppler-utils, libpoppler-glib8t64, libpoppler147, and openssl
* 07:28 MirahezeLSBot: [void@puppet181] Upgraded packages on mw172: openssl-provider-legacy, libssl3t64, poppler-utils, libpoppler-glib8t64, libpoppler147, and openssl
* 07:27 MirahezeLSBot: [void@puppet181] Upgraded packages on mw171: openssl-provider-legacy, libssl3t64, poppler-utils, libpoppler-glib8t64, libpoppler147, and openssl
* 07:27 MirahezeLSBot: [void@puppet181] Upgraded packages on mw162: openssl-provider-legacy, libssl3t64, poppler-utils, libpoppler-glib8t64, libpoppler147, and openssl
* 07:27 MirahezeLSBot: [void@puppet181] Upgraded packages on mem191: openssl-provider-legacy, libssl3t64, and openssl
* 07:26 MirahezeLSBot: [void@puppet181] Upgraded packages on mon181: openssl-provider-legacy, libssl3t64, and openssl
* 07:26 MirahezeLSBot: [void@puppet181] Upgraded packages on mw153: openssl-provider-legacy, libssl3t64, poppler-utils, libpoppler-glib8t64, libpoppler147, and openssl
* 07:26 MirahezeLSBot: [void@puppet181] Upgraded packages on mw152: openssl-provider-legacy, libssl3t64, poppler-utils, libpoppler-glib8t64, libpoppler147, and openssl
* 07:25 MirahezeLSBot: [void@puppet181] Upgraded packages on mw151: openssl-provider-legacy, libssl3t64, poppler-utils, libpoppler-glib8t64, libpoppler147, and openssl
* 07:25 MirahezeLSBot: [void@puppet181] Upgraded packages on llm191: openssl-provider-legacy, libssl3t64, and openssl
* 07:25 MirahezeLSBot: [void@puppet181] Upgraded packages on mem201: openssl-provider-legacy, libssl3t64, and openssl
* 07:24 MirahezeLSBot: [void@puppet181] Upgraded packages on matomo151: openssl-provider-legacy, libssl3t64, and openssl
* 07:24 MirahezeLSBot: [void@puppet181] Upgraded packages on mem151: openssl-provider-legacy, libssl3t64, and openssl
* 07:24 MirahezeLSBot: [void@puppet181] Upgraded packages on kafka182: openssl-provider-legacy, libssl3t64, and openssl
* 07:23 MirahezeLSBot: [void@puppet181] Upgraded packages on mem161: openssl-provider-legacy, libssl3t64, and openssl
* 07:23 MirahezeLSBot: [void@puppet181] Upgraded packages on ldap171: openssl-provider-legacy, libssl3t64, and openssl
* 07:23 MirahezeLSBot: [void@puppet181] Upgraded packages on mattermost2: openssl-provider-legacy, libssl3t64, and openssl
* 07:22 MirahezeLSBot: [void@puppet181] Upgraded packages on db192: openssl-provider-legacy, libssl3t64, and openssl
* 07:22 MirahezeLSBot: [void@puppet181] Upgraded packages on cp201: openssl-provider-legacy, libssl3t64, and openssl
* 07:22 MirahezeLSBot: [void@puppet181] Upgraded packages on db182: openssl-provider-legacy, libssl3t64, and openssl
* 07:21 MirahezeLSBot: [void@puppet181] Upgraded packages on eventgate182: libssl-dev, openssl-provider-legacy, libssl3t64, and openssl
* 07:21 MirahezeLSBot: [void@puppet181] Upgraded packages on db181: openssl-provider-legacy, libssl3t64, and openssl
* 07:21 MirahezeLSBot: [void@puppet181] Upgraded packages on db201: openssl-provider-legacy, libssl3t64, and openssl
* 07:20 MirahezeLSBot: [void@puppet181] Upgraded packages on graylog161: openssl-provider-legacy, libssl3t64, and openssl
* 07:20 MirahezeLSBot: [void@puppet181] Upgraded packages on db151: openssl-provider-legacy, libssl3t64, and openssl
* 07:20 MirahezeLSBot: [void@puppet181] Upgraded packages on bast181: openssl-provider-legacy, libssl3t64, and openssl
* 07:19 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud19: openssl-provider-legacy, libssl3t64, and openssl
* 07:19 MirahezeLSBot: [void@puppet181] Upgraded packages on cp171: openssl-provider-legacy, libssl3t64, and openssl
* 07:19 MirahezeLSBot: [void@puppet181] Upgraded packages on db161: openssl-provider-legacy, libssl3t64, and openssl
* 07:18 MirahezeLSBot: [void@puppet181] Upgraded packages on cp191: openssl-provider-legacy, libssl3t64, and openssl
* 07:18 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud20: openssl-provider-legacy, libssl3t64, and openssl
* 07:18 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud17: openssl-provider-legacy, libssl3t64, and openssl
* 07:17 MirahezeLSBot: [void@puppet181] Upgraded packages on cp161: openssl-provider-legacy, libssl3t64, and openssl
* 07:17 MirahezeLSBot: [void@puppet181] Upgraded packages on db172: openssl-provider-legacy, libssl3t64, and openssl
* 07:17 MirahezeLSBot: [void@puppet181] Upgraded packages on changeprop202: libssl-dev, openssl-provider-legacy, libssl3t64, and openssl
* 07:16 MirahezeLSBot: [void@puppet181] Upgraded packages on db171: openssl-provider-legacy, libssl3t64, and openssl
* 07:16 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud18: openssl-provider-legacy, libssl3t64, and openssl
* 07:16 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud15: openssl-provider-legacy, libssl3t64, and openssl
* 07:16 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud16: openssl-provider-legacy, libssl3t64, and openssl
* 07:15 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud21: openssl-provider-legacy, libssl3t64, and openssl
* 07:15 MirahezeLSBot: [void@puppet181] Upgraded packages on bast161: openssl-provider-legacy, libssl3t64, and openssl
* 07:15 MirahezeLSBot: [void@puppet181] Upgraded packages on bots171: openssl-provider-legacy, libssl3t64, and openssl
* 07:13 MirahezeLSBot: [void@db181] restart sql-backup

## 2026-06-09 

* 23:05 MirahezeLSBot: [somerandomdeveloper@test151] DEPLOY ABORTED: Non-Zero Exit Code in prep, see output.
* 23:04 MirahezeLSBot: [somerandomdeveloper@test151] starting deploy of {'pull': 'world', 'world': True, 'versions': '1.46'} to test151

## 2026-06-08 

* 22:49 SomeRandomDeveloper: deployed new patches for T15475
* 19:41 MirahezeLSBot: [void@puppet181] Upgraded packages on test151: strongswan-starter, libcharon-extauth-plugins, libcharon-extra-plugins, strongswan-pki, strongswan-libcharon, strongswan-charon, libstrongswan, and libstrongswan-standard-plugins
* 16:41 MirahezeLSBot: [wwr@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php initSiteStats --wiki=gsgwwiki --update (END - exit=0)
* 16:40 MirahezeLSBot: [wwr@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php initSiteStats --wiki=gsgwwiki (END - exit=0)

## 2026-06-07 

* 22:54 MirahezeLSBot: [void@puppet181] Upgraded packages on puppet181: nginx and nginx-common
* 22:54 MirahezeLSBot: [void@puppet181] Upgraded packages on cp161: nginx and nginx-common
* 22:17 MirahezeLSBot: [void@puppet181] Upgraded packages on test151: nginx and nginx-common
* 22:17 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftproxy161: nginx and nginx-common
* 22:16 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftproxy171: nginx and nginx-common
* 22:16 MirahezeLSBot: [void@puppet181] Upgraded packages on os202: nginx and nginx-common
* 22:15 MirahezeLSBot: [void@puppet181] Upgraded packages on os162: nginx and nginx-common
* 22:15 MirahezeLSBot: [void@puppet181] Upgraded packages on reports171: nginx and nginx-common
* 22:14 MirahezeLSBot: [void@puppet181] Upgraded packages on phorge171: nginx and nginx-common
* 22:14 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask181: nginx and nginx-common
* 22:14 MirahezeLSBot: [void@puppet181] Upgraded packages on os151: nginx and nginx-common
* 22:13 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask171: nginx and nginx-common
* 22:13 MirahezeLSBot: [void@puppet181] Upgraded packages on mw193: nginx and nginx-common
* 22:11 MirahezeLSBot: [void@puppet181] Upgraded packages on mw182: nginx and nginx-common
* 22:09 MirahezeLSBot: [void@puppet181] Upgraded packages on mw181: nginx and nginx-common
* 22:08 MirahezeLSBot: [void@puppet181] Upgraded packages on mw183: nginx and nginx-common
* 22:07 MirahezeLSBot: [void@puppet181] Upgraded packages on mw192: nginx and nginx-common
* 22:06 MirahezeLSBot: [void@puppet181] Upgraded packages on mw202: nginx and nginx-common
* 22:04 MirahezeLSBot: [void@puppet181] Upgraded packages on mw203: nginx and nginx-common
* 22:03 MirahezeLSBot: [void@puppet181] Upgraded packages on mw163: nginx and nginx-common
* 22:02 MirahezeLSBot: [void@puppet181] Upgraded packages on mw152: nginx and nginx-common
* 22:01 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask161: nginx and nginx-common
* 22:00 MirahezeLSBot: [void@puppet181] Upgraded packages on mw201: nginx and nginx-common
* 21:59 MirahezeLSBot: [void@puppet181] Upgraded packages on mw191: nginx and nginx-common
* 21:57 MirahezeLSBot: [void@puppet181] Upgraded packages on mw173: nginx and nginx-common
* 21:55 MirahezeLSBot: [void@puppet181] Upgraded packages on mw171: nginx and nginx-common
* 21:54 MirahezeLSBot: [void@puppet181] Upgraded packages on mw172: nginx and nginx-common
* 21:53 MirahezeLSBot: [void@puppet181] Upgraded packages on mw153: nginx and nginx-common
* 21:52 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask151: nginx and nginx-common
* 21:51 MirahezeLSBot: [void@puppet181] Upgraded packages on mon181: nginx and nginx-common
* 21:51 MirahezeLSBot: [void@puppet181] Upgraded packages on mw162: nginx and nginx-common
* 21:49 MirahezeLSBot: [void@puppet181] Upgraded packages on mw161: nginx and nginx-common
* 21:48 MirahezeLSBot: [void@puppet181] Upgraded packages on mw151: nginx and nginx-common
* 21:47 MirahezeLSBot: [void@puppet181] Upgraded packages on graylog161: nginx and nginx-common
* 21:46 MirahezeLSBot: [void@puppet181] Upgraded packages on llm191: nginx and nginx-common
* 21:46 MirahezeLSBot: [void@puppet181] Upgraded packages on matomo151: nginx and nginx-common
* 21:45 MirahezeLSBot: [void@puppet181] Upgraded packages on mattermost2: nginx and nginx-common
* 15:51 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php /srv/mediawiki/1.45/maintenance/initSiteStats.php --wiki=hoggieswiki --update (END - exit=0)
* 15:51 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php /srv/mediawiki/1.45/maintenance/rebuildall.php --wiki=hoggieswiki (END - exit=0)
* 15:40 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php /srv/mediawiki/1.45/maintenance/rebuildall.php --wiki=hoggieswiki (START)
* 15:40 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php /srv/mediawiki/1.45/maintenance/importDump.php --wiki=hoggieswiki dump.xml --no-updates (END - exit=0)
* 15:27 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php /srv/mediawiki/1.45/maintenance/importDump.php --wiki=hoggieswiki dump.xml --no-updates (START)

## 2026-06-06 

* 23:46 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask181: apache2, apache2-bin, apache2-data, and apache2-utils
* 23:46 MirahezeLSBot: [void@puppet181] Upgraded packages on test151: apache2, apache2-bin, apache2-data, and apache2-utils
* 23:45 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask171: apache2, apache2-bin, apache2-data, and apache2-utils
* 23:44 MirahezeLSBot: [void@puppet181] Upgraded packages on mon181: apache2-bin and apache2-utils
* 23:44 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask161: apache2, apache2-bin, apache2-data, and apache2-utils
* 23:43 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask151: apache2, apache2-bin, apache2-data, and apache2-utils
* 23:42 MirahezeLSBot: [void@puppet181] Upgraded packages on prometheus151: apache2, apache2-bin, apache2-data, and apache2-utils
* 21:55 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php refreshLinks --wiki=fantendowiki (START)
* 21:54 MirahezeLSBot: [skye@mwtask171] Finished import for fantendowiki (XML: fantendo_pages_full.xml; Images: None) (END - exit=-2)
* 21:54 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php rebuildall --wiki=fantendowiki (END - exit=-2)
* 21:46 MirahezeLSBot: [skye@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 26s
* 21:46 MirahezeLSBot: [skye@test151] finished deploy of {'pull': 'config', 'config': True} to test151 - SUCCESS in 0s
* 21:46 MirahezeLSBot: [skye@test151] starting deploy of {'pull': 'config', 'config': True} to test151
* 21:46 MirahezeLSBot: [skye@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 21:46 MirahezeLSBot: [skye@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 20:49 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php initSiteStats --wiki=fantendowiki (END - exit=0)
* 20:42 MirahezeLSBot: [wwr@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php nukeNS --wiki=fantendowiki --delete --all --ns=3006 (END - exit=0)
* 20:37 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php nukeNS --wiki=fantendowiki --delete --all --ns=3008 (END - exit=0)
* 20:36 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php nukeNS --wiki=fantendowiki --delete --all --ns=3008 (START)
* 20:35 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php nukeNS --wiki=fantendowiki --delete --all --ns=3016 (END - exit=0)
* 20:35 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php nukeNS --wiki=fantendowiki --delete --all --ns=3016 (START)
* 20:35 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php nukeNS --wiki=fantendowiki --delete --all --ns=3012 (END - exit=0)
* 20:35 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php nukeNS --wiki=fantendowiki --delete --all --ns=3012 (START)
* 20:34 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php nukeNS --wiki=fantendowiki --delete --all --ns=3010 (END - exit=0)
* 20:34 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php nukeNS --wiki=fantendowiki --delete --all --ns=3010 (START)
* 20:31 MirahezeLSBot: [skye@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php namespaceDupes --wiki=fantendowiki --fix (END - exit=0)
* 20:26 MirahezeLSBot: [wwr@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php nukeNS --wiki=fantendowiki --delete --all --ns=3006 (START)
* 20:26 MirahezeLSBot: [wwr@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php nukeNS --wiki=fantendowiki --delete --all --ns=3004 (END - exit=0)
* 19:21 MirahezeLSBot: [wwr@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php nukeNS --wiki=fantendowiki --delete --all --ns=3004 (START)
* 19:20 MirahezeLSBot: [wwr@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php nukeNS --wiki=fantendowiki --delete --all --ns=3002 (END - exit=0)
* 19:15 MirahezeLSBot: [wwr@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php nukeNS --wiki=fantendowiki --delete --all --ns=3002 (START)
* 19:15 MirahezeLSBot: [wwr@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php nukeNS --wiki=fantendowiki --delete --all --ns=1 (END - exit=0)
* 18:54 MirahezeLSBot: [wwr@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php nukeNS --wiki=fantendowiki --delete --all --ns=1 (START)
* 18:53 MirahezeLSBot: [wwr@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php nukeNS --wiki=fantendowiki --delete --ns=1 --ns=3002 --ns=3004 --ns=3006 --ns=3008 --ns=3010 --ns=3012 --ns=3016 --all (END - exit=256)
* 18:53 MirahezeLSBot: [wwr@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php nukeNS --wiki=fantendowiki --delete --ns=1 --ns=3002 --ns=3004 --ns=3006 --ns=3008 --ns=3010 --ns=3012 --ns=3016 --all (START)
* 16:46 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php /srv/mediawiki/1.45/maintenance/initSiteStats.php --wiki=sneakysasquatchwiki --update (END - exit=0)
* 16:46 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php /srv/mediawiki/1.45/maintenance/rebuildall.php --wiki=sneakysasquatchwiki (END - exit=0)
* 16:04 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php /srv/mediawiki/1.45/maintenance/rebuildall.php --wiki=sneakysasquatchwiki (START)
* 16:04 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php /srv/mediawiki/1.45/maintenance/importDump.php --wiki=sneakysasquatchwiki dump.xml --no-updates (END - exit=0)
* 16:01 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php /srv/mediawiki/1.45/maintenance/importDump.php --wiki=sneakysasquatchwiki dump.xml --no-updates (START)
* 12:33 @paladox: apt-get dist-upgrade on puppet181 and reboot
* 12:29 @paladox: apt-get dist-upgrade on mon181 and reboot
* 12:12 @paladox: upgrade icinga2 on mon181
* 12:05 @paladox: upgrade grafana to v13
* 04:09 MirahezeLSBot: [universalomega@mwtask181] finished deploy of {'config': True, 'force': True} to all - SUCCESS in 19s
* 04:08 MirahezeLSBot: [universalomega@mwtask181] starting deploy of {'config': True, 'force': True} to all
* 04:03 Universal Omega: stop and start db161 from host
* 03:45 MirahezeLSBot: [petramagna@mwtask181] starting deploy of {'config': True, 'force': True} to all
* 01:31 TheWWRNerdGuy: `$wgDefaultSkin = "vector-2022"` on fivenightsatfreddyswiki

## 2026-06-04 

* 19:13 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php CreateWiki:SetContainersAccess --wiki=sapphirinedatabasewiki (END - exit=0)
* 19:10 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RenameDatabase --wiki=loginwiki --rename --old=thesapphirinefictionaluniversewiki --new=sapphirinedatabasewiki --user=Skye (END - exit=0)
* 19:07 Skye: c1: DROP DATABASE systemseveredunofficalwikiwiki;
* 19:04 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php CreateWiki:SetContainersAccess --wiki=systemseveredwiki (END - exit=0)
* 19:03 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RenameDatabase --wiki=loginwiki --rename --old=systemseveredunofficalwikiwiki --new=systemseveredwiki --user=Skye (END - exit=0)
* 17:44 MirahezeLSBot: [skye@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 51s
* 17:43 MirahezeLSBot: [skye@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 17:43 MirahezeLSBot: [skye@test151] finished deploy of {'pull': 'config', 'config': True} to test151 - SUCCESS in 0s
* 17:43 MirahezeLSBot: [skye@test151] starting deploy of {'pull': 'config', 'config': True} to test151
* 17:43 @paladox: rebooted bots171
* 17:40 Skye: test
* 00:57 MirahezeLSBot: [skye@mwtask171] Finished import for evnovawiki (XML: evn_pages_full.xml; Images: images) (END - exit=0)
* 00:57 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php initSiteStats --wiki=evnovawiki --update (END - exit=0)
* 00:56 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php initSiteStats --wiki=evnovawiki --update (START)
* 00:56 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php initEditCount --wiki=evnovawiki (END - exit=0)
* 00:56 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php initEditCount --wiki=evnovawiki (START)
* 00:56 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php rebuildall --wiki=evnovawiki (END - exit=0)
* 00:25 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php rebuildall --wiki=evnovawiki (START)
* 00:25 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=evnovawiki --sleep=0 '--comment=Importing files from [https://evn.fandom.com/](https://evn.fandom.com/) ([T15480](https://meta.miraheze.org/wiki/phorge:T15480))' -- images (END - exit=0)
* 00:02 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=evnovawiki --sleep=0 '--comment=Importing files from [https://evn.fandom.com/](https://evn.fandom.com/) ([T15480](https://meta.miraheze.org/wiki/phorge:T15480))' -- images (START)
* 00:02 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importDump --wiki=evnovawiki --no-updates --username-prefix=fandom:evn -- evn_pages_full.xml (END - exit=0)

## 2026-06-03 

* 23:26 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importDump --wiki=evnovawiki --no-updates --username-prefix=fandom:evn -- evn_pages_full.xml (START)
* 23:26 MirahezeLSBot: [skye@mwtask171] Starting import for evnovawiki (XML: evn_pages_full.xml; Images: images) (START)
* 22:49 Skye: [skye@mwtask171] evnovawiki: DELETE FROM text;
* 22:46 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php purgeOldText --wiki=evnovawiki --purge (END - exit=0)
* 22:43 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php nukeNS --wiki=evnovawiki --delete --ns=829 --all (END - exit=0)
* 22:43 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php nukeNS --wiki=evnovawiki --delete --ns=829 --all (START)
* 22:43 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php nukeNS --wiki=evnovawiki --delete --ns=828 --all (END - exit=0)
* 22:43 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php nukeNS --wiki=evnovawiki --delete --ns=828 --all (START)
* 22:42 Skye: for i in {0..15}; do mwscript nukeNS evnovawiki --delete --ns=${i} --all --y --no-log; done
* 22:19 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php nukeNS --wiki=evnovawiki --delete --ns=0 --ns=1 --ns=2 --ns=3 --ns=4 --ns=5 --ns=6 --ns=7 --ns=8 --ns=9 --ns=10 --ns=11 --ns=12 --ns=13 --ns=14 --ns=15 --all (END - exit=256)
* 22:19 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php nukeNS --wiki=evnovawiki --delete --ns=0 --ns=1 --ns=2 --ns=3 --ns=4 --ns=5 --ns=6 --ns=7 --ns=8 --ns=9 --ns=10 --ns=11 --ns=12 --ns=13 --ns=14 --ns=15 --all (START)
* 20:15 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php updateSpecialPages --wiki=fantendowiki --only=MediaStatistics (END - exit=0)
* 20:13 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=fantendowiki . --comment='Importing gifs from fantendo.fandom.com ([T15427](https://meta.miraheze.org/wiki/phorge:T15427))' --skip-dupes (END - exit=0)
* 20:10 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=fantendowiki . --comment='Importing gifs from fantendo.fandom.com ([T15427](https://meta.miraheze.org/wiki/phorge:T15427))' --skip-dupes (START)
* 17:45 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=fantendowiki . --comment='Importing images from fantendo.fandom.com ([T15427](https://meta.miraheze.org/wiki/phorge:T15427))' --skip-dupes (END - exit=256)
* 16:56 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php /srv/mediawiki/1.45/maintenance/initSiteStats.php --wiki=evnovawiki --update (END - exit=0)
* 16:56 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php /srv/mediawiki/1.45/maintenance/rebuildall.php --wiki=evnovawiki (END - exit=0)
* 16:29 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php /srv/mediawiki/1.45/maintenance/rebuildall.php --wiki=evnovawiki (START)
* 16:29 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php /srv/mediawiki/1.45/maintenance/importDump.php --wiki=evnovawiki dump.xml --no-updates (END - exit=0)
* 15:59 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php /srv/mediawiki/1.45/maintenance/importDump.php --wiki=evnovawiki dump.xml --no-updates (START)
* 03:00 MirahezeLSBot: [skye@mwtask171] Finished import for aniphobiawiki (XML: None; Images: .) (END - exit=0)
* 03:00 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php initSiteStats --wiki=aniphobiawiki --update (END - exit=0)
* 03:00 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php initSiteStats --wiki=aniphobiawiki --update (START)
* 03:00 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=aniphobiawiki --sleep=0 '--comment=Importing files from [https://aniphobia.fandom.com/](https://aniphobia.fandom.com/) ([T15474](https://meta.miraheze.org/wiki/phorge:T15474))' -- . (END - exit=0)
* 03:00 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=aniphobiawiki --sleep=0 '--comment=Importing files from [https://aniphobia.fandom.com/](https://aniphobia.fandom.com/) ([T15474](https://meta.miraheze.org/wiki/phorge:T15474))' -- . (START)
* 03:00 MirahezeLSBot: [skye@mwtask171] Starting import for aniphobiawiki (XML: None; Images: .) (START)
* 02:36 MirahezeLSBot: [void@cloud17] reboot phorge171

## 2026-06-02 

* 22:09 MirahezeLSBot: [skye@test151] finished deploy of {'pull': 'config', 'config': True} to test151 - SUCCESS in 1s
* 22:09 MirahezeLSBot: [skye@test151] starting deploy of {'pull': 'config', 'config': True} to test151
* 22:08 MirahezeLSBot: [skye@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 26s
* 22:08 MirahezeLSBot: [skye@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 17:20 SomeRandomDeveloper: deployed security patch for T15475
* 00:27 MirahezeLSBot: [wwr@mwtask171] fixconts --wiki scpclassifiedwiki
* 00:26 MirahezeLSBot: [wwr@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php CreateWiki:SetContainersAccess --wiki=scpclassifiedwiki (END - exit=0)

## 2026-06-01 

* 21:46 MirahezeLSBot: [void@phorge171] restart phorge_db-backup service
* 21:44 MirahezeLSBot: [void@db182] [phabricator_calendar]> UPDATE calendar_event SET editPolicy="PHID-PLCY-w6bznnja2gez3vq6ea57" WHERE name="Miraheze Creation Date (or Birthday)"; -- T13002
* 21:36 MirahezeLSBot: [void@phorge171] ./bin/remove destroy F4051737 -- old unused upload
* 21:32 MirahezeLSBot: [void@phorge171] ./bin/remove destroy F4059763 -- old unused upload
* 21:31 MirahezeLSBot: [void@phorge171] ./bin/remove destroy F2122720 -- old unused upload
* 21:30 MirahezeLSBot: [void@phorge171] ./bin/remove destroy F4059762 -- old unfinished upload
* 21:29 MirahezeLSBot: [void@phorge171] ./bin/remove destroy F4059761 -- old unfinished upload
* 21:22 MirahezeLSBot: [void@phorge171] ./bin/remove destroy F1423152 -- old incomplete upload
* 21:16 MirahezeLSBot: [void@phorge171] ./bin/remove destroy F5468524 -- XML for completed import T14843
* 20:55 MirahezeLSBot: [void@phorge171] ./bin/remove destroy F6715656 -- 44GB dump, accessible in other ways, probably done being processed too
* 20:35 MirahezeLSBot: [void@phorge171] ./bin/remove destroy PHID-FILE-k2tylsmhfn6x3kliwqzp -- 65GB dump, not used for anything
* 20:06 MirahezeLSBot: [wwr@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php CirrusSearch:ForceSearchIndex --wiki=reconvergentfateswiki (END - exit=0)
* 20:05 MirahezeLSBot: [wwr@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php CirrusSearch:UpdateSearchIndexConfig --wiki=reconvergentfateswiki --startOver (END - exit=0)
* 20:04 MirahezeLSBot: [wwr@mwtask171] curl -X DELETE [https://opensearch-mw.wikitide.net/reconvergentfateswiki_content](https://opensearch-mw.wikitide.net/reconvergentfateswiki_content) [https://opensearch-mw.wikitide.net/reconvergentfateswiki_general](https://opensearch-mw.wikitide.net/reconvergentfateswiki_general)
* 20:01 MirahezeLSBot: [wwr@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php CirrusSearch:UpdateSearchIndexConfig --wiki=reconvergentfateswiki --startOver (END - exit=256)
* 16:09 RhinosF1: destroyed F6727665
* 02:18 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject201: swift-object, swift, and python3-swift
* 02:18 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject181: swift-object, swift, and python3-swift
* 02:17 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject191: swift-object, swift, and python3-swift
* 02:17 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask181: php-symfony-string, php-symfony-console, php-symfony-filesystem, php-symfony-finder, and php-symfony-process
* 02:16 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject171: swift-object, swift, and python3-swift
* 02:15 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject161: swift-object-expirer, swift-object, swift, and python3-swift
* 02:15 MirahezeLSBot: [void@puppet181] Upgraded packages on test151: php-symfony-string, php-symfony-console, php-symfony-filesystem, php-symfony-finder, and php-symfony-process
* 02:15 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftac171: swift-account, swift-container, swift, and python3-swift
* 02:14 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftproxy161: swift-proxy, swift, and python3-swift
* 02:14 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftproxy171: swift-proxy, swift, and python3-swift
* 02:13 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject151: swift-object, swift, and python3-swift
* 02:13 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject211: swift-object, swift, and python3-swift
* 02:12 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask171: php-symfony-string, php-symfony-console, php-symfony-filesystem, php-symfony-finder, and php-symfony-process
* 02:12 MirahezeLSBot: [void@puppet181] Upgraded packages on reports171: php-symfony-string, php-symfony-console, php-symfony-filesystem, php-symfony-finder, and php-symfony-process
* 02:12 MirahezeLSBot: [void@puppet181] Upgraded packages on matomo151: php-symfony-string, php-symfony-console, php-symfony-filesystem, php-symfony-finder, and php-symfony-process
* 01:11 MirahezeLSBot: [petramagna@test151] finished deploy of {'files': '1.46/includes/Block/AbstractBlock.php'} to test151 - SUCCESS in 0s
* 01:11 MirahezeLSBot: [petramagna@test151] starting deploy of {'files': '1.46/includes/Block/AbstractBlock.php'} to test151
* 01:10 MirahezeLSBot: [petramagna@test151] DEPLOY ABORTED: Non-Zero Exit Code in prep, see output.
* 01:10 MirahezeLSBot: [petramagna@test151] starting deploy of {'world': True, 'versions': '1.46'} to test151
* 00:00 MirahezeLSBot: [www-data@mwtask181] Began automatic backing up

----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:Server_admin_log/2026-06)**