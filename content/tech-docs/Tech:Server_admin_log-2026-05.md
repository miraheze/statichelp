---
title: Tech:Server admin log/2026-05
---

`{{ {{Server admin log/nav}} }}`

## 2026-05-31 

* 19:12 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=fantendowiki . --comment='Importing images from fantendo.fandom.com ([T15427](https://meta.miraheze.org/wiki/phorge:T15427))' --skip-dupes (START)
* 19:11 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=fantendowiki . --images-comment='Importing images from fantendo.fandom.com ([T15427](https://meta.miraheze.org/wiki/phorge:T15427))' --skip-dupes (END - exit=256)
* 19:11 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=fantendowiki . --images-comment='Importing images from fantendo.fandom.com ([T15427](https://meta.miraheze.org/wiki/phorge:T15427))' --skip-dupes (START)
* 19:10 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=fantendowiki . --source-wiki-url=' [https://fantendo.fandom.com/'](https://fantendo.fandom.com/') (END - exit=256)
* 19:10 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=fantendowiki . --source-wiki-url=' [https://fantendo.fandom.com/'](https://fantendo.fandom.com/') (START)
* 09:16 MirahezeLSBot: [petramagna@test151] finished deploy of {'folders': '1.46/extensions/GlobalBlocking'} to test151 - SUCCESS in 0s
* 09:16 MirahezeLSBot: [petramagna@test151] starting deploy of {'folders': '1.46/extensions/GlobalBlocking'} to test151
* 09:14 MirahezeLSBot: [petramagna@test151] finished deploy of {'folders': '1.46/extensions/GlobalBlocking'} to test151 - SUCCESS in 0s
* 09:14 MirahezeLSBot: [petramagna@test151] starting deploy of {'folders': '1.46/extensions/GlobalBlocking'} to test151
* 09:13 MirahezeLSBot: [petramagna@test151] starting deploy of {'folders': '1.46/extensions/GlobalBlock'} to test151
* 06:45 MirahezeLSBot: [petramagna@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 21s
* 06:44 MirahezeLSBot: [petramagna@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 06:40 MirahezeLSBot: [petramagna@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 25s
* 06:39 MirahezeLSBot: [petramagna@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all

## 2026-05-30 

* 00:47 MirahezeLSBot: [skye@test151] finished deploy of {'versions': ['1.45', '1.46'], 'upgrade_extensions': 'ThemeToggle'} to test151 - SUCCESS in 1s
* 00:47 MirahezeLSBot: [skye@test151] starting deploy of {'versions': ['1.45', '1.46'], 'upgrade_extensions': 'ThemeToggle'} to test151
* 00:45 MirahezeLSBot: [skye@mwtask181] finished deploy of {'versions': '1.45', 'upgrade_extensions': 'ThemeToggle'} to all - SUCCESS in 26s
* 00:45 MirahezeLSBot: [skye@mwtask181] starting deploy of {'versions': '1.45', 'upgrade_extensions': 'ThemeToggle'} to all
* 00:44 MirahezeLSBot: [skye@mwtask181] DEPLOY ABORTED: Non-Zero Exit Code in prep, see output.
* 00:44 MirahezeLSBot: [skye@mwtask181] starting deploy of {'versions': '1.45', 'upgrade_extensions': 'ThemeToggle'} to all
* 00:43 MirahezeLSBot: [skye@mwtask181] finished deploy of {'versions': '1.45', 'upgrade_extensions': 'ThemeToggle'} to all - SUCCESS in 0s
* 00:43 MirahezeLSBot: [skye@mwtask181] starting deploy of {'versions': '1.45', 'upgrade_extensions': 'ThemeToggle'} to all
* 00:43 Skye: mwtask181: sudo -u www-data rm -rf /srv/mediawiki-staging/1.45/extensions/ThemeToggle
* 00:42 Skye: test151: sudo -u www-data rm -rf /srv/mediawiki-staging/{1.45,1.46}/extensions/ThemeToggle

## 2026-05-29 

* 23:34 MirahezeLSBot: [skye@mwtask171] Finished import for tinyplanetswiki (XML: None; Images: .) (END - exit=0)
* 23:34 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php initSiteStats --wiki=tinyplanetswiki --update (END - exit=0)
* 23:34 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php initSiteStats --wiki=tinyplanetswiki --update (START)
* 23:34 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=tinyplanetswiki --sleep=0 '--comment=Importing images from [https://tinyplanets.fandom.com](https://tinyplanets.fandom.com) ([T15451](https://meta.miraheze.org/wiki/phorge:T15451))' -- . (END - exit=0)
* 23:32 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=tinyplanetswiki --sleep=0 '--comment=Importing images from [https://tinyplanets.fandom.com](https://tinyplanets.fandom.com) ([T15451](https://meta.miraheze.org/wiki/phorge:T15451))' -- . (START)
* 23:32 MirahezeLSBot: [skye@mwtask171] Starting import for tinyplanetswiki (XML: None; Images: .) (START)
* 23:17 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php CreateWiki:SetContainersAccess --wiki=ovalpediawiki (END - exit=0)
* 23:17 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RenameDatabase --wiki=loginwiki --rename --old=ovalhistorywiki --new=ovalpediawiki --user=Skye (END - exit=0)
* 23:13 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php CreateWiki:SetContainersAccess --wiki=voxeliawiki (END - exit=0)
* 23:12 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RenameDatabase --wiki=loginwiki --rename --old=volexiawiki --new=voxeliawiki --user=Skye (END - exit=0)
* 23:10 Skye: DROP DATABASE*
* 23:09 Skye: c4: DROP voxeliawiki;
* 22:56 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RenameDatabase --wiki=loginwiki --rename --old=volexiawiki --new=voxeliawiki --user=Skye (END - exit=256)
* 22:55 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php CreateWiki:SetContainersAccess --wiki=ukgbwiki (END - exit=0)
* 22:47 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RenameDatabase --wiki=loginwiki --rename --old=ukgbdiscordwiki --new=ukgbwiki --user=Skye (END - exit=0)
* 22:44 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php CreateWiki:SetContainersAccess --wiki=unofficialvoxeliawiki (END - exit=0)
* 22:43 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RenameDatabase --wiki=loginwiki --rename --old=voxeliawiki --new=unofficialvoxeliawiki --user=Skye (END - exit=0)
* 21:16 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:ResetWiki --wiki=loginwiki --dbname=scpclassifiedwiki --requester=KenLumni (END - exit=0)
* 21:13 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php initSiteStats --wiki=weltenzyklopadiewiki --update (END - exit=0)
* 21:12 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php initSiteStats --wiki=weltenzyklopadiewiki (END - exit=0)

## 2026-05-28 

* 19:49 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject201: linux-libc-dev
* 19:49 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject191: linux-libc-dev
* 19:49 MirahezeLSBot: [void@puppet181] Upgraded packages on test151: linux-libc-dev
* 19:48 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftproxy171: linux-libc-dev
* 19:48 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftproxy161: linux-libc-dev
* 19:48 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject211: linux-libc-dev
* 19:48 MirahezeLSBot: [void@puppet181] Upgraded packages on ns2: linux-libc-dev
* 19:47 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject171: linux-libc-dev
* 19:47 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject161: linux-libc-dev
* 19:47 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject181: linux-libc-dev
* 19:46 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftac171: linux-libc-dev
* 19:46 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject151: linux-libc-dev
* 19:46 MirahezeLSBot: [void@puppet181] Upgraded packages on os202: linux-libc-dev
* 19:46 MirahezeLSBot: [void@puppet181] Upgraded packages on os191: linux-libc-dev
* 19:45 MirahezeLSBot: [void@puppet181] Upgraded packages on os201: linux-libc-dev
* 19:45 MirahezeLSBot: [void@puppet181] Upgraded packages on rdb191: linux-libc-dev
* 19:45 MirahezeLSBot: [void@puppet181] Upgraded packages on os162: linux-libc-dev
* 19:44 MirahezeLSBot: [void@puppet181] Upgraded packages on puppet181: linux-libc-dev
* 19:44 MirahezeLSBot: [void@puppet181] Upgraded packages on phorge171: linux-libc-dev
* 19:44 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask181: linux-libc-dev
* 19:44 MirahezeLSBot: [void@puppet181] Upgraded packages on reports171: linux-libc-dev
* 19:43 MirahezeLSBot: [void@puppet181] Upgraded packages on os161: linux-libc-dev
* 19:43 MirahezeLSBot: [void@puppet181] Upgraded packages on prometheus151: linux-libc-dev
* 19:43 MirahezeLSBot: [void@puppet181] Upgraded packages on ns1: linux-libc-dev
* 19:43 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask171: linux-libc-dev
* 19:42 MirahezeLSBot: [void@puppet181] Upgraded packages on os151: linux-libc-dev
* 19:42 MirahezeLSBot: [void@puppet181] Upgraded packages on mw203: linux-libc-dev
* 19:42 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask151: linux-libc-dev
* 19:41 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask161: linux-libc-dev
* 19:41 MirahezeLSBot: [void@puppet181] Upgraded packages on mw202: linux-libc-dev
* 19:41 MirahezeLSBot: [void@puppet181] Upgraded packages on mw201: linux-libc-dev
* 19:40 MirahezeLSBot: [void@puppet181] Upgraded packages on mw193: linux-libc-dev
* 19:40 MirahezeLSBot: [void@puppet181] Upgraded packages on mw192: linux-libc-dev
* 19:40 MirahezeLSBot: [void@puppet181] Upgraded packages on mw183: linux-libc-dev
* 19:39 MirahezeLSBot: [void@puppet181] Upgraded packages on mw181: linux-libc-dev
* 19:39 MirahezeLSBot: [void@puppet181] Upgraded packages on mw182: linux-libc-dev
* 19:39 MirahezeLSBot: [void@puppet181] Upgraded packages on mw171: linux-libc-dev
* 19:38 MirahezeLSBot: [void@puppet181] Upgraded packages on mw191: linux-libc-dev
* 19:38 MirahezeLSBot: [void@puppet181] Upgraded packages on mw161: linux-libc-dev
* 19:38 MirahezeLSBot: [void@puppet181] Upgraded packages on mw163: linux-libc-dev
* 19:38 MirahezeLSBot: [void@puppet181] Upgraded packages on mw173: linux-libc-dev
* 19:37 MirahezeLSBot: [void@puppet181] Upgraded packages on mw172: linux-libc-dev
* 19:37 MirahezeLSBot: [void@puppet181] Upgraded packages on mw162: linux-libc-dev
* 19:37 MirahezeLSBot: [void@puppet181] Upgraded packages on mw153: linux-libc-dev
* 19:36 MirahezeLSBot: [void@puppet181] Upgraded packages on mw152: linux-libc-dev
* 19:36 MirahezeLSBot: [void@puppet181] Upgraded packages on mon181: linux-libc-dev
* 19:36 MirahezeLSBot: [void@puppet181] Upgraded packages on mem191: linux-libc-dev
* 19:36 MirahezeLSBot: [void@puppet181] Upgraded packages on mw151: linux-libc-dev
* 19:35 MirahezeLSBot: [void@puppet181] Upgraded packages on llm191: linux-libc-dev
* 19:35 MirahezeLSBot: [void@puppet181] Upgraded packages on mem201: linux-libc-dev
* 19:35 MirahezeLSBot: [void@puppet181] Upgraded packages on mem161: linux-libc-dev
* 19:35 MirahezeLSBot: [void@puppet181] Upgraded packages on mem151: linux-libc-dev
* 19:34 MirahezeLSBot: [void@puppet181] Upgraded packages on matomo151: linux-libc-dev
* 19:34 MirahezeLSBot: [void@puppet181] Upgraded packages on kafka182: linux-libc-dev
* 19:34 MirahezeLSBot: [void@puppet181] Upgraded packages on ldap171: linux-libc-dev
* 19:34 MirahezeLSBot: [void@puppet181] Upgraded packages on mattermost2: linux-libc-dev
* 19:33 MirahezeLSBot: [void@puppet181] Upgraded packages on db201: linux-libc-dev
* 19:33 MirahezeLSBot: [void@puppet181] Upgraded packages on cp201: linux-libc-dev
* 19:33 MirahezeLSBot: [void@puppet181] Upgraded packages on eventgate182: linux-libc-dev
* 19:33 MirahezeLSBot: [void@puppet181] Upgraded packages on db192: linux-libc-dev
* 19:32 MirahezeLSBot: [void@puppet181] Upgraded packages on db181: linux-libc-dev
* 19:32 MirahezeLSBot: [void@puppet181] Upgraded packages on cp171: linux-libc-dev
* 19:32 MirahezeLSBot: [void@puppet181] Upgraded packages on graylog161: linux-libc-dev
* 19:31 MirahezeLSBot: [void@puppet181] Upgraded packages on db182: linux-libc-dev
* 19:31 MirahezeLSBot: [void@puppet181] Upgraded packages on bast181: linux-libc-dev
* 19:31 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud17: linux-libc-dev, libcpupower1, and linux-cpupower
* 19:30 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud20: linux-libc-dev, libcpupower1, and linux-cpupower
* 19:30 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud18: linux-libc-dev, libcpupower1, and linux-cpupower
* 19:30 MirahezeLSBot: [void@puppet181] Upgraded packages on cp191: linux-libc-dev
* 19:30 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud16: linux-libc-dev, libcpupower1, and linux-cpupower
* 19:29 MirahezeLSBot: [void@puppet181] Upgraded packages on changeprop202: linux-libc-dev
* 19:29 MirahezeLSBot: [void@puppet181] Upgraded packages on db151: linux-libc-dev
* 19:29 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud19: linux-libc-dev, libcpupower1, and linux-cpupower
* 19:28 MirahezeLSBot: [void@puppet181] Upgraded packages on db172: linux-libc-dev
* 19:28 MirahezeLSBot: [void@puppet181] Upgraded packages on db171: linux-libc-dev
* 19:28 MirahezeLSBot: [void@puppet181] Upgraded packages on db161: linux-libc-dev
* 19:28 MirahezeLSBot: [void@puppet181] Upgraded packages on cp161: linux-libc-dev
* 19:27 MirahezeLSBot: [void@puppet181] Upgraded packages on bots171: linux-libc-dev
* 19:27 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud15: linux-libc-dev, libcpupower1, and linux-cpupower
* 19:27 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud21: linux-libc-dev, libcpupower1, and linux-cpupower
* 19:27 MirahezeLSBot: [void@puppet181] Upgraded packages on bast161: linux-libc-dev
* 05:27 MirahezeLSBot: [void@db171] systemctl reset-failed sql-backup && systemctl restart sql-backup

## 2026-05-27 

* 23:35 Void: ban an IP in cloudflare for odd behavior related to static
* 22:59 MirahezeLSBot: [void@puppet181] Upgraded packages on cp171: libvarnishapi3 and varnish
* 22:58 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud17: libunbound8
* 22:58 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud15: libunbound8
* 22:58 MirahezeLSBot: [void@puppet181] Upgraded packages on cp191: libvarnishapi3 and varnish
* 22:58 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud21: libunbound8
* 22:57 MirahezeLSBot: [void@puppet181] Upgraded packages on cp161: libvarnishapi3 and varnish
* 22:41 MirahezeLSBot: [void@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 25s
* 22:41 MirahezeLSBot: [void@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 22:09 MirahezeLSBot: [void@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 22:09 MirahezeLSBot: [void@test151] starting deploy of {'config': True} to test151
* 22:06 MirahezeLSBot: [void@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 22:06 MirahezeLSBot: [void@test151] starting deploy of {'config': True} to test151
* 22:04 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php refreshLinks --wiki=fantendowiki (END - exit=33280)
* 22:03 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php refreshLinks --wiki=fantendowiki (START)
* 21:48 MirahezeLSBot: [skye@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 25s
* 21:48 MirahezeLSBot: [skye@test151] finished deploy of {'pull': 'config', 'config': True} to test151 - SUCCESS in 1s
* 21:48 MirahezeLSBot: [skye@test151] starting deploy of {'pull': 'config', 'config': True} to test151
* 21:47 MirahezeLSBot: [skye@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 21:13 MirahezeLSBot: [void@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 21:13 MirahezeLSBot: [void@test151] starting deploy of {'config': True} to test151
* 20:46 MirahezeLSBot: [void@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 20:46 MirahezeLSBot: [void@test151] starting deploy of {'config': True} to test151
* 19:10 MirahezeLSBot: [void@db171] systemctl reset-failed sql-backup && systemctl restart sql-backup
* 11:06 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php rebuildall --wiki=fantendowiki (START)
* 11:06 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importDump --wiki=fantendowiki --no-updates --username-prefix=fandom:fantendo -- fantendo_pages_full.xml (END - exit=0)
* 03:06 Skye: [skye@mwtask171] sudo -u www-data foreachwikiindblist /home/skye/maps/maps.php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:NotifyWikiUsers --header='Maps extensions has been disabled' ... --group=bureaucrat --group=sysop
* 02:48 Skye: test
* 01:06 MirahezeLSBot: [skye@mwtask171] sudo -u www-data /usr/local/bin/foreachwikiindblist /tmp/maps.php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:GenerateExtensionDatabaseList metawiki --directory=~/maps (END - exit=33280)
* 01:05 MirahezeLSBot: [skye@mwtask171] sudo -u www-data /usr/local/bin/foreachwikiindblist /tmp/maps.php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:GenerateExtensionDatabaseList metawiki --directory=~/maps (START)
* 00:04 MirahezeLSBot: [somerandomdeveloper@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 24s
* 00:03 MirahezeLSBot: [somerandomdeveloper@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all

## 2026-05-26 

* 23:29 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php initEditCount --wiki=b3313wiki (END - exit=0)
* 23:22 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:AssignImportedEdits --wiki=b3313wiki --import-prefix=fandom:b3313 --from='TheGreatestRoman-old' --to=TheGreatestRoman (END - exit=0)
* 23:22 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:AssignImportedEdits --wiki=b3313wiki --import-prefix=fandom:b3313 --from='TheGreatestRomanIsTaken' --to=TheGreatestRoman (END - exit=0)
* 23:22 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:AssignImportedEdits --wiki=b3313wiki --import-prefix=fandom:b3313 --from='TheGreatestRoman111' --to=TheGreatestRoman (END - exit=0)
* 23:13 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:AssignImportedEdits --wiki=b3313wiki --import-prefix=fandom:b3313 --from=Stevoisiak (END - exit=256)
* 23:13 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:AssignImportedEdits --wiki=b3313wiki --import-prefix=fandom:b3313 --from='Soupnuts6061' --to=Somepersononthenet (END - exit=0)
* 23:12 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:AssignImportedEdits --wiki=b3313wiki --import-prefix=fandom:b3313 --from='Apollyon Pal' --to=RollyPollyPal (END - exit=0)
* 23:12 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:AssignImportedEdits --wiki=b3313wiki --import-prefix=fandom:b3313 --from=MrWorlder --to=Poxta (END - exit=0)
* 23:11 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:AssignImportedEdits --wiki=b3313wiki --import-prefix=fandom:b3313 --from='Intellectual Hindu' --to=Poxta (END - exit=0)
* 23:08 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:AssignImportedEdits --wiki=b3313wiki --import-prefix=fandom:b3313 --from=Intellectual_Hindu --to=Poxta (END - exit=256)
* 23:03 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:AssignImportedEdits --wiki=b3313wiki --import-prefix=fandom:b3313 --from=AutumnBen1 --to=Oktoberautumn (END - exit=256)
* 23:02 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:AssignImportedEdits --wiki=b3313wiki --import-prefix=fandom:b3313 --from=ComplexitySigma --to=FaintBreath (END - exit=0)
* 23:02 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:AssignImportedEdits --wiki=b3313wiki --import-prefix=fandom:b3313 --from=FaintBreath (END - exit=256)
* 23:00 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:AssignImportedEdits --wiki=b3313wiki --import-prefix=fandom:b3313 --from=Branleaf (END - exit=256)
* 22:53 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:AssignImportedEdits --wiki=b3313wiki --import-prefix=fandom:b3313 --from=Bb010g (END - exit=256)
* 21:14 MirahezeLSBot: [void@puppet181] Upgraded packages on mw203: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 21:14 MirahezeLSBot: [void@puppet181] Upgraded packages on mw202: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 21:14 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask181: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 21:13 MirahezeLSBot: [void@puppet181] Upgraded packages on mw183: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 21:13 MirahezeLSBot: [void@puppet181] Upgraded packages on mw182: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 21:12 MirahezeLSBot: [void@puppet181] Upgraded packages on mw173: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 21:12 MirahezeLSBot: [void@puppet181] Upgraded packages on mw201: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 21:12 MirahezeLSBot: [void@puppet181] Upgraded packages on mw191: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 21:11 MirahezeLSBot: [void@puppet181] Upgraded packages on mw193: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 21:11 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask171: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 21:11 MirahezeLSBot: [void@puppet181] Upgraded packages on mw163: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 21:10 MirahezeLSBot: [void@puppet181] Upgraded packages on mw192: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 21:10 MirahezeLSBot: [void@puppet181] Upgraded packages on mw181: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 21:10 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask151: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 21:09 MirahezeLSBot: [void@puppet181] Upgraded packages on test151: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 21:09 MirahezeLSBot: [void@puppet181] Upgraded packages on mw161: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 21:09 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask161: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 21:08 MirahezeLSBot: [void@puppet181] Upgraded packages on mw171: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 21:08 MirahezeLSBot: [void@puppet181] Upgraded packages on mw162: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 21:08 MirahezeLSBot: [void@puppet181] Upgraded packages on mw172: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 21:07 MirahezeLSBot: [void@puppet181] Upgraded packages on mw153: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 21:07 MirahezeLSBot: [void@puppet181] Upgraded packages on mw151: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 21:07 MirahezeLSBot: [void@puppet181] Upgraded packages on mw152: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 20:29 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject201: libtalloc2, libtevent0t64, libsmbclient0, samba-common, smbclient, libtdb1, python3-samba, samba-common-bin, python3-ldb, libldb2, samba-libs, libwbclient0, python3-tdb, python3-talloc, and tdb-tools
* 20:29 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftproxy161: libtalloc2, libtevent0t64, libsmbclient0, samba-common, smbclient, libtdb1, python3-samba, samba-common-bin, python3-ldb, libldb2, samba-libs, libwbclient0, python3-tdb, python3-talloc, and tdb-tools
* 20:28 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftproxy171: libtalloc2, libtevent0t64, libsmbclient0, samba-common, smbclient, libtdb1, python3-samba, samba-common-bin, python3-ldb, libldb2, samba-libs, libwbclient0, python3-tdb, python3-talloc, and tdb-tools
* 20:28 MirahezeLSBot: [void@puppet181] Upgraded packages on test151: libtalloc2, libtevent0t64, libsmbclient0, samba-common, smbclient, libtdb1, python3-samba, samba-common-bin, python3-ldb, libldb2, samba-libs, libwbclient0, python3-tdb, python3-talloc, and tdb-tools
* 20:28 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject211: libtalloc2, libtevent0t64, libsmbclient0, samba-common, smbclient, libtdb1, python3-samba, samba-common-bin, python3-ldb, libldb2, samba-libs, libwbclient0, python3-tdb, python3-talloc, and tdb-tools
* 20:27 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject191: libtalloc2, libtevent0t64, libsmbclient0, samba-common, smbclient, libtdb1, python3-samba, samba-common-bin, python3-ldb, libldb2, samba-libs, libwbclient0, python3-tdb, python3-talloc, and tdb-tools
* 20:27 MirahezeLSBot: [void@puppet181] Upgraded packages on ns2: libtalloc2, libtevent0t64, libsmbclient0, samba-common, smbclient, libtdb1, python3-samba, samba-common-bin, python3-ldb, libldb2, samba-libs, libwbclient0, python3-tdb, python3-talloc, and tdb-tools
* 20:26 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject181: libtalloc2, libtevent0t64, libsmbclient0, samba-common, smbclient, libtdb1, python3-samba, samba-common-bin, python3-ldb, libldb2, samba-libs, libwbclient0, python3-tdb, python3-talloc, and tdb-tools
* 20:26 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject161: libtalloc2, libtevent0t64, libsmbclient0, samba-common, smbclient, libtdb1, python3-samba, samba-common-bin, python3-ldb, libldb2, samba-libs, libwbclient0, python3-tdb, python3-talloc, and tdb-tools
* 20:26 MirahezeLSBot: [void@puppet181] Upgraded packages on os201: libtalloc2, libtevent0t64, libsmbclient0, samba-common, smbclient, libtdb1, python3-samba, samba-common-bin, python3-ldb, libldb2, samba-libs, libwbclient0, python3-tdb, python3-talloc, and tdb-tools
* 20:25 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject171: libtalloc2, libtevent0t64, libsmbclient0, samba-common, smbclient, libtdb1, python3-samba, samba-common-bin, python3-ldb, libldb2, samba-libs, libwbclient0, python3-tdb, python3-talloc, and tdb-tools
* 20:25 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftac171: libtalloc2, libtevent0t64, libsmbclient0, samba-common, smbclient, libtdb1, python3-samba, samba-common-bin, python3-ldb, libldb2, samba-libs, libwbclient0, python3-tdb, python3-talloc, and tdb-tools
* 20:24 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject151: libtalloc2, libtevent0t64, libsmbclient0, samba-common, smbclient, libtdb1, python3-samba, samba-common-bin, python3-ldb, libldb2, samba-libs, libwbclient0, python3-tdb, python3-talloc, and tdb-tools
* 20:24 MirahezeLSBot: [void@puppet181] Upgraded packages on os202: libtalloc2, libtevent0t64, libsmbclient0, samba-common, smbclient, libtdb1, python3-samba, samba-common-bin, python3-ldb, libldb2, samba-libs, libwbclient0, python3-tdb, python3-talloc, and tdb-tools
* 20:23 MirahezeLSBot: [void@puppet181] Upgraded packages on puppet181: libtalloc2, libtevent0t64, libsmbclient0, samba-common, smbclient, libtdb1, python3-samba, samba-common-bin, python3-ldb, libldb2, samba-libs, libwbclient0, python3-tdb, python3-talloc, and tdb-tools
* 20:23 MirahezeLSBot: [void@puppet181] Upgraded packages on os162: libtalloc2, libtevent0t64, libsmbclient0, samba-common, smbclient, libtdb1, python3-samba, samba-common-bin, python3-ldb, libldb2, samba-libs, libwbclient0, python3-tdb, python3-talloc, and tdb-tools
* 20:23 MirahezeLSBot: [void@puppet181] Upgraded packages on rdb191: libtalloc2, libtevent0t64, libsmbclient0, samba-common, smbclient, libtdb1, python3-samba, samba-common-bin, python3-ldb, libldb2, samba-libs, libwbclient0, python3-tdb, python3-talloc, and tdb-tools
* 20:22 MirahezeLSBot: [void@puppet181] Upgraded packages on reports171: libtalloc2, libtevent0t64, libsmbclient0, samba-common, smbclient, libtdb1, python3-samba, samba-common-bin, python3-ldb, libldb2, samba-libs, libwbclient0, python3-tdb, python3-talloc, and tdb-tools
* 20:22 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask181: libtalloc2, libtevent0t64, libsmbclient0, samba-common, smbclient, libtdb1, python3-samba, samba-common-bin, python3-ldb, libldb2, samba-libs, libwbclient0, python3-tdb, python3-talloc, and tdb-tools
* 20:21 MirahezeLSBot: [void@puppet181] Upgraded packages on prometheus151: libtalloc2, libtevent0t64, libsmbclient0, samba-common, smbclient, libtdb1, python3-samba, samba-common-bin, python3-ldb, libldb2, samba-libs, libwbclient0, python3-tdb, python3-talloc, and tdb-tools
* 20:21 MirahezeLSBot: [void@puppet181] Upgraded packages on os191: libtalloc2, libtevent0t64, libsmbclient0, samba-common, smbclient, libtdb1, python3-samba, samba-common-bin, python3-ldb, libldb2, samba-libs, libwbclient0, python3-tdb, python3-talloc, and tdb-tools
* 20:21 MirahezeLSBot: [void@puppet181] Upgraded packages on phorge171: libtalloc2, libtevent0t64, libsmbclient0, samba-common, smbclient, libtdb1, python3-samba, samba-common-bin, python3-ldb, libldb2, samba-libs, libwbclient0, python3-tdb, python3-talloc, and tdb-tools
* 20:20 MirahezeLSBot: [void@puppet181] Upgraded packages on os151: libtalloc2, libtevent0t64, libsmbclient0, samba-common, smbclient, libtdb1, python3-samba, samba-common-bin, python3-ldb, libldb2, samba-libs, libwbclient0, python3-tdb, python3-talloc, and tdb-tools
* 20:20 MirahezeLSBot: [void@puppet181] Upgraded packages on os161: libtalloc2, libtevent0t64, libsmbclient0, samba-common, smbclient, libtdb1, python3-samba, samba-common-bin, python3-ldb, libldb2, samba-libs, libwbclient0, python3-tdb, python3-talloc, and tdb-tools
* 20:20 MirahezeLSBot: [void@puppet181] Upgraded packages on ns1: libtalloc2, libtevent0t64, libsmbclient0, samba-common, smbclient, libtdb1, python3-samba, samba-common-bin, python3-ldb, libldb2, samba-libs, libwbclient0, python3-tdb, python3-talloc, and tdb-tools
* 20:19 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask151: libtalloc2, libtevent0t64, libsmbclient0, samba-common, smbclient, libtdb1, python3-samba, samba-common-bin, python3-ldb, libldb2, samba-libs, libwbclient0, python3-tdb, python3-talloc, and tdb-tools
* 20:19 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask171: libtalloc2, libtevent0t64, libsmbclient0, samba-common, smbclient, libtdb1, python3-samba, samba-common-bin, python3-ldb, libldb2, samba-libs, libwbclient0, python3-tdb, python3-talloc, and tdb-tools
* 20:18 MirahezeLSBot: [void@puppet181] Upgraded packages on mw203: libtalloc2, libtevent0t64, libsmbclient0, samba-common, smbclient, libtdb1, python3-samba, samba-common-bin, python3-ldb, libldb2, samba-libs, libwbclient0, python3-tdb, python3-talloc, and tdb-tools
* 20:18 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask161: libtalloc2, libtevent0t64, libsmbclient0, samba-common, smbclient, libtdb1, python3-samba, samba-common-bin, python3-ldb, libldb2, samba-libs, libwbclient0, python3-tdb, python3-talloc, and tdb-tools
* 20:17 MirahezeLSBot: [void@puppet181] Upgraded packages on mw202: libtalloc2, libtevent0t64, libsmbclient0, samba-common, smbclient, libtdb1, python3-samba, samba-common-bin, python3-ldb, libldb2, samba-libs, libwbclient0, python3-tdb, python3-talloc, and tdb-tools
* 20:17 MirahezeLSBot: [void@puppet181] Upgraded packages on mw201: libtalloc2, libtevent0t64, libsmbclient0, samba-common, smbclient, libtdb1, python3-samba, samba-common-bin, python3-ldb, libldb2, samba-libs, libwbclient0, python3-tdb, python3-talloc, and tdb-tools
* 20:17 MirahezeLSBot: [void@puppet181] Upgraded packages on mw193: libtalloc2, libtevent0t64, libsmbclient0, samba-common, smbclient, libtdb1, python3-samba, samba-common-bin, python3-ldb, libldb2, samba-libs, libwbclient0, python3-tdb, python3-talloc, and tdb-tools
* 20:16 MirahezeLSBot: [void@puppet181] Upgraded packages on mw191: libtalloc2, libtevent0t64, libsmbclient0, samba-common, smbclient, libtdb1, python3-samba, samba-common-bin, python3-ldb, libldb2, samba-libs, libwbclient0, python3-tdb, python3-talloc, and tdb-tools
* 20:16 MirahezeLSBot: [void@puppet181] Upgraded packages on mw192: libtalloc2, libtevent0t64, libsmbclient0, samba-common, smbclient, libtdb1, python3-samba, samba-common-bin, python3-ldb, libldb2, samba-libs, libwbclient0, python3-tdb, python3-talloc, and tdb-tools
* 20:15 MirahezeLSBot: [void@puppet181] Upgraded packages on mw183: libtalloc2, libtevent0t64, libsmbclient0, samba-common, smbclient, libtdb1, python3-samba, samba-common-bin, python3-ldb, libldb2, samba-libs, libwbclient0, python3-tdb, python3-talloc, and tdb-tools
* 20:15 MirahezeLSBot: [void@puppet181] Upgraded packages on mw182: libtalloc2, libtevent0t64, libsmbclient0, samba-common, smbclient, libtdb1, python3-samba, samba-common-bin, python3-ldb, libldb2, samba-libs, libwbclient0, python3-tdb, python3-talloc, and tdb-tools
* 20:14 MirahezeLSBot: [void@puppet181] Upgraded packages on mw181: libtalloc2, libtevent0t64, libsmbclient0, samba-common, smbclient, libtdb1, python3-samba, samba-common-bin, python3-ldb, libldb2, samba-libs, libwbclient0, python3-tdb, python3-talloc, and tdb-tools
* 20:14 MirahezeLSBot: [void@puppet181] Upgraded packages on mw173: libtalloc2, libtevent0t64, libsmbclient0, samba-common, smbclient, libtdb1, python3-samba, samba-common-bin, python3-ldb, libldb2, samba-libs, libwbclient0, python3-tdb, python3-talloc, and tdb-tools
* 20:13 MirahezeLSBot: [void@puppet181] Upgraded packages on mw163: libtalloc2, libtevent0t64, libsmbclient0, samba-common, smbclient, libtdb1, python3-samba, samba-common-bin, python3-ldb, libldb2, samba-libs, libwbclient0, python3-tdb, python3-talloc, and tdb-tools
* 20:13 MirahezeLSBot: [void@puppet181] Upgraded packages on mw171: libtalloc2, libtevent0t64, libsmbclient0, samba-common, smbclient, libtdb1, python3-samba, samba-common-bin, python3-ldb, libldb2, samba-libs, libwbclient0, python3-tdb, python3-talloc, and tdb-tools
* 20:12 MirahezeLSBot: [void@puppet181] Upgraded packages on mw162: libtalloc2, libtevent0t64, libsmbclient0, samba-common, smbclient, libtdb1, python3-samba, samba-common-bin, python3-ldb, libldb2, samba-libs, libwbclient0, python3-tdb, python3-talloc, and tdb-tools
* 20:12 MirahezeLSBot: [void@puppet181] Upgraded packages on mw153: libtalloc2, libtevent0t64, libsmbclient0, samba-common, smbclient, libtdb1, python3-samba, samba-common-bin, python3-ldb, libldb2, samba-libs, libwbclient0, python3-tdb, python3-talloc, and tdb-tools
* 20:11 MirahezeLSBot: [void@puppet181] Upgraded packages on mw172: libtalloc2, libtevent0t64, libsmbclient0, samba-common, smbclient, libtdb1, python3-samba, samba-common-bin, python3-ldb, libldb2, samba-libs, libwbclient0, python3-tdb, python3-talloc, and tdb-tools
* 20:11 MirahezeLSBot: [void@puppet181] Upgraded packages on mw161: libtalloc2, libtevent0t64, libsmbclient0, samba-common, smbclient, libtdb1, python3-samba, samba-common-bin, python3-ldb, libldb2, samba-libs, libwbclient0, python3-tdb, python3-talloc, and tdb-tools
* 20:11 MirahezeLSBot: [void@puppet181] Upgraded packages on mw151: libtalloc2, libtevent0t64, libsmbclient0, samba-common, smbclient, libtdb1, python3-samba, samba-common-bin, python3-ldb, libldb2, samba-libs, libwbclient0, python3-tdb, python3-talloc, and tdb-tools
* 20:10 MirahezeLSBot: [void@puppet181] Upgraded packages on mw152: libtalloc2, libtevent0t64, libsmbclient0, samba-common, smbclient, libtdb1, python3-samba, samba-common-bin, python3-ldb, libldb2, samba-libs, libwbclient0, python3-tdb, python3-talloc, and tdb-tools
* 20:10 MirahezeLSBot: [void@puppet181] Upgraded packages on mon181: libtalloc2, libtevent0t64, libsmbclient0, samba-common, smbclient, libtdb1, python3-samba, samba-common-bin, python3-ldb, libldb2, samba-libs, libwbclient0, python3-tdb, python3-talloc, and tdb-tools
* 20:09 MirahezeLSBot: [void@puppet181] Upgraded packages on mem191: libtalloc2, libtevent0t64, libsmbclient0, samba-common, smbclient, libtdb1, python3-samba, samba-common-bin, python3-ldb, libldb2, samba-libs, libwbclient0, python3-tdb, python3-talloc, and tdb-tools
* 20:09 MirahezeLSBot: [void@puppet181] Upgraded packages on llm191: libtalloc2, libtevent0t64, libsmbclient0, samba-common, smbclient, libtdb1, python3-samba, samba-common-bin, python3-ldb, libldb2, samba-libs, libwbclient0, python3-tdb, python3-talloc, and tdb-tools
* 20:08 MirahezeLSBot: [void@puppet181] Upgraded packages on ldap171: libtalloc2, libtevent0t64, libsmbclient0, samba-common, smbclient, libtdb1, python3-samba, samba-common-bin, python3-ldb, libldb2, samba-libs, libwbclient0, python3-tdb, python3-talloc, and tdb-tools
* 20:08 MirahezeLSBot: [void@puppet181] Upgraded packages on mem201: libtalloc2, libtevent0t64, libsmbclient0, samba-common, smbclient, libtdb1, python3-samba, samba-common-bin, python3-ldb, libldb2, samba-libs, libwbclient0, python3-tdb, python3-talloc, and tdb-tools
* 20:08 MirahezeLSBot: [void@puppet181] Upgraded packages on mem151: libtalloc2, libtevent0t64, libsmbclient0, samba-common, smbclient, libtdb1, python3-samba, samba-common-bin, python3-ldb, libldb2, samba-libs, libwbclient0, python3-tdb, python3-talloc, and tdb-tools
* 20:07 MirahezeLSBot: [void@puppet181] Upgraded packages on mem161: libtalloc2, libtevent0t64, libsmbclient0, samba-common, smbclient, libtdb1, python3-samba, samba-common-bin, python3-ldb, libldb2, samba-libs, libwbclient0, python3-tdb, python3-talloc, and tdb-tools
* 20:07 MirahezeLSBot: [void@puppet181] Upgraded packages on matomo151: libtalloc2, libtevent0t64, libsmbclient0, samba-common, smbclient, libtdb1, python3-samba, samba-common-bin, python3-ldb, libldb2, samba-libs, libwbclient0, python3-tdb, python3-talloc, and tdb-tools
* 20:06 MirahezeLSBot: [void@puppet181] Upgraded packages on kafka182: libtalloc2, libtevent0t64, libsmbclient0, samba-common, smbclient, libtdb1, python3-samba, samba-common-bin, python3-ldb, libldb2, samba-libs, libwbclient0, python3-tdb, python3-talloc, and tdb-tools
* 20:06 MirahezeLSBot: [void@puppet181] Upgraded packages on mattermost2: libtalloc2, libtevent0t64, libsmbclient0, samba-common, smbclient, libtdb1, python3-samba, samba-common-bin, python3-ldb, libldb2, samba-libs, libwbclient0, python3-tdb, python3-talloc, and tdb-tools
* 20:06 MirahezeLSBot: [void@puppet181] Upgraded packages on eventgate182: libtalloc2, libtevent0t64, libsmbclient0, samba-common, smbclient, libtdb1, python3-samba, samba-common-bin, python3-ldb, libldb2, samba-libs, libwbclient0, python3-tdb, python3-talloc, and tdb-tools
* 20:05 MirahezeLSBot: [void@puppet181] Upgraded packages on db181: libtalloc2, libtevent0t64, libsmbclient0, samba-common, smbclient, libtdb1, python3-samba, samba-common-bin, python3-ldb, libldb2, samba-libs, libwbclient0, python3-tdb, python3-talloc, and tdb-tools
* 20:05 MirahezeLSBot: [void@puppet181] Upgraded packages on db192: libtalloc2, libtevent0t64, libsmbclient0, samba-common, smbclient, libtdb1, python3-samba, samba-common-bin, python3-ldb, libldb2, samba-libs, libwbclient0, python3-tdb, python3-talloc, and tdb-tools
* 20:04 MirahezeLSBot: [void@puppet181] Upgraded packages on graylog161: libtalloc2, libtevent0t64, libsmbclient0, samba-common, smbclient, libtdb1, python3-samba, samba-common-bin, python3-ldb, libldb2, samba-libs, libwbclient0, python3-tdb, python3-talloc, and tdb-tools
* 20:04 MirahezeLSBot: [void@puppet181] Upgraded packages on db201: libtalloc2, libtevent0t64, libsmbclient0, samba-common, smbclient, libtdb1, python3-samba, samba-common-bin, python3-ldb, libldb2, samba-libs, libwbclient0, python3-tdb, python3-talloc, and tdb-tools
* 20:04 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud20: libtalloc2, libtevent0t64, libsmbclient0, samba-common, smbclient, libtdb1, libldb2, samba-libs, and libwbclient0
* 20:03 MirahezeLSBot: [void@puppet181] Upgraded packages on cp201: libtalloc2, libtevent0t64, libsmbclient0, samba-common, smbclient, libtdb1, python3-samba, samba-common-bin, python3-ldb, libldb2, samba-libs, libwbclient0, python3-tdb, python3-talloc, and tdb-tools
* 20:03 MirahezeLSBot: [void@puppet181] Upgraded packages on cp171: libtalloc2, libtevent0t64, libsmbclient0, samba-common, smbclient, libtdb1, python3-samba, samba-common-bin, python3-ldb, libldb2, samba-libs, libwbclient0, python3-tdb, python3-talloc, and tdb-tools
* 20:02 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud19: libtalloc2, libtevent0t64, libsmbclient0, samba-common, smbclient, libtdb1, libldb2, samba-libs, and libwbclient0
* 20:02 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud15: libtalloc2, libtevent0t64, libsmbclient0, samba-common, smbclient, libtdb1, libldb2, samba-libs, and libwbclient0
* 20:02 MirahezeLSBot: [void@puppet181] Upgraded packages on bast181: libtalloc2, libtevent0t64, libsmbclient0, samba-common, smbclient, libtdb1, python3-samba, samba-common-bin, python3-ldb, libldb2, samba-libs, libwbclient0, python3-tdb, python3-talloc, and tdb-tools
* 20:01 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud18: libtalloc2, libtevent0t64, libsmbclient0, samba-common, smbclient, libtdb1, libldb2, samba-libs, and libwbclient0
* 20:01 MirahezeLSBot: [void@puppet181] Upgraded packages on db182: libtalloc2, libtevent0t64, libsmbclient0, samba-common, smbclient, libtdb1, python3-samba, samba-common-bin, python3-ldb, libldb2, samba-libs, libwbclient0, python3-tdb, python3-talloc, and tdb-tools
* 20:01 MirahezeLSBot: [void@puppet181] Upgraded packages on db171: libtalloc2, libtevent0t64, libsmbclient0, samba-common, smbclient, libtdb1, python3-samba, samba-common-bin, python3-ldb, libldb2, samba-libs, libwbclient0, python3-tdb, python3-talloc, and tdb-tools
* 20:00 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud16: libtalloc2, libtevent0t64, libsmbclient0, samba-common, smbclient, libtdb1, libldb2, samba-libs, and libwbclient0
* 20:00 MirahezeLSBot: [void@puppet181] Upgraded packages on db161: libtalloc2, libtevent0t64, libsmbclient0, samba-common, smbclient, libtdb1, python3-samba, samba-common-bin, python3-ldb, libldb2, samba-libs, libwbclient0, python3-tdb, python3-talloc, and tdb-tools
* 20:00 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud17: libtalloc2, libtevent0t64, libsmbclient0, samba-common, smbclient, libtdb1, libldb2, samba-libs, and libwbclient0
* 19:59 MirahezeLSBot: [void@puppet181] Upgraded packages on cp161: libtalloc2, libtevent0t64, libsmbclient0, samba-common, smbclient, libtdb1, python3-samba, samba-common-bin, python3-ldb, libldb2, samba-libs, libwbclient0, python3-tdb, python3-talloc, and tdb-tools
* 19:59 MirahezeLSBot: [void@puppet181] Upgraded packages on db151: libtalloc2, libtevent0t64, libsmbclient0, samba-common, smbclient, libtdb1, python3-samba, samba-common-bin, python3-ldb, libldb2, samba-libs, libwbclient0, python3-tdb, python3-talloc, and tdb-tools
* 19:59 MirahezeLSBot: [void@puppet181] Upgraded packages on db172: libtalloc2, libtevent0t64, libsmbclient0, samba-common, smbclient, libtdb1, python3-samba, samba-common-bin, python3-ldb, libldb2, samba-libs, libwbclient0, python3-tdb, python3-talloc, and tdb-tools
* 19:58 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud21: libtalloc2, libtevent0t64, libsmbclient0, samba-common, smbclient, libtdb1, libldb2, samba-libs, and libwbclient0
* 19:58 MirahezeLSBot: [void@puppet181] Upgraded packages on changeprop202: libtalloc2, libtevent0t64, libsmbclient0, samba-common, smbclient, libtdb1, python3-samba, samba-common-bin, python3-ldb, libldb2, samba-libs, libwbclient0, python3-tdb, python3-talloc, and tdb-tools
* 19:58 MirahezeLSBot: [void@puppet181] Upgraded packages on bast161: libtalloc2, libtevent0t64, libsmbclient0, samba-common, smbclient, libtdb1, python3-samba, samba-common-bin, python3-ldb, libldb2, samba-libs, libwbclient0, python3-tdb, python3-talloc, and tdb-tools
* 19:57 MirahezeLSBot: [void@puppet181] Upgraded packages on bots171: libtalloc2, libtevent0t64, libsmbclient0, samba-common, smbclient, libtdb1, python3-samba, samba-common-bin, python3-ldb, libldb2, samba-libs, libwbclient0, python3-tdb, python3-talloc, and tdb-tools
* 19:57 MirahezeLSBot: [void@puppet181] Upgraded packages on cp191: libtalloc2, libtevent0t64, libsmbclient0, samba-common, smbclient, libtdb1, python3-samba, samba-common-bin, python3-ldb, libldb2, samba-libs, libwbclient0, python3-tdb, python3-talloc, and tdb-tools
* 17:21 MirahezeLSBot: [skye@mwtask171] Finished import for aniphobiawiki (XML: None; Images: .) (END - exit=0)
* 17:21 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php initSiteStats --wiki=aniphobiawiki --update (END - exit=0)
* 17:21 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php initSiteStats --wiki=aniphobiawiki --update (START)
* 17:21 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=aniphobiawiki --sleep=1 '--comment=Importing images from [https://aniphobia.fandom.com/](https://aniphobia.fandom.com/) ([T15436](https://meta.miraheze.org/wiki/phorge:T15436))' -- . (END - exit=0)
* 16:52 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importDump --wiki=fantendowiki --no-updates --username-prefix=fandom:fantendo -- fantendo_pages_full.xml (START)
* 16:52 MirahezeLSBot: [skye@mwtask171] Starting import for fantendowiki (XML: fantendo_pages_full.xml; Images: None) (START)
* 16:41 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=aniphobiawiki --sleep=1 '--comment=Importing images from [https://aniphobia.fandom.com/](https://aniphobia.fandom.com/) ([T15436](https://meta.miraheze.org/wiki/phorge:T15436))' -- . (START)
* 16:41 MirahezeLSBot: [skye@mwtask171] Starting import for aniphobiawiki (XML: None; Images: .) (START)
* 16:22 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php CreateWiki:SetContainersAccess --wiki=friendshipeternalwiki (END - exit=0)
* 16:21 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RenameDatabase --wiki=loginwiki --rename --old=kayoumylittleponyccgwiki --new=friendshipeternalwiki --user=Skye (END - exit=0)
* 16:15 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php CreateWiki:SetContainersAccess --wiki=chaoticbeingswiki (END - exit=0)
* 16:09 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RenameDatabase --wiki=loginwiki --rename --old=astralbeingswiki --new=chaoticbeingswiki --user=Skye (END - exit=0)
* 15:37 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php CreateWiki:SetContainersAccess --wiki=theblockheadswiki (END - exit=0)
* 15:37 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RenameDatabase --wiki=loginwiki --rename --old=blockheadswiki --new=theblockheadswiki --user=Skye (END - exit=0)
* 15:34 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php CreateWiki:SetContainersAccess --wiki=splatoonidyllwiki (END - exit=0)
* 15:33 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RenameDatabase --wiki=loginwiki --rename --old=projecteuphoriasquarewiki --new=splatoonidyllwiki --user=Skye (END - exit=0)
* 15:28 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php CreateWiki:SetContainersAccess --wiki=marswiki (END - exit=0)
* 15:24 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RenameDatabase --wiki=loginwiki --rename --old=ficreationwiki --new=marswiki --user=Skye (END - exit=0)
* 15:14 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php CreateWiki:SetContainersAccess --wiki=smcmwiki (END - exit=0)
* 15:12 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RenameDatabase --wiki=loginwiki --rename --old=wikimfggnexuswiki --new=smcmwiki --user=Skye (END - exit=0)
* 04:33 MirahezeLSBot: [skye@mwtask171] Finished import for doorswiki (XML: None; Images: .) (END - exit=0)
* 04:33 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php initSiteStats --wiki=doorswiki --update (END - exit=0)
* 04:33 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php initSiteStats --wiki=doorswiki --update (START)
* 04:33 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=doorswiki --sleep=1 '--comment=Importing images from [https://doors-game.fandom.com/wiki/](https://doors-game.fandom.com/wiki/) ([T15438](https://meta.miraheze.org/wiki/phorge:T15438))' -- . (END - exit=0)
* 00:49 MirahezeLSBot: [skye@mwtask171] Finished import for aniphobiawiki (XML: pages.xml; Images: None) (END - exit=0)
* 00:49 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php initSiteStats --wiki=aniphobiawiki --update (END - exit=0)
* 00:49 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php initSiteStats --wiki=aniphobiawiki --update (START)
* 00:49 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php initEditCount --wiki=aniphobiawiki (END - exit=0)
* 00:49 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php initEditCount --wiki=aniphobiawiki (START)
* 00:49 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php rebuildall --wiki=aniphobiawiki (END - exit=0)
* 00:45 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php rebuildall --wiki=aniphobiawiki (START)
* 00:45 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importDump --wiki=aniphobiawiki --no-updates --username-prefix=fandom:aniphobia -- pages.xml (END - exit=0)
* 00:34 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importDump --wiki=aniphobiawiki --no-updates --username-prefix=fandom:aniphobia -- pages.xml (START)
* 00:34 MirahezeLSBot: [skye@mwtask171] Starting import for aniphobiawiki (XML: pages.xml; Images: None) (START)
* 00:23 MirahezeLSBot: [somerandomdeveloper@db201] SET GLOBAL slave_connections_needed_for_purge = 0
* 00:22 MirahezeLSBot: [somerandomdeveloper@db181] SET GLOBAL slave_connections_needed_for_purge = 0
* 00:22 MirahezeLSBot: [somerandomdeveloper@db172] SET GLOBAL slave_connections_needed_for_purge = 0
* 00:21 MirahezeLSBot: [somerandomdeveloper@db171] SET GLOBAL slave_connections_needed_for_purge = 0
* 00:20 MirahezeLSBot: [somerandomdeveloper@db151] SET GLOBAL slave_connections_needed_for_purge = 0
* 00:17 MirahezeLSBot: [skye@mwtask171] Finished import for sxswiki (XML: history.xml; Images: None) (END - exit=0)
* 00:17 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php initSiteStats --wiki=sxswiki --update (END - exit=0)
* 00:17 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php initSiteStats --wiki=sxswiki --update (START)
* 00:17 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php initEditCount --wiki=sxswiki (END - exit=0)
* 00:17 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php initEditCount --wiki=sxswiki (START)
* 00:17 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php rebuildall --wiki=sxswiki (END - exit=0)
* 00:17 SomeRandomDeveloper: ran "SET GLOBAL slave_connections_needed_for_purge = 0;" on db192
* 00:16 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php rebuildall --wiki=sxswiki (START)
* 00:16 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importDump --wiki=sxswiki --no-updates --username-prefix=fandom:swordxstaff -- history.xml (END - exit=0)
* 00:16 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importDump --wiki=sxswiki --no-updates --username-prefix=fandom:swordxstaff -- history.xml (START)
* 00:16 MirahezeLSBot: [skye@mwtask171] Starting import for sxswiki (XML: history.xml; Images: None) (START)
* 00:10 MirahezeLSBot: [skye@mwtask171] Finished import for sxswiki (XML: None; Images: .) (END - exit=0)
* 00:10 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php initSiteStats --wiki=sxswiki --update (END - exit=0)
* 00:10 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php initSiteStats --wiki=sxswiki --update (START)
* 00:10 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=sxswiki --sleep=0 '--comment=Importing images from swordxstaff.fandom.com/wiki/SwordxStaff_Wiki ([T15434](https://meta.miraheze.org/wiki/phorge:T15434))' -- . (END - exit=0)
* 00:09 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=sxswiki --sleep=0 '--comment=Importing images from swordxstaff.fandom.com/wiki/SwordxStaff_Wiki ([T15434](https://meta.miraheze.org/wiki/phorge:T15434))' -- . (START)
* 00:09 MirahezeLSBot: [skye@mwtask171] Starting import for sxswiki (XML: None; Images: .) (START)

## 2026-05-25 

* 21:43 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=doorswiki --sleep=1 '--comment=Importing images from [https://doors-game.fandom.com/wiki/](https://doors-game.fandom.com/wiki/) ([T15438](https://meta.miraheze.org/wiki/phorge:T15438))' -- . (START)
* 21:43 MirahezeLSBot: [skye@mwtask171] Starting import for doorswiki (XML: None; Images: .) (START)
* 20:58 MirahezeLSBot: [skye@test151] finished deploy of {'versions': '1.46', 'upgrade_extensions': 'OATHAuth'} to test151 - SUCCESS in 1s
* 20:58 MirahezeLSBot: [skye@test151] starting deploy of {'versions': '1.46', 'upgrade_extensions': 'OATHAuth'} to test151
* 20:46 MirahezeLSBot: [skye@mwtask171] Finished import for doorswiki (XML: None; Images: .) (END - exit=1)
* 20:46 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=doorswiki --sleep=1 '--comment=Importing images from [https://doors-game.fandom.com/wiki/](https://doors-game.fandom.com/wiki/) ([T15438](https://meta.miraheze.org/wiki/phorge:T15438))' -- . (END - exit=1)
* 20:46 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=doorswiki --sleep=1 '--comment=Importing images from [https://doors-game.fandom.com/wiki/](https://doors-game.fandom.com/wiki/) ([T15438](https://meta.miraheze.org/wiki/phorge:T15438))' -- . (START)
* 20:46 MirahezeLSBot: [skye@mwtask171] Starting import for doorswiki (XML: None; Images: .) (START)
* 19:25 MirahezeLSBot: [skye@test151] finished deploy of {'versions': '1.46', 'upgrade_extensions': 'OATHAuth'} to test151 - SUCCESS in 1s
* 19:25 MirahezeLSBot: [skye@test151] starting deploy of {'versions': '1.46', 'upgrade_extensions': 'OATHAuth'} to test151
* 18:55 MirahezeLSBot: [somerandomdeveloper@phorge171] bin/remove destroy F6694907
* 18:15 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.46/maintenance/run.php RebuildRecentchanges --wiki=wwrtest3wikibeta (END - exit=0)
* 18:14 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.46/maintenance/run.php RebuildRecentchanges --wiki=metawikibeta (END - exit=0)
* 18:14 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.46/maintenance/run.php RebuildRecentchanges --wiki=exttestwikibeta (END - exit=0)
* 18:05 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:AssignImportedEdits --wiki=xyywiki --import-prefix=fandom:xyy --from='Kernel-chan' --to='Nueiheh tsiang' (END - exit=0)
* 18:04 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:AssignImportedEdits --wiki=xyywiki --import-prefix=imported --from='Kernel-chan' --to='Nueiheh tsiang' (END - exit=0)
* 17:39 MirahezeLSBot: [skye@mwtask171] Finished import for doorswiki (XML: doorsgame_pages_full.xml; Images: None) (END - exit=0)
* 17:39 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php initSiteStats --wiki=doorswiki --update (END - exit=0)
* 17:39 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php initSiteStats --wiki=doorswiki --update (START)
* 17:39 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php initEditCount --wiki=doorswiki (END - exit=0)
* 17:39 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php initEditCount --wiki=doorswiki (START)
* 17:39 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php rebuildall --wiki=doorswiki (END - exit=0)
* 17:34 MirahezeLSBot: [paladox@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 27s
* 17:34 MirahezeLSBot: [paladox@test151] finished deploy of {'pull': 'config', 'config': True} to test151 - SUCCESS in 1s
* 17:34 MirahezeLSBot: [paladox@test151] starting deploy of {'pull': 'config', 'config': True} to test151
* 17:34 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 16:02 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php rebuildall --wiki=doorswiki (START)
* 16:02 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importDump --wiki=doorswiki --no-updates --username-prefix=fandom:doors-game -- doorsgame_pages_full.xml (END - exit=0)
* 14:09 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importDump --wiki=doorswiki --no-updates --username-prefix=fandom:doors-game -- doorsgame_pages_full.xml (START)
* 14:08 MirahezeLSBot: [skye@mwtask171] Starting import for doorswiki (XML: doorsgame_pages_full.xml; Images: None) (START)

## 2026-05-24 

* 00:53 MirahezeLSBot: [petramagna@test151] finished deploy of {'versions': ['1.45', '1.46'], 'upgrade_extensions': 'ThemeToggle'} to test151 - SUCCESS in 1s
* 00:53 MirahezeLSBot: [petramagna@test151] starting deploy of {'versions': ['1.45', '1.46'], 'upgrade_extensions': 'ThemeToggle'} to test151

## 2026-05-23 

* 22:50 MirahezeLSBot: [void@ldap171] restart slapd to apply cert update
* 22:26 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject191: linux-libc-dev
* 22:26 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftproxy161: linux-libc-dev
* 22:26 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject201: linux-libc-dev
* 22:25 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftproxy171: linux-libc-dev
* 22:25 MirahezeLSBot: [void@puppet181] Upgraded packages on test151: linux-libc-dev
* 22:25 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject211: linux-libc-dev
* 22:25 MirahezeLSBot: [void@puppet181] Upgraded packages on ns2: linux-libc-dev
* 22:24 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject181: linux-libc-dev
* 22:24 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject171: linux-libc-dev
* 22:24 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject161: linux-libc-dev
* 22:23 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftac171: linux-libc-dev
* 22:23 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject151: linux-libc-dev
* 22:23 MirahezeLSBot: [void@puppet181] Upgraded packages on os202: linux-libc-dev
* 22:23 MirahezeLSBot: [void@puppet181] Upgraded packages on os191: linux-libc-dev
* 22:22 MirahezeLSBot: [void@puppet181] Upgraded packages on puppet181: linux-libc-dev
* 22:22 MirahezeLSBot: [void@puppet181] Upgraded packages on rdb191: linux-libc-dev
* 22:22 MirahezeLSBot: [void@puppet181] Upgraded packages on os201: linux-libc-dev
* 22:21 MirahezeLSBot: [void@puppet181] Upgraded packages on reports171: linux-libc-dev
* 22:21 MirahezeLSBot: [void@puppet181] Upgraded packages on prometheus151: linux-libc-dev
* 22:21 MirahezeLSBot: [void@puppet181] Upgraded packages on os162: linux-libc-dev
* 22:21 MirahezeLSBot: [void@puppet181] Upgraded packages on phorge171: linux-libc-dev
* 22:20 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask181: linux-libc-dev
* 22:20 MirahezeLSBot: [void@puppet181] Upgraded packages on os151: linux-libc-dev
* 22:20 MirahezeLSBot: [void@puppet181] Upgraded packages on os161: linux-libc-dev
* 22:20 MirahezeLSBot: [void@puppet181] Upgraded packages on ns1: linux-libc-dev
* 22:19 MirahezeLSBot: [void@puppet181] Upgraded packages on mw203: linux-libc-dev
* 22:19 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask171: linux-libc-dev
* 22:19 MirahezeLSBot: [void@puppet181] Upgraded packages on mw202: linux-libc-dev
* 22:18 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask161: linux-libc-dev
* 22:18 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask151: linux-libc-dev
* 22:18 MirahezeLSBot: [void@puppet181] Upgraded packages on mw201: linux-libc-dev
* 22:18 MirahezeLSBot: [void@puppet181] Upgraded packages on mw183: linux-libc-dev
* 22:17 MirahezeLSBot: [void@puppet181] Upgraded packages on mw193: linux-libc-dev
* 22:17 MirahezeLSBot: [void@puppet181] Upgraded packages on mw192: linux-libc-dev
* 22:17 MirahezeLSBot: [void@puppet181] Upgraded packages on mw182: linux-libc-dev
* 22:16 MirahezeLSBot: [void@puppet181] Upgraded packages on mw181: linux-libc-dev
* 22:16 MirahezeLSBot: [void@puppet181] Upgraded packages on mw191: linux-libc-dev
* 22:16 MirahezeLSBot: [void@puppet181] Upgraded packages on mw173: linux-libc-dev
* 22:15 MirahezeLSBot: [void@puppet181] Upgraded packages on mw171: linux-libc-dev
* 22:15 MirahezeLSBot: [void@puppet181] Upgraded packages on mw172: linux-libc-dev
* 22:15 MirahezeLSBot: [void@puppet181] Upgraded packages on mw153: linux-libc-dev
* 22:15 MirahezeLSBot: [void@puppet181] Upgraded packages on mw161: linux-libc-dev
* 22:14 MirahezeLSBot: [void@puppet181] Upgraded packages on mw163: linux-libc-dev
* 22:14 MirahezeLSBot: [void@puppet181] Upgraded packages on mw151: linux-libc-dev
* 22:14 MirahezeLSBot: [void@puppet181] Upgraded packages on mon181: linux-libc-dev
* 22:13 MirahezeLSBot: [void@puppet181] Upgraded packages on mw162: linux-libc-dev
* 22:13 MirahezeLSBot: [void@puppet181] Upgraded packages on mw152: linux-libc-dev
* 22:13 MirahezeLSBot: [void@puppet181] Upgraded packages on mem191: linux-libc-dev
* 22:13 MirahezeLSBot: [void@puppet181] Upgraded packages on llm191: linux-libc-dev
* 22:12 MirahezeLSBot: [void@puppet181] Upgraded packages on mem201: linux-libc-dev
* 22:12 MirahezeLSBot: [void@puppet181] Upgraded packages on mem161: linux-libc-dev
* 22:12 MirahezeLSBot: [void@puppet181] Upgraded packages on mem151: linux-libc-dev
* 22:12 MirahezeLSBot: [void@puppet181] Upgraded packages on ldap171: linux-libc-dev
* 22:11 MirahezeLSBot: [void@puppet181] Upgraded packages on kafka182: linux-libc-dev
* 22:11 MirahezeLSBot: [void@puppet181] Upgraded packages on matomo151: linux-libc-dev
* 22:11 MirahezeLSBot: [void@puppet181] Upgraded packages on mattermost2: linux-libc-dev
* 22:11 MirahezeLSBot: [void@puppet181] Upgraded packages on cp201: linux-libc-dev
* 22:10 MirahezeLSBot: [void@puppet181] Upgraded packages on db201: linux-libc-dev
* 22:10 MirahezeLSBot: [void@puppet181] Upgraded packages on db192: linux-libc-dev
* 22:10 MirahezeLSBot: [void@puppet181] Upgraded packages on eventgate182: linux-libc-dev
* 22:09 MirahezeLSBot: [void@puppet181] Upgraded packages on cp171: linux-libc-dev
* 22:09 MirahezeLSBot: [void@puppet181] Upgraded packages on cp191: linux-libc-dev
* 22:09 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud19: linux-libc-dev, libcpupower1, and linux-cpupower
* 22:09 MirahezeLSBot: [void@puppet181] Upgraded packages on db182: linux-libc-dev
* 22:08 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud18: linux-libc-dev, libcpupower1, and linux-cpupower
* 22:08 MirahezeLSBot: [void@puppet181] Upgraded packages on graylog161: linux-libc-dev
* 22:08 MirahezeLSBot: [void@puppet181] Upgraded packages on db181: linux-libc-dev
* 22:08 MirahezeLSBot: [void@puppet181] Upgraded packages on bast181: linux-libc-dev
* 22:07 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud20: linux-libc-dev, libcpupower1, and linux-cpupower
* 22:07 MirahezeLSBot: [void@puppet181] Upgraded packages on changeprop202: linux-libc-dev
* 22:07 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud16: linux-libc-dev, libcpupower1, and linux-cpupower
* 22:06 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud15: linux-libc-dev, libcpupower1, and linux-cpupower
* 22:06 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud17: linux-libc-dev, libcpupower1, and linux-cpupower
* 22:06 MirahezeLSBot: [void@puppet181] Upgraded packages on db171: linux-libc-dev
* 22:06 MirahezeLSBot: [void@puppet181] Upgraded packages on db151: linux-libc-dev
* 22:05 MirahezeLSBot: [void@puppet181] Upgraded packages on db161: linux-libc-dev
* 22:05 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud21: linux-libc-dev, libcpupower1, and linux-cpupower
* 22:05 MirahezeLSBot: [void@puppet181] Upgraded packages on bots171: linux-libc-dev
* 22:05 MirahezeLSBot: [void@puppet181] Upgraded packages on db172: linux-libc-dev
* 22:05 MirahezeLSBot: [void@puppet181] Upgraded packages on cp161: linux-libc-dev
* 22:04 MirahezeLSBot: [void@puppet181] Upgraded packages on bast161: linux-libc-dev
* 17:19 MirahezeLSBot: [wwr@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:ReplaceTextEligible --wiki=mathpediaenwiki (END - exit=0)
* 17:18 MirahezeLSBot: [wwr@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:ReplaceTextEligible --wiki=mathpediawiki (END - exit=0)
* 07:57 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php CreateWiki:DeclineStaleWikiRequests --wiki=metawiki --days=5 (END - exit=0)
* 07:55 MirahezeLSBot: [reception@mwtask181] finished deploy of {'l10n': True, 'lang': 'en', 'versions': '1.45'} to all - SUCCESS in 25s
* 07:55 MirahezeLSBot: [reception@mwtask181] starting deploy of {'l10n': True, 'lang': 'en', 'versions': '1.45'} to all
* 07:55 MirahezeLSBot: [reception@mwtask181] DEPLOY ABORTED: Non-Zero Exit Code in prep, see output.
* 07:55 MirahezeLSBot: [reception@mwtask181] starting deploy of {'l10n': True, 'lang': 'en', 'versions': '1.45'} to all
* 07:54 MirahezeLSBot: [reception@mwtask181] finished deploy of {'force_upgrade': True, 'versions': '1.45', 'upgrade_extensions': 'CreateWiki'} to all - SUCCESS in 30s
* 07:53 MirahezeLSBot: [reception@mwtask181] starting deploy of {'force_upgrade': True, 'versions': '1.45', 'upgrade_extensions': 'CreateWiki'} to all
* 03:51 MirahezeLSBot: [skye@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 24s
* 03:50 MirahezeLSBot: [skye@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 03:45 MirahezeLSBot: [skye@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 23s
* 03:45 MirahezeLSBot: [skye@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 03:29 MirahezeLSBot: [somerandomdeveloper@mwtask181] finished deploy of {'folders': '1.45'} to all - SUCCESS in 123s
* 03:27 MirahezeLSBot: [somerandomdeveloper@mwtask181] starting deploy of {'folders': '1.45'} to all
* 03:25 MirahezeLSBot: [somerandomdeveloper@test151] finished deploy of {'folders': '1.45'} to test151 - SUCCESS in 3s
* 03:25 MirahezeLSBot: [somerandomdeveloper@test151] starting deploy of {'folders': '1.45'} to test151
* 03:23 MirahezeLSBot: [somerandomdeveloper@test151] finished deploy of {'folders': '1.45'} to test151 - SUCCESS in 3s
* 03:22 MirahezeLSBot: [somerandomdeveloper@test151] starting deploy of {'folders': '1.45'} to test151
* 03:17 MirahezeLSBot: [somerandomdeveloper@test151] finished deploy of {'world': True, 'versions': '1.45'} to test151 - SUCCESS in 29s
* 03:17 MirahezeLSBot: [somerandomdeveloper@test151] starting deploy of {'world': True, 'versions': '1.45'} to test151
* 01:46 MirahezeLSBot: [petramagna@test151] sudo -u www-data php /srv/mediawiki/1.46/maintenance/run.php rebuildrecentchanges --wiki=loadouttest6wikibeta (END - exit=0)

## 2026-05-22 

* 23:25 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject201: krb5-locales, libk5crypto3, libgssapi-krb5-2, libkrb5support0, libkrb5-3, and libgcrypt20
* 23:25 MirahezeLSBot: [void@puppet181] Upgraded packages on test151: krb5-locales, libk5crypto3, libgssapi-krb5-2, libkrb5support0, libkrb5-3, and libgcrypt20
* 23:25 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject191: krb5-locales, libk5crypto3, libgssapi-krb5-2, libkrb5support0, libkrb5-3, and libgcrypt20
* 23:24 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftproxy161: krb5-locales, libk5crypto3, libgssapi-krb5-2, libkrb5support0, libkrb5-3, and libgcrypt20
* 23:24 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftproxy171: krb5-locales, libk5crypto3, libgssapi-krb5-2, libkrb5support0, libkrb5-3, and libgcrypt20
* 23:24 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject211: krb5-locales, libk5crypto3, libgssapi-krb5-2, libkrb5support0, libkrb5-3, and libgcrypt20
* 23:23 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject181: krb5-locales, libk5crypto3, libgssapi-krb5-2, libkrb5support0, libkrb5-3, and libgcrypt20
* 23:23 MirahezeLSBot: [void@puppet181] Upgraded packages on ns2: libk5crypto3, libgssapi-krb5-2, libkrb5support0, libkrb5-3, and libgcrypt20
* 23:23 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject171: krb5-locales, libk5crypto3, libgssapi-krb5-2, libkrb5support0, libkrb5-3, and libgcrypt20
* 23:23 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftac171: krb5-locales, libk5crypto3, libgssapi-krb5-2, libkrb5support0, libkrb5-3, and libgcrypt20
* 23:22 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject161: krb5-locales, libk5crypto3, libgssapi-krb5-2, libkrb5support0, libkrb5-3, and libgcrypt20
* 23:22 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject151: krb5-locales, libk5crypto3, libgssapi-krb5-2, libkrb5support0, libkrb5-3, and libgcrypt20
* 23:22 MirahezeLSBot: [void@puppet181] Upgraded packages on rdb191: krb5-locales, libk5crypto3, libgssapi-krb5-2, libkrb5support0, libkrb5-3, and libgcrypt20
* 23:22 MirahezeLSBot: [void@puppet181] Upgraded packages on puppet181: krb5-locales, libk5crypto3, libgssapi-krb5-2, libkrb5support0, libkrb5-3, and libgcrypt20
* 23:21 MirahezeLSBot: [void@puppet181] Upgraded packages on os202: krb5-locales, libk5crypto3, libgssapi-krb5-2, libkrb5support0, libkrb5-3, and libgcrypt20
* 23:21 MirahezeLSBot: [void@puppet181] Upgraded packages on reports171: krb5-locales, libk5crypto3, libgssapi-krb5-2, libkrb5support0, libkrb5-3, and libgcrypt20
* 23:21 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask181: krb5-locales, libk5crypto3, libgssapi-krb5-2, libkrb5support0, libkrb5-3, and libgcrypt20
* 23:20 MirahezeLSBot: [void@puppet181] Upgraded packages on prometheus151: krb5-locales, libk5crypto3, libgssapi-krb5-2, libkrb5support0, libkrb5-3, and libgcrypt20
* 23:20 MirahezeLSBot: [void@puppet181] Upgraded packages on phorge171: krb5-locales, libk5crypto3, libgssapi-krb5-2, libkrb5support0, libkrb5-3, and libgcrypt20
* 23:20 MirahezeLSBot: [void@puppet181] Upgraded packages on os162: krb5-locales, libk5crypto3, libgssapi-krb5-2, libkrb5support0, libkrb5-3, and libgcrypt20
* 23:19 MirahezeLSBot: [void@puppet181] Upgraded packages on os201: krb5-locales, libk5crypto3, libgssapi-krb5-2, libkrb5support0, libkrb5-3, and libgcrypt20
* 23:19 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask171: krb5-locales, libk5crypto3, libgssapi-krb5-2, libkrb5support0, libkrb5-3, and libgcrypt20
* 23:19 MirahezeLSBot: [void@puppet181] Upgraded packages on os191: krb5-locales, libk5crypto3, libgssapi-krb5-2, libkrb5support0, libkrb5-3, and libgcrypt20
* 23:19 MirahezeLSBot: [void@puppet181] Upgraded packages on ns1: krb5-locales, libk5crypto3, libgssapi-krb5-2, libkrb5support0, libkrb5-3, and libgcrypt20
* 23:18 MirahezeLSBot: [void@puppet181] Upgraded packages on os151: krb5-locales, libk5crypto3, libgssapi-krb5-2, libkrb5support0, libkrb5-3, and libgcrypt20
* 23:18 MirahezeLSBot: [void@puppet181] Upgraded packages on os161: krb5-locales, libk5crypto3, libgssapi-krb5-2, libkrb5support0, libkrb5-3, and libgcrypt20
* 23:18 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask161: krb5-locales, libk5crypto3, libgssapi-krb5-2, libkrb5support0, libkrb5-3, and libgcrypt20
* 23:18 MirahezeLSBot: [void@puppet181] Upgraded packages on mw203: krb5-locales, libk5crypto3, libgssapi-krb5-2, libkrb5support0, libkrb5-3, and libgcrypt20
* 23:17 MirahezeLSBot: [void@puppet181] Upgraded packages on mw202: krb5-locales, libk5crypto3, libgssapi-krb5-2, libkrb5support0, libkrb5-3, and libgcrypt20
* 23:17 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask151: krb5-locales, libk5crypto3, libgssapi-krb5-2, libkrb5support0, libkrb5-3, and libgcrypt20
* 23:17 MirahezeLSBot: [void@puppet181] Upgraded packages on mw201: krb5-locales, libk5crypto3, libgssapi-krb5-2, libkrb5support0, libkrb5-3, and libgcrypt20
* 23:16 MirahezeLSBot: [void@puppet181] Upgraded packages on mw183: krb5-locales, libk5crypto3, libgssapi-krb5-2, libkrb5support0, libkrb5-3, and libgcrypt20
* 23:16 MirahezeLSBot: [void@puppet181] Upgraded packages on mw181: krb5-locales, libk5crypto3, libgssapi-krb5-2, libkrb5support0, libkrb5-3, and libgcrypt20
* 23:16 MirahezeLSBot: [void@puppet181] Upgraded packages on mw193: krb5-locales, libk5crypto3, libgssapi-krb5-2, libkrb5support0, libkrb5-3, and libgcrypt20
* 23:16 MirahezeLSBot: [void@puppet181] Upgraded packages on mw192: krb5-locales, libk5crypto3, libgssapi-krb5-2, libkrb5support0, libkrb5-3, and libgcrypt20
* 23:15 MirahezeLSBot: [void@puppet181] Upgraded packages on mw182: krb5-locales, libk5crypto3, libgssapi-krb5-2, libkrb5support0, libkrb5-3, and libgcrypt20
* 23:15 MirahezeLSBot: [void@puppet181] Upgraded packages on mw173: krb5-locales, libk5crypto3, libgssapi-krb5-2, libkrb5support0, libkrb5-3, and libgcrypt20
* 23:15 MirahezeLSBot: [void@puppet181] Upgraded packages on mw191: krb5-locales, libk5crypto3, libgssapi-krb5-2, libkrb5support0, libkrb5-3, and libgcrypt20
* 23:14 MirahezeLSBot: [void@puppet181] Upgraded packages on mw171: krb5-locales, libk5crypto3, libgssapi-krb5-2, libkrb5support0, libkrb5-3, and libgcrypt20
* 23:14 MirahezeLSBot: [void@puppet181] Upgraded packages on mw172: krb5-locales, libk5crypto3, libgssapi-krb5-2, libkrb5support0, libkrb5-3, and libgcrypt20
* 23:14 MirahezeLSBot: [void@puppet181] Upgraded packages on ldap171: krb5-locales, libk5crypto3, libgssapi-krb5-2, libkrb5support0, libkrb5-3, and libgcrypt20
* 23:13 MirahezeLSBot: [void@puppet181] Upgraded packages on mw163: krb5-locales, libk5crypto3, libgssapi-krb5-2, libkrb5support0, libkrb5-3, and libgcrypt20
* 23:13 MirahezeLSBot: [void@puppet181] Upgraded packages on mw162: krb5-locales, libk5crypto3, libgssapi-krb5-2, libkrb5support0, libkrb5-3, and libgcrypt20
* 23:13 MirahezeLSBot: [void@puppet181] Upgraded packages on mw161: krb5-locales, libk5crypto3, libgssapi-krb5-2, libkrb5support0, libkrb5-3, and libgcrypt20
* 23:13 MirahezeLSBot: [void@puppet181] Upgraded packages on mw152: krb5-locales, libk5crypto3, libgssapi-krb5-2, libkrb5support0, libkrb5-3, and libgcrypt20
* 23:12 MirahezeLSBot: [void@puppet181] Upgraded packages on mw153: krb5-locales, libk5crypto3, libgssapi-krb5-2, libkrb5support0, libkrb5-3, and libgcrypt20
* 23:12 MirahezeLSBot: [void@puppet181] Upgraded packages on mon181: krb5-locales, libk5crypto3, libgssapi-krb5-2, libkrb5support0, libkrb5-3, and libgcrypt20
* 23:12 MirahezeLSBot: [void@puppet181] Upgraded packages on mw151: krb5-locales, libk5crypto3, libgssapi-krb5-2, libkrb5support0, libkrb5-3, and libgcrypt20
* 23:11 MirahezeLSBot: [void@puppet181] Upgraded packages on mem191: krb5-locales, libk5crypto3, libgssapi-krb5-2, libkrb5support0, libkrb5-3, and libgcrypt20
* 23:11 MirahezeLSBot: [void@puppet181] Upgraded packages on mem201: krb5-locales, libk5crypto3, libgssapi-krb5-2, libkrb5support0, libkrb5-3, and libgcrypt20
* 23:11 MirahezeLSBot: [void@puppet181] Upgraded packages on llm191: krb5-locales, libk5crypto3, libgssapi-krb5-2, libkrb5support0, libkrb5-3, and libgcrypt20
* 23:11 MirahezeLSBot: [void@puppet181] Upgraded packages on mem161: krb5-locales, libk5crypto3, libgssapi-krb5-2, libkrb5support0, libkrb5-3, and libgcrypt20
* 23:10 MirahezeLSBot: [void@puppet181] Upgraded packages on kafka182: krb5-locales, libk5crypto3, libgssapi-krb5-2, libkrb5support0, libkrb5-3, and libgcrypt20
* 23:10 MirahezeLSBot: [void@puppet181] Upgraded packages on mem151: krb5-locales, libk5crypto3, libgssapi-krb5-2, libkrb5support0, libkrb5-3, and libgcrypt20
* 23:10 MirahezeLSBot: [void@puppet181] Upgraded packages on matomo151: krb5-locales, libk5crypto3, libgssapi-krb5-2, libkrb5support0, libkrb5-3, and libgcrypt20
* 23:10 MirahezeLSBot: [void@puppet181] Upgraded packages on mattermost2: libk5crypto3, libgssapi-krb5-2, libkrb5support0, libkrb5-3, and libgcrypt20
* 23:09 MirahezeLSBot: [void@puppet181] Upgraded packages on eventgate182: krb5-locales, libk5crypto3, libgssapi-krb5-2, libkrb5support0, libkrb5-3, and libgcrypt20
* 23:09 MirahezeLSBot: [void@puppet181] Upgraded packages on db192: krb5-locales, libk5crypto3, libgssapi-krb5-2, libkrb5support0, libkrb5-3, and libgcrypt20
* 23:09 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud20: krb5-locales, libgcrypt20, libk5crypto3, libgssapi-krb5-2, libkrb5support0, and libkrb5-3
* 23:09 MirahezeLSBot: [void@puppet181] Upgraded packages on db201: krb5-locales, libk5crypto3, libgssapi-krb5-2, libkrb5support0, libkrb5-3, and libgcrypt20
* 23:08 MirahezeLSBot: [void@puppet181] Upgraded packages on bast181: krb5-locales, libk5crypto3, libgssapi-krb5-2, libkrb5support0, libkrb5-3, and libgcrypt20
* 23:08 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud18: krb5-locales, libgcrypt20, libk5crypto3, libgssapi-krb5-2, libkrb5support0, and libkrb5-3
* 23:08 MirahezeLSBot: [void@puppet181] Upgraded packages on db181: krb5-locales, libk5crypto3, libgssapi-krb5-2, libkrb5support0, libkrb5-3, and libgcrypt20
* 23:07 MirahezeLSBot: [void@puppet181] Upgraded packages on db182: krb5-locales, libk5crypto3, libgssapi-krb5-2, libkrb5support0, libkrb5-3, and libgcrypt20
* 23:07 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud19: krb5-locales, libgcrypt20, libk5crypto3, libgssapi-krb5-2, libkrb5support0, and libkrb5-3
* 23:07 MirahezeLSBot: [void@puppet181] Upgraded packages on cp171: haproxy, krb5-locales, libk5crypto3, libgssapi-krb5-2, libkrb5support0, libkrb5-3, and libgcrypt20
* 23:07 MirahezeLSBot: [void@puppet181] Upgraded packages on graylog161: krb5-locales, libk5crypto3, libgssapi-krb5-2, libkrb5support0, libkrb5-3, and libgcrypt20
* 23:06 MirahezeLSBot: [void@puppet181] Upgraded packages on cp201: haproxy, krb5-locales, libk5crypto3, libgssapi-krb5-2, libkrb5support0, libkrb5-3, and libgcrypt20
* 23:06 MirahezeLSBot: [void@puppet181] Upgraded packages on db151: krb5-locales, libk5crypto3, libgssapi-krb5-2, libkrb5support0, libkrb5-3, and libgcrypt20
* 23:06 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud17: krb5-locales, libgcrypt20, libk5crypto3, libgssapi-krb5-2, libkrb5support0, and libkrb5-3
* 23:05 MirahezeLSBot: [void@puppet181] Upgraded packages on db172: krb5-locales, libk5crypto3, libgssapi-krb5-2, libkrb5support0, libkrb5-3, and libgcrypt20
* 23:05 MirahezeLSBot: [void@puppet181] Upgraded packages on cp161: krb5-locales, libk5crypto3, libgssapi-krb5-2, libkrb5support0, libkrb5-3, and libgcrypt20
* 23:05 MirahezeLSBot: [void@puppet181] Upgraded packages on changeprop202: haproxy, krb5-locales, libk5crypto3, libgssapi-krb5-2, libkrb5support0, libkrb5-3, and libgcrypt20
* 23:05 MirahezeLSBot: [void@puppet181] Upgraded packages on cp191: haproxy, krb5-locales, libk5crypto3, libgssapi-krb5-2, libkrb5support0, libkrb5-3, and libgcrypt20
* 23:04 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud15: krb5-locales, libgcrypt20, libk5crypto3, libgssapi-krb5-2, libkrb5support0, and libkrb5-3
* 23:04 MirahezeLSBot: [void@puppet181] Upgraded packages on db171: krb5-locales, libk5crypto3, libgssapi-krb5-2, libkrb5support0, libkrb5-3, and libgcrypt20
* 23:04 MirahezeLSBot: [void@puppet181] Upgraded packages on db161: krb5-locales, libk5crypto3, libgssapi-krb5-2, libkrb5support0, libkrb5-3, and libgcrypt20
* 23:04 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud16: krb5-locales, libgcrypt20, libk5crypto3, libgssapi-krb5-2, libkrb5support0, and libkrb5-3
* 23:03 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud21: krb5-locales, libgcrypt20, libk5crypto3, libgssapi-krb5-2, libkrb5support0, and libkrb5-3
* 23:03 MirahezeLSBot: [void@puppet181] Upgraded packages on bots171: libk5crypto3, libgssapi-krb5-2, libkrb5support0, libkrb5-3, krb5-locales, and libgcrypt20
* 23:03 MirahezeLSBot: [void@puppet181] Upgraded packages on bast161: krb5-locales, libk5crypto3, libgssapi-krb5-2, libkrb5support0, libkrb5-3, and libgcrypt20
* 22:54 MirahezeLSBot: [paladox@mwtask181] finished deploy of {'l10n': True, 'force_upgrade': True, 'versions': '1.45', 'upgrade_extensions': 'PageForms'} to all - SUCCESS in 478s
* 22:52 MirahezeLSBot: [paladox@test151] finished deploy of {'l10n': True, 'force_upgrade': True, 'versions': ['1.45', '1.46'], 'upgrade_extensions': 'PageForms'} to test151 - SUCCESS in 375s
* 22:46 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'l10n': True, 'force_upgrade': True, 'versions': '1.45', 'upgrade_extensions': 'PageForms'} to all
* 22:46 MirahezeLSBot: [paladox@mwtask181] DEPLOY ABORTED: Non-Zero Exit Code in prep, see output.
* 22:46 MirahezeLSBot: [paladox@test151] starting deploy of {'l10n': True, 'force_upgrade': True, 'versions': ['1.45', '1.46'], 'upgrade_extensions': 'PageForms'} to test151
* 22:46 MirahezeLSBot: [paladox@test151] DEPLOY ABORTED: Non-Zero Exit Code in prep, see output.
* 22:46 MirahezeLSBot: [paladox@test151] starting deploy of {'l10n': True, 'force_upgrade': True, 'versions': ['1.45', '1.46'], 'upgrade_extensions': 'PageForms'} to test151
* 22:46 MirahezeLSBot: [paladox@test151] DEPLOY ABORTED: Non-Zero Exit Code in prep, see output.
* 22:45 MirahezeLSBot: [paladox@test151] starting deploy of {'l10n': True, 'force_upgrade': True, 'versions': ['1.45', '1.46'], 'upgrade_extensions': 'PageForms'} to test151
* 22:44 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'l10n': True, 'force_upgrade': True, 'versions': '1.45', 'upgrade_extensions': 'PageForms'} to all
* 22:42 MirahezeLSBot: [paladox@mwtask181] DEPLOY ABORTED: Non-Zero Exit Code in prep, see output.
* 22:42 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'l10n': True, 'versions': '1.45', 'upgrade_extensions': 'PageForms'} to all
* 22:34 MirahezeLSBot: [paladox@mwtask181] DEPLOY ABORTED: Non-Zero Exit Code in prep, see output.
* 22:34 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'l10n': True, 'force_upgrade': True, 'versions': '1.45', 'upgrade_extensions': 'PageForms'} to all
* 22:33 MirahezeLSBot: [paladox@mwtask181] DEPLOY ABORTED: Non-Zero Exit Code in prep, see output.
* 22:33 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'l10n': True, 'versions': '1.45', 'upgrade_extensions': 'PageForms'} to all
* 21:39 SomeRandomDeveloper: depool c2
* 20:55 Reception123: MariaDB [mhglobal]> UPDATE cw_wikis SET wiki_inactive_exempt_reason = 'comp' WHERE wiki_inactive_exempt_reason = 'mtr'; ('mtr' and 'comp' have been merged)
* 20:54 MirahezeLSBot: [reception@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 25s
* 20:53 MirahezeLSBot: [reception@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 19:34 MirahezeLSBot: [reception@mwtask181] finished deploy of {'world': True, 'versions': '1.45'} to all - SUCCESS in 210s
* 19:33 MirahezeLSBot: [wwr@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php CreateWiki:SetContainersAccess --wiki=scratchwiki (END - exit=0)
* 19:30 MirahezeLSBot: [reception@mwtask181] starting deploy of {'world': True, 'versions': '1.45'} to all
* 19:30 TheWWRNerdGuy: yes I did use quote marks just logsal doesn't like to notice that
* 19:29 MirahezeLSBot: [wwr@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:ResetWiki --wiki=loginwiki --dbname=scratchwiki --requester=MC mrjone (END - exit=0)
* 17:14 MirahezeLSBot: [reception@mwtask181] DEPLOY ABORTED: Non-Zero Exit Code in prep, see output.
* 17:14 MirahezeLSBot: [reception@mwtask181] starting deploy of {'world': True, 'force': True, 'versions': '1.45'} to all
* 17:14 MirahezeLSBot: [reception@mwtask181] DEPLOY ABORTED: Non-Zero Exit Code in prep, see output.
* 17:14 MirahezeLSBot: [reception@mwtask181] starting deploy of {'world': True, 'versions': '1.45', 'upgrade_extensions': 'CreateWiki'} to all
* 17:13 MirahezeLSBot: [reception@mwtask181] DEPLOY ABORTED: Non-Zero Exit Code in prep, see output.
* 17:13 MirahezeLSBot: [reception@mwtask181] starting deploy of {'world': True, 'force': True, 'versions': '1.45', 'upgrade_extensions': 'CreateWiki'} to all
* 17:12 MirahezeLSBot: [reception@mwtask181] finished deploy of {'l10n': True, 'versions': '1.45', 'upgrade_extensions': 'CreateWiki'} to all - SUCCESS in 527s
* 17:03 MirahezeLSBot: [reception@mwtask181] starting deploy of {'l10n': True, 'versions': '1.45', 'upgrade_extensions': 'CreateWiki'} to all
* 01:45 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php CreateWiki:SetContainersAccess --wiki=hyperchargewiki (END - exit=0)
* 01:44 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RenameDatabase --wiki=loginwiki --rename --old=funiraccoongamewiki --new=hyperchargewiki --user=Skye (END - exit=0)
* 01:41 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php CreateWiki:SetContainersAccess --wiki=doomsdayhunterswiki (END - exit=0)
* 01:39 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RenameDatabase --wiki=loginwiki --rename --old=raccoinwiki --new=doomsdayhunterswiki --user=Skye (END - exit=0)
* 01:36 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php CreateWiki:SetContainersAccess --wiki=uaccfoundationofficialwiki (END - exit=0)
* 01:33 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RenameDatabase --wiki=loginwiki --rename --old=amcfoundationofficialwiki --new=uaccfoundationofficialwiki --user=Skye (END - exit=0)
* 01:23 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php CreateWiki:SetContainersAccess --wiki=aswonuwiki (END - exit=0)
* 01:21 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RenameDatabase --wiki=loginwiki --rename --old=negapaintwiki --new=aswonuwiki --user=Skye (END - exit=0)
* 01:12 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php CreateWiki:SetContainersAccess --wiki=vyetnapediawiki (END - exit=0)
* 01:09 MirahezeLSBot: [petramagna@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 24s
* 01:09 MirahezeLSBot: [petramagna@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 01:06 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RenameDatabase --wiki=loginwiki --rename --old=uncwikiwiki --new=vyetnapediawiki --user=Skye (END - exit=0)
* 00:59 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php CreateWiki:SetContainersAccess --wiki=havoreywiki (END - exit=0)
* 00:57 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RenameDatabase --wiki=loginwiki --rename --old=osterholtwiki --new=havoreywiki --user=Skye (END - exit=0)
* 00:49 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php CreateWiki:SetContainersAccess --wiki=malwaredlcwiki (END - exit=0)
* 00:46 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RenameDatabase --wiki=loginwiki --rename --old=impostorsyndromewiki --new=malwaredlcwiki --user=Skye (END - exit=0)
* 00:43 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php CreateWiki:SetContainersAccess --wiki=conquerorsofthecraftwiki (END - exit=0)
* 00:04 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RenameDatabase --wiki=loginwiki --rename --old=alentiniszerwiki --new=conquerorsofthecraftwiki --user=Skye (END - exit=0)

## 2026-05-21 

* 23:31 MirahezeLSBot: [void@puppet181] Upgraded packages on puppet181: libnss3
* 23:30 MirahezeLSBot: [void@puppet181] Upgraded packages on graylog161: libnss3
* 22:10 MirahezeLSBot: [void@puppet181] Upgraded packages on os191: libnss3
* 22:10 MirahezeLSBot: [void@puppet181] Upgraded packages on os201: libnss3
* 22:09 MirahezeLSBot: [void@puppet181] Upgraded packages on os151: libnss3
* 22:09 MirahezeLSBot: [void@puppet181] Upgraded packages on os202: libnss3
* 22:09 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask181: libnss3
* 22:09 MirahezeLSBot: [void@puppet181] Upgraded packages on test151: libnss3
* 22:08 MirahezeLSBot: [void@puppet181] Upgraded packages on os161: libnss3
* 22:08 MirahezeLSBot: [void@puppet181] Upgraded packages on mw203: libnss3
* 22:08 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask171: libnss3
* 22:07 MirahezeLSBot: [void@puppet181] Upgraded packages on os162: libnss3
* 22:07 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask161: libnss3
* 22:07 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask151: libnss3
* 22:07 MirahezeLSBot: [void@puppet181] Upgraded packages on mw183: libnss3
* 22:06 MirahezeLSBot: [void@puppet181] Upgraded packages on mw192: libnss3
* 22:06 MirahezeLSBot: [void@puppet181] Upgraded packages on mw193: libnss3
* 22:06 MirahezeLSBot: [void@puppet181] Upgraded packages on mw202: libnss3
* 22:05 MirahezeLSBot: [void@puppet181] Upgraded packages on mw201: libnss3
* 22:05 MirahezeLSBot: [void@puppet181] Upgraded packages on mw182: libnss3
* 22:05 MirahezeLSBot: [void@puppet181] Upgraded packages on mw181: libnss3
* 22:05 MirahezeLSBot: [void@puppet181] Upgraded packages on mw153: libnss3
* 22:04 MirahezeLSBot: [void@puppet181] Upgraded packages on mw191: libnss3
* 22:04 MirahezeLSBot: [void@puppet181] Upgraded packages on mw173: libnss3
* 22:04 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud20: libnss3
* 22:03 MirahezeLSBot: [void@puppet181] Upgraded packages on mw163: libnss3
* 22:03 MirahezeLSBot: [void@puppet181] Upgraded packages on mw172: libnss3
* 22:03 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud18: libnss3
* 22:03 MirahezeLSBot: [void@puppet181] Upgraded packages on mw171: libnss3
* 22:02 MirahezeLSBot: [void@puppet181] Upgraded packages on mw161: libnss3
* 22:02 MirahezeLSBot: [void@puppet181] Upgraded packages on mw162: libnss3
* 22:02 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud19: libnss3
* 22:02 MirahezeLSBot: [void@puppet181] Upgraded packages on mw151: libnss3
* 22:01 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud17: libnss3
* 22:01 MirahezeLSBot: [void@puppet181] Upgraded packages on mw152: libnss3
* 22:01 MirahezeLSBot: [void@puppet181] Upgraded packages on kafka182: libnss3
* 22:01 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud16: libnss3
* 22:00 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud15: libnss3
* 22:00 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud21: libnss3
* 20:14 MirahezeLSBot: [skye@mwtask171] Finished import for b3313wiki (XML: None; Images: files/) (END - exit=0)
* 20:14 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php initSiteStats --wiki=b3313wiki --update (END - exit=0)
* 20:14 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php initSiteStats --wiki=b3313wiki --update (START)
* 20:14 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=b3313wiki --sleep=1 '--comment=Importing files from b3313.fandom.com ([T15374](https://meta.miraheze.org/wiki/phorge:T15374))' -- files/ (END - exit=0)
* 20:00 PetraMagna: Run SQL `update securepoll_properties set pr_value=3 where pr_entity=59 and pr_key='default-score';` on metawiki
* 19:50 MirahezeLSBot: [petramagna@mwtask181] finished deploy of {'folders': '1.45/extensions/SecurePoll'} to all - SUCCESS in 24s
* 19:50 MirahezeLSBot: [petramagna@mwtask181] starting deploy of {'folders': '1.45/extensions/SecurePoll'} to all
* 19:31 MirahezeLSBot: [skye@mwtask171] Finished import for housingwiki (XML: None; Images: .) (END - exit=0)
* 19:31 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php initSiteStats --wiki=housingwiki --update (END - exit=0)
* 19:31 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php initSiteStats --wiki=housingwiki --update (START)
* 19:31 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=housingwiki --sleep=1 '--comment=Importing images from horrific-housing.fandom.com ([T15385](https://meta.miraheze.org/wiki/phorge:T15385))' -- . (END - exit=0)
* 19:07 MirahezeLSBot: [petramagna@test151] finished deploy of {'folders': '1.46/extensions/SecurePoll'} to test151 - SUCCESS in 0s
* 19:07 MirahezeLSBot: [petramagna@test151] starting deploy of {'folders': '1.46/extensions/SecurePoll'} to test151
* 19:06 MirahezeLSBot: [petramagna@test151] finished deploy of {'folders': '1.46/extensions/SecurePoll'} to test151 - SUCCESS in 0s
* 19:06 MirahezeLSBot: [petramagna@test151] starting deploy of {'folders': '1.46/extensions/SecurePoll'} to test151
* 18:39 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=housingwiki --sleep=1 '--comment=Importing images from horrific-housing.fandom.com ([T15385](https://meta.miraheze.org/wiki/phorge:T15385))' -- . (START)
* 18:39 MirahezeLSBot: [skye@mwtask171] Starting import for housingwiki (XML: None; Images: .) (START)
* 18:30 PetraMagna: Executing SQL `delete from securepoll_properties where pr_entity=58 and pr_key='tally-error';` on metawiki
* 18:30 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=b3313wiki --sleep=1 '--comment=Importing files from b3313.fandom.com ([T15374](https://meta.miraheze.org/wiki/phorge:T15374))' -- files/ (START)
* 18:30 MirahezeLSBot: [skye@mwtask171] Starting import for b3313wiki (XML: None; Images: files/) (START)
* 18:28 MirahezeLSBot: [skye@mwtask171] Finished import for b3313wiki (XML: b3313_pages_full.xml; Images: files/) (END - exit=1)
* 18:28 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=b3313wiki --sleep=1 '--comment=Importing files from b3313.fandom.com ([T15374](https://meta.miraheze.org/wiki/phorge:T15374))' -- files/ (END - exit=1)
* 18:25 MirahezeLSBot: [petramagna@test151] finished deploy of {'folders': '1.46/extensions/SecurePoll'} to test151 - SUCCESS in 0s
* 18:25 MirahezeLSBot: [petramagna@test151] starting deploy of {'folders': '1.46/extensions/SecurePoll'} to test151
* 18:24 MirahezeLSBot: [skye@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 26s
* 18:24 MirahezeLSBot: [skye@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 18:23 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=b3313wiki --sleep=1 '--comment=Importing files from b3313.fandom.com ([T15374](https://meta.miraheze.org/wiki/phorge:T15374))' -- files/ (START)
* 18:23 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importDump --wiki=b3313wiki --no-updates --username-prefix=fandom:b3313 -- b3313_pages_full.xml (END - exit=0)
* 18:13 MirahezeLSBot: [skye@mwtask171] Finished import for frojoappswiki (XML: None; Images: .) (END - exit=0)
* 18:13 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php initSiteStats --wiki=frojoappswiki --update (END - exit=0)
* 18:13 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php initSiteStats --wiki=frojoappswiki --update (START)
* 18:13 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=frojoappswiki --sleep=1 '--comment=Importing images from frojoapps.fandom.com ([T15355](https://meta.miraheze.org/wiki/phorge:T15355))' -- . (END - exit=0)
* 17:59 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importDump --wiki=b3313wiki --no-updates --username-prefix=fandom:b3313 -- b3313_pages_full.xml (START)
* 17:59 MirahezeLSBot: [skye@mwtask171] Starting import for b3313wiki (XML: b3313_pages_full.xml; Images: files/) (START)
* 17:50 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=frojoappswiki --sleep=1 '--comment=Importing images from frojoapps.fandom.com ([T15355](https://meta.miraheze.org/wiki/phorge:T15355))' -- . (START)
* 17:50 MirahezeLSBot: [skye@mwtask171] Starting import for frojoappswiki (XML: None; Images: .) (START)

## 2026-05-20 

* 21:41 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftproxy161: bind9-host, bind9-dnsutils, and bind9-libs
* 21:41 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject201: bind9-host, bind9-dnsutils, and bind9-libs
* 21:41 MirahezeLSBot: [void@puppet181] Upgraded packages on test151: bind9-host, bind9-dnsutils, and bind9-libs
* 21:40 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftproxy171: bind9-host, bind9-dnsutils, and bind9-libs
* 21:40 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject191: bind9-host, bind9-dnsutils, and bind9-libs
* 21:40 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject211: bind9-host, bind9-dnsutils, and bind9-libs
* 21:39 MirahezeLSBot: [void@puppet181] Upgraded packages on ns2: bind9-host, bind9-dnsutils, and bind9-libs
* 21:39 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject171: bind9-host, bind9-dnsutils, and bind9-libs
* 21:39 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject181: bind9-host, bind9-dnsutils, and bind9-libs
* 21:38 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject161: bind9-host, bind9-dnsutils, and bind9-libs
* 21:38 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftac171: bind9-host, bind9-dnsutils, and bind9-libs
* 21:38 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject151: bind9-host, bind9-dnsutils, and bind9-libs
* 21:38 MirahezeLSBot: [void@puppet181] Upgraded packages on rdb191: bind9-host, bind9-dnsutils, and bind9-libs
* 21:37 MirahezeLSBot: [void@puppet181] Upgraded packages on os201: bind9-host, bind9-dnsutils, and bind9-libs
* 21:37 MirahezeLSBot: [void@puppet181] Upgraded packages on puppet181: bind9-host, bind9-dnsutils, and bind9-libs
* 21:37 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask181: bind9-host, bind9-dnsutils, and bind9-libs
* 21:36 MirahezeLSBot: [void@puppet181] Upgraded packages on os202: bind9-host, bind9-dnsutils, and bind9-libs
* 21:36 MirahezeLSBot: [void@puppet181] Upgraded packages on prometheus151: bind9-host, bind9-dnsutils, and bind9-libs
* 21:36 MirahezeLSBot: [void@puppet181] Upgraded packages on reports171: bind9-host, bind9-dnsutils, and bind9-libs
* 21:36 MirahezeLSBot: [void@puppet181] Upgraded packages on os191: bind9-host, bind9-dnsutils, and bind9-libs
* 21:35 MirahezeLSBot: [void@puppet181] Upgraded packages on phorge171: bind9-host, bind9-dnsutils, and bind9-libs
* 21:35 MirahezeLSBot: [void@puppet181] Upgraded packages on os161: bind9-host, bind9-dnsutils, and bind9-libs
* 21:35 MirahezeLSBot: [void@puppet181] Upgraded packages on os151: bind9-host, bind9-dnsutils, and bind9-libs
* 21:35 MirahezeLSBot: [void@puppet181] Upgraded packages on os162: bind9-host, bind9-dnsutils, and bind9-libs
* 21:34 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask161: bind9-host, bind9-dnsutils, and bind9-libs
* 21:34 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask171: bind9-host, bind9-dnsutils, and bind9-libs
* 21:34 MirahezeLSBot: [void@puppet181] Upgraded packages on mw203: bind9-host, bind9-dnsutils, and bind9-libs
* 21:33 MirahezeLSBot: [void@puppet181] Upgraded packages on ns1: bind9-host, bind9-dnsutils, and bind9-libs
* 21:33 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask151: bind9-host, bind9-dnsutils, and bind9-libs
* 21:33 MirahezeLSBot: [void@puppet181] Upgraded packages on mw202: bind9-host, bind9-dnsutils, and bind9-libs
* 21:33 MirahezeLSBot: [void@puppet181] Upgraded packages on mw201: bind9-host, bind9-dnsutils, and bind9-libs
* 21:32 MirahezeLSBot: [void@puppet181] Upgraded packages on mw183: bind9-host, bind9-dnsutils, and bind9-libs
* 21:32 MirahezeLSBot: [void@puppet181] Upgraded packages on mw192: bind9-host, bind9-dnsutils, and bind9-libs
* 21:32 MirahezeLSBot: [void@puppet181] Upgraded packages on mw193: bind9-host, bind9-dnsutils, and bind9-libs
* 21:31 MirahezeLSBot: [void@puppet181] Upgraded packages on mw182: bind9-host, bind9-dnsutils, and bind9-libs
* 21:31 MirahezeLSBot: [void@puppet181] Upgraded packages on mw181: bind9-host, bind9-dnsutils, and bind9-libs
* 21:31 MirahezeLSBot: [void@puppet181] Upgraded packages on mw173: bind9-host, bind9-dnsutils, and bind9-libs
* 21:30 MirahezeLSBot: [void@puppet181] Upgraded packages on mw191: bind9-host, bind9-dnsutils, and bind9-libs
* 21:30 MirahezeLSBot: [void@puppet181] Upgraded packages on mw172: bind9-host, bind9-dnsutils, and bind9-libs
* 21:30 MirahezeLSBot: [void@puppet181] Upgraded packages on mw153: bind9-host, bind9-dnsutils, and bind9-libs
* 21:29 MirahezeLSBot: [void@puppet181] Upgraded packages on mw162: bind9-host, bind9-dnsutils, and bind9-libs
* 21:29 MirahezeLSBot: [void@puppet181] Upgraded packages on mw163: bind9-host, bind9-dnsutils, and bind9-libs
* 21:29 MirahezeLSBot: [void@puppet181] Upgraded packages on mw171: bind9-host, bind9-dnsutils, and bind9-libs
* 21:28 MirahezeLSBot: [void@puppet181] Upgraded packages on mw161: bind9-host, bind9-dnsutils, and bind9-libs
* 21:28 MirahezeLSBot: [void@puppet181] Upgraded packages on mw152: bind9-host, bind9-dnsutils, and bind9-libs
* 21:28 MirahezeLSBot: [void@puppet181] Upgraded packages on mem191: bind9-host, bind9-dnsutils, and bind9-libs
* 21:28 MirahezeLSBot: [void@puppet181] Upgraded packages on mon181: bind9-host, bind9-dnsutils, and bind9-libs
* 21:27 MirahezeLSBot: [void@puppet181] Upgraded packages on mw151: bind9-host, bind9-dnsutils, and bind9-libs
* 21:27 MirahezeLSBot: [void@puppet181] Upgraded packages on mem201: bind9-host, bind9-dnsutils, and bind9-libs
* 21:27 MirahezeLSBot: [void@puppet181] Upgraded packages on llm191: bind9-host, bind9-dnsutils, and bind9-libs
* 21:26 MirahezeLSBot: [void@puppet181] Upgraded packages on ldap171: bind9-host, bind9-dnsutils, and bind9-libs
* 21:26 MirahezeLSBot: [void@puppet181] Upgraded packages on mem151: bind9-host, bind9-dnsutils, and bind9-libs
* 21:26 MirahezeLSBot: [void@puppet181] Upgraded packages on mem161: bind9-host, bind9-dnsutils, and bind9-libs
* 21:26 MirahezeLSBot: [void@puppet181] Upgraded packages on kafka182: bind9-host, bind9-dnsutils, and bind9-libs
* 21:25 MirahezeLSBot: [void@puppet181] Upgraded packages on matomo151: bind9-host, bind9-dnsutils, and bind9-libs
* 21:25 MirahezeLSBot: [void@puppet181] Upgraded packages on mattermost2: bind9-host, bind9-dnsutils, and bind9-libs
* 21:25 MirahezeLSBot: [void@puppet181] Upgraded packages on db201: bind9-host, bind9-dnsutils, and bind9-libs
* 21:25 MirahezeLSBot: [void@puppet181] Upgraded packages on cp201: bind9-host, bind9-dnsutils, and bind9-libs
* 21:24 MirahezeLSBot: [void@puppet181] Upgraded packages on db182: bind9-host, bind9-dnsutils, and bind9-libs
* 21:24 MirahezeLSBot: [void@puppet181] Upgraded packages on db181: bind9-host, bind9-dnsutils, and bind9-libs
* 21:24 MirahezeLSBot: [void@puppet181] Upgraded packages on graylog161: bind9-host, bind9-dnsutils, and bind9-libs
* 21:24 MirahezeLSBot: [void@puppet181] Upgraded packages on db192: bind9-host, bind9-dnsutils, and bind9-libs
* 21:23 MirahezeLSBot: [void@puppet181] Upgraded packages on eventgate182: bind9-host, bind9-dnsutils, and bind9-libs
* 21:23 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud20: bind9-host, bind9-dnsutils, and bind9-libs
* 21:23 MirahezeLSBot: [void@puppet181] Upgraded packages on changeprop202: bind9-host, bind9-dnsutils, and bind9-libs
* 21:22 MirahezeLSBot: [void@puppet181] Upgraded packages on bast181: bind9-host, bind9-dnsutils, and bind9-libs
* 21:22 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud18: bind9-host, bind9-dnsutils, and bind9-libs
* 21:22 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud16: bind9-host, bind9-dnsutils, and bind9-libs
* 21:22 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud19: bind9-host, bind9-dnsutils, and bind9-libs
* 21:22 MirahezeLSBot: [petramagna@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 21:22 MirahezeLSBot: [petramagna@test151] starting deploy of {'config': True} to test151
* 21:21 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud17: bind9-host, bind9-dnsutils, and bind9-libs
* 21:21 MirahezeLSBot: [void@puppet181] Upgraded packages on db161: bind9-host, bind9-dnsutils, and bind9-libs
* 21:21 MirahezeLSBot: [void@puppet181] Upgraded packages on cp171: bind9-host, bind9-dnsutils, and bind9-libs
* 21:21 MirahezeLSBot: [void@puppet181] Upgraded packages on db151: bind9-host, bind9-dnsutils, and bind9-libs
* 21:20 MirahezeLSBot: [void@puppet181] Upgraded packages on cp191: bind9-host, bind9-dnsutils, and bind9-libs
* 21:20 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud15: bind9-host, bind9-dnsutils, and bind9-libs
* 21:20 MirahezeLSBot: [void@puppet181] Upgraded packages on cp161: bind9-host, bind9-dnsutils, and bind9-libs
* 21:20 MirahezeLSBot: [void@puppet181] Upgraded packages on db171: bind9-host, bind9-dnsutils, and bind9-libs
* 21:19 MirahezeLSBot: [void@puppet181] Upgraded packages on db172: bind9-host, bind9-dnsutils, and bind9-libs
* 21:19 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud21: bind9-host, bind9-dnsutils, and bind9-libs
* 21:19 MirahezeLSBot: [void@puppet181] Upgraded packages on bots171: bind9-host, bind9-dnsutils, and bind9-libs
* 21:19 MirahezeLSBot: [void@puppet181] Upgraded packages on bast161: bind9-host, bind9-dnsutils, and bind9-libs
* 20:12 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject201: rsync
* 20:11 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftproxy161: rsync
* 20:11 MirahezeLSBot: [void@puppet181] Upgraded packages on test151: rsync
* 20:11 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject191: rsync
* 20:10 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftproxy171: rsync
* 20:10 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject211: rsync
* 20:10 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject181: rsync
* 20:09 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject171: rsync
* 20:09 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject161: rsync
* 20:09 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftac171: rsync
* 20:08 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject151: rsync
* 20:07 MirahezeLSBot: [void@puppet181] Upgraded packages on puppet181: rsync
* 20:07 MirahezeLSBot: [void@puppet181] Upgraded packages on reports171: rsync
* 20:07 MirahezeLSBot: [void@puppet181] Upgraded packages on os161: rsync
* 20:06 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask181: rsync
* 20:06 MirahezeLSBot: [void@puppet181] Upgraded packages on prometheus151: rsync
* 20:06 MirahezeLSBot: [void@puppet181] Upgraded packages on phorge171: rsync
* 20:05 MirahezeLSBot: [void@puppet181] Upgraded packages on os162: rsync
* 20:05 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask171: rsync
* 20:05 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask151: rsync
* 20:04 MirahezeLSBot: [void@puppet181] Upgraded packages on os151: rsync
* 20:04 MirahezeLSBot: [void@puppet181] Upgraded packages on mw203: rsync
* 20:04 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask161: rsync
* 20:03 MirahezeLSBot: [void@puppet181] Upgraded packages on mw202: rsync
* 20:02 MirahezeLSBot: [void@puppet181] Upgraded packages on mw201: rsync
* 20:02 MirahezeLSBot: [void@puppet181] Upgraded packages on mw193: rsync
* 20:00 MirahezeLSBot: [void@puppet181] Upgraded packages on mw192: rsync
* 19:59 MirahezeLSBot: [void@puppet181] Upgraded packages on mw182: rsync
* 19:59 MirahezeLSBot: [void@puppet181] Upgraded packages on mw183: rsync
* 19:58 MirahezeLSBot: [void@puppet181] Upgraded packages on mw191: rsync
* 19:57 MirahezeLSBot: [void@puppet181] Upgraded packages on mw173: rsync
* 19:56 MirahezeLSBot: [void@puppet181] Upgraded packages on mw163: rsync
* 19:56 MirahezeLSBot: [void@puppet181] Upgraded packages on mw181: rsync
* 19:55 MirahezeLSBot: [void@puppet181] Upgraded packages on mw161: rsync
* 19:54 MirahezeLSBot: [void@puppet181] Upgraded packages on mw171: rsync
* 19:53 MirahezeLSBot: [void@puppet181] Upgraded packages on mw172: rsync
* 19:52 MirahezeLSBot: [void@puppet181] Upgraded packages on mw153: rsync
* 19:51 MirahezeLSBot: [void@puppet181] Upgraded packages on mw162: rsync
* 19:50 MirahezeLSBot: [void@puppet181] Upgraded packages on mw152: rsync
* 19:50 MirahezeLSBot: [void@puppet181] Upgraded packages on mon181: rsync
* 19:49 MirahezeLSBot: [void@puppet181] Upgraded packages on mw151: rsync
* 19:48 MirahezeLSBot: [void@puppet181] Upgraded packages on mem161: rsync
* 19:48 MirahezeLSBot: [void@puppet181] Upgraded packages on mem151: rsync
* 19:47 MirahezeLSBot: [void@puppet181] Upgraded packages on matomo151: rsync
* 19:47 MirahezeLSBot: [void@puppet181] Upgraded packages on ldap171: rsync
* 19:47 MirahezeLSBot: [void@puppet181] Upgraded packages on graylog161: rsync
* 19:47 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud18: rsync
* 19:46 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud19: rsync
* 19:46 MirahezeLSBot: [void@puppet181] Upgraded packages on db192: rsync
* 19:45 MirahezeLSBot: [void@puppet181] Upgraded packages on db201: rsync
* 19:45 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud17: rsync
* 19:45 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud20: rsync
* 19:44 MirahezeLSBot: [void@puppet181] Upgraded packages on db182: rsync
* 19:44 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud16: rsync
* 19:44 MirahezeLSBot: [void@puppet181] Upgraded packages on cp171: rsync
* 19:43 MirahezeLSBot: [void@puppet181] Upgraded packages on cp161: rsync
* 19:43 MirahezeLSBot: [void@puppet181] Upgraded packages on db181: rsync
* 19:43 MirahezeLSBot: [void@puppet181] Upgraded packages on db171: rsync
* 19:42 MirahezeLSBot: [void@puppet181] Upgraded packages on bast181: rsync
* 19:42 MirahezeLSBot: [void@puppet181] Upgraded packages on db161: rsync
* 19:42 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud21: rsync
* 19:42 MirahezeLSBot: [void@puppet181] Upgraded packages on db172: rsync
* 19:41 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud15: rsync
* 19:41 MirahezeLSBot: [void@puppet181] Upgraded packages on db151: rsync
* 19:41 MirahezeLSBot: [void@puppet181] Upgraded packages on bots171: rsync
* 19:40 MirahezeLSBot: [void@puppet181] Upgraded packages on bast161: rsync
* 15:20 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.46/maintenance/run.php RebuildRecentchanges --wiki=exttestwikibeta (END - exit=0)
* 08:48 PetraMagna: Run SQL statement `delete from securepoll_properties where pr_entity=58 and pr_key='tally-job-enqueued';` on metawiki due to failed SecurePoll tally job exectuion.
* 08:39 MirahezeLSBot: [petramagna@test151] starting deploy of {'folders': '1.46/extensions/ManageWiki'} to test151
* 08:38 MirahezeLSBot: [petramagna@test151] starting deploy of {'folders': '1.46/extensions/ManageWiki'} to test151
* 07:56 MirahezeLSBot: [petramagna@test151] finished deploy of {'folders': '1.46/extensions/ManageWiki'} to test151 - SUCCESS in 0s
* 07:56 MirahezeLSBot: [petramagna@test151] starting deploy of {'folders': '1.46/extensions/ManageWiki'} to test151
* 06:57 MirahezeLSBot: [petramagna@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 23s
* 06:57 MirahezeLSBot: [petramagna@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 01:47 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject201: libgnutls30t64
* 01:46 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject191: libgnutls30t64
* 01:46 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftproxy161: libgnutls30t64
* 01:46 MirahezeLSBot: [void@puppet181] Upgraded packages on test151: libgnutls30t64
* 01:46 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftproxy171: libgnutls30t64
* 01:45 MirahezeLSBot: [void@puppet181] Upgraded packages on ns2: libgnutls30t64
* 01:45 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject211: libgnutls30t64
* 01:45 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject181: libgnutls30t64
* 01:44 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject161: libgnutls30t64
* 01:44 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject171: libgnutls30t64
* 01:44 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftac171: libgnutls30t64
* 01:44 MirahezeLSBot: [void@puppet181] Upgraded packages on os191: libgnutls30t64
* 01:43 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject151: libgnutls30t64
* 01:43 MirahezeLSBot: [void@puppet181] Upgraded packages on os161: libgnutls30t64
* 01:43 MirahezeLSBot: [void@puppet181] Upgraded packages on os201: libgnutls30t64
* 01:43 MirahezeLSBot: [void@puppet181] Upgraded packages on os151: libgnutls30t64
* 01:42 MirahezeLSBot: [void@puppet181] Upgraded packages on os202: libgnutls30t64
* 01:42 MirahezeLSBot: [void@puppet181] Upgraded packages on rdb191: libgnutls30t64
* 01:42 MirahezeLSBot: [void@puppet181] Upgraded packages on puppet181: libgnutls30t64
* 01:41 MirahezeLSBot: [void@puppet181] Upgraded packages on reports171: libgnutls30t64
* 01:41 MirahezeLSBot: [void@puppet181] Upgraded packages on os162: libgnutls30t64
* 01:41 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask181: libgnutls30t64
* 01:40 MirahezeLSBot: [void@puppet181] Upgraded packages on phorge171: libgnutls30t64
* 01:40 MirahezeLSBot: [void@puppet181] Upgraded packages on prometheus151: libgnutls30t64
* 01:40 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask171: libgnutls30t64
* 01:40 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask151: libgnutls30t64
* 01:39 MirahezeLSBot: [void@puppet181] Upgraded packages on ns1: libgnutls30t64
* 01:39 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask161: libgnutls30t64
* 01:39 MirahezeLSBot: [void@puppet181] Upgraded packages on mw202: libgnutls30t64
* 01:39 MirahezeLSBot: [void@puppet181] Upgraded packages on mw203: libgnutls30t64
* 01:38 MirahezeLSBot: [void@puppet181] Upgraded packages on mw201: libgnutls30t64
* 01:38 MirahezeLSBot: [void@puppet181] Upgraded packages on mw182: libgnutls30t64
* 01:38 MirahezeLSBot: [void@puppet181] Upgraded packages on mw193: libgnutls30t64
* 01:37 MirahezeLSBot: [void@puppet181] Upgraded packages on mw183: libgnutls30t64
* 01:37 MirahezeLSBot: [void@puppet181] Upgraded packages on mw173: libgnutls30t64
* 01:37 MirahezeLSBot: [void@puppet181] Upgraded packages on mw192: libgnutls30t64
* 01:37 MirahezeLSBot: [void@puppet181] Upgraded packages on mw181: libgnutls30t64
* 01:36 MirahezeLSBot: [void@puppet181] Upgraded packages on mw191: libgnutls30t64
* 01:36 MirahezeLSBot: [void@puppet181] Upgraded packages on mw171: libgnutls30t64
* 01:36 MirahezeLSBot: [void@puppet181] Upgraded packages on mw172: libgnutls30t64
* 01:35 MirahezeLSBot: [void@puppet181] Upgraded packages on mw163: libgnutls30t64
* 01:35 MirahezeLSBot: [void@puppet181] Upgraded packages on mw161: libgnutls30t64
* 01:35 MirahezeLSBot: [void@puppet181] Upgraded packages on mw162: libgnutls30t64
* 01:34 MirahezeLSBot: [void@puppet181] Upgraded packages on mw153: libgnutls30t64
* 01:34 MirahezeLSBot: [void@puppet181] Upgraded packages on mon181: libgnutls30t64
* 01:34 MirahezeLSBot: [void@puppet181] Upgraded packages on mw151: libgnutls30t64
* 01:34 MirahezeLSBot: [void@puppet181] Upgraded packages on mw152: libgnutls30t64
* 01:33 MirahezeLSBot: [void@puppet181] Upgraded packages on mem191: libgnutls30t64
* 01:33 MirahezeLSBot: [void@puppet181] Upgraded packages on llm191: libgnutls30t64
* 01:33 MirahezeLSBot: [void@puppet181] Upgraded packages on mem201: libgnutls30t64
* 01:33 MirahezeLSBot: [void@puppet181] Upgraded packages on mem161: libgnutls30t64
* 01:32 MirahezeLSBot: [void@puppet181] Upgraded packages on mem151: libgnutls30t64
* 01:32 MirahezeLSBot: [void@puppet181] Upgraded packages on kafka182: libgnutls30t64
* 01:32 MirahezeLSBot: [void@puppet181] Upgraded packages on matomo151: libgnutls30t64
* 01:32 MirahezeLSBot: [void@puppet181] Upgraded packages on ldap171: libgnutls30t64
* 01:31 MirahezeLSBot: [void@puppet181] Upgraded packages on mattermost2: libgnutls30t64
* 01:31 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud19: libgnutls-dane0t64, libgnutls30t64, and gnutls-bin
* 01:31 MirahezeLSBot: [void@puppet181] Upgraded packages on db192: libgnutls30t64
* 01:31 MirahezeLSBot: [void@puppet181] Upgraded packages on cp201: libgnutls30t64
* 01:30 MirahezeLSBot: [void@puppet181] Upgraded packages on eventgate182: libgnutls30t64
* 01:30 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud20: libgnutls-dane0t64, libgnutls30t64, and gnutls-bin
* 01:30 MirahezeLSBot: [void@puppet181] Upgraded packages on db181: libgnutls30t64
* 01:29 MirahezeLSBot: [void@puppet181] Upgraded packages on graylog161: libgnutls30t64
* 01:29 MirahezeLSBot: [void@puppet181] Upgraded packages on db201: libgnutls30t64
* 01:29 MirahezeLSBot: [void@puppet181] Upgraded packages on cp171: libgnutls30t64
* 01:29 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud16: libgnutls-dane0t64, libgnutls30t64, and gnutls-bin
* 01:28 MirahezeLSBot: [void@puppet181] Upgraded packages on db182: libgnutls30t64
* 01:28 MirahezeLSBot: [void@puppet181] Upgraded packages on db161: libgnutls30t64
* 01:28 MirahezeLSBot: [void@puppet181] Upgraded packages on db151: libgnutls30t64
* 01:28 MirahezeLSBot: [void@puppet181] Upgraded packages on db171: libgnutls30t64
* 01:27 MirahezeLSBot: [void@puppet181] Upgraded packages on changeprop202: libgnutls30t64
* 01:27 MirahezeLSBot: [void@puppet181] Upgraded packages on bast181: libgnutls30t64
* 01:27 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud15: libgnutls-dane0t64, libgnutls30t64, and gnutls-bin
* 01:27 MirahezeLSBot: [void@puppet181] Upgraded packages on cp161: libgnutls30t64
* 01:26 MirahezeLSBot: [void@puppet181] Upgraded packages on cp191: libgnutls30t64
* 01:26 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud18: libgnutls-dane0t64, libgnutls30t64, and gnutls-bin
* 01:26 MirahezeLSBot: [void@puppet181] Upgraded packages on bots171: libgnutls30t64
* 01:26 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud17: libgnutls-dane0t64, libgnutls30t64, and gnutls-bin
* 01:25 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud21: libgnutls-dane0t64, libgnutls30t64, and gnutls-bin
* 01:25 MirahezeLSBot: [void@puppet181] Upgraded packages on db172: libgnutls30t64
* 01:25 MirahezeLSBot: [void@puppet181] Upgraded packages on bast161: libgnutls30t64

## 2026-05-19 

* 23:07 MirahezeLSBot: [somerandomdeveloper@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 23s
* 23:07 MirahezeLSBot: [somerandomdeveloper@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 22:09 MirahezeLSBot: [wwr@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php ManageWiki:PopulateWikiSettings --wiki=loginwiki --setting=wgTitleIcon_CSSSelector --sourcelist=titleicon.txt (END - exit=0)
* 22:08 MirahezeLSBot: [wwr@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php ManageWiki:PopulateWikiSettings --wiki=loginwiki --setting=wgTitleIcon_CSSSelector sourcelist=titleicon.txt (END - exit=256)
* 20:47 MirahezeLSBot: [wwr@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 25s
* 20:47 MirahezeLSBot: [wwr@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 20:46 MirahezeLSBot: [wwr@test151] finished deploy of {'pull': 'config', 'config': True} to test151 - SUCCESS in 1s
* 20:46 MirahezeLSBot: [wwr@test151] starting deploy of {'pull': 'config', 'config': True} to test151
* 20:28 MirahezeLSBot: [wwr@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 20:28 MirahezeLSBot: [wwr@test151] starting deploy of {'config': True} to test151
* 20:23 MirahezeLSBot: [wwr@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 20:23 MirahezeLSBot: [wwr@test151] starting deploy of {'config': True} to test151
* 04:14 MirahezeLSBot: [void@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 25s
* 04:13 MirahezeLSBot: [void@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all

## 2026-05-18 

* 23:49 MirahezeLSBot: [void@db172] deleted mariadb full backup from June 2025
* 17:34 RhinosF1: doing a deploy
* 01:59 MirahezeLSBot: [petramagna@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php Bucket:CreateInitialSchemaForBucketIssues --wiki=sagan4alphawiki (END - exit=0)

## 2026-05-17 

* 19:08 MirahezeLSBot: [void@puppet181] Upgraded packages on test151: redis-server and redis-tools
* 19:08 MirahezeLSBot: [void@puppet181] Upgraded packages on rdb191: redis-server and redis-tools
* 19:07 MirahezeLSBot: [void@puppet181] Upgraded packages on changeprop202: redis-server and redis-tools
* 19:07 MirahezeLSBot: [void@puppet181] Upgraded packages on matomo151: redis-server and redis-tools

## 2026-05-16 

* 20:00 MirahezeLSBot: [void@puppet181] Upgraded packages on puppet181: nginx and nginx-common
* 19:59 MirahezeLSBot: [void@puppet181] Upgraded packages on cp161: nginx and nginx-common
* 19:50 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftproxy161: nginx and nginx-common
* 19:49 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftproxy171: nginx and nginx-common
* 19:49 MirahezeLSBot: [void@puppet181] Upgraded packages on phorge171: nginx and nginx-common
* 19:49 MirahezeLSBot: [void@puppet181] Upgraded packages on reports171: nginx and nginx-common
* 19:48 MirahezeLSBot: [void@puppet181] Upgraded packages on test151: nginx and nginx-common
* 19:48 MirahezeLSBot: [void@puppet181] Upgraded packages on os202: nginx and nginx-common
* 19:47 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask181: modsecurity-crs, nginx, and nginx-common
* 19:47 MirahezeLSBot: [void@puppet181] Upgraded packages on os162: nginx and nginx-common
* 19:46 MirahezeLSBot: [void@puppet181] Upgraded packages on os151: nginx and nginx-common
* 19:46 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask171: nginx and nginx-common
* 19:46 MirahezeLSBot: [void@puppet181] Upgraded packages on graylog161: nginx and nginx-common
* 19:45 MirahezeLSBot: [void@puppet181] Upgraded packages on mw191: nginx and nginx-common
* 19:44 MirahezeLSBot: [void@puppet181] Upgraded packages on mon181: nginx and nginx-common
* 19:44 MirahezeLSBot: [void@puppet181] Upgraded packages on llm191: nginx and nginx-common
* 19:44 MirahezeLSBot: [void@puppet181] Upgraded packages on mw183: nginx and nginx-common
* 19:43 MirahezeLSBot: [void@puppet181] Upgraded packages on mw182: nginx and nginx-common
* 19:42 MirahezeLSBot: [void@puppet181] Upgraded packages on mw193: nginx and nginx-common
* 19:41 MirahezeLSBot: [void@puppet181] Upgraded packages on mw203: nginx and nginx-common
* 19:41 MirahezeLSBot: [void@puppet181] Upgraded packages on mw202: nginx and nginx-common
* 19:40 MirahezeLSBot: [void@puppet181] Upgraded packages on mw201: nginx and nginx-common
* 19:39 MirahezeLSBot: [void@puppet181] Upgraded packages on mw192: nginx and nginx-common
* 19:38 MirahezeLSBot: [void@puppet181] Upgraded packages on matomo151: nginx and nginx-common
* 19:38 MirahezeLSBot: [void@puppet181] Upgraded packages on mw173: nginx and nginx-common
* 19:37 MirahezeLSBot: [void@puppet181] Upgraded packages on mw181: nginx and nginx-common
* 19:36 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask151: nginx and nginx-common
* 19:36 MirahezeLSBot: [void@puppet181] Upgraded packages on mw172: nginx and nginx-common
* 19:35 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask161: nginx and nginx-common
* 19:34 MirahezeLSBot: [void@puppet181] Upgraded packages on mw153: nginx and nginx-common
* 19:34 MirahezeLSBot: [void@puppet181] Upgraded packages on mw161: nginx and nginx-common
* 19:33 MirahezeLSBot: [void@puppet181] Upgraded packages on mw151: nginx and nginx-common
* 19:32 MirahezeLSBot: [void@puppet181] Upgraded packages on mw152: nginx and nginx-common
* 19:31 MirahezeLSBot: [void@puppet181] Upgraded packages on mw162: nginx and nginx-common
* 19:30 MirahezeLSBot: [void@puppet181] Upgraded packages on mw171: nginx and nginx-common
* 19:30 MirahezeLSBot: [void@puppet181] Upgraded packages on mw163: nginx and nginx-common
* 19:29 MirahezeLSBot: [void@puppet181] Upgraded packages on mattermost2: nginx and nginx-common
* 08:50 MirahezeLSBot: [petramagna@test151] finished deploy of {'folders': '1.46/extensions/ManageWiki'} to test151 - SUCCESS in 0s
* 08:50 MirahezeLSBot: [petramagna@test151] starting deploy of {'folders': '1.46/extensions/ManageWiki'} to test151
* 08:48 MirahezeLSBot: [petramagna@test151] finished deploy of {'folders': '1.46/extensions/ManageWiki'} to test151 - SUCCESS in 0s
* 08:48 MirahezeLSBot: [petramagna@test151] starting deploy of {'folders': '1.46/extensions/ManageWiki'} to test151
* 08:40 MirahezeLSBot: [petramagna@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 08:40 MirahezeLSBot: [petramagna@test151] starting deploy of {'config': True} to test151
* 08:32 MirahezeLSBot: [petramagna@test151] finished deploy of {'folders': '1.46/extensions/ManageWiki'} to test151 - SUCCESS in 0s
* 08:32 MirahezeLSBot: [petramagna@test151] starting deploy of {'folders': '1.46/extensions/ManageWiki'} to test151
* 02:11 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject181: libopenjp2-7
* 02:10 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject201: libopenjp2-7
* 02:10 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject191: libopenjp2-7
* 02:10 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftproxy171: libopenjp2-7
* 02:09 MirahezeLSBot: [void@puppet181] Upgraded packages on test151: libopenjp2-7
* 02:09 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftproxy161: libopenjp2-7
* 02:09 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject171: libopenjp2-7
* 02:09 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject211: libopenjp2-7
* 02:08 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask181: libopenjp2-7
* 02:08 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftac171: libopenjp2-7
* 02:08 MirahezeLSBot: [void@puppet181] Upgraded packages on mw183: libopenjp2-7
* 02:08 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject161: libopenjp2-7
* 02:07 MirahezeLSBot: [void@puppet181] Upgraded packages on mw203: libopenjp2-7
* 02:07 MirahezeLSBot: [void@puppet181] Upgraded packages on mw152: libopenjp2-7
* 02:07 MirahezeLSBot: [void@puppet181] Upgraded packages on mw201: libopenjp2-7
* 02:06 MirahezeLSBot: [void@puppet181] Upgraded packages on mw171: libopenjp2-7
* 02:06 MirahezeLSBot: [void@puppet181] Upgraded packages on mw151: libopenjp2-7
* 02:06 MirahezeLSBot: [void@puppet181] Upgraded packages on mw192: libopenjp2-7
* 02:06 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask151: libopenjp2-7
* 02:05 MirahezeLSBot: [void@puppet181] Upgraded packages on mw181: libopenjp2-7
* 02:05 MirahezeLSBot: [void@puppet181] Upgraded packages on mw163: libopenjp2-7
* 02:05 MirahezeLSBot: [void@puppet181] Upgraded packages on mw172: libopenjp2-7
* 02:04 MirahezeLSBot: [void@puppet181] Upgraded packages on mw193: libopenjp2-7
* 02:04 MirahezeLSBot: [void@puppet181] Upgraded packages on mw173: libopenjp2-7
* 02:04 MirahezeLSBot: [void@puppet181] Upgraded packages on mw182: libopenjp2-7
* 02:04 MirahezeLSBot: [void@puppet181] Upgraded packages on mw202: libopenjp2-7
* 02:03 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask171: libopenjp2-7
* 02:03 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask161: libopenjp2-7
* 02:03 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject151: libopenjp2-7
* 02:03 MirahezeLSBot: [void@puppet181] Upgraded packages on mw191: libopenjp2-7
* 02:02 MirahezeLSBot: [void@puppet181] Upgraded packages on mw153: libopenjp2-7
* 02:02 MirahezeLSBot: [void@puppet181] Upgraded packages on mw162: libopenjp2-7
* 02:02 MirahezeLSBot: [void@puppet181] Upgraded packages on mw161: libopenjp2-7
* 02:01 MirahezeLSBot: [void@puppet181] Upgraded packages on bots171: libopenjp2-7

## 2026-05-15 

* 23:37 SomeRandomDeveloper: repool c2
* 23:37 MirahezeLSBot: [somerandomdeveloper@mwtask181] finished deploy of {'config': True, 'force': True} to all - SUCCESS in 18s
* 23:37 MirahezeLSBot: [somerandomdeveloper@mwtask181] starting deploy of {'config': True, 'force': True} to all
* 23:31 SomeRandomDeveloper: depool c2
* 23:31 MirahezeLSBot: [somerandomdeveloper@mwtask181] finished deploy of {'config': True, 'force': True} to all - SUCCESS in 20s
* 23:31 MirahezeLSBot: [somerandomdeveloper@mwtask181] starting deploy of {'config': True, 'force': True} to all
* 20:44 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject201: linux-libc-dev
* 20:44 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftproxy161: linux-libc-dev
* 20:43 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject191: linux-libc-dev
* 20:43 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftproxy171: linux-libc-dev
* 20:43 MirahezeLSBot: [void@puppet181] Upgraded packages on test151: linux-libc-dev
* 20:43 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject181: linux-libc-dev
* 20:42 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject211: linux-libc-dev
* 20:42 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject171: linux-libc-dev
* 20:42 MirahezeLSBot: [void@puppet181] Upgraded packages on ns2: linux-libc-dev
* 20:42 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftac171: linux-libc-dev
* 20:41 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject161: linux-libc-dev
* 20:41 MirahezeLSBot: [void@puppet181] Upgraded packages on os201: linux-libc-dev
* 20:41 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject151: linux-libc-dev
* 20:41 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask181: linux-libc-dev
* 20:40 MirahezeLSBot: [void@puppet181] Upgraded packages on os191: linux-libc-dev
* 20:40 MirahezeLSBot: [void@puppet181] Upgraded packages on phorge171: linux-libc-dev
* 20:40 MirahezeLSBot: [void@puppet181] Upgraded packages on os162: linux-libc-dev
* 20:40 MirahezeLSBot: [void@puppet181] Upgraded packages on reports171: linux-libc-dev
* 20:39 MirahezeLSBot: [void@puppet181] Upgraded packages on puppet181: linux-libc-dev
* 20:39 MirahezeLSBot: [void@puppet181] Upgraded packages on os202: linux-libc-dev
* 20:39 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask171: linux-libc-dev
* 20:38 MirahezeLSBot: [void@puppet181] Upgraded packages on os151: linux-libc-dev
* 20:38 MirahezeLSBot: [void@puppet181] Upgraded packages on prometheus151: linux-libc-dev
* 20:38 MirahezeLSBot: [void@puppet181] Upgraded packages on os161: linux-libc-dev
* 20:38 MirahezeLSBot: [void@puppet181] Upgraded packages on rdb191: linux-libc-dev
* 20:37 MirahezeLSBot: [void@puppet181] Upgraded packages on ns1: linux-libc-dev
* 20:37 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask161: linux-libc-dev
* 20:37 MirahezeLSBot: [void@puppet181] Upgraded packages on mw203: linux-libc-dev
* 20:37 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask151: linux-libc-dev
* 20:37 MirahezeLSBot: [void@puppet181] Upgraded packages on mw202: linux-libc-dev
* 20:36 MirahezeLSBot: [void@puppet181] Upgraded packages on mw193: linux-libc-dev
* 20:36 MirahezeLSBot: [void@puppet181] Upgraded packages on mw201: linux-libc-dev
* 20:36 MirahezeLSBot: [void@puppet181] Upgraded packages on mw192: linux-libc-dev
* 20:35 MirahezeLSBot: [void@puppet181] Upgraded packages on mw183: linux-libc-dev
* 20:35 MirahezeLSBot: [void@puppet181] Upgraded packages on mw191: linux-libc-dev
* 20:35 MirahezeLSBot: [void@puppet181] Upgraded packages on mw182: linux-libc-dev
* 20:35 MirahezeLSBot: [void@puppet181] Upgraded packages on mw181: linux-libc-dev
* 20:34 MirahezeLSBot: [void@puppet181] Upgraded packages on mw173: linux-libc-dev
* 20:34 MirahezeLSBot: [void@puppet181] Upgraded packages on mw172: linux-libc-dev
* 20:34 MirahezeLSBot: [void@puppet181] Upgraded packages on mw163: linux-libc-dev
* 20:34 MirahezeLSBot: [void@puppet181] Upgraded packages on mw171: linux-libc-dev
* 20:33 MirahezeLSBot: [void@puppet181] Upgraded packages on mw162: linux-libc-dev
* 20:33 MirahezeLSBot: [void@puppet181] Upgraded packages on mw161: linux-libc-dev
* 20:33 MirahezeLSBot: [void@puppet181] Upgraded packages on mw153: linux-libc-dev
* 20:32 MirahezeLSBot: [void@puppet181] Upgraded packages on mon181: linux-libc-dev
* 20:32 MirahezeLSBot: [void@puppet181] Upgraded packages on mem191: linux-libc-dev
* 20:32 MirahezeLSBot: [void@puppet181] Upgraded packages on db201: linux-libc-dev
* 20:31 MirahezeLSBot: [void@puppet181] Upgraded packages on mw151: linux-libc-dev
* 20:31 MirahezeLSBot: [void@puppet181] Upgraded packages on mw152: linux-libc-dev
* 20:31 MirahezeLSBot: [void@puppet181] Upgraded packages on changeprop202: linux-libc-dev
* 20:30 MirahezeLSBot: [void@puppet181] Upgraded packages on llm191: linux-libc-dev
* 20:30 MirahezeLSBot: [void@puppet181] Upgraded packages on mem201: linux-libc-dev
* 20:30 MirahezeLSBot: [void@puppet181] Upgraded packages on mem161: linux-libc-dev
* 20:30 MirahezeLSBot: [void@puppet181] Upgraded packages on mem151: linux-libc-dev
* 20:30 MirahezeLSBot: [void@puppet181] Upgraded packages on matomo151: linux-libc-dev
* 20:29 MirahezeLSBot: [void@puppet181] Upgraded packages on kafka182: linux-libc-dev
* 20:29 MirahezeLSBot: [void@puppet181] Upgraded packages on ldap171: linux-libc-dev
* 20:29 MirahezeLSBot: [void@puppet181] Upgraded packages on mattermost2: linux-libc-dev
* 20:29 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud19: linux-libc-dev, libcpupower1, and linux-cpupower
* 20:28 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud18: linux-libc-dev, libcpupower1, and linux-cpupower
* 20:28 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud20: linux-libc-dev, libcpupower1, and linux-cpupower
* 20:28 MirahezeLSBot: [void@puppet181] Upgraded packages on db181: linux-libc-dev
* 20:27 MirahezeLSBot: [void@puppet181] Upgraded packages on cp191: linux-libc-dev
* 20:27 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud17: linux-libc-dev, libcpupower1, and linux-cpupower
* 20:27 MirahezeLSBot: [void@puppet181] Upgraded packages on cp201: linux-libc-dev
* 20:27 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud16: linux-libc-dev, libcpupower1, and linux-cpupower
* 20:26 MirahezeLSBot: [void@puppet181] Upgraded packages on graylog161: linux-libc-dev
* 20:26 MirahezeLSBot: [void@puppet181] Upgraded packages on cp171: linux-libc-dev
* 20:26 MirahezeLSBot: [void@puppet181] Upgraded packages on eventgate182: linux-libc-dev
* 20:26 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud15: linux-libc-dev, libcpupower1, and linux-cpupower
* 20:26 MirahezeLSBot: [void@puppet181] Upgraded packages on db182: linux-libc-dev
* 20:25 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud21: linux-libc-dev, libcpupower1, and linux-cpupower
* 20:25 MirahezeLSBot: [void@puppet181] Upgraded packages on bast181: linux-libc-dev
* 20:25 MirahezeLSBot: [void@puppet181] Upgraded packages on bast161: linux-libc-dev
* 20:25 MirahezeLSBot: [void@puppet181] Upgraded packages on db151: linux-libc-dev
* 20:24 MirahezeLSBot: [void@puppet181] Upgraded packages on db161: linux-libc-dev
* 20:24 MirahezeLSBot: [void@puppet181] Upgraded packages on db192: linux-libc-dev
* 20:24 MirahezeLSBot: [void@puppet181] Upgraded packages on db171: linux-libc-dev
* 20:24 MirahezeLSBot: [void@puppet181] Upgraded packages on cp161: linux-libc-dev
* 20:23 MirahezeLSBot: [void@puppet181] Upgraded packages on bots171: linux-libc-dev
* 20:23 MirahezeLSBot: [void@puppet181] Upgraded packages on db172: linux-libc-dev

## 2026-05-14 

* 21:41 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftproxy161: libnghttp2-14 and libpq5
* 21:41 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject201: libnghttp2-14 and libpq5
* 21:41 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftproxy171: libnghttp2-14 and libpq5
* 21:40 MirahezeLSBot: [void@puppet181] Upgraded packages on test151: libswscale8, libavdevice61, libavformat61, libavfilter10, libavcodec61, libavutil59, libpostproc58, libswresample5, ffmpeg, libnghttp2-dev, nghttp2-client, libnghttp2-14, and libpq5
* 21:40 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject211: libnghttp2-14 and libpq5
* 21:40 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject191: libnghttp2-14 and libpq5
* 21:39 MirahezeLSBot: [void@puppet181] Upgraded packages on ns2: libnghttp2-14 and libpq5
* 21:39 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject181: libnghttp2-14 and libpq5
* 21:39 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject171: libnghttp2-14 and libpq5
* 21:39 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject161: libnghttp2-14 and libpq5
* 21:38 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftac171: libnghttp2-14 and libpq5
* 21:38 MirahezeLSBot: [void@puppet181] Upgraded packages on rdb191: libnghttp2-14 and libpq5
* 21:38 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject151: libnghttp2-14 and libpq5
* 21:38 MirahezeLSBot: [void@puppet181] Upgraded packages on os202: libnghttp2-14 and libpq5
* 21:37 MirahezeLSBot: [void@puppet181] Upgraded packages on os201: libnghttp2-14 and libpq5
* 21:37 MirahezeLSBot: [void@puppet181] Upgraded packages on puppet181: gsasl-common, libgsasl18, libnghttp2-14, libpq5, postgresql-client-17, and postgresql-17
* 21:37 MirahezeLSBot: [void@puppet181] Upgraded packages on os162: libnghttp2-14 and libpq5
* 21:36 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask181: libswscale8, libavdevice61, libavformat61, libavfilter10, libavcodec61, libavutil59, libpostproc58, libswresample5, ffmpeg, libnghttp2-14, and libpq5
* 21:36 MirahezeLSBot: [void@puppet181] Upgraded packages on reports171: libnghttp2-14 and libpq5
* 21:36 MirahezeLSBot: [void@puppet181] Upgraded packages on os191: libnghttp2-14 and libpq5
* 21:36 MirahezeLSBot: [void@puppet181] Upgraded packages on prometheus151: libnghttp2-14 and libpq5
* 21:35 MirahezeLSBot: [void@puppet181] Upgraded packages on phorge171: libnghttp2-14 and libpq5
* 21:35 MirahezeLSBot: [void@puppet181] Upgraded packages on os161: libnghttp2-14 and libpq5
* 21:35 MirahezeLSBot: [void@puppet181] Upgraded packages on ns1: libnghttp2-14 and libpq5
* 21:35 MirahezeLSBot: [void@puppet181] Upgraded packages on mw203: libswscale8, libavdevice61, libavformat61, libavfilter10, libavcodec61, libavutil59, libpostproc58, libswresample5, ffmpeg, libnghttp2-14, and libpq5
* 21:34 MirahezeLSBot: [void@puppet181] Upgraded packages on os151: libnghttp2-14 and libpq5
* 21:34 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask171: libswscale8, libavdevice61, libavformat61, libavfilter10, libavcodec61, libavutil59, libpostproc58, libswresample5, ffmpeg, libnghttp2-14, and libpq5
* 21:34 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask151: libswscale8, libavdevice61, libavformat61, libavfilter10, libavcodec61, libavutil59, libpostproc58, libswresample5, ffmpeg, libnghttp2-14, and libpq5
* 21:34 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask161: libswscale8, libavdevice61, libavformat61, libavfilter10, libavcodec61, libavutil59, libpostproc58, libswresample5, ffmpeg, libnghttp2-14, and libpq5
* 21:33 MirahezeLSBot: [void@puppet181] Upgraded packages on mw202: libswscale8, libavdevice61, libavformat61, libavfilter10, libavcodec61, libavutil59, libpostproc58, libswresample5, ffmpeg, libnghttp2-14, and libpq5
* 21:33 MirahezeLSBot: [void@puppet181] Upgraded packages on mw201: libswscale8, libavdevice61, libavformat61, libavfilter10, libavcodec61, libavutil59, libpostproc58, libswresample5, ffmpeg, libnghttp2-14, and libpq5
* 21:33 MirahezeLSBot: [void@puppet181] Upgraded packages on mw192: libswscale8, libavdevice61, libavformat61, libavfilter10, libavcodec61, libavutil59, libpostproc58, libswresample5, ffmpeg, libnghttp2-14, and libpq5
* 21:32 MirahezeLSBot: [void@puppet181] Upgraded packages on mw191: libswscale8, libavdevice61, libavformat61, libavfilter10, libavcodec61, libavutil59, libpostproc58, libswresample5, ffmpeg, libnghttp2-14, and libpq5
* 21:32 MirahezeLSBot: [void@puppet181] Upgraded packages on mw181: libswscale8, libavdevice61, libavformat61, libavfilter10, libavcodec61, libavutil59, libpostproc58, libswresample5, ffmpeg, libnghttp2-14, and libpq5
* 21:32 MirahezeLSBot: [void@puppet181] Upgraded packages on mw183: libswscale8, libavdevice61, libavformat61, libavfilter10, libavcodec61, libavutil59, libpostproc58, libswresample5, ffmpeg, libnghttp2-14, and libpq5
* 21:31 MirahezeLSBot: [void@puppet181] Upgraded packages on mw193: libswscale8, libavdevice61, libavformat61, libavfilter10, libavcodec61, libavutil59, libpostproc58, libswresample5, ffmpeg, libnghttp2-14, and libpq5
* 21:31 MirahezeLSBot: [void@puppet181] Upgraded packages on mw182: libswscale8, libavdevice61, libavformat61, libavfilter10, libavcodec61, libavutil59, libpostproc58, libswresample5, ffmpeg, libnghttp2-14, and libpq5
* 21:31 MirahezeLSBot: [void@puppet181] Upgraded packages on mw163: libswscale8, libavdevice61, libavformat61, libavfilter10, libavcodec61, libavutil59, libpostproc58, libswresample5, ffmpeg, libnghttp2-14, and libpq5
* 21:30 MirahezeLSBot: [void@puppet181] Upgraded packages on mw173: libswscale8, libavdevice61, libavformat61, libavfilter10, libavcodec61, libavutil59, libpostproc58, libswresample5, ffmpeg, libnghttp2-14, and libpq5
* 21:30 MirahezeLSBot: [void@puppet181] Upgraded packages on mw171: libswscale8, libavdevice61, libavformat61, libavfilter10, libavcodec61, libavutil59, libpostproc58, libswresample5, ffmpeg, libnghttp2-14, and libpq5
* 21:30 MirahezeLSBot: [void@puppet181] Upgraded packages on mw161: libswscale8, libavdevice61, libavformat61, libavfilter10, libavcodec61, libavutil59, libpostproc58, libswresample5, ffmpeg, libnghttp2-14, and libpq5
* 21:29 MirahezeLSBot: [void@puppet181] Upgraded packages on mw162: libswscale8, libavdevice61, libavformat61, libavfilter10, libavcodec61, libavutil59, libpostproc58, libswresample5, ffmpeg, libnghttp2-14, and libpq5
* 21:29 MirahezeLSBot: [void@puppet181] Upgraded packages on mw153: libswscale8, libavdevice61, libavformat61, libavfilter10, libavcodec61, libavutil59, libpostproc58, libswresample5, ffmpeg, libnghttp2-14, and libpq5
* 21:29 MirahezeLSBot: [void@puppet181] Upgraded packages on mw151: libswscale8, libavdevice61, libavformat61, libavfilter10, libavcodec61, libavutil59, libpostproc58, libswresample5, ffmpeg, libnghttp2-14, and libpq5
* 21:28 MirahezeLSBot: [void@puppet181] Upgraded packages on mon181: libnghttp2-14 and libpq5
* 21:28 MirahezeLSBot: [void@puppet181] Upgraded packages on mw172: libswscale8, libavdevice61, libavformat61, libavfilter10, libavcodec61, libavutil59, libpostproc58, libswresample5, ffmpeg, libnghttp2-14, and libpq5
* 21:28 MirahezeLSBot: [void@puppet181] Upgraded packages on mw152: libswscale8, libavdevice61, libavformat61, libavfilter10, libavcodec61, libavutil59, libpostproc58, libswresample5, ffmpeg, libnghttp2-14, and libpq5
* 21:28 MirahezeLSBot: [void@puppet181] Upgraded packages on mem191: libnghttp2-14 and libpq5
* 21:27 MirahezeLSBot: [void@puppet181] Upgraded packages on llm191: libnghttp2-14 and libpq5
* 21:27 MirahezeLSBot: [void@puppet181] Upgraded packages on mem201: libnghttp2-14 and libpq5
* 21:27 MirahezeLSBot: [void@puppet181] Upgraded packages on kafka182: libnghttp2-14 and libpq5
* 21:27 MirahezeLSBot: [void@puppet181] Upgraded packages on mem161: libnghttp2-14 and libpq5
* 21:26 MirahezeLSBot: [void@puppet181] Upgraded packages on mem151: libnghttp2-14 and libpq5
* 21:26 MirahezeLSBot: [void@puppet181] Upgraded packages on ldap171: libnghttp2-14 and libpq5
* 21:26 MirahezeLSBot: [void@puppet181] Upgraded packages on matomo151: libnghttp2-14 and libpq5
* 21:26 MirahezeLSBot: [void@puppet181] Upgraded packages on mattermost2: libnghttp2-14, libpq5, postgresql-client-17, and postgresql-17
* 21:25 MirahezeLSBot: [void@puppet181] Upgraded packages on cp191: libnghttp2-14 and libpq5
* 21:25 MirahezeLSBot: [void@puppet181] Upgraded packages on db201: libnghttp2-14 and libpq5
* 21:25 MirahezeLSBot: [void@puppet181] Upgraded packages on db192: libnghttp2-14 and libpq5
* 21:25 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud17: libnghttp2-14 and libpq5
* 21:24 MirahezeLSBot: [void@puppet181] Upgraded packages on cp171: libnghttp2-14 and libpq5
* 21:24 MirahezeLSBot: [void@puppet181] Upgraded packages on eventgate182: libnghttp2-14 and libpq5
* 21:24 MirahezeLSBot: [void@puppet181] Upgraded packages on bast181: libnghttp2-14 and libpq5
* 21:24 MirahezeLSBot: [void@puppet181] Upgraded packages on graylog161: libnghttp2-14 and libpq5
* 21:23 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud19: libnghttp2-14 and libpq5
* 21:23 MirahezeLSBot: [void@cloud21] clear ipmi server event log (inlet temperature going high again)
* 21:23 MirahezeLSBot: [void@puppet181] Upgraded packages on changeprop202: libnghttp2-14 and libpq5
* 21:23 MirahezeLSBot: [void@puppet181] Upgraded packages on db181: libnghttp2-14 and libpq5
* 21:23 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud20: libnghttp2-14 and libpq5
* 21:22 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud18: libnghttp2-14 and libpq5
* 21:22 MirahezeLSBot: [void@puppet181] Upgraded packages on db182: libnghttp2-14 and libpq5
* 21:22 MirahezeLSBot: [void@puppet181] Upgraded packages on cp201: libnghttp2-14 and libpq5
* 21:22 MirahezeLSBot: [void@puppet181] Upgraded packages on bast161: libnghttp2-14 and libpq5
* 21:22 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud16: libnghttp2-14 and libpq5
* 21:21 MirahezeLSBot: [void@puppet181] Upgraded packages on cp161: libnghttp2-14 and libpq5
* 21:21 MirahezeLSBot: [void@puppet181] Upgraded packages on db171: libnghttp2-14 and libpq5
* 21:20 MirahezeLSBot: [void@puppet181] Upgraded packages on db172: libnghttp2-14 and libpq5
* 21:20 MirahezeLSBot: [void@puppet181] Upgraded packages on db161: libnghttp2-14 and libpq5
* 21:20 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud15: libnghttp2-14 and libpq5
* 21:20 MirahezeLSBot: [void@puppet181] Upgraded packages on bots171: libnghttp2-14 and libpq5
* 21:20 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud21: libnghttp2-14 and libpq5
* 21:19 MirahezeLSBot: [void@puppet181] Upgraded packages on db151: libnghttp2-14 and libpq5
* 03:54 MirahezeLSBot: [skye@mwtask171] Finished import for kartkingdomwiki (XML: None; Images: .) (END - exit=0)
* 03:54 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php initSiteStats --wiki=kartkingdomwiki --update (END - exit=0)
* 03:54 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php initSiteStats --wiki=kartkingdomwiki --update (START)
* 03:54 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=kartkingdomwiki --sleep=1 '--comment=Importing images from [https://kart-kingdomkarts.fandom.com/](https://kart-kingdomkarts.fandom.com/) ([T15336](https://meta.miraheze.org/wiki/phorge:T15336))' -- . (END - exit=0)
* 01:05 MirahezeLSBot: [skye@mwtask171] Finished import for lapfoxhalleywiki (XML: None; Images: .) (END - exit=0)
* 01:05 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php initSiteStats --wiki=lapfoxhalleywiki --update (END - exit=0)
* 01:05 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php initSiteStats --wiki=lapfoxhalleywiki --update (START)
* 01:05 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=lapfoxhalleywiki --sleep=1 '--comment=Importing files from lapfoxtrax.fandom.com ([T15350](https://meta.miraheze.org/wiki/phorge:T15350))' -- . (END - exit=0)

## 2026-05-13 

* 23:43 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=lapfoxhalleywiki --sleep=1 '--comment=Importing files from lapfoxtrax.fandom.com ([T15350](https://meta.miraheze.org/wiki/phorge:T15350))' -- . (START)
* 23:43 MirahezeLSBot: [skye@mwtask171] Starting import for lapfoxhalleywiki (XML: None; Images: .) (START)
* 23:18 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=kartkingdomwiki --sleep=1 '--comment=Importing images from [https://kart-kingdomkarts.fandom.com/](https://kart-kingdomkarts.fandom.com/) ([T15336](https://meta.miraheze.org/wiki/phorge:T15336))' -- . (START)
* 23:18 MirahezeLSBot: [skye@mwtask171] Starting import for kartkingdomwiki (XML: None; Images: .) (START)

## 2026-05-12 

* 23:09 MirahezeLSBot: [somerandomdeveloper@mwtask181] finished deploy of {'versions': '1.45', 'upgrade_extensions': ['Maps', 'SemanticMediaWiki']} to all - SUCCESS in 55s
* 23:08 MirahezeLSBot: [somerandomdeveloper@mwtask181] starting deploy of {'versions': '1.45', 'upgrade_extensions': ['Maps', 'SemanticMediaWiki']} to all
* 23:08 MirahezeLSBot: [somerandomdeveloper@test151] finished deploy of {'versions': ['1.45', '1.46'], 'upgrade_extensions': ['Maps', 'SemanticMediaWiki']} to test151 - SUCCESS in 1s
* 23:08 MirahezeLSBot: [somerandomdeveloper@test151] starting deploy of {'versions': ['1.45', '1.46'], 'upgrade_extensions': ['Maps', 'SemanticMediaWiki']} to test151
* 22:01 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.46/maintenance/run.php MirahezeMagic:UpgradeWiki --wiki=testwikibeta --json=UpgradeWikiSchema.json (END - exit=0)
* 22:01 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.46/maintenance/run.php MirahezeMagic:UpgradeWiki --wiki=t14400test2wikibeta --json=UpgradeWikiSchema.json (END - exit=0)
* 22:01 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.46/maintenance/run.php MirahezeMagic:UpgradeWiki --wiki=skye69wikibeta --json=UpgradeWikiSchema.json (END - exit=0)
* 22:00 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.46/maintenance/run.php MirahezeMagic:UpgradeWiki --wiki=skye2wikibeta --json=UpgradeWikiSchema.json (END - exit=0)
* 21:59 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.46/maintenance/run.php MirahezeMagic:UpgradeWiki --wiki=atestwikibeta --json=UpgradeWikiSchema.json (END - exit=0)
* 21:59 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.46/maintenance/run.php MirahezeMagic:UpgradeWiki --wiki=exttestwikibeta --json=UpgradeWikiSchema.json (END - exit=0)
* 21:51 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.46/maintenance/run.php TimedMediaHandler:migrateTranscodeStates --wiki=atestwikibeta (END - exit=0)
* 21:49 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.46/maintenance/run.php MirahezeMagic:UpgradeWiki --wiki=atestwikibeta --json=UpgradeWikiSchema.json (END - exit=256)
* 21:46 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.46/maintenance/run.php TimedMediaHandler:MigrateTranscodeStates --wiki=atestwikibeta (END - exit=256)
* 21:22 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.46/maintenance/run.php MirahezeMagic:UpgradeWiki --wiki=atestwikibeta --json=UpgradeWikiSchema.json (END - exit=256)
* 21:17 MirahezeLSBot: [somerandomdeveloper@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 21:17 MirahezeLSBot: [somerandomdeveloper@test151] starting deploy of {'config': True} to test151
* 21:16 MirahezeLSBot: [somerandomdeveloper@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 21:16 MirahezeLSBot: [somerandomdeveloper@test151] starting deploy of {'config': True} to test151
* 15:26 MirahezeLSBot: [skye@mwtask181] finished deploy of {'versions': '1.45', 'upgrade_skins': 'Medik'} to all - SUCCESS in 36s
* 15:26 MirahezeLSBot: [skye@mwtask181] starting deploy of {'versions': '1.45', 'upgrade_skins': 'Medik'} to all
* 15:23 MirahezeLSBot: [skye@test151] finished deploy of {'versions': ['1.45', '1.46'], 'upgrade_skins': 'Medik'} to test151 - SUCCESS in 1s
* 15:23 MirahezeLSBot: [skye@test151] starting deploy of {'versions': ['1.45', '1.46'], 'upgrade_skins': 'Medik'} to test151
* 15:17 MirahezeLSBot: [skye@test151] starting deploy of {'pull': 'config', 'config': True, 'l10n': True, 'extension_list': True, 'force_upgrade': True, 'versions': '1.45', 'upgrade_skins': 'Medik'} to test151
* 15:16 Skye: [skye@test151] sudo -u www-data rm -rf /srv/mediawiki-staging/1.45/skins/Medik/
* 15:12 MirahezeLSBot: [skye@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:ResetWiki --wiki=loginwiki --dbname=b3313wiki --requester=Poxta (END - exit=0)
* 15:08 MirahezeLSBot: [skye@test151] DEPLOY ABORTED: Non-Zero Exit Code in prep, see output.
* 15:08 MirahezeLSBot: [skye@test151] starting deploy of {'versions': ['1.45', '1.46'], 'upgrade_skins': 'Medik'} to test151
* 14:50 MirahezeLSBot: [skye@mwtask181] finished deploy of {'versions': '1.45', 'upgrade_extensions': 'EmbedVideo'} to all - SUCCESS in 27s
* 14:50 MirahezeLSBot: [skye@mwtask181] starting deploy of {'versions': '1.45', 'upgrade_extensions': 'EmbedVideo'} to all
* 14:50 MirahezeLSBot: [skye@test151] finished deploy of {'versions': ['1.45', '1.46'], 'upgrade_extensions': 'EmbedVideo'} to test151 - SUCCESS in 1s
* 14:50 MirahezeLSBot: [skye@test151] starting deploy of {'versions': ['1.45', '1.46'], 'upgrade_extensions': 'EmbedVideo'} to test151
* 01:15 MirahezeLSBot: [wwr@test151] sudo -u www-data /usr/local/bin/foreachwikiindblist ./dblist.php /srv/mediawiki/1.46/maintenance/run.php MirahezeMagic:UpgradeWiki --json=UpgradeWikiSchema.json
* 01:11 MirahezeLSBot: [wwr@test151] sudo -u www-data /usr/local/bin/foreachwikiindblist ./dblist.php /srv/mediawiki/1.46/maintenance/run.php sql wwr-patch-cusi_case.sql
* 01:11 MirahezeLSBot: [wwr@test151] sudo -u www-data /usr/local/bin/foreachwikiindblist ./dblist.php /srv/mediawiki/1.46/maintenance/run.php sql wwr-patch-imagelinks.sql
* 01:08 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.46/maintenance/run.php MirahezeMagic:UpgradeWiki --wiki=loadouttest13wikibeta --json=UpgradeWikiSchema.json (END - exit=0)
* 01:06 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.46/maintenance/run.php MirahezeMagic:UpgradeWiki --wiki=quicktest1wikibeta --json=UpgradeWikiSchema.json (END - exit=0)
* 01:03 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.46/maintenance/run.php MirahezeMagic:UpgradeWiki --wiki=exttestadvancedwikibeta --json=UpgradeWikiSchema.json (END - exit=0)
* 01:00 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.46/maintenance/run.php MirahezeMagic:UpgradeWiki --wiki=cdwikibeta --json=UpgradeWikiSchema.json (END - exit=0)
* 00:59 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.46/maintenance/run.php MirahezeMagic:UpgradeWiki --wiki=cdwikibeta --json=UpgradeWikiSchema.json (END - exit=256)
* 00:58 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.46/maintenance/run.php MirahezeMagic:UpgradeWiki --wiki=cdwikibeta --json=UpgradeWikiSchema.json (END - exit=256)
* 00:54 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.46/maintenance/run.php MirahezeMagic:UpgradeWiki --wiki=testwikibeta2wikibeta --json=UpgradeWikiSchema.json (END - exit=0)
* 00:52 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.46/maintenance/run.php MirahezeMagic:UpgradeWiki --wiki=testwikibeta2wikibeta --json=UpgradeWikiSchema.json (END - exit=256)
* 00:52 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.46/maintenance/run.php MirahezeMagic:UpgradeWiki --wiki=testwikibeta2wikibeta --json=UpgradeWikiSchema.json (END - exit=256)
* 00:51 TheWWRNerdGuy: [wwr@test151] sudo -u www-data /usr/local/bin/foreachwikiindblist ./dblist.php /srv/mediawiki/1.46/maintenance/run.php sql /srv/mediawiki/1.46/extensions/CheckUser/schema/mysql/patch-cusi_user-def.sql
* 00:50 MirahezeLSBot: [wwr@test151] sudo -u www-data /usr/local/bin/foreachwikiindblist ./dblist.php /srv/mediawiki/1.46/maintenance/run.php sql /srv/mediawiki/1.46/extensions/CheckUser/schema/mysql/patch-cusi_signal-def.sql
* 00:43 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.46/maintenance/run.php MirahezeMagic:UpgradeWiki --wiki=testwikibeta2wikibeta --json=UpgradeWikiSchema.json (END - exit=256)
* 00:39 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.46/maintenance/run.php MirahezeMagic:UpgradeWiki --wiki=explodemeeewikibeta --json=UpgradeWikiSchema.json (END - exit=0)
* 00:37 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.46/maintenance/run.php MirahezeMagic:UpgradeWiki --wiki=explodemeeewikibeta --json=UpgradeWikiSchema.json (END - exit=256)
* 00:12 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.46/maintenance/run.php MirahezeMagic:UpgradeWiki --wiki=wwrtest3wikibeta --json=UpgradeWikiSchema.json (END - exit=0)
* 00:11 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.46/maintenance/run.php MirahezeMagic:UpgradeWiki --wiki=wwrtest3wikibeta --json=UpgradeWikiSchema.json (END - exit=256)
* 00:11 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.46/maintenance/run.php MirahezeMagic:UpgradeWiki --wiki=wwrtest3wikibeta --json=UpgradeWikiSchema.json (END - exit=256)
* 00:03 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.46/maintenance/run.php MirahezeMagic:UpgradeWiki --wiki=wwrtest3wikibeta --json=UpgradeWikiSchema.json (END - exit=256)
* 00:02 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.46/maintenance/run.php MirahezeMagic:UpgradeWiki --wiki=wwrtest3wikibeta --json=UpgradeWikiSchema.json (END - exit=256)

## 2026-05-11 

* 23:58 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.46/maintenance/run.php MirahezeMagic:UpgradeWiki --wiki=wwrtest3wikibeta --json=UpgradeWikiSchema.json (END - exit=256)
* 23:55 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.46/maintenance/run.php MirahezeMagic:UpgradeWiki --wiki=wwrtest3wikibeta --json=UpgradeWikiSchema.json (END - exit=256)
* 23:53 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.46/maintenance/run.php MirahezeMagic:UpgradeWiki --wiki=wwrtest3wikibeta --json=UpgradeWikiSchema.json (END - exit=256)
* 23:25 TheWWRNerdGuy: [wwr@test151] sudo -u www-data /usr/local/bin/foreachwikiindblist ./dblist.php /srv/mediawiki/1.46/maintenance/run.php sql /srv/mediawiki/1.46/extensions/CheckUser/schema/mysql/patch-cusi_case-def.sql
* 22:44 TheWWRNerdGuy: [wwr@test151] sudo -u www-data /usr/local/bin/foreachwikiindblist ./dblist.php /srv/mediawiki/1.46/maintenance/run.php MirahezeMagic:UpgradeWiki --json=UpgradeWikiSchema.json
* 22:30 TheWWRNerdGuy: [wwr@test151] sudo -u www-data /usr/local/bin/foreachwikiindblist ./dblist.php /srv/mediawiki/1.46/maintenance/run.php MirahezeMagic:UpgradeWiki --json=UpgradeWikiSchema.json
* 22:24 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.46/maintenance/run.php MirahezeMagic:ChangeMediaWikiVersion --wiki=semanticmediawiki1wikibeta --mwversion=1.46 (END - exit=0)
* 22:24 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.46/maintenance/run.php MirahezeMagic:ChangeMediaWikiVersion --wiki=smwtestwikibeta --mwversion=1.46 (END - exit=0)
* 22:01 MirahezeLSBot: [macfan@test151] finished deploy of {'force_upgrade': True, 'versions': '1.45', 'upgrade_extensions': 'SemanticMediaWiki'} to test151 - SUCCESS in 0s
* 22:01 MirahezeLSBot: [macfan@test151] starting deploy of {'force_upgrade': True, 'versions': '1.45', 'upgrade_extensions': 'SemanticMediaWiki'} to test151
* 21:41 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.46/maintenance/run.php OATHAuth:PopulateUserHandles --wiki=metawikibeta (END - exit=0)
* 21:41 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.46/maintenance/run.php sql --wiki=metawikibeta /srv/mediawiki/1.46/extensions/GlobalBlocking/sql/mysql/patch-globalblocks-modify-gb_address-type.sql --wikidb=testglobal (END - exit=0)
* 21:41 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.46/maintenance/run.php sql --wiki=metawikibeta /srv/mediawiki/1.46/extensions/GlobalBlocking/sql/mysql/patch-globalblocks-add-gb_block_email.sql --wikidb=testglobal (END - exit=0)
* 21:40 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.46/maintenance/run.php sql --wiki=metawikibeta /srv/mediawiki/1.46/extensions/OATHAuth/sql/mysql/patch-add-oathauth_user_handles.sql --wikidb=testglobal (END - exit=0)
* 21:37 MirahezeLSBot: [wwr@test151] sudo -u www-data php /srv/mediawiki/1.46/maintenance/run.php MirahezeMagic:ChangeMediaWikiVersion --wiki=loginwikibeta --mwversion=1.46 --file=dblist.txt (END - exit=0)
* 21:34 MirahezeLSBot: [wwr@test151] finished deploy of {'pull': 'config', 'config': True} to test151 - SUCCESS in 1s
* 21:34 MirahezeLSBot: [wwr@test151] starting deploy of {'pull': 'config', 'config': True} to test151
* 17:25 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php /srv/mediawiki/1.45/maintenance/initSiteStats.php --wiki=b3313wiki --update (END - exit=0)
* 17:25 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php /srv/mediawiki/1.45/maintenance/rebuildall.php --wiki=b3313wiki (END - exit=0)
* 16:51 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php /srv/mediawiki/1.45/maintenance/rebuildall.php --wiki=b3313wiki (START)
* 16:51 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php /srv/mediawiki/1.45/maintenance/importDump.php --wiki=b3313wiki dump.xml --no-updates (END - exit=0)
* 16:50 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php /srv/mediawiki/1.45/maintenance/importDump.php --wiki=b3313wiki dump.xml --no-updates (START)

## 2026-05-10 

* 19:20 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php /srv/mediawiki/1.45/maintenance/initSiteStats.php --wiki=itihasawiki --update (END - exit=0)
* 19:20 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php /srv/mediawiki/1.45/maintenance/rebuildall.php --wiki=itihasawiki (END - exit=0)
* 19:19 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php /srv/mediawiki/1.45/maintenance/rebuildall.php --wiki=itihasawiki (START)
* 19:19 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php /srv/mediawiki/1.45/maintenance/importDump.php --wiki=itihasawiki dump.xml --no-updates (END - exit=0)
* 19:15 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php /srv/mediawiki/1.45/maintenance/importDump.php --wiki=itihasawiki dump.xml --no-updates (START)
* 16:38 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on swiftobject201: liblcms2-2 and libpng16-16t64
* 16:38 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on swiftproxy171: liblcms2-2 and libpng16-16t64
* 16:38 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on swiftproxy161: liblcms2-2 and libpng16-16t64
* 16:38 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on test151: liblcms2-2, libpng-tools, libpng-dev, and libpng16-16t64
* 16:37 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on swiftobject191: liblcms2-2 and libpng16-16t64
* 16:37 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on swiftobject211: liblcms2-2 and libpng16-16t64
* 16:37 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on ns2: liblcms2-2 and libpng16-16t64
* 16:36 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on swiftobject181: liblcms2-2 and libpng16-16t64
* 16:36 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on swiftobject161: liblcms2-2 and libpng16-16t64
* 16:36 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on swiftobject171: liblcms2-2 and libpng16-16t64
* 16:36 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on swiftac171: liblcms2-2 and libpng16-16t64
* 16:35 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on os202: liblcms2-2 and libpng16-16t64
* 16:35 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on swiftobject151: liblcms2-2 and libpng16-16t64
* 16:35 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on os201: liblcms2-2 and libpng16-16t64
* 16:34 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on rdb191: liblcms2-2 and libpng16-16t64
* 16:34 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on reports171: liblcms2-2 and libpng16-16t64
* 16:34 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on puppet181: liblcms2-2 and libpng16-16t64
* 16:34 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on os162: liblcms2-2 and libpng16-16t64
* 16:33 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on phorge171: liblcms2-2 and libpng16-16t64
* 16:33 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on os191: liblcms2-2 and libpng16-16t64
* 16:33 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on os151: liblcms2-2 and libpng16-16t64
* 16:33 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on os161: libpng16-16t64
* 16:32 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on mwtask171: liblcms2-2, libpng-tools, libpng-dev, and libpng16-16t64
* 16:32 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on mwtask181: liblcms2-2, libpng-tools, libpng-dev, and libpng16-16t64
* 16:31 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on mw202: libpng-tools, libpng-dev, and libpng16-16t64
* 16:31 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on mw201: libpng-tools, libpng-dev, and libpng16-16t64
* 16:30 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on mw183: libpng-tools, libpng-dev, and libpng16-16t64
* 16:30 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on mw181: libpng-tools, libpng-dev, and libpng16-16t64
* 16:30 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on mon181: libpng16-16t64
* 16:29 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on mw192: liblcms2-2, libpng-tools, libpng-dev, and libpng16-16t64
* 16:29 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on mw162: libpng-tools, libpng-dev, and libpng16-16t64
* 16:29 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on mw182: libpng-tools, libpng-dev, and libpng16-16t64
* 16:28 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on mw152: libpng-tools, libpng-dev, and libpng16-16t64
* 16:28 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on mw191: liblcms2-2, libpng-tools, libpng-dev, and libpng16-16t64
* 16:28 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on mw151: liblcms2-2, libpng-tools, libpng-dev, and libpng16-16t64
* 16:27 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on mw171: liblcms2-2, libpng-tools, libpng-dev, and libpng16-16t64
* 16:27 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on mw163: liblcms2-2, libpng-tools, libpng-dev, and libpng16-16t64
* 16:27 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on mw153: liblcms2-2, libpng-tools, libpng-dev, and libpng16-16t64
* 16:26 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on mem191: liblcms2-2 and libpng16-16t64
* 16:26 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on mem201: libpng16-16t64
* 16:26 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on mem151: liblcms2-2 and libpng16-16t64
* 16:25 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on matomo151: libpng16-16t64
* 16:25 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on ldap171: libpng16-16t64
* 16:25 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on kafka182: liblcms2-2 and libpng16-16t64
* 16:25 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on mattermost2: libpng16-16t64
* 16:24 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on eventgate182: libpng16-16t64
* 16:24 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on db192: libpng16-16t64
* 16:24 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on graylog161: liblcms2-2 and libpng16-16t64
* 16:23 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on cp191: liblcms2-2 and libpng16-16t64
* 16:23 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on bast181: libpng16-16t64
* 16:23 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on cloud17: libpng16-16t64
* 16:23 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on db181: libpng16-16t64
* 16:22 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on db201: liblcms2-2 and libpng16-16t64
* 16:22 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on db182: liblcms2-2 and libpng16-16t64
* 16:22 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on cloud20: libpng16-16t64
* 16:22 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on cloud18: libpng16-16t64
* 16:21 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on cp201: libpng16-16t64
* 16:21 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on cloud19: liblcms2-2 and libpng16-16t64
* 16:21 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on db151: libpng16-16t64
* 16:21 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on cloud16: libpng16-16t64
* 16:21 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on db172: liblcms2-2 and libpng16-16t64
* 16:20 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on db171: liblcms2-2 and libpng16-16t64
* 16:20 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on bast161: liblcms2-2 and libpng16-16t64
* 16:20 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on changeprop202: libpng16-16t64
* 16:20 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on db161: liblcms2-2 and libpng16-16t64
* 16:19 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on bots171: liblcms2-2 and libpng16-16t64
* 16:19 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on cloud15: liblcms2-2 and libpng16-16t64
* 16:19 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on cloud21: liblcms2-2 and libpng16-16t64
* 16:19 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on cp161: liblcms2-2 and libpng16-16t64
* 16:18 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on ns1: liblcms2-2 and libpng16-16t64
* 16:18 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on prometheus151: liblcms2-2 and libpng16-16t64
* 16:18 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on mw203: liblcms2-2, libpng-tools, libpng-dev, and libpng16-16t64
* 16:18 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on mwtask151: liblcms2-2, libpng-tools, libpng-dev, and libpng16-16t64
* 16:17 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on os161: liblcms2-2
* 16:17 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on mw202: liblcms2-2
* 16:17 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on mwtask161: liblcms2-2, libpng-tools, libpng-dev, and libpng16-16t64
* 16:17 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on mw201: liblcms2-2
* 16:16 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on mw183: liblcms2-2
* 16:16 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on mw193: liblcms2-2, libpng-tools, libpng-dev, and libpng16-16t64
* 16:16 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on mw181: liblcms2-2
* 16:15 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on mw182: liblcms2-2
* 16:15 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on mw173: liblcms2-2, libpng-tools, libpng-dev, and libpng16-16t64
* 16:14 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on mw172: liblcms2-2, libpng-tools, libpng-dev, and libpng16-16t64
* 16:14 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on mw161: liblcms2-2, libpng-tools, libpng-dev, and libpng16-16t64
* 16:13 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on mw162: liblcms2-2
* 16:13 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on mon181: liblcms2-2
* 16:13 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on mw152: liblcms2-2
* 16:12 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on llm191: liblcms2-2 and libpng16-16t64
* 16:12 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on mem201: liblcms2-2
* 16:12 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on mem161: liblcms2-2 and libpng16-16t64
* 16:11 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on ldap171: liblcms2-2
* 16:11 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on matomo151: liblcms2-2
* 16:11 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on mattermost2: liblcms2-2
* 16:11 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on db192: liblcms2-2
* 16:10 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on cloud20: liblcms2-2
* 16:10 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on cp201: liblcms2-2
* 16:10 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on cp171: liblcms2-2 and libpng16-16t64
* 16:09 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on eventgate182: liblcms2-2
* 16:09 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on db181: liblcms2-2
* 16:09 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on cloud16: liblcms2-2
* 16:09 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on cloud18: liblcms2-2
* 16:08 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on db151: liblcms2-2
* 16:08 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on cloud17: liblcms2-2
* 16:07 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on bast181: liblcms2-2
* 16:07 MirahezeLSBot: [rhinos@puppet181] Upgraded packages on changeprop202: liblcms2-2
* 15:56 MirahezeLSBot: [rhinos@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php /srv/mediawiki/1.45/extensions/CentralAuth/maintenance/fixStuckGlobalRename.php --wiki=steelfightwiki --logwiki=metawiki JustLeafy2k3 JustLeafy (END - exit=0)
* 15:56 MirahezeLSBot: [rhinos@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php /srv/mediawiki/1.45/extensions/ManageWiki/maintenance/ResetWikiCaches.php --wiki=steelfightwiki (END - exit=0)
* 15:56 MirahezeLSBot: [rhinos@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php /srv/mediawiki/1.45/extensions/ManageWiki/maintenance/ResetWikiCaches.php --wiki=steelfightwiki (START)
* 15:56 RhinosF1: UPDATE mw_permissions SET perm_autopromote = NULL WHERE perm_dbname = 'steelfightwiki' AND perm_group = 'blocked';
* 15:55 MirahezeLSBot: [rhinos@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php /srv/mediawiki/1.45/extensions/ManageWiki/maintenance/resetWikiCaches.php --wiki=steelfightwiki (END - exit=256)
* 15:55 MirahezeLSBot: [rhinos@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php /srv/mediawiki/1.45/extensions/ManageWiki/maintenance/resetWikiCaches.php --wiki=steelfightwiki (START)
* 15:48 MirahezeLSBot: [rhinos@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php /srv/mediawiki/1.45/extensions/CentralAuth/maintenance/fixStuckGlobalRename.php --wiki=steelfightwiki --logwiki=metawiki JustLeafy2k3 JustLeafy (END - exit=256)
* 15:46 MirahezeLSBot: [rhinos@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php /srv/mediawiki/1.45/extensions/CentralAuth/maintenance/createLocalAccount.php --wiki=steelfightwiki NotAracham (END - exit=0)
* 15:42 MirahezeLSBot: [rhinos@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php /srv/mediawiki/1.45/extensions/CentralAuth/maintenance/attachAccount.php --wiki=metawiki --help --no-log (END - exit=256)
* 15:39 MirahezeLSBot: [rhinos@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php /srv/mediawiki/1.45/extensions/CentralAuth/maintenance/fixStuckGlobalRename.php --wiki=steelfightwiki --logwiki=metawiki JustLeafy2k3 JustLeafy (END - exit=256)
* 15:39 MirahezeLSBot: [rhinos@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php /srv/mediawiki/1.45/extensions/CentralAuth/maintenance/fixStuckGlobalRename.php --wiki=steelfightwiki --log=metawiki JustLeafy2k3 JustLeafy (END - exit=256)

## 2026-05-09 

* 18:50 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject201: python3-jwt
* 18:50 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject191: python3-jwt
* 18:50 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftproxy161: python3-jwt
* 18:50 MirahezeLSBot: [void@puppet181] Upgraded packages on test151: python3-jwt
* 18:49 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject211: python3-jwt
* 18:49 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftproxy171: python3-jwt
* 18:49 MirahezeLSBot: [void@puppet181] Upgraded packages on ns2: python3-jwt
* 18:49 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject181: python3-jwt
* 18:48 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject161: python3-jwt
* 18:48 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject171: python3-jwt
* 18:48 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject151: python3-jwt
* 18:48 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftac171: python3-jwt
* 18:46 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask181: python3-jwt
* 18:45 MirahezeLSBot: [void@puppet181] Upgraded packages on mw203: python3-jwt
* 18:45 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask171: python3-jwt
* 18:45 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask151: python3-jwt
* 18:44 MirahezeLSBot: [void@puppet181] Upgraded packages on mw202: python3-jwt
* 18:44 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask161: python3-jwt
* 18:44 MirahezeLSBot: [void@puppet181] Upgraded packages on mw201: python3-jwt
* 18:44 MirahezeLSBot: [void@puppet181] Upgraded packages on mw193: python3-jwt
* 18:43 MirahezeLSBot: [void@puppet181] Upgraded packages on mw181: python3-jwt
* 18:43 MirahezeLSBot: [void@puppet181] Upgraded packages on mw192: python3-jwt
* 18:43 MirahezeLSBot: [void@puppet181] Upgraded packages on mw182: python3-jwt
* 18:43 MirahezeLSBot: [void@puppet181] Upgraded packages on mw183: python3-jwt
* 18:42 MirahezeLSBot: [void@puppet181] Upgraded packages on mw191: python3-jwt
* 18:42 MirahezeLSBot: [void@puppet181] Upgraded packages on mw163: python3-jwt
* 18:42 MirahezeLSBot: [void@puppet181] Upgraded packages on mw173: python3-jwt
* 18:41 MirahezeLSBot: [void@puppet181] Upgraded packages on mw171: python3-jwt
* 18:41 MirahezeLSBot: [void@puppet181] Upgraded packages on mw153: python3-jwt
* 18:41 MirahezeLSBot: [void@puppet181] Upgraded packages on mw162: python3-jwt
* 18:41 MirahezeLSBot: [void@puppet181] Upgraded packages on mw172: python3-jwt
* 18:40 MirahezeLSBot: [void@puppet181] Upgraded packages on mw152: python3-jwt
* 18:40 MirahezeLSBot: [void@puppet181] Upgraded packages on mw151: python3-jwt
* 18:40 MirahezeLSBot: [void@puppet181] Upgraded packages on mw161: python3-jwt
* 18:39 MirahezeLSBot: [void@puppet181] Upgraded packages on mattermost2: python3-jwt
* 18:38 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud20: python3-jwt
* 18:38 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud18: python3-jwt
* 18:38 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud19: python3-jwt
* 18:37 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud16: python3-jwt
* 18:36 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud17: python3-jwt
* 18:35 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud15: python3-jwt
* 18:35 MirahezeLSBot: [void@puppet181] Upgraded packages on bots171: python3-jwt
* 17:36 MirahezeLSBot: [wwr@test151] finished deploy of {'world': True, 'l10n': True, 'extension_list': True, 'versions': '1.46', 'ignore_time': True} to test151 - SUCCESS in 72s
* 17:35 MirahezeLSBot: [wwr@test151] starting deploy of {'world': True, 'l10n': True, 'extension_list': True, 'versions': '1.46', 'ignore_time': True} to test151
* 17:35 MirahezeLSBot: [wwr@test151] finished deploy of {'pull': 'config', 'config': True} to test151 - SUCCESS in 1s
* 17:35 MirahezeLSBot: [wwr@test151] starting deploy of {'pull': 'config', 'config': True} to test151
* 00:11 MirahezeLSBot: [skye@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php ManageWiki:PopulateWikiSettings --wiki=metawiki --setting=wgCosmosWikiHeaderBackgroundColor --sourcelist=./cosmoslist.txt (END - exit=0)
* 00:07 MirahezeLSBot: [somerandomdeveloper@puppet181] sudo systemctl restart listdomains_github_push

## 2026-05-08 

* 23:26 SomeRandomDeveloper: sudo salt-ssh -E 'mw.*' cmd.run 'sudo -u www-data rm -rf /srv/mediawiki/1.45/extensions/ReportIncident/'
* 22:51 MirahezeLSBot: [skye@mwtask181] finished deploy of {'pull': 'config', 'config': True, 'world': True, 'l10n': True, 'extension_list': True, 'versions': '1.45'} to all - SUCCESS in 711s
* 22:39 MirahezeLSBot: [skye@mwtask181] starting deploy of {'pull': 'config', 'config': True, 'world': True, 'l10n': True, 'extension_list': True, 'versions': '1.45'} to all
* 22:32 MirahezeLSBot: [skye@mwtask181] DEPLOY ABORTED: Non-Zero Exit Code in prep, see output.
* 22:30 MirahezeLSBot: [skye@mwtask181] starting deploy of {'pull': 'config', 'config': True, 'world': True, 'l10n': True, 'extension_list': True, 'versions': '1.45'} to all
* 22:23 MirahezeLSBot: [skye@test151] finished deploy of {'pull': 'config', 'config': True, 'world': True, 'l10n': True, 'extension_list': True, 'versions': '1.45'} to test151 - SUCCESS in 348s
* 22:17 MirahezeLSBot: [skye@test151] starting deploy of {'pull': 'config', 'config': True, 'world': True, 'l10n': True, 'extension_list': True, 'versions': '1.45'} to test151
* 22:17 Skye: mwtask181/test151: sudo -u www-data rm -rf /srv/mediawiki-staging/{1.45,1.46}/extensions/ReportIncident/
* 20:50 MirahezeLSBot: [skye@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 25s
* 20:50 MirahezeLSBot: [skye@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 20:50 MirahezeLSBot: [skye@test151] finished deploy of {'pull': 'config', 'config': True} to test151 - SUCCESS in 0s
* 20:50 MirahezeLSBot: [skye@test151] starting deploy of {'pull': 'config', 'config': True} to test151
* 20:47 MirahezeLSBot: [skye@test151] finished deploy of {'pull': 'config', 'config': True} to test151 - SUCCESS in 1s
* 20:47 MirahezeLSBot: [skye@test151] starting deploy of {'pull': 'config', 'config': True} to test151
* 20:21 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftproxy161: linux-libc-dev
* 20:21 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject191: linux-libc-dev
* 20:20 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject201: linux-libc-dev
* 20:20 MirahezeLSBot: [void@puppet181] Upgraded packages on test151: linux-libc-dev, php8.4-zip, php8.4-xml, php8.4-readline, php8.4-opcache, php8.4-cli, php8.4-phpdbg, php8.4-mysql, php8.4-mbstring, php8.4-ldap, php8.4-intl, php8.4-gmp, php8.4-gd, php8.4-fpm, php8.4-dev, php8.4-dba, php8.4-curl, php8.4-bz2, php8.4-bcmath, and php8.4-common
* 20:19 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftproxy171: linux-libc-dev
* 20:19 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject211: linux-libc-dev
* 20:18 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject181: linux-libc-dev
* 20:18 MirahezeLSBot: [void@puppet181] Upgraded packages on ns2: linux-libc-dev
* 20:18 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject171: linux-libc-dev
* 20:18 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject161: linux-libc-dev
* 20:17 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftac171: linux-libc-dev
* 20:17 MirahezeLSBot: [void@puppet181] Upgraded packages on swiftobject151: linux-libc-dev
* 20:17 MirahezeLSBot: [void@puppet181] Upgraded packages on os202: linux-libc-dev
* 20:16 MirahezeLSBot: [void@puppet181] Upgraded packages on os201: linux-libc-dev
* 20:16 MirahezeLSBot: [void@puppet181] Upgraded packages on rdb191: linux-libc-dev
* 20:16 MirahezeLSBot: [void@puppet181] Upgraded packages on puppet181: linux-libc-dev
* 20:16 MirahezeLSBot: [void@puppet181] Upgraded packages on reports171: linux-libc-dev, php8.4-zip, php8.4-xml, php8.4-readline, php8.4-opcache, php8.4-phpdbg, php8.4-mysql, php8.4-mbstring, php8.4-ldap, php8.4-intl, php8.4-gmp, php8.4-gd, php8.4-fpm, php8.4-curl, php8.4-cli, and php8.4-common
* 20:15 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask181: linux-libc-dev, php8.4-zip, php8.4-xml, php8.4-readline, php8.4-opcache, php8.4-cli, php8.4-phpdbg, php8.4-mysql, php8.4-mbstring, php8.4-ldap, php8.4-intl, php8.4-gmp, php8.4-gd, php8.4-fpm, php8.4-dba, php8.4-curl, php8.4-bz2, php8.4-bcmath, and php8.4-common
* 20:14 MirahezeLSBot: [void@puppet181] Upgraded packages on os161: linux-libc-dev
* 20:13 MirahezeLSBot: [void@puppet181] Upgraded packages on prometheus151: linux-libc-dev
* 20:13 MirahezeLSBot: [void@puppet181] Upgraded packages on phorge171: linux-libc-dev, php8.4-zip, php8.4-xml, php8.4-readline, php8.4-opcache, php8.4-phpdbg, php8.4-mysql, php8.4-mbstring, php8.4-ldap, php8.4-intl, php8.4-gmp, php8.4-gd, php8.4-fpm, php8.4-curl, php8.4-cli, and php8.4-common
* 20:12 MirahezeLSBot: [void@puppet181] Upgraded packages on os162: linux-libc-dev
* 20:12 MirahezeLSBot: [void@puppet181] Upgraded packages on os191: linux-libc-dev
* 20:12 MirahezeLSBot: [void@puppet181] Upgraded packages on os151: linux-libc-dev
* 20:12 MirahezeLSBot: [void@puppet181] Upgraded packages on mw203: linux-libc-dev, php8.4-zip, php8.4-xml, php8.4-readline, php8.4-opcache, php8.4-cli, php8.4-phpdbg, php8.4-mysql, php8.4-mbstring, php8.4-ldap, php8.4-intl, php8.4-gmp, php8.4-gd, php8.4-fpm, php8.4-dba, php8.4-curl, php8.4-bz2, php8.4-bcmath, and php8.4-common
* 20:10 MirahezeLSBot: [void@puppet181] Upgraded packages on ns1: linux-libc-dev
* 20:10 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask171: linux-libc-dev, php8.4-zip, php8.4-xml, php8.4-readline, php8.4-opcache, php8.4-cli, php8.4-phpdbg, php8.4-mysql, php8.4-mbstring, php8.4-ldap, php8.4-intl, php8.4-gmp, php8.4-gd, php8.4-fpm, php8.4-dba, php8.4-curl, php8.4-bz2, php8.4-bcmath, and php8.4-common
* 20:09 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask161: linux-libc-dev, php8.4-zip, php8.4-xml, php8.4-readline, php8.4-opcache, php8.4-cli, php8.4-phpdbg, php8.4-mysql, php8.4-mbstring, php8.4-ldap, php8.4-intl, php8.4-gmp, php8.4-gd, php8.4-fpm, php8.4-dba, php8.4-curl, php8.4-bz2, php8.4-bcmath, and php8.4-common
* 20:08 MirahezeLSBot: [void@puppet181] Upgraded packages on mw202: linux-libc-dev, php8.4-zip, php8.4-xml, php8.4-readline, php8.4-opcache, php8.4-cli, php8.4-phpdbg, php8.4-mysql, php8.4-mbstring, php8.4-ldap, php8.4-intl, php8.4-gmp, php8.4-gd, php8.4-fpm, php8.4-dba, php8.4-curl, php8.4-bz2, php8.4-bcmath, and php8.4-common
* 20:06 MirahezeLSBot: [void@puppet181] Upgraded packages on mw201: linux-libc-dev, php8.4-zip, php8.4-xml, php8.4-readline, php8.4-opcache, php8.4-cli, php8.4-phpdbg, php8.4-mysql, php8.4-mbstring, php8.4-ldap, php8.4-intl, php8.4-gmp, php8.4-gd, php8.4-fpm, php8.4-dba, php8.4-curl, php8.4-bz2, php8.4-bcmath, and php8.4-common
* 20:05 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask151: linux-libc-dev, php8.4-zip, php8.4-xml, php8.4-readline, php8.4-opcache, php8.4-cli, php8.4-phpdbg, php8.4-mysql, php8.4-mbstring, php8.4-ldap, php8.4-intl, php8.4-gmp, php8.4-gd, php8.4-fpm, php8.4-dba, php8.4-curl, php8.4-bz2, php8.4-bcmath, and php8.4-common
* 20:04 MirahezeLSBot: [void@puppet181] Upgraded packages on mw183: linux-libc-dev, php8.4-zip, php8.4-xml, php8.4-readline, php8.4-opcache, php8.4-cli, php8.4-phpdbg, php8.4-mysql, php8.4-mbstring, php8.4-ldap, php8.4-intl, php8.4-gmp, php8.4-gd, php8.4-fpm, php8.4-dba, php8.4-curl, php8.4-bz2, php8.4-bcmath, and php8.4-common
* 20:03 MirahezeLSBot: [void@puppet181] Upgraded packages on mw193: linux-libc-dev, php8.4-zip, php8.4-xml, php8.4-readline, php8.4-opcache, php8.4-cli, php8.4-phpdbg, php8.4-mysql, php8.4-mbstring, php8.4-ldap, php8.4-intl, php8.4-gmp, php8.4-gd, php8.4-fpm, php8.4-dba, php8.4-curl, php8.4-bz2, php8.4-bcmath, and php8.4-common
* 20:02 MirahezeLSBot: [skye@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 23s
* 20:01 MirahezeLSBot: [void@puppet181] Upgraded packages on mw173: linux-libc-dev, php8.4-zip, php8.4-xml, php8.4-readline, php8.4-opcache, php8.4-cli, php8.4-phpdbg, php8.4-mysql, php8.4-mbstring, php8.4-ldap, php8.4-intl, php8.4-gmp, php8.4-gd, php8.4-fpm, php8.4-dba, php8.4-curl, php8.4-bz2, php8.4-bcmath, and php8.4-common
* 20:01 MirahezeLSBot: [skye@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 20:01 MirahezeLSBot: [skye@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 25s
* 20:01 MirahezeLSBot: [skye@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 20:00 MirahezeLSBot: [void@puppet181] Upgraded packages on mw192: linux-libc-dev, php8.4-zip, php8.4-xml, php8.4-readline, php8.4-opcache, php8.4-cli, php8.4-phpdbg, php8.4-mysql, php8.4-mbstring, php8.4-ldap, php8.4-intl, php8.4-gmp, php8.4-gd, php8.4-fpm, php8.4-dba, php8.4-curl, php8.4-bz2, php8.4-bcmath, and php8.4-common
* 19:59 MirahezeLSBot: [void@puppet181] Upgraded packages on mw181: linux-libc-dev, php8.4-zip, php8.4-xml, php8.4-readline, php8.4-opcache, php8.4-cli, php8.4-phpdbg, php8.4-mysql, php8.4-mbstring, php8.4-ldap, php8.4-intl, php8.4-gmp, php8.4-gd, php8.4-fpm, php8.4-dba, php8.4-curl, php8.4-bz2, php8.4-bcmath, and php8.4-common
* 19:58 MirahezeLSBot: [void@puppet181] Upgraded packages on mw182: linux-libc-dev, php8.4-zip, php8.4-xml, php8.4-readline, php8.4-opcache, php8.4-cli, php8.4-phpdbg, php8.4-mysql, php8.4-mbstring, php8.4-ldap, php8.4-intl, php8.4-gmp, php8.4-gd, php8.4-fpm, php8.4-dba, php8.4-curl, php8.4-bz2, php8.4-bcmath, and php8.4-common
* 19:56 MirahezeLSBot: [void@puppet181] Upgraded packages on mw191: linux-libc-dev, php8.4-zip, php8.4-xml, php8.4-readline, php8.4-opcache, php8.4-cli, php8.4-phpdbg, php8.4-mysql, php8.4-mbstring, php8.4-ldap, php8.4-intl, php8.4-gmp, php8.4-gd, php8.4-fpm, php8.4-dba, php8.4-curl, php8.4-bz2, php8.4-bcmath, and php8.4-common
* 19:55 MirahezeLSBot: [void@puppet181] Upgraded packages on mw163: linux-libc-dev, php8.4-zip, php8.4-xml, php8.4-readline, php8.4-opcache, php8.4-cli, php8.4-phpdbg, php8.4-mysql, php8.4-mbstring, php8.4-ldap, php8.4-intl, php8.4-gmp, php8.4-gd, php8.4-fpm, php8.4-dba, php8.4-curl, php8.4-bz2, php8.4-bcmath, and php8.4-common
* 19:54 MirahezeLSBot: [void@puppet181] Upgraded packages on mw171: linux-libc-dev, php8.4-zip, php8.4-xml, php8.4-readline, php8.4-opcache, php8.4-cli, php8.4-phpdbg, php8.4-mysql, php8.4-mbstring, php8.4-ldap, php8.4-intl, php8.4-gmp, php8.4-gd, php8.4-fpm, php8.4-dba, php8.4-curl, php8.4-bz2, php8.4-bcmath, and php8.4-common
* 19:52 MirahezeLSBot: [void@puppet181] Upgraded packages on mw153: linux-libc-dev, php8.4-zip, php8.4-xml, php8.4-readline, php8.4-opcache, php8.4-cli, php8.4-phpdbg, php8.4-mysql, php8.4-mbstring, php8.4-ldap, php8.4-intl, php8.4-gmp, php8.4-gd, php8.4-fpm, php8.4-dba, php8.4-curl, php8.4-bz2, php8.4-bcmath, and php8.4-common
* 19:51 MirahezeLSBot: [void@puppet181] Upgraded packages on mw162: linux-libc-dev, php8.4-zip, php8.4-xml, php8.4-readline, php8.4-opcache, php8.4-cli, php8.4-phpdbg, php8.4-mysql, php8.4-mbstring, php8.4-ldap, php8.4-intl, php8.4-gmp, php8.4-gd, php8.4-fpm, php8.4-dba, php8.4-curl, php8.4-bz2, php8.4-bcmath, and php8.4-common
* 19:50 MirahezeLSBot: [void@puppet181] Upgraded packages on mw172: linux-libc-dev, php8.4-zip, php8.4-xml, php8.4-readline, php8.4-opcache, php8.4-cli, php8.4-phpdbg, php8.4-mysql, php8.4-mbstring, php8.4-ldap, php8.4-intl, php8.4-gmp, php8.4-gd, php8.4-fpm, php8.4-dba, php8.4-curl, php8.4-bz2, php8.4-bcmath, and php8.4-common
* 19:49 MirahezeLSBot: [void@puppet181] Upgraded packages on mon181: linux-libc-dev, php8.4-opcache, php8.4-readline, php8.4-cli, libapache2-mod-php8.4, php8.4-xml, php8.4-soap, php8.4-pgsql, php8.4-mysql, php8.4-mbstring, php8.4-ldap, php8.4-gmp, php8.4-gd, php8.4-fpm, php8.4-curl, php8.4-intl, php8.4-common, and php8.4
* 19:48 MirahezeLSBot: [void@puppet181] Upgraded packages on mw152: linux-libc-dev, php8.4-zip, php8.4-xml, php8.4-readline, php8.4-opcache, php8.4-cli, php8.4-phpdbg, php8.4-mysql, php8.4-mbstring, php8.4-ldap, php8.4-intl, php8.4-gmp, php8.4-gd, php8.4-fpm, php8.4-dba, php8.4-curl, php8.4-bz2, php8.4-bcmath, and php8.4-common
* 19:46 MirahezeLSBot: [void@puppet181] Upgraded packages on mw161: linux-libc-dev, php8.4-zip, php8.4-xml, php8.4-readline, php8.4-opcache, php8.4-cli, php8.4-phpdbg, php8.4-mysql, php8.4-mbstring, php8.4-ldap, php8.4-intl, php8.4-gmp, php8.4-gd, php8.4-fpm, php8.4-dba, php8.4-curl, php8.4-bz2, php8.4-bcmath, and php8.4-common
* 19:45 MirahezeLSBot: [void@puppet181] Upgraded packages on mw151: linux-libc-dev, php8.4-zip, php8.4-xml, php8.4-readline, php8.4-opcache, php8.4-cli, php8.4-phpdbg, php8.4-mysql, php8.4-mbstring, php8.4-ldap, php8.4-intl, php8.4-gmp, php8.4-gd, php8.4-fpm, php8.4-dba, php8.4-curl, php8.4-bz2, php8.4-bcmath, and php8.4-common
* 19:44 MirahezeLSBot: [void@puppet181] Upgraded packages on llm191: linux-libc-dev
* 19:43 MirahezeLSBot: [void@puppet181] Upgraded packages on mem191: linux-libc-dev
* 19:43 MirahezeLSBot: [void@puppet181] Upgraded packages on mem201: linux-libc-dev
* 19:43 MirahezeLSBot: [void@puppet181] Upgraded packages on mem151: linux-libc-dev
* 19:43 MirahezeLSBot: [void@puppet181] Upgraded packages on mem161: linux-libc-dev
* 19:43 MirahezeLSBot: [void@puppet181] Upgraded packages on matomo151: linux-libc-dev, php8.4-zip, php8.4-xml, php8.4-readline, php8.4-opcache, php8.4-phpdbg, php8.4-mysql, php8.4-mbstring, php8.4-ldap, php8.4-intl, php8.4-gmp, php8.4-gd, php8.4-fpm, php8.4-curl, php8.4-cli, and php8.4-common
* 19:42 MirahezeLSBot: [void@puppet181] Upgraded packages on mattermost2: linux-libc-dev
* 19:41 MirahezeLSBot: [void@puppet181] Upgraded packages on kafka182: linux-libc-dev
* 19:41 MirahezeLSBot: [void@puppet181] Upgraded packages on ldap171: linux-libc-dev
* 19:41 MirahezeLSBot: [void@puppet181] Upgraded packages on db181: linux-libc-dev
* 19:41 MirahezeLSBot: [void@puppet181] Upgraded packages on cp171: linux-libc-dev
* 19:40 MirahezeLSBot: [void@puppet181] Upgraded packages on db192: linux-libc-dev
* 19:40 MirahezeLSBot: [void@puppet181] Upgraded packages on cp201: linux-libc-dev
* 19:40 MirahezeLSBot: [void@puppet181] Upgraded packages on db201: linux-libc-dev
* 19:40 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud18: linux-libc-dev, libcpupower1, and linux-cpupower
* 19:39 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud19: linux-libc-dev, libcpupower1, and linux-cpupower
* 19:39 MirahezeLSBot: [void@puppet181] Upgraded packages on cp191: linux-libc-dev
* 19:39 MirahezeLSBot: [void@puppet181] Upgraded packages on bast181: linux-libc-dev
* 19:39 MirahezeLSBot: [void@puppet181] Upgraded packages on eventgate182: linux-libc-dev
* 19:38 MirahezeLSBot: [void@puppet181] Upgraded packages on graylog161: linux-libc-dev
* 19:38 MirahezeLSBot: [void@puppet181] Upgraded packages on db182: linux-libc-dev
* 19:38 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud17: linux-libc-dev, libcpupower1, and linux-cpupower
* 19:38 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud20: linux-libc-dev, libcpupower1, and linux-cpupower
* 19:37 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud15: linux-libc-dev, libcpupower1, and linux-cpupower
* 19:37 MirahezeLSBot: [void@puppet181] Upgraded packages on changeprop202: linux-libc-dev
* 19:37 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud16: linux-libc-dev, libcpupower1, and linux-cpupower
* 19:37 MirahezeLSBot: [void@puppet181] Upgraded packages on db171: linux-libc-dev
* 19:36 MirahezeLSBot: [void@puppet181] Upgraded packages on db151: linux-libc-dev
* 19:36 MirahezeLSBot: [void@puppet181] Upgraded packages on db172: linux-libc-dev
* 19:36 MirahezeLSBot: [void@puppet181] Upgraded packages on cp161: linux-libc-dev
* 19:36 MirahezeLSBot: [void@puppet181] Upgraded packages on cloud21: linux-libc-dev, libcpupower1, and linux-cpupower
* 19:36 MirahezeLSBot: [void@puppet181] Upgraded packages on bast161: linux-libc-dev
* 19:35 MirahezeLSBot: [void@puppet181] Upgraded packages on db161: linux-libc-dev
* 19:35 MirahezeLSBot: [void@puppet181] Upgraded packages on bots171: linux-libc-dev
* 17:05 MirahezeLSBot: [wwr@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 30s
* 17:04 MirahezeLSBot: [wwr@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 16:59 MirahezeLSBot: [wwr@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 16:59 MirahezeLSBot: [wwr@test151] starting deploy of {'config': True} to test151
* 16:44 MirahezeLSBot: [wwr@test151] finished deploy of {'force_upgrade': True, 'versions': '1.45', 'upgrade_extensions': 'PdfHandler'} to test151 - SUCCESS in 0s
* 16:44 MirahezeLSBot: [wwr@test151] starting deploy of {'force_upgrade': True, 'versions': '1.45', 'upgrade_extensions': 'PdfHandler'} to test151
* 16:40 MirahezeLSBot: [wwr@test151] finished deploy of {'force_upgrade': True, 'versions': '1.45', 'upgrade_extensions': 'PdfHandler'} to test151 - SUCCESS in 0s
* 16:40 MirahezeLSBot: [wwr@test151] starting deploy of {'force_upgrade': True, 'versions': '1.45', 'upgrade_extensions': 'PdfHandler'} to test151
* 16:39 MirahezeLSBot: [wwr@test151] starting deploy of {'force_upgrade': True, 'versions': '1.45', 'upgrade_extensions': 'PdfHandler'} to test151
* 16:28 MirahezeLSBot: [wwr@test151] DEPLOY ABORTED: Canary check failed for meta.mirabeta.org@localhost
* 16:28 MirahezeLSBot: [wwr@test151] starting deploy of {'folders': '1.45/extensions/PdfHandler'} to test151
* 16:26 MirahezeLSBot: [wwr@test151] DEPLOY ABORTED: Canary check failed for meta.mirabeta.org@localhost
* 16:26 MirahezeLSBot: [wwr@test151] starting deploy of {'force_upgrade': True, 'versions': '1.45', 'upgrade_extensions': 'PdfHandler'} to test151
* 16:24 MirahezeLSBot: [wwr@test151] DEPLOY ABORTED: Canary check failed for meta.mirabeta.org@localhost
* 16:24 MirahezeLSBot: [wwr@test151] starting deploy of {'folders': '.'} to test151
* 16:20 MirahezeLSBot: [wwr@test151] starting deploy of {'pull': 'config', 'config': True, 'l10n': True, 'extension_list': True, 'force_upgrade': True, 'versions': '1.45', 'upgrade_extensions': 'PdfHandler'} to test151
* 14:46 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php CirrusSearch:ForceSearchIndex --wiki=arawynnslorehubwiki (END - exit=0)
* 14:46 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php CirrusSearch:UpdateSearchIndexConfig --wiki=arawynnslorehubwiki --startOver (END - exit=0)

## 2026-05-07 

* 20:02 MirahezeLSBot: [void@puppet181] Upgraded packages on mon181: libwireshark-data, libwsutil16, libwiretap15, libwireshark18, tshark, and wireshark-common
* 20:02 MirahezeLSBot: [void@puppet181] Upgraded packages on db182: libwireshark-data, libwsutil16, libwiretap15, libwireshark18, tshark, and wireshark-common
* 04:30 MirahezeLSBot: [petramagna@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 26s
* 04:30 MirahezeLSBot: [petramagna@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 04:17 MirahezeLSBot: [petramagna@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 04:17 MirahezeLSBot: [petramagna@test151] starting deploy of {'config': True} to test151
* 04:16 MirahezeLSBot: [skye@mwtask171] Finished import for domainswiki (XML: internetdomains.xml; Images: None) (END - exit=0)
* 04:15 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php initSiteStats --wiki=domainswiki --update (END - exit=0)
* 04:15 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php initSiteStats --wiki=domainswiki --update (START)
* 04:15 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php initEditCount --wiki=domainswiki (END - exit=0)
* 04:15 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php initEditCount --wiki=domainswiki (START)
* 04:15 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php rebuildall --wiki=domainswiki (END - exit=0)

## 2026-05-06 

* 22:45 MirahezeLSBot: [skye@mwtask171] Finished import for teletran2wiki (XML: backup.xml; Images: None) (END - exit=0)
* 22:45 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php initSiteStats --wiki=teletran2wiki --update (END - exit=0)
* 22:45 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php initSiteStats --wiki=teletran2wiki --update (START)
* 22:45 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php initEditCount --wiki=teletran2wiki (END - exit=0)
* 22:45 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php initEditCount --wiki=teletran2wiki (START)
* 22:45 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php rebuildall --wiki=teletran2wiki (END - exit=0)
* 19:19 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php CreateWiki:SetContainersAccess --wiki=fragmenteddestinywiki (END - exit=0)
* 19:18 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RenameDatabase --wiki=loginwiki --rename --old=shatteredrealitywiki --new=fragmenteddestinywiki --user=Skye (END - exit=0)
* 18:33 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask181: apache2, apache2-bin, apache2-data, and apache2-utils
* 18:33 MirahezeLSBot: [void@puppet181] Upgraded packages on test151: apache2, apache2-bin, apache2-data, and apache2-utils
* 18:32 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask151: apache2, apache2-bin, apache2-data, and apache2-utils
* 18:32 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask171: apache2, apache2-bin, apache2-data, and apache2-utils
* 18:31 MirahezeLSBot: [void@puppet181] Upgraded packages on mon181: apache2-bin and apache2-utils
* 18:31 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask161: apache2, apache2-bin, apache2-data, and apache2-utils
* 18:31 MirahezeLSBot: [void@puppet181] Upgraded packages on prometheus151: apache2, apache2-bin, apache2-data, and apache2-utils
* 04:06 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php rebuildall --wiki=teletran2wiki (START)
* 04:05 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importDump --wiki=teletran2wiki --no-updates --username-prefix=tfwiki -- backup.xml (END - exit=0)
* 01:12 MirahezeLSBot: [somerandomdeveloper@mwtask181] finished deploy of {'l10n': True, 'extension_list': True, 'versions': '1.45'} to all - SUCCESS in 534s
* 01:08 MirahezeLSBot: [somerandomdeveloper@test151] finished deploy of {'l10n': True, 'extension_list': True, 'versions': '1.45'} to test151 - SUCCESS in 324s
* 01:03 MirahezeLSBot: [somerandomdeveloper@mwtask181] starting deploy of {'l10n': True, 'extension_list': True, 'versions': '1.45'} to all
* 01:03 MirahezeLSBot: [somerandomdeveloper@mwtask181] DEPLOY ABORTED: Non-Zero Exit Code in prep, see output.
* 01:03 MirahezeLSBot: [somerandomdeveloper@mwtask181] starting deploy of {'l10n': True, 'extension_list': True, 'versions': '1.45'} to all
* 01:03 MirahezeLSBot: [somerandomdeveloper@test151] starting deploy of {'l10n': True, 'extension_list': True, 'versions': '1.45'} to test151
* 01:02 SomeRandomDeveloper: sudo salt-ssh -E 'mw.*' cmd.run 'sudo -u www-data rm -rf /srv/mediawiki/1.45/extensions/CampaignEvents/'
* 01:01 MirahezeLSBot: [somerandomdeveloper@mwtask181] sudo -u www-data rm -rf /srv/mediawiki-staging/1.45/extensions/CampaignEvents/
* 01:01 MirahezeLSBot: [somerandomdeveloper@test151] sudo -u www-data rm -rf /srv/mediawiki-staging/1.45/extensions/CampaignEvents/
* 01:01 MirahezeLSBot: [somerandomdeveloper@test151] sudo -u www-data rm -rf /srv/mediawiki/1.45/extensions/CampaignEvents/
* 00:54 MirahezeLSBot: [somerandomdeveloper@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 26s
* 00:53 MirahezeLSBot: [somerandomdeveloper@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 00:53 MirahezeLSBot: [somerandomdeveloper@test151] finished deploy of {'pull': 'config', 'config': True} to test151 - SUCCESS in 10s
* 00:53 MirahezeLSBot: [somerandomdeveloper@test151] starting deploy of {'pull': 'config', 'config': True} to test151
* 00:52 MirahezeLSBot: [somerandomdeveloper@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 00:51 MirahezeLSBot: [somerandomdeveloper@test151] starting deploy of {'config': True} to test151

## 2026-05-05 

* 23:19 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importDump --wiki=teletran2wiki --no-updates --username-prefix=tfwiki -- backup.xml (START)
* 23:18 MirahezeLSBot: [skye@mwtask171] Starting import for teletran2wiki (XML: backup.xml; Images: None) (START)
* 23:13 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php initSiteStats --wiki=crygaiawiki --update (END - exit=0)
* 23:13 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php initEditCount --wiki=crygaiawiki (END - exit=0)
* 22:55 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php rebuildall --wiki=crygaiawiki (END - exit=0)
* 21:30 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php rebuildall --wiki=crygaiawiki (START)
* 20:17 MirahezeLSBot: [skye@mwtask171] Finished import for crygaiawiki (XML: history.xml; Images: ./images) (END - exit=1)
* 20:17 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php rebuildall --wiki=crygaiawiki (END - exit=1)
* 20:17 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php rebuildall --wiki=crygaiawiki (START)
* 20:17 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=crygaiawiki --sleep=1 '--comment=Importing images from wiki.crygaia.org ([T15337](https://meta.miraheze.org/wiki/phorge:T15337))' -- ./images (END - exit=0)
* 16:34 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=crygaiawiki --sleep=1 '--comment=Importing images from wiki.crygaia.org ([T15337](https://meta.miraheze.org/wiki/phorge:T15337))' -- ./images (START)
* 16:34 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importDump --wiki=crygaiawiki --no-updates --username-prefix=crygaia -- history.xml (END - exit=0)
* 15:50 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importDump --wiki=crygaiawiki --no-updates --username-prefix=crygaia -- history.xml (START)
* 15:50 MirahezeLSBot: [skye@mwtask171] Starting import for crygaiawiki (XML: history.xml; Images: ./images) (START)
* 15:45 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:ResetWiki --wiki=loginwiki --dbname=crygaiawiki --requester=SnerkDevil (END - exit=0)
* 04:56 MirahezeLSBot: [skye@mwtask171] Finished import for unanythingwiki (XML: None; Images: .) (END - exit=0)
* 04:56 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php initSiteStats --wiki=unanythingwiki --update (END - exit=0)
* 04:56 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php initSiteStats --wiki=unanythingwiki --update (START)
* 04:56 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=unanythingwiki --sleep=1 '--comment=Importing images from [https://unanything.fandom.com/](https://unanything.fandom.com/) ([T15300](https://meta.miraheze.org/wiki/phorge:T15300))' -- . (END - exit=0)

## 2026-05-04 

* 23:57 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importImages --wiki=unanythingwiki --sleep=1 '--comment=Importing images from [https://unanything.fandom.com/](https://unanything.fandom.com/) ([T15300](https://meta.miraheze.org/wiki/phorge:T15300))' -- . (START)
* 23:57 MirahezeLSBot: [skye@mwtask171] Starting import for unanythingwiki (XML: None; Images: .) (START)
* 23:16 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php rebuildall --wiki=domainswiki (START)
* 23:16 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importDump --wiki=domainswiki --no-updates --username-prefix=domains -- internetdomains.xml (END - exit=0)
* 21:17 MirahezeLSBot: [skye@mwtask171] Finished import for unanythingwiki (XML: unanything_pages_full.xml; Images: None) (END - exit=0)
* 21:17 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php initSiteStats --wiki=unanythingwiki --update (END - exit=0)
* 21:17 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php initSiteStats --wiki=unanythingwiki --update (START)
* 21:17 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php initEditCount --wiki=unanythingwiki (END - exit=0)
* 21:17 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php initEditCount --wiki=unanythingwiki (START)
* 21:17 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php rebuildall --wiki=unanythingwiki (END - exit=0)
* 21:14 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php CreateWiki:SetContainersAccess --wiki=circumferencewikiwiki (END - exit=0)
* 21:13 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RenameDatabase --wiki=loginwiki --rename --old=ajustwikiwiki --new=circumferencewikiwiki --user=Skye (END - exit=0)
* 19:06 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php rebuildall --wiki=unanythingwiki (START)
* 19:06 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importDump --wiki=unanythingwiki --no-updates --username-prefix=fandom:unanything -- unanything_pages_full.xml (END - exit=0)
* 18:45 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importDump --wiki=domainswiki --no-updates --username-prefix=domains -- internetdomains.xml (START)
* 18:45 MirahezeLSBot: [skye@mwtask171] Starting import for domainswiki (XML: internetdomains.xml; Images: None) (START)
* 18:41 MirahezeLSBot: [skye@mwtask171] Finished import for domainswiki (XML: internetdomains.xml; Images: None) (END - exit=1)
* 18:41 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importDump --wiki=domainswiki --no-updates --username-prefix=domains -- internetdomains.xml (END - exit=1)
* 18:41 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importDump --wiki=domainswiki --no-updates --username-prefix=domains -- internetdomains.xml (START)
* 18:41 MirahezeLSBot: [skye@mwtask171] Starting import for domainswiki (XML: internetdomains.xml; Images: None) (START)
* 18:26 MirahezeLSBot: [void@db161] systemctl reset-failed sql-backup && systemctl restart sql-backup
* 18:14 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importDump --wiki=unanythingwiki --no-updates --username-prefix=fandom:unanything -- unanything_pages_full.xml (START)
* 18:14 MirahezeLSBot: [skye@mwtask171] Starting import for unanythingwiki (XML: unanything_pages_full.xml; Images: None) (START)
* 18:14 MirahezeLSBot: [skye@mwtask171] Finished import for unanythingwiki (XML: unanything_pages_full.xml; Images: None) (END - exit=-2)
* 18:14 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importDump --wiki=unanythingwiki --no-updates --username-prefix=fandom:unanything -- unanything_pages_full.xml (END - exit=-2)
* 18:12 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importDump --wiki=unanythingwiki --no-updates --username-prefix=fandom:unanything -- unanything_pages_full.xml (START)
* 18:12 MirahezeLSBot: [skye@mwtask171] Starting import for unanythingwiki (XML: unanything_pages_full.xml; Images: None) (START)
* 18:10 MirahezeLSBot: [skye@mwtask171] Finished import for unanythingwiki (XML: unanything_pages_full.xml; Images: None) (END - exit=1)
* 18:10 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importDump --wiki=unanythingwiki --no-updates --username-prefix=fandom:unanything -- unanything_pages_full.xml (END - exit=1)
* 18:10 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php importDump --wiki=unanythingwiki --no-updates --username-prefix=fandom:unanything -- unanything_pages_full.xml (START)
* 18:10 MirahezeLSBot: [skye@mwtask171] Starting import for unanythingwiki (XML: unanything_pages_full.xml; Images: None) (START)
* 17:44 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php CreateWiki:SetContainersAccess --wiki=saltationismwiki (END - exit=0)
* 17:42 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RenameDatabase --wiki=loginwiki --rename --old=variegatedwiki --new=saltationismwiki --user=Skye (END - exit=0)
* 17:38 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php CreateWiki:SetContainersAccess --wiki=nnpwiki (END - exit=0)
* 17:37 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RenameDatabase --wiki=loginwiki --rename --old=naramonuclearplantv2wiki --new=nnpwiki --user=Skye (END - exit=0)
* 17:34 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php CreateWiki:SetContainersAccess --wiki=rotwoodvalecnwiki (END - exit=0)
* 17:33 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RenameDatabase --wiki=loginwiki --rename --old=rotwoodvalcnwiki --new=rotwoodvalecnwiki --user=Skye (END - exit=0)
* 17:31 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RenameDatabase --wiki=loginwiki --rename --old=rotwoodvalcnwiki --new=rotwoodvalecn=wiki --user=Skye (END - exit=256)
* 17:31 MirahezeLSBot: [skye@mwtask171] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:RenameDatabase --wiki=loginwiki --rename --old=rotwoodvalcnwiki --newrotwoodvalecn=wiki --user=Skye (END - exit=256)

## 2026-05-03 

* 22:35 MirahezeLSBot: [void@db161] systemctl reset-failed sql-backup && systemctl restart sql-backup
* 02:22 MirahezeLSBot: [void@mwtask181] repool c2
* 02:22 MirahezeLSBot: [void@mwtask181] finished deploy of {'config': True, 'force': True} to all - SUCCESS in 18s
* 02:22 MirahezeLSBot: [void@mwtask181] starting deploy of {'config': True, 'force': True} to all
* 02:19 MirahezeLSBot: [void@db161] reboot db161
* 02:19 MirahezeLSBot: [void@mwtask181] finished deploy of {'pull': 'config', 'config': True, 'force': True} to all - SUCCESS in 19s
* 02:19 MirahezeLSBot: [void@mwtask181] starting deploy of {'pull': 'config', 'config': True, 'force': True} to all
* 02:19 MirahezeLSBot: [void@mwtask181] DEPLOY ABORTED: Canary check failed for publictestwiki.com@localhost
* 02:18 MirahezeLSBot: [void@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 01:41 MirahezeLSBot: [void@mwtask181] depool c2
* 01:41 MirahezeLSBot: [void@mwtask181] finished deploy of {'config': True, 'force': True} to all - SUCCESS in 19s
* 01:41 MirahezeLSBot: [void@mwtask181] starting deploy of {'config': True, 'force': True} to all

## 2026-05-02 

* 22:52 MirahezeLSBot: [skye@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 25s
* 22:51 MirahezeLSBot: [skye@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 20:26 MirahezeLSBot: [petramagna@mwtask181] finished deploy of {'versions': '1.45', 'upgrade_extensions': 'MatomoAnalytics'} to all - SUCCESS in 26s
* 20:26 MirahezeLSBot: [petramagna@mwtask181] starting deploy of {'versions': '1.45', 'upgrade_extensions': 'MatomoAnalytics'} to all
* 20:14 MirahezeLSBot: [petramagna@test151] finished deploy of {'folders': '1.45/extensions/MatomoAnalytics'} to test151 - SUCCESS in 0s
* 20:14 MirahezeLSBot: [petramagna@test151] starting deploy of {'folders': '1.45/extensions/MatomoAnalytics'} to test151
* 18:12 MirahezeLSBot: [skye@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 28s
* 18:11 MirahezeLSBot: [skye@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all

## 2026-05-01 

* 19:42 MirahezeLSBot: [void@puppet181] Upgraded packages on mw183: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 19:42 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask181: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 19:41 MirahezeLSBot: [void@puppet181] Upgraded packages on mw163: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 19:41 MirahezeLSBot: [void@puppet181] Upgraded packages on mw153: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 19:41 MirahezeLSBot: [void@puppet181] Upgraded packages on mw191: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 19:40 MirahezeLSBot: [void@puppet181] Upgraded packages on test151: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 19:40 MirahezeLSBot: [void@puppet181] Upgraded packages on mw192: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 19:40 MirahezeLSBot: [void@puppet181] Upgraded packages on mw203: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 19:39 MirahezeLSBot: [void@puppet181] Upgraded packages on mw181: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 19:39 MirahezeLSBot: [void@puppet181] Upgraded packages on mw182: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 19:39 MirahezeLSBot: [void@puppet181] Upgraded packages on mw202: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 19:38 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask161: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 19:38 MirahezeLSBot: [void@puppet181] Upgraded packages on mw201: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 19:38 MirahezeLSBot: [void@puppet181] Upgraded packages on mw193: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 19:38 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask171: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 19:37 MirahezeLSBot: [void@puppet181] Upgraded packages on mwtask151: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 19:37 MirahezeLSBot: [void@puppet181] Upgraded packages on mw173: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 19:37 MirahezeLSBot: [void@puppet181] Upgraded packages on mw161: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 19:36 MirahezeLSBot: [void@puppet181] Upgraded packages on mw162: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 19:36 MirahezeLSBot: [void@puppet181] Upgraded packages on mw152: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 19:36 MirahezeLSBot: [void@puppet181] Upgraded packages on mw171: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 19:35 MirahezeLSBot: [void@puppet181] Upgraded packages on mw151: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 19:35 MirahezeLSBot: [void@puppet181] Upgraded packages on mw172: libimage-magick-perl, imagemagick-7-common, libmagickcore-7.q16-10, libimage-magick-q16-perl, libmagickwand-7.q16-10, imagemagick-7.q16, imagemagick, and libmagickcore-7.q16-10-extra
* 16:03 SomeRandomDeveloper: repool c1 (hopefully for the last time)
* 16:02 MirahezeLSBot: [somerandomdeveloper@mwtask181] finished deploy of {'config': True, 'force': True} to all - SUCCESS in 18s
* 16:02 MirahezeLSBot: [somerandomdeveloper@mwtask181] starting deploy of {'config': True, 'force': True} to all
* 15:39 MirahezeLSBot: [somerandomdeveloper@mwtask181] starting deploy of {'config': True, 'force': True} to all
* 15:38 SomeRandomDeveloper: repool c1
* 15:38 MirahezeLSBot: [somerandomdeveloper@mwtask181] finished deploy of {'config': True, 'force': True} to all - SUCCESS in 18s
* 15:37 MirahezeLSBot: [somerandomdeveloper@mwtask181] starting deploy of {'config': True, 'force': True} to all
* 15:32 MirahezeLSBot: [somerandomdeveloper@mwtask181] finished deploy of {'config': True, 'force': True} to all - SUCCESS in 18s
* 15:32 MirahezeLSBot: [somerandomdeveloper@mwtask181] starting deploy of {'config': True, 'force': True} to all
* 15:27 MirahezeLSBot: [somerandomdeveloper@mwtask181] finished deploy of {'config': True, 'force': True} to all - SUCCESS in 19s
* 10:09 MirahezeLSBot: [petramagna@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 25s
* 10:09 MirahezeLSBot: [petramagna@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 10:07 MirahezeLSBot: [petramagna@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 10:07 MirahezeLSBot: [petramagna@test151] starting deploy of {'config': True} to test151
* 10:06 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php /srv/mediawiki/1.45/maintenance/importDump.php --wiki=unanythingwiki --username-prefix=unanything /home/reception/unanything_pages_full.xml (END - exit=256)
* 09:29 MirahezeLSBot: [petramagna@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 09:29 MirahezeLSBot: [petramagna@test151] starting deploy of {'config': True} to test151
* 08:07 MirahezeLSBot: [petramagna@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 08:07 MirahezeLSBot: [petramagna@test151] starting deploy of {'config': True} to test151
* 05:34 MirahezeLSBot: [petramagna@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 26s
* 05:33 MirahezeLSBot: [petramagna@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 05:31 MirahezeLSBot: [petramagna@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 05:31 MirahezeLSBot: [petramagna@test151] starting deploy of {'config': True} to test151
* 00:00 MirahezeLSBot: [www-data@mwtask181] Began automatic backing up

----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:Server_admin_log/2026-05)**