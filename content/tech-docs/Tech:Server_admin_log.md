---
title: Tech:Server admin log
---

## 2025-02-27 

* 18:52 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'config': True, 'world': True, 'landing': True, 'errorpages': True, 'l10n': True, 'force': True, 'versions': '1.43'} to [mw201, mw202, mw203]
* 18:38 RhinosF1: shift fischwiki to cp38
* 18:02 MirahezeLSBot: [paladox@mwtask181] finished deploy of {'config': True, 'world': True, 'landing': True, 'errorpages': True, 'l10n': True, 'force': True, 'versions': '1.43'} to [mw191, mw192, mw193] - SUCCESS in 17s
* 18:01 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'config': True, 'world': True, 'landing': True, 'errorpages': True, 'l10n': True, 'force': True, 'versions': '1.43'} to [mw191, mw192, mw193]
* 16:42 MirahezeLSBot: [paladox@mwtask181] finished deploy of {'force': True, 'files': 'cache/databases.php'} to [mw191, mw192, mw193] - SUCCESS in 6s
* 16:42 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'force': True, 'files': 'cache/databases.php'} to [mw191, mw192, mw193]
* 16:39 MirahezeLSBot: [paladox@mwtask181] finished deploy of {'force': True, 'files': '/srv/mediawiki/cache/databases.php'} to [mw191, mw192, mw193] - FAIL: [768]
* 16:39 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'force': True, 'files': '/srv/mediawiki/cache/databases.php'} to [mw191, mw192, mw193]
* 16:36 MirahezeLSBot: [paladox@mwtask181] finished deploy of {'config': True, 'world': True, 'landing': True, 'errorpages': True, 'l10n': True, 'force': True, 'versions': '1.43'} to [mw191, mw192, mw193] - SUCCESS in 16s
* 16:35 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'config': True, 'world': True, 'landing': True, 'errorpages': True, 'l10n': True, 'force': True, 'versions': '1.43'} to [mw191, mw192, mw193]
* 16:35 MirahezeLSBot: [paladox@mwtask181] finished deploy of {'config': True, 'world': True, 'errorpages': True, 'l10n': True, 'force': True, 'versions': '1.43'} to [mw191, mw192, mw193] - SUCCESS in 81s
* 16:34 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'config': True, 'world': True, 'errorpages': True, 'l10n': True, 'force': True, 'versions': '1.43'} to [mw191, mw192, mw193]
* 14:55 RhinosF1: increase cp38 traffic from 25% to 50% (fully pooled)
* 14:30 MirahezeLSBot: [paladox@mwtask181] finished deploy of {'l10n': True, 'versions': '1.43', 'upgrade_extensions': 'CreateWiki'} to all - SUCCESS in 200s
* 14:27 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'l10n': True, 'versions': '1.43', 'upgrade_extensions': 'CreateWiki'} to all
* 14:25 MirahezeLSBot: [paladox@test151] finished deploy of {'l10n': True, 'versions': ['1.43', '1.44'], 'upgrade_extensions': 'CreateWiki'} to test151 - SUCCESS in 565s
* 14:23 MirahezeLSBot: [paladox@mwtask181] DEPLOY ABORTED: Canary check failed for publictestwiki.com@mw151.wikitide.net
* 14:18 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'l10n': True, 'versions': '1.43', 'upgrade_extensions': 'CreateWiki'} to all
* 14:16 MirahezeLSBot: [paladox@test151] starting deploy of {'l10n': True, 'versions': ['1.43', '1.44'], 'upgrade_extensions': 'CreateWiki'} to test151
* 14:14 RhinosF1: ramp cp38 up to 25% of traffic
* 14:13 MirahezeLSBot: [paladox@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 18s
* 14:13 MirahezeLSBot: [paladox@test151] finished deploy of {'pull': 'config', 'config': True} to test151 - SUCCESS in 1s
* 14:13 MirahezeLSBot: [paladox@test151] starting deploy of {'pull': 'config', 'config': True} to test151
* 14:13 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 14:07 MirahezeLSBot: [paladox@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 18s
* 14:06 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 14:02 RhinosF1: pool cp38 to 10% of traffic
* 13:33 RhinosF1: add cp38 to cf and disable it
* 13:31 RhinosF1: delete cp36 from cf
* 12:09 RhinosF1: double cache times for new cf caches
* 01:04 MirahezeLSBot: [void@cloud15] clear ipmi sel (resolved inlet temperature alerts)
* 00:27 MirahezeLSBot: [void@cloud20.wikitide.net] clear ipmi sel (contained some resolved inlet temperature alerts)

## 2025-02-26 

* 23:00 Universal Omega: add cloud19 and cloud20 to proxmox cluster
* 22:37 Universal Omega: add cloud19 and cloud20 to puppet
* 22:28 MirahezeLSBot: [paladox@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 20s
* 22:28 MirahezeLSBot: [paladox@test151] finished deploy of {'pull': 'config', 'config': True} to test151 - SUCCESS in 0s
* 22:28 MirahezeLSBot: [paladox@test151] starting deploy of {'pull': 'config', 'config': True} to test151
* 22:28 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 22:21 Universal Omega: set hostname, setup networking, and apt upgrade and reboot on cloud19 and cloud20
* 18:27 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/rebuildall.php --wiki=trollpastawiki (END - exit=0)
* 18:12 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/rebuildall.php --wiki=spongebobfanonwiki (END - exit=2)
* 18:12 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/rebuildall.php --wiki=spongebobfanonwiki (START)
* 18:12 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/importDump.php --wiki=spongebobfanonwiki dump.xml --no-updates (END - exit=2)
* 17:10 Universal Omega: reboot mattermost1
* 15:28 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/rebuildall.php --wiki=trollpastawiki (START)
* 15:25 MirahezeLSBot: [paladox@test151] finished deploy of {'l10n': True, 'versions': ['1.43', '1.44'], 'upgrade_extensions': ['CreateWiki', 'SimpleBlogPage']} to test151 - SUCCESS in 377s
* 15:23 MirahezeLSBot: [paladox@mwtask181] finished deploy of {'l10n': True, 'versions': '1.43', 'upgrade_extensions': ['CreateWiki', 'SimpleBlogPage']} to all - SUCCESS in 487s
* 15:19 MirahezeLSBot: [paladox@test151] starting deploy of {'l10n': True, 'versions': ['1.43', '1.44'], 'upgrade_extensions': ['CreateWiki', 'SimpleBlogPage']} to test151
* 15:16 MirahezeLSBot: [paladox@test151] DEPLOY ABORTED: Non-Zero Exit Code in prep, see output.
* 15:15 MirahezeLSBot: [paladox@test151] starting deploy of {'l10n': True, 'versions': ['1.43', '1.44'], 'upgrade_extensions': 'CreateWiki'} to test151
* 15:15 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'l10n': True, 'versions': '1.43', 'upgrade_extensions': ['CreateWiki', 'SimpleBlogPage']} to all
* 13:40 MirahezeLSBot: [paladox@test151] DEPLOY ABORTED: Non-Zero Exit Code in prep, see output.
* 13:40 MirahezeLSBot: [paladox@mwtask181] DEPLOY ABORTED: Non-Zero Exit Code in prep, see output.
* 13:40 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'l10n': True, 'versions': '1.43', 'upgrade_extensions': ['CreateWiki', 'SimpleBlogPage']} to all
* 13:35 MirahezeLSBot: [paladox@test151] starting deploy of {'l10n': True, 'versions': ['1.43', '1.44'], 'upgrade_extensions': 'CreateWiki'} to test151
* 13:35 MirahezeLSBot: [paladox@mwtask181] DEPLOY ABORTED: Non-Zero Exit Code in prep, see output.
* 13:35 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'l10n': True, 'versions': '1.43', 'upgrade_extensions': 'CreateWiki'} to all
* 02:26 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/importDump.php --wiki=spongebobfanonwiki dump.xml --no-updates (START)

## 2025-02-25 

* 16:22 RhinosF1: cache static.wikitide.net for 5 minutes; cache /1.43/ for 30 minutes
* 13:50 MirahezeLSBot: [paladox@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 22s
* 13:50 MirahezeLSBot: [paladox@test151] finished deploy of {'pull': 'config', 'config': True} to test151 - SUCCESS in 1s
* 13:50 MirahezeLSBot: [paladox@test151] starting deploy of {'pull': 'config', 'config': True} to test151
* 13:50 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 10:15 MirahezeLSBot: [blankeclair@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php rebuildall --wiki=hcmwiki (END - exit=0)
* 10:13 MirahezeLSBot: [blankeclair@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php rebuildall --wiki=hcmwiki (START)
* 10:13 MirahezeLSBot: [blankeclair@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php importImages --wiki=hcmwiki /home/blankeclair/images --comment='Importing file per request ([T13259](https://meta.miraheze.org/wiki/phorge:T13259))' --search-recursively (END - exit=0)
* 10:13 MirahezeLSBot: [blankeclair@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php importImages --wiki=hcmwiki /home/blankeclair/images --comment='Importing file per request ([T13259](https://meta.miraheze.org/wiki/phorge:T13259))' --search-recursively (START)
* 10:13 MirahezeLSBot: [blankeclair@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php importImages --wiki=hcmwiki /home/blankeclair/images --comment=Importing file per request ([T13259](https://meta.miraheze.org/wiki/phorge:T13259)) --search-recursively (END - exit=512)
* 10:13 MirahezeLSBot: [blankeclair@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php importImages --wiki=hcmwiki /home/blankeclair/images --comment=Importing file per request ([T13259](https://meta.miraheze.org/wiki/phorge:T13259)) --search-recursively (START)
* 09:04 MirahezeLSBot: [blankeclair@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php importDump --wiki=hcmwiki /home/blankeclair/mediawiki-20250221-history.xml --no-updates --report 100 (END - exit=0)
* 08:58 MirahezeLSBot: [blankeclair@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php importDump --wiki=hcmwiki /home/blankeclair/mediawiki-20250221-history.xml --no-updates --report 100 (START)
* 08:05 MirahezeLSBot: [universalomega@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 20s
* 08:05 MirahezeLSBot: [universalomega@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 04:34 Universal Omega: created BlankEclair's email login

## 2025-02-22 

* 22:26 MirahezeLSBot: [void@cp37] delete old nginx logs and manually trigger logrotate to compress logs
* 18:02 MirahezeLSBot: [macfan@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 22s
* 18:01 MirahezeLSBot: [macfan@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all

## 2025-02-21 

* 20:43 MirahezeLSBot: [macfan@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 20s
* 20:43 MirahezeLSBot: [macfan@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all

## 2025-02-20 

* 06:06 MirahezeLSBot: [reception@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 19s
* 06:05 MirahezeLSBot: [reception@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 01:22 MirahezeLSBot: [oa@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/sql.php --wiki=loginwiki --wikidb mhglobal /srv/mediawiki/1.43/extensions/GlobalBlocking/sql/mysql/patch-global_block_whitelist-default-gbw_address.sql (END - exit=0)
* 01:21 MirahezeLSBot: [oa@mwtask181] finished deploy of {'world': True, 'versions': '1.43', 'upgrade_extensions': 'GlobalBlocking'} to all - SUCCESS in 151s
* 01:19 MirahezeLSBot: [oa@mwtask181] starting deploy of {'world': True, 'versions': '1.43', 'upgrade_extensions': 'GlobalBlocking'} to all
* 01:16 MirahezeLSBot: [oa@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/sql.php --wiki=loginwiki --wikidb mhglobal /srv/mediawiki/1.43/extensions/GlobalBlocking/sql/mysql/patch-global_block_whitelist-default-gbw_address.sql (END - exit=0)

## 2025-02-19 

* 20:12 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/initSiteStats.php --wiki=jbcstudioswiki --update (END - exit=0)
* 20:12 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/rebuildall.php --wiki=jbcstudioswiki (END - exit=0)
* 19:30 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/rebuildall.php --wiki=jbcstudioswiki (START)
* 19:30 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/importDump.php --wiki=jbcstudioswiki cooleritemasylum_pages_full.xml --no-updates (END - exit=0)
* 17:22 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/extensions/MirahezeMagic/maintenance/replaceTextEligible.php --wiki=pandorastalewiki (END - exit=0)
* 16:32 MirahezeLSBot: [reception@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 22s
* 16:31 MirahezeLSBot: [reception@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 15:51 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/refreshLinks.php --wiki=metawiki (START)
* 15:51 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/refreshLinks.php --wiki=shintowiki (START)
* 15:50 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/importDump.php --wiki=jbcstudioswiki cooleritemasylum_pages_full.xml --no-updates (START)
* 06:10 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/extensions/MirahezeMagic/maintenance/renameDatabase.php --wiki=loginwiki --old=the51stinfernocompanywiki --new=51stinfernocompanywiki (END - exit=0)

## 2025-02-18 

* 23:52 MirahezeLSBot: [macfan@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 20s
* 23:52 MirahezeLSBot: [macfan@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 23:51 MirahezeLSBot: [macfan@test151] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php /srv/mediawiki/1.44/extensions/ManageWiki/maintenance/toggleExtension.php --wiki=metawikibeta cirrussearch --disable (END - exit=0)
* 23:50 MirahezeLSBot: [macfan@test151] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php /srv/mediawiki/1.44/extensions/ManageWiki/maintenance/toggleExtension.php --wiki=metawikibeta growthexperiments --disable (END - exit=0)
* 23:49 MirahezeLSBot: [macfan@test151] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php /srv/mediawiki/1.44/extensions/ManageWiki/maintenance/toggleExtension.php --wiki=metawikibeta GrowthExperiments --disable (END - exit=0)
* 23:48 MirahezeLSBot: [macfan@test151] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php /srv/mediawiki/1.44/extensions/ManageWiki/maintenance/toggleExtension.php --wiki=metawikibeta CirrusSearch --disable (END - exit=0)
* 23:48 MirahezeLSBot: [macfan@test151] sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php /srv/mediawiki/1.44/extensions/ManageWiki/maintenance/togleExtension.php --wiki=metawikibeta CirrusSearch (END - exit=256)
* 23:46 MirahezeLSBot: [macfan@test151] finished deploy of {'pull': 'config', 'config': True} to test151 - SUCCESS in 1s
* 23:46 MirahezeLSBot: [macfan@test151] starting deploy of {'pull': 'config', 'config': True} to test151
* 21:37 Universal Omega: upgrade opensearch to 2.19.0
* 20:52 MirahezeLSBot: [universalomega@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 21s
* 20:52 MirahezeLSBot: [universalomega@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 19:11 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/importImages.php --wiki=chidurianwikiwiki images --search-recursively (END - exit=0)
* 18:57 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/importImages.php --wiki=chidurianwikiwiki images --search-recursively (START)
* 16:40 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/importImages.php --wiki=mythcommunitywiki images --search-recursively (END - exit=0)
* 16:04 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/importImages.php --wiki=mythcommunitywiki images --search-recursively (START)
* 05:31 MirahezeLSBot: [macfan@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 20s
* 05:31 MirahezeLSBot: [macfan@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all

## 2025-02-15 

* 20:26 MirahezeLSBot: [universalomega@mwtask181] finished deploy of {'l10n': True, 'versions': '1.43'} to all - SUCCESS in 454s
* 20:18 MirahezeLSBot: [universalomega@mwtask181] starting deploy of {'l10n': True, 'versions': '1.43'} to all
* 20:18 MirahezeLSBot: [universalomega@mwtask181] finished deploy of {'versions': '1.43', 'upgrade_extensions': 'CreateWiki'} to all - SUCCESS in 20s
* 20:18 MirahezeLSBot: [universalomega@mwtask181] starting deploy of {'versions': '1.43', 'upgrade_extensions': 'CreateWiki'} to all
* 20:17 MirahezeLSBot: [universalomega@mwtask181] finished deploy of {'versions': '1.43', 'upgrade_skins': ['DuskToDawn', 'Mask', 'Refreshed']} to all - SUCCESS in 59s
* 20:16 MirahezeLSBot: [universalomega@mwtask181] starting deploy of {'versions': '1.43', 'upgrade_skins': ['DuskToDawn', 'Mask', 'Refreshed']} to all
* 19:54 MirahezeLSBot: [universalomega@test151] finished deploy of {'world': True, 'versions': '1.44', 'ignore_time': True} to test151 - SUCCESS in 49s
* 19:53 MirahezeLSBot: [universalomega@test151] starting deploy of {'world': True, 'versions': '1.44', 'ignore_time': True} to test151
* 18:31 MirahezeLSBot: [universalomega@test151] finished deploy of {'versions': '1.44', 'upgrade_extensions': 'CreateWiki'} to test151 - SUCCESS in 1s
* 18:31 MirahezeLSBot: [universalomega@test151] starting deploy of {'versions': '1.44', 'upgrade_extensions': 'CreateWiki'} to test151
* 18:31 MirahezeLSBot: [universalomega@test151] finished deploy of {'pull': 'config', 'config': True} to test151 - SUCCESS in 0s
* 18:31 MirahezeLSBot: [universalomega@test151] starting deploy of {'pull': 'config', 'config': True} to test151
* 16:28 @paladox: upgrade phorge

## 2025-02-14 

* 19:01 MirahezeLSBot: [universalomega@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 20s
* 19:00 MirahezeLSBot: [universalomega@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 18:53 MirahezeLSBot: [universalomega@mwtask181] finished deploy of {'versions': '1.43', 'upgrade_pack': 'wikitide'} to all - SUCCESS in 227s
* 18:49 MirahezeLSBot: [universalomega@mwtask181] starting deploy of {'versions': '1.43', 'upgrade_pack': 'wikitide'} to all
* 18:49 MirahezeLSBot: [universalomega@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 20s
* 18:48 MirahezeLSBot: [universalomega@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 18:36 Universal Omega: destroy graphite151 VM
* 18:27 Universal Omega: remove graphite151 from puppet
* 15:36 MirahezeLSBot: [paladox@test151] finished deploy of {'force_upgrade': True, 'versions': ['1.43', '1.44'], 'upgrade_extensions': 'Cargo'} to test151 - SUCCESS in 1s
* 15:36 MirahezeLSBot: [paladox@test151] starting deploy of {'force_upgrade': True, 'versions': ['1.43', '1.44'], 'upgrade_extensions': 'Cargo'} to test151
* 15:36 MirahezeLSBot: [paladox@mwtask181] finished deploy of {'force_upgrade': True, 'versions': '1.43', 'upgrade_extensions': 'Cargo'} to all - SUCCESS in 20s
* 15:36 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'force_upgrade': True, 'versions': '1.43', 'upgrade_extensions': 'Cargo'} to all
* 13:20 MirahezeLSBot: [paladox@mwtask181] finished deploy of {'force_upgrade': True, 'versions': '1.43', 'upgrade_extensions': 'Cargo'} to all - SUCCESS in 19s
* 13:19 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'force_upgrade': True, 'versions': '1.43', 'upgrade_extensions': 'Cargo'} to all
* 13:10 MirahezeLSBot: [paladox@mwtask181] finished deploy of {'force_upgrade': True, 'versions': '1.43', 'upgrade_extensions': 'Cargo'} to all - SUCCESS in 19s
* 13:10 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'force_upgrade': True, 'versions': '1.43', 'upgrade_extensions': 'Cargo'} to all
* 12:37 MirahezeLSBot: [paladox@mwtask181] finished deploy of {'force_upgrade': True, 'versions': '1.43', 'upgrade_extensions': 'Cargo'} to all - SUCCESS in 48s
* 12:36 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'force_upgrade': True, 'versions': '1.43', 'upgrade_extensions': 'Cargo'} to all
* 12:36 MirahezeLSBot: [paladox@mwtask181] finished deploy of {'versions': '1.43', 'upgrade_extensions': 'Cargo'} to all - SUCCESS in 2s
* 12:36 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'versions': '1.43', 'upgrade_extensions': 'Cargo'} to all
* 08:59 MirahezeLSBot: [universalomega@test151] finished deploy of {'versions': ['1.43', '1.44'], 'upgrade_pack': 'universalomega'} to test151 - SUCCESS in 10s
* 08:58 MirahezeLSBot: [universalomega@test151] starting deploy of {'versions': ['1.43', '1.44'], 'upgrade_pack': 'universalomega'} to test151
* 08:54 MirahezeLSBot: [universalomega@test151] finished deploy of {'versions': ['1.43', '1.44'], 'upgrade_pack': 'wikitide'} to test151 - SUCCESS in 18s
* 08:54 MirahezeLSBot: [universalomega@test151] starting deploy of {'versions': ['1.43', '1.44'], 'upgrade_pack': 'wikitide'} to test151
* 08:53 MirahezeLSBot: [universalomega@test151] finished deploy of {'pull': 'config', 'config': True} to test151 - SUCCESS in 1s
* 08:53 MirahezeLSBot: [universalomega@test151] starting deploy of {'pull': 'config', 'config': True} to test151
* 06:17 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/extensions/MirahezeMagic/maintenance/renameDatabase.php --wiki=loginwiki --old=tyrillianencyclopediawiki --new=tyrillymwiki (END - exit=0)
* 06:16 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/extensions/MirahezeMagic/maintenance/checkSwiftContainers.php --wiki=metawiki --delete (END - exit=0)
* 06:15 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/extensions/MirahezeMagic/maintenance/renameDatabase.php --wiki=loginwiki --old=wildcardsrchivewiki --new=wildcardarchivewiki (END - exit=0)
* 06:14 MirahezeLSBot: [reception@mwtask181] finished deploy of {'versions': '1.43', 'upgrade_extensions': 'MirahezeMagic'} to all - SUCCESS in 21s
* 06:14 MirahezeLSBot: [reception@mwtask181] starting deploy of {'versions': '1.43', 'upgrade_extensions': 'MirahezeMagic'} to all
* 06:05 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/extensions/MirahezeMagic/maintenance/checkSwiftContainers.php --wiki=metawiki --delete (START)
* 05:54 Reception123: swift delete miraheze-animatedmusclewomenwiki-local-thumb (not deleted when the wiki was?)
* 05:51 Reception123: swift delete miraheze-removededmsongswiki-local-transcoded

## 2025-02-13 

* 23:56 MirahezeLSBot: [paladox@mwtask181] finished deploy of {'l10n': True, 'versions': '1.43', 'upgrade_extensions': 'Cargo'} to all - SUCCESS in 469s
* 23:50 MirahezeLSBot: [paladox@test151] finished deploy of {'l10n': True, 'versions': ['1.43', '1.44'], 'upgrade_extensions': 'Cargo'} to test151 - SUCCESS in 115s
* 23:49 MirahezeLSBot: [paladox@test151] starting deploy of {'l10n': True, 'versions': ['1.43', '1.44'], 'upgrade_extensions': 'Cargo'} to test151
* 23:48 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'l10n': True, 'versions': '1.43', 'upgrade_extensions': 'Cargo'} to all
* 23:20 Universal Omega: UPDATE cw_requests SET cw_status = 'inreview' WHERE cw_id = '54640';
* 16:18 MirahezeLSBot: [reception@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 21s
* 16:18 MirahezeLSBot: [reception@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 15:42 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/extensions/CirrusSearch/maintenance/ForceSearchIndex.php --wiki=snowmanwiki --skipParse (END - exit=0)
* 15:42 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/extensions/CirrusSearch/maintenance/ForceSearchIndex.php --wiki=snowmanwiki --skipLinks --indexOnSkip (END - exit=0)
* 15:41 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/extensions/CirrusSearch/maintenance/UpdateSearchIndexConfig.php --wiki=snowmanwiki (END - exit=0)
* 15:40 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/extensions/CirrusSearch/maintenance/ForceSearchIndex.php --wiki=vroomstatswiki --skipParse (END - exit=0)
* 15:40 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/extensions/CirrusSearch/maintenance/ForceSearchIndex.php --wiki=vroomstatswiki --skipLinks --indexOnSkip (END - exit=0)
* 15:40 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/extensions/CirrusSearch/maintenance/UpdateSearchIndexConfig.php --wiki=vroomstatswiki (END - exit=0)
* 15:39 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/extensions/CirrusSearch/maintenance/ForceSearchIndex.php --wiki=vroomstatswiki --skipParse (END - exit=256)
* 15:39 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/extensions/CirrusSearch/maintenance/ForceSearchIndex.php --wiki=vroomstatswiki --skipLinks --indexOnSkip (END - exit=256)
* 15:39 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/extensions/CirrusSearch/maintenance/UpdateSearchIndexConfig.php --wiki=vroomstatswiki (END - exit=256)
* 15:36 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/extensions/CirrusSearch/maintenance/ForceSearchIndex.php --wiki=historikawiki --skipLinks --indexOnSkip (END - exit=0)
* 15:36 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/extensions/CirrusSearch/maintenance/UpdateSearchIndexConfig.php --wiki=historikawiki (END - exit=0)
* 15:36 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/extensions/CirrusSearch/maintenance/ForceSearchIndex.php --wiki=blocklandwiki --skipParse (END - exit=0)
* 15:36 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/extensions/CirrusSearch/maintenance/ForceSearchIndex.php --wiki=blocklandwiki --skipLinks --indexOnSkip (END - exit=0)
* 15:36 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/extensions/CirrusSearch/maintenance/UpdateSearchIndexConfig.php --wiki=blocklandwiki (END - exit=0)
* 15:36 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/extensions/CirrusSearch/maintenance/ForceSearchIndex.php --wiki=maskoftherosewiki --skipParse (END - exit=0)
* 15:36 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/extensions/CirrusSearch/maintenance/ForceSearchIndex.php --wiki=maskoftherosewiki --skipLinks --indexOnSkip (END - exit=0)
* 15:35 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/extensions/CirrusSearch/maintenance/UpdateSearchIndexConfig.php --wiki=maskoftherosewiki (END - exit=0)
* 15:35 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/extensions/CirrusSearch/maintenance/ForceSearchIndex.php --wiki=sunlessskieswiki --skipParse (END - exit=0)
* 15:35 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/extensions/CirrusSearch/maintenance/ForceSearchIndex.php --wiki=sunlessskieswiki --skipLinks --indexOnSkip (END - exit=0)
* 15:35 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/extensions/CirrusSearch/maintenance/UpdateSearchIndexConfig.php --wiki=sunlessskieswiki (END - exit=0)
* 15:35 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/extensions/CirrusSearch/maintenance/ForceSearchIndex.php --wiki=sunlessseawiki --skipParse (END - exit=0)
* 15:34 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/extensions/CirrusSearch/maintenance/ForceSearchIndex.php --wiki=sunlessseawiki --skipLinks --indexOnSkip (END - exit=0)
* 15:34 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/extensions/CirrusSearch/maintenance/UpdateSearchIndexConfig.php --wiki=sunlessseawiki (END - exit=0)
* 12:24 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/deleteBatch.php --wiki=mythcommunitywiki /home/reception/mythcommunitydel.txt --r=Deletion of Fandom leftovers per T13165 (END - exit=0)
* 12:15 MirahezeLSBot: [reception@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 38s
* 12:15 MirahezeLSBot: [reception@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 12:04 MirahezeLSBot: [reception@mwtask181] finished deploy of {'versions': '1.43', 'upgrade_extensions': 'NoTitle'} to all - SUCCESS in 20s
* 12:03 MirahezeLSBot: [reception@mwtask181] starting deploy of {'versions': '1.43', 'upgrade_extensions': 'NoTitle'} to all
* 12:01 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/deleteBatch.php --wiki=mythcommunitywiki /home/reception/mythcommunitydel.txt --r=Deletion of Fandom leftovers per T13165 (START)
* 11:46 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/extensions/WikiSEO/maintenance/GenerateDescription.php --wiki=gimkitwiki 0 (END - exit=0)
* 11:28 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/invalidateUserSessions.php --wiki=metawiki --user=Emperore (END - exit=0)
* 11:28 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/invalidateUserSessions.php --wiki=wehrmachtwiki --user=Emperore (END - exit=0)
* 11:28 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/invalidateUserSessions.php --wiki=--wiki=wehrmachtwiki --user=Emperore (END - exit=0)
* 11:27 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/invalidateUserSessions.php --wiki=--wiki=wehrmachtwiki --user=Emperore (END - exit=0)
* 07:35 Reception123: sudo -u www-data /usr/local/bin/foreachwikiindblist /tmp/dynamicpagelist3.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/extensions/DynamicPageList3/maintenance/CreateView.php --recreate --force
* 07:11 Reception123: MariaDB [weaverswiki]> DROP VIEW weaverswiki.dpl_clview;
* 07:09 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/sql.php --wiki=weaverswiki (END - exit=2)
* 07:07 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/extensions/MirahezeMagic/maintenance/renameDatabase.php --wiki=loginwiki --old=weaverswiki --new=jjtwiki (END - exit=256)
* 07:06 MirahezeLSBot: [reception@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 20s
* 07:06 MirahezeLSBot: [reception@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 07:01 MirahezeLSBot: [reception@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 20s
* 07:01 MirahezeLSBot: [reception@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 06:59 MirahezeLSBot: [reception@mwtask181] finished deploy of {'world': True, 'versions': '1.43'} to all - SUCCESS in 153s
* 06:58 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/purgeList.php --wiki=battlenationswiki --all-namespaces (END - exit=0)
* 06:57 MirahezeLSBot: [reception@mwtask181] starting deploy of {'world': True, 'versions': '1.43'} to all
* 06:56 MirahezeLSBot: [reception@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 20s
* 06:55 MirahezeLSBot: [reception@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 06:53 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/purgeList.php --wiki=battlenationswiki --all-namespaces (START)
* 04:20 MirahezeLSBot: [macfan@test151] finished deploy of {'l10n': True, 'force_upgrade': True, 'versions': ['1.43', '1.44'], 'upgrade_extensions': ['MirahezeMagic', 'RequestSSL']} to test151 - SUCCESS in 383s
* 04:17 MirahezeLSBot: [macfan@mwtask181] finished deploy of {'l10n': True, 'versions': '1.43', 'upgrade_extensions': ['MirahezeMagic', 'RequestSSL']} to all - SUCCESS in 440s
* 04:14 MirahezeLSBot: [macfan@test151] starting deploy of {'l10n': True, 'force_upgrade': True, 'versions': ['1.43', '1.44'], 'upgrade_extensions': ['MirahezeMagic', 'RequestSSL']} to test151
* 04:14 MirahezeLSBot: [macfan@test151] DEPLOY ABORTED: Non-Zero Exit Code in prep, see output.
* 04:10 MirahezeLSBot: [macfan@mwtask181] starting deploy of {'l10n': True, 'versions': '1.43', 'upgrade_extensions': ['MirahezeMagic', 'RequestSSL']} to all
* 04:10 MirahezeLSBot: [macfan@test151] starting deploy of {'l10n': True, 'force_upgrade': True, 'versions': '1.44', 'upgrade_extensions': ['MirahezeMagic', 'RequestSSL']} to test151
* 03:59 MirahezeLSBot: [macfan@test151] finished deploy of {'force_upgrade': True, 'versions': '1.44', 'upgrade_extensions': 'RequestSSL'} to test151 - SUCCESS in 1s
* 03:59 MirahezeLSBot: [macfan@test151] starting deploy of {'force_upgrade': True, 'versions': '1.44', 'upgrade_extensions': 'RequestSSL'} to test151
* 03:49 MirahezeLSBot: [macfan@test151] finished deploy of {'force_upgrade': True, 'versions': '1.44', 'upgrade_extensions': 'RequestSSL'} to test151 - SUCCESS in 1s
* 03:49 MirahezeLSBot: [macfan@test151] starting deploy of {'force_upgrade': True, 'versions': '1.44', 'upgrade_extensions': 'RequestSSL'} to test151
* 02:58 MirahezeLSBot: [macfan@test151] finished deploy of {'l10n': True, 'force_upgrade': True, 'versions': '1.44', 'upgrade_extensions': 'RequestSSL'} to test151 - SUCCESS in 278s
* 02:53 MirahezeLSBot: [macfan@test151] starting deploy of {'l10n': True, 'force_upgrade': True, 'versions': '1.44', 'upgrade_extensions': 'RequestSSL'} to test151
* 02:51 MirahezeLSBot: [macfan@test151] finished deploy of {'force_upgrade': True, 'versions': '1.44', 'upgrade_extensions': 'RequestSSL'} to test151 - SUCCESS in 0s
* 02:51 MirahezeLSBot: [macfan@test151] starting deploy of {'force_upgrade': True, 'versions': '1.44', 'upgrade_extensions': 'RequestSSL'} to test151
* 02:47 MirahezeLSBot: [macfan@test151] finished deploy of {'force_upgrade': True, 'versions': '1.44', 'upgrade_extensions': 'RequestSSL'} to test151 - SUCCESS in 0s
* 02:47 MirahezeLSBot: [macfan@test151] starting deploy of {'force_upgrade': True, 'versions': '1.44', 'upgrade_extensions': 'RequestSSL'} to test151
* 02:47 MirahezeLSBot: [macfan@test151] finished deploy of {'versions': '1.44', 'upgrade_extensions': 'RequestSSL'} to test151 - SUCCESS in 0s
* 02:47 MirahezeLSBot: [macfan@test151] starting deploy of {'versions': '1.44', 'upgrade_extensions': 'RequestSSL'} to test151
* 02:18 MirahezeLSBot: [macfan@mwtask181] finished deploy of {'versions': '1.43', 'upgrade_extensions': 'RequestSSL'} to all - SUCCESS in 21s
* 02:17 MirahezeLSBot: [macfan@mwtask181] starting deploy of {'versions': '1.43', 'upgrade_extensions': 'RequestSSL'} to all
* 02:17 MirahezeLSBot: [macfan@test151] finished deploy of {'versions': ['1.43', '1.44'], 'upgrade_extensions': 'RequestSSL'} to test151 - SUCCESS in 1s
* 02:17 MirahezeLSBot: [macfan@test151] starting deploy of {'versions': ['1.43', '1.44'], 'upgrade_extensions': 'RequestSSL'} to test151
* 02:16 MirahezeLSBot: [macfan@test151] finished deploy of {'versions': '1.44', 'upgrade_extensions': 'RequestSSL'} to test151 - SUCCESS in 1s
* 02:16 MirahezeLSBot: [macfan@test151] starting deploy of {'versions': '1.44', 'upgrade_extensions': 'RequestSSL'} to test151

## 2025-02-12 

* 20:52 MirahezeLSBot: [universalomega@mwtask181] sudo -u www-data /usr/local/bin/foreachwikiindblist /tmp/dynamicpagelist3.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/extensions/DynamicPageList3/maintenance/CreateView.php --recreate --force (END - exit=0)
* 20:44 MirahezeLSBot: [universalomega@mwtask181] sudo -u www-data /usr/local/bin/foreachwikiindblist /tmp/dynamicpagelist3.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/extensions/DynamicPageList3/maintenance/CreateView.php --recreate --force (START)
* 20:39 MirahezeLSBot: [universalomega@bots171] Restart irclogserverbot
* 20:22 Universal Omega: destroy jobchron171 VM
* 20:13 Universal Omega: remove jobchron171 from puppet
* 07:01 Reception123: DELETE wiki animatedmusclewomenwiki
* 06:42 Reception123: > UPDATE page SET page_namespace = '4' WHERE page_id = '3'; UPDATE page SET page_namespace = '4' WHERE page_id = '193'; (ssbuniversewiki)
* 06:31 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/rebuildall.php --wiki=ssbuniversewiki (END - exit=0)
* 06:30 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/rebuildall.php --wiki=ssbuniversewiki (START)
* 06:30 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/cleanupTitles.php --wiki=ssbuniversewiki (END - exit=0)
* 06:30 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/cleanupTitles.php --wiki=ssbuniverseswiki (END - exit=65280)

## 2025-02-11 

* 21:58 MirahezeLSBot: [void@puppet181] Upgraded packages linux-libc-dev, and libtasn1-6 on swiftobject181
* 21:58 MirahezeLSBot: [void@puppet181] Upgraded packages linux-libc-dev, and libtasn1-6 on swiftobject161
* 21:58 MirahezeLSBot: [void@puppet181] Upgraded packages linux-libc-dev, and libtasn1-6 on swiftproxy161
* 21:58 MirahezeLSBot: [void@puppet181] Upgraded packages linux-libc-dev, and libtasn1-6 on swiftobject151
* 21:57 MirahezeLSBot: [void@puppet181] Upgraded packages linux-libc-dev, and libtasn1-6 on swiftobject171
* 21:57 MirahezeLSBot: [void@puppet181] Upgraded packages linux-libc-dev, and libtasn1-6 on swiftproxy171
* 21:57 MirahezeLSBot: [void@puppet181] Upgraded packages linux-libc-dev, and libtasn1-6 on swiftac171
* 21:57 MirahezeLSBot: [void@puppet181] Upgraded packages libtasn1-6, and linux-libc-dev on test151
* 21:56 MirahezeLSBot: [void@puppet181] Upgraded packages linux-libc-dev, and libtasn1-6 on puppet181
* 21:56 MirahezeLSBot: [void@puppet181] Upgraded packages libtasn1-6, and linux-libc-dev on reports171
* 21:56 MirahezeLSBot: [void@puppet181] Upgraded packages libtasn1-6, and linux-libc-dev on rdb151
* 21:56 MirahezeLSBot: [void@puppet181] Upgraded packages libtasn1-6, and linux-libc-dev on prometheus151
* 21:56 MirahezeLSBot: [void@puppet181] Upgraded packages linux-libc-dev, and libtasn1-6 on ns2
* 21:55 MirahezeLSBot: [void@puppet181] Upgraded packages libtasn1-6, and linux-libc-dev on phorge171
* 21:55 MirahezeLSBot: [void@puppet181] Upgraded packages linux-libc-dev, and libtasn1-6 on os162
* 21:55 MirahezeLSBot: [void@puppet181] Upgraded packages linux-libc-dev, and libtasn1-6 on os161
* 21:55 MirahezeLSBot: [void@puppet181] Upgraded packages libtasn1-6, and linux-libc-dev on mwtask181
* 21:54 MirahezeLSBot: [void@puppet181] Upgraded packages libtasn1-6, and linux-libc-dev on mwtask161
* 21:54 MirahezeLSBot: [void@puppet181] Upgraded packages libtasn1-6, and linux-libc-dev on mw183
* 21:54 MirahezeLSBot: [void@puppet181] Upgraded packages libtasn1-6, and linux-libc-dev on mwtask151
* 21:54 MirahezeLSBot: [void@puppet181] Upgraded packages libtasn1-6, and linux-libc-dev on mw182
* 21:53 MirahezeLSBot: [void@puppet181] Upgraded packages libtasn1-6, and linux-libc-dev on mw184
* 21:53 MirahezeLSBot: [void@puppet181] Upgraded packages libtasn1-6, and linux-libc-dev on mwtask171
* 21:53 MirahezeLSBot: [void@puppet181] Upgraded packages libtasn1-6, and linux-libc-dev on mw174
* 21:53 MirahezeLSBot: [void@puppet181] Upgraded packages libtasn1-6, and linux-libc-dev on mw181
* 21:53 MirahezeLSBot: [void@puppet181] Upgraded packages linux-libc-dev, and libtasn1-6 on ns1
* 21:52 MirahezeLSBot: [void@puppet181] Upgraded packages libtasn1-6, and linux-libc-dev on mw164
* 21:52 MirahezeLSBot: [void@puppet181] Upgraded packages libtasn1-6, and linux-libc-dev on mw173
* 21:52 MirahezeLSBot: [void@puppet181] Upgraded packages libtasn1-6, and linux-libc-dev on mw172
* 21:52 MirahezeLSBot: [void@puppet181] Upgraded packages libtasn1-6, and linux-libc-dev on mw153
* 21:51 MirahezeLSBot: [void@puppet181] Upgraded packages libtasn1-6, and linux-libc-dev on mw171
* 21:51 MirahezeLSBot: [void@puppet181] Upgraded packages libtasn1-6, and linux-libc-dev on mw151
* 21:51 MirahezeLSBot: [void@puppet181] Upgraded packages libtasn1-6, and linux-libc-dev on mw163
* 21:51 MirahezeLSBot: [void@puppet181] Upgraded packages libtasn1-6, and linux-libc-dev on mw162
* 21:50 MirahezeLSBot: [void@puppet181] Upgraded packages linux-libc-dev, and libtasn1-6 on os151
* 21:50 MirahezeLSBot: [void@puppet181] Upgraded packages libtasn1-6, and linux-libc-dev on mw161
* 21:50 MirahezeLSBot: [void@puppet181] Upgraded packages libtasn1-6, and linux-libc-dev on mw154
* 21:50 MirahezeLSBot: [void@puppet181] Upgraded packages libtasn1-6, and linux-libc-dev on mw152
* 21:50 MirahezeLSBot: [void@puppet181] Upgraded packages libtasn1-6, and linux-libc-dev on mon181
* 21:49 MirahezeLSBot: [void@puppet181] Upgraded packages linux-libc-dev, and libtasn1-6 on mem161
* 21:49 MirahezeLSBot: [void@puppet181] Upgraded packages linux-libc-dev, and libtasn1-6 on bast181
* 21:49 MirahezeLSBot: [void@puppet181] Upgraded packages linux-libc-dev, and libtasn1-6 on ldap171
* 21:49 MirahezeLSBot: [void@puppet181] Upgraded packages linux-libc-dev, and libtasn1-6 on bast161
* 21:48 MirahezeLSBot: [void@puppet181] Upgraded packages libtasn1-6, and linux-libc-dev on cloud15
* 21:48 MirahezeLSBot: [void@puppet181] Upgraded packages libtasn1-6, and linux-libc-dev on db181
* 21:48 MirahezeLSBot: [void@puppet181] Upgraded packages libtasn1-6, and linux-libc-dev on matomo151
* 21:48 MirahezeLSBot: [void@puppet181] Upgraded packages libtasn1-6, and linux-libc-dev on cloud16
* 21:48 MirahezeLSBot: [void@puppet181] Upgraded packages libtasn1-6, and linux-libc-dev on cloud18
* 21:47 MirahezeLSBot: [void@puppet181] Upgraded packages libtasn1-6, and linux-libc-dev on cloud17
* 21:47 MirahezeLSBot: [void@puppet181] Upgraded packages libtasn1-6, and linux-libc-dev on db182
* 21:47 MirahezeLSBot: [void@puppet181] Upgraded packages linux-libc-dev, and libtasn1-6 on graylog161
* 21:47 MirahezeLSBot: [void@puppet181] Upgraded packages linux-libc-dev, and libtasn1-6 on graphite151
* 21:47 MirahezeLSBot: [void@puppet181] Upgraded packages libtasn1-6, and linux-libc-dev on eventgate181
* 21:46 MirahezeLSBot: [void@puppet181] Upgraded packages libtasn1-6, and linux-libc-dev on kafka181
* 21:46 MirahezeLSBot: [void@puppet181] Upgraded packages linux-libc-dev, and libtasn1-6 on mem151
* 21:46 MirahezeLSBot: [void@puppet181] Upgraded packages libtasn1-6, and linux-libc-dev on db151
* 21:46 MirahezeLSBot: [void@puppet181] Upgraded packages libtasn1-6, and linux-libc-dev on cp37
* 21:46 MirahezeLSBot: [void@puppet181] Upgraded packages libtasn1-6, and linux-libc-dev on db161
* 21:45 MirahezeLSBot: [void@puppet181] Upgraded packages libtasn1-6, and linux-libc-dev on db171
* 21:45 MirahezeLSBot: [void@puppet181] Upgraded packages libtasn1-6, and linux-libc-dev on cp36
* 21:45 MirahezeLSBot: [void@puppet181] Upgraded packages libtasn1-6, and linux-libc-dev on jobchron171
* 21:45 MirahezeLSBot: [void@puppet181] Upgraded packages libtasn1-6, and linux-libc-dev on bots171
* 21:45 MirahezeLSBot: [void@puppet181] Upgraded packages libtasn1-6, and linux-libc-dev on db172
* 21:44 MirahezeLSBot: [void@puppet181] Upgraded packages libtasn1-6, and linux-libc-dev on changeprop151
* 21:44 MirahezeLSBot: [void@puppet181] Upgraded packages libtasn1-6, and linux-libc-dev on mattermost1
* 19:31 MirahezeLSBot: [reception@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 24s
* 19:30 MirahezeLSBot: [reception@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 19:29 Reception123: MariaDB [phightingwiki]> DROP TABLE user_profile;
* 19:16 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/deleteBatch.php --wiki=toimunwiki /home/reception/deltoimun.txt --r=T13040 (END - exit=256)
* 19:16 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/deleteBatch.php --wiki=toimunwiki /home/reception/deltoimun.txt --r=T13040 (START)
* 19:13 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/deleteBatch.php --wiki=incubatorwiki /home/reception/delincubator.txt --r=T13033 (END - exit=0)
* 19:13 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/deleteBatch.php --wiki=incubatorwiki /home/reception/delincubator.txt --r=T13033 (START)
* 18:54 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/extensions/MirahezeMagic/maintenance/replaceTextEligible.php --wiki=kagagawiki (END - exit=0)
* 18:42 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/extensions/MirahezeMagic/maintenance/replaceTextEligible.php --wiki=dragdownwiki (END - exit=0)
* 18:41 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/replaceTextEligible.php --wiki=dragdownwiki (END - exit=256)
* 05:04 Universal Omega: restart nginx on matamo151
* 02:31 Universal Omega: restart nginx on swiftproxy*

## 2025-02-08 

* 17:59 Universal Omega: restart nginx on swiftproxy*
* 17:11 MirahezeLSBot: [paladox@mwtask181] finished deploy of {'world': True, 'l10n': True, 'versions': '1.43'} to all - SUCCESS in 158s
* 17:08 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'world': True, 'l10n': True, 'versions': '1.43'} to all
* 15:45 MirahezeLSBot: [paladox@test151] finished deploy of {'pull': 'config', 'config': True} to test151 - SUCCESS in 1s
* 15:45 MirahezeLSBot: [paladox@test151] starting deploy of {'pull': 'config', 'config': True} to test151
* 15:34 MirahezeLSBot: [paladox@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 22s
* 15:34 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 14:12 MirahezeLSBot: [paladox@mwtask181] finished deploy of {'world': True, 'l10n': True, 'versions': '1.43'} to all - SUCCESS in 164s
* 14:09 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'world': True, 'l10n': True, 'versions': '1.43'} to all
* 12:53 MirahezeLSBot: [paladox@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 21s
* 12:52 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 12:51 MirahezeLSBot: [paladox@mwtask181] finished deploy of {'world': True, 'l10n': True, 'versions': '1.43'} to all - SUCCESS in 203s
* 12:48 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'world': True, 'l10n': True, 'versions': '1.43'} to all
* 12:43 MirahezeLSBot: [paladox@mwtask181] DEPLOY ABORTED: Non-Zero Exit Code in prep, see output.
* 12:41 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'world': True, 'l10n': True, 'versions': '1.43'} to all
* 12:39 MirahezeLSBot: [paladox@mwtask181] DEPLOY ABORTED: Non-Zero Exit Code in prep, see output.
* 12:38 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'world': True, 'l10n': True, 'versions': '1.43'} to all
* 12:35 MirahezeLSBot: [paladox@mwtask181] DEPLOY ABORTED: Non-Zero Exit Code in prep, see output.
* 12:31 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'world': True, 'l10n': True, 'versions': '1.43'} to all
* 04:59 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/importImages.php --wiki=talesofwiki images --search-recursively (END - exit=0)
* 04:45 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/importImages.php --wiki=talesofwiki images --search-recursively (START)
* 03:51 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/initSiteStats.php --wiki=talesofwiki --update (END - exit=0)
* 03:51 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/rebuildall.php --wiki=talesofwiki (END - exit=0)
* 03:26 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/rebuildall.php --wiki=talesofwiki (START)
* 03:26 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/importDump.php --wiki=talesofwiki detalesof233_pages_full.xml --no-updates (END - exit=0)
* 02:21 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/importDump.php --wiki=talesofwiki detalesof233_pages_full.xml --no-updates (START)

## 2025-02-07 

* 10:34 MirahezeLSBot: [paladox@mwtask181] finished deploy of {'world': True, 'l10n': True, 'versions': '1.43'} to all - SUCCESS in 220s
* 10:30 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'world': True, 'l10n': True, 'versions': '1.43'} to all
* 10:10 MirahezeLSBot: [paladox@mwtask181] finished deploy of {'config': True} to all - SUCCESS in 19s
* 10:10 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'config': True} to all
* 10:02 MirahezeLSBot: [paladox@mwtask181] finished deploy of {'config': True} to all - SUCCESS in 19s
* 10:02 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'config': True} to all
* 10:01 MirahezeLSBot: [paladox@mwtask181] finished deploy of {'world': True, 'l10n': True, 'versions': '1.43'} to all - SUCCESS in 565s
* 09:52 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'world': True, 'l10n': True, 'versions': '1.43'} to all
* 05:06 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/invalidateUserSessions.php --wiki=metawiki --user=TheScrungo (END - exit=0)
* 05:06 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/invalidateUserSessions.php --wiki=summitpediawiki --user=TheScrungo (END - exit=0)
* 05:06 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/invalidateUserSessions.php --wiki=loginwiki --user=TheScrungo (END - exit=0)
* 05:04 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/invalidateUserSessions.php --wiki=loginwiki --user=TheScrungo (END - exit=0)
* 05:04 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/invalidateUserSessions.php --wiki=summitpediawiki --user=TheScrungo (END - exit=0)
* 05:03 MirahezeLSBot: [macfan@mwtask181] finished deploy of {'force_upgrade': True, 'versions': '1.43', 'upgrade_extensions': 'MirahezeMagic'} to all - SUCCESS in 19s
* 05:02 MirahezeLSBot: [macfan@mwtask181] starting deploy of {'force_upgrade': True, 'versions': '1.43', 'upgrade_extensions': 'MirahezeMagic'} to all
* 04:59 MirahezeLSBot: [macfan@mwtask181] finished deploy of {'force_upgrade': True, 'versions': '1.43', 'upgrade_extensions': 'DynamicPageList3'} to all - SUCCESS in 19s
* 04:59 MirahezeLSBot: [macfan@mwtask181] starting deploy of {'force_upgrade': True, 'versions': '1.43', 'upgrade_extensions': 'DynamicPageList3'} to all
* 04:57 MirahezeLSBot: [macfan@mwtask181] finished deploy of {'force_upgrade': True, 'versions': '1.43', 'upgrade_extensions': 'MirahezeMagic'} to all - SUCCESS in 20s
* 04:57 MirahezeLSBot: [macfan@mwtask181] starting deploy of {'force_upgrade': True, 'versions': '1.43', 'upgrade_extensions': 'MirahezeMagic'} to all
* 04:49 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/extensions/MirahezeMagic/maintenance/renameDatabase.php --wiki=summitpediawiki --old=bordrrevivedwiki --new=fraudulentfronterawiki (END - exit=256)
* 04:45 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/extensions/CreateWiki/maintenance/setContainersAccess.php --wiki=summitpediawiki (END - exit=0)
* 04:44 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/extensions/CreateWiki/maintenance/maintenance --wiki=summitpediawiki (END - exit=256)
* 04:26 MacFan4000: DROP VIEW antonballwiki.dpl_clview;
* 04:25 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/extensions/MirahezeMagic/maintenance/renameDatabase.php --wiki=summitpediawiki --old=antonballwiki --new=summitpediawiki (END - exit=0)
* 04:21 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/extensions/MirahezeMagic/maintenance/renameDatabase.php --wiki=summitpediawiki --old=antonballwiki --new=summitpediawiki (END - exit=256)
* 04:20 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/extensions/MirahezeMagic/maintenance/renameDatabase.php --wiki=summitpediawiki --old=antonballwiki --new=summitpediawiki (END - exit=65280)
* 04:19 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/extensions/MirahezeMagic/maintenance/renameDatabase.php --wiki=summitpediawiki --old=antonballwiki --new=summitpediawiki (END - exit=256)
* 04:07 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/extensions/MirahezeMagic/maintenance/renameDatabase.php --wiki=summitpediawiki --old=antonballwiki --new=summitpediawiki (END - exit=256)
* 04:06 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/extensions/MirahezeMagic/maintenance/renameDatabase.php --wiki=--old=antonballwiki --new=summitpediawiki (END - exit=0)

## 2025-02-06 

* 20:54 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/importImages.php --wiki=balkansirlwiki images --search-recursively (END - exit=0)
* 20:52 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/importImages.php --wiki=balkansirlwiki images --search-recursively (START)
* 20:38 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/initSiteStats.php --wiki=balkansirlwiki --update (END - exit=0)
* 20:38 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/rebuildall.php --wiki=balkansirlwiki (END - exit=0)
* 20:37 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/rebuildall.php --wiki=balkansirlwiki (START)
* 20:37 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/importDump.php --wiki=balkansirlwiki balkansirl_pages_full.xml --no-updates (END - exit=0)
* 20:33 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/importDump.php --wiki=balkansirlwiki balkansirl_pages_full.xml --no-updates (START)
* 18:51 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/extensions/MirahezeMagic/maintenance/renameDatabase.php --wiki=loginwiki --old=summitpediawiki --new=antonballwiki (END - exit=256)
* 18:51 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/extensions/MirahezeMagic/maintenance/renameDatabase.php --wiki=loginwiki --old=antonballwiki --new=summitpediawiki (END - exit=256)
* 18:15 MirahezeLSBot: [reception@mwtask171] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/purgeList.php --wiki=battlenationswiki --all-namespaces (END - exit=0)
* 18:14 MirahezeLSBot: [reception@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 21s
* 18:14 MirahezeLSBot: [reception@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 18:11 MirahezeLSBot: [reception@mwtask171] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/purgeList.php --wiki=battlenationswiki --all-namespaces (START)
* 18:10 MirahezeLSBot: [reception@mwtask171] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/purgeList.php --wiki=battlenationswiki --all (END - exit=256)
* 18:10 MirahezeLSBot: [reception@mwtask171] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/purgeList.php --wiki=battlenationswiki --all (START)
* 18:10 MirahezeLSBot: [reception@mwtask171] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/purgeList.php --wiki=battlenationswiki --all-namespaces (END - exit=2)
* 18:10 MirahezeLSBot: [reception@mwtask171] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/purgeList.php --wiki=battlenationswiki --all-namespaces (START)
* 17:25 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/importImages.php --wiki=animalroyalezhwiki images --search-recursively (END - exit=0)
* 17:24 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/importImages.php --wiki=animalroyalezhwiki images --search-recursively (START)
* 00:15 MirahezeLSBot: [void@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 19s
* 00:14 MirahezeLSBot: [void@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 00:13 MirahezeLSBot: [void@mwtask181] finished deploy of {'config': True} to all - SUCCESS in 20s
* 00:13 MirahezeLSBot: [void@mwtask181] starting deploy of {'config': True} to all

## 2025-02-05 

* 21:55 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/importImages.php --wiki=battlenationswiki images --search-recursively (END - exit=0)
* 21:55 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/importImages.php --wiki=battlenationswiki images --search-recursively (START)
* 16:37 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/importImages.php --wiki=battlenationswiki images --search-recursively (END - exit=0)
* 16:07 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/importImages.php --wiki=battlenationswiki images --search-recursively (START)
* 14:18 MacFan4000: (metawiki) DELETE FROM echo_unread_wikis WHERE euw_user=431746;
* 09:32 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/initSiteStats.php --wiki=battlenationswiki --update (END - exit=0)
* 09:32 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/rebuildall.php --wiki=battlenationswiki (END - exit=0)
* 05:22 MacFan4000: (nfswiki) UPDATE echo_notification SET notification_read_timestamp=20240415090051 WHERE notification_user=9;
* 04:11 MirahezeLSBot: [agent@mwtask181] finished deploy of {'config': True, 'force': True} to all - SUCCESS in 20s
* 04:11 MirahezeLSBot: [agent@mwtask181] starting deploy of {'config': True, 'force': True} to all
* 03:15 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/rebuildall.php --wiki=battlenationswiki (START)
* 03:15 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/importDump.php --wiki=battlenationswiki battlenations_pages_full.xml --no-updates (END - exit=0)

## 2025-02-04 

* 23:51 MacFan4000: (metawiki) DELETE FROM echo_unread_wikis WHERE euw_user=531746;
* 20:51 MirahezeLSBot: [agent@mwtask181] sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/databases.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/cleanupTitles.php (END - exit=0)
* 17:19 MirahezeLSBot: [agent@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/extensions/CreateWiki/maintenance/generateMissingCache.php --wiki=metawiki (END - exit=0)
* 17:18 MirahezeLSBot: [agent@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/extensions/CreateWiki/maintenance/generateMissingCaches.php --wiki=metawiki (END - exit=256)
* 17:17 MirahezeLSBot: [agent@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 19s
* 17:16 MirahezeLSBot: [agent@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 17:13 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/importDump.php --wiki=battlenationswiki battlenations_pages_full.xml --no-updates (START)
* 17:10 MirahezeLSBot: [agent@mwtask151] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/extensions/WikiSEO/maintenance/GenerateDescription.php --wiki=gimkitwiki 0,1,2,3 (END - exit=0)
* 17:09 MirahezeLSBot: [agent@mwtask151] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/extensions/WikiSEO/maintenance/GenerateDescription.php --wiki=gimkitwiki (END - exit=256)
* 17:05 MirahezeLSBot: [agent@mwtask181] sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/databases.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/cleanupTitles.php (START)
* 16:16 MirahezeLSBot: [macfan@mwtask181] finished deploy of {'versions': '1.43', 'upgrade_extensions': 'ManageWiki'} to all - SUCCESS in 22s
* 16:15 MirahezeLSBot: [macfan@mwtask181] starting deploy of {'versions': '1.43', 'upgrade_extensions': 'ManageWiki'} to all
* 16:15 MirahezeLSBot: [macfan@test151] finished deploy of {'force_upgrade': True, 'versions': ['1.44', '1.43'], 'upgrade_extensions': 'ManageWiki'} to test151 - SUCCESS in 1s
* 16:15 MirahezeLSBot: [macfan@test151] starting deploy of {'force_upgrade': True, 'versions': ['1.44', '1.43'], 'upgrade_extensions': 'ManageWiki'} to test151
* 16:11 MirahezeLSBot: [macfan@test151] finished deploy of {'force_upgrade': True, 'versions': ['1.44', '1.43'], 'upgrade_extensions': 'ManageWiki'} to test151 - SUCCESS in 1s
* 16:11 MirahezeLSBot: [macfan@test151] starting deploy of {'force_upgrade': True, 'versions': ['1.44', '1.43'], 'upgrade_extensions': 'ManageWiki'} to test151
* 16:10 MirahezeLSBot: [macfan@test151] finished deploy of {'force_upgrade': True, 'versions': ['1.44', '1.43'], 'upgrade_extensions': 'ManageWiki'} to test151 - SUCCESS in 2s
* 16:10 MirahezeLSBot: [macfan@test151] starting deploy of {'force_upgrade': True, 'versions': ['1.44', '1.43'], 'upgrade_extensions': 'ManageWiki'} to test151
* 16:10 MirahezeLSBot: [macfan@test151] finished deploy of {'force_upgrade': True, 'versions': ['1.44', '1.43'], 'upgrade_extensions': 'ManageWiki'} to test151 - SUCCESS in 1s
* 16:10 MirahezeLSBot: [macfan@test151] starting deploy of {'force_upgrade': True, 'versions': ['1.44', '1.43'], 'upgrade_extensions': 'ManageWiki'} to test151
* 16:08 MirahezeLSBot: [macfan@test151] finished deploy of {'versions': ['1.44', '1.43'], 'upgrade_extensions': 'ManageWiki'} to test151 - SUCCESS in 1s
* 16:08 MirahezeLSBot: [macfan@test151] starting deploy of {'versions': ['1.44', '1.43'], 'upgrade_extensions': 'ManageWiki'} to test151
* 16:04 MirahezeLSBot: [macfan@test151] finished deploy of {'versions': ['1.44', '1.43'], 'upgrade_extensions': 'ManageWiki'} to test151 - SUCCESS in 1s
* 16:04 MirahezeLSBot: [macfan@test151] starting deploy of {'versions': ['1.44', '1.43'], 'upgrade_extensions': 'ManageWiki'} to test151
* 16:02 MirahezeLSBot: [macfan@test151] finished deploy of {'versions': ['1.44', '1.43'], 'upgrade_extensions': 'ManageWiki'} to test151 - SUCCESS in 1s
* 16:02 MirahezeLSBot: [macfan@test151] starting deploy of {'versions': ['1.44', '1.43'], 'upgrade_extensions': 'ManageWiki'} to test151
* 15:57 MirahezeLSBot: [macfan@test151] finished deploy of {'versions': ['1.44', '1.43'], 'upgrade_extensions': 'ManageWiki'} to test151 - SUCCESS in 1s
* 15:57 MirahezeLSBot: [macfan@test151] starting deploy of {'versions': ['1.44', '1.43'], 'upgrade_extensions': 'ManageWiki'} to test151
* 15:54 MirahezeLSBot: [macfan@test151] finished deploy of {'versions': ['1.44', '1.43'], 'upgrade_extensions': 'ManageWiki'} to test151 - SUCCESS in 1s
* 15:54 MirahezeLSBot: [macfan@test151] starting deploy of {'versions': ['1.44', '1.43'], 'upgrade_extensions': 'ManageWiki'} to test151
* 15:50 MirahezeLSBot: [macfan@test151] finished deploy of {'versions': '1.44', 'upgrade_extensions': 'ManageWiki'} to test151 - SUCCESS in 1s
* 15:50 MirahezeLSBot: [macfan@test151] starting deploy of {'versions': '1.44', 'upgrade_extensions': 'ManageWiki'} to test151
* 15:45 MirahezeLSBot: [macfan@test151] finished deploy of {'versions': '1.43', 'upgrade_extensions': 'ManageWiki'} to test151 - SUCCESS in 0s
* 15:45 MirahezeLSBot: [macfan@test151] starting deploy of {'versions': '1.43', 'upgrade_extensions': 'ManageWiki'} to test151
* 15:45 MirahezeLSBot: [macfan@test151] finished deploy of {'versions': '1.44', 'upgrade_extensions': 'ManageWiki'} to test151 - SUCCESS in 1s
* 15:45 MirahezeLSBot: [macfan@test151] starting deploy of {'versions': '1.44', 'upgrade_extensions': 'ManageWiki'} to test151
* 15:40 MirahezeLSBot: [macfan@test151] finished deploy of {'force_upgrade': True, 'versions': '1.44', 'upgrade_extensions': 'ManageWiki'} to test151 - SUCCESS in 0s
* 15:40 MirahezeLSBot: [macfan@test151] starting deploy of {'force_upgrade': True, 'versions': '1.44', 'upgrade_extensions': 'ManageWiki'} to test151
* 15:31 MirahezeLSBot: [macfan@test151] finished deploy of {'force_upgrade': True, 'versions': '1.43', 'upgrade_extensions': 'ManageWiki'} to test151 - SUCCESS in 0s
* 15:31 MirahezeLSBot: [macfan@test151] starting deploy of {'force_upgrade': True, 'versions': '1.43', 'upgrade_extensions': 'ManageWiki'} to test151
* 15:31 MirahezeLSBot: [macfan@test151] finished deploy of {'versions': '1.43', 'upgrade_extensions': 'ManageWiki'} to test151 - SUCCESS in 0s
* 15:31 MirahezeLSBot: [macfan@test151] starting deploy of {'versions': '1.43', 'upgrade_extensions': 'ManageWiki'} to test151
* 15:29 MirahezeLSBot: [macfan@test151] DEPLOY ABORTED: Non-Zero Exit Code in prep, see output.
* 15:29 MirahezeLSBot: [macfan@test151] starting deploy of {'versions': '1.43', 'upgrade_extensions': 'ManageWiki'} to test151
* 06:00 MirahezeLSBot: [macfan@mwtask181] finished deploy of {'versions': '1.43', 'upgrade_extensions': 'ImportDump'} to all - SUCCESS in 20s
* 06:00 MirahezeLSBot: [macfan@mwtask181] starting deploy of {'versions': '1.43', 'upgrade_extensions': 'ImportDump'} to all
* 05:57 MirahezeLSBot: [macfan@test151] finished deploy of {'versions': ['1.43', '1.44'], 'upgrade_extensions': 'ImportDump'} to test151 - SUCCESS in 1s
* 05:57 MirahezeLSBot: [macfan@test151] starting deploy of {'versions': ['1.43', '1.44'], 'upgrade_extensions': 'ImportDump'} to test151
* 04:05 MirahezeLSBot: [macfan@mwtask181] finished deploy of {'versions': '1.43', 'upgrade_extensions': 'RequestSSL'} to all - SUCCESS in 20s
* 04:05 MirahezeLSBot: [macfan@mwtask181] starting deploy of {'versions': '1.43', 'upgrade_extensions': 'RequestSSL'} to all
* 04:01 MirahezeLSBot: [macfan@test151] finished deploy of {'versions': '1.43', 'upgrade_extensions': 'RequestSSL'} to test151 - SUCCESS in 1s
* 04:01 MirahezeLSBot: [macfan@test151] starting deploy of {'versions': '1.43', 'upgrade_extensions': 'RequestSSL'} to test151
* 03:58 MirahezeLSBot: [macfan@test151] finished deploy of {'versions': '1.44', 'upgrade_extensions': 'RequestSSL'} to test151 - SUCCESS in 1s
* 03:58 MirahezeLSBot: [macfan@test151] starting deploy of {'versions': '1.44', 'upgrade_extensions': 'RequestSSL'} to test151
* 00:11 MirahezeLSBot: [void@puppet181] restart puppetserver (needed after jre update)

## 2025-02-03 

* 23:08 MirahezeLSBot: [void@puppet181] Upgraded packages redis-server, and redis-tools on test151
* 23:08 MirahezeLSBot: [void@puppet181] Upgraded packages openjdk-17-jdk, openjdk-17-jdk-headless, openjdk-17-jre, and openjdk-17-jre-headless on puppet181
* 23:07 MirahezeLSBot: [void@puppet181] Upgraded packages redis-server, and redis-tools on rdb151
* 23:07 MirahezeLSBot: [void@puppet181] Upgraded packages openjdk-17-jdk, openjdk-17-jdk-headless, openjdk-17-jre, and openjdk-17-jre-headless on os161
* 23:07 MirahezeLSBot: [void@puppet181] Upgraded packages openjdk-17-jdk, openjdk-17-jdk-headless, openjdk-17-jre, and openjdk-17-jre-headless on os162
* 23:06 MirahezeLSBot: [void@puppet181] Upgraded packages openjdk-17-jdk, openjdk-17-jdk-headless, openjdk-17-jre, and openjdk-17-jre-headless on os151
* 23:03 MirahezeLSBot: [void@puppet181] Upgraded packages openjdk-17-jdk, openjdk-17-jdk-headless, openjdk-17-jre, and openjdk-17-jre-headless on graylog161
* 23:02 MirahezeLSBot: [void@puppet181] Upgraded packages openjdk-17-jre, and openjdk-17-jre-headless on kafka181
* 23:01 MirahezeLSBot: [void@puppet181] Upgraded packages redis-server, and redis-tools on jobchron171
* 23:01 MirahezeLSBot: [void@puppet181] Upgraded packages redis-server, and redis-tools on changeprop151
* 14:54 MirahezeLSBot: [paladox@mwtask181] finished deploy of {'l10n': True, 'versions': '1.43', 'upgrade_extensions': ['CreateWiki', 'ManageWiki']} to all - SUCCESS in 467s
* 14:53 MirahezeLSBot: [paladox@test151] finished deploy of {'l10n': True, 'versions': ['1.43', '1.44'], 'upgrade_extensions': ['CreateWiki', 'ManageWiki']} to test151 - SUCCESS in 368s
* 14:46 MirahezeLSBot: [paladox@test151] starting deploy of {'l10n': True, 'versions': ['1.43', '1.44'], 'upgrade_extensions': ['CreateWiki', 'ManageWiki']} to test151
* 14:46 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'l10n': True, 'versions': '1.43', 'upgrade_extensions': ['CreateWiki', 'ManageWiki']} to all
* 12:08 MirahezeLSBot: [paladox@mwtask181] finished deploy of {'l10n': True, 'force_upgrade': True, 'versions': '1.43', 'upgrade_extensions': 'RatePage'} to all - SUCCESS in 115s
* 12:06 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'l10n': True, 'force_upgrade': True, 'versions': '1.43', 'upgrade_extensions': 'RatePage'} to all
* 11:59 MirahezeLSBot: [paladox@mwtask181] finished deploy of {'l10n': True, 'force_upgrade': True, 'versions': '1.43', 'upgrade_extensions': 'LinkCards'} to all - SUCCESS in 416s
* 11:54 MirahezeLSBot: [paladox@test151] finished deploy of {'upgrade_world': True, 'upgrade_vendor': True, 'l10n': True, 'versions': '1.44', 'upgrade_extensions': 'all', 'upgrade_skins': 'all'} to test151 - SUCCESS in 1216s
* 11:52 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'l10n': True, 'force_upgrade': True, 'versions': '1.43', 'upgrade_extensions': 'LinkCards'} to all
* 11:52 MirahezeLSBot: [paladox@mwtask181] finished deploy of {'l10n': True, 'versions': '1.43', 'upgrade_extensions': 'LinkCards'} to all - SUCCESS in 68s
* 11:50 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'l10n': True, 'versions': '1.43', 'upgrade_extensions': 'LinkCards'} to all
* 11:37 MirahezeLSBot: [paladox@mwtask181] finished deploy of {'l10n': True, 'versions': '1.43', 'upgrade_extensions': 'LockAuthor'} to all - SUCCESS in 88s
* 11:35 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'l10n': True, 'versions': '1.43', 'upgrade_extensions': 'LockAuthor'} to all
* 11:34 MirahezeLSBot: [paladox@test151] starting deploy of {'upgrade_world': True, 'upgrade_vendor': True, 'l10n': True, 'versions': '1.44', 'upgrade_extensions': 'all', 'upgrade_skins': 'all'} to test151
* 11:24 MirahezeLSBot: [paladox@test151] finished deploy of {'l10n': True, 'versions': ['1.43', '1.44'], 'upgrade_extensions': 'CheckUser'} to test151 - SUCCESS in 400s
* 11:19 MirahezeLSBot: [paladox@mwtask181] finished deploy of {'l10n': True, 'versions': '1.43', 'upgrade_extensions': 'CheckUser'} to all - SUCCESS in 115s
* 11:17 MirahezeLSBot: [paladox@test151] starting deploy of {'l10n': True, 'versions': ['1.43', '1.44'], 'upgrade_extensions': 'CheckUser'} to test151
* 11:17 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'l10n': True, 'versions': '1.43', 'upgrade_extensions': 'CheckUser'} to all
* 04:44 MirahezeLSBot: [void@mwtask181] sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/databases.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/extensions/MirahezeMagic/maintenance/resetWikiCaches.php (END - exit=0)
* 01:41 MirahezeLSBot: [void@mwtask181] sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/databases.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/extensions/MirahezeMagic/maintenance/resetWikiCaches.php (START)
* 01:33 MirahezeLSBot: [void@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/extensions/MirahezeMagic/maintenance/resetWikiCaches.php --wiki=testwiki (END - exit=0)

## 2025-02-02 

* 17:49 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/initSiteStats.php --wiki=peppafanonwiki --update (END - exit=0)
* 17:49 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/rebuildall.php --wiki=peppafanonwiki (END - exit=0)
* 17:49 MirahezeLSBot: [reception@mwtask171] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/refreshLinks.php --wiki=tfukwiki (END - exit=0)
* 17:47 MirahezeLSBot: [reception@mwtask171] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/refreshLinks.php --wiki=tfukwiki (START)
* 13:24 MirahezeLSBot: [paladox@mwtask181] finished deploy of {'l10n': True, 'versions': '1.43', 'upgrade_extensions': 'RatePage'} to all - SUCCESS in 85s
* 13:22 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'l10n': True, 'versions': '1.43', 'upgrade_extensions': 'RatePage'} to all
* 13:20 MirahezeLSBot: [paladox@mwtask181] DEPLOY ABORTED: Non-Zero Exit Code in prep, see output.
* 13:18 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'l10n': True, 'versions': '1.43', 'upgrade_extensions': 'RatePage'} to all
* 13:14 MirahezeLSBot: [paladox@mwtask181] DEPLOY ABORTED: Non-Zero Exit Code in prep, see output.
* 13:10 MirahezeLSBot: [paladox@test151] finished deploy of {'l10n': True, 'versions': ['1.43', '1.44'], 'upgrade_extensions': 'RatePage'} to test151 - SUCCESS in 114s
* 13:08 MirahezeLSBot: [paladox@test151] starting deploy of {'l10n': True, 'versions': ['1.43', '1.44'], 'upgrade_extensions': 'RatePage'} to test151
* 13:08 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'l10n': True, 'versions': '1.43', 'upgrade_extensions': 'RatePage'} to all
* 12:52 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/rebuildall.php --wiki=peppafanonwiki (START)
* 12:52 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/importDump.php --wiki=peppafanonwiki peppapedia_pages_full.xml --no-updates (END - exit=0)
* 02:09 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/importDump.php --wiki=peppafanonwiki peppapedia_pages_full.xml --no-updates (START)
* 01:30 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/initSiteStats.php --wiki=dendronwiki --update (END - exit=0)
* 01:30 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/rebuildall.php --wiki=dendronwiki (END - exit=0)
* 01:15 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/rebuildall.php --wiki=dendronwiki (START)
* 01:15 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/importDump.php --wiki=dendronwiki esalderapedia_pages_full.xml --no-updates (END - exit=0)
* 00:14 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/importDump.php --wiki=dendronwiki esalderapedia_pages_full.xml --no-updates (START)

## 2025-02-01 

* 22:21 @paladox: restart swift-proxy, swift-object, swift-account and swift-container on all swift serversa
* 22:21 @paladox: restart pdns-recursor on all servers
* 22:21 @paladox: truncate access.log on cp37
* 15:20 MirahezeLSBot: [paladox@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 21s
* 15:20 MirahezeLSBot: [paladox@test151] finished deploy of {'pull': 'config', 'config': True} to test151 - SUCCESS in 1s
* 15:20 MirahezeLSBot: [paladox@test151] starting deploy of {'pull': 'config', 'config': True} to test151
* 15:20 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 00:00 MirahezeLSBot: [www-data@mwtask181] Began automatic backing up
* 00:00 MirahezeLSBot: [www-data@test151] Began automatic backing up

## 2025-01-31 

* 23:27 MirahezeLSBot: [agent@mwtask181] finished deploy of {'versions': '1.43', 'upgrade_extensions': 'CreateWiki'} to all - SUCCESS in 20s
* 23:27 MirahezeLSBot: [agent@mwtask181] starting deploy of {'versions': '1.43', 'upgrade_extensions': 'CreateWiki'} to all
* 21:11 MirahezeLSBot: [agent@mwtask181] finished deploy of {'l10n': True, 'versions': '1.43'} to all - SUCCESS in 431s
* 21:04 MirahezeLSBot: [agent@mwtask181] starting deploy of {'l10n': True, 'versions': '1.43'} to all
* 21:04 MirahezeLSBot: [agent@mwtask181] finished deploy of {'config': True} to all - SUCCESS in 18s
* 21:03 MirahezeLSBot: [agent@mwtask181] starting deploy of {'config': True} to all
* 21:02 MirahezeLSBot: [agent@mwtask181] finished deploy of {'versions': '1.43', 'upgrade_extensions': 'CreateWiki'} to all - SUCCESS in 24s
* 21:02 MirahezeLSBot: [agent@mwtask181] starting deploy of {'versions': '1.43', 'upgrade_extensions': 'CreateWiki'} to all
* 13:26 @paladox: truncate some tables on db182 for matomo
* 10:04 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/extensions/MirahezeMagic/maintenance/renameDatabase.php --wiki=loginwiki --old=nightwindwiki --new=whispersofthevalkyrieswiki (END - exit=0)
* 10:01 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/extensions/MirahezeMagic/maintenance/renameDatabase.php --wiki=loginwiki --old=wehrapediawiki --new=wehrmachtwiki (END - exit=0)
* 09:54 MirahezeLSBot: [paladox@mwtask181] [root@mwtask181:/srv/mediawiki/1.43/extensions/CreateWiki/maintenance]# sudo -u www-data php setContainersAccess.php --wiki fantasymediahubwiki
* 01:52 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/extensions/DynamicPageList3/maintenance/createTemplate.php --wiki=amenorinfowiki (END - exit=0)
* 01:52 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/extensions/DynamicPageList3/maintenance/createView.php --wiki=amenorinfowiki (END - exit=0)

## 2025-01-30 

* 14:38 MirahezeLSBot: [agent@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/migrateBlocks.php --wiki=whitesidewiki (END - exit=0)
* 14:38 MirahezeLSBot: [agent@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/migrateBlocks.php --wiki=whitesideswiki (END - exit=65280)
* 03:32 MirahezeLSBot: [agent@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/refreshLinks.php --wiki=holidayswiki (END - exit=0)
* 02:48 MirahezeLSBot: [void@cloud17.wikitide.net] clear ipmi sel
* 02:09 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/initSiteStats.php --wiki=mythcommunitywiki --update (END - exit=0)
* 02:09 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/rebuildall.php --wiki=mythcommunitywiki (END - exit=0)
* 01:22 MirahezeLSBot: [void@puppet181] apply bind9 upgrades to puppet181 and matomo151
* 01:15 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/rebuildall.php --wiki=mythcommunitywiki (START)
* 01:15 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/importDump.php --wiki=mythcommunitywiki robloxianmythhunters949_pages_full.xml --no-updates (END - exit=0)
* 00:35 MirahezeLSBot: [void@puppet181] Upgraded packages bind9-host, bind9-dnsutils, bind9-libs, and libopenjp2-7 on swiftproxy171
* 00:34 MirahezeLSBot: [void@puppet181] Upgraded packages bind9-host, bind9-dnsutils, bind9-libs, and libopenjp2-7 on swiftproxy161
* 00:34 MirahezeLSBot: [void@puppet181] Upgraded packages bind9-host, bind9-dnsutils, bind9-libs, and libopenjp2-7 on swiftobject181
* 00:34 MirahezeLSBot: [void@puppet181] Upgraded packages bind9-host, bind9-dnsutils, bind9-libs, and libopenjp2-7 on swiftobject171
* 00:34 MirahezeLSBot: [void@puppet181] Upgraded packages bind9-host, bind9-dnsutils, bind9-libs, and libopenjp2-7 on swiftobject161
* 00:33 MirahezeLSBot: [void@puppet181] Upgraded packages bind9-host, bind9-dnsutils, bind9-libs, and libopenjp2-7 on swiftobject151
* 00:33 MirahezeLSBot: [void@puppet181] Upgraded packages bind9-host, bind9-dnsutils, bind9-libs, and libopenjp2-7 on swiftac171
* 00:33 MirahezeLSBot: [void@puppet181] Upgraded packages bind9-host, bind9-dnsutils, bind9-libs, and libopenjp2-7 on test151
* 00:33 MirahezeLSBot: [void@puppet181] Upgraded packages bind9-host, bind9-dnsutils, bind9-libs, and dnsutils on ns2
* 00:32 MirahezeLSBot: [void@puppet181] Upgraded packages bind9-host, bind9-dnsutils, and bind9-libs on reports171
* 00:32 MirahezeLSBot: [void@puppet181] Upgraded packages bind9-host, bind9-dnsutils, and bind9-libs on puppet181
* 00:32 MirahezeLSBot: [void@puppet181] Upgraded packages bind9-host, bind9-dnsutils, and bind9-libs on rdb151
* 00:32 MirahezeLSBot: [void@puppet181] Upgraded packages bind9-host, bind9-dnsutils, and bind9-libs on prometheus151
* 00:32 MirahezeLSBot: [void@puppet181] Upgraded packages bind9-host, bind9-dnsutils, and bind9-libs on phorge171
* 00:31 MirahezeLSBot: [void@puppet181] Upgraded packages bind9-host, bind9-dnsutils, and bind9-libs on ns1
* 00:31 MirahezeLSBot: [void@puppet181] Upgraded packages bind9-host, bind9-dnsutils, and bind9-libs on os162
* 00:31 MirahezeLSBot: [void@puppet181] Upgraded packages bind9-host, bind9-dnsutils, and bind9-libs on os161
* 00:31 MirahezeLSBot: [void@puppet181] Upgraded packages bind9-host, bind9-dnsutils, and bind9-libs on mw154
* 00:30 MirahezeLSBot: [void@puppet181] Upgraded packages bind9-host, bind9-dnsutils, and bind9-libs on os151
* 00:30 MirahezeLSBot: [void@puppet181] Upgraded packages bind9-host, bind9-dnsutils, and bind9-libs on mw183
* 00:30 MirahezeLSBot: [void@puppet181] Upgraded packages bind9-host, bind9-dnsutils, and bind9-libs on mw184
* 00:30 MirahezeLSBot: [void@puppet181] Upgraded packages bind9-host, bind9-dnsutils, and bind9-libs on mwtask181
* 00:29 MirahezeLSBot: [void@puppet181] Upgraded packages bind9-host, bind9-dnsutils, and bind9-libs on mwtask171
* 00:29 MirahezeLSBot: [void@puppet181] Upgraded packages bind9-host, bind9-dnsutils, and bind9-libs on mw181
* 00:29 MirahezeLSBot: [void@puppet181] Upgraded packages bind9-host, bind9-dnsutils, and bind9-libs on mw172
* 00:29 MirahezeLSBot: [void@puppet181] Upgraded packages bind9-host, bind9-dnsutils, and bind9-libs on mwtask161
* 00:28 MirahezeLSBot: [void@puppet181] Upgraded packages bind9-host, bind9-dnsutils, and bind9-libs on mw163
* 00:28 MirahezeLSBot: [void@puppet181] Upgraded packages bind9-host, bind9-dnsutils, and bind9-libs on mw164
* 00:28 MirahezeLSBot: [void@puppet181] Upgraded packages bind9-host, bind9-dnsutils, and bind9-libs on mwtask151
* 00:28 MirahezeLSBot: [void@puppet181] Upgraded packages bind9-host, bind9-dnsutils, and bind9-libs on mw173
* 00:28 MirahezeLSBot: [void@puppet181] Upgraded packages bind9-host, bind9-dnsutils, and bind9-libs on mw182
* 00:27 MirahezeLSBot: [void@puppet181] Upgraded packages bind9-host, bind9-dnsutils, and bind9-libs on mw174
* 00:27 MirahezeLSBot: [void@puppet181] Upgraded packages bind9-host, bind9-dnsutils, and bind9-libs on mw162
* 00:27 MirahezeLSBot: [void@puppet181] Upgraded packages bind9-host, bind9-dnsutils, and bind9-libs on mw161
* 00:27 MirahezeLSBot: [void@puppet181] Upgraded packages bind9-host, bind9-dnsutils, and bind9-libs on mw152
* 00:26 MirahezeLSBot: [void@puppet181] Upgraded packages bind9-host, bind9-dnsutils, and bind9-libs on mw171
* 00:26 MirahezeLSBot: [void@puppet181] Upgraded packages bind9-host, bind9-dnsutils, and bind9-libs on mw153
* 00:26 MirahezeLSBot: [void@puppet181] Upgraded packages bind9-host, bind9-dnsutils, and bind9-libs on mw151
* 00:26 MirahezeLSBot: [void@puppet181] Upgraded packages bind9-host, bind9-dnsutils, and bind9-libs on mon181
* 00:26 MirahezeLSBot: [void@puppet181] Upgraded packages bind9-host, bind9-dnsutils, and bind9-libs on mem161
* 00:25 MirahezeLSBot: [void@puppet181] Upgraded packages bind9-host, bind9-dnsutils, and bind9-libs on cloud16
* 00:25 MirahezeLSBot: [void@puppet181] Upgraded packages bind9-host, bind9-dnsutils, and bind9-libs on matomo151
* 00:25 MirahezeLSBot: [void@puppet181] Upgraded packages bind9-host, bind9-dnsutils, bind9-libs, and dnsutils on mattermost1
* 00:25 MirahezeLSBot: [void@puppet181] Upgraded packages bind9-host, bind9-dnsutils, and bind9-libs on db181
* 00:24 MirahezeLSBot: [void@puppet181] Upgraded packages bind9-host, bind9-dnsutils, and bind9-libs on cloud15
* 00:24 MirahezeLSBot: [void@puppet181] Upgraded packages bind9-host, bind9-dnsutils, and bind9-libs on cloud17
* 00:24 MirahezeLSBot: [void@puppet181] Upgraded packages bind9-host, bind9-dnsutils, and bind9-libs on ldap171
* 00:24 MirahezeLSBot: [void@puppet181] Upgraded packages bind9-host, bind9-dnsutils, and bind9-libs on bast161
* 00:24 MirahezeLSBot: [void@puppet181] Upgraded packages bind9-host, bind9-dnsutils, and bind9-libs on cloud18
* 00:23 MirahezeLSBot: [void@puppet181] Upgraded packages bind9-host, bind9-dnsutils, and bind9-libs on bast181
* 00:23 MirahezeLSBot: [void@puppet181] Upgraded packages bind9-host, bind9-dnsutils, and bind9-libs on db182
* 00:23 MirahezeLSBot: [void@puppet181] Upgraded packages bind9-host, bind9-dnsutils, and bind9-libs on kafka181
* 00:23 MirahezeLSBot: [void@puppet181] Upgraded packages bind9-host, bind9-dnsutils, and bind9-libs on graylog161
* 00:23 MirahezeLSBot: [void@puppet181] Upgraded packages bind9-host, bind9-dnsutils, and bind9-libs on cp36
* 00:22 MirahezeLSBot: [void@puppet181] Upgraded packages bind9-host, bind9-dnsutils, bind9-libs, and dnsutils on graphite151
* 00:22 MirahezeLSBot: [void@puppet181] Upgraded packages bind9-host, bind9-dnsutils, and bind9-libs on cp37
* 00:22 MirahezeLSBot: [void@puppet181] Upgraded packages bind9-host, bind9-dnsutils, and bind9-libs on db161
* 00:22 MirahezeLSBot: [void@puppet181] Upgraded packages bind9-host, bind9-dnsutils, and bind9-libs on db151
* 00:22 MirahezeLSBot: [void@puppet181] Upgraded packages bind9-host, bind9-dnsutils, and bind9-libs on mem151
* 00:21 MirahezeLSBot: [void@puppet181] Upgraded packages bind9-host, bind9-dnsutils, and bind9-libs on db172
* 00:21 MirahezeLSBot: [void@puppet181] Upgraded packages bind9-host, bind9-dnsutils, and bind9-libs on db171
* 00:21 MirahezeLSBot: [void@puppet181] Upgraded packages bind9-host, bind9-dnsutils, and bind9-libs on jobchron171
* 00:21 MirahezeLSBot: [void@puppet181] Upgraded packages bind9-host, bind9-dnsutils, bind9-libs, and dnsutils on eventgate181
* 00:21 MirahezeLSBot: [void@puppet181] Upgraded packages bind9-host, bind9-dnsutils, and bind9-libs on bots171
* 00:20 MirahezeLSBot: [void@puppet181] Upgraded packages bind9-host, bind9-dnsutils, bind9-libs, and dnsutils on changeprop151

## 2025-01-29 

* 22:14 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/importDump.php --wiki=mythcommunitywiki robloxianmythhunters949_pages_full.xml --no-updates (START)
* 20:37 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/importImages.php --wiki=fantasymediahubwiki images --search-recursively (END - exit=0)
* 20:37 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/importImages.php --wiki=fantasymediahubwiki images --search-recursively (START)
* 20:31 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/initSiteStats.php --wiki=fantasymediahubwiki --update (END - exit=0)
* 20:31 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/rebuildall.php --wiki=fantasymediahubwiki (END - exit=0)
* 20:31 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/rebuildall.php --wiki=fantasymediahubwiki (START)
* 20:31 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/importDump.php --wiki=fantasymediahubwiki dump.xml --no-updates (END - exit=0)
* 20:29 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/importDump.php --wiki=fantasymediahubwiki dump.xml --no-updates (START)
* 20:28 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/initSiteStats.php --wiki=fantasymediahubwiki --update (END - exit=0)
* 20:28 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/rebuildall.php --wiki=fantasymediahubwiki (END - exit=0)
* 20:28 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/rebuildall.php --wiki=fantasymediahubwiki (START)
* 20:28 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/importDump.php --wiki=fantasymediahubwiki fantasymediahub.fandom.com-20250127-history.xml --no-updates (END - exit=256)
* 20:28 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/importDump.php --wiki=fantasymediahubwiki fantasymediahub.fandom.com-20250127-history.xml --no-updates (START)
* 20:09 MirahezeLSBot: [agent@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/refreshLinks.php --wiki=holidayswiki (START)
* 19:45 MirahezeLSBot: [agent@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/refreshLinks.php --wiki=ilvandorwiki (END - exit=0)
* 19:41 MirahezeLSBot: [agent@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/refreshLinks.php --wiki=ilvandorwiki (START)
* 18:55 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/initSiteStats.php --wiki=deepwokenwiki --update (END - exit=0)
* 18:55 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/rebuildall.php --wiki=deepwokenwiki (END - exit=0)
* 18:46 MirahezeLSBot: [paladox@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 20s
* 18:46 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 18:23 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/rebuildall.php --wiki=deepwokenwiki (START)
* 18:23 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/importDump.php --wiki=deepwokenwiki projectdeepwoken_pages_full.xml --no-updates (END - exit=0)
* 17:36 MirahezeLSBot: [paladox@test151] finished deploy of {'pull': 'config', 'config': True} to test151 - SUCCESS in 0s
* 17:35 MirahezeLSBot: [paladox@test151] starting deploy of {'pull': 'config', 'config': True} to test151
* 17:34 MirahezeLSBot: [paladox@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 23s
* 17:34 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 17:21 MirahezeLSBot: [paladox@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 20s
* 17:21 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 17:19 MirahezeLSBot: [paladox@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 21s
* 17:19 MirahezeLSBot: [paladox@test151] finished deploy of {'pull': 'config', 'config': True} to test151 - SUCCESS in 0s
* 17:19 MirahezeLSBot: [paladox@test151] starting deploy of {'pull': 'config', 'config': True} to test151
* 17:18 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 16:41 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/importDump.php --wiki=deepwokenwiki projectdeepwoken_pages_full.xml --no-updates (START)

## 2025-01-28 

* 21:32 MirahezeLSBot: [paladox@mwtask181] finished deploy of {'l10n': True, 'versions': '1.43', 'upgrade_extensions': 'CommonsMetadata'} to all - SUCCESS in 144s
* 21:32 MirahezeLSBot: [paladox@test151] finished deploy of {'l10n': True, 'versions': ['1.43', '1.44'], 'upgrade_extensions': 'CommonsMetadata'} to test151 - SUCCESS in 108s
* 21:30 MirahezeLSBot: [paladox@test151] starting deploy of {'l10n': True, 'versions': ['1.43', '1.44'], 'upgrade_extensions': 'CommonsMetadata'} to test151
* 21:30 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'l10n': True, 'versions': '1.43', 'upgrade_extensions': 'CommonsMetadata'} to all
* 21:19 MirahezeLSBot: [paladox@mwtask181] finished deploy of {'l10n': True, 'versions': '1.43', 'upgrade_skins': 'Monaco'} to all - SUCCESS in 149s
* 21:18 MirahezeLSBot: [paladox@test151] finished deploy of {'l10n': True, 'versions': ['1.43', '1.44'], 'upgrade_skins': 'Monaco'} to test151 - SUCCESS in 118s
* 21:17 @paladox: installed security update on all servers
* 21:16 MirahezeLSBot: [paladox@test151] starting deploy of {'l10n': True, 'versions': ['1.43', '1.44'], 'upgrade_skins': 'Monaco'} to test151
* 21:16 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'l10n': True, 'versions': '1.43', 'upgrade_skins': 'Monaco'} to all
* 18:52 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/initSiteStats.php --wiki=sunlessskieswiki --update (END - exit=0)
* 18:52 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/rebuildall.php --wiki=sunlessskieswiki (END - exit=0)
* 18:31 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/rebuildall.php --wiki=sunlessskieswiki (START)
* 18:31 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/importDump.php --wiki=sunlessskieswiki sunlessskies.fandom.com-20250119-history.xml --no-updates (END - exit=0)
* 18:25 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/importDump.php --wiki=sunlessskieswiki sunlessskies.fandom.com-20250119-history.xml --no-updates (START)
* 18:24 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/initSiteStats.php --wiki=sunlessskieswikiwiki --update (END - exit=2)
* 18:24 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/rebuildall.php --wiki=sunlessskieswikiwiki (END - exit=65280)
* 18:24 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/rebuildall.php --wiki=sunlessskieswikiwiki (START)
* 18:24 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/importDump.php --wiki=sunlessskieswikiwiki sunlessskies.fandom.com-20250119-history.xml --no-updates (END - exit=65280)
* 18:24 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/importDump.php --wiki=sunlessskieswikiwiki sunlessskies.fandom.com-20250119-history.xml --no-updates (START)
* 17:53 RhinosF1: disable TLS1.2 for core domains via cf
* 17:28 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/importImages.php --wiki=sunlessseawiki images --search-recursively (END - exit=0)
* 17:22 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/importImages.php --wiki=sunlessseawiki images --search-recursively (START)
* 14:52 MirahezeLSBot: [agent@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/extensions/MirahezeMagic/maintenance/resetWikiCaches.php --wiki=giannawiki (END - exit=0)
* 14:52 MirahezeLSBot: [agent@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/extensions/MirahezeMagic/maintenance/resetWikiCaches.php --wiki=giannawiki (END - exit=0)
* 14:50 MirahezeLSBot: [agent@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/extensions/MirahezeMagic/maintenance/resetWikiCaches.php --wiki=trollpastawiki (END - exit=0)
* 14:50 MirahezeLSBot: [agent@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/extensions/MirahezeMagic/maintenance/resetWikiCaches.php --wiki=trollpastawiki (END - exit=0)
* 06:09 Universal Omega: reboot all swift, opensearch, and graylog servers
* 06:05 MirahezeLSBot: [macfan@test151] finished deploy of {'pull': 'config', 'config': True} to test151 - SUCCESS in 1s
* 06:05 MirahezeLSBot: [macfan@test151] starting deploy of {'pull': 'config', 'config': True} to test151
* 06:05 MirahezeLSBot: [macfan@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 19s
* 06:05 MirahezeLSBot: [macfan@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 05:38 MirahezeLSBot: [macfan@test151] finished deploy of {'pull': 'config', 'config': True} to test151 - SUCCESS in 1s
* 05:38 MirahezeLSBot: [macfan@test151] starting deploy of {'pull': 'config', 'config': True} to test151
* 04:30 MirahezeLSBot: [macfan@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 19s
* 04:30 MirahezeLSBot: [macfan@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 04:10 MirahezeLSBot: [macfan@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 19s
* 04:10 MirahezeLSBot: [macfan@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 04:04 MirahezeLSBot: [macfan@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 19s
* 04:03 MirahezeLSBot: [macfan@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 02:32 MirahezeLSBot: [agent@mwtask181] sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/databases.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/extensions/MirahezeMagic/maintenance/MigrateSearchIndexSql.php (END - exit=0)
* 01:01 MirahezeLSBot: [agent@mwtask151] sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/databases.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/updateSpecialPages.php (END - exit=0)

## 2025-01-27 

* 23:23 MirahezeLSBot: [macfan@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 20s
* 23:22 MirahezeLSBot: [macfan@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 23:18 MirahezeLSBot: [agent@mwtask171] sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/databases.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/extensions/CheckUser/maintenance/populateCentralCheckUserIndexTables.php (END - exit=0)
* 22:59 MirahezeLSBot: [agent@mwtask151] sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/databases.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/sql.php /srv/mediawiki/1.43/extensions/AbuseFilter/db_patches/mysql/patch-drop-afh_user.sql (END - exit=0)
* 22:59 MirahezeLSBot: [agent@mwtask151] sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/databases.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/sql.php /srv/mediawiki/1.43/extensions/AbuseFilter/db_patches/mysql/patch-drop-afh_user.sql (END - exit=256)
* 22:45 MirahezeLSBot: [agent@mwtask151] sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/databases.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/sql.php /srv/mediawiki/1.43/extensions/AbuseFilter/db_patches/mysql/patch-drop-af_user.sql (END - exit=0)
* 22:45 MirahezeLSBot: [agent@mwtask151] sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/databases.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/sql.php /srv/mediawiki/1.43/extensions/AbuseFilter/db_patches/mysql/patch-drop-af_user.sql (END - exit=256)
* 22:32 MirahezeLSBot: [agent@mwtask151] sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/databases.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/sql.php /srv/mediawiki-staging/1.43/extensions/CheckUser/schema/mysql/cuci_wiki_map.sql (END - exit=256)
* 21:12 MirahezeLSBot: [agent@mwtask171] sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/databases.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/extensions/CheckUser/maintenance/deleteReadOldRowsInCuChanges.php (END - exit=0)
* 21:12 MirahezeLSBot: [agent@mwtask171] sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/databases.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/fixAutoblockLogTitles.php (END - exit=0)
* 20:15 MirahezeLSBot: [agent@mwtask181] sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/databases.php /srv/mediawiki/1.42/maintenance/run.php /srv/mediawiki/1.42/maintenance/sql.php /srv/mediawiki-staging/1.43/maintenance/archives/patch-searchindex-pk-titlelength.sql (END - exit=65280)
* 20:05 MirahezeLSBot: [agent@mwtask181] sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/databases.php /srv/mediawiki/1.42/maintenance/run.php /srv/mediawiki/1.42/maintenance/sql.php /srv/mediawiki-staging/1.43/maintenance/archives/patch-revision-cleanup.sql (END - exit=65280)
* 20:04 MirahezeLSBot: [agent@mwtask181] sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/databases.php /srv/mediawiki/1.42/maintenance/run.php /srv/mediawiki/1.42/maintenance/sql.php /srv/mediawiki-staging/1.43/maintenance/archives/patch-change_tag-ct_rc_id.sql (END - exit=65280)
* 20:04 MirahezeLSBot: [agent@mwtask181] sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/databases.php /srv/mediawiki/1.42/maintenance/run.php /srv/mediawiki/1.42/maintenance/sql.php /srv/mediawiki-staging/1.43/maintenance/archives/patch-recentchanges-rc_id-bigint.sql (END - exit=65280)
* 19:54 MirahezeLSBot: [agent@mwtask151] sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/deleted.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/extensions/CheckUser/maintenance/populateCentralCheckUserIndexTables.php (END - exit=0)
* 19:53 MirahezeLSBot: [agent@mwtask151] sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/deleted.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/extensions/CheckUser/maintenance/deleteReadOldRowsInCuChanges.php (END - exit=0)
* 19:53 MirahezeLSBot: [agent@mwtask151] sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/deleted.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/sql.php /srv/mediawiki-staging/1.43/extensions/CheckUser/schema/mysql/cuci_user.sql (END - exit=256)
* 19:53 MirahezeLSBot: [agent@mwtask151] sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/deleted.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/sql.php /srv/mediawiki-staging/1.43/extensions/CheckUser/schema/mysql/patch-cu_changes-drop-cuc_only_for_read_old.sql (END - exit=256)
* 19:53 MirahezeLSBot: [agent@mwtask151] sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/deleted.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/fixAutoblockLogTitles.php (END - exit=0)
* 19:53 MirahezeLSBot: [agent@mwtask151] sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/deleted.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/sql.php /srv/mediawiki-staging/1.43/maintenance/archives/patch-pagelinks-drop-pl_title.sql (END - exit=256)
* 19:53 MirahezeLSBot: [agent@mwtask151] sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/deleted.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/sql.php /srv/mediawiki-staging/1.43/maintenance/archives/patch-searchindex-pk-titlelength.sql (END - exit=256)
* 19:53 MirahezeLSBot: [agent@mwtask151] sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/deleted.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/sql.php /srv/mediawiki-staging/1.43/extensions/CheckUser/schema/mysql/cuci_temp_edit.sql (END - exit=256)
* 19:53 MirahezeLSBot: [agent@mwtask151] sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/deleted.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/sql.php /srv/mediawiki-staging/1.43/extensions/CheckUser/schema/mysql/patch-cu_changes-drop-cuc_actiontext.sql (END - exit=256)
* 19:53 MirahezeLSBot: [agent@mwtask151] sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/deleted.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/sql.php /srv/mediawiki-staging/1.43/maintenance/archives/patch-recentchanges-rc_id-bigint.sql (END - exit=256)
* 19:53 MirahezeLSBot: [agent@mwtask151] sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/deleted.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/sql.php /srv/mediawiki-staging/1.43/extensions/CheckUser/schema/mysql/patch-cu_changes-drop-cuc_private.sql (END - exit=256)
* 19:53 MirahezeLSBot: [agent@mwtask151] sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/deleted.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/sql.php /srv/mediawiki-staging/1.43/maintenance/archives/patch-change_tag-ct_rc_id.sql (END - exit=256)
* 19:53 MirahezeLSBot: [agent@mwtask151] sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/deleted.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/sql.php /srv/mediawiki-staging/1.43/maintenance/archives/patch-revision-cleanup.sql (END - exit=256)
* 19:53 MirahezeLSBot: [agent@mwtask151] sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/deleted.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/sql.php /srv/mediawiki-staging/1.43/maintenance/archives/patch-page-page_links_updated-noinfinite.sql (END - exit=256)
* 19:50 MirahezeLSBot: [agent@mwtask151] sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/deleted.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/extensions/CheckUser/maintenance/populateCentralCheckUserIndexTables.php (START)
* 19:50 MirahezeLSBot: [agent@mwtask151] sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/deleted.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/sql.php /srv/mediawiki-staging/1.43/maintenance/archives/patch-searchindex-pk-titlelength.sql (START)
* 19:50 MirahezeLSBot: [agent@mwtask151] sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/deleted.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/fixAutoblockLogTitles.php (START)
* 19:50 MirahezeLSBot: [agent@mwtask151] sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/deleted.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/sql.php /srv/mediawiki-staging/1.43/maintenance/archives/patch-recentchanges-rc_id-bigint.sql (START)
* 19:50 MirahezeLSBot: [agent@mwtask151] sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/deleted.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/extensions/CheckUser/maintenance/deleteReadOldRowsInCuChanges.php (START)
* 19:50 MirahezeLSBot: [agent@mwtask151] sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/deleted.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/sql.php /srv/mediawiki-staging/1.43/extensions/CheckUser/schema/mysql/patch-cu_changes-drop-cuc_only_for_read_old.sql (START)
* 19:50 MirahezeLSBot: [agent@mwtask151] sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/deleted.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/sql.php /srv/mediawiki-staging/1.43/maintenance/archives/patch-change_tag-ct_rc_id.sql (START)
* 19:50 MirahezeLSBot: [agent@mwtask151] sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/deleted.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/sql.php /srv/mediawiki-staging/1.43/maintenance/archives/patch-page-page_links_updated-noinfinite.sql (START)
* 19:50 MirahezeLSBot: [agent@mwtask151] sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/deleted.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/sql.php /srv/mediawiki-staging/1.43/maintenance/archives/patch-pagelinks-drop-pl_title.sql (START)
* 19:50 MirahezeLSBot: [agent@mwtask151] sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/deleted.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/sql.php /srv/mediawiki-staging/1.43/extensions/CheckUser/schema/mysql/patch-cu_changes-drop-cuc_actiontext.sql (START)
* 19:50 MirahezeLSBot: [agent@mwtask151] sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/deleted.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/sql.php /srv/mediawiki-staging/1.43/maintenance/archives/patch-revision-cleanup.sql (START)
* 19:50 MirahezeLSBot: [agent@mwtask151] sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/deleted.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/sql.php /srv/mediawiki-staging/1.43/extensions/CheckUser/schema/mysql/patch-cu_changes-drop-cuc_private.sql (START)
* 19:50 MirahezeLSBot: [agent@mwtask151] sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/deleted.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/sql.php /srv/mediawiki-staging/1.43/extensions/CheckUser/schema/mysql/cuci_user.sql (START)
* 19:50 MirahezeLSBot: [agent@mwtask151] sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/databases.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/sql.php /srv/mediawiki-staging/1.43/extensions/CheckUser/schema/mysql/cuci_wiki_map.sql (START)
* 19:50 MirahezeLSBot: [agent@mwtask151] sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/deleted.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/sql.php /srv/mediawiki-staging/1.43/extensions/CheckUser/schema/mysql/cuci_temp_edit.sql (START)
* 19:45 MirahezeLSBot: [agent@mwtask151] sudo -u www-data /usr/local/bin/foreachwikiindblist /tmp/semanticmediawiki.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/extensions/SemanticMediaWiki/maintenance/setupStore.php (END - exit=0)
* 19:40 MirahezeLSBot: [agent@mwtask151] sudo -u www-data /usr/local/bin/foreachwikiindblist /tmp/semanticmediawiki.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/extensions/SemanticMediaWiki/maintenance/setupStore.php (START)
* 19:38 MirahezeLSBot: [agent@mwtask151] sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/databases.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/updateSpecialPages.php (START)
* 19:31 MirahezeLSBot: [agent@mwtask151] sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/databases.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/sql.php /srv/mediawiki/1.43/maintenance/archives/patch-pagelinks-drop-pl_title.sql (END - exit=2)
* 19:29 MirahezeLSBot: [agent@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/sql.php --wiki=bluearchivewiki (END - exit=2)
* 19:20 MirahezeLSBot: [agent@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 20s
* 19:19 MirahezeLSBot: [agent@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 19:18 MirahezeLSBot: [agent@mwtask181] DEPLOY ABORTED: Canary check failed for publictestwiki.com@mw183.wikitide.net
* 19:18 MirahezeLSBot: [agent@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 19:17 MirahezeLSBot: [agent@mwtask151] sudo -u www-data /usr/local/bin/foreachwikiindblist /tmp/titlekey.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/sql.php /srv/mediawiki/1.43/extensions/TitleKey/db_patches/abstractSchemaChanges/patch-modify-tk_key.sql (END - exit=0)
* 19:17 MirahezeLSBot: [agent@mwtask181] sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/databases.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/extensions/MirahezeMagic/maintenance/MigrateSearchIndexSql.php (START)
* 19:16 MirahezeLSBot: [agent@mwtask181] finished deploy of {'versions': '1.43', 'upgrade_extensions': 'MirahezeMagic'} to all - SUCCESS in 95s
* 19:15 MirahezeLSBot: [agent@mwtask181] starting deploy of {'versions': '1.43', 'upgrade_extensions': 'MirahezeMagic'} to all
* 19:12 MirahezeLSBot: [agent@mwtask151] sudo -u www-data /usr/local/bin/foreachwikiindblist /tmp/titlekey.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/sql.php /srv/mediawiki/1.43/extensions/TitleKey/db_patches/abstractSchemaChanges/patch-modify-tk_key.sql (START)
* 19:12 MirahezeLSBot: [agent@mwtask151] sudo -u www-data /usr/local/bin/foreachwikiindblist /tmp/titlekey.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/sql.php /srv/mediawiki-staging/1.43/extensions/TitleKey/db_patches/abstractSchemaChanges/patch-modify-tk_key.sql (END - exit=2)
* 19:12 MirahezeLSBot: [agent@mwtask151] sudo -u www-data /usr/local/bin/foreachwikiindblist /tmp/titlekey.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/sql.php /srv/mediawiki-staging/1.43/extensions/TitleKey/db_patches/abstractSchemaChanges/patch-modify-tk_key.sql (START)
* 19:04 MirahezeLSBot: [agent@mwtask151] sudo -u www-data /usr/local/bin/foreachwikiindblist /tmp/translate.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/sql.php /srv/mediawiki/1.43/extensions/Translate/sql/mysql/patch-translate_reviews-unsigned.sql (END - exit=0)
* 19:04 MirahezeLSBot: [agent@mwtask151] sudo -u www-data /usr/local/bin/foreachwikiindblist /tmp/translate.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/sql.php /srv/mediawiki/1.43/extensions/Translate/sql/mysql/patch-revtag-int-to-bigint-unsigned.sql (END - exit=0)
* 19:04 MirahezeLSBot: [agent@mwtask151] sudo -u www-data /usr/local/bin/foreachwikiindblist /tmp/translate.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/sql.php /srv/mediawiki/1.43/extensions/Translate/sql/mysql/translate_message_group_subscriptions.sql (END - exit=0)
* 19:04 MirahezeLSBot: [agent@mwtask151] sudo -u www-data /usr/local/bin/foreachwikiindblist /tmp/translate.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/sql.php /srv/mediawiki/1.43/extensions/Translate/sql/mysql/patch-translate_message_group_subscriptions-composite-primary-key.sql (END - exit=256)
* 19:03 MirahezeLSBot: [agent@mwtask151] sudo -u www-data /usr/local/bin/foreachwikiindblist /tmp/newsletter.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/sql.php /srv/mediawiki/1.43/extensions/Newsletter/sql/mysql/patch-drop-unique-indices.sql (END - exit=0)
* 19:00 MirahezeLSBot: [agent@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/sql.php --wiki=loginwiki --wikidb mhglobal /srv/mediawiki-staging/1.43/extensions/GlobalBlocking/sql/mysql/patch-globalblocks-modify-gb_autoblock_parent_id-default.sql (END - exit=0)
* 19:00 MirahezeLSBot: [agent@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/sql.php --wiki=loginwiki --wikidb mhglobal /srv/mediawiki-staging/1.43/extensions/GlobalBlocking/sql/mysql/patch-globalblocks-modify-gb_address-index.sql (END - exit=256)
* 19:00 MirahezeLSBot: [agent@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/sql.php --wiki=loginwiki --wikidb mhglobal /srv/mediawiki-staging/1.43/extensions/GlobalBlocking/sql/mysql/patch-globalblocks-drop-gb_by.sql (END - exit=0)
* 19:00 MirahezeLSBot: [agent@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/sql.php --wiki=loginwiki --wikidb mhglobal /srv/mediawiki-staging/1.43/extensions/GlobalBlocking/sql/mysql/patch-globalblocks-add-gb_enable_autoblock.sql (END - exit=256)
* 18:59 MirahezeLSBot: [agent@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/sql.php --wiki=loginwiki --wikidb mhglobal /srv/mediawiki-staging/1.43/extensions/GlobalBlocking/sql/mysql/patch-globalblocks-add-gb_create_account.sql (END - exit=256)
* 18:58 MirahezeLSBot: [agent@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/sql.php --wiki=loginwiki --wikidb mhglobal /srv/mediawiki-staging/1.43/extensions/GlobalBlocking/sql/mysql/patch-globalblocks-add-gb_autoblock_parent_id.sql (END - exit=256)
* 18:58 MirahezeLSBot: [agent@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/sql.php --wiki=loginwiki --wikidb mhglobal /srv/mediawiki-staging/1.43/extensions/GlobalBlocking/sql/mysql/patch-global_block_whitelist-default-gbw_address.sql (END - exit=0)
* 18:58 MirahezeLSBot: [agent@mwtask181] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/sql.php --wiki=loginwiki --wikidb mhglobal /srv/mediawiki-staging/1.43/extensions/CentralAuth/schema/mysql/patch-rq_type.sql (END - exit=256)
* 18:57 MirahezeLSBot: [agent@mwtask151] sudo -u www-data /usr/local/bin/foreachwikiindblist /tmp/newsletter.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/sql.php /srv/mediawiki/1.43/extensions/Newsletter/sql/mysql/patch-drop-unique-indices.sql (START)
* 18:57 MirahezeLSBot: [agent@mwtask151] sudo -u www-data /usr/local/bin/foreachwikiindblist /tmp/translate.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/sql.php /srv/mediawiki/1.43/extensions/Translate/sql/mysql/translate_message_group_subscriptions.sql (START)
* 18:57 MirahezeLSBot: [agent@mwtask151] sudo -u www-data /usr/local/bin/foreachwikiindblist /tmp/translate.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/sql.php /srv/mediawiki/1.43/extensions/Translate/sql/mysql/patch-translate_reviews-unsigned.sql (START)
* 18:57 MirahezeLSBot: [agent@mwtask151] sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/databases.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/sql.php /srv/mediawiki/1.43/extensions/AbuseFilter/db_patches/mysql/patch-drop-af_user.sql (START)
* 18:57 MirahezeLSBot: [agent@mwtask151] sudo -u www-data /usr/local/bin/foreachwikiindblist /tmp/translate.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/sql.php /srv/mediawiki/1.43/extensions/Translate/sql/mysql/patch-translate_message_group_subscriptions-composite-primary-key.sql (START)
* 18:57 MirahezeLSBot: [agent@mwtask151] sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/databases.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/sql.php /srv/mediawiki/1.43/extensions/AbuseFilter/db_patches/mysql/patch-drop-afh_user.sql (START)
* 18:57 MirahezeLSBot: [agent@mwtask151] sudo -u www-data /usr/local/bin/foreachwikiindblist /tmp/translate.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/sql.php /srv/mediawiki/1.43/extensions/Translate/sql/mysql/patch-revtag-int-to-bigint-unsigned.sql (START)
* 18:56 MirahezeLSBot: [agent@mwtask151] sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/databases.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/sql.php /srv/mediawiki/1.43/extensions/AbuseFilter/db_patches/mysql/patch-drop-af_user.sql (START)
* 18:56 MirahezeLSBot: [agent@mwtask151] sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/databases.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/sql.php /srv/mediawiki/1.43/extensions/AbuseFilter/db_patches/mysql/patch-drop-afh_user.sql (START)
* 18:54 MirahezeLSBot: [agent@mwtask151] sudo -u www-data /usr/local/bin/foreachwikiindblist /tmp/abusefilter.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/sql.php /srv/mediawiki/1.43/extensions/AbuseFilter/db_patches/mysql/patch-drop-afh_user.sql (END - exit=256)
* 18:54 MirahezeLSBot: [agent@mwtask151] sudo -u www-data /usr/local/bin/foreachwikiindblist /tmp/abusefilter.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/sql.php /srv/mediawiki/1.43/extensions/AbuseFilter/db_patches/mysql/patch-drop-af_user.sql (END - exit=256)
* 18:54 MirahezeLSBot: [agent@mwtask151] sudo -u www-data /usr/local/bin/foreachwikiindblist /tmp/abusefilter.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/sql.php /srv/mediawiki/1.43/extensions/AbuseFilter/db_patches/mysql/patch-drop-afh_user.sql (START)
* 18:54 MirahezeLSBot: [agent@mwtask151] sudo -u www-data /usr/local/bin/foreachwikiindblist /tmp/abusefilter.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/sql.php /srv/mediawiki/1.43/extensions/AbuseFilter/db_patches/mysql/patch-drop-af_user.sql (START)
* 18:48 MirahezeLSBot: [agent@mwtask171] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/extensions/GlobalBlocking/maintenance/UpdateAutoBlockParentIdColumn.php --wiki=metawiki (END - exit=0)
* 18:43 MirahezeLSBot: [agent@mwtask151] sudo -u www-data /usr/local/bin/foreachwikiindblist /tmp/discussiontools.json /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/extensions/DiscussionTools/maintenance/FixTrailingWhitespaceIds.php (END - exit=256)
* 18:43 MirahezeLSBot: [agent@mwtask151] sudo -u www-data /usr/local/bin/foreachwikiindblist /tmp/discussiontools.json /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/extensions/DiscussionTools/maintenance/FixTrailingWhitespaceIds.php (START)
* 18:43 MirahezeLSBot: [agent@mwtask151] sudo -u www-data /usr/local/bin/foreachwikiindblist /tmp/DiscussionTools.json /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/extensions/DiscussionTools/maintenance/FixTrailingWhitespaceIds.php (END - exit=256)
* 18:43 MirahezeLSBot: [agent@mwtask151] sudo -u www-data /usr/local/bin/foreachwikiindblist /tmp/DiscussionTools.json /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/extensions/DiscussionTools/maintenance/FixTrailingWhitespaceIds.php (START)
* 18:40 MirahezeLSBot: [agent@mwtask171] sudo -u www-data php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/extensions/CentralAuth/maintenance/migrateGuSalt.php --wiki=metawiki (END - exit=0)
* 18:30 MirahezeLSBot: [agent@mwtask171] sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/databases.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/extensions/CheckUser/maintenance/populateCentralCheckUserIndexTables.php (START)
* 18:30 MirahezeLSBot: [agent@mwtask171] sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/databases.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/extensions/CheckUser/maintenance/populateCentralCheckUserIndexTables.php (END - exit=2)
* 18:28 MirahezeLSBot: [agent@mwtask151] sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/databases.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/sql.php /srv/mediawiki/1.43/extensions/CheckUser/schema/mysql/cuci_wiki_map.sql (START)
* 18:28 MirahezeLSBot: [agent@mwtask151] sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/databases.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/sql.php /srv/mediawiki/1.43/extensions/CheckUser/schema/mysql/patch-cu_changes-drop-cuc_private.sql (START)
* 18:28 MirahezeLSBot: [agent@mwtask151] sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/databases.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/sql.php /srv/mediawiki/1.43/maintenance/archives/patch-pagelinks-drop-pl_title.sql (START)
* 18:27 MirahezeLSBot: [agent@mwtask151] sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/databases.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/sql.php /srv/mediawiki/1.43/maintenance/archives/patch-page-page_links_updated-noinfinite.sql (START)
* 18:26 MirahezeLSBot: [agent@mwtask151] sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/databases.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/sql.php /srv/mediawiki-staging/1.43/maintenance/archives/patch-page-page_links_updated-noinfinite.sql (START)
* 18:26 MirahezeLSBot: [agent@mwtask151] sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/databases.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/sql.php /srv/mediawiki-staging/1.43/extensions/CheckUser/schema/mysql/patch-cu_changes-drop-cuc_private.sql (START)
* 18:26 MirahezeLSBot: [agent@mwtask151] sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/databases.php /srv/mediawiki/1.43/maintenance/run.php /srv/mediawiki/1.43/maintenance/sql.php /srv/mediawiki-staging/1.43/extensions/CheckUser/schema/mysql/cuci_wiki_map.sql (START)
* 18:00 MirahezeLSBot: [agent@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 22s
* 18:00 MirahezeLSBot: [agent@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 17:57 MirahezeLSBot: [agent@mwtask181] sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/databases.php /srv/mediawiki/1.42/maintenance/run.php /srv/mediawiki/1.42/maintenance/sql.php /srv/mediawiki-staging/1.43/maintenance/archives/patch-searchindex-pk-titlelength.sql (START)
* 17:56 MirahezeLSBot: [agent@mwtask181] sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/databases.php /srv/mediawiki/1.42/maintenance/run.php /srv/mediawiki/1.42/maintenance/sql.php /srv/mediawiki-staging/1.43/maintenance/archives/patch-searchindex-pk-titlelength.sql (END - exit=2)
* 17:55 MirahezeLSBot: [agent@mwtask181] sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/databases.php /srv/mediawiki/1.42/maintenance/run.php /srv/mediawiki/1.42/maintenance/sql.php /srv/mediawiki-staging/1.43/maintenance/archives/patch-searchindex-pk-titlelength.sql (START)
* 17:55 MirahezeLSBot: [agent@mwtask181] sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/databases.php /srv/mediawiki/1.42/maintenance/run.php /srv/mediawiki/1.42/maintenance/sql.php /srv/mediawiki-staging/1.43/maintenance/archives/patch-change_tag-ct_rc_id.sql (START)
* 17:55 MirahezeLSBot: [agent@mwtask181] sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/databases.php /srv/mediawiki/1.42/maintenance/run.php /srv/mediawiki/1.42/maintenance/sql.php /srv/mediawiki-staging/1.43/maintenance/archives/patch-revision-cleanup.sql (START)
* 17:55 MirahezeLSBot: [agent@mwtask181] sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/databases.php /srv/mediawiki/1.42/maintenance/run.php /srv/mediawiki/1.42/maintenance/sql.php /srv/mediawiki-staging/1.43/maintenance/archives/patch-recentchanges-rc_id-bigint.sql (START)
* 06:58 Reception123: same as below for jbcstudioswiki and animalroyalewiki
* 06:51 Reception123: sudo -u www-data php /srv/mediawiki/1.42/extensions/CirrusSearch/maintenance/ForceSearchIndex.php --wiki outlasterwiki --skipLinks --indexOnSkip (logged in wrong order)
* 06:50 Reception123: sudo -u www-data php /srv/mediawiki/1.42/extensions/CirrusSearch/maintenance/ForceSearchIndex.php --wiki outlasterwiki --skipParse
* 06:50 Reception123: sudo -u www-data php /srv/mediawiki/1.42/extensions/CirrusSearch/maintenance/UpdateSearchIndexConfig.php --wiki outlasterwiki
* 00:50 MirahezeLSBot: [void@puppet181] Upgraded packages git-man, and git on swiftobject181
* 00:50 MirahezeLSBot: [void@puppet181] Upgraded packages git-man, and git on swiftobject161
* 00:50 MirahezeLSBot: [void@puppet181] Upgraded packages git-man, and git on swiftobject151
* 00:49 MirahezeLSBot: [void@puppet181] Upgraded packages git-man, and git on swiftproxy171
* 00:49 MirahezeLSBot: [void@puppet181] Upgraded packages git-man, and git on swiftobject171
* 00:49 MirahezeLSBot: [void@puppet181] Upgraded packages git-man, and git on swiftproxy161
* 00:48 MirahezeLSBot: [void@puppet181] Upgraded packages git-man, and git on swiftac171
* 00:48 MirahezeLSBot: [void@puppet181] Upgraded packages git-man, and git on test151
* 00:48 MirahezeLSBot: [void@puppet181] Upgraded packages git-man, and git on puppet181
* 00:48 MirahezeLSBot: [void@puppet181] Upgraded packages git-man, and git on reports171
* 00:47 MirahezeLSBot: [void@puppet181] Upgraded packages git-man, and git on os162
* 00:47 MirahezeLSBot: [void@puppet181] Upgraded packages git-man, and git on ns2
* 00:47 MirahezeLSBot: [void@puppet181] Upgraded packages git-man, and git on rdb151
* 00:47 MirahezeLSBot: [void@puppet181] Upgraded packages git-man, and git on prometheus151
* 00:46 MirahezeLSBot: [void@puppet181] Upgraded packages git-man, and git on phorge171
* 00:46 MirahezeLSBot: [void@puppet181] Upgraded packages git-man, and git on os161
* 00:46 MirahezeLSBot: [void@puppet181] Upgraded packages git-man, and git on mwtask181
* 00:46 MirahezeLSBot: [void@puppet181] Upgraded packages git-man, and git on mw184
* 00:45 MirahezeLSBot: [void@puppet181] Upgraded packages git-man, and git on mw154
* 00:45 MirahezeLSBot: [void@puppet181] Upgraded packages git-man, and git on mw183
* 00:45 MirahezeLSBot: [void@puppet181] Upgraded packages git-man, and git on mwtask151
* 00:44 MirahezeLSBot: [void@puppet181] Upgraded packages git-man, and git on mwtask171
* 00:44 MirahezeLSBot: [void@puppet181] Upgraded packages git-man, and git on mw181
* 00:44 MirahezeLSBot: [void@puppet181] Upgraded packages git-man, and git on os151
* 00:44 MirahezeLSBot: [void@puppet181] Upgraded packages git-man, and git on mw174
* 00:43 MirahezeLSBot: [void@puppet181] Upgraded packages git-man, and git on mwtask161
* 00:43 MirahezeLSBot: [void@puppet181] Upgraded packages git-man, and git on mw173
* 00:43 MirahezeLSBot: [void@puppet181] Upgraded packages git-man, and git on ns1
* 00:42 MirahezeLSBot: [void@puppet181] Upgraded packages git-man, and git on mw182
* 00:42 MirahezeLSBot: [void@puppet181] Upgraded packages git-man, and git on mw163
* 00:42 MirahezeLSBot: [void@puppet181] Upgraded packages git-man, and git on mw164
* 00:42 MirahezeLSBot: [void@puppet181] Upgraded packages git-man, and git on mw172
* 00:41 MirahezeLSBot: [void@puppet181] Upgraded packages git-man, and git on mw161
* 00:41 MirahezeLSBot: [void@puppet181] Upgraded packages git-man, and git on mw171
* 00:41 MirahezeLSBot: [void@puppet181] Upgraded packages git-man, and git on mw162
* 00:41 MirahezeLSBot: [void@puppet181] Upgraded packages git-man, and git on mw153
* 00:40 MirahezeLSBot: [void@puppet181] Upgraded packages git-man, and git on mw151
* 00:40 MirahezeLSBot: [void@puppet181] Upgraded packages git-man, and git on mw152
* 00:40 MirahezeLSBot: [void@puppet181] Upgraded packages git-man, and git on mon181
* 00:39 MirahezeLSBot: [void@puppet181] Upgraded packages git-man, and git on mem161
* 00:39 MirahezeLSBot: [void@puppet181] Upgraded packages git-man, and git on cloud15
* 00:39 MirahezeLSBot: [void@puppet181] Upgraded packages git-man, and git on cloud17
* 00:39 MirahezeLSBot: [void@puppet181] Upgraded packages git-man, and git on mattermost1
* 00:39 MirahezeLSBot: [void@puppet181] Upgraded packages git-man, and git on cloud16
* 00:38 MirahezeLSBot: [void@bots171] restart logbot
* 00:38 MirahezeLSBot: [void@puppet181] Upgraded packages git-man, and git on cloud18
* 00:38 MirahezeLSBot: [void@puppet181] Upgraded packages git-man, and git on bast161

## 2025-01-23 

* 00:23 MirahezeLSBot: [paladox@mwtask181] finished deploy of {'l10n': True, 'versions': ['1.42', '1.43'], 'upgrade_extensions': 'MirahezeMagic'} to all - SUCCESS in 1040s
* 00:21 MirahezeLSBot: [paladox@test151] finished deploy of {'l10n': True, 'versions': ['1.42', '1.43', '1.44'], 'upgrade_extensions': 'MirahezeMagic'} to test151 - SUCCESS in 945s
* 00:05 MirahezeLSBot: [paladox@test151] starting deploy of {'l10n': True, 'versions': ['1.42', '1.43', '1.44'], 'upgrade_extensions': 'MirahezeMagic'} to test151
* 00:05 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'l10n': True, 'versions': ['1.42', '1.43'], 'upgrade_extensions': 'MirahezeMagic'} to all

## 2025-01-22 

* 18:48 MirahezeLSBot: [reception@mwtask181] finished deploy of {'world': True, 'l10n': True, 'extension_list': True, 'force': True, 'versions': '1.42'} to all - SUCCESS in 565s
* 18:39 MirahezeLSBot: [reception@mwtask181] starting deploy of {'world': True, 'l10n': True, 'extension_list': True, 'force': True, 'versions': '1.42'} to all
* 18:38 MirahezeLSBot: [reception@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 23s
* 18:38 MirahezeLSBot: [reception@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 13:09 @paladox: installed nethogs on mw152 and db171

## 2025-01-21 

* 15:56 @paladox: run dist-upgrade on kafka181 and reboot
* 15:55 @paladox: run dist-upgrade on eventgate181 and reboot
* 15:54 @paladox: run dist-upgrade on changeprop151 and reboot
* 15:48 @paladox: run dist-upgrade on rdb151 and reboot
* 14:01 MirahezeLSBot: [paladox@test151] finished deploy of {'l10n': True, 'versions': ['1.42', '1.43', '1.44'], 'upgrade_extensions': 'CreateWiki'} to test151 - SUCCESS in 182s
* 13:58 MirahezeLSBot: [paladox@test151] starting deploy of {'l10n': True, 'versions': ['1.42', '1.43', '1.44'], 'upgrade_extensions': 'CreateWiki'} to test151
* 13:31 @paladox: increase rdb151 ram to 4gib
* 13:12 MirahezeLSBot: [paladox@mwtask181] finished deploy of {'l10n': True, 'versions': ['1.42', '1.43'], 'upgrade_extensions': 'CreateWiki'} to all - SUCCESS in 201s
* 13:09 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'l10n': True, 'versions': ['1.42', '1.43'], 'upgrade_extensions': 'CreateWiki'} to all
* 12:32 @paladox: restart db171

## 2025-01-20 

* 10:39 MirahezeLSBot: [reception@mwtask181] finished deploy of {'world': True, 'l10n': True, 'extension_list': True, 'versions': '1.42'} to all - SUCCESS in 576s
* 10:33 MirahezeLSBot: [reception@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 20s
* 10:33 MirahezeLSBot: [reception@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 10:29 MirahezeLSBot: [reception@mwtask181] starting deploy of {'world': True, 'l10n': True, 'extension_list': True, 'versions': '1.42'} to all
* 10:29 MirahezeLSBot: [reception@mwtask181] DEPLOY ABORTED: Non-Zero Exit Code in prep, see output.
* 10:29 MirahezeLSBot: [reception@mwtask181] starting deploy of {'world': True, 'l10n': True, 'versions': '1.42'} to all
* 10:21 MirahezeLSBot: [reception@mwtask181] finished deploy of {'world': True, 'force': True, 'versions': '1.42'} to all - SUCCESS in 158s
* 10:18 MirahezeLSBot: [reception@mwtask181] starting deploy of {'world': True, 'force': True, 'versions': '1.42'} to all

## 2025-01-19 

* 22:48 MirahezeLSBot: [macfan@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 21s
* 22:47 MirahezeLSBot: [macfan@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 13:16 MirahezeLSBot: [paladox@test151] finished deploy of {'l10n': True, 'versions': ['1.42', '1.43', '1.44'], 'upgrade_extensions': 'CommentStreams'} to test151 - SUCCESS in 180s
* 13:15 MirahezeLSBot: [paladox@mwtask181] finished deploy of {'l10n': True, 'versions': ['1.42', '1.43'], 'upgrade_extensions': 'CommentStreams'} to all - SUCCESS in 189s
* 13:13 MirahezeLSBot: [paladox@test151] starting deploy of {'l10n': True, 'versions': ['1.42', '1.43', '1.44'], 'upgrade_extensions': 'CommentStreams'} to test151
* 13:12 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'l10n': True, 'versions': ['1.42', '1.43'], 'upgrade_extensions': 'CommentStreams'} to all
* 12:37 MirahezeLSBot: [paladox@mwtask181] finished deploy of {'config': True, 'force': True} to all - SUCCESS in 62s
* 12:36 MirahezeLSBot: [paladox@mwtask181] DEPLOY ABORTED: Canary check failed for publictestwiki.com@mw153.wikitide.net

## 2025-01-17 

* 12:31 Reception123: (restarted that is..)
* 03:46 MirahezeLSBot: [void@puppet181] Upgraded packages rsync on swiftproxy171
* 03:46 MirahezeLSBot: [void@puppet181] Upgraded packages rsync on swiftproxy161
* 03:45 MirahezeLSBot: [void@puppet181] Upgraded packages rsync on swiftobject181
* 03:45 MirahezeLSBot: [void@puppet181] Upgraded packages rsync on swiftobject171
* 03:45 MirahezeLSBot: [void@puppet181] Upgraded packages rsync on swiftobject161
* 03:44 MirahezeLSBot: [void@puppet181] Upgraded packages rsync on swiftobject151
* 03:44 MirahezeLSBot: [void@puppet181] Upgraded packages rsync on swiftac171
* 03:44 MirahezeLSBot: [void@puppet181] Upgraded packages rsync on test151
* 03:44 MirahezeLSBot: [void@puppet181] Upgraded packages rsync on reports171
* 03:43 MirahezeLSBot: [void@puppet181] Upgraded packages rsync on puppet181
* 03:43 MirahezeLSBot: [void@puppet181] Upgraded packages rsync on rdb151
* 03:43 MirahezeLSBot: [void@puppet181] Upgraded packages rsync on prometheus151
* 03:43 MirahezeLSBot: [void@puppet181] Upgraded packages rsync on os162
* 03:42 MirahezeLSBot: [void@puppet181] Upgraded packages rsync on phorge171
* 03:42 MirahezeLSBot: [void@puppet181] Upgraded packages rsync on ns2
* 03:42 MirahezeLSBot: [void@puppet181] Upgraded packages rsync on os161
* 03:41 MirahezeLSBot: [void@puppet181] Upgraded packages rsync on mw184
* 03:41 MirahezeLSBot: [void@puppet181] Upgraded packages rsync on mw183
* 03:41 MirahezeLSBot: [void@puppet181] Upgraded packages rsync on mw182
* 03:41 MirahezeLSBot: [void@puppet181] Upgraded packages rsync on mw154
* 03:40 MirahezeLSBot: [void@puppet181] Upgraded packages rsync on mwtask171
* 03:40 MirahezeLSBot: [void@puppet181] Upgraded packages rsync on mwtask161
* 03:40 MirahezeLSBot: [void@puppet181] Upgraded packages rsync on mwtask151
* 03:40 MirahezeLSBot: [void@puppet181] Upgraded packages rsync on mwtask181
* 03:39 MirahezeLSBot: [void@puppet181] Upgraded packages rsync on mw181
* 03:39 MirahezeLSBot: [void@puppet181] Upgraded packages rsync on mw174
* 03:39 MirahezeLSBot: [void@puppet181] Upgraded packages rsync on mw173
* 03:38 MirahezeLSBot: [void@puppet181] Upgraded packages rsync on mw163
* 03:38 MirahezeLSBot: [void@puppet181] Upgraded packages rsync on mw172
* 03:38 MirahezeLSBot: [void@puppet181] Upgraded packages rsync on os151
* 03:38 MirahezeLSBot: [void@puppet181] Upgraded packages rsync on mw161
* 03:37 MirahezeLSBot: [void@puppet181] Upgraded packages rsync on ns1
* 03:37 MirahezeLSBot: [void@puppet181] Upgraded packages rsync on mw171
* 03:37 MirahezeLSBot: [void@puppet181] Upgraded packages rsync on mw162
* 03:37 MirahezeLSBot: [void@puppet181] Upgraded packages rsync on mw153
* 03:36 MirahezeLSBot: [void@puppet181] Upgraded packages rsync on mw164
* 03:36 MirahezeLSBot: [void@puppet181] Upgraded packages rsync on mw152
* 03:36 MirahezeLSBot: [void@puppet181] Upgraded packages rsync on mw151
* 03:36 MirahezeLSBot: [void@puppet181] Upgraded packages rsync on mon181
* 03:35 MirahezeLSBot: [void@puppet181] Upgraded packages rsync on mem161
* 03:35 MirahezeLSBot: [void@puppet181] Upgraded packages rsync on mattermost1
* 03:35 MirahezeLSBot: [void@puppet181] Upgraded packages rsync, and libgstreamer1.0-0 on cloud17
* 03:35 MirahezeLSBot: [void@puppet181] Upgraded packages rsync, and libgstreamer1.0-0 on cloud16
* 03:34 MirahezeLSBot: [void@puppet181] Upgraded packages rsync on db181
* 03:34 MirahezeLSBot: [void@puppet181] Upgraded packages rsync on graylog161
* 03:34 MirahezeLSBot: [void@puppet181] Upgraded packages rsync, and libgstreamer1.0-0 on cloud15
* 03:34 MirahezeLSBot: [void@puppet181] Upgraded packages rsync on matomo151
* 03:33 MirahezeLSBot: [void@puppet181] Upgraded packages rsync on bast161
* 03:33 MirahezeLSBot: [void@puppet181] Upgraded packages rsync on cp37
* 03:33 MirahezeLSBot: [void@puppet181] Upgraded packages rsync, and libgstreamer1.0-0 on cloud18
* 03:33 MirahezeLSBot: [void@puppet181] Upgraded packages rsync on ldap171
* 03:32 MirahezeLSBot: [void@puppet181] Upgraded packages rsync on bast181
* 03:32 MirahezeLSBot: [void@puppet181] Upgraded packages rsync on cp36
* 03:32 MirahezeLSBot: [void@puppet181] Upgraded packages rsync on db171
* 03:32 MirahezeLSBot: [void@puppet181] Upgraded packages rsync on mem151
* 03:31 MirahezeLSBot: [void@puppet181] Upgraded packages rsync on db161
* 03:31 MirahezeLSBot: [void@puppet181] Upgraded packages rsync on jobchron171
* 03:31 MirahezeLSBot: [void@puppet181] Upgraded packages rsync on eventgate181
* 03:31 MirahezeLSBot: [void@puppet181] Upgraded packages rsync on graphite151
* 03:31 MirahezeLSBot: [void@puppet181] Upgraded packages rsync on db151
* 03:30 MirahezeLSBot: [void@puppet181] Upgraded packages rsync on db182
* 03:30 MirahezeLSBot: [void@puppet181] Upgraded packages rsync on kafka181
* 03:30 MirahezeLSBot: [void@puppet181] Upgraded packages rsync on bots171
* 03:30 MirahezeLSBot: [void@puppet181] Upgraded packages rsync on db172
* 03:29 MirahezeLSBot: [void@puppet181] Upgraded packages rsync on changeprop151

## 2025-01-16 

* 12:54 MirahezeLSBot: [paladox@mwtask181] [root@mwtask181:/srv/mediawiki/1.42/maintenance]# sudo -u www-data php refreshLinks.php --wiki kanrikyarawiki - T13084
* 12:52 @paladox: upgrade rsync on all servers
* 00:19 MirahezeLSBot: [paladox@mwtask181] finished deploy of {'l10n': True, 'versions': ['1.42', '1.43'], 'upgrade_extensions': ['MirahezeMagic', 'RemovePII']} to all - SUCCESS in 232s
* 00:19 MirahezeLSBot: [paladox@test151] finished deploy of {'l10n': True, 'versions': ['1.42', '1.43', '1.44'], 'upgrade_extensions': ['MirahezeMagic', 'RemovePII']} to test151 - SUCCESS in 176s
* 00:16 MirahezeLSBot: [paladox@test151] starting deploy of {'l10n': True, 'versions': ['1.42', '1.43', '1.44'], 'upgrade_extensions': ['MirahezeMagic', 'RemovePII']} to test151
* 00:16 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'l10n': True, 'versions': ['1.42', '1.43'], 'upgrade_extensions': ['MirahezeMagic', 'RemovePII']} to all

## 2025-01-14 

* 23:33 MirahezeLSBot: [oa@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 21s
* 23:32 MirahezeLSBot: [oa@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 23:30 MirahezeLSBot: [oa@mwtask181] finished deploy of {'config': True, 'world': True, 'l10n': True, 'extension_list': True, 'versions': '1.42'} to all - SUCCESS in 594s
* 23:21 MirahezeLSBot: [oa@mwtask181] starting deploy of {'config': True, 'world': True, 'l10n': True, 'extension_list': True, 'versions': '1.42'} to all
* 20:49 MirahezeLSBot: [paladox@test151] finished deploy of {'l10n': True, 'versions': ['1.42', '1.43', '1.44'], 'upgrade_extensions': ['DataTransfer', 'GlobalBlocking', 'SocialProfile']} to test151 - SUCCESS in 428s
* 20:45 MirahezeLSBot: [paladox@mwtask181] finished deploy of {'l10n': True, 'versions': ['1.42', '1.43'], 'upgrade_extensions': ['DataTransfer', 'GlobalBlocking', 'SocialProfile']} to all - SUCCESS in 315s
* 20:42 MirahezeLSBot: [paladox@test151] starting deploy of {'l10n': True, 'versions': ['1.42', '1.43', '1.44'], 'upgrade_extensions': ['DataTransfer', 'GlobalBlocking', 'SocialProfile']} to test151
* 20:39 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'l10n': True, 'versions': ['1.42', '1.43'], 'upgrade_extensions': ['DataTransfer', 'GlobalBlocking', 'SocialProfile']} to all
* 17:55 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.42/maintenance/run.php /srv/mediawiki/1.42/maintenance/importImages.php --wiki=thrillingintentwiki images --search-recursively (END - exit=0)
* 17:51 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.42/maintenance/run.php /srv/mediawiki/1.42/maintenance/importImages.php --wiki=thrillingintentwiki images --search-recursively (START)

## 2025-01-13 

* 15:40 MirahezeLSBot: [reception@mwtask181] finished deploy of {'versions': '1.43', 'upgrade_skins': 'Medik'} to all - SUCCESS in 19s
* 15:39 MirahezeLSBot: [reception@mwtask181] starting deploy of {'versions': '1.43', 'upgrade_skins': 'Medik'} to all
* 15:38 MirahezeLSBot: [reception@mwtask181] finished deploy of {'versions': '1.42', 'upgrade_skins': 'Medik'} to all - SUCCESS in 21s
* 15:38 MirahezeLSBot: [reception@mwtask181] starting deploy of {'versions': '1.42', 'upgrade_skins': 'Medik'} to all
* 06:32 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.42/maintenance/run.php /srv/mediawiki/1.42/extensions/MirahezeMagic/maintenance/renameDatabase.php --wiki=loginwiki --old=thedualhorizonwiki --new=thelonehorizonwiki (END - exit=0)
* 06:31 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.42/maintenance/run.php /srv/mediawiki/1.42/extensions/MirahezeMagic/maintenance/renameDatabase.php --wiki=loginwiki --old=bordrrevivedwiki --new=fraudulentfronterawiki (END - exit=256)
* 06:30 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.42/maintenance/run.php /srv/mediawiki/1.42/extensions/MirahezeMagic/maintenance/renameDatabase.php --wiki=loginwiki --old=projectahkyuwiki --new=bebuildinghistorywiki (END - exit=0)
* 06:28 Reception123: sudo -u www-data php /srv/mediawiki/1.42/extensions/CirrusSearch/maintenance/ForceSearchIndex.php --wiki cafewiki --skipParse
* 06:28 Reception123: sudo -u www-data php /srv/mediawiki/1.42/extensions/CirrusSearch/maintenance/ForceSearchIndex.php --wiki cafewiki --skipLinks --indexOnSkip
* 06:27 Reception123: sudo -u www-data php /srv/mediawiki/1.42/extensions/CirrusSearch/maintenance/UpdateSearchIndexConfig.php --wiki cafewiki

## 2025-01-11 

* 07:39 Reception123: sudo -u www-data php /srv/mediawiki/1.42/extensions/CirrusSearch/maintenance/ForceSearchIndex.php --wiki utgwiki --skipParse
* 07:39 Reception123: sudo -u www-data php /srv/mediawiki/1.42/extensions/CirrusSearch/maintenance/ForceSearchIndex.php --wiki utgwiki --skipLinks --indexOnSkip
* 07:39 Reception123: sudo -u www-data php /srv/mediawiki/1.42/extensions/CirrusSearch/maintenance/UpdateSearchIndexConfig.php --wiki utgwiki
* 07:38 MirahezeLSBot: [reception@mwtask181] finished deploy of {'files': '../mediawiki/1.42/extensions/SemanticMediaWiki/.smw.json'} to all - SUCCESS in 18s
* 07:38 MirahezeLSBot: [reception@mwtask181] starting deploy of {'files': '../mediawiki/1.42/extensions/SemanticMediaWiki/.smw.json'} to all
* 07:38 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.42/maintenance/run.php /srv/mediawiki/1.42/extensions/SemanticMediaWiki/maintenance/setupStore.php --wiki=lingowiki (END - exit=0)
* 07:38 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.42/maintenance/run.php /srv/mediawiki/1.42/extensions/SemanticMediaWiki/maintenance/setupStore.php --wiki=lingowiki (END - exit=0)
* 07:34 MirahezeLSBot: [reception@mwtask181] finished deploy of {'files': '../mediawiki/1.42/extensions/SemanticMediaWiki/.smw.json'} to all - SUCCESS in 18s
* 07:33 MirahezeLSBot: [reception@mwtask181] starting deploy of {'files': '../mediawiki/1.42/extensions/SemanticMediaWiki/.smw.json'} to all
* 07:33 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.42/maintenance/run.php /srv/mediawiki/1.42/extensions/SemanticMediaWiki/maintenance/setupStore.php --wiki=alphacentauriwiki (END - exit=0)
* 07:33 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.42/maintenance/run.php /srv/mediawiki/1.42/extensions/SemanticMediaWiki/maintenance/setupStore.php --wiki=alphacentauriwiki (END - exit=0)
* 07:32 MirahezeLSBot: [reception@mwtask181] finished deploy of {'files': '../mediawiki/1.42/extensions/SemanticMediaWiki/.smw.json'} to all - SUCCESS in 18s
* 07:32 MirahezeLSBot: [reception@mwtask181] starting deploy of {'files': '../mediawiki/1.42/extensions/SemanticMediaWiki/.smw.json'} to all
* 07:31 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.42/maintenance/run.php /srv/mediawiki/1.42/extensions/SemanticMediaWiki/maintenance/setupStore.php --wiki=2b2tocewiki (END - exit=0)
* 07:31 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.42/maintenance/run.php /srv/mediawiki/1.42/extensions/SemanticMediaWiki/maintenance/setupStore.php --wiki=2b2tocewiki (END - exit=0)
* 07:29 Reception123: sudo -u www-data php /srv/mediawiki/1.42/extensions/CirrusSearch/maintenance/ForceSearchIndex.php --wiki qualtiversewikiwiki --skipParse
* 07:29 Reception123: sudo -u www-data php /srv/mediawiki/1.42/extensions/CirrusSearch/maintenance/ForceSearchIndex.php --wiki qualtiversewikiwiki --skipLinks --indexOnSkip
* 07:28 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.42/maintenance/run.php /srv/mediawiki/1.42/extensions/SemanticMediaWiki/maintenance/setupStore.php --wiki=gejrfleaudacierwiki sudo -u www-data php /srv/mediawiki/1.42/extensions/CirrusSearch/maintenance/UpdateSearchIndexConfig.php --wiki qualtiversewikiwiki (END - exit=256)
* 07:27 Reception123:  sudo -u www-data php /srv/mediawiki/1.42/extensions/CirrusSearch/maintenance/UpdateSearchIndexConfig.php --wiki qualtiversewikiwiki
* 07:27 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.42/maintenance/run.php /srv/mediawiki/1.42/extensions/SemanticMediaWiki/maintenance/setupStore.php --wiki=gejrfleaudacierwiki sudo -u www-data php /srv/mediawiki/1.42/extensions/CirrusSearch/maintenance/UpdateSearchIndexConfig.php --wiki qualtiversewikiwiki (END - exit=256)
* 07:23 MirahezeLSBot: [reception@mwtask181] finished deploy of {'files': '../mediawiki/1.42/extensions/SemanticMediaWiki/.smw.json'} to all - SUCCESS in 18s
* 07:23 MirahezeLSBot: [reception@mwtask181] starting deploy of {'files': '../mediawiki/1.42/extensions/SemanticMediaWiki/.smw.json'} to all
* 07:23 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.42/maintenance/run.php /srv/mediawiki/1.42/extensions/SemanticMediaWiki/maintenance/setupStore.php --wiki=gejrfleaudacierwiki (END - exit=0)
* 07:23 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.42/maintenance/run.php /srv/mediawiki/1.42/extensions/SemanticMediaWiki/maintenance/setupStore.php --wiki=gejrfleaudacierwiki (END - exit=0)
* 07:21 MirahezeLSBot: [reception@mwtask181] finished deploy of {'files': '../mediawiki/1.42/extensions/SemanticMediaWiki/.smw.json'} to all - SUCCESS in 19s
* 07:20 MirahezeLSBot: [reception@mwtask181] starting deploy of {'files': '../mediawiki/1.42/extensions/SemanticMediaWiki/.smw.json'} to all
* 07:20 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.42/maintenance/run.php /srv/mediawiki/1.42/extensions/SemanticMediaWiki/maintenance/setupStore.php --wiki=ecopediawiki (END - exit=0)
* 07:20 MirahezeLSBot: [reception@mwtask181] sudo -u www-data php /srv/mediawiki/1.42/maintenance/run.php /srv/mediawiki/1.42/extensions/SemanticMediaWiki/maintenance/setupStore.php --wiki=ecopediawiki (END - exit=0)

## 2025-01-09 

* 00:03 MacFan4000: delete 394 private keys from git that don't have a corresponding public key

## 2025-01-07 

* 20:27 MirahezeLSBot: [paladox@mwtask181] finished deploy of {'versions': ['1.42', '1.43'], 'upgrade_extensions': 'mw-snapblocks'} to all - SUCCESS in 41s
* 20:26 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'versions': ['1.42', '1.43'], 'upgrade_extensions': 'mw-snapblocks'} to all
* 20:23 MirahezeLSBot: [paladox@mwtask181] finished deploy of {'upgrade_world': True, 'upgrade_vendor': True, 'versions': '1.42', 'upgrade_extensions': 'all', 'upgrade_skins': 'all'} to all - SUCCESS in 1652s
* 19:56 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'upgrade_world': True, 'upgrade_vendor': True, 'versions': '1.42', 'upgrade_extensions': 'all', 'upgrade_skins': 'all'} to all
* 19:55 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'upgrade_world': True, 'upgrade_vendor': True, 'versions': '1.42', 'upgrade_extensions': 'all', 'upgrade_skins': 'all'} to mwtask181
* 19:50 MirahezeLSBot: [paladox@mwtask181] finished deploy of {'upgrade_vendor': True, 'versions': '1.42'} to mwtask181 - SUCCESS in 22s
* 19:49 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'upgrade_vendor': True, 'versions': '1.42'} to mwtask181
* 19:42 MirahezeLSBot: [paladox@mwtask181] finished deploy of {'upgrade_world': True, 'versions': '1.42', 'upgrade_extensions': 'all', 'upgrade_skins': 'all'} to mwtask181 - SUCCESS in 540s
* 19:33 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'upgrade_world': True, 'versions': '1.42', 'upgrade_extensions': 'all', 'upgrade_skins': 'all'} to mwtask181
* 19:33 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'upgrade_world': True, 'versions': '1.42', 'upgrade_extensions': 'all', 'upgrade_skins': 'all'} to all
* 19:22 MirahezeLSBot: [paladox@mwtask181] DEPLOY ABORTED: Non-Zero Exit Code in prep, see output.
* 19:18 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'upgrade_world': True, 'versions': '1.42', 'upgrade_extensions': 'all', 'upgrade_skins': 'all'} to all

## 2025-01-06 

* 22:52 MirahezeLSBot: [paladox@mwtask181] finished deploy of {'config': True} to all - SUCCESS in 19s
* 22:52 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'config': True} to all
* 22:52 MirahezeLSBot: [paladox@test151] finished deploy of {'config': True} to test151 - SUCCESS in 0s
* 22:52 MirahezeLSBot: [paladox@test151] starting deploy of {'config': True} to test151
* 22:52 MirahezeLSBot: [paladox@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 20s
* 22:51 MirahezeLSBot: [paladox@test151] finished deploy of {'pull': 'config', 'config': True} to test151 - SUCCESS in 1s
* 22:51 MirahezeLSBot: [paladox@test151] starting deploy of {'pull': 'config', 'config': True} to test151
* 22:51 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 22:51 MirahezeLSBot: [paladox@mwtask181] finished deploy of {'upgrade_world': True, 'upgrade_vendor': True, 'versions': '1.43', 'upgrade_extensions': 'all', 'upgrade_skins': 'all'} to all - SUCCESS in 1715s
* 22:44 MirahezeLSBot: [paladox@test151] finished deploy of {'upgrade_world': True, 'upgrade_vendor': True, 'force': True, 'force_upgrade': True, 'versions': ['1.42', '1.43', '1.44'], 'upgrade_extensions': 'all', 'upgrade_skins': 'all'} to test151 - SUCCESS in 3648s
* 22:22 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'upgrade_world': True, 'upgrade_vendor': True, 'versions': '1.43', 'upgrade_extensions': 'all', 'upgrade_skins': 'all'} to all
* 21:44 MirahezeLSBot: [paladox@test151] starting deploy of {'upgrade_world': True, 'upgrade_vendor': True, 'force': True, 'force_upgrade': True, 'versions': ['1.42', '1.43', '1.44'], 'upgrade_extensions': 'all', 'upgrade_skins': 'all'} to test151
* 21:41 MirahezeLSBot: [paladox@test151] starting deploy of {'upgrade_world': True, 'upgrade_vendor': True, 'force_upgrade': True, 'versions': ['1.42', '1.43', '1.44'], 'upgrade_extensions': 'all', 'upgrade_skins': 'all'} to test151
* 21:40 MirahezeLSBot: [paladox@mwtask181] finished deploy of {'config': True} to all - SUCCESS in 19s
* 21:40 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'config': True} to all
* 21:40 MirahezeLSBot: [paladox@mwtask181] finished deploy of {'pull': 'config', 'config': True} to all - SUCCESS in 20s
* 21:39 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'pull': 'config', 'config': True} to all
* 21:34 MirahezeLSBot: [paladox@mwtask181] finished deploy of {'l10n': True, 'versions': ['1.42', '1.43'], 'upgrade_extensions': 'Moderation'} to all - SUCCESS in 237s
* 21:30 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'l10n': True, 'versions': ['1.42', '1.43'], 'upgrade_extensions': 'Moderation'} to all
* 21:30 MirahezeLSBot: [paladox@test151] DEPLOY ABORTED: Non-Zero Exit Code in prep, see output.
* 21:30 MirahezeLSBot: [paladox@mwtask181] finished deploy of {'l10n': True, 'versions': ['1.42', '1.43'], 'upgrade_extensions': 'WikiForum'} to all - SUCCESS in 840s
* 21:16 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'l10n': True, 'versions': ['1.42', '1.43'], 'upgrade_extensions': 'WikiForum'} to all
* 21:15 MirahezeLSBot: [paladox@test151] starting deploy of {'upgrade_world': True, 'upgrade_vendor': True, 'force_upgrade': True, 'versions': ['1.42', '1.43', '1.44'], 'upgrade_extensions': 'all', 'upgrade_skins': 'all'} to test151
* 16:29 RhinosF1: switched beta to TLS1.3 only
* 16:25 MirahezeLSBot: [paladox@test151] starting deploy of {'upgrade_world': True, 'upgrade_vendor': True, 'versions': ['1.42', '1.43', '1.44'], 'upgrade_extensions': 'all', 'upgrade_skins': 'all'} to test151

## 2025-01-04 

* 23:35 MirahezeLSBot: [paladox@test151] finished deploy of {'versions': ['1.42', '1.43', '1.44'], 'upgrade_extensions': 'TabberNeue'} to test151 - SUCCESS in 3s
* 23:35 MirahezeLSBot: [paladox@test151] starting deploy of {'versions': ['1.42', '1.43', '1.44'], 'upgrade_extensions': 'TabberNeue'} to test151
* 23:34 MirahezeLSBot: [paladox@mwtask181] finished deploy of {'versions': ['1.42', '1.43'], 'upgrade_extensions': 'TabberNeue'} to all - SUCCESS in 40s
* 23:33 MirahezeLSBot: [paladox@mwtask181] starting deploy of {'versions': ['1.42', '1.43'], 'upgrade_extensions': 'TabberNeue'} to all

## 2025-01-03 

* 19:02 RhinosF1: importing 212 custom hostnames from domains at apex in miraheze/dns to cloudflare config

## 2025-01-01 

* 23:04 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.42/maintenance/run.php /srv/mediawiki/1.42/maintenance/importImages.php --wiki=sexypediawiki images --search-recursively (END - exit=0)
* 22:44 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.42/maintenance/run.php /srv/mediawiki/1.42/maintenance/importImages.php --wiki=sexypediawiki images --search-recursively (START)
* 22:07 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.42/maintenance/run.php /srv/mediawiki/1.42/maintenance/initSiteStats.php --wiki=sexypediawiki --update (END - exit=0)
* 22:07 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.42/maintenance/run.php /srv/mediawiki/1.42/maintenance/rebuildall.php --wiki=sexypediawiki (END - exit=0)
* 21:53 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.42/maintenance/run.php /srv/mediawiki/1.42/maintenance/rebuildall.php --wiki=sexypediawiki (START)
* 21:53 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.42/maintenance/run.php /srv/mediawiki/1.42/maintenance/importDump.php --wiki=sexypediawiki tumblrsexymen_pages_full.xml --no-updates (END - exit=0)
* 20:50 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.42/maintenance/run.php /srv/mediawiki/1.42/maintenance/importDump.php --wiki=sexypediawiki tumblrsexymen_pages_full.xml --no-updates (START)
* 20:11 MirahezeLSBot: [macfan@mwtask181] sudo -u www-data php /srv/mediawiki/1.42/maintenance/run.php /srv/mediawiki/1.42/extensions/OATHAuth/maintenance/disableOATHAuthForUser.php --wiki=metawiki MacFan4000 (END - exit=0)
* 13:14 MirahezeLSBot: [paladox@mwtask181] sudo -u www-data php cleanupTitles.php --wiki lustfuldesireswiki

----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:Server_admin_log)**