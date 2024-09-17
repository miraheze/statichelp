---
title: Tech:Server admin log/2019
---

`{{ {{TOC right}} }}`
## 2019-12-31 

* 19:45 paladox: ManageWikiCDB::changes( 'namespaces' ); - hispanowiki
* 19:45 paladox: ManageWikiCDB::changes( 'namespaces' ); - privadowiki
* 19:40 paladox: MariaDB [mhglobal]> delete from mw_namespaces where ns_dbname = 'privadowiki' and ns_namespace_id = 1633;
* 19:12 paladox: MariaDB [mhglobal]> delete from mw_namespaces where ns_dbname = 'hispanowiki' and ns_namespace_id = 3011; - T4994
* 19:12 paladox: MariaDB [mhglobal]> delete from mw_namespaces where ns_dbname = 'hispanowiki' and ns_namespace_id = 3007; - T4994
* 19:11 paladox: MariaDB [mhglobal]> delete from mw_namespaces where ns_dbname = 'hispanowiki' and ns_namespace_id = 3003; - T4994
* 18:41 paladox: rm -rf /srv/mediawiki/w/cache/managewiki/** on mw* and lizardfs6
* 18:22 paladox: MariaDB [mhglobal]> update mw_namespaces set ns_content_model = *where ns_namespace_id = 828;
* 18:21 paladox: rebuild lc on mw* and lizardfs6
* 18:07 paladox: MariaDB [mhglobal]> update mw_namespaces set ns_content_model =* where ns_dbname = 'metawiki' and ns_namespace_id = 828;
* 18:06 paladox: MariaDB [mhglobal]> update mw_namespaces set ns_dbname = 'metawiki' where ns_dbname = 'metawikis' and ns_namespace_id = 828;
* 18:01 paladox: MariaDB [mhglobal]> update mw_namespaces set ns_dbname = 'metawikis' where ns_dbname = 'metawiki' and ns_namespace_id = 828;
* 13:37 paladox: reboot puppet1
* 01:01 paladox: restart logbot on misc1
* 00:58 paladox: root@misc2:/srv/redis# rm dump.rdb
* 00:58 paladox: root@misc2:/srv/redis# rm appendonly.aof
* 00:43 paladox: rebuild lc on mw* and lizardfs6

## 2019-12-30 

* 22:47 paladox: restart nginx on cp*
* 22:47 paladox: restart nginx and php7.3-fpm on mw* and lizardfs6

## 2019-12-29 

* 23:32 paladox: restart nginx and php7.3-fpm on mw* and lizardfs6
* 22:28 paladox: sudo -u www-data php populateGroupPermissionsWithDefaults.php --wiki=cosasdemifamiliawiki --overwrite - mw1
* 18:20 paladox: varnish> ban req.http.Host == donate.miraheze.org - cp2, cp3 and cp4
* 18:17 paladox: varnish> ban req.http.Host == miraheze.org - cp3
* 18:17 paladox: varnish> ban req.http.Host == miraheze.org - cp2
* 18:16 paladox: varnish> ban req.http.Host == miraheze.org - cp4
* 16:20 Reception123: reception@mw1:~$ sudo -u www-data php /srv/mediawiki/w//maintenance/deleteBatch.php  -r "let's try this again" -u Reception123 /home/reception/twinkledel.txt --wiki testwiki

## 2019-12-28 

* 22:43 paladox: rebuild lc on mw* and lizard
* 01:43 paladox: reboot cp3
* 01:41 paladox: apt-get install linux-image-amd64
* 01:39 paladox: apt-get upgrade - cp3

## 2019-12-27 

* 07:45 John: create mw_settings on mhglobal

## 2019-12-26 

* 16:46 paladox: rebuild lc on mw* and lizardfs6
* 11:56 Reception123: restarted jobrunner
* 11:42 Reception123: re-ran jobs above
* 11:38 Reception123: reception@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php runJobs.php --wiki diavwiki

## 2019-12-25 

* 23:30 paladox: restart jobchron on lizardfs6
* 22:46 John: running jobs for meta on mw1

## 2019-12-24 

* 16:59 paladox: reimage cp4 a debian 10
* 16:54 paladox: depool and repool mw3, restart php7.3-fpm and nginx
* 16:53 paladox: repool lizardfs6
* 16:52 paladox: depool lizardfs6
* 16:25 paladox: turn off TUN on cp4
* 13:43 paladox: apt-get upgrade on cp2
* 13:15 paladox: [13:12:00]  <+paladox>	!log restart varnish on cp4
* 13:13 paladox: apt-get upgrade on cp4
* 13:12 paladox: restart stunnel4 on cp4
* 02:05 paladox: sudo service jobrunner restart && sudo service jobchron restart (lizardfs6)
* 01:32 paladox: /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/maintenance/sql.php /srv/mediawiki/w/extensions/OATHAuth/sql/mysql/patch-remove_module_specific_fields.sql
* 01:31 paladox: /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/maintenance/sql.php 	/srv/mediawiki/w/extensions/Wikibase/repo/sql/AddNormalizedTermsTablesDDL.sql
* 01:31 paladox: /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/maintenance/sql.php /srv/mediawiki/w/extensions/PageTriage/sql/PageTriageTagsPatch-recreated.sql
* 01:11 John: restarted redis-server to free up disk space

## 2019-12-23 

* 22:25 paladox: /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/maintenance/sql.php /srv/mediawiki/w/extensions/AbuseFilter/db_patches/patch-drop_afl_log_id.sql
* 22:24 paladox: /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/maintenance/sql.php /srv/mediawiki/w/extensions/Flow/db_patches/patch-flow_tree_idx_fix_2.sql
* 21:54 paladox: /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/maintenance/sql.php /srv/mediawiki/w/maintenance/archives/patch-drop-user-fields.sql
* 21:54 paladox: /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/maintenance/sql.php /srv/mediawiki/w/maintenance/archives/patch-drop-archive-usertext_timestamp.sql
* 21:53 paladox: /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/maintenance/sql.php /srv/mediawiki/w/maintenance/archives/patch-drop-archive-ar_usertext_timestamp.sql
* 21:32 paladox: /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/maintenance/sql.php /srv/mediawiki/w/extensions/Flow/db_patches/patch-increase-varchar-ref_src_wiki.sql
* 18:55 Reception123: reception@mw2:/srv/mediawiki/w/maintenance$ sudo -u www-data php runJobs.php --wiki metawiki
* 18:04 paladox: MariaDB [hrznwiki]> INSERT INTO `content_models` (`model_id`,`model_name`) VALUES (4, 'Scribunto');
* 18:04 paladox: MariaDB [hrznwiki]> INSERT INTO `content_models` (`model_id`,`model_name`) VALUES (5, 'json');
* 18:03 paladox: MariaDB [hrznwiki]> INSERT INTO `content_models` (`model_id`,`model_name`) VALUES (2, 'css');
* 18:03 paladox: MariaDB [hrznwiki]> INSERT INTO `content_models` (`model_id`,`model_name`) VALUES (3, 'javascript');
* 18:01 paladox: MariaDB [hrznwiki]> INSERT INTO `content_models` (`model_id`,`model_name`) VALUES (1, 'wikitext');
* 14:53 paladox: starting upload for rhinodiarywiki - T5013 (mw1)
* 14:44 paladox: rebuild lc on mw* and lizard*
* 12:57 paladox: rebuild lc on mw* and lizard*
* 02:42 paladox: 127.0.0.1:6379> CONFIG SET timeout 0
* 01:18 paladox: $wm = new WikiManager( 'hrznwiki' ); $wm->delete( true ); (through eval)
* 01:10 paladox: recreating howtimhardingreplacedstevienicholsonwiki
* 01:10 paladox: MariaDB [mhglobal]> drop database howtimhardingreplacedstevienicholsonwiki;
* 01:09 paladox: MariaDB [mhglobal]> delete from cw_wikis where wiki_dbname = 'howtimhardingreplacedstevienicholsonwiki';
* 00:28 paladox: MariaDB [mhglobal]> delete from cw_wikis where wiki_dbname = 'hrznwiki';
* 00:26 paladox: recreating hrznwiki.

## 2019-12-22 

* 23:55 paladox: restart nginx & php7.3-fpm on mw* and lizardfs6
* 23:43 paladox: rebuilding lc on mw* and lizardfs6
* 23:42 paladox: varnish> ban req.http.Host == beidipedia.miraheze.org - cp4
* 23:40 paladox: repool mw3
* 23:34 paladox: depool mw3
* 23:25 paladox: sudo -u www-data php /srv/mediawiki/w/extensions/OATHAuth/maintenance/updateTOTPToMultipleKeys.php --wiki=metawiki
* 23:25 paladox: sudo -u www-data php /srv/mediawiki/w/extensions/OATHAuth/maintenance/updateDatabaseValueFormat.php --wiki=metawiki
* 23:24 paladox: sudo -u www-data php /srv/mediawiki/w/maintenance/sql.php --wiki=metawiki /srv/mediawiki/w/extensions/GlobalBlocking/sql/patch-global_block_whitelist-use-varbinary.sql
* 23:23 paladox: sudo -u www-data php /srv/mediawiki/w/maintenance/sql.php --wiki=metawiki /srv/mediawiki/w/extensions/GlobalBlocking/sql/patch-global_block_whitelist-reason-length.sql
* 23:23 paladox: sudo -u www-data php /srv/mediawiki/w/maintenance/sql.php --wiki=metawiki /srv/mediawiki/w/extensions/GlobalBlocking/sql/patch-globalblocks-reason-length.sql
* 23:21 paladox: root@mw3:/srv# ./foreachwikiindblist /srv/mediawiki/dblist/all.dblist
* 19:57 paladox: MariaDB [hispanowiki]> update actor set actor_user = NULL where actor_name = 'Flow talk page manager';
* 19:37 paladox: MariaDB [hispanowiki]> update actor set actor_user = 28 where actor_name = 'Flow talk page manager';
* 13:17 paladox: 127.0.0.1:6379> CONFIG SET timeout 5 - misc2
* 13:12 paladox: ulimit -Sn 100000
* 13:11 paladox: ulimit -n on misc2
* 12:57 paladox: depool, repool mw2, restart php7.3-fpm
* 12:54 paladox: depool, repool mw3, restart php7.3-fpm
* 12:43 paladox: repool lizardfs6
* 04:14 paladox: hacked mw* config (redis) and undone hack
* 04:01 paladox: depool lizardfs6
* 03:28 paladox: /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/maintenance/sql.php /home/paladox/aft.sql (test1)
* 02:58 Zppix: rebuild rc and initsitestats for uncyclomirrorwiki after import completion
* 02:26 paladox: /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/maintenance/sql.php /home/paladox/comments.sql (test1)

## 2019-12-21 

* 15:22 paladox: run lc on mw* and lizard*
* 02:30 paladox: repool lizardfs6
* 00:32 paladox: depool lizardfs6

## 2019-12-20 

* 21:45 paladox: ignore that, it appears to have version 1 installed, version 2 cannot seem to be found
* 21:39 paladox: install jemalloc on misc2

## 2019-12-19 

* 22:36 paladox: [22:35:01]  <+paladox>	!log reboot misc1
* 22:33 paladox: restarted networking on misc1
* 20:36 paladox: rebuild lc on mw2
* 19:40 paladox: rebuild lc on lizardfs6
* 19:39 Zppix: rebuild lc on mw123
* 19:13 Zppix: sudo -u www-data php sql.php --wiki=metawiki --query="update cw_requests set cw_status = 'approved' where cw_id = 10227;" on mw1

## 2019-12-18 

* 21:47 John: restart redis-server
* 17:01 paladox: [14:59:31]  <+paladox>	!log restart logbot on misc1
* 17:01 paladox: [14:58:18]  <+paladox>	!log apt-get upgrade - misc4
* 16:17 paladox: test
* 16:07 paladox: test
* 09:38 Southparkfan: install cron on mics2 to restart redis each 15 minutes
* 08:56 Southparkfan: disable puppet on misc2
* 08:26 Reception123: redis-server restarted
* 07:46 Reception123: restarted redis-server
* 02:07 paladox: apt-get upgrade - misc3
* 01:47 paladox: reboot misc3 - high load

## 2019-12-17 

* 21:50 paladox: reboot mw2
* 21:49 paladox: apt-get upgrade on mw*
* 21:30 paladox: restart php7.3-fpm and nginx on mw*
* 19:40 paladox: apt-get upgrade on lizardfs6
* 18:18 Zppix: run changePassword.php for a user that lost their login, temp password sent directly to user. (ON MW1)
* 16:54 paladox: hack redis config
* 16:23 SantaRhino: 16:19:23 <SantaRhino> !log update mailerlite donate link on 'test1' per metawiki
* 16:22 John: restarted logbot

## 2019-12-16 

* 17:17 paladox: restart nginx on mw* and cp[24]
* 16:51 paladox: restarted php7.3-fpm on mw3
* 16:48 paladox: restart redis-server

## 2019-12-14 

* 16:01 paladox: sudo -u www-data php purgeParserCache.php --wiki=unmusicfestwiki --age=1
* 13:44 paladox: remove rhinosf1 from status.miraheze.wiki
* 13:41 paladox: root@misc1:/home/paladox# deluser rhinosf1
* 13:40 Reception123: removed RhinosF1 from @GitHub project

## 2019-12-13 

* 20:38 Zppix: UPDATE cw_wikis SET wiki_settings = REPLACE(wiki_settings, '"wgServer":"https:\/\/wiki.8b8t.com "', null ) WHERE wiki_dbname = '8b8twiki'; using sql.php on mw1

## 2019-12-12 

* 19:06 Zppix: create database lizardfs6wiki on mw1 using sql.php to prevent potential problematic wiki creations
* 16:28 Zppix: restart import on mw1 for T4821

## 2019-12-11 

* 19:27 paladox: MatomoAnalyticsHooks::wikiCreation( 'xyssponwiki' ); (mw1)
* 19:24 paladox: create database wikiwiki; (db4)
* 19:23 paladox: sudo -u www-data php /srv/mediawiki/w/extensions/CreateWiki/maintenance/renameWiki.php --wiki=loginwiki --rename wikiwiki xyssponwiki paladox

## 2019-12-10 

* 22:41 paladox: root@mw2:/srv/mediawiki/w/maintenance# sudo -u www-data php updateArticleCount.php --wiki=ucroniaswiki --update
* 20:15 paladox: unhacked redis conifg file
* 20:07 paladox: hacked redis config on misc2 to use volatile-lfu
* 20:01 paladox: restart nginx and php7.3-fpm on mw*
* 19:51 paladox: re-delete adhdwiki
* 19:07 paladox: sudo -u www-data php /srv/mediawiki/w/extensions/OATH*/maint*/updateTOTPToMultipleKeys.php --wiki=metawiki (test1)
* 19:06 paladox: MariaDB [mhglobal]> ALTER TABLE /*_*/oathauth_users
* 19:00 paladox: turns out that, that file does not exist on mw1 but rather test1, so ran it on test1
* 18:59 paladox: sudo -u www-data php /srv/mediawiki/w/maintenance/sql.php --wiki=metawiki /srv/mediawiki/w/extensions/OATHAuth/sql/mysql/patch-add_generic_fields.sql (mw1)

## 2019-12-09 

* 18:45 paladox: depool and repool mw1
* 18:39 paladox: sudo -u www-data php purgeList.php --purge --all --wiki=paliwikiwiki (mw1) - T4877
* 18:32 paladox: sudo -u www-data php fixStuckGlobalRename.php --wiki=<wiki> IAmEiji "No Face" --logwiki=metawiki
* 18:27 paladox: undelete regoinaldifferencegameswikiwiki temporarily
* 18:21 paladox: depool and repool mw2
* 18:20 paladox: repool mw3

## 2019-12-07 

* 14:49 paladox: depool lizardfs6
* 11:48 Reception123: reception@mw3:/srv/mediawiki/w/maintenance$ sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki inforevivalwiki /home/reception/InfoRevival20191207.xml (screen)
* 11:35 RhinosF1: finished deploy mailerlite (set up important and all email groups, configure workflow)
* 11:18 RhinosF1: finished deploying mailerlite landing page 'test1'
* 11:07 RhinosF1: finished deploying mailerlite accounts
* 10:53 RhinosF1: adding owen, void and zppix as well (so making that everyone on staff and board@)
* 10:52 RhinosF1: starting deploy mailerlite - create operations accounts
* 10:16 RhinosF1: created site ‘test1’ on mailerlite

## 2019-12-06 

* 15:02 Zppix: rebuild LC on test1
* 14:58 paladox: rebooted db5 after networking stoped after running "sudo service networking restart"
* 14:50 Zppix: rebuild LC on mw2
* 14:47 Zppix: rebuild lc on mw[13]; MW2 puppet run failed, paladox is fixing, will run rebuild lc after
* 14:38 Zppix: force puppet runs on mw[123] to deploy [https://git.io/Jey8R](https://git.io/Jey8R)

## 2019-12-05 

* 22:14 Zppix: deleteBatch.php on mw1 for T4954
* 00:49 paladox: restart php7.3-fpm on mw[123] and lizardfs6
* 00:45 paladox: set 8.8.8.8 back in resolv.conf on mw[123], cp[24] and misc[1234]
* 00:20 paladox: root@mw2:/var/log/mediawiki/debuglogs# rm *

## 2019-12-04 

* 22:05 paladox: restart nginx and php7.3-fpm on mw[23]
* 20:48 paladox: depool mw1
* 20:37 paladox: MariaDB [simswiki]> delete from user_properties where up_user = 19;

## 2019-12-03 

* 23:19 Zppix: rebuildrc, initsitestats after import completed for wfhbwiki
* 22:27 paladox: revert back to  8.8.4.4 on mw*
* 22:25 paladox: that's in /etc/resolv.conf
* 22:25 paladox: switched mw* to use 1.1.1.1
* 21:58 paladox: rebuild lc on mw3
* 21:53 paladox: repool mw3
* 21:00 paladox: stopped script
* 20:59 Zppix: run rebuildrecentchanges.php and initsitestats.php on brokenwindowswiki on mw2 following completion of request import
* 20:56 paladox: run sudo -u www-data /usr/bin/nice -19 /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/maint*/runJobs.php on mw2
* 20:33 paladox: restarting networking on misc* (temporarily hack by crossing out 8.8.8.8 in /etc/resolv.conf)
* 20:31 paladox: restart nginx and php7.3-fpm on mw[12]
* 20:31 Zppix: begin import for brokenwindowswiki (T4946)
* 20:29 paladox: restarting networking on cp* and mw* (temporarily hack by crossing out 8.8.8.8 in /etc/resolv.conf)
* 20:19 paladox: restart networking service on misc4
* 19:35 paladox: [19:31:46]  <+paladox>	!log reboot mw3
* 18:56 paladox: UPDATE cw_wikis SET wiki_settings = REPLACE(wiki_settings, '"wgServer":"https:\/\/wiki.hackdown.org "', null ) WHERE wiki_dbname = 'hackdownwiki';
* 18:55 paladox: UPDATE cw_wikis SET wiki_settings = REPLACE(wiki_settings, '"wgServer":"https:\/\/wiki.hackdown.org"> "', null ) WHERE wiki_dbname = 'hackdownwiki';
* 18:50 paladox: UPDATE cw_wikis SET wiki_settings = REPLACE(wiki_settings, '"wgServer":"https:\/\/wiki.isina.ir "', null ) WHERE wiki_dbname = 'ivazeduwiki';
* 18:05 paladox: cancled run on mw3 and instead are running it on mw2
* 17:58 paladox: stop jobrunner/jobchron temporarily on mw3
* 17:57 paladox: run sudo -u www-data /usr/bin/nice -19 /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/maint*/runJobs.php on mw3

## 2019-12-02 

* 17:06 paladox: depool mw3
* 16:29 paladox: switch off TUN/TAP on mw3 (not needed now)
* 13:36 Zppix: Update for T4821: Restarting import after it was killed by MW1

## 2019-12-01 

* 23:27 paladox: restart php7.3-fpm and nginx on mw2
* 23:24 paladox: upgrade php on mw3
* 23:17 paladox: reboot mw3
* 22:36 Zppix: rebuild LC on test1
* 20:04 paladox: repool mw2
* 17:28 paladox: depool mw2
* 17:04 paladox: sudo -u www-data php createLocalAccount.php --wiki=loginwiki QuIRC (on mw2) and per RhinosF1 request
* 16:46 paladox: restart php-fpm on mw2
* 16:38 paladox: update php on misc4 including libidn2-0 libsodium23

## 2019-11-30 

* 23:26 paladox: repool mw2
* 21:03 paladox: depool mw2
* 16:38 Reception123: root@mw1:/srv/mediawiki/w/extensions/Cargo/maintenance# php cargoRecreateData.php --wiki rswiki --table Level
* 16:36 Zppix: run sudo -u www-data php cargoRecreateData.php --wiki rswiki --table Level on mw1 —Failed

## 2019-11-29 

* 22:02 paladox: repool mw2
* 22:01 paladox: upgrade php on mw2 to 7.3.12
* 22:01 paladox: depool mw2
* 21:02 paladox: root@misc2:/srv/matomo# sudo service php7.3-fpm restart
* 20:54 paladox: rebuild lc on lizardfs6
* 20:49 Zppix: rebuild LC on mw*

## 2019-11-27 

* 19:09 paladox: restart php7.3-fpm on mw3

## 2019-11-25 

* 01:27 paladox: delete and recreated puppetdb database on postgresql
* 01:27 paladox: ran my purge-binary script on db[45]

## 2019-11-24 

* 19:49 Zppix: rebuild LC on test1 for [https://git.io/JePU9](https://git.io/JePU9)
* 19:27 paladox: rebuild lc on mw* and lizardfs6
* 19:07 paladox: restart php7.3-fpm and nginx on mw1
* 18:35 Zppix: rebuild LC on mw*
* 18:28 paladox: rebuilding lc on lizardfs6
* 17:05 paladox: upgrade phabricator on misc4
* 17:03 paladox: reset paladox password on phabricator by running `bin/auth recover`
* 00:47 paladox: depool mw3

## 2019-11-23 

* 15:19 paladox: root@mw3:/home/paladox# apt-get install libidn2-0 libsodium23 puppet-agent
* 15:16 paladox: repool mw3

## 2019-11-22 

* 17:50 paladox: apt-get install puppet-agent puppetdb puppetdb-termini puppetserver - puppet1
* 17:47 paladox: apt-get upgrade on ns1
* 17:29 paladox: disable ipv6 on lizardfs6 temporarily
* 16:48 paladox: reboot misc3
* 16:15 Zppix: rebuild LC on test1
* 14:20 paladox: rm *.log* and *.log in /var/log/mediawiki on mw3
* 01:45 paladox: depool mw3 temporarily

## 2019-11-21 

* 23:41 paladox: repool mw2
* 17:21 paladox: depool mw2 temporarily
* 16:16 Southparkfan: on mw2 access files were owned by nginx:adm, changed to www-data:adm
* 10:59 paladox: reboot mw3
* 10:59 paladox: reboot mw3
* 01:07 paladox: building lc on mw2

## 2019-11-20 

* 23:37 paladox: repooled mw2
* 21:48 paladox: reimage mw2 as buster (10)
* 21:48 paladox: depool mw2
* 20:39 paladox: deleted all the logs apart from debuglogs in /var/log/mediawiki on mw2
* 16:09 paladox: restart nginx and php7.3 on mw2
* 02:31 paladox: regenerating backups
* 02:23 paladox: reboot bacula1 - kernel update
* 02:17 paladox: apt-get upgrade on bacula1
* 02:13 paladox: root@bacula1:/bacula/backup# rm *

## 2019-11-19 

* 19:03 paladox: restart php7.3-fpm on mw*
* 18:56 paladox: reboot mw1
* 18:04 paladox: repool mw2
* 18:03 paladox: remove haveged from mw2
* 18:03 paladox: depool mw2 temporarily
* 17:56 paladox: install haveged on mw2
* 17:01 paladox: upgrade some php packages on mw*
* 16:54 paladox: reboot mw2
* 16:34 John: restart ngninx and php7.3-fpm on mw2

## 2019-11-18 

* 23:19 paladox: restart php7.3-fpm on mw1
* 23:17 paladox: restart php7.3-fpm on mw2
* 17:42 paladox: also depooled then repool mw1
* 17:42 paladox: reboot mw1
* 13:45 paladox: depool, upgrade php7.2 to php7.3 and repool on mw[123] and lizardfs6
* 13:26 Zppix: Just an update restarting import for T4821

## 2019-11-17 

* 22:49 paladox: reboot test1
* 22:34 paladox: deleted lizardfs[45] from puppetdb
* 22:17 paladox: revoke lizardfs[45] puppet cert, remove from salt (deleting salt key) and delete instance
* 21:51 paladox: remove lizardfs* from lizardfs6
* 21:43 paladox: depool mw1, reboot and repool
* 21:41 paladox: depool mw2, reboot and repool
* 21:37 paladox: depool mw3, reboot and repool
* 21:21 paladox: root@lizardfs6:/mnt/mediawiki-static# rm -rf z*
* 21:06 paladox: root@lizardfs6:/mnt/mediawiki-static# rm -rf y*
* 17:05 paladox: root@lizardfs6:/mnt/mediawiki-static# rm -rf x*
* 17:01 paladox: root@lizardfs6:/mnt/mediawiki-static# rm -rf w*
* 16:58 paladox: restart lizardfs-master on lizardfs6
* 15:48 paladox: root@lizardfs6:/mnt/mediawiki-static# rm -rf v*
* 14:43 paladox: root@lizardfs6:/mnt/mediawiki-static# rm -rf u*
* 09:42 Reception123: add vnederbotwiki webhook
* 09:40 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki testwiki /home/reception/Wikipedia-20191116181322.xml on mw3
* 00:54 paladox: restart lizardfs-master on lizardfs6
* 00:43 paladox: root@lizardfs6:/mnt/mediawiki-static# rm -rf s*

## 2019-11-16 

* 19:43 paladox: root@lizardfs6:/mnt/mediawiki-static# rm -rf r*
* 19:41 paladox: root@lizardfs6:/mnt/mediawiki-static# rm r*
* 18:14 paladox: restart nginx on mw2
* 18:14 paladox: restart php7.2-fpm on mw2
* 18:09 paladox: root@lizardfs6:/mnt/mediawiki-static# rm -rf q*
* 18:04 Reception123: reception@mw3:/srv/mediawiki/w/maintenance$ sudo -u www-data php deleteBatch.php --wiki metawiki --r="Mass deletion of Twinkle pages, to be reimported" --u="Reception123" /home/reception/delete.txt
* 17:53 paladox: root@lizardfs6:/mnt/mediawiki-static# rm -rf p*
* 15:02 paladox: root@lizardfs6:/mnt/mediawiki-static# rm -rf o*
* 01:40 paladox: root@lizardfs6:/mnt/mediawiki-static# rm -rf m*
* 01:21 paladox:  dpkg -i libjs-moment-timezone_0.5.23+dfsg1-1_all.deb ([https://packages.debian.org/buster/all/libjs-moment-timezone/download](https://packages.debian.org/buster/all/libjs-moment-timezone/download)) required by the prometheus upgrade 2.3 -> 2.7 in stretch-backports, apt package not avilable.

## 2019-11-15 

* 22:29 paladox: restart lizardfs-chunkserver on lizardfs*
* 22:27 paladox: restart lizardfs-master on lizardfs6
* 21:58 paladox: root@lizardfs6:/mnt/mediawiki-static# rm -rf n*
* 20:01 RhinosF1: rhinos@mw1:~$ sudo -u www-data nice -5 php /srv/mediawiki/w/maintenance/refreshLinks.php 17600 --wiki=metawiki
* 19:17 RhinosF1: sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildall.php --wiki=metawiki (import and some stat issue with translations
* 19:16 RhinosF1: sudo -u www-data php /srv/mediawiki/w/maintenance/updateSpecialPages.php --override --wiki=metawiki
* 18:17 paladox: root@lizardfs6:/mnt/mediawiki-static# rm -rf l*
* 18:08 paladox: depool mw2 && reboot mw2 && repool
* 18:07 paladox: restart php7.2-fpm on mw2
* 17:16 paladox: root@lizardfs6:/mnt/mediawiki-static# rm -rf k*
* 15:58 paladox: root@lizardfs6:/mnt/mediawiki-static# rm -rf j*
* 15:23 paladox: root@lizardfs6:/mnt/mediawiki-static# rm -rf i*
* 14:11 paladox: root@lizardfs6:/mnt/mediawiki-static# rm -rf h*
* 13:10 paladox: root@lizardfs6:/mnt/mediawiki-static# rm -rf g*

## 2019-11-14 

* 22:56 paladox: root@lizardfs6:/mnt/mediawiki-static# rm -rf f*
* 22:55 paladox: root@lizardfs6:/mnt/mediawiki-static# rm -rf e*
* 18:56 paladox: root@lizardfs6:/mnt/mediawiki-static# rm -rf d*
* 17:25 paladox: root@lizardfs6:/mnt/mediawiki-static# rm -rf c*
* 17:23 paladox: root@lizardfs6:/mnt/mediawiki-static# rm -rf b*
* 17:17 paladox: root@lizardfs6:/mnt/mediawiki-static# rm -rf a*
* 13:19 paladox: restart lizardfs-master on lizardfs6
* 06:18 Reception123:  reception@mw2:/srv/mediawiki/w/maintenance$ sudo -u www-data php deleteBatch.php --wiki mashedpotaytoeswiki --r="MediaWiki exception, force delete" --u="Reception123" /home/reception/deletebatch.txt

## 2019-11-13 

* 22:38 paladox: grafana-cli plugins install grafana-piechart-panel - misc1
* 21:42 paladox: install make on misc3
* 21:40 paladox: install golang on misc3
* 17:10 paladox: restart php-fpm on lizardfs6
* 16:25 paladox: MatomoAnalyticsHooks::wikiCreation( 'windows95wikiwiki' ); on mw1

## 2019-11-12 

* 23:54 paladox: install fio on lizardfs6
* 19:29 Zppix: rebuild LC on mw[123] and test1
* 16:58 paladox: restart lizardfs-master on lizardfs6

## 2019-11-11 

* 17:50 Reception123: add valkyrienskieswiki discord webhook (re-add)
* 16:41 paladox: running lc on lizardfs6
* 16:39 RhinosF1: sudo -u www-data php /srv/mediawiki/w/maintenance/mergeMessageFileList.php --output /srv/mediawiki/config/ExtensionMessageFiles.php --wiki loginwiki and  sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildLocalisationCache.php --wiki loginwiki on mw[123] and test1
* 13:42 paladox: restart lizardfs-master on lizardfs6
* 08:25 Reception123: DROP DATABASE from this list: [https://phabricator.miraheze.org/P235](https://phabricator.miraheze.org/P235)\
* 08:09 Reception123: ran deletedwikis script on mw1
* 08:02 Reception123: bash ./deletedbackups.sh /home/reception/temp.dblist
* 07:51 Reception123: recreated mashedpotaytoeswiki (empty wiki; login issues)
* 07:24 Reception123: renamed customwiki to mashedpotaytoeswiki

## 2019-11-10 

* 23:07 paladox: userdel macfan on test1
* 22:58 paladox: reboot test1
* 20:09 paladox: restart lizardfs-master on lizardfs6

## 2019-11-08 

* 22:03 paladox: delete from mw_namespaces where ns_namespace_name = 'Forum_talk' and ns_dbname = 'csydeswiki'; on db4 - [https://meta.miraheze.org/w/index.php?title=Stewards%27_noticeboard&oldid=88031#Issue_with_the_redundant_Forum_talk_namespace_which_hasn.27t_been_deleted_properly](https://meta.miraheze.org/w/index.php?title=Stewards%27_noticeboard&oldid=88031#Issue_with_the_redundant_Forum_talk_namespace_which_hasn.27t_been_deleted_properly)

## 2019-11-07 

* 18:28 Zppix: rebuildlc on mw[123]
* 15:39 Zppix: ran CreateLocalAccount and fixStuckRename on mw1 for global rename for Gaddman

## 2019-11-06 

* 23:29 paladox: depool mw[123], rebuild lc and repool mw[123]
* 23:20 paladox: running lc on test1
* 23:11 Zppix:  sudo -u www-data php toggleExtension.php --disable  --wiki testwiki fontawesome
* 21:46 paladox: [21:41:55]  <+paladox>	!log restart lizardfs-master on lizardfs6
* 19:21 paladox: restarted nginx on mw[12]
* 19:17 paladox: restarted php7.2-fpm on mw3
* 19:16 paladox: restarted php7.2-fpm on mw2
* 19:11 paladox: restarted php7.2-fpm on mw3
* 18:24 paladox: restarted php7.2-fpm on mw3
* 18:23 paladox: restarted php7.2-fpm on mw2
* 01:20 paladox: repool mw2
* 00:32 paladox: depool mw2
* 00:22 paladox: restart php7.2-fpm on mw[23]

## 2019-11-05 

* 21:51 paladox: depool mw1
* 18:13 John: changed status for 2 wiki requests to approved from inreview
* 16:21 RhinosF1: sudo -u www-data php /srv/mediawiki/w/extensions/CentralAuth/maintenance/createLocalAccount.php --wiki=garbageandcleanredditwiki GasMask0217 (was fixing broke wiki requests 9783 and 9773)
* 16:18 RhinosF1: sudo -u www-data php /srv/mediawiki/w/extensions/CreateWiki/maintenance/populateMainPage.php --wiki=garbageandcleanredditwiki
* 16:16 RhinosF1: sudo -u www-data php /srv/mediawiki/w/extensions/CreateWiki/maintenance/populateMainPage.php --wiki=kangarootestingwiki

## 2019-11-04 

* 18:27 paladox: reboot test1
* 17:03 paladox: restart php-fpm on mw[123]
* 16:27 paladox: restart php-fpm on mw3
* 16:17 paladox: restart php-fpm on mw[123]
* 16:06 paladox: restart php-fpm on mw3
* 16:04 paladox: restart php-fpm on mw2
* 16:00 paladox: restart php-fpm on mw1
* 15:24 paladox: [15:19:14]  <+paladox>	!log restart nginx on mw[123]
* 15:23 paladox: [15:18:03]  <+paladox>	!log restart php-fpm on mw[123]
* 15:20 paladox: restart nginx on mw[123]
* 15:20 paladox: restart php-fpm on mw[123]
* 15:19 paladox: restart php-fpm on mw[123]

## 2019-11-03 

* 23:32 paladox: restart php-fpm on mw1, was slow
* 23:29 paladox: root@db5:/home/paladox# ./purge-binary.sh
* 23:29 paladox: root@db4:/home/paladox# ./purge-binary.sh
* 22:28 Zppix: zppix@mw1:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki uncyclomirrorwiki /home/zppix/uncyclopedia-full-2019-05-15.xml
* 19:01 Zppix:  UPDATE actor SET actor_name = 'Flow talk page manager2' WHERE actor_id = '485' for ucroniaswiki

## 2019-11-02 

* 20:03 paladox: /usr/bin/nice -19 /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/extensions/ManageWiki/maintenance/toggleExtension.php darkmode
* 20:00 paladox: sudo -u www-data php toggleExtension.php --wiki=metawiki darkmode
* 18:09 paladox: update GeoLite2-Country.mmdb on ns1 and misc1 (and restart gdnsd)
* 17:26 paladox: restart lizardfs-chunkserver on lizardfs6
* 16:24 paladox: restart lizardfs-chunkserver on lizardfs6
* 15:02 paladox: restart lizardfs-chunkserver on lizardfs6
* 14:56 paladox: restart lizardfs-chunkserver on lizardfs6
* 14:51 paladox: [14:44:26]  <+paladox>	!log restart lizardfs-chunkserver on lizardfs6
* 04:24 paladox: scp'ing loginwiki to lizardfs6
* 02:05 paladox: restart lizardfs-chunkserver on lizardfs6
* 01:46 paladox: scp'ing metawiki, test1wiki and mhglobal to lizardfs6

## 2019-11-01 

* 23:05 Zppix: run /usr/bin/nice -10 sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/extensions/ManageWiki/maintenance/toggleExtension.php DarkMode on mw1
* 16:34 RhinosF1: sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildLocalisationCache.php --wiki loginwiki (both this and above on mw[123]
* 16:33 RhinosF1: sudo -u www-data php /srv/mediawiki/w/maintenance/mergeMessageFileList.php --output /srv/mediawiki/config/ExtensionMessageFiles.php --wiki loginwiki
* 15:40 RhinosF1: on test1 that is
* 15:40 RhinosF1: sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildLocalisationCache.php --wiki loginwiki
* 15:40 RhinosF1: sudo -u www-data php /srv/mediawiki/w/maintenance/mergeMessageFileList.php --output /srv/mediawiki/config/ExtensionMessageFiles.php --wiki loginwiki on test1
* 02:07 paladox: [01:59:01]  <+paladox>	!log deploy updated wildcard.miraheze.org to mw[123] and puppet1
* 02:02 paladox: deploy updated wildcard.miraheze.org to cp[234]
* 02:01 paladox: deploy updated wildcard.miraheze.org to misc[1234]
* 01:38 paladox: restart mysql on db[45] to pick up new cert, outage will happen
* 01:37 paladox: deploy updated wildcard.miraheze.org to db[45]
* 01:34 paladox: deploying updated wildcard.miraheze.org to test1
* 01:32 paladox: update wildcard.miraheze.org private cert

## 2019-10-31 

* 20:43 paladox: rebuilding misc3 (restbase will fail for a bit) also moving it to the 1gb plan
* 09:42 Reception123: removed wgServer setting on om3gawiki via DB (domain no longer pointing)
* 02:28 paladox: purged mysql binary on db4

## 2019-10-30 

* 17:12 paladox: restart php7.2-fpm on mw[123]
* 17:10 paladox: restart lizardfs-master on lizardfs6
* 15:45 paladox: switch swap off on lizardfs6
* 15:34 paladox: reload lizardfs-chunkserver on lizardfs[45]
* 15:17 paladox: restart lizardfs-chunkserver & change master
* 11:06 Reception123: nice 10 for all of the above
* 11:06 Reception123: reception@mw1:~$ sudo php /srv/mediawiki/w/maintenance/dumpBackup.php --wiki nonciclopediawiki --full --output gzip:/home/reception/nonciclopediawiki30102019.xml (part of wikibackups)
* 11:04 Reception123: reception@mw3:~$ sudo php /srv/mediawiki/w/maintenance/dumpBackup.php --wiki nonsensopediawiki --full --output gzip:/home/reception/nonsensopediawiki30102019.xml (part of wikibackups)
* 11:04 Reception123: reception@mw2:~$ sudo php /srv/mediawiki/w/maintenance/dumpBackup.php --wiki poserdazfreebieswiki --full --output gzip:/home/reception/poserdazfreebieswiki30102019.xml (part of wikibackups)
* 11:03 Reception123: reception@mw1:~$ sudo php /srv/mediawiki/w/maintenance/dumpBackup.php --wiki allthetropeswiki --full --output gzip:/home/reception/allthetropes30102019.xml (part of wikibackups)
* 04:28 RhinosF1: deleted account ‘macfan’ on status.miraheze.wiki

## 2019-10-29 

* 20:47 paladox: depool and repool mw[123]
* 19:57 paladox: restarting php7.2-fpm accross mw[123]
* 14:37 paladox: install iotop on mw1
* 14:32 paladox: depool and repool mw[123]
* 02:00 paladox: depooled and repooled mw1

## 2019-10-28 

* 21:05 paladox: depool and repool mw[123]
* 21:00 paladox: depool and repool mw2
* 19:25 paladox: depool and repool mw3
* 19:22 paladox: depool and repool mw2
* 19:21 paladox: depool and repool mw1
* 15:36 paladox: update cw_wikis set wiki_deleted = 1 where wiki_dbname = 'mw1wiki'; - db4
* 15:30 paladox: $wm = new WikiManager( 'mw1wiki' ); $wm->delete( true ); on mw1

## 2019-10-27 

* 23:57 paladox: depool and repool mw1
* 20:56 paladox: depool and repool mw[123]
* 20:38 paladox: depool and repool mw1
* 19:16 paladox: upgraded mariadb to 10.2 on misc1
* 16:28 paladox: running ./wikibackups.sh /home/reception/allpublic.dblist in Reception123 homedir on mw1
* 15:25 paladox: upgrade icinga2 on misc1
* 15:24 paladox: upgrade libcupsimage2 libglib2.0-0 libglib2.0-data libicu57 libidn2-0 libldap-2.4-2 libcups2 on misc1
* 15:24 paladox: upgrade libldap-common libsodium23 libxml2 libxslt1.1 php7.2 php7.3 autopoint base-files debian-archive-keyring gettext gettext-base on misc1
* 15:23 paladox: upgrade systemd-sysv tzdata udev unzip libssl-dev libssl1.1 libsystemd0 on misc1
* 15:20 paladox: upgrade puppet-agent on misc4
* 15:20 paladox: upgrade puppet-agent on misc[123]
* 15:19 paladox: upgrade nodejs on misc4
* 15:17 paladox: upgrade php and openssl on misc[124]
* 15:09 paladox: upgrade puppet-agent on test1
* 15:06 paladox: upgrade php, nodejs and openssl on test1
* 15:05 paladox: repool mw1
* 15:05 paladox: also upgraded php7.3 on mw[123]
* 15:04 paladox: upgraded nodejs on mw[123]
* 15:04 paladox: upgrade openssl on mw1
* 15:04 paladox: depool mw1
* 15:04 paladox: repool mw3
* 15:03 paladox: upgrade php and openssl on mw3
* 15:02 paladox: depool mw3
* 15:02 paladox: repool mw2
* 15:02 paladox: upgrade openssl on mw2
* 15:00 paladox: upgrade php on mw2
* 15:00 paladox: depool mw2
* 14:35 paladox: depool and repool mw3
* 14:32 paladox: depool and repool mw2
* 14:21 paladox: depool and repool mw1

## 2019-10-26 

* 14:51 paladox: rebooting mw1
* 14:32 paladox: restart lizardfs-chunkserver on lizardfs[45
* 14:23 paladox: restart lizardfs-master on misc3
* 07:27 Reception123: tar zcvf speleowiki26102019.tar.gz /mnt/mediawiki-static/speleowiki on mw2
* 07:04 Reception123: running wikibackups (bash ./wikibackups.sh /home/reception/allpublic.dblist /srv/mediawiki/w/maintenance/dumpBackup.php)
* 01:05 paladox: repool mw3
* 01:04 paladox: depool mw3
* 01:00 paladox: repool mw3
* 00:59 paladox: depool mw3

## 2019-10-25 

* 17:28 Reception123: reception@mw2:/srv/mediawiki/w/maintenance$  sudo -u www-data php /srv/mediawiki/w/maintenance/dumpBackup.php --wiki speleowiki --full --output gzip:/home/reception/speleo25102019.xml
* 16:21 paladox: upgrade puppetdb to 6.7.2 on puppet1

## 2019-10-24 

* 00:43 Southparkfan: restarted dovecot

## 2019-10-23 

* 19:26 paladox: upgrade mariadb on db[45]
* 19:24 paladox: updating wildcard.miraheze.org on db[45]
* 19:23 paladox: update wildcard.miraheze.org in the private puppet repo
* 19:13 paladox: disable puppet everywhere
* 15:52 paladox: remove global file locking from all mounts on mw[123] and test1
* 14:34 paladox: revoke lizardfs6 puppet cert
* 13:54 paladox: restart lizardfs-master on misc3 for configuation change
* 13:35 paladox: shutdown -r on lizardfs6
* 00:52 paladox: [01:47:40]  <+paladox>	!log restart lizardfs-master
* 00:26 paladox: restart lizardfs-master
* 00:26 paladox: [01:14:49]  <+paladox>	!log restart lizardfs-master on misc3 - config change

## 2019-10-22 

* 16:39 paladox: hacked fstab on mw[123]
* 16:19 paladox: install iotop on lizardfs4
* 16:11 paladox: repool mw3
* 16:11 paladox: depool mw3
* 16:11 paladox: repool mw2
* 16:10 paladox: depool mw2
* 16:10 paladox: repool mw1
* 16:10 paladox: depool mw1
* 15:39 John: added discord webhook for nbdbwiki
* 15:37 John: added discord webhok for cwarswiki

## 2019-10-21 

* 07:55 Reception123: mount -a on mw*
* 07:45 Reception123: unmounted static on mw*
* 07:28 paladox: restart lizardfs-chunkserver on lizardfs[45]

## 2019-10-20 

* 16:20 paladox: restart lizardfs-chunkserver on lizardfs[45]
* 14:29 paladox: run lc on mw[123], test1
* 14:01 paladox: running lc on mw[123]
* 13:28 paladox: root@misc4:/srv/parsoid# sudo -u root npm install service-runner@2.6.19
* 13:18 paladox: root@misc4:/srv/parsoid# npm install worker-farm@1.7.0
* 13:11 paladox: upgrade phabricator on misc4
* 13:07 paladox: root@misc4:/srv/parsoid# npm install node-worker-farm@1.5.4
* 12:59 paladox: reboot misc4

## 2019-10-19 

* 16:28 paladox: upgrade puppet-agent on mw3
* 16:22 paladox: repool mw2
* 16:09 paladox: reboot mw2
* 16:09 paladox: depool mw2
* 16:06 paladox: upgrade puppet-agent on mw2
* 14:49 paladox: upgrade puppet-agent on db[45] misc[13]
* 14:36 paladox: upgrade puppet-agent puppetdb puppetdb-termini puppetserver on puppet1
* 14:35 paladox: upgrade openssl on misc1
* 14:32 paladox: upgrade php on misc1
* 14:12 paladox: restarted nginx on mw[123]
* 13:48 paladox: upgrade grafana to 6.4.3
* 13:48 paladox: upgrade icingaweb2 to 2.7.3 on misc1
* 13:47 paladox: upgrade icinga2 to 2.11.1 on misc1
* 09:13 Reception123: reception@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php importDump.php --wiki degreesoflewditywiki /home/reception/degreesoflewdity_pages_full.xml

## 2019-10-18 

* 18:11 RhinosF1: created blank databases for all commissioned servers using; sql.php --wiki=metawiki CREATE database [servername]wiki;
* 18:10 John: destroyed [https://phabricator.miraheze.org/P232](https://phabricator.miraheze.org/P232)
* 17:07 Zppix: deleteBatch --wiki caeruleawik ~/home/zppix/delete.txt and then populateMainPage.php --wiki caeruleawiki
* 14:50 paladox: reboot misc4 as it oom

## 2019-10-17 

* 23:58 paladox: depool and repool mw[123]
* 22:35 John:  UPDATE actor SET actor_name = 'Flow talk page manager2' WHERE actor_id = 1471; on oecumenewiki
* 21:57 Zppix: rebuild rc on test1wiki on test1
* 21:29 Zppix: rebuild lc and mergemessagefiles on test1
* 18:00 Zppix: mergemessagefiles and rebuild lc on mw[123]
* 17:54 Zppix: rebuildlc and mergemessagefiles on test1
* 17:35 Zppix: rebuild lc and mergemessagefiles on test1
* 17:34 paladox: reboot misc4
* 16:30 Reception123: reception@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php importDump.php --wiki darkfallnewdawnwiki /home/reception/delbackups/darkfallnewdawnwiki.xml
* 15:45 Reception123: MariaDB [(none)]> DROP DATABASE caeruleawiki; on db4
* 15:45 Reception123: deleted caeruleawiki
* 15:29 Reception123: reception@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php importDump.php --wiki agoldenbraidwiki /home/reception/delbackups/agoldenbraidwiki.xml
* 10:50 Southparkfan: ran importDump.php, rebuildrecentchanges.php and initSiteStats.php for T4776

## 2019-10-16 

* 22:28 paladox: restart lizardfs-chunkserver on lizardfs6
* 22:27 paladox: restart lizardfs-chunkserver on lizardfs[45]
* 20:46 Zppix: re-enabled puppet on test1
* 15:57 paladox: restart nginx on mw2
* 15:57 paladox: restart nginx on mw1
* 15:55 paladox: rolling restart of php-fpm on mw[123]
* 15:04 paladox: running  sudo chown -R www-data:www-data /mnt/mediawiki-static on mw1
* 14:57 paladox: depool and repool mw3
* 14:55 paladox: depool and repool mw2
* 14:55 paladox: depool and repool mw1
* 01:15 paladox: reboot misc4 - OOM
* 00:43 paladox: restart php-fpm on mw2
* 00:43 paladox: restart php-fpm on mw1

## 2019-10-15 

* 23:31 Zppix: same on mw[23]
* 23:28 Zppix: sudo -u www-data  php /srv/mediawiki/w/maintenance/rebuildLocalisationCache.php --wiki loginwiki and sudo -u www-data  php /srv/mediawiki/w/maintenance/mergeMessageFileList.php --output /srv/mediawiki/config/ExtensionMessageFiles.php --wiki loginwiki on mw1
* 22:40 RhinosF1: with --wiki test1wiki
* 22:37 RhinosF1: rebuildlc on test1
* 22:27 Zppix: rebuildlc on test1
* 22:24 RhinosF1: rhinos@test1:/srv/mediawiki/config$ sudo -u www-data git pull
* 22:21 RhinosF1: rhinos@test1:/srv/mediawiki/w$ sudo -u www-data git pull
* 22:13 RhinosF1: rhinos@test1:/srv/mediawiki/w/extensions$ sudo -u www-data git reset --hard
* 22:11 RhinosF1: rhinos@test1:/srv/mediawiki/config$ sudo -u www-data rm -rf /srv/mediawiki/w/extensions/LastModified
* 22:10 RhinosF1: rhinos@test1:/srv/mediawiki/config$ sudo -u www-data git reset --hard
* 22:06 RhinosF1: rhinos@test1:/srv/mediawiki/config$ sudo -u www-data rm -rf /srv/mediawiki/w/extensions/lastmodified
* 21:48 Zppix: sudo -u www-data git pull in /srv/mediawiki/config and /w/ on test1
* 18:44 Zppix: zppix@test1:/$ sudo -u www-data php  /srv/mediawiki/w/maintenance/initSiteStats.php --update --wiki test1wiki
* 18:41 paladox: upgrade sudo on test1
* 18:41 paladox: upgrade sudo on bacula1
* 18:41 paladox: upgrade sudo on lizardfs[45]
* 18:38 paladox: upgrade sudo on cp[234]
* 18:36 paladox: upgrade sudo on misc[1234]
* 18:35 paladox: upgrade sudo on db[45]
* 18:34 paladox: upgrade sudo on mw[123]
* 17:30 paladox: run MatomoAnalyticsHooks::wikiCreation( 'mlgyaanipediawiki' ); in eval.php on mw1

## 2019-10-14 

* 23:55 paladox: rolling restart of php-fpm on mw[123]
* 21:58 RhinosF1: mergemessagelists, i18n rebuilt and git pull config on test1
* 21:55 paladox: rolling restart of php-fpm on mw[123]
* 21:33 RhinosF1: 22:15 RhinosF1: sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildLocalisationCache.php --wiki loginwiki
* 21:26 RhinosF1: sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildLocalisationCache.php --wiki loginwiki (AFTER mergemesssagelists on test1)
* 21:23 RhinosF1: git-pull config on test1
* 21:14 paladox: reboot misc4
* 20:50 RhinosF1: last two on all mw* servers and git pulling config on mw3 due to puppet killing itself
* 20:45 RhinosF1: sudo -u www-data php /srv/mediawiki/w/maintenance/mergeMessageFileList.php --output /srv/mediawiki/config/ExtensionMessageFiles.php --wiki loginwiki (test1)
* 20:44 RhinosF1: rhinos@test1:/srv/mediawiki/config$ sudo -u www-data git pull
* 20:34 RhinosF1: rhinos@test1:/srv/mediawiki/config$ sudo -u www-data git pull
* 15:29 RhinosF1: rhinos@mw1:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/initSiteStats.php --update --wiki wiesepediawiki (post import clean up)
* 15:10 RhinosF1: rhinos@mw1:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildall.php --wiki wiesepediawiki (to fix recent changes after import)
* 15:07 RhinosF1: restarting that import to test paladox fix
* 14:50 RhinosF1: rhinos@mw1:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php /home/rhinos/Wiesepedia-Respaldo.xml --wiki wiesepediawiki (x2 erroring with Warning: in_array() expects parameter 2 to be array, string given in /srv/mediawiki/config/LocalWiki.php on line 298 but proceeding)
* 01:50 paladox: rolling restart of php-fpm on mw[123]
* 00:08 Southparkfan: restarted php-fpm across all mw hosts

## 2019-10-13 

* 23:57 Southparkfan: dropped profiling table from test1wiki
* 23:33 paladox: /mnt/mediawiki-static# echo "DirectIO=false" > .lizardfs_tweaks - mw[123]
* 23:07 Southparkfan: testing profiling (un-puppetized) on test1
* 22:03 Southparkfan: created profiling table on db4 for test1wiki
* 12:30 paladox: mount -a on mw[123]
* 12:29 paladox: umount /mnt/mediawiki-static on mw[123] (it disconnected from the master)

## 2019-10-12 

* 22:34 paladox: repool mw1
* 22:32 paladox: depool mw1 and reboot - high cpu and load
* 21:56 paladox: echo "DirectIO=true" > .lizardfs_tweaks on mw[123]
* 17:40 paladox: [18:12:26]  <+paladox>	!log resizing misc3 to 3gb SKVM (bst time)
* 17:13 paladox: stopping lizardfs-master on misc3 short downtime
* 02:07 paladox: keeping puppet disabled on mw[123] overnight. php-fpm config hacked to experiment with different settings.

## 2019-10-11 

* 22:30 paladox: hacked php-fpm on mw[23]
* 22:15 paladox: restarting lizardfs-master
* 21:47 paladox: lower childs to 22 on mw1
* 21:43 paladox: hacked php fpm on mw1 to have 32 childs (experimenting)
* 20:35 PuppyKun: ndkilla@misc1 sudo passwd ndkilla
* 13:37 paladox: re-enabled puppet on misc3
* 13:02 paladox: disabled puppet on misc3 and experimenting with vm.swappiness = 0
* 12:58 paladox: reboot test1
* 12:58 paladox: reboot mw1
* 12:54 paladox: reboot mw2
* 12:48 paladox: reboot mw3

## 2019-10-10 

* 23:22 paladox: regenerate backups on bacula1
* 23:22 paladox: remove all backups
* 23:09 paladox: remove STATIC incomplete backups from bacula1
* 22:15 RhinosF1: sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildLocalisationCache.php --wiki loginwiki
* 22:15 RhinosF1: sudo -u www-data php /srv/mediawiki/w/maintenance/mergeMessageFileList.php --output /srv/mediawiki/config/ExtensionMessageFiles.php --wiki loginwiki
* 22:08 RhinosF1: running [https://meta.miraheze.org/wiki/Tech:Updating_an_extension](https://meta.miraheze.org/wiki/Tech:Updating_an_extension) on [test/mw]*
* 21:20 RhinosF1: rhinos@mw1:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/cleanupEmptyCategories.php --mode=remove --force  --wiki=ildrilwiki
* 21:18 RhinosF1: running recountCat for --mode=[files/subcats] per script output
* 21:17 RhinosF1: rhinos@mw1:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/cleanupEmptyCategories.php --mode=remove --wiki=ildrilwiki x2
* 21:16 RhinosF1: rhinos@mw1:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/recountCategories.php --mode=pages --wiki=ildrilwiki
* 21:15 RhinosF1: running again, no impact seen
* 21:13 RhinosF1: rhinos@mw1:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/populateCategory.php --force --wiki=ildrilwiki
* 21:07 RhinosF1: that was on rhinos@mw1.miraheze.org
* 21:06 RhinosF1: sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildall.php --wiki=ildrilwiki
* 08:07 paladox: reboot mw1 (high cpu)
* 03:09 PuppyKun: (50 minutes late) manually ran puppet on all servers for key update

## 2019-10-09 

* 23:44 paladox: MatomoAnalyticsHooks::wikiCreation( 'bestmusicandsongswiki' ); in eval.php
* 23:03 paladox: repool mw3
* 23:00 paladox: depool mw3
* 22:59 paladox: repool mw2
* 22:57 paladox: depool mw2
* 22:55 paladox: repool mw1
* 22:49 paladox: depool mw1
* 20:53 paladox: reload lizardfs-master
* 20:50 paladox: hack puppet on puppet1
* 19:03 paladox: hack fstab on mw[23]

## 2019-10-08 

* 22:14 paladox: removed hacks from mw*, puppet ran.
* 22:07 paladox: depool and repool mw2
* 21:35 paladox: apply fstab hack to mw1 (depool and repool)
* 21:24 paladox: sudo service prometheus-node-exporter start - mw3
* 21:16 paladox: sudo service prometheus-node-exporter stop - mw3
* 19:36 paladox: restarted nginx on mw3
* 19:13 paladox: depool mw3 again
* 19:03 paladox: repool mw3
* 19:03 paladox: hack fstab on mw3 to test some configuation changes
* 18:56 paladox: repool mw3
* 18:56 paladox: kill -9 111 - mw3
* 18:53 paladox: depool mw3

## 2019-10-06 

* 19:49 paladox: stop electron on misc3
* 13:51 paladox: restarting php-fpm on mw3
* 01:19 paladox: restart lizardfs-master

## 2019-10-05 

* 23:04 paladox: depool and repool mw[23]
* 22:52 paladox: depool mw1 and repool
* 20:28 RhinosF1: sudo -u www-data php /srv/mediawiki/w/maintenance/resetUserEmail.php ZppixBot tools.zppixbot@tools.wmflabs.org --wiki=loginwiki (requested, operator known on irc)

## 2019-10-04 

* 22:14 RhinosF1: (belated - 23:03) - restarted last job (again on mw1) due to redis error
* 21:18 RhinosF1: sudo -u www-data php /srv/mediawiki/w/maintenance/deleteBatch.php --u="RhinosF1" --r="Copyright Violation per [Miraheze Commons:Files uploaded by Penarc1](https://meta.miraheze.org/wiki/Miraheze_Commons:Files_uploaded_by_Penarc1)"  /home/rhinos/list.txt --wiki=commonswiki
* 20:58 John: fixed exception forumwiki

## 2019-10-03 

* 01:14 paladox: restart lizardfs-master

## 2019-10-02 

* 14:01 paladox: depool and repool mw[123]
* 13:48 paladox: restart icinga2 on misc1
* 13:47 paladox: restart ircecho on misc1
* 13:28 paladox: reboot test1
* 00:07 paladox: root@mw1:/srv/mediawiki/w/maintenance# sudo -u www-data php rebuildrecentchanges.php --wiki=incrediblewikisanduserswiki

## 2019-10-01 

* 23:13 paladox: update flow_revision set rev_edit_user_wiki = 'incrediblewikisanduserswiki' where rev_edit_user_wiki = 'flawlessfandomuserswiki';
* 23:12 paladox: update flow_revision set rev_mod_user_wiki = 'incrediblewikisanduserswiki' where rev_mod_user_wiki = 'flawlessfandomuserswiki';
* 22:43 paladox: update flow_ext_ref set ref_src_wiki = *where ref_src_wiki = 'flawlessfandomus';
* 22:42 paladox: update flow_tree_revision set tree_orig_user_wiki = 'incrediblewikisanduserswiki' where tree_orig_user_wiki = 'flawlessfandomuserswiki';
* 22:40 paladox: update flow_workflow set workflow_wiki = 'incrediblewikisanduserswiki' where workflow_wiki = 'flawlessfandomuserswiki';
* 22:39 paladox: update flow_wiki_ref set ref_src_wiki =* where ref_src_wiki = 'flawlessfandomus';
* 22:36 paladox: update flow_revision set rev_user_wiki = 'incrediblewikisanduserswiki' where rev_user_wiki = 'flawlessfandomuserswiki';
* 19:26 paladox: root@mw2:/home/paladox# sudo -u www-data php /srv/mediawiki/w/extensions/CreateWiki/maintenance/renameWiki.php --wiki=loginwiki --rename flawlessfandomuserswiki incrediblewikisanduserswiki paladox - T4755
* 16:44 paladox: restart lizardfs-chunkserver on lizardfs[45]

## 2019-09-30 

* 22:08 paladox: restarted php-fpm on mw1
* 17:51 paladox: [18:46:22]  <+paladox>	!log rebooting mw3
* 14:46 paladox: reboot mw3
* 14:38 paladox: reboot mw1
* 12:23 paladox: depool and repool mw[123]

## 2019-09-29 

* 23:07 paladox: depool and repool mw[23]
* 23:01 paladox: sudo usermod -a -G ssl-cert www-data - mw2
* 23:01 paladox: sudo usermod -a -G ssl-cert www-data - mw3
* 19:55 paladox: depool and repool mw1
* 15:27 paladox: rm /mnt/mediawiki-static/allthetropeswiki/lockdir/*.lock
* 15:27 paladox: rm /mnt/mediawiki-static/metawiki/lockdir/obm4i1gmrsn12ek8soh4eorwgw4t4kh.lock
* 13:15 paladox: restart lizardfs-chunkserver on lizardfs[45]
* 08:42 Reception123: reception@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php rebuildall.php --wiki kkutuwiki

## 2019-09-28 

* 22:05 paladox: depool mw[123] and repool
* 21:44 paladox: sudo -u www-data php fixStuckGlobalRename.php --wiki=reverseatrociousdeviantswiki --logwiki=metawiki PapercutsExist PaperClip
* 16:37 RhinosF1: sudo -u www-data php /srv/mediawiki/w/extensions/CentralAuth/maintenance/fixStuckGlobalRename.php --wiki=reverseafwuwiki --logwiki=metawiki 'PapercutsExist' 'PaperClip' (attemtpting to fix rename but redis has crashed so failed)
* 16:12 Reception123: reception@mw1:~$ sudo -u www-data php /srv/mediawiki/w/extensions/CentralAuth/maintenance/fixStuckGlobalRename.php --wiki=horribleobjectshowswiki --logwiki=metawiki 'PapercutsExist' 'PaperClip'
* 16:06 Reception123: reception@mw1:~$ sudo -u www-data php /srv/mediawiki/w/extensions/CentralAuth/maintenance/fixStuckGlobalRename.php --wiki=gamelabwiki --logwiki=metawiki 'PapercutsExist' 'PaperClip'
* 16:06 Reception123: MariaDB [mhglobal]> DELETE FROM renameuser_status WHERE ru_wiki = 'gamebreakingwiki';
* 15:57 Reception123: reception@mw1:~$ sudo -u www-data php /srv/mediawiki/w/extensions/CentralAuth/maintenance/fixStuckGlobalRename.php --wiki=bakapediawiki --logwiki=metawiki 'PapercutsExist' 'PaperClip'
* 15:55 Reception123: sudo -u www-data php /srv/mediawiki/w/extensions/CentralAuth/maintenance/fixStuckGlobalRename.php --wiki=awiki --logwiki=metawiki 'PapercutsExist' 'PaperClip' on mw1
* 15:54 Reception123: MariaDB [mhglobal]> DELETE FROM renameuser_status WHERE ru_wiki = 'awfultvshowswiki';
* 14:52 RhinosF1: rhinos@mw1:~$ sudo -u www-data php /srv/mediawiki/w/extensions/CentralAuth/maintenance/fixStuckGlobalRename.php --wiki=amazingreceptionwikiswiki --logwiki=metawiki 'PapercutsExist' 'PaperClip'

## 2019-09-27 

* 23:41 paladox: delete glusterfs[12]
* 23:05 paladox: depool and repool mw[123]
* 21:30 RhinosF1: rhinos@mw1:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php /home/rhinos/infoboxes/*.xml --wiki wikimdwiki
* 12:57 paladox: apt-get upgrade - puppet1
* 09:38 paladox: reboot misc4 - high cpu
* 09:33 paladox: apt-get upgrade - misc4
* 09:28 paladox: apt-get upgrade - misc2
* 09:13 paladox: repool mw3
* 09:11 paladox: depool mw3
* 09:11 paladox: repool mw2
* 09:07 paladox: depool mw2
* 09:07 paladox: repool mw1
* 09:05 paladox: apt-get upgrade - mw1
* 09:04 paladox: depool mw1

## 2019-09-26 

* 23:02 paladox: running lc on mw*
* 19:55 paladox: apt-get upgrade - lizardfs[45]
* 19:54 paladox: apt-get upgrade - misc3
* 16:07 paladox: reboot glusterfs[12]

## 2019-09-24 

* 22:17 RhinosF1: regenerate last ssl cert due dns change
* 22:06 RhinosF1: rhinos@mw1:~$ sudo /root/ssl-certificate -d pastport.org -g -o

## 2019-09-22 

* 21:43 paladox: depool and repool mw[123] (upgrading gluster client to 6.5)
* 21:27 paladox: upgrade glusterfs on glusterfs[12] to 6.5
* 21:19 paladox: depool mw3 and repool (disabling mediawiki-static-new mount to prevent wikis going down)
* 21:18 paladox: depool mw2 and repool (disabling mediawiki-static-new mount to prevent wikis going down)
* 21:17 paladox: depool mw1 and repool (disabling mediawiki-static-new mount to prevent wikis going down)
* 12:45 paladox: runninc lc on mw*

## 2019-09-21 

* 20:55 paladox: reboot glusterfs[12]
* 19:46 paladox: depool mw[123] in order and repool
* 18:21 RhinosF1: removed PII for a user (ToU enforcement)
* 17:24 paladox: upgrade icinga2 on misc1
* 17:24 paladox: restarted ircecho on misc1
* 16:36 paladox: depooled mw1, mw2 and mw3 (in order and repooled)
* 10:32 paladox: repool mw3
* 10:30 paladox: depool mw3
* 10:30 paladox: repool mw2
* 10:26 paladox: reboot mw2
* 10:25 paladox: depooled mw2
* 10:10 Southparkfan: installed pv on db5
* 10:07 Southparkfan: purged even more binlogs @ db5
* 09:47 Southparkfan: purged binlogs on db5
* 09:18 Southparkfan: baobabarchiveswiki migrated to db5, changed cluster in cw_wikis, dropped database
* 08:51 Southparkfan: purged even more binlogs on db4

## 2019-09-20 

* 22:28 RhinosF1: rhinos@mw1:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php /home/rhinos/infobox.xml --wiki philosiversewiki
* 22:05 RhinosF1: rhinos@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php sql.php --wiki=metawiki --query="update cw_requests set cw_status = 'approved' where cw_id = 9311;"
* 21:55 paladox: disabled [https://phabricator.miraheze.org/H35](https://phabricator.miraheze.org/H35) and [https://phabricator.miraheze.org/H25](https://phabricator.miraheze.org/H25)
* 21:53 paladox: rebooted db5
* 21:52 RhinosF1: rhinos@mw1:/srv/mediawiki/w/extensions/CentralAuth/maintenance$ sudo -u www-data php createLocalAccount.php --wiki=bestmusicandsongswiki Inkster
* 21:50 RhinosF1: rhinos@mw1:/srv/mediawiki/w/extensions/CreateWiki/maintenance$ sudo -u www-data php populateMainPage.php --wiki=bestmusicandsongswiki
* 21:37 RhinosF1: rhinos@mw1:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php /home/rhinos/6.xml --wiki philosiversewiki
* 21:23 paladox: restarted networking on db5
* 21:03 paladox: rebooted glusterfs[12]
* 20:19 paladox: apt upgrade on test1
* 20:07 paladox: reboot test1
* 19:11 Reception123: purge binary logs before '2019-09-20 16:00:00'; on db4
* 16:44 paladox: granted RhinosF1 view rights on matomo
* 12:06 paladox: install nload on glusterfs1
* 07:19 RhinosF1: rhinos@mw1:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/initSiteStats.php --update  --wiki philosiversewiki
* 07:16 RhinosF1: rhinos@mw1:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildall.php --wiki philosiversewiki (post import maintenance)
* 07:11 RhinosF1: rhinos@mw1:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php /home/rhinos/[345].xml --wiki philosiversewiki
* 07:10 RhinosF1: rhinos@mw1:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php /home/rhinos/2.xml --wiki philosiversewiki
* 07:04 RhinosF1: rhinos@mw1:~$ sudo /root/ssl-certificate -d yellowiki.xyz -g -o
* 06:53 RhinosF1: rhinos@mw1:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php /home/rhinos/1.xml --wiki philosiversewiki
* 06:22 Reception123: purge binary logs before '2019-09-20 02:00:00';

## 2019-09-19 

* 17:04 paladox: revert is working!
* 17:01 paladox: manually reverting [https://git.io/Je3BR](https://git.io/Je3BR) on mw (each by each) testing new configuation change gluster side.
* 16:38 paladox: gluster volume set mvolume performance.parallel-readdir "on"
* 16:36 paladox: gluster volume set mvolume network.ping-timeout "20"
* 16:13 paladox: restarted glusterd on glusterfs[12]
* 16:09 paladox: gluster volume set mvolume performance.io-thread-count "12" - on gluster

## 2019-09-18 

* 23:42 paladox: gluster volume set mvolume server.event-threads "1" - on gluster
* 22:57 RhinosF1: rhinos@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php deleteBatch.php -r [mh:meta:User_talk:RhinosF1](https://meta.miraheze.org/wiki/mh:meta:User_talk:RhinosF1) /home/rhinos/pagedel.txt --wiki philosiversewik
* 21:55 paladox: update content_models set model_id = 3 where model_id = 4;
* 21:54 paladox: MariaDB [philosiversewiki]> update content_models set model_id = 4 where model_id = 3;
* 21:53 paladox: MariaDB [philosiversewiki]> update content_models set model_id = 1 where model_id = 4;
* 21:09 paladox: drop all wikis from [https://phabricator.miraheze.org/P227](https://phabricator.miraheze.org/P227)
* 18:12 paladox: delete philosiversewiki per request [https://meta.miraheze.org/wiki/User_talk:RhinosF1](https://meta.miraheze.org/wiki/User_talk:RhinosF1)
* 15:38 paladox: gluster volume set mvolume network.ping-timeout "15"
* 15:31 paladox: gluster volume set mvolume performance.parallel-readdir off - on gluster
* 15:30 paladox: gluster volume set mvolume client.event-threads "2"
* 14:48 paladox: gluster volume set mvolume performance.parallel-readdir on - on gluster
* 14:15 paladox: gluster volume set mvolume server.event-threads "2" - on gluster
* 14:10 paladox: gluster volume set mvolume client.event-threads "6" - on gluster
* 13:57 paladox: gluster volume set mvolume network.ping-timeout "10" on gluster

## 2019-09-17 

* 17:20 Southparkfan: run "SET GLOBAL expire_logs_days=4;" on db[45] to apply [https://git.io/JeOiN](https://git.io/JeOiN) without restart

## 2019-09-16 

* 21:41 RhinosF1: rhinos@mw1:/mnt/mediawiki-static$ sudo -u www-data mkdir -p milvagoxwiki
* 21:07 paladox: ban req.http.Host == tallguysfree.miraheze.org - cp2/cp3
* 21:06 paladox: ban req.http.Host == tallguysfree.miraheze.org - cp4
* 19:14 paladox: root@mw1:/mnt/mediawiki-static# mkdir -p nomansskywiki
* 19:10 paladox: root@mw1:/mnt/mediawiki-static# mkdir -p tallguysfreewiki
* 17:33 RhinosF1: generated ssl cert for wiki.tallfreeguys.com on mw1
* 17:18 RhinosF1: sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildLocalisationCache.php --wiki loginwiki (test1 and mw* (again))
* 17:18 RhinosF1: sudo -u www-data php /srv/mediawiki/w/maintenance/mergeMessageFileList.php --output /srv/mediawiki/config/ExtensionMessageFiles.php --wiki loginwiki (test1 and mw* (again))
* 17:18 RhinosF1: update managewiki on test1 due to puppet being off
* 17:13 RhinosF1: sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildLocalisationCache.php --wiki loginwiki (mw*)
* 17:13 RhinosF1: sudo -u www-data php /srv/mediawiki/w/maintenance/mergeMessageFileList.php --output /srv/mediawiki/config/ExtensionMessageFiles.php --wiki loginwiki (mw*)

## 2019-09-15 

* 22:51 paladox: reboot test1
* 22:32 RhinosF1: on test1 as well
* 22:28 RhinosF1: sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildLocalisationCache.php --wiki loginwiki on mw*
* 22:28 RhinosF1: sudo -u www-data php /srv/mediawiki/w/maintenance/mergeMessageFileList.php --output /srv/mediawiki/config/ExtensionMessageFiles.php --wiki loginwiki on mw*
* 21:20 RhinosF1: sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildLocalisationCache.php --wiki test1wiki
* 21:05 RhinosF1: sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildLocalisationCache.php --wiki loginwiki (both on test1)
* 21:04 RhinosF1: sudo -u www-data php /srv/mediawiki/w/maintenance/mergeMessageFileList.php --output /srv/mediawiki/config/ExtensionMessageFiles.php --wiki loginwiki
* 19:26 paladox: delete mw[456]
* 19:12 paladox: revoking firewalls on all servers for mw[456]
* 19:10 paladox: root@mw2:/mnt/mediawiki-static# mkdir -p perfectrobloxgameswiki
* 19:05 paladox: revoke mw[456] cert on puppet1
* 18:34 paladox: repool mw1
* 18:30 paladox: depool mw1 temporarily
* 18:20 paladox: repool mw1 temporarily
* 18:16 paladox: depool mw1
* 16:04 paladox: reboot test1
* 12:47 RhinosF1: rhinos@mw1:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/initSiteStats.php --update --active --wiki colchaguawiki (following import - observed dodgy stats)
* 12:31 RhinosF1: moved to mw1 (high load on test1)
* 12:18 RhinosF1: rhinos@test1:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildall.php --wiki colchaguawiki (following import)

## 2019-09-14 

* 23:23 paladox: upgrade phabricator - misc4
* 21:42 RhinosF1: rhinos@test1:/srv/mediawiki/config$ sudo -u www-data git pull (to deploy local settings change due to puppet being off)
* 20:41 paladox: root@mw1:/mnt/mediawiki-static# mkdir -p swedishmuseumwiki
* 15:34 RhinosF1: move import to test1 due to redis/JQ error
* 15:21 RhinosF1: restarting with screen
* 15:10 RhinosF1: rhinos@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php importDump.php --wiki colchaguawiki  /home/rhinos/colchaguawiki.xml
* 12:51 paladox: reboot test1
* 12:31 paladox: reimage gluserfs[12]

## 2019-09-13 

* 21:59 paladox: depool mw1
* 12:09 paladox: install golang on glusterfs1 to build the gluster prometheus exporter
* 00:45 paladox: depool mw[456]

## 2019-09-12 

* 23:12 paladox: adding 512M swap to mw5/mw6
* 22:33 paladox: rebooted mw5
* 15:46 RhinosF1: rhinos@mw1 sudo -u www-data php /srv/mediawiki/w/maintenance/importImages.php --wiki oecumenewiki /home/rhinos/oecumene/
* 12:17 paladox: rebooted mw1 through the control panel (was showing offline)
* 00:25 paladox: rsync /mnt/test (lizardfs) to /mnt/mediawiki-static (gluster) on test1

## 2019-09-11 

* 23:59 paladox: enable quota and set limit for / to 584GB on gluster
* 22:41 paladox: reset git dir on puppet1 back to what's in the git repo
* 22:13 paladox: reboot test1
* 19:56 paladox: reinstalling glusterfs[12]
* 19:00 RhinosF1: rhinos@test1:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/importImages.php --wiki oecumenewiki /home/rhinos/oecumene/ --search-recursively (T4958 - test1)
* 15:08 RhinosF1: and on mw1 finally
* 15:05 RhinosF1: +on mw3 as well (last 2)
* 15:00 RhinosF1: sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildLocalisationCache.php --wiki loginwiki
* 14:59 RhinosF1: sudo -u www-data php srv/Mediawiki/w/maintenance/mergeMessageFileList.php --output /srv/mediawiki/config/ExtensionMessageFiles.php --wiki loginwiki (on test1 and mw2)
* 07:06 Reception123: purge binary logs before '2019-09-11 02:00:00'; on db4
* 07:05 Reception123: deleted and dropped  agilesoftwaredevelopmentwiki; alphaanarchywiki; animefurryfeetwiki aqferwiki; article13wiki; asfrwiki; ayurbookswiki; bchitguideswiki  besttvchannelswiki; biblioenricowiki birdhousewiki;blooperwikiwiki; bubbawiki;bus42ruswiki; capgeminiplaybookwiki;casual4casualswiki; ccwpwiki; cgsimwiki;dellplanetwikiwiki;dreddbookwiki;mirahezewiki;
* 07:01 Reception123: sudo -u www-data php /srv/mediawiki/w/extensions/CreateWiki/maintenance/deleteWikis.php --wiki loginwiki --delete Reception123
* 05:58 Reception123: sudo -u www-data php /srv/mediawiki/w/extensions/CreateWiki/maintenance/renameWiki.php --wiki=loginwiki --rename uncyclopedia2wiki uncyc2wiki Reception123
* 05:54 Reception123: renamed sudo -u www-data php /srv/mediawiki/w/extensions/CreateWiki/maintenance/renameWiki.php --wiki=loginwiki --rename ogftreveldwiki evsmapswiki Reception123

## 2019-09-10 

* 21:36 paladox: that is on cp2
* 21:36 paladox: ban req.http.Host == meta.miraheze.org && req.url ~ "^/favicon.ico"
* 21:05 paladox: depool mw4
* 20:59 paladox: /srv/mediawiki/w/composer.phar install - mw4
* 19:40 paladox: [20:25:30]  <+paladox>    !log reboot lizardfs4
* 19:40 paladox:
* 19:38 paladox: restarted php-fpm on mw2
* 18:07 Reception123: created an icinga account for rhinosf1
* 16:59 Reception123: MariaDB [metawiki]> update cw_requests set cw_status = 'approved' where cw_id = 9205;
* 16:49 Reception123: created Matomo account for RhinosF1
* 16:48 RhinosF1: on test1
* 16:48 RhinosF1: sudo -u www-data php CreateLocalAccount.php --wiki=macrochasmwiki '	GambinoMacro'
* 16:36 Reception123: added RhinosF1 to @miraheze/mw-admins team on github
* 16:28 Reception123: created mail account for 'rhinosf1'
* 16:20 Reception123: purge binary logs before '2019-09-10 02:00:00';

## 2019-09-09 

* 19:24 paladox: creating glusterfs[12] instances in the cloud

## 2019-09-08 

* 19:54 paladox: setting up glusterfs on lizardfs[45] (temporarily)
* 18:21 paladox: delete from incidents_reviewer where r_incident = 21 and r_user = 'john'; - db4
* 15:17 Southparkfan: created mail account for voidwalker
* 15:04 paladox: depool mw4
* 14:58 paladox: repool mw4
* 14:11 paladox: depool mw4
* 13:40 paladox: hack hieradata/hosts/mw4.yaml on puppet1
* 13:38 paladox: pool mw4

## 2019-09-07 

* 21:15 paladox: ban req.http.Host == meta.miraheze.org && req.url ~ "^/favicon.ico" - cp2
* 00:34 paladox: UPDATE  `incidents` SET i_outage_total = '51',i_outage_visible = '53.15' WHERE i_id = '21'; - db4

## 2019-09-06 

* 19:16 paladox: depool mw4
* 16:44 paladox: running lc on mw4
* 16:43 paladox: reloaded lizardfs-master on misc3
* 14:10 paladox: increased swap to 1280M on misc3
* 02:16 paladox: a small downtime will happen (this is being done because misc3 OOM)
* 02:16 paladox: increasing swap size on misc3 to 768

## 2019-09-05 

* 21:30 paladox: revoke firewall for lizardfs[123] on misc3
* 21:24 paladox: revoke puppet cert for lizardfs[123]
* 20:53 paladox: restarting lizardfs-chunkserver on lizardfs4
* 20:49 paladox: stop lizardfs-chunkserver on lizardfs[123]
* 20:11 paladox: apt-get upgrade on misc1 and puppet1

## 2019-09-04 

* 17:19 paladox: [18:17:57]  <+paladox>	!log restarted lizardfs-chunkserver on lizardfs[45]
* 05:34 Reception123:  purge binary logs before '2019-09-04 02:00:00';

## 2019-09-02 

* 21:00 paladox: install make and g++ on misc3 (required for some npm dependancy in restbase)

## 2019-09-01 

* 15:14 Reception123: add valkyrienskieswiki to discord webhooks
* 14:54 Reception123: sudo service php7.2-fpm restart on mw*
* 00:23 paladox: repool mw2
* 00:21 paladox: depool mw2
* 00:18 paladox: repool mw2
* 00:10 paladox: depool mw2
* 00:07 paladox: reinstalling bacula1 with debian 10

## 2019-08-31 

* 21:48 paladox: delete from daemon_log where pid = 15565; on db4
* 21:48 paladox: delete from daemon_log where pid = 15083; on db4
* 21:47 paladox: delete from daemon_log where pid = 10833; on db4
* 21:39 paladox: upgrade phabricator on misc4
* 20:26 paladox: upgrade nodejs on misc1
* 20:26 paladox: apt-get install php-intl php-ldap php-mailparse php-mbstring php-mysql php-xml  php php-common php-curl php-igbinary php-imagick - misc1
* 20:25 paladox: apt-get install icingacli icingaweb2 icingaweb2-common icingaweb2-module-doc icingaweb2-module-monitoring - misc1
* 20:24 paladox: upgrade grafana on misc1
* 14:54 paladox: root@misc2:/home/paladox# apt-get install libgd3 libxml2 php-common php-igbinary php-imagick php-mailparse php-mbstring php-mysql php-xml
* 14:31 Reception123: reception@mw1:/srv/mediawiki/w/extensions/ManageWiki/maintenance$ sudo -u www-data php populateGroupPermissionsWithDefaults.php --wiki dfcharacterwiki --overwrite
* 07:11 Reception123: apt upgrade lilypond lilypond-data on mw*

## 2019-08-30 

* 22:41 paladox: running lc on mw*
* 18:59 paladox: dropping cargo__Train* from pokemonmasterswiki

## 2019-08-29 

* 12:35 Reception123: added simswiki to discord webhooks

## 2019-08-28 

* 20:52 Reception123: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki loginwiki
* 20:00 Reception123: added reviwikiwiki discord webhook to hiera
* 14:29 Reception123: added cwarswiki to discord webhooks in hiera
* 08:27 Reception123: purge binary logs before '2019-08-27 22:00:00'; on db4

## 2019-08-27 

* 21:36 paladox: running runJob on test1
* 20:09 Reception123: MariaDB [mhglobal]> DELETE FROM renameuser_status WHERE ru_wiki = 'brynda1231wiki';
* 20:04 Reception123: fixed further rename stuck issues after removing entries from db
* 20:00 Reception123: MariaDB [mhglobal]> DELETE FROM renameuser_status WHERE ru_wiki = 'besttvchannelswiki';
* 19:59 Reception123: MariaDB [mhglobal]> DELETE FROM renameuser_status WHERE ru_wiki = 'allwikiswiki';
* 19:20 Reception123: reception@mw1:/srv/mediawiki/w/extensions/CentralAuth/maintenance$ sudo -u www-data php fixStuckGlobalRename.php --logwiki metawiki --wiki metawiki AntiJawn PapercutsExist
* 19:19 Reception123: reception@mw1:/srv/mediawiki/w/extensions/CentralAuth/maintenance$ sudo -u www-data php fixStuckGlobalRename.php --logwiki metawiki --wiki metawiki JJTA1211 Jordan3047
* 19:15 Reception123: deleted and dropped agrolibrarywiki; akdorfgeschichtewiki; alerte112wiki; alientoasterdogwiki; alloverwiki; allwikiswiki; amcwiki; anarchymcwiki; angelwisewiki; arbreapalabrewiki; armourywikiwiki; arnathwiki;aufterrawiki; aukumniawiki; aweiowiki;battleaxewiki;bean3dwiki;billcgenealogywiki;bmsswiki; bncc3wiki; bokwiki; brucefamilywiki; brynda1231wiki; bscwiki;c105opwiki; calibrowiki;capouwiki; captainchumakwiki;cdisenoneswiki;
9:15 PM cedarcraftwiki;charleroiwiki; cheesewiki; cimphoniec2nwiki;clarencewiki; clarketransportwiki; closinglogoswiki;clubpenguinbrasilfanonwiki; cmhocwiki; collabuibfcwiki; comnumthwiki;esigningwiki; hypotheticalmetawiki; inprincipowiki; kyivstarwiki; mirahezefakenewswiki;orangistwiki; tallercristianowiki; testdelete10wiki; testdelete2wiki; weatherwiki;
* 06:50 Reception123: UPDATE cw_wikis SET wiki_settings = '{"wgDefaultSkin":"vector","wgLocaltimezone":"Asia\/Seoul","wgServer":"","wmgWikiLicense":"cc-by-sa"}' WHERE wiki_dbname = 'kkutuwiki'; (custom domain no longer points to us)

## 2019-08-26 

* 23:06 paladox: run runJob.php on test1
* 19:22 Reception123: MariaDB [metawiki]> update cw_requests set cw_status = 'approved' where cw_id = 9063;
* 19:22 Reception123: restarted jobrunner
* 19:20 Reception123: reception@mw1:/srv/mediawiki/w/extensions/CreateWiki/maintenance$ sudo -u www-data php populateMainPage.php --wiki=goanimatev6wiki
* 19:19 Reception123: reception@mw1:/srv/mediawiki/w/extensions/CentralAuth/maintenance$ sudo -u www-data php createLocalAccount.php --wiki=goanimatev6wiki 'Eijitheawesome'
* 18:34 Reception123: drop piwik database and reimport on db5
* 18:25 Reception123: MariaDB [metawiki]> update cw_requests set cw_status = 'approved' where cw_id = 9061;
* 18:23 Reception123: reception@mw1:/srv/mediawiki/w/extensions/CentralAuth/maintenance$ sudo -u www-data php createLocalAccount.php --wiki=2b2tmcpewiki 'Memelord27 '
* 18:22 Reception123: reception@mw1:/srv/mediawiki/w/extensions/CreateWiki/maintenance$ sudo -u www-data php populateMainPage.php --wiki=2b2tmcpewiki
* 18:19 Reception123: MariaDB [metawiki]> update cw_requests set cw_status = 'approved' where cw_id = 9062;
* 18:17 Reception123: reception@mw1:/srv/mediawiki/w/extensions/CreateWiki/maintenance$ sudo -u www-data php populateMainPage.php --wiki=aescraftwiki
* 16:50 Reception123: MariaDB [metawiki]> update cw_requests set cw_status = 'approved' where cw_id = 9058;
* 16:46 paladox: exporting matomo db, and reimporting it on db5
* 14:57 paladox: root@mw2:/home/paladox# sudo service cron start
* 12:45 Reception123: repool mw2
* 12:44 Reception123: started sshd and removed /var/run/nologin on mw2
* 12:33 Reception123: reboot mw2 (offline)
* 12:33 Reception123: depool mw2

## 2019-08-25 

* 21:36 paladox: running lc on mw*
* 16:09 Reception123: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki loginwiki on mw*
* 14:02 Reception123: deleted and dropped actualitywiki adullamwiki; aeriontechwiki; ag7732wiki;
* 13:44 paladox: running lc on mw*
* 02:55 paladox: root@lizardfs3:/home/paladox# sudo service lizardfs-chunkserver restart
* 02:54 paladox: root@lizardfs2:/home/paladox# sudo service lizardfs-chunkserver restart
* 02:34 paladox: root@lizardfs1:/home/paladox# sudo service lizardfs-chunkserver restart
* 01:28 paladox: restarting lizardfs chunkserver on lizardfs[123] to pickup a master ip change
* 01:06 paladox: added 1gb of swap to misc3 (new host)
* 00:47 paladox: sudo ufw allow from 185.52.1.71 on misc3

## 2019-08-23 

* 23:14 John: deleted Examknow account on Phabricator

## 2019-08-20 

* 20:04 Reception123: added horizonwiki to hiera private settings Discord webhook
* 13:54 Reception123: UPDATE cw_wikis SET wiki_dbcluster = 'c1'; (c2 wikis are old from db3, therefore pointless and confusing)

## 2019-08-19 

* 17:30 Reception123: moved frikipediawiki from db4 to db5 and DROP DATABASE frikipediawiki on db4
* 16:41 Reception123: moved testwiki from db4 to db5 and DROP DATABASE testwiki on db4
* 16:12 John: ran mediawiki grants for db5, wasn't done on install
* 16:06 Reception123: re-ran script above to force account rename
* 16:05 Reception123: temporarily re-added mirahezefakenewswiki to undeleted to resolve rename error
* 16:03 Reception123: reception@mw1:/srv/mediawiki/w/extensions/CentralAuth/maintenance$ sudo -u www-data php fixStuckGlobalRename.php --logwiki metawiki --wiki metawiki Znotch190711 OwenFung87
* 16:03 Reception123: temporarily re-added hypotheticalmetawiki to undeleted to resolve rename error
* 15:56 Reception123: reception@mw1:/srv/mediawiki/w/extensions/CentralAuth/maintenance$  sudo -u www-data php createLocalAccount.php --wiki=typhoonwikiwiki 'OwenFung87 '
* 13:21 Reception123: purge binary logs before '2019-08-19 06:00:00';

## 2019-08-18 

* 13:08 Reception123: sudo service lizardfs-chunkserver restart on lizardfs*
* 13:02 Reception123: sudo service lizardfs-chunkserver restart
* 12:29 Reception123: purge binary logs before '2019-08-17 22:00:00';

## 2019-08-17 

* 16:45 paladox: sudo -u www-data php removeOrphanedEvents.php --wiki=americangirldollswiki --force
* 16:39 paladox: running runJobs.php for all wikis on test1
* 16:29 paladox: redis-cli --scan --pattern *:cookieWarningIpLookupCache* | xargs -n 1 -d '\n' redis-cli  del
* 16:29 paladox: restarting redis
* 16:29 paladox: restart logbot - misc1
* 16:28 paladox: restarting redis
* 16:28 paladox: redis-cli --scan --pattern *:cookieWarningIpLookupCache* | xargs -n 1 -d '\n' redis-cli  del
* 16:28 paladox: restarting redis
* 16:12 paladox: redis-cli --scan --pattern *CookieWarning\Decisions:cookieWarningIpLookupCache* | xargs redis-cli  del
* 16:11 paladox: redis-cli --scan --pattern *cirrus* | xargs redis-cli  del
* 16:03 paladox: delete cp5 from firewall on mw*
* 11:27 Reception123: moved import for osaindexwiki to test1 due to redis issues
* 10:58 Reception123: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki loginwiki on mw*

## 2019-08-16 

* 19:42 Reception123: DROPPED DATABASE for 0h4rkwiki; 2019frst352wiki;  3mwiki; aceteccwiki
* 19:42 Reception123: deleted 0h4rkwiki; 2019frst352wiki;  3mwiki; aceteccwiki
* 18:04 Reception123: sudo -u www-data php /srv/mediawiki/w/maint*/mergeMessageFileList.php --output /srv/mediawiki/config/ExtensionMessageFiles.php --wiki loginwiki on test1
* 17:49 Reception123: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki loginwiki on mw*
* 17:49 Reception123: sudo -u www-data php /srv/mediawiki/w/maint*/mergeMessageFileList.php --output /srv/mediawiki/config/ExtensionMessageFiles.php --wiki loginwiki
* 17:44 Reception123: reception@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php importDump.php --no-local-users --username-prefix "오사위키" --wiki osaindexwiki /home/reception/dump_original.xml
* 11:10 Reception123: used update set to perform same replace command as above on opendominionwiki
* 10:52 Reception123: UPDATE cw_wikis SET wiki_settings = REPLACE(wiki_settings, '"wgServer":"https:\/\/wiki.opendominion.net "', '"wgServer":"https:\/\/wiki.opendominion.net"') WHERE wiki_dbname = 'opendominionwiki';

## 2019-08-15 

* 15:24 paladox: starting import for oecumenewiki - T4598
* 15:18 paladox: MariaDB [iceriawiki]> INSERT INTO content_models (model_id,model_name) VALUES (4,'Scribunto');
* 15:18 paladox: MariaDB [iceriawiki]> INSERT INTO content_models (model_id,model_name) VALUES (2,'css');
* 15:18 paladox: MariaDB [iceriawiki]> INSERT INTO content_models (model_id,model_name) VALUES (3,'javascript');
* 15:18 paladox: MariaDB [iceriawiki]> INSERT INTO content_models (model_id,model_name) VALUES (5,'json');
* 15:17 paladox: MariaDB [iceriawiki]> INSERT INTO content_models (model_id,model_name) VALUES (1,'wikitext');

## 2019-08-14 

* 23:04 paladox: delete from mw_namespaces where ns_dbname = 'hispanowiki' and ns_namespace_id = 3001;
* 18:49 paladox: restarting lizardfs-master on misc3 (proccess seemed to have stopped)
* 18:49 paladox: restarting lizardfs-master on misc3 (proccess seemed to have stopped)
* 18:49 paladox: restarting lizardfs-master on misc3 (proccess seemed to have stopped)
* 17:52 paladox: update mw_namespaces set ns_namespace_name = 'Guía_discusión' where ns_dbname = 'hispanowiki' and ns_namespace_name = 'Guía_talk';
* 16:35 Reception123: reception@mw1:/srv/mediawiki/w/extensions/RottenLinks/maintenance$ sudo -u www-data php updateExternalLinks.php --wiki cwarswiki
* 16:27 Reception123: upgraded phabricator
* 16:21 Reception123: MariaDB [phabricator_file]> UPDATE file SET viewPolicy = 'admin' WHERE id = 1012789;
* 16:21 Reception123: MariaDB [phabricator_file]> UPDATE file SET viewPolicy = 'admin' WHERE id = 1003845;
* 15:57 Reception123: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki loginwiki  on mw*
* 15:09 paladox: starting import for iceriawiki - T4648
* 14:48 paladox: recreating iceriawiki - [https://phabricator.miraheze.org/T4648](https://phabricator.miraheze.org/T4648)
* 05:21 Reception123: deleted and dropped testdelete1wiki
* 05:20 Reception123: restarted logbot

## 2019-08-13 

* 21:32 paladox: sudo ufw allow from 185.52.3.121 to any port 9113 - test1
* 19:01 paladox: upgrade nginx and php on misc1
* 19:01 paladox: upgrade grafana on misc1
* 18:58 paladox: upgrade php and nginx on misc4
* 18:57 paladox: upgrade php and nginx on misc2
* 18:53 paladox: reboot cp3
* 18:47 paladox: upgrade linux-image-4.9.0-9-amd64 linux-libc-dev nginx on cp4
* 18:46 paladox: also upgraded linux-libc-dev on cp[123]
* 18:45 paladox: upgrade nginx on cp2
* 18:42 paladox: upgrade nginx on cp4
* 18:28 paladox: repool mw2
* 18:22 paladox: depool mw2 and reboot
* 18:21 paladox: repool mw3
* 18:18 paladox: upgrade nginx & php on mw3
* 18:18 paladox: depool mw3
* 18:18 paladox: repool mw2
* 18:16 paladox: upgrade nginx & php on mw2
* 18:15 paladox: depool mw2
* 18:15 paladox: repool mw1
* 18:04 paladox: upgrade nginx & php on mw1
* 18:02 paladox: depool mw1

## 2019-08-12 

* 21:15 paladox: delete file F1012413 from phab
* 21:15 paladox: starting import for iceriawiki - T4646
* 18:06 Reception123: MariaDB [mhglobal]> UPDATE cw_wikis SET wiki_settings = REPLACE(wiki_settings, '"wgServer":"https:\/\/ahmsaqib.cf"', *) WHERE wiki_dbname = 'ahmsaqibwiki';
* 17:55 paladox: remove swapspace from misc2
* 17:53 paladox: install swapspace on misc2
* 05:22 Reception123: reception@mw2:/$ sudo php /srv/mediawiki/w/maintenance/dumpBackup.php --wiki zhdelwiki --full --output gzip:/home/reception/zhdelwiki12082019.xml --report 1 (part of wikibackups)
* 05:16 Reception123: reception@mw2:/mnt/mediawiki-static$ sudo php /srv/mediawiki/w/maintenance/dumpBackup.php --wiki nltramswiki --full --output gzip:/home/reception/nltramswiki12082019.xml --report 1 (part of wikibackups)
* 05:10 Reception123: sudo service lizardfs-chunkserver restart

## 2019-08-11 

* 18:49 Reception123: reception@mw2:~$ sudo php /srv/mediawiki/w/maintenance/dumpBackup.php --wiki nonciclopediawiki --full --output gzip:/home/reception/nonciclopediawiki11082019.xml --report 1 (part of wikibackups)
* 18:45 Reception123: sudo -u www-data php deleteBatch.php --wiki projectbiologiawiki --r="Deletion of Времянка/ per T4541" /home/reception/projectbiologia_del.txt
* 18:39 Reception123: reception@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php deleteBatch.php --wiki willdonahuewiki --r="Deletion of infoboxes per T4633" /home/reception/delete_willdonahue.txt
* 18:31 Reception123: dropped lcpsseacwiki (rename)
* 18:29 Reception123: sudo -u www-data php /srv/mediawiki/w/extensions/CreateWiki/maintenance/renameWiki.php --wiki=loginwiki --rename lcpsseacwiki loudounseacwki Reception123
* 16:19 Reception123: reception@mw2:~$ sudo php /srv/mediawiki/w/maintenance/dumpBackup.php --wiki poserdazfreebieswiki --full --output gzip:/home/reception/poserdazfreebieswiki11082019.xml --report 1 (part of wikibackups)
* 10:52 Reception123: sudo php /srv/mediawiki/w/maintenance/dumpBackup.php --wiki allthetropeswiki --full --output gzip:/home/reception/allthetropes11082019.xml --report 1 (on mw2; part of wikibackups)
* 10:20 Reception123: reception@test1:/srv/mediawiki/w/maintenance$ sudo -u www-data php importDump.php --wiki wandocyberwiki /home/reception/wandocyberwiki.xml
* 10:20 Reception123: sudo -u www-data php importDump.php --wiki apellidosmurcianoswiki /home/reception/apellidosmurcianoswiki.xml

## 2019-08-10 

* 23:00 paladox: MariaDB [metawiki]> update cw_requests set cw_status = 'approved' where cw_id = 8923;
* 22:22 paladox: root@mw1:/srv/mediawiki/w/extensions/CreateWiki/maintenance# sudo -u www-data php populateMainPage.php --wiki=botdogswiki
* 15:11 paladox: delete miraheze/search-extra
* 15:11 paladox: delete miraheze/operations-software-elasticsearch-plugins
* 12:48 paladox: MariaDB [(none)]> drop database testdb
* 12:46 Reception123: re-run wikibackups (./wikibackups.sh /home/reception/allpublic.dblist /srv/mediawiki/w/maintenance/dumpBackup.php)

## 2019-08-09 

* 21:48 paladox: import images from MediatecaWiki to CommonsWiki - T4634
* 11:46 paladox: restart mysql on db5
* 11:46 paladox: usermod -a -G ssl-cert mysql - db5
* 10:31 Reception123: reception@test1:/srv/mediawiki/w/maintenance$ sudo -u www-data php importDump.php --wiki mprwiki /home/reception/Wikipedia-20190809082641.xml (restarted on test1 instead of mw1; redis fails)
* 10:30 Reception123: > UPDATE cw_requests SET cw_status = 'approved' WHERE cw_id = 8910;
* 10:29 Reception123: > UPDATE cw_requests SET cw_status = 'approved' WHERE cw_id = 8909;
* 10:19 Reception123: reception@mw2:/srv/mediawiki/w/extensions/CentralAuth/maintenance$ sudo -u www-data php createLocalAccount.php --wiki=discoveryofindiawiki 'TheHangedAstronaut '
* 10:18 Reception123: reception@mw2:/srv/mediawiki/w/extensions/CentralAuth/maintenance$ sudo -u www-data php createLocalAccount.php --wiki=alacritysimwiki 'Bobbie3254'
* 08:56 Reception123: reception@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php importDump.php --wiki mprwiki /home/reception/Wikipedia-20190809082641.xml
* 06:27 Reception123: running wikibackups (./wikibackups.sh /home/reception/allpublic.dblist /srv/mediawiki/w/maintenance/dumpBackup.php)

## 2019-08-08 

* 21:34 paladox: update cw_requests set cw_status = 'approved' where cw_id = 8907;
* 20:53 paladox: root@mw1:/srv/mediawiki/w/extensions/CentralAuth/maintenance# sudo -u www-data php createLocalAccount.php --wiki=megamanspritecomicwiki 'JJTA1211'
* 20:52 paladox: root@mw1:/srv/mediawiki/w# sudo -u www-data php extensions/CreateWiki/maintenance/populateMainPage.php --wiki=megamanspritecomicwiki
* 12:54 paladox: upgrade phabricator

## 2019-08-07 

* 17:48 paladox: starting import for crystalmaidenswiki - T4577

## 2019-08-06 

* 21:53 paladox: starting import for usruwiki - T4575
* 21:48 paladox: starting import for ucroniaswiki

## 2019-08-05 

* 23:07 paladox: reset puppet repo on puppet1 (removing hacks for stunnel)
* 21:09 paladox: starting import for commonwealthwiki
* 19:01 paladox: starting import for evilbabeswiki - T4571
* 18:58 paladox: starting import for incubatorwiki - T4517
* 18:43 paladox: starting import for trollpastawikiwiki - T4215
* 16:08 paladox: hacked stunnel config on puppet1 again
* 00:55 paladox: upgraded stunnel on cp3 (a while ago)
* 00:17 paladox: apt-get install -t stretch-backports stunnel4 - cp4
* 00:15 paladox: add www-data to ssl-cert group on cp3

## 2019-08-04 

* 23:04 paladox: install mysql-client on mw1
* 22:55 paladox: reboot mw1 (having mysql conn issues)
* 19:23 paladox: depooling cp2 (testing some configuation changes && package update)
* 14:31 paladox: recreating ucroniaswiki
* 14:16 paladox: MariaDB [mhglobal]> drop table mw_permissions2; -db4
* 14:15 paladox: delete from cw_wikis where wiki_dbname = 'ucroniaswiki'; -db4
* 14:14 paladox: drop from cw_wikis where wiki_dbname = 'ucroniaswiki'; -db4
* 14:05 paladox: change /etc/hosts on db5 to have "185.52.1.89 db5.miraheze.org        db5" instead of "127.0.1.1      db5.miraheze.org        db5"
* 13:51 paladox: drop ucroniaswiki db
* 13:24 paladox: renaming ucroniaswiki to ucroniasantiguowiki - T4606

## 2019-08-03 

* 23:33 paladox: apt-get upgrade on bacula1
* 23:32 paladox: deleting old backups on bacula1 (fresh backups will start being generated in ~30mins)
* 21:53 paladox: restart stunnel4 on cp2
* 21:36 paladox: restart varnish and nginx on cp2
* 16:14 paladox: sudo service lizardfs-chunkserver restart on lizardfs[123]
* 11:56 Reception123: sudo service lizardfs-chunkserver restart (again)
* 11:56 Reception123: removed /srv/mediawiki-static/dumps (obsolete, replaced by datadump_
* 11:51 Reception123: sudo service lizardfs-chunkserver restart

## 2019-08-02 

* 14:26 John: DELETE FROM config_entry WHERE configKey = 'phabricator.uninstalled-applications';
* 13:59 paladox: sudo -u www-data php updateArticleCount.php --wiki=nonciclopediawiki --update - T4312
* 13:46 paladox: root@mw1:/srv/mediawiki/w/maintenance# sudo -u www-data php updateArticleCount.php --wiki=gfiwiki --update - T4595

## 2019-08-01 

* 20:51 paladox: ban req.http.Host == g12.miraheze.org - cp4
* 20:40 paladox: upgrade packages on cp[234]
* 20:37 paladox: upgrade packages on lizardfs[123]
* 20:34 paladox: upgrade puppet on lizardfs[123]
* 20:30 paladox: upgrade php and puppet on test1
* 20:27 paladox: upgrade puppet on mw[123]
* 20:25 paladox: upgrade puppet-agent on db4
* 20:23 paladox: upgrade a few packages on misc3
* 20:14 paladox: upgrade puppet on ns1
* 20:02 paladox: upgrade icingaweb2, php and puppet-agent on misc1
* 20:00 paladox: upgrade puppet to 6.7.2 on puppet1 (it will fix the regression)
* 19:59 paladox: upgrade puppet to 6.7.2 on misc4 (it will fix the regression)
* 19:59 Reception123: removed /etc/aliases on misc4 (puppet bug, refresh)
* 18:26 paladox: restart jobchron and jobrunner on mw3
* 18:19 paladox: upgrade php on misc2
* 18:19 paladox: delete cirrusSearchLinksUpdatePrioritized from redis
* 18:19 paladox: delete cirrusSearchLinksUpdate from redis
* 18:18 paladox: delete cirrusSearchElasticaWrite from redis
* 18:14 paladox: sudo -u www-data php rebuildtextindex.php --wiki=test1wiki - mw1
* 18:14 paladox: sudo -u www-data php rebuildtextindex.php --wiki=pointmanwiki - mw1
* 18:13 paladox: create searchindex table for test1wiki on db4
* 18:13 paladox: create searchindex table for pointmanwiki on db4
* 18:12 paladox: sudo -u www-data php rebuildtextindex.php --wiki=nonsensopediawiki - mw1
* 18:12 paladox: create searchindex table for nonsensopediawiki on db4
* 18:08 paladox: sudo -u www-data php rebuildtextindex.php --wiki=isvwiki - mw1
* 18:07 paladox: sudo -u www-data php rebuildtextindex.php --wiki= isvwiki - mw1
* 18:07 paladox: create searchindex table for isvwiki on db4
* 18:06 paladox: sudo -u www-data php rebuildtextindex.php --wiki=buswiki - mw1
* 18:06 paladox: rebuildtextindex.php being ran on mw1 not db4
* 18:05 paladox: create searchindex table for buswiki on db4
* 18:00 paladox: sudo -u www-data php rebuildtextindex.php --wiki=allthetropeswiki - db4
* 17:59 paladox: create searchindex table for allthetropeswiki on db4
* 17:58 paladox: sudo -u www-data php rebuildtextindex.php --wiki=metawiki - db4
* 17:57 paladox: create searchindex table for metawiki on db4
* 16:25 paladox: drop piwik on db4
* 15:29 paladox: moving piwik (matomo) db to db5
* 15:28 paladox: root@misc2:/home/paladox# sudo service php7.3-fpm stop - misc2
* 15:10 paladox: REVOKE ALL PRIVILEGES ON *.* FROM 'icinga'@'185.52.1.76'; -db4
* 15:08 paladox: revoke usage on *.* from 'icinga'@'185.52.1.76'; -db4
* 00:43 paladox: MariaDB [icinga]> drop table test; -db5
* 00:32 paladox: GRANT SELECT, INSERT, UPDATE, DELETE, DROP, CREATE VIEW, INDEX, EXECUTE ON icinga.* TO 'icinga'@'185.52.1.76' IDENTIFIED BY 'xxxx'; -db4
* 00:32 paladox: REVOKE ALL PRIVILEGES ON *.* FROM 'icinga'@'81.4.109.166'; -db4
* 00:31 paladox: that's for db4 not db5
* 00:31 paladox: REVOKE ALL PRIVILEGES ON *.* FROM 'icinga'@'185.52.1.76'; -db5

## 2019-07-31 

* 23:10 paladox: CREATE TABLE /*_*/test (`test` VARCHAR(64) NOT NULL); - db5
* 11:45 Reception123: purge binary logs before '2019-07-31 11:00:00';
* 11:37 Reception123: removed /etc/aliases on misc4 (refresh, puppet error)
* 11:34 Reception123: re-enable puppet on misc4

## 2019-07-26 

* 16:41 paladox: sudo -u www-data /usr/local/bin/fileLockScript.sh /tmp/matomo_file_lock "/usr/bin/nice -19 /usr/bin/php /srv/matomo/console core:archive --url= [https://matomo.miraheze.org/](https://matomo.miraheze.org/)" > /srv/matomo-archive.log - misc2
* 15:19 paladox: root@mw1:/mnt/mediawiki-static/windows95wikiwiki# cp -R /srv/mediawiki/w/extensions/SocialProfile/awards ./awards - T4578
* 15:18 paladox: root@mw1:/mnt/mediawiki-static/windows95wikiwiki# cp -R /srv/mediawiki/w/extensions/SocialProfile/avatars ./avatars - T4578
* 02:11 paladox: disable the salt master temporarily

## 2019-07-25 

* 20:26 paladox: reboot misc4
* 18:43 paladox: upgrading salt accross all hosts
* 18:38 paladox: accidentally removed /var/log on misc3 (was ment to remove /var/log/salt but missed 'salt')
* 17:18 paladox: apt-upgrade - misc4
* 13:16 paladox: deleting es* instances

## 2019-07-24 

* 20:03 paladox: [20:59:45] <+paladox>	!log restart mysql - db4
* 19:27 paladox: shutting es[1-4]
* 18:28 Reception123: UPDATE cw_requests SET cw_status = 'approved' WHERE cw_id = 8739;
* 18:11 Reception123: reception@mw1:/srv/mediawiki/w/extensions/CentralAuth/maintenance$ sudo -u www-data php createLocalAccount.php --wiki topbikewiki TomK
* 17:57 Reception123: UPDATE cw_requests SET cw_status = 'approved' WHERE cw_id = '8727'; (cannot be done on-wiki)
* 17:49 Reception123: reception@mw1:/srv/mediawiki/w/extensions/CentralAuth/maintenance$ sudo -u www-data php createLocalAccount.php --wiki thecommonwealthwiki Monatch
* 15:48 paladox: switched es3 back on
* 15:43 paladox: shut down es3 temporarily
* 15:30 paladox: stop salt-master on misc4 temporarily
* 15:27 paladox: rebooted misc4 - oom
* 00:22 paladox: reboot misc4

## 2019-07-23 

* 21:42 paladox: upgrade puppet-agent, puppetdb and puppetserver on puppet1
* 21:35 paladox: root@misc4:/srv# rm /etc/aliases - puppet failing with " Could not prefetch mailalias provider 'aliases': Could not parse line "postmaster: root" (file: /etc/aliases, line: 3)"
* 21:28 paladox: upgrade puppet-agent - misc4
* 21:28 paladox: that was for misc4
* 21:28 paladox: restart prometheus - phd - php-fpm on misc (OOM)
* 20:36 paladox: sudo -u www-data /usr/local/bin/fileLockScript.sh /tmp/matomo_file_lock "/usr/bin/nice -19 /usr/bin/php /srv/matomo/console core:archive --url= [https://matomo.miraheze.org/](https://matomo.miraheze.org/)" > /srv/matomo-archive.log' - misc2
* 15:28 paladox: apt upgrade - test1
* 14:46 paladox: reboot cp3
* 14:45 paladox: increasing swap on cp3 to 2gb
* 14:40 paladox: depool cp3

## 2019-07-22 

* 21:51 paladox: deleted db5
* 18:46 paladox: resetting es cluster
* 14:29 paladox: db4: MariaDB [piwik]> drop database piwik;
* 03:03 paladox: GRANT REPLICATION CLIENT ON *.* TO 'wikiadmin'@'%'; - db4
* 00:42 paladox: db5: sudo fallocate -l 8G /swapfile ; sudo chmod 600 /swapfile ; sudo mkswap /swapfile ; sudo swapon /swapfile
* 00:11 paladox: provision db5

## 2019-07-21 

* 23:39 paladox: root@db4:/home/paladox# rm /srv/mariadb/mysql-bin.000982 (bin log was not in /srv/mariadb/mysql-bin.index)
* 20:01 Reception123: purge binary logs before '2019-07-21 18:00:00';
* 16:35 paladox: rebuilding es2
* 06:26 Reception123: purge binary logs before '2019-07-21 05:00:00';

## 2019-07-20 

* 19:56 Reception123: purge binary logs before '2019-07-20 18:00:00';
* 17:37 paladox: upgrade phabricator - misc4
* 17:36 paladox: apt upgrade - misc1
* 17:35 paladox: apt upgrade - misc4
* 17:14 paladox: apt upgrade - puppet1
* 16:58 paladox: root@mw1:/srv/mediawiki/w/maintenance# sudo -u www-data php deleteBatch.php --wiki=cwarswiki page_deletion
* 14:46 paladox: root@misc2:/etc/php/7.3# apt-get upgrade
* 13:44 paladox: root@misc2:/var/spool/cron/crontabs# rm www-data
* 13:43 paladox: removing the archive script from misc2 (temporarily, to stop space filling up on the db, this will stop stats from updating)
* 09:38 Reception123: purge binary logs before '2019-07-20 07:00:00';
* 02:38 paladox: reboot cp4
* 02:37 paladox: apt upgrade - cp4
* 02:34 paladox: depool cp4
* 02:23 paladox: apt-get upgrade - misc2

## 2019-07-19 

* 22:39 paladox: apt install maven on test1
* 22:38 paladox: forking [https://github.com/wikimedia/operations-software-elasticsearch-plugins](https://github.com/wikimedia/operations-software-elasticsearch-plugins)
* 20:20 paladox: provision es4
* 19:34 Reception123: purge binary logs before '2019-07-19 17:00:00';
* 15:40 paladox: restarting elasticsearch on es* (includes stopping and starting)
* 15:04 paladox: adjusting swap on es2
* 14:53 paladox: adjusting swap on es1
* 14:29 paladox: stopping es on es1
* 14:20 paladox: (started es on es3 a few minutes ag)
* 14:13 paladox: stopping es on es3 to adjust swap
* 12:59 paladox: install iotop on es1
* 12:51 paladox: forking [https://github.com/wikimedia/search-extra](https://github.com/wikimedia/search-extra)
* 05:18 Reception123: purge binary logs before '2019-07-19 03:00:00';

## 2019-07-18 

* 19:38 Reception123: purge binary logs before '2019-07-18 17:00:00';
* 18:18 paladox: reinstall es1 as stretch
* 17:28 paladox: connected es1 up to puppet1
* 15:14 Reception123: purge binary logs before '2019-07-18 13:00:00';
* 13:53 paladox: deleted test1wiki:* from redis
* 05:40 Reception123: purge binary logs before '2019-07-18 04:00:00';

## 2019-07-17 

* 23:25 paladox: rebooted elasticsearch2
* 21:26 paladox: connected elasticsearch2 to puppet1
* 17:31 paladox: MariaDB [piwik]> OPTIMIZE table piwik_archive_blob_2019_06;
* 14:27 Reception123: deleted and dropped reviwbwiki
* 11:57 Reception123: purge binary logs before '2019-07-17 10:00:00';

## 2019-07-16 

* 19:32 paladox: downgrade restbase back to ab6b368
* 19:25 Reception123: purge binary logs before '2019-07-16 16:00:00';
* 17:10 paladox: upgrade from ab6b368 to bdc4029 (restbase on misc3)
* 17:10 paladox: root@misc3:/srv/restbase# sudo -u restbase git pull
* 11:21 paladox: MariaDB [piwik]> OPTIMIZE table piwik_archive_blob_2019_06;
* 11:07 paladox: root@misc2:/var/spool/cron/crontabs# /usr/local/bin/fileLockScript.sh /tmp/matomo_file_locks "/usr/bin/nice -19 /usr/bin/php /srv/matomo/console core:purge-old-archive-data all"
* 09:09 Reception123: reception@misc2:/srv/matomo$ sudo /usr/bin/php /srv/matomo/console core:archive --url= [https://matmo.miraheze.org/matomo/](https://matmo.miraheze.org/matomo/) > /home/reception/matomo-archive.log
* 05:11 Reception123: purge binary logs before '2019-07-16 03:00:00';

## 2019-07-15 

* 17:42 Reception123: purge binary logs before '2019-07-15 16:00:00';
* 05:25 Reception123: purge binary logs before '2019-07-15 03:00:00';

## 2019-07-14 

* 18:52 John: UPDATE cw_requests SET cw_status = 'approved' WHERE cw_id = 8681;
* 09:00 Reception123: purge binary logs before '2019-07-14 09:00:00';

## 2019-07-13 

* 19:47 Reception123: deleted and dropped dbs listed [https://phabricator.miraheze.org/P214](https://phabricator.miraheze.org/P214)
* 19:41 Reception123: reception@mw1:~$ sudo -u www-data php /srv/mediawiki/w/extensions/CreateWiki/maintenance/deleteWikis.php --wiki loginwiki Reception123 --delete
* 16:11 paladox: root@db4:/bacula/restore# rm -rf *
* 15:57 paladox: [16:41:38] <+paladox>	!log restarted lizardfs-master on misc3 (appears to have stopped it's self)
* 12:09 Reception123: renamed medlitreviewswiki to theliteratureprojectwiki.
* 06:06 Reception123: purge binary logs before '2019-07-13 06:00:00';

## 2019-07-12 

* 23:32 paladox: reboot elasticsearch1
* 21:46 paladox: resetting elasticsearch
* 20:34 paladox: deleted jobrunner jobs for absolutetruthwiki (including wiki specific jobs)
* 19:34 paladox: root@elasticsearch1:/home/paladox# curl -X POST -H 'Content-Type: application/json' localhost:9200/mw_cirrus_metastore_first/settings -d '{"settings": {"index.priority": 10}}'
* 18:03 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=wackypediawiki --report=1 /home/reception/illogicopedia_pages_full.xml on test1 (due to Redis hack)
* 18:03 Reception123: hack Redis.php on test1 for import
* 09:53 Reception123: reception@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=wackypediawiki --report=1 /home/reception/illogicopedia_pages_full.xml
* 09:52 Reception123: reception@mw2:/srv/mediawiki/w/maintenance$ sudo -u www-data php importImages.php --wiki wackypediawiki --search-recursively /home/reception/wackypediaimages
* 09:33 Reception123: purge binary logs before '2019-07-12 09:00:00';

## 2019-07-11 

* 22:58 paladox: running updateOneSearchIndexConfig.php for all wikis
* 22:45 paladox: reverting php-fpm childs on mw*
* 21:56 paladox: repool mw3
* 21:50 paladox: depool mw3, and reboot
* 21:40 paladox: kill -9 749 (mw3)
* 21:40 paladox: kill -9 7626 (mw3)
* 21:39 paladox: kill -9 7625 (mw3)
* 21:07 paladox: kill $(ps -A -ostat,ppid | awk '/[zZ]/ && !a[$2]++ {print $2}') on mw3
* 20:59 paladox: depool mw3 && hack php-fpm childs && restart php-fpm && repool mw3
* 20:57 paladox: depool mw1 && hack php-fpm childs && restart php-fpm && repool mw1
* 19:42 paladox: repool mw2
* 19:38 paladox: depool mw2
* 01:13 paladox: repool mw2
* 01:04 paladox: depool mw2
* 00:59 paladox: root@mw1:/home/reception# rm -rf wikibackups
* 00:28 paladox: repool mw2
* 00:27 paladox: root@mw1:/home/reception# tar -zcvf wikibackups.tar.gz wikibackups
* 00:22 paladox: depool mw2 and reboot

## 2019-07-10 

* 23:59 paladox: that's for mw1
* 23:59 paladox: rm undefined.log*
* 23:53 paladox: cancle updateSearchIndexConfig.php (es OOM)
* 23:35 paladox: repool mw2
* 23:32 paladox: restart php-fpm && nginx on mw2
* 23:30 paladox: depool mw2
* 23:04 paladox: running updateSearchIndexConfig.php for all wikis

## 2019-07-09 

* 17:19 paladox: [18:15:08] <+paladox>	!log rm /srv/mariadb/mysql-bin.001240 && sudo service mysql restart
* 00:59 paladox: /usr/bin/nice -19 /usr/local/bin/foreachwikiindblist /srv/mediawiki/w/extensions/CirrusSearch/maintenance/eswikis /srv/mediawiki/w/extensions/CirrusSearch/maintenance/forceSearchIndex.php
* 00:10 paladox: /usr/bin/nice -19 /usr/local/bin/foreachwikiindblist /srv/mediawiki/w/extensions/CirrusSearch/maintenance/eswikis /srv/mediawiki/w/extensions/CirrusSearch/maintenance/updateSearchIndexConfig.php --reindexAndRemoveOk --indexIdentifier now
* 00:08 paladox: sudo -u www-data php metastore.php --upgrade --wiki=metawiki
* 00:03 paladox: upgrading elasticsearch to 6 on elasticsearch1

## 2019-07-08 

* 20:44 paladox: deleted Lifelonglearner per [https://meta.miraheze.org/w/index.php?title=Meta:Administrators%27_noticeboard&diff=prev&oldid=77234](https://meta.miraheze.org/w/index.php?title=Meta:Administrators%27_noticeboard&diff=prev&oldid=77234)
* 08:03 Reception123: purge binary logs before '2019-07-08 05:00:00';

## 2019-07-07 

* 21:55 paladox: depool mw1 && revert nginx / php-fpm change && repool
* 20:42 paladox: changing php-fpm to use TCP rather then socket on mw1 (includes depooling and repooling mw1)
* 20:40 paladox: reverted nginx config
* 20:33 paladox: depool mw1 && remove "use epoll" from nginx (to see how it does) && repool mw1
* 20:15 paladox: repool mw1
* 20:15 paladox: restarting nginx on mw1
* 20:12 paladox: depool mw1
* 20:05 paladox: root@mw1:/var/log/nginx# sysctl -w net.core.somaxconn=256
* 14:05 Reception123: purge binary logs before '2019-07-07 09:00:00';
* 04:02 paladox: upgrade puppet-agent on bacula1
* 03:16 paladox: doing the same for DB4 (and other backups)
* 03:14 paladox: deleting STATIC* on bacula1 (to generate a new backup)
* 02:53 paladox: depool mw1 && restart nginx (due to D state) && repool
* 02:48 paladox: repool mw2
* 02:42 paladox: depooling mw2 (and rebooting due to nginx process stuck in D)
* 02:39 paladox: repool mw1
* 02:33 paladox: reboot mw1
* 02:32 paladox: depool mw1
* 02:31 paladox: repool mw1
* 02:30 paladox: restarting php-fpm on mw1 (proccesses stuck in D)
* 02:28 paladox: depool mw1

## 2019-07-06 

* 11:52 paladox: cleaned bin logs && restarted mysql (due to out of storage)

## 2019-07-05 

* 03:43 paladox: that's on misc2
* 03:43 paladox: killed stray puppet-agent processes (3)
* 03:34 paladox: running matomo archive in a screen (misc2)
* 03:27 paladox: killed a bunch of duplicate matomo archive processes under the user wwww-data

## 2019-07-04 

* 23:06 paladox: depool mw3 and restart php-fpm to pick up .so file and repool
* 23:05 paladox: depool mw1 and restart php-fpm to pick up .so file and repool
* 23:03 paladox: repool mw2
* 23:00 paladox: depooling mw2 && restarting php-fpm to pickup .so file
* 22:46 paladox: running lc on mw*
* 22:37 paladox: repool mw2
* 22:19 paladox: upgraded puppet-agent and dbus on mw2
* 22:17 paladox: depool mw2 (and restart as nginx is showing as a D state process)
* 22:04 paladox: repooling mw2
* 21:57 paladox: killing a D state process (nginx) on mw2
* 21:57 paladox: depool mw2
* 21:29 paladox: remove PII from a user
* 20:38 paladox: MariaDB [nonciclopediawiki]> truncate objectcache;
* 17:27 paladox: deleting tsbsaltmineswiki (for it to be recreated)
* 16:45 paladox: running lc on mw*
* 14:56 paladox: setting REL1_33 as default branch in mediawiki
* 12:45 paladox: root@mw1:/var/log/mediawiki# rm *.log*
* 12:13 paladox: rm undefined.log* (mw1)
* 00:48 paladox: aborted, appears update.php is doing it.
* 00:47 paladox: apply Echo/db_patches/patch-drop-notification_bundle_display_hash.sql to all wikis
* 00:34 paladox: restarted jobrunner/jobchron on mw3

## 2019-07-03 

* 20:28 paladox: make that all mw*
* 20:27 paladox: adding nginx exporter to mw1
* 20:13 paladox: hacking puppet manifest to enable nginx exporter on test1
* 20:04 paladox: restarting php-fpm across mw*
* 19:34 paladox: installing [https://github.com/martin-helmich/prometheus-nginxlog-exporter](https://github.com/martin-helmich/prometheus-nginxlog-exporter) on test1
* 12:52 paladox: removing a users PII
* 01:08 paladox: running update.php for all wikis (on mw1 in a screen)
* 00:50 paladox: repool mw2
* 00:39 paladox: running lc on mw1 and mw3
* 00:35 paladox: depool mw2 to upgrade to mw 1.33
* 00:35 paladox: repool mw3
* 00:22 paladox: depool mw3 for mw upgrade to 1.33
* 00:22 paladox: repool mw1
* 00:04 paladox: depool mw1 for upgrade to mw 1.33.

## 2019-07-02 

* 21:02 paladox: update cw_wikis set wiki_settings = REPLACE(wiki_settings, '"wgDefaultSkin":"darkvector"', '"wgDefaultSkin":"vector"');

## 2019-07-01 

* 18:57 paladox: running ALTER TABLE mw_namespaces MODIFY COLUMN ns_core INT(1) NOT NULL DEFAULT 0;

## 2019-06-29 

* 19:28 paladox: update mw_namespaces set ns_content_model = 'wikitext' where ns_namespace_name = 'Module_talk';
* 18:17 paladox: added "Module_talk" ns to all wikis in mw_namespace
* 17:58 paladox: upgraded phabricator
* 17:37 paladox: delete from mw_namespaces where ns_namespace_name = 'Module' on db4
* 17:37 paladox: sudo -u www-data php populateNamespacesWithDefaults.php --wiki=0h4rkwiki --overwrite on mw1
* 17:32 paladox: added "Module" ns to all wikis in mw_namespace
* 17:32 paladox: added "Module_talk" ns to 'default' dbname in mw_namespace
* 17:31 paladox: added "Module" ns to 'default' dbname in mw_namespace
* 15:02 paladox: deleting all pages that start with Thread: on rottenwebsiteswiki - T4407
* 14:08 paladox: test
* 13:53 paladox: root@test1:/srv/mediawiki/w/extensions/ManageWiki# sudo -u www-data git reset --hard origin/master
* 13:53 paladox: root@test1:/srv/mediawiki/w/extensions/MirahezeMagic# sudo -u www-data git reset --hard origin/master

## 2019-06-28 

* 01:15 paladox: cp4 i cleaned the firewall actually not mw1.
* 01:14 paladox: repool mw1
* 01:12 paladox: depooling mw1 to clean firewall
* 01:10 paladox: delete banned ip from firewall

## 2019-06-27 

* 23:49 paladox: starting import for cwarswiki - T4498
* 23:17 paladox: banning an ip on cp4 firewall
* 22:09 paladox: sudo apt-get install php7.2-dev liblua5.1-0-dev on mw1
* 21:18 paladox: repooling mw1 temporarily to see if max childs 6 for php-fpm improves stability
* 21:16 paladox: that ^^ is for mw1
* 21:15 paladox: testing setting php-fpm max childs to 6
* 21:15 paladox: depool mw1
* 17:50 paladox: repool mw1
* 17:40 paladox: rebooting mw1 (due to some process causing high load)
* 17:40 paladox: depool mw1
* 17:21 paladox: depool mw1 && restart nginx && repool
* 17:19 paladox: repool mw1
* 17:17 paladox: restart php7.2-fpm on mw1
* 17:17 paladox: depool mw1
* 13:54 paladox: TRUNCATE TABLE objectcache; for allthetropeswiki
* 13:53 paladox: TRUNCATE TABLE objectcache; for buswiki
* 13:51 paladox: drop searchindex table for buswiki

## 2019-06-26 

* 19:30 paladox: delete from mw_namespaces where ns_namespace_name = 'Module_talk';
* 19:30 paladox: delete from mw_namespaces where ns_namespace_name = 'Module';
* 11:09 paladox: uprade puppet-agent on misc2

## 2019-06-25 

* 22:36 paladox: deleted CleavagesCwars from phabricator (per email)
* 18:29 paladox: apt-get install nginx postfix postfix-sqlite puppet-agent rsync tzdata unzip on elasticsearch1
* 16:51 paladox: running forceSearchIndex.php for buswiki
* 16:50 paladox: running updateSearchIndexConfig.php for buswiki
* 12:30 paladox: [13:22:19] <+paladox>	!log restart mysql on db4

## 2019-06-24 

* 13:14 Southparkfan: install sysbench on mw3
* 13:07 Southparkfan: install sysbench on db4

## 2019-06-23 

* 13:32 paladox: running lc on mw*

## 2019-06-22 

* 20:50 paladox: (before the last log, i removed all site maps so that i could generate fresh ones)
* 20:44 paladox: running generateMirahezeSitemap.php on mw1
* 16:06 Reception123: purge binary logs before '2019-06-22 12:00:00';
* 15:21 paladox: repool mw2
* 15:20 paladox: depooled mw2 && restarted php-fpm
* 15:19 paladox: killed puppet process on mw2

## 2019-06-21 

* 16:50 paladox: ran lc on mw*
* 16:45 paladox: reboot cp3
* 16:44 paladox: also upgrading kernel on cp3
* 16:43 paladox: apt-get upgrade on cp3
* 16:39 paladox: upgrade nginx to 1.16 on cp2
* 16:39 paladox: downgrade nginx to 1.16 on misc1
* 16:38 paladox: upgrade puppet-agent on cp2 and misc1
* 16:35 paladox: upgrade nginx to 1.16 on cp4
* 16:33 paladox: downgrade nginx on misc4 to 1.16
* 16:27 paladox: repool mw1
* 16:23 paladox: downgrading nginx to 1.16 on mw1
* 16:23 paladox: depool mw1
* 16:23 paladox: repool mw3
* 16:18 paladox: downgrading nginx to 1.16 on mw3
* 16:18 paladox: depool mw3
* 16:17 paladox: downgrading nginx to 1.16 on misc2
* 16:16 paladox: repool mw2
* 16:14 paladox: downgrading nginx to 1.16 on mw2
* 16:08 paladox: depool mw2
* 16:03 paladox: repool mw2
* 15:49 paladox: reboot mw2
* 15:48 paladox: depooled mw2 for reboot
* 15:37 paladox: killing a D state nginx process on mw2
* 15:29 paladox: enabling categorytree for all wikis
* 13:13 paladox: drop table searchindex for isvwiki
* 13:09 paladox: running forceSearchIndex.php for isvwiki - T4479
* 13:01 paladox: running updateSearchIndexConfig.php for isvwiki - T4479
* 00:37 paladox: repool mw3
* 00:36 paladox: upgrade firefox-esr on mw3
* 00:31 paladox: reboot mw3 (as there is a proccess in D state, but it's not shown long enough for me to kill it)
* 00:18 paladox: stopped nginx on mw3 && disabled puppet
* 00:14 paladox: depool mw3
* 00:09 paladox: update cw_wikis set wiki_settings = REPLACE(wiki_settings, '"wgRottenLinksCurlTimeout":"30"', '"wgRottenLinksCurlTimeout":"10"');

## 2019-06-20 

* 23:45 paladox: killed some updateExternalLinks.php pids to reduce load on mw3

## 2019-06-19 

* 18:14 paladox: upgrade puppet-agent on mw*
* 18:09 paladox: upgrade puppet-agent on cp4 && apt-get upgraon puppet1
* 16:25 paladox: apt-get upgrade on test1

## 2019-06-18 

* 06:38 Reception123: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki loginwiki on mw*

## 2019-06-17 

* 22:44 John: removed binary logs on db4
* 15:28 paladox: salt -E "mw.*" cmd.run "rm -rf /srv/mediawiki/w/cache/managewiki/**"
* 13:43 paladox: just to note that i re enabled blogpage on amazingyoutuberswiki through MW
* 13:42 paladox: disable blogpage on amazingyoutuberswiki (temp)
* 03:48 paladox: ran PIIRemoval.php (enforcing ToU) (again)
* 03:48 paladox: ran PIIRemoval.php (enforcing ToU)

## 2019-06-16 

* 20:08 paladox: upgrade phabricator on misc4
* 19:51 paladox: UPDATE mw_permissions SET perm_permissions = REPLACE(perm_permissions, "read", "") WHERE perm_group = "*"; on db4 (1525 rows updated)
* 19:36 paladox: delete from mw_permissions where perm_group = '\'*\*; on db4
* 19:34 paladox: delete from mw_permissions where perm_group = '"*"'; on db4
* 19:32 paladox: /usr/bin/nice -19 /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/extensions/ManageWiki/maintenance/modifyGroupPermission.php --removeperms=read \"*\" (mw1)
* 19:32 paladox: delete from mw_permissions where perm_group = 'modifyGroupPermission.php'; on db4
* 19:26 paladox: running /usr/bin/nice -19 /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/extensions/ManageWiki/maintenance/modifyGroupPermission.php --removeperms=read '*' (mw1)
* 19:24 paladox: remove read from horridreceptionwikiswiki
* 05:57 Reception123: running wikibackups (./wikibackups.sh /home/reception/allpublic.dblist /srv/mediawiki/w/maintenance/dumpBackup.php)
* 03:08 paladox: running lc on mw* and test1
* 02:52 paladox: due to out of space on db4
* 02:52 paladox: <+paladox>	!log restarted mysql (at 03:43 bst)

## 2019-06-14 

* 16:44 paladox: restart prometheus-node-exporter on misc2
* 16:42 paladox: kill puppet on misc2
* 14:08 paladox: removing gluster and installing ceph on test1
* 10:38 Reception123: root@mw1:/home/paladox# rm allthetropeswiki.xml.gz (restart dump with current revs)
* 10:37 Reception123: reception@mw1:/mnt/mediawiki-static/dumps$ sudo -u www-data php /srv/mediawiki/w/maintenance/dumpBackup.php --wiki allthetropeswiki --current --output gzip:/mnt/mediawiki-static/dumps/allthetropes14062019.xml.gz (restart dump without full rev)
* 00:20 paladox: installing gluster on test1

## 2019-06-13 

* 22:49 paladox: root@test1:/home/reception# rm -rf wikibackups
* 22:21 paladox: running forceSearchIndex.php for pointmanwiki
* 22:20 paladox: running updateSearchIndexConfig.php for pointmanwiki
* 17:48 Reception123: reception@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php deleteBatch.php --wiki sdiywiki --r="Deletion of pages in Category:CGS Serge kit image" --u="Reception123" /home/reception/sdiy-pages-delete.txt
* 01:04 paladox: running dumpBackup.php for allthetropes (on mw1)

## 2019-06-11 

* 23:22 paladox: ALTER TABLE mw_permissions CONVERT TO CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;
* 23:22 paladox: ALTER TABLE cw_wikis CONVERT TO CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;
* 22:54 paladox: repool mw1
* 22:49 paladox: depooling mw1
* 00:33 paladox: remove newusopediawiki-namespaces.cdb on mw*
* 00:28 paladox: running ALTER TABLE mw_namespaces CONVERT TO CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci; on db4

## 2019-06-10 

* 22:02 paladox: upgrade dirmngr gnupg gnupg-agent gpgv libc-bin libc-l10n libc6 libc6-dbg libcups2 on db4
* 21:59 paladox: upgrade base-files on db4

## 2019-06-08 

* 20:16 paladox: recreating amenthesprojectwiki
* 17:19 paladox: running lc on mw*
* 15:28 paladox: upgrading test1 to mw 1.33
* 13:31 paladox: update cw_wikis set wiki_locked = 0 where wiki_locked = 1 and wiki_dbname = 'metawiki';

## 2019-06-07 

* 22:25 paladox: branching REL1_33

## 2019-06-06 

* 23:38 paladox: repool mw3
* 23:34 paladox: also running lc on mw*
* 23:34 paladox: depool mw3 or a mw upgrade
* 23:34 paladox: repool mw2
* 23:31 paladox: depool mw2 or a mw upgrade
* 23:30 paladox: repool mw1
* 23:27 paladox: depool mw1 or a mw upgrade
* 16:47 paladox: running lc on test1, mw*
* 15:45 paladox: apt-get install dns-root-data grafana python3-cryptography rsync tzdata unzip postfix postfix-pcre postfix-sqlite publicsuffix python-cryptography libjs-jquery - misc1
* 15:44 paladox: apt-get install nginx mariadb-client mariadb-client-10.1 mariadb-client-core-10.1 mariadb-common - misc1
* 13:29 paladox: repool mw1
* 13:29 paladox: upgrade php-redis to 4.3 on mw*
* 13:24 paladox: rebooting mw1
* 13:18 paladox: depool mw1
* 00:15 paladox: installing openvpn on puppet1

## 2019-06-05 

* 19:13 paladox: sudo apt-get install devscripts fakeroot on test1
* 16:50 paladox: reset /srv/mediawiki/config on test1 (merge conflicts)
* 01:36 paladox: installing netcat on test1

## 2019-06-04 

* 23:08 paladox: installing strongswan on test1 following [https://www.digitalocean.com/community/tutorials/how-to-set-up-an-ikev2-vpn-server-with-strongswan-on-ubuntu-16-04](https://www.digitalocean.com/community/tutorials/how-to-set-up-an-ikev2-vpn-server-with-strongswan-on-ubuntu-16-04)
* 18:37 paladox: running rebuildall.php for quircwiki on mw1

## 2019-06-03 

* 22:19 paladox: starting more imports for quircwiki
* 21:46 paladox: hacking Redis.php on mw1 to disable redis if using cli
* 21:44 paladox: compressing quircwiki wiki

## 2019-06-02 

* 19:59 paladox: running lc on mw*

## 2019-06-01 

* 23:20 paladox: upgrade a few minor packages on bacula1
* 23:19 paladox: delete backups on bacula (for them to have a full backup in ~40mins)
* 16:36 Reception123: disabled OATHAuth for Eduaddad (php disableOATHAuthForUser.php "Eduaddad" --wiki metawiki)
* 15:11 paladox: mkdir /tmp on db4 at 14:46
* 05:35 Reception123: purge binary logs before '2019-05-31 12:00:00';
* 05:33 Reception123: removed /tmp on db4
* 00:23 paladox: upgraded vpncloud to 1.0 accross all hosts

## 2019-05-31 

* 15:40 paladox: upgrade php, nginx and nodejs on misc4
* 15:38 paladox: upgrade php on misc2
* 15:06 paladox: repool mw3
* 15:00 paladox: upgrade packages on mw3
* 14:58 paladox: depool mw3
* 14:58 paladox: repool mw2
* 14:53 paladox: upgrading some packages on mw1/mw2
* 14:53 paladox: upgrade  postfix postfix-sqlite python-cryptography python-pip python-pip-whl python3-cryptography on mw1
* 14:52 paladox: upgrade apt-get install  postfix postfix-sqlite python-cryptography python-pip python-pip-whl python3-cryptography on mw2
* 14:51 paladox: upgrade samba-common samba-common-bin samba-libs smbclient tzdata on  mw2
* 14:49 paladox: upgrade libmagickcore-6.q16-3 libmagickcore-6.q16-3-extra libmagickwand-6.q16-3 on mw2
* 14:47 paladox: upgrade nginx on mw2
* 14:46 paladox: upgrade php7.2-common php7.3-common unzip imagemagick imagemagick-6-common imagemagick-6.q16 puppet-agent on mw2
* 14:45 paladox: depool mw2
* 14:44 paladox: repool mw1
* 14:43 paladox: upgrade ffmpeg
* 14:42 paladox: upgrade unzip on mw1
* 14:39 paladox: upgrade nginx from 1.15 to 1.17 on mw1
* 14:34 paladox: upgrading php to 7.2.19 on mw1
* 14:27 paladox: depool mw1
* 06:36 Reception123: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki loginwiki on mw*

## 2019-05-30 

* 02:43 paladox: running lc on mw*

## 2019-05-29 

* 22:17 paladox: upgraded phabricator - T4426
* 14:53 paladox: remove ip
* 13:26 paladox: remove email from a user per ToU

## 2019-05-28 

* 00:53 paladox: created empty commonswikiwiki db on db4

## 2019-05-27 

* 23:29 John: created "Anse1997_tries_again" on several wikis
* 20:11 paladox: upgrade grafana to 6.2.1
* 20:10 paladox: upgrade icinga2 to 2.10.5
* 20:10 paladox: rebooting misc1 to enable TUN
* 19:46 paladox: rename commonswikiwiki to commonswiki

## 2019-05-26 

* 13:13 paladox: rm -rf /srv/mediawiki/w/cache/managewiki/** on mw*
* 13:12 paladox: ran update mw_permissions set perm_removegroupsfromself = '[]' where perm_removegroupsfromself = *
**on db4**

* 13:10 paladox: ran update mw_permissions set perm_addgroupstoself = '[]' where perm_addgroupstoself =*; on db4

## 2019-05-25 

* 15:02 paladox: upgrade phabricator

## 2019-05-24 

* 22:40 paladox: starting import for quircwiki
* 17:41 paladox: remove hack from /srv/mediawiki/config on mw1
* 17:41 paladox: remove hack from /srv/mediawiki/w on mw1
* 17:04 paladox: restore reports 1-11 from a backup
* 17:03 paladox: dropping incidents reports 1-11 in the incidents table (restoring from a backup shortly)
* 13:07 paladox: rebooting mw3 to replace lizardfs mount point
* 12:27 paladox: remove blogpage from besttvshowswiki - T4411
* 02:08 paladox: running rebuildall.php and initSiteStats.php for thelastsovereignwiki
* 02:07 paladox: running rebuildall.php and initSiteStats.php for trollpastawiki
* 02:05 paladox: running rebuildall.php and initSiteStats.php for animatedfeetwiki
* 02:05 paladox: running rebuildall.php and initSiteStats.php for animebathswiki
* 01:19 paladox: running lc on mw*

## 2019-05-23 

* 23:44 paladox: starting import for americangirldollswiki - T4384
* 23:33 Southparkfan: ran userdel on mw*/puppet1 per f19fe61a9321b95bdef730e0aeff30102b4f2ca7
* 22:57 Southparkfan: deleted user account 'macfan' on mail server
* 18:18 paladox: running populateGroupPermissionsWithDefaults.php for all wikis (will only effect new wikis created since the 5th of may)
* 17:47 paladox: dropping cdb cache for all wikis
* 17:46 paladox: dropping mw_permissions to restore from backup - T4405
* 16:55 paladox: dropped wikicreator && updated proxybot to drop centralauth-lock and globalblock
* 16:45 paladox: INSERT INTO mw_permissions (perm_dbname, perm_group, perm_permissions, perm_addgroups, perm_removegroups, perm_addgroupstoself, perm_removegroupsfromself, perm_autopromote) VALUES ('metawiki', 'wikicreator', '["createwiki"]', '[]', '[]', '[]', '[]', NULL);
* 16:38 paladox: granting editsitecss, editsitejson and editsitejs to sysop for all wikis
* 16:10 paladox: granting editsitecss, editsitejson and editsitejs to sysop through ManageWikiDefaultPermissions
* 12:29 paladox: rebooting test1
* 01:46 paladox: install mariadb-server on test1 to test restoring backups.

## 2019-05-22 

* 23:47 paladox: rm -rf /srv/mediawiki/w/cache/managewiki/** on mw*
* 18:33 MacFan4000: DELETE FROM mw_permissions WHERE perm_dbname='metawiki' AND perm_group='comentadmin';
* 18:31 MacFan4000: DELETE FROM mw_permissions WHERE perm_dbname='metawiki' AND perm_group='chatmod';
* 18:30 MacFan4000: DELETE FROM mw_permissions WHERE perm_dbname='metawiki' AND perm_group='forumadmin';

## 2019-05-21 

* 16:09 John: fix db values for content_model
* 00:39 MacFan4000: UPDATE cw_requests SET cw_status = 'declined' WHERE cw_id = '8135';
* 00:30 paladox: running lc on mw3
* 00:29 paladox: running lc on mw2
* 00:28 paladox: running lc on mw1

## 2019-05-20 

* 21:01 paladox: running rebuildall.php for scruffywiki

## 2019-05-19 

* 21:35 paladox: drop popnmusicwiki database - T4380
* 13:33 paladox: running rebuildall for thelastsovereignwiki

## 2019-05-18 

* 23:07 paladox: disabled puppet on mw1 at 23:38 bst time to prevent cert problems.
* 21:01 paladox: stopped mirahezerenewssl
* 16:12 paladox: upgrading phabricator on misc4
* 15:17 paladox: starting import for animebathswiki on mw1 - T4294
* 15:08 paladox: starting import for thelastsovereignwiki on mw1 - T4362
* 03:28 John: UPDATE cw_requests SET cw_status = "approved" WHERE cw_id = 8106;

## 2019-05-17 

* 22:45 paladox: started import for wiki hispanowiki - T4378
* 17:40 paladox: disable blogpage on atrociousdeviantswiki, extension requires voteny to be installed first
* 17:11 paladox: upgrade puppetdb to 6.3.2 and puppet-agent to 6.4.2 on puppet1
* 16:00 paladox: enabled UniversalLanguageSelector on metawiki

## 2019-05-16 

* 00:09 John: running conversion from LS->DB for new ManageWikiNamespacesAdditional stuff

## 2019-05-15 

* 22:22 John: ALTER TABLE mw_namespaces ADD COLUMN ns_additional LONGTEXT AFTER ns_core;
* 21:05 MacFan4000: DELETE FROM echo_unread_wikis WHERE euw_user = '9736'; (metawiki)
* 16:20 paladox: renamed Ucronistaw  to Hispano76 in phabricator

## 2019-05-12 

* 22:33 paladox: disable blogpage on flawlessfandomuserswiki - T4361

## 2019-05-11 

* 14:13 paladox: killing the mw cache on mw*
* 14:13 paladox: update mw_permissions set perm_addgroups = '[]' where perm_addgroups = 'null'; on db4 (13 entries updated)
* 14:12 paladox: update mw_permissions set perm_removegroups = '[]' where perm_removegroups = 'null'; on db4 (13 entries updated)
* 14:11 paladox: update mw_permissions set perm_addgroupstoself = '[]' where perm_addgroupstoself = 'null'; on db4 (94 entries updated)
* 14:11 paladox: update mw_permissions set perm_removegroupsfromself = '[]' where perm_removegroupsfromself = 'null'; on db4 (94 entries updated)
* 14:00 paladox: upgrade php-igbinary on mw1
* 13:59 paladox: upgrade certbot and python3-certbot on mw1
* 13:58 paladox: upgrade imagemagick imagemagick-6-common imagemagick-6.q16 puppet-agent  on mw1
* 13:57 paladox: upgrade puppet-agent  imagemagick-6.q16  imagemagick on mw3
* 13:56 paladox: repool mw3
* 13:54 paladox: depool and upgrade mw3 php7.2 to php 7.2.18
* 13:52 paladox: repool mw2
* 13:50 paladox: depool and upgrade mw2 php7.2 to php 7.2.18
* 13:48 paladox: repool mw1
* 13:40 paladox: depool mw1
* 13:30 paladox: upgrade php7.2 to 7.2.18 on mw1
* 10:19 John: purged all permissions entries
* 10:19 John: DELETE FROM mw_permissions WHERE perm_group = 'oversight';

## 2019-05-10 

* 22:45 paladox: updating some packages on cp4
* 22:17 paladox: hacking User.php on mw1
* 21:48 Southparkfan: removed 'citoid' extension from mar9122wiki - T4356
* 00:00 paladox: running lc on mw*

## 2019-05-09 

* 23:10 paladox: hacking Redis.php to disable job stuff if using cli (so that imports work)
* 22:36 paladox: running lc on mw*
* 21:56 John: deleted some $wiki-permissions.cdb files to trigger rehashes
* 21:54 John: UPDATE mw_permissions SET perm_autopromote = NULL WHERE perm_autopromote = 'null';
* 15:46 John:  UPDATE mw_permissions SET perm_autopromote = '["&",[1,10],[2,345600]]' WHERE perm_autopromote IS NULL AND perm_group = "autoconfirmed";
* 15:45 John:  UPDATE mw_permissions SET perm_removegroupsfromself = '[]' WHERE perm_removegroupsfromself = *
****

* 15:45 John: UPDATE mw_permissions SET perm_addgroupstoself = '[]' WHERE perm_addgroupstoself =*;
* 13:40 paladox: starting import for trollpastawiki - T4215
* 13:39 paladox: compressed trollpastawiki

## 2019-05-07 

* 16:18 paladox: ban bch.miraheze.org from varnish - T4350

## 2019-05-05 

* 23:10 paladox: running lc on mw*
* 15:25 paladox: restoring wiki's file storage
* 15:09 paladox: stopping LizardFS backup so that the restore of some wiki's file storage can be done
* 00:05 paladox: repooling mw2

## 2019-05-04 

* 23:57 paladox: depool mw2 (and downtime for 15 minutes)
* 23:56 paladox: repool mw1
* 23:49 paladox: depool mw1
* 23:47 paladox: switch on TUN on misc4 - T4346
* 23:45 paladox: switch on TUN on ns1 - T4346
* 23:44 paladox: switch on TUN on puppet1 - T4346
* 23:43 paladox: remove cargo from misc1
* 23:15 Southparkfan: delete firewall rules on cp4/test1/db4/elasticsearch1 related to vpncloud port
* 23:10 paladox: installing cargo on misc1
* 22:52 paladox: removed temp firewall rule
* 22:45 paladox: allowing 10.0.1.1 to acccess port 9200 temporarily on elasticsearch1
* 22:05 Southparkfan: vpncloud refuses to work on elasticsearch, possible container/node issue, opened ticket #158843
* 21:50 Southparkfan: graceful elasticsearch, attempting to re-enable TUN/TAP
* 21:13 Southparkfan: killed old RottenLinks processes on mw3 (ps aux | grep RottenLinks | grep -E '(Apr|May)' | awk '{print $2}' | sudo xargs kill)
* 14:43 paladox: running lc on mw*
* 12:33 Reception123: actually undelete test1wiki (forgot *)
* 05:12 Reception123: running wikibackups (./wikibackups.sh /home/reception/allpublic.dblist /srv/mediawiki/w/maintenance/dumpBackup.php)
* 05:11 Reception123: UPDATE cw_wikis SET wiki_deleted = 0 WHERE wiki_dbname = "test1wiki";

## 2019-05-03 

* 23:36 paladox: running lc on mw*
* 23:27 paladox: rm -rf /srv/mediawiki/w/cache/managewiki/** on all mw* using salt
* 23:20 paladox: running import for liveactionfeetwiki - T4323
* 20:06 paladox: restart php7.2-fpm on mw1 due to "Resource temporarily unavailable"
* 19:17 paladox: restoring files for thecscwiki from backup

## 2019-05-02 

* 21:53 paladox: restarting lizardfs-master on misc3 after deploying [https://git.io/fjZhE](https://git.io/fjZhE)
* 16:57 paladox: changing phabricator.serious-business to true in phab's ui

## 2019-05-01 

* 20:51 paladox: live hacking core/CronArchive.php on misc2
* 16:45 paladox: disable puppet on lizardfs[1-3]
* 16:17 paladox: restoring file storage for zendariwiki, toxicfandomsandhatedomswiki, digimonwiki and testwiki
* 00:43 paladox: restarting lizardfs-chunkserver on lizardfs1
* 00:43 paladox: restarting lizardfs-chunkserver on lizardfs2
* 00:41 paladox: restarting lizardfs-chunkserver on lizardfs3
* 00:35 paladox: restarting lizardfs-master on misc3
* 00:09 John: ALTER TABLE cw_wikis MODIFY COLUMN wiki_creation BINARY(14) NOT NULL, MODIFY COLUMN wiki_private TINYINT NOT NULL;
* 00:07 John: set wiki_creation for digimonwiki, heistwiki and macfan4000wiki using first recorded entry in logging tables
* 00:06 paladox: running core:archive --force-all-websites on misc2 (for matomo)
* 00:04 John: set wiki_creation for addawiki, bigforestwiki, hypopediawiki, omniversaliswiki, podpediawiki, r2wiki, unpediawiki, vukufwiki from metawiki log history

## 2019-04-30 

* 23:46 John: noting that is to bring things more inline with what they should be. Code changes will follow eventually of course. Wanting to change wiki_creation but late introduction means 11 rows have NULL as value which shouldn't happen. Will either fix or dummy set their dates
* 23:45 John: ALTER TABLE cw_wikis MODIFY COLUMN wiki_closed TINYINT NOT NULL DEFAULT 0, MODIFY COLUMN wiki_inactive TINYINT NOT NULL DEFAULT 0;
* 22:41 paladox: deleting rpwiki ructionarywiki rumechguidewiki russopediawiki rwbyrpwikiwiki rwmdwiki rxywiki ryokutowiki sabbakawiki sadereawiki saharinspacewiki sambokitwiki sandvallangswiki sanmaronwiki satbirsoniwiki sau226wiki sbcgamingwiki sbinfinitywiki scamafriwebwiki scambaitingwiki scannotwiki schafschuetzenwiki schicksalswikiwiki schulwiki (per dormancy policy)
* 22:38 paladox: deleting schupiewiktionarywiki scientiawikiwiki scottwatsonwiki scoutswiki seagullwiki seahorsewiki searchingdiligentlywiki senlawiki senpagawiki sensonewiki serinfhospwiki serviceshiftwiki sfwarehousewiki sgmbwiki sgswiki shadowrunwiki sharingcvwiki shatteredpodcastwiki shatteredworldwiki shefwiki shirinnoeiwiki shortwikiwiki shosumosuwiki silentsunwiki sinwikiwiki sirikotwiki sitraduwiki sivzachwiki sixa503wiki skepticwikiwiki skkdoccwiki skydivingwiki skyfleetwiki sladewatkinswiki slaynetworkwiki sm64orgwiki smartphoneswiki smartwiki smashbroslawlwiki smoswiki snizhwiki snowthegamewiki (per dormancy policy)
* 22:36 paladox: deleting soaitwiki sofoziacnowiki softwarewiki sonsofamericamodwiki sonsofamericawiki sophosdeloswiki sorilliawiki soundboardwiki spiritualitywiki splatvgwiki splunkwiki spoonerwiki sprachkurs20wiki sptrwiki sql4rmwiki sqlite4rmwiki sstournamentstestwiki staffr0xwiki startcrowdwiki startungwiki stavenheimwiki stellawiki stelscapewiki stepediawiki sterlzwikiwiki stjohannisharvestehudewiki stormerswiki storycarpwiki stpeterseasternhillchoirwiki strategy2executionwiki strathacewiki streetwiki studentcenterwiki studingwiki suave101wiki sufwiki suginamisannekiwiki summerhousewiki sunchildwiki (per dormancy policy)
* 22:34 paladox: deleting sunserferswiki sunsetwiki supercrewwiki superhospitalwiki supernamuwiki survivalerawiki sweetjissousekiwiki synthpediawiki syntopiwikiwiki sysadminwiki systemdafricawiki tabithareeveswiki takeittothevetwiki takethatwikiwiki talkingtomandfriendswiki tangotextewiki tarovisionwiki taxiantwiki taylorswift13wiki team13wiki teammontmartrebpwiki techpredwiki tecnologiaseducacaowiki tekkenwiki teknowiki telegrambotswiki templeofdivinitywiki tenlosssyndicatewiki tenniselbowwiki tensorflowglossarywiki terrafractumwiki terredelsolewiki tescommunitywiki testdelete7wiki (per dormancy policy)
* 22:33 paladox: deleting testingnewsandtranslatedontenterwiki teswiki tetracommunwiki textbookwiki tfwikiswiki thax39wiki theamazingworldofgumballwiki theanimationwikiwiki theavatararenawiki theavatarchronicleswiki thebluecafewiki thedarkworldwiki thedistancewiki thedominancewiki theedishwiki thenozomiwiki therifterwiki theshookwiki thesimswiki thesimulatorwiki thewildawaitswiki theworldwithinwiki thireswiki thrivingwiki thunderwiki tik2018wiki titaniawiki togettoknowhumanswiki toljsewiki toolkitcitiengovwiki toonpediawiki totalfreedomwikiwiki totcwiki tourbasewiki tpgwiki (per dormancy policy)
* 22:31 paladox: deleting tradingmexwiki trafficresearchwiki tramswiki transparencyguidewiki travauxlibwiki travelguidewiki treelivewiki trexwiki tribulabwiki triseptsolutionswiki trnixwiki tswikiwiki tumodulewiki tunisianwiki tutorielwikiwiki twopairsofgreyeyeswiki twrailwaypediawiki txfrmrwiki tzbookwiki ucietestwiki uclalinuxwiki udcmwiki uefagameplaywiki ufprformulawiki undertaleorisitwiki unibielefeldenactuswiki unichwiki unicornswiki universepediawiki unixtlfwiki unknownchronicleswiki unknownlandswiki unmusicfestivalwiki unoitudowiki unoiwiki uoluwiki (per dormancy policy)
* 22:28 paladox: deleting upcarquitecturadesoftwarewiki urbexwiki usopediawiki usuniwikiwiki utasmotorsportswiki utopiaewikiwiki uwlexperiencewiki uwlinternationalwiki uzeruswiki vaistrawiki valkohwiki vandalwiki vandatechwiki vasardenwiki vawtwiki veerawiki venturewiki veraciawikiwiki verhalenwiki verrahwiki vertaistuotantowiki vestedgameswiki viewpediawiki virtualfrenchwiki vlierhofwiki vndbreviewwiki voiceactivatedwiki voidbornewiki vostarwiki voxpopuliwiki vtagwiki vtkwiki (per dormancy policy)
* 22:26 paladox: deleting vtwiki wanselinwiki warondestinywiki warriorsfanguidewiki waywardwiki wbsfisiwiki wbswikiwiki weakypidiawiki wearyourdictionarywiki weatherwikiwiki weefeewillwiki weichgewebstumorenwiki wellawiki wepwikiwiki whartonprojectwiki wholemindhealthwiki whufcyouthwiki whysowiki wiki wikiageingwiki wikiajbwiki wikibakawiki wikibiblewiki wikibregiswiki wikiclinicwiki wikicombowiki wikicristianowiki wikigallerywiki wikigreenwiki wikigwiki wikihamaareewiki wikihousewiki wikimaenwiki wikimoviewiki wikinationswiki (per dormancy policy)
* 22:25 paladox: deleting wikioftextwiki wikipandawiki wikipediabiaswiki wikiptminerswiki wikiswiki wikitestwiki wikitransparencywiki wikiturawiki wikiwebwiki wikiwiki willwiki willyleewiki windhambomberswiki windowswiki winnipegwikiwiki wirtschaftsinformatikhbswiki wisdomwiki wizcopycatwiki woodallscookwiki woorilindywiki workinprogresswiki worldcontestwiki wtfjhtwiki wvscwiki xavipwiki xelestialwiki xenharmonicwiki xrpwikiwiki xuniversewiki yacresourceswiki yaguwiki yamawiki yatesmillwiki yherchianwiki yikipediawiki yourbuddywiki yourkickstartersuckswiki yuuyuuwiki zerononcensewiki zitabiteswiki (per dormancy policy)
* 22:23 paladox: deleting rasamrutawiki rastr11wiki rdfwiki rebolngwiki redealternativowiki redworldwiki renecassinwiki renessenceswiki requiemwiki researchadwaywadekarwiki residentbrasilwiki resiwikiunicapwiki resiwikiwiki resonancewiki retailwiki retrofuturism1950wiki retrospectivefacilitatorgatheringwiki reversemediawiki reversewiki richardswiki richardyan314wiki rico9wiki rikimaruwiki riseofthechosenwiki risonwiki roadtrip2018wiki robertsnoteswiki roguesgallerywiki rollerderbylillewiki ronito030wiki roschfallenwiki rotaractorwikiwiki royalquestplwiki rpcauthoritywiki rpgwiki rpgzinzinswiki (per dormancy policy)
* 22:21 paladox: deleting pokesurvivorwiki polishmyfanworldwiki pomopediawiki popteamepicwiki postscriptumhungarywiki poswiki ppfwiki praxeumwiki prg2018wiki primesportwiki prinyawiki processwiki progress4parkwaywiki projectwilsonwiki promoinsidewiki propagandawiki protonwiki proxmoxhclwiki pruebamatesaraujowiki prumsamdywiki psc18wiki pscwiki pslwiki pti18wiki q3dwiki qhsewiki qissmathlabwiki qutlawnoteswiki rackdos777wiki rageofbahamutwiki rajsreenwiki raltseyewiki rambahadurbomjonwiki ramenpediawiki randomwiki (per dormancy policy)
* 22:19 paladox: deleting patternswiki paulsletterswiki pb2leveleditorwiki pb2stofwiki pcarchitectwiki pedrobritowiki pedrorenanwiki pengalewiki penjhorngwiki penwikiwiki pepisptestwiki permaguruwiki pessoalzywiki petctviewerwiki pfathaswiki pfgjaverianamswiki pfl2wiki phantomforceswiki pharmacywikiwiki phicompwiki philowiki philowikiwiki philteacherswiki phragmatawiki pinballwiki pispediawiki pitchwiki pixterwiki placesrobloxwiki pmavwiki podcastswiki poewikiwiki pokemondustwiki pokeonewiki (per dormancy policy)
* 22:17 paladox: deleting oncprojectwiki oneupcloudwiki openonderwijswiki opgetfundingwiki opiumchangwiki opmiwiki orelandswiki osapwiki oscwiki oshyewiki osintwiki ossiwiki otherworldwiki otimizewiki oultrecaramaniawiki outoriowiki overseasuwlwiki oxfordniwiki pactrackwiki palatiaswiki pamwiki panselmewiki panthertoonswiki paradiselodgewiki paranormalwiki parentswiki parliamentarydemocracywiki parvisregionwiki pattawiki (per dormancy policy)
* 22:16 paladox: deleting netapediawiki newalbionwiki newworldoriendwiki nghtwiki nicorewiki nicuwiki niggpediawiki nihilistenhymnewiki nlwikiwiki noahwikiwiki nomaliaswiki norskrapwiki nosqlwiki notbookwiki noteswiki novayawiki nowbuskingwiki nrkwiki nudelworldbuildingwiki numhwywiki nursewikiwiki nutritionwiki nutscriptclonewarswiki nvcowiki nvliuwiki nxwikiwiki nyohwikiwiki o3dpwiki oalandwiki oceanuswiki oecumenewiki officialgeosworldalpharchivewiki ogowiki okwiki omcwikiwiki omfaxsystemswiki (per dormancy policy)
* 22:14 paladox: deleting ms2987wiki mscyberprivacywiki msgilwiki msnhinet8testwiki msnhinet8wiki mspugwiki mtamasterswiki mtascripterswiki muktipediawiki mundanapediawiki mundepwiki mundissongcontestwiki murlidharwiki musgovwiki music101wiki musiccupwiki musicpediawiki musicwikiwiki musicworldgamewiki mvwiki mwpermtestwiki myao93wiki myclassprojectswiki mydevexperiencewiki mymoneywiki mynintendowiki mysummerholydayswiki n2gowiki nafetswiki nagygenitalorszagwiki namudatawiki nanotrixwiki natturkowiki navmedwiki nayan28589wiki nbss13wiki neoottomanwiki (per dormancy policy)
* 22:12 paladox: deleting medicowiki meditationwikiwiki megacorpwiki megavisionwiki memburyofficialwiki memorieswiki menageriewiki menschenrechtewiki mesturetwiki metalistwiki metodosnumericosunalmzlwiki mfcwiki mfscwiki michelleatallahwiki mightymeeplewiki mikipediawiki minewiki miningpromieswiki minnanpediawiki mirahezewiki miraiakariwikiwiki mirbalwiki mitihoneywellwiki mkwikiwiki moatwiki modellbahnwiki modelusgovwiki moosbachwiki mouziloarchiveswiki mpwiki mrmaywiki (per dormancy policy)
* 22:10 paladox: deleting lyricswiki madiklopediwiki mafiasocietywiki magipediawiki magnaorbiswiki magnoliahousewiki maidenheadroleplayingwiki maindotawiki mainlandsongcontestwiki makeiteasyautoswiki malabwiki mamsprawdzonewiki manawinstttwiki maralertwiki marconswiki marksteinwiki masariwiki mathteachwiki matomotestwiki mattlemon675wiki mattsworldbuildingwiki maztowikiwiki mbitswiki mcbejpwiki mcbscomm12wiki mckwiki meadowtrailwiki medehollinwiki medgwiki mediacultures1wiki mediamatikawiki mediawiki (per dormancy policy)
* 22:03 paladox: deleting libobasicwiki libreartwiki liffeywiki ligaleciwiki ligamxwiki lightningbugwiki limeydragonwiki linglotwiki litcircleswiki literaryfreedomwiki littletikeshackswiki liveandlawwiki livesnowmapwiki livingdeadmanwiki livwiki lmvmdnoteswiki lomewiki lonsichoeumwiki loopywiki lostminecraftminerswiki lovelivewiki lovetweakswiki lowwiki lucewiki lucklessfoolswiki lucunewiki luntarawiki luzenglishcornerwiki (per dormancy policy)
* 22:00 paladox: deleting korbowiki kotakmimpiwiki krebswiki kreuz9561wiki kscmwiki ktspatentprosecutionwiki kzhealthwiki lacroiseedescheminswiki laikanprojectwiki lambdapsikkywiki lambelwiki lamdlcaselistwiki lapoliticswiki larcencieldeghiswiki lasrwiki lastcrewwiki latywiki laugofwiki lawlibwiki lawlrainbowversewiki lazygtawiki legalmovieswiki leginawiki legitimatestrategywiki leparkingetage63wiki leuvensecommonswiki lexicwiki lfobwiki (per dormancy policy)
* 21:58 paladox: deleting jinjuwiki johntestwiki jonraswiki jordanpetersonwiki jourrougewiki jurisdictionswikiwiki jurrassicworldwiki justipediawiki jwjohnsojrwiki kaltawiki kalyandevelopersthrissurwiki kapuluanwiki kassaiwiki kastritislabwiki kasucudenwiki ketitawiki keyruswiki kfootballwiki kgbwiki kgdrankwiki khepwiki kithearawiki kittydogwiki kkunnawiki klimagruppewiki knoweldgebasewiki knowledgeboxwiki knowledgepediawiki koisomemomijiwiki (per dormancy policy)
* 21:57 paladox: deleting integr8wiki intelwiki intelymerwiki internetstateswiki intrabasewiki iridianwiki ironandrustwiki ironsagawiki isatwiki itautowiki itreewiki iveaghwiki iwgwiki j4fclanwiki jaaglwiki jaavierselfdocumentationwiki jackalbersonwikiwiki jacktanwiki jalproversewiki janitestwiki japanunivwiki javaforjuniorwiki jaydecuswiki jbpdiscordwiki jdjwiki jeunessewiki jgtextwiki jhalabwiki (per dormancy policy)
* 21:54 paladox: deleting hpfwiki hrwiki hugawiki huncityvisionsongcontestwiki hydrantwikiwiki ialadinwiki iansnotebookwiki idealsongcontestwiki identityvwiki ideowiki idobelievewiki idolmasterwiki idoxwiki iecmhwiki ifapmecp1wiki ifmwiki ihadwiki iibwiki iictestwiki iicwiki iitpwiki im2wiki imaginewiki imhowiki immoinvestwikiwiki improwikiwiki imwiki inactifswiki indiasimwiki infapomgrwiki infobasewiki informatiquewiki insightfulmindswiki (per dormancy policy)
* 21:52 paladox: deleting hanminwiki harrypotterwiki harveyfengwiki hawkingmysterywiki hawkvisionwiki haxballportugalwiki healthylivewiki heidelbergwiki helpmectfwiki henwikiwiki heritagewikiwiki hesperusartswiki hgwikiwiki hillfolkwiki hjorthwiki hkimgboardwiki hklaicharwiki hnrgwiki hobbieswiki hobbymewiki hofstragrammarwiki holidaymasterswiki hollowcrownwiki homeiotwiki homenetwiki hordeswiki hornewiki hossainelsafayetwiki hostmicrobewiki howtogradewiki (per dormancy policy)
* 21:50 paladox: deleting giladipediawiki gliesewiki globaldataconsortiumwiki gloopsandboxwiki glueckssammlerwiki glw35wiki gmdkoreanwiki godottutswiki goldenpalladinwiki gomalawiki gombergwiki goodcounselwiki goodwiki gospelstudieswiki govarchivewiki graidyardwiki graveswiki graymainewikiwiki greeklawswiki grevanwiki greyhawkwiki grovespacewiki gsdmafwiki gstvpcpdwiki gunsgirl2wikiwiki h1z1wikiwiki habbohangwiki haifawiki halaqawiki (per dormancy policy)
* 21:48 paladox: deleting freerunetwiki freevandalismwiki freewikiwiki frknuniversewiki fxwiki fyonwiki g8kwiki gaeaworldwiki galaxier38wiki gamdugwiki gamingwikiwiki garfieldroboticswiki gastronomiaromaneascawiki gctwikiwiki gecomwiki gemawiki geminizuniversecomwiki genesiswiki geodominuswiki geometrydashkrwiki gestionticswiki gettyfamilywiki gfernandezwiki ggwikiwiki giangiwiki gianroyalwiki gibsonwiki (per dormancy policy)
* 21:47 paladox: deleting exceliawiki eyrwiki factory4rndwiki fair0002wiki fakepaediawiki familiahornoswiki faretraitewiki ferferwiki fiberpediawiki financialfindswiki fingerprintwiki fisicawiki flamepediawiki flipnotewiki floogstarboundwiki fmbvwiki fnecwiki foolmaptoolboxwiki forexobbrasilwiki forexwiki fortnitewiki forwardbiaswiki foundationwiki fpvwiki fquestwiki franmagdlaenawiki freecollegeprojectwiki freedomrespectlogoswiki (per dormancy policy)
* 21:45 paladox: deleting enchantmentwiki enciclopediaposmodernawiki enexpomathwiki engineeringnoteswiki engstudiowiki ensemblemulhousewiki entmonwiki enwiki epimorfositpewiki erethwiki erothwiki erotipediawiki ertywiki esogeekswiki esrokuakawiki estoelwiki eswikitransparencywiki etatenvauclusewiki etheliawiki eturdayawiki evawiki everythingiknowwiki evotvwiki evozangtalwiki exampediawiki (per dormancy policy)
* 21:38 paladox: deleting dragonwarriorwiki drakawiki drones4allwiki drothwiki dsgroupwiki duatprojectwiki ducklingswiki durawiki dynaswiki dys31wiki eaberlinwiki earthianwiki ecegradswiki econhistgenealogywiki economicswiki ecoprospectorswiki ecoucherwiki edominationsptbrwiki educationalgamesv2wiki edugirowiki egyptlawwiki elarawiki electracoinwiki elementaladvwiki elgafferwiki embobadawiki emeralddawnwiki (per dormancy policy)
* 21:34 paladox: deleting deadleaguewiki deixacomigowiki dekoerwiki denasoftiowiki denasoftkbwiki denimonewiki designatedsurvivorwiki dev7nullwiki devexperiencedwiki didaprowiki digitaldesigntechwiki dijarawiki dimplexwiki disabledlifewiki discipleshipanonymouswiki discordvisionteamswiki disinstrucpediawiki dollywiki dominiumwiki domithiwiki donaldduckwiki donaldtrumpwikiwiki doubleatravelwiki drachenbergwiki dragalialostwiki (per dormancy policy)
* 21:32 paladox: deleting cpcwiki cpudevwiki crazybloxiantimeswiki credcowiki cryptobotswiki crystlejexwiki culturemappingwiki cunydh2018wiki curiousdreamswiki currentmusicwiki cwiki cyberiawiki cybertripwiki cyberweatherwiki cycleofbloodwiki cyrylwiki cywiki czelwiki dakhilcommunitywiki dancascirculareswiki dancerconcretedesignwiki dascwiki datarightswiki davidewiki dcinsidewiki (per dormancy policy)
* 21:21 paladox: deleting cmggcmwiki cmnhiwiki cnamewiki cocrevampmodwiki codeuinowiki codexwiki cognetikwiki cogversewiki coineli5wiki coinspectwiki colpittsdesignwiki coltldwiki comexitaliawiki commonswiki compartirwiki comradeswiki comsiswiki conversewiki coppercubewiki corepediawiki corporativetestewiki counterwikiwiki coxtiwiki (per dormancy policy)
* 21:19 paladox: deleting cbtswiki cchpcwiki cctestwiki cdcwiki cdsicwiki celiawiki cfcwiki cfpluswiki cfwiki chamberwiki changemakerswiki chaosrollwiki cheesewinewiki chemwiki chessypigwiki christianmusicwiki chtechwiki circlewiki citixxiwiki civcraftwiki cjwikiwiki ckcwiki classhangoutwiki classsoftwiki cloakcoinwiki clwwiki (per dormancy policy)
* 21:17 paladox: deleting brokenironwiki bsawikiwiki budawiki bugsigdbwiki buyanypartwiki byblopediawiki byfireandswordrpgwiki caes2wiki2ppiswiki caestaronwiki caltherawiki canailleswikiwiki cancelledgameswiki cancelledmovieswiki cannabisconcentrateswiki cantorijwiki capcyberwikiwiki cardmonsterswiki carmeltechwiki casebankwiki caswiki (per dormancy policy)
* 21:15 paladox: deleting bigbrothersimulatorwiki bikeshedwiki bildungwiki bimmanualwiki birdspediawiki biskwiki bitnetwiki bkdrumwiki blhawiki bloodclotwiki bloowikiwiki blueskyocgwiki bluewaywiki bnntalkwiki boardroomwiki bobbyshawwiki bobocharwiki bohwikiwiki bozemanstorybuilderswiki brasilnanzwiki briocheswiki (per dormancy policy)
* 21:12 paladox: deleting aumatwiki auriliawiki aussimwiki austnationalgamewiki automationlondonwiki automobilewikipediawiki avoronwiki awesomegameswikiwiki aymcommercewiki ayurjakewiki b1tcashwiki b1teswiki badwrigglerswiki barbarismwiki barbecubewiki bardacontinentwiki bataswiki bausudwikiwiki bbawiki bbsazwiki bcadharmaschoolwiki bdorpwiki behmodwiki bementlabwiki bernimpressionswiki berntoonswiki bettermovieswiki bhffedwiki bhimeswiki biastrackerwiki biblebeahkusuwiki bibliothecalucemwiki (per dormancy policy)
* 21:09 paladox: deleting apexpredatorwiki aposbgwiki apostoliswiki apowiki appdecatwiki appsecwikiwiki aptozwiki aratiswiki archerwiki aresteamwiki aresteamwikiwiki arizonancornerwiki arkorderwiki arma3frwiki arqibewiki artsycraftwiki arynwiki asheeshscratchwiki assemblingphysicswiki astoriinfwiki astrapediawiki atablswiki atemreichwiki (per dormancy policy)
* 21:06 paladox: deleting alacritysimwiki alaskapediawiki albustestwiki alewiki alfredwiki alhayarmaths6wiki alineowiki althistoriawiki althistorywiki alzestorswiki amarenawiki ambirtestwiki amielbrickellwiki amirampwiki amshalwiki andusanwiki animamondaywiki aniwotawikiwiki anomalieswiki ansiblewiki antropologiaargentinawiki (per dormancy policy)
* 20:45 paladox: deleting 10yearswiki 123sartawiki 690squadronwiki 8recommendswiki aa2022wiki abhirupghoshwiki accorderiewiki accountingwiki acordswiki acqintwiki acrotrendwiki actartletraswiki adamwiki adminbuswiki advisingwiki aerobristolwiki aeromwiki aescwiki aetheriawiki afterlifewiki agathachristiewiki ageofwormswiki airportsofwings900wiki aisgwiki aistudywiki wiki's (per dormancy policy)
* 20:28 Southparkfan: purged 16G of mysql binary logs
* 20:23 Southparkfan: removed parted package from db4
* 20:16 Southparkfan: install 'parted' on db4

## 2019-04-29 

* 19:13 paladox: restarting php7.2-fpm on mw1 (due to "Resource temporarily unavailable")
* 18:26 John: UPDATE mw_permissions SET perm_addgroupstoself = '[]' WHERE perm_addgroupstoself =*;
* 18:26 John:  UPDATE mw_permissions SET perm_removegroupsfromself = '[]' WHERE perm_removegroupsfromself = '';
* 18:19 John: DELETE FROM mw_permissions WHERE perm_group = "modifyGroupPermission.php";

## 2019-04-27 

* 23:16 paladox: removing read from * on all wiki's
* 22:43 paladox: rewording last log to state all wikis have "read" remove from user
* 22:40 paladox: running modifyGroupPermission.php on mw1 - removing all read perms from 'user' permission on all private wiki's
* 16:24 paladox: upgrade ns1 to debian 9.9
* 15:53 paladox: revoke read from user on the default table in mw_permissions
* 15:45 paladox: revoke read from * in default table in mw_permissions
* 15:08 paladox: revoke read from * on meiouandtaxeswiki
* 13:09 paladox: upgrade puppet1 to debian 9.9

## 2019-04-26 

* 22:06 paladox: disable automatically archiving from the web browser in matomo. (per recommendation, switching it to a cron)
* 21:54 paladox: running ./console core:purge-old-archive-data all on misc2
* 16:38 paladox: running ./console core:archive --url= [https://matomo.miraheze.org/](https://matomo.miraheze.org/) > ./test.log on misc2 (per settings recommendation)

## 2019-04-25 

* 14:39 paladox: upgrade icingaweb2 to 2.6.3 on misc1

## 2019-04-22 

* 23:51 paladox: restarted rc bot
* 20:51 John: fixed some malformed DB entries for perm_autopromote
* 18:26 John: UPDATE mw_permissions SET perm_autopromote = '["&",[1,10],[2,345600]]' WHERE perm_dbname = "default" AND perm_group = "autoconfirmed";
* 18:13 John: populating perm_autopromote on all wikis using a hack script
* 02:45 John: add self group management to groups via DB sql (very few uses apparently")

## 2019-04-21 

* 21:39 paladox: repooled mw2
* 21:35 paladox: depooled mw2 to reinstall php
* 16:44 paladox: running lc on mw*
* 15:38 John: UPDATE mw_permissions SET perm_removegroups = '[]' WHERE perm_removegroups = 'null';
* 15:38 John: UPDATE mw_permissions SET perm_addgroups = '[]' WHERE perm_addgroups = 'null';
* 14:18 paladox: upgraded some packages on mw2 (php-fpm, nodejs, nginx, systemd, wget and a few more)
* 14:17 paladox: upgraded some packages on mw1 (php-fpm, nodejs, nginx, systemd, wget and a few more)
* 14:16 paladox: upgraded some packages on mw3 (php-fpm, nodejs, nginx, systemd, wget and a few more)
* 13:21 paladox: running gdb for php (due to a segmentation fault)
* 13:20 paladox: installing gdb on mw2
* 01:09 paladox: update mw_permissions set perm_removegroups = '[]' where perm_removegroups like 'null%' on db4
* 01:09 paladox: update mw_permissions set perm_addgroups = '[]' where perm_addgroups like 'null%'; on db4

## 2019-04-20 

* 21:42 paladox: running lc on mw*
* 17:42 paladox: installing [https://apt.wikimedia.org/wikimedia/pool/main/t/trafficserver/trafficserver-experimental-plugins_8.0.3-1wm1_amd64.deb](https://apt.wikimedia.org/wikimedia/pool/main/t/trafficserver/trafficserver-experimental-plugins_8.0.3-1wm1_amd64.deb) on test1
* 17:42 paladox: apt-get install libcjose0  libjansson4  libmemcached11 libmemcachedutil2 -t stretch-backports on test1

## 2019-04-19 

* 23:32 paladox: stopping nginx on test1
* 22:54 paladox: apt-get --purge remove trafficserver on cp4 (installing trafficserver on test1 instead).
* 22:52 paladox: noting that i also "apt-get install libc++1 libc++abi1 libhwloc5 libluajit-5.1-2 libtcl8.6 libunwind8 libnuma1 libluajit-5.1-common libhwloc5 -t stretch-backports" required by trafficserver
* 22:49 paladox: installing trafficserver on cp4 to test (from [https://apt.wikimedia.org/wikimedia/pool/main/t/trafficserver/trafficserver_8.0.3-1wm1_amd64.deb](https://apt.wikimedia.org/wikimedia/pool/main/t/trafficserver/trafficserver_8.0.3-1wm1_amd64.deb))
* 21:19 paladox: upgrading puppetdb to 6.3.1 on puppet1
* 17:30 Southparkfan: remove sysbench package from cp4 (+db4, I also benchmarked db4)
* 17:26 paladox: restarted php-fpm and nginx on misc2
* 17:25 Southparkfan: install 'sysbench' on cp4
* 16:50 paladox: running lc on mw*

## 2019-04-18 

* 12:15 paladox: starting import for abysmalrobloxgameswiki on mw2
* 11:59 paladox: starting dump import for trollpastauncensoredwiki on mw2

## 2019-04-17 

* 21:31 John: set columns to be [] where null in the value in mw_permissions
* 20:18 paladox: renaming imperiuswiki to addawiki - T4296
* 17:54 paladox: chrown sotuhparkfan:mail for southparkfan in /var/mail/ on misc1 (matching the other files)
* 14:54 paladox: rolling out php-fpm tweeks
* 14:00 paladox: live hacking puppetmaster
* 13:39 paladox: disabling puppet on mw3 to test tweeking php-fpm using live traffic.
* 13:35 paladox: disabling puppet on mw2 to test tweeking php-fpm using live traffic.
* 13:02 paladox: disabling puppet on mw1 to test tweeking php-fpm using live traffic.
* 02:24 paladox: killed a long running puppet process causing higher cpu then normal on db4
* 00:47 paladox: removing cp5 from salt-master
* 00:45 paladox: restarting php-fpm on mw* (depooling each one as i restart)

## 2019-04-16 

* 19:50 paladox: rebuilding lc on mw*

## 2019-04-15 

* 21:57 John: verified domain ownership within GitHub

## 2019-04-13 

* 17:56 paladox: deleting user Micru on phabricator
* 16:42 paladox: update mw_permissions set perm_addgroups = '[]' where perm_addgroups like 'null%' and perm_dbname = 'shumikenwiki';
* 16:41 paladox: update mw_permissions set perm_removegroups = '[]' where perm_removegroups like 'null%' and perm_dbname = 'shumikenwiki';
* 16:39 paladox: update mw_permissions set perm_removegroups = '[]' where perm_removegroups like 'null%' and perm_dbname = 'anotheredenwiki';
* 16:39 paladox: update mw_permissions set perm_addgroups = '[]' where perm_addgroups like 'null%' and perm_dbname = 'anotheredenwiki';
* 15:47 paladox: grant "managewiki" right on kakukokkawiki again per T4278
* 01:18 paladox: re grant read to * for cristianopediawiki - T4274
* 01:12 paladox: remove perms cdb file from mw* (so it can be regenerated)
* 01:11 paladox: update mw_permissions set perm_addgroups = '[]' where perm_addgroups like 'null%';
* 01:11 paladox: update mw_permissions set perm_removegroups = '[]' where perm_removegroups like 'null%';
* 01:03 paladox: update mw_permissions set perm_removegroups = '[]' where perm_removegroups = null;
* 01:03 paladox: update mw_permissions set perm_addgroups = '[]' where perm_addgroups = null;

## 2019-04-12 

* 01:06 paladox: running lc on mw*

## 2019-04-11 

* 23:45 paladox: ran updateSpecialPages.php against nonciclopediawiki on mw1
* 20:04 paladox: running lc on mw*
* 02:30 paladox: upgraded phabricator on misc4 (hour and half ago)
* 00:26 paladox: generating image dump for mediatecawiki - T4261
* 00:26 paladox: generating image dump for holycrosswiki - T4262

## 2019-04-10 

* 17:22 paladox: running lc on mw*
* 15:15 paladox: generating image dump for electowiki

## 2019-04-09 

* 22:46 paladox: running lc on mw* and test1
* 22:40 paladox: applying data_dump.dumps_timestamp to all wikis through patch-dumps_timestamp.sql sql patch (on mw1)
* 05:40 Reception123: reception@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php importDump.php --wiki cristianopediawiki /home/reception/Wikipedia-20190409003230.xml
* 05:33 Reception123: RENAMED vocalharmonywiki to metafolkwiki

## 2019-04-07 

* 17:33 paladox: upgrade debian to 9.8 on cp2
* 17:26 paladox: update debian to 9.8 on cp4
* 16:44 paladox: restarted nginx on cp3, appeared to have not been serving traffic all day.

## 2019-04-06 

* 23:23 paladox: root@bacula1:/bacula/backup# rm * on bacula1
* 23:22 paladox: db4, phab static and private git backups
* 23:11 paladox: deleting static backups
* 22:19 paladox: restoring kurwowizjawiki files from bacula
* 22:08 paladox: ^^ for bacula1
* 22:08 paladox: adding temporarily swap boost (3gb)
* 18:40 paladox: adding delete-dump, generate-dump and view-dump rights to all wiki's (for sysop)
* 18:37 paladox: add delete-dump, generate-dump and view-dump rights to 'default' in mw_permissions
* 18:11 paladox: run lc on mw*
* 17:28 Reception123: DROPPED databases mentioned before
* 17:27 Reception123: delete from CW_WIKIS badgameswikiwiki and crappygameswikiwiki
* 16:29 paladox: deleted WANCache:* key from redis
* 05:49 Reception123: DROP DATABASE wikilandwiki
* 05:49 Reception123: deleted wikilandwiki from cw_wikis
* 05:46 Reception123: DROP DATABASE taotacwiki
* 05:45 Reception123: deleted taotacwiki from CW_WIKIS
* 01:54 paladox: reverted hacks on mw3

## 2019-04-05 

* 23:46 paladox: hacking change on mw3
* 22:28 paladox: upgrade elasticsearch nginx puppet-agent wget on elasticsearch1
* 22:28 paladox: upgrading grafana nginx puppet-agent wget on misc1
* 16:28 paladox: disabling blogpost temporarily on loathsomecharacterswiki
* 16:12 paladox: running lc on mw3
* 16:10 paladox: running lc on mw2
* 04:57 John: decom cp5

## 2019-04-04 

* 23:54 paladox: running lc on mw*
* 21:47 paladox: starting import for pseudocienciawiki
* 20:58 paladox: repool mw2
* 20:31 paladox: depool mw2
* 20:30 paladox: repool mw3
* 20:23 paladox: depool mw3
* 20:05 paladox: repool mw1
* 19:57 paladox: depool mw1

## 2019-03-31 

* 22:36 paladox: repool mw3
* 22:29 paladox: reboot mw3 to reduce ram consumption (almost OOM)
* 22:28 paladox: depool mw3
* 20:37 paladox: granting the rest of our mw extensions access to sonarcloud
* 20:27 paladox: authorising sonarcloud to read ManageWiki in github. (for finding vulns/bugs)
* 19:31 paladox: reverting prevous action
* 19:29 paladox: granting view-dump, generate-dump and delete-dump rights to sysops on metawiki
* 19:25 paladox: running lc on mw*
* 19:21 paladox: apply DataDump sql to all wiki
* 19:08 paladox: reboot misc4 due to high load
* 19:01 paladox: upgraded phabricator on misc4
* 14:56 paladox: upgrade puppet agent and salt on lizardfs* and misc3

## 2019-03-30 

* 01:19 paladox: importing xml dump on fapceowiki T4175
* 01:18 paladox: upgrade php 7.3 to 7.3.3 on mw1
* 01:09 paladox: rename metapediawiki to itpediawiki T4226
* 00:42 paladox: running lc on mw*

## 2019-03-28 

* 22:53 paladox: remove blogpost from hypopediawiki T4205
* 22:49 paladox: drop caputiawiki database
* 22:49 paladox: drop autombilepediawiki and zhautomobilepediawiki database.
* 22:48 paladox: drop iceriawiki database
* 22:38 paladox: starting import on animatedfeetwiki (mw1)
* 19:01 paladox: upgrading puppetdb to 6.3, puppet-agent to 6.4 and puppetserver to 6.3 on puppet1

## 2019-03-25 

* 21:17 MacFan4000: deleting iceriawiki, autombilepediawiki, zhautomobilepediawiki, caputiawiki

## 2019-03-24 

* 14:15 paladox: reboot puppet1
* 09:24 Reception123: reception@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php importDump.php --wiki neciklopediowiki /home/reception/Neciklopedio-20190306130123.xml

## 2019-03-23 

* 02:26 paladox: reinstalling postgresql on db4
* 02:02 paladox: dropping puppetdb db && recreating it
* 01:30 paladox: deleting misc1 from puppetdb && regenerating cert
* 01:18 paladox: temporarily stopping nginx on misc2
* 00:43 PuppyKun: (to bypass mime detection) php importImages.php --wiki concordancewiki /home/ndkilla/

## 2019-03-22 

* 14:17 paladox: rm -rf /srv/mediawiki/w/cache/managewiki/** as getting "Failed to generate additional resources using 'eval_generate': invalid byte sequence in UTF-8"
* 13:53 paladox: restart puppetserver

## 2019-03-19 

* 00:11 John: running hack script for Cargo move

## 2019-03-18 

* 22:23 John: set ns_content = 1 in defaults for ns_namespace_id = 0
* 17:48 paladox: restarting puppetserver && puppetdb on puppet1

## 2019-03-17 

* 19:53 paladox: reload lizardfs-master

## 2019-03-16 

* 22:09 paladox: deleted pokemonadventures wiki
* 19:29 paladox: re enable puppet on mw*
* 15:25 paladox: disabling puppet on mw*
* 14:36 paladox: drop table searchindex on allthetropes wiki
* 01:35 PuppyKun: changed the mail password for ndkilla (yes again)

## 2019-03-15 

* 01:54 paladox: set manage_etc_hosts to false in  /etc/cloud/templates/hosts.tmpl on cp3
* 01:39 paladox: reboot cp3

## 2019-03-14 

* 13:37 paladox:  [13:22:07]  <+paladox>    !log increasing swap to 512M on cp3
* 13:26 paladox:  [13:22:07]  <+paladox>	!log increasing swap to 512M on cp3
* 13:18 paladox: adding swap to cp3 (256MB)
* 00:06 paladox: restarted puppetserver on puppet1

## 2019-03-13 

* 18:35 Southparkfan: repool mw1 and enable puppet on mw1/cp4
* 17:38 Southparkfan: depool mw1
* 17:30 Southparkfan: disable puppet on cp4
* 17:14 paladox: indexing allthetropeswiki for elasticsearch
* 17:12 paladox: generate elasticsearch index for allthetropeswiki
* 16:48 Southparkfan: disabling puppet on mw1
* 15:35 Southparkfan: drop searchindex table for nonsensopediawiki
* 13:11 PuppyKun: changed the misc1 shell passwd for ndkilla (root@misc1:/home/ndkilla# passwd ndkilla)

## 2019-03-12 

* 23:46 Southparkfan: drop metawiki.searchindex
* 23:21 Southparkfan: populating elasticsearch for metawiki
* 05:31 Reception123: reception@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php importDump.php --wiki damselswiki /home/reception/damsel_pages_full.xml

## 2019-03-11 

* 22:59 paladox: switched test1 to elasticsearch
* 01:07 paladox: running lc on mw*

## 2019-03-10 

* 22:24 paladox: created data_dump table (and inserted sql) on test1wiki

## 2019-03-09 

* 22:29 paladox: created DataDump repo
* 22:16 paladox: update php on test1 && nginx && openssh (and a few other packages)
* 17:57 MacFan4000: deleting astropediawiki and parapediawiki (wikis of an LTA)

## 2019-03-08 

* 21:18 paladox: starting import on mw2
* 17:45 paladox: starting gdb on mw1 (to debug segfaults with php)

## 2019-03-05 

* 00:35 paladox: re enable puppet on all hosts

## 2019-03-04 

* 22:58 paladox: enabling puppet on mw*
* 22:14 paladox: re enabled puppet on mw1
* 22:05 paladox: disabling puppet on all hosts
* 22:02 paladox: root@mw1:/mnt/mediawiki-static/private/miraheze/letsencrypt# cp -rp /etc/letsencrypt/** ./
* 19:39 paladox: migrate "Phantom Dusclops'92" from nonciclopedia to be attached to it's centralauth account.
* 17:04 paladox: apt-get install php7.2-xdebug on mw1
* 17:02 paladox: install gdb on mw1

## 2019-03-03 

* 22:14 Southparkfan: revert previous actions, operation is too risky
* 21:48 Southparkfan: disable swap on db4; attempting to reduce swap from 16GB to 6GB and reclaiming 10GB in root partition

## 2019-03-02 

* 18:21 Reception123: reception@mw1:~$ cd /srv/med*/w && sudo -u www-data git pull && sudo -u www-data git submodule update (Puppet disabled on mw1, inbalance created by change)
* 16:59 paladox: mkdir /mnt/mediawiki-static/private/miraheze && /mnt/mediawiki-static/private/miraheze/letsencrypt
* 16:46 paladox: stop miraheze ssl renewal service on mw1 && disable puppet
* 15:44 paladox: installing security updates on db4, mw*
* 15:36 paladox: upgrade puppet1 to debian 9.8
* 15:24 paladox: upgraded salt on bacula1
* 14:59 paladox: upgraded grafana to version 6 and icinga2 to 2.10.3 on misc1
* 14:14 Reception123: reception@mw3:/srv/mediawiki/w/maintenance/storage$ sudo -u www-data php compressOld.php --wiki absurdopediawiki -t = 'gzip'
* 06:13 Reception123: reception@mw3:/srv/mediawiki/w/maintenance$ sudo -u www-data php importDump.php --wiki absurdopediawiki /home/reception/absurdopedia_reverted_pages_full.xml
* 02:05 Southparkfan: graceful vpncloud shutdown
* 01:20 Southparkfan: previous entry also for db4
* 01:07 Southparkfan: ensure presence of iperf, vpncloud and net-tools packages on cp5 and test1

## 2019-02-28 

* 17:06 paladox: import beidipedia dump
* 16:49 paladox: upgrade phabricator
* 16:27 paladox: [15:25:56]  <+paladox>    !log rm mysql-bin.0* on db4
* 16:27 paladox: [15:19:55]  <+paladox>    !log stopping mysql (to be able to remove the binary logs manually)
* 16:27 paladox: run lc on mw*

## 2019-02-26 

* 00:14 paladox: run lc on mw*

## 2019-02-25 

* 17:24 paladox: run populateWikiSettings.php inserting wmgUseModeration into the db
* 17:11 paladox: MatomoAnalytics::deleteSite( 'pdacwiki' ); in eval.php (site does not exist)
* 17:10 paladox: MatomoAnalytics::deleteSite( 'alterwiki' ); in eval.php (site does not exist)
* 17:08 paladox: run MatomoAnalytics::addSite( 'mystarawiki' ); ; MatomoAnalytics::addSite( 'alterwiki' ); ; MatomoAnalytics::addSite( 'pdacwiki' ); in eval.php (sites were not in matomo)

## 2019-02-24 

* 23:03 paladox: running lc on mw*
* 17:13 John: UPDATE mw_permissions SET perm_permissions = '["createaccount","read","edit","createpage","createtalk","writeapi","viewmywatchlist","editmywatchlist","viewmyprivateinfo","editmyprivateinfo","editmyoptions","abusefilter-log","abusefilter-log-detail","abusefilter-view","autocreateaccount","centralauth-merge","oathauth-enable"]' WHERE perm_dbname = "metawiki" and perm_group = '*';
* 16:47 paladox: repool mw1
* 16:40 paladox: upgrade php on mw1 to 7.3.2 (bug fixes) && also dist upgrade to 9.8
* 16:40 paladox: depool mw1
* 16:37 MacFan4000: deleting permission cache files for metawiki
* 16:33 MacFan4000: UPDATE mw_permissions SET perm_permissions='["createaccount","read","edit","createpage","createtalk","writeapi","viewmywatchlist","editmywatchlist","viewmyprivateinfo","editmyprivateinfo","editmyoptions","abusefilter-log","abusefilter-log-detail","abusefilter-view","autocreateaccount","centralauth-merge","oathauth-enable""]' WHERE perm_dbname='metawiki' AND perm_group='*';
* 16:29 paladox: upgrade misc1 to debian 9.8
* 16:27 paladox: repool mw3
* 16:26 MacFan4000: UPDATE mw_permissions SET perm_permissions='["translate-review","move","move-subpages","move-rootuserpages","move-categorypages","movefile","read","edit","createtalk","writeapi","upload","reupload","reupload-shared","minoredit","editmyusercss","editmyuserjson","editmyuserjs","purge","sendemail","applychangetags","changetags","editcontentmodel","requestwiki","user","translate-messagereview","mwoauthmanagemygrants"]' WHERE perm_dbname='metawiki' AND perm_group='user';
* 16:22 MacFan4000: UPDATE mw_permissions SET perm_permissions='["autoconfirmed","editsemiprotected","move","createpage","translate","mwoauthproposeconsumer","mwoauthupdateownconsumer","skipcaptcha","createaccount"]' WHERE perm_dbname='metawiki' AND perm_group='autoconfirmed';
* 16:21 paladox: reboot mw3
* 16:19 paladox: upgrade php on mw3 to 7.3.2 (bug fixes) && also dist upgrade to 9.8
* 16:19 paladox: depool mw3
* 16:18 MacFan4000: UPDATE mw_permissions SET perm_addgroups='["flood","translator","translationadmin","autopatrolled","confirmed","rollbacker"]' WHERE perm_dbname='metawiki' AND perm_group='sysop';
* 16:18 paladox: repool mw2
* 16:13 MacFan4000: UPDATE mw_permissions SET perm_permissions='["autopatrol","block","blockemail","browsearchive","createaccount","createpage","createtalk","delete","deletechangetags","deletedhistory","deletedtext","deletelogentry","deleterevision","edit","editcontentmodel","editinterface","editprotected","editsemiprotected","editusercss","edituserjson","edituserjs","import","importupload","minoredit","move","noratelimit","override-export-depth","pagelang","patrol","patrolmarks","protect","purge","rollback","suppressredirect","unblockself","undelete","upload_by_url","abusefilter-modify","abusefilter-log-detail","abusefilter-view","abusefilter-log","abusefilter-modify-restricted","abusefilter-revert","abusefilter-view-private","abusefilter-log-private","override-antispoof","gadgets-edit","gadgets-definition-edit","globalblock-whitelist","nuke","oathauth-enable","oathauth-api-all","mwoauthproposeconsumer","mwoauthupdateownconsumer","tboverride","tboverride-account","titleblacklistlog","translate","translate-import","translate-manage","translate-messagereview","translate-groupreview","pagetranslation","massmessage"]' WHERE perm_dbname='metawiki' AND perm_group='sysop';
* 16:11 paladox: rebooted mw2
* 16:09 paladox: upgrade php on mw2 to 7.3.2 (bug fixes) && also dist upgrade to 9.8
* 16:08 paladox: depool mw2
* 16:06 MacFan4000: UPDATE mw_permissions SET perm_removegroups='["interface-admin","bot","sysop"]' WHERE perm_dbname='metawiki' AND perm_group='bureaucrat';
* 16:05 MacFan4000: UPDATE mw_permissions SET perm_addgroups='["interface-admin","bot","bureaucrat","sysop"]' WHERE perm_dbname='metawiki' AND perm_group='bureaucrat';
* 15:54 MacFan4000: UPDATE mw_permissions SET perm_permissions='["move","createpage","translate","mwoauthproposeconsumer","mwoauthupdateownconsumer","editsemiprotected","autoconfirmed","skipcaptcha"]' WHERE perm_dbname='metawiki' AND perm_group='confirmed';
* 15:51 MacFan4000: UPDATE mw_permissions SET perm_permissions='["rollback"]' WHERE perm_dbname='metawiki' AND perm_group='rollbacker';
* 15:46 MacFan4000: UPDATE mw_permissions SET perm_permissions='["editinterface","editusercss","edituserjson","edituserjs","editsitecss","editsitejson","editsitejs"]' WHERE perm_dbname='metawiki' AND perm_group='interface-admin';
* 15:43 MacFan4000: DELETE FROM mw_permissions WHERE perm_dbname='metawiki' AND perm_group='comentadmin';
* 15:43 MacFan4000: DELETE FROM mw_permissions WHERE perm_dbname='metawiki' AND perm_group='chatmod';
* 15:40 MacFan4000: DELETE FROM mw_permissions WHERE perm_dbname='metawiki' AND perm_group='forumadmin';
* 15:39 MacFan4000: DELETE FROM mw_permissions WHERE perm_dbname='metawiki' AND perm_group='oversight'; (was only adding one perm)
* 15:35 MacFan4000: DELETE FROM mw_permissions WHERE perm_dbname='metawiki' AND perm_group='reviewer';

## 2019-02-23 

* 20:59 paladox: upgrading puppet* to 6.3 (puppetserver to 6.2) on puppet1
* 03:27 paladox: run compressOld.php on baobabarchiveswiki (on mw1)
* 01:47 paladox: mass restarting of bacula-fd accross all servers

## 2019-02-22 

* 23:56 paladox: puppetserver ca sign --certname bacula1.miraheze.org on puppet1
* 23:52 paladox: puppetserver ca clean --certname bacula1.miraheze.org on puppet1
* 23:52 paladox: puppetserver ca revoke --certname bacula1.miraheze.org on puppet1
* 22:43 paladox: reimage bacula1 with 64-bit stretch image
* 22:25 Southparkfan: aaaaaand give tun/tap yet another try
* 22:12 paladox: shutdown bacula1
* 21:59 Southparkfan: disable TUN/TAP on test1, seems to break stuff
* 21:42 Southparkfan: enable TUN/TAP on test1, may require reboot
* 21:31 Southparkfan: install vpncloud package on test1

## 2019-02-21 

* 20:34 Reception123: sudo -u www-data /usr/bin/nice -12 /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/maintenance/runJobs.php on mw1

## 2019-02-20 

* 15:21 paladox: upgrade misc4 to debian 9.8
* 15:18 paladox: disabling puppet on lizardfs*
* 15:04 paladox: shut down prometheus master on misc4
* 14:25 paladox: shutting down salt on misc4 (and removing)
* 14:15 Reception123: rebuild LC on mw*
* 08:02 Reception123: rebuild LC on all wikis
* 06:54 Reception123: reception@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php importDump.php --wiki pathofexilewiki /home/paladox/Path+of+Exile+Wiki-20190211171816.xml

## 2019-02-19 

* 15:25 paladox: running lc on mw*
* 01:44 paladox: delete wiki's electronicsforallwiki eli5wiki elitefestwiki ellersliedemowiki elsharqwiki elswiki enchantedsongcontestwiki engineering4kidswiki epbwiki epi36wiki erdewiki escaladawiki escwiki eurovisiongameswiki everythingmodwiki experimentalpublicationgroupwiki exposingjillianepperlywiki eyebobswiki ezidiawiki fablacwiki faespherewiki fagslandwiki farfallewiki fatinsangelswiki fcsplwiki felfelwiki fgnoteswiki firstroboticswikiwiki fisicaapplicatawiki flatwiki florianwikiwiki flumeisinglasswiki foodhallwiki forgottennovelwiki fortheempirewiki fosnetwiki fredybashwiki freestateofjoneswiki freewillwiki frejaerikssonwiki frmwiki frontdeskswiki fsxworldspainwiki funnyvisionsongcontestwiki furbyislandwiki futurepartywiki fyrnsidubrasilwiki fysm1217wiki gafwiki gahoolewiki gamewiki gapzerodechetwiki garrettcountyguidewiki gastrolegnanowiki gatewiki gaysinspacewiki gendertransitionwiki generationsbamorowiki geometrydashwiki geopediawiki geresbamyanwiki gesotericowiki ggdrwiki gifpglobalwiki gilaaswiki givewiki gontranwiki granislawiki grbuenowiki grecipeswiki grinopellewiki groepeenwiki gsunixwiki guawiki gugacastwiki gunsensewiki guyswikiwiki hackwikiwiki halloweenwikiwiki hamimwiki hamkaastostiwiki hantpediawiki harmontownwiki haxionspacewiki hccwiki hdafbgwiki healthvectorwiki heathenwiki hedgeyourbetwiki heimwegtelefonwiki herazimewiki hestiaroboticswiki hexelswiki hiddenhistorywiki hirukowiki hockeyprospectswiki hogsmeadewiki holmeswiki holonterapiwiki homestuckwiki homevideowiki honkai3rdwiki hostitaliawiki howtogettowiki iawwiki iceposeidonwiki icmscholarswiki icterwiki idwwiki ignitewiki igorhersonwiki ijebustateinfowiki ilzurichwiki imperialwiki infiniteunknownwiki infofizsmwiki infojefprivwiki inkbloodwritersguildwiki innovwikiprotowiki integrawiki intersectionwiki inversionpasivawiki iotawiki ironswordswiki isfcomodorowiki isiliawiki islamwikillywiki isnstjustwiki itasiawiki itspuglewiki iubriswiki iwnwiki iwysanwiki jayprakash12345wiki jeanargentywiki jennyscwiki justinbieberwiki jwwikiwiki karagashwiki kasopediawiki kaufmannwiki kazhikwiki kbrprojectwiki kclwiki keepbusheycountryclubwiki kempowiki kerbalismwiki khorashanwiki kioscwiki kl6fwiki knowledgewiki kpiqwiki kpopswiki kspancevowiki kstartupswiki kzagwiki l45testwiki lambdawarswiki landofikioswiki langspacewiki languagerevitalizationwiki lapeninsulewiki larpsiteswiki lawrencescafuriwiki lcars47wiki lecolibriswiki leecheswiki leeryescribirenlaeradigitalwiki leftypolwiki lensoftwiki leyesprwiki liberhistoricawiki liesbornwikiwiki lifewiki liko12wiki liutfprwiki localizationwiki lodjawiki logalnetwiki lolwiki loraldwiki lovelyzwiki lspdfrwiki ltgsaleswiki luskwiki lzhscpwikiwiki macedoniskagovwiki machiningwiki magicvariantswiki makerlabwiki makingitpodcastwiki makipediawiki maktabawiki masseffectwiki mastermindhackswiki mathwiki maxwellwiki mcserawiki medergistswiki medicinawiki medienkurswiki mekniywiki mentalhealthinfoukwiki mesonwiki metaldetectorwiki mikeandchrisproductionswiki mikrocontrollerwiki minariwiki minecraftwiki minerrowiki miraiwiki mistralcupwiki mistralwiki mncwikipediawiki mobawiki modwikichickenkillerwiki monsterheartswiki monsterlegendswiki moofmilkerswiki morfarkultenwiki mscwiki msramwiki muenchowwiki mugiwikiwiki mumkeycinematicuniversewiki munawikiwiki musi339wiki musmyswiki mutewiki mvscwiki mwswiki mycpuwiki myragnarokwiki mystic20swiki mytenniswiki mywisdowwiki nanodlpwiki nathandernicewiki nationsglorywiki nddb2wiki neptuniawikiwiki nerdwiki nescwiki nestartstechwiki netthreewiki newnamlawiki newsalinaswiki newsniviwiki newstickerwiki ngrwikiwiki nhauwiki nigelshikeswiki nikiwiki nocontextforyouwiki noobdevopswiki norfolkconstabularywiki notezenwiki nouvellequerbeswiki ntlawwiki nulibrtewiki nvdanlwiki nysyoungcandidateswiki occultismpediawiki oldschoolrunescapewiki ombrewiki onepiecewiki onkopediawiki opsdailynoticeswiki orangesamuraiwiki orbusvrwiki organismwiki ortuswiki ostravawiki ourmetawiki ourpediajpwiki ourrailwiki ourwikiwiki owanetworkwiki paperhubwiki patelinwiki pdacwiki peitwiki pelaorolangawiki penalwikiwiki perdidosenlapcwiki pfiffigertonwiki pfsolutionswiki physikzusammenfassungwiki pirateswiki pisopacowiki pk83wiki plataformastrabajocolaborativowiki plataformawiki plnonbinarywiki pmpediawiki pmresourceswiki poleteawiki popmundowiki positiveparentingwiki printmakingbewiki printzillawiki priyowiki productarchivewiki programacionetcwiki programmingwiki projectstatuswiki proniateempirewiki proyectosdeaccionwiki pseudoterapiaswiki psychwiki pwscmwwiki pythiawiki pythonminecraftwiki qualityboxwiki quanticwiki qweelylookwiki r2b2wiki radviserwiki realmgrinderwiki rensing1wiki repairhelpwiki reproduceitwiki reptilehusbandrywiki republicoframulwiki researchafricawiki ressourceswiki retkiwiki reviworkwiki rfdswiki rigpapariswiki robloxwiki rockdomwiki rogesgrandiwiki roslwiki roxannewiki rpfolderwiki rptshelpwiki rtwiki rwhdwiki rwsaleswiki sadpepswiki safespacewiki sainsterbukawiki savetawiki sbffwiki scgmarchivewiki sciencelandwiki servicesnetwiki servinetwiki southparkfanwiki spacewikiwiki wrlwiki
* 01:29 paladox: delete wiki's cekbwiki  centralboxwiki  changemyorgwiki  chasingtimewiki  christianmusictempwiki  cifdwiki  claviushuntwiki  clickraidwiki  climatedbwiki  clonedeploywiki  cloudtvwiki  cloudwiki  coconutmanwiki  cocwiki  codetutswiki  codewiki  cointelwiki  colepinosgenilwiki  colonizemarswiki  colossalseagullwiki  commercialistiwiki  complexdoomwikiawiki  constancywiki  costestwiki  cowofgoldwiki  cpdiscordeditionwiki  cprarchiveswiki  craftcartelwiki  criptowikiwiki  crisisheroinewiki  cryptokittieswiki  cstwiki  cwwwiki  d8tawiki  daesocialwiki  danielgalewiki  daudvydwiki  davislistwiki  ddwikiwiki  deanostoolswiki  delete1wiki  delpetwiki  demetriowiki  denemewiki  despacitowiki  deutschkurswiki  devotedanddisgruntledwiki  diascwiki  didatticawiki  dipinsrpskiwiki  disabledpoundwiki  discovereachotherwiki  disstmsphdwiki  dongyangwiki  dotapiwiki  dpartwiki  drgcorsicawiki  drielnoxwiki  dryfusewiki  duallanguagewiki  dunklermondwiki  dystopiawiki  e501wiki  earthvisionwiki  eastbournetownsquarewiki  eccatoniawiki  eclaireurswiki  economicwarewiki  edisonwiki  edmundwiki  edustudentwiki  eduwiki  ekomwiki  eldritchtaleswiki
* 01:20 paladox: Delete wiki's antspacewiki appl2018wiki arbkfamilysearchwiki archives19emewiki archiwumsportowewiki armsinstitutewiki arrinesnotebookwiki artbyannewiki artecresourceswiki artificercreationswiki artwikiwiki arunedbwiki asckeyswiki ashehistorywiki assovelowiki asswiki asystelecowiki atlantiwiki attackontitanwiki aureliawiki aurellewikiwiki australiawiki autismwikiwiki autodocwiki automationwiki avaecanvaswiki azurlanewikiwiki babelfilmswiki badyoutuberswiki bakufuwiki balcanopediascharlatanicawiki barbarasherwikiwiki batterysafetytechwiki bazarbdwiki bcagparchivewiki bchplswiki beetcodewiki benchaseytwiki beremagnewiki berlinowiki bermudiwiki bewellmedicalwiki bftwiki bibleblogwiki bierpongwiki biglakemnhistorywiki bigtoewiki bijiawikiwiki biografiaschilenaswiki biologywiki blgameswiki blocknetwiki bloodstainedwiki blpwiki brtz3wiki bruscatowiki bruwiki bs12wiki bugolaviawiki burropediawiki buxmontuuwiki c1mwiki caduwiki caelishchronicleswiki campbellpagewiki carmeigatwiki castapediawiki cawiki cchowiki ccwikiwiki cebuvisayasdirectorywiki
* 01:09 paladox: delete wiki's alterwikiwiki, altruniversewiki, amcdlwiki, ameciclowiki, amicsdesmuseucawiki, amicsdesmuseuwiki, amntwiki, amxwikiwiki, analogypediawiki and anchorhrgwiki
* 01:07 paladox: delete wiki's aidyllicwiki, airwiki, akancyclopediawiki, aklassewiki, alfrescowiki, alifloktawiki, alittletroutywiki and allsamemonsterswiki
* 01:06 paladox: delete wiki's adantewiki, adminbookclubwiki, adnovumwiki , aerowikiwiki, africavisionwiki, agathinonwiki, ageofwushuwiki and agropediawiki
* 01:03 paladox: deleteted wiki's absurdopediawiki, abundancewiki, acasrbijawiki
* 01:02 paladox: deleteted wiki's 2cvcupfrancewiki, 3dprinterscncwiki, 4mindswiki, aapwiki, abainnovationwiki, abarrethwiki and abeldenwiki

## 2019-02-18 

* 20:07 paladox: running lc on mw*

## 2019-02-17 

* 16:34 Reception123: reception@mw2:/srv/mediawiki/w/maintenance$ sudo -u www-data php importDump.php --wiki animatedfemalemusclewiki /home/reception/animatedmusclewomen_pages_full.xml
* 15:55 paladox: reboot test1
* 15:52 paladox: upgrade test1 to debian 9.8

## 2019-02-16 

* 12:30 Reception123: running wikibackups (./test.sh /home/reception/allpublic.dblist /srv/mediawiki/w/maintenance/dumpBackup.php)
* 02:51 John: created tables in incidents database

## 2019-02-15 

* 13:39 paladox: renewing m.miraheze.org cert

## 2019-02-14 

* 06:27 Reception123: restarted logbot
* 06:24 Reception123: removed 2FA from Samwilson on Phabricator

## 2019-02-12 

* 06:07 Reception123: renamed karrotwiki to methruwiki

## 2019-02-10 

* 23:53 paladox: removing 2FA from Eduaddad T4090

## 2019-02-09 

* 21:27 paladox: upgrade phabricator

## 2019-02-08 

* 09:28 Reception123: reception@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php importDump.php --wiki pippipediawiki /home/reception/creationbetheworld23s_pages_full.xml

## 2019-02-06 

* 19:23 paladox: restarting varnish on cp4 due to "unknown backend" showing

## 2019-02-04 

* 01:07 paladox: ran a update on the sites table for ffgxvwiki
* 00:38 paladox: running lc on mw*
* 00:22 paladox: import starwars_pages_full.xml on baobabarchiveswiki

## 2019-01-26 

* 01:26 paladox: upgrading puppet to puppet 6.2.0 on puppet1
* 01:24 paladox: import starwars_pages_full.xml  on baobabarchiveswiki
* 01:18 John: rebuilding rc on attwiki
* 01:11 paladox: creating GDPRAccount on all wiki's (miraheze account to comply with GDPR)
* 00:43 paladox: removed a user email address per email at privacy@

## 2019-01-25 

* 20:05 Southparkfan: running sendBulkEmails.php on mw1
* 13:32 paladox: upgrade phabricator on misc4

## 2019-01-24 

* 14:39 paladox: upgrade phabricator on misc4
* 14:09 John: removed editothersprofiles from all groups
* 03:47 paladox: ran modifyGroupPermission.php per T4046

## 2019-01-23 

* 17:38 Southparkfan: issues a varnish ban for req.url ~ ^/robots.txt on all cache proxies
* 17:30 paladox: running generateMirahezeSitemap.php on mw1

## 2019-01-22 

* 22:27 paladox: upgrading apt on all servers
* 12:12 John: set wiki_inactive_exempt = 1 for all wikis in $wgCreateWikiInactiveWikisWhitelist
* 12:06 John: ALTER TABLE cw_wikis ADD COLUMN wiki_inactive_exempt TINYINT NOT NULL DEFAULT '0' AFTER wiki_inactive_timestamp;

## 2019-01-21 

* 15:14 John: falling back to Redis for session and main caching temporarily

## 2019-01-20 

* 22:36 paladox: reboot misc2 to reduce ram
* 22:32 paladox: setting prometheus master up on misc4
* 22:30 paladox: shutting prometheus master down on misc2
* 15:17 paladox: upgrade phabricator to fix a bug on misc4
* 15:15 Southparkfan: set global local_infile=OFF; on db4
* 01:18 paladox: reboot cp5 for kernel upgrade.

## 2019-01-19 

* 19:34 paladox: dropping "math" table from all wiki's
* 19:32 paladox: drop "math" table from metawiki, no longer exists in the math extension
* 17:24 paladox: running lc on mw[23]
* 15:29 paladox: rename wiki intpwiki to taswinwiki
* 15:19 paladox: upgrade phabricator on misc4
* 00:48 paladox: upgrading phabricator on misc4
* 00:36 paladox: fix namespaces lpawiki, mindgartwiki, ianyinwiki, gllwiki, naturepediawiki, bscwiki, stiffwiki, qboxnextwiki, craedopediawiki
* 00:35 paladox: fix namespaces hominwiki, kmtfwiki, utoowiki, indiawiki, platcomicswiki, swashbucklerwiki
* 00:35 paladox: fix namespaces gbgschulpflegschaftwiki, deutschlandburgerwiki, anarchymcwiki, ckdocswiki, cuttingroomwiki, uas5wiki
* 00:34 paladox: fix namespaces readysteadyyetiwiki, twimwikiwiki, vechicleswiki, ipuwikiwiki, soprometwiki, wintermoorwiki, gjtwiki, atlaswiki
* 00:34 paladox: fix namespaces ebmscwiki, arbreapalabrewiki, ekodengewiki, dellplanetwikiwiki, tlmwiki, fantasypediawiki

## 2019-01-18 

* 22:56 paladox: running lc on mw*
* 16:42 paladox: running insertNamespaces.php on battleaxewiki, ff5fjfwiki, yurinikolaiwiki, fanmadetvchannelswiki, woerterbuchwiki, amcwiki, seerwiki, chronostormwiki and iriswiki
* 16:38 paladox: running insertNamespaces.php on alientoasterdogwiki, mrgshowswiki, djruddhawiki, igwikiwiki, testghrwiki
* 16:37 paladox: running insertNamespaces.php on goldpediawiki
* 16:35 paladox: insert default namespaces into 'default' from loginwiki
* 16:31 paladox: running insertNamespaces.php on uncyclopedia2wiki
* 00:04 paladox: running lc on mw*

## 2019-01-17 

* 22:08 paladox: repool mw3
* 22:04 paladox: depool mw3
* 21:26 paladox: repool mw2
* 21:16 paladox: depool mw2
* 21:15 paladox: repool mw1
* 20:50 paladox: depool mw1
* 09:44 John: reverted my last log message change (because test1wiki shouldn't be deleted, change works though)
* 09:43 John: setting wiki_deleted to 1 for test1wiki temp
* 09:25 John:  ALTER TABLE cw_wikis ADD COLUMN wiki_deleted TINYINT NOT NULL DEFAULT '0' AFTER wiki_closed_timestamp, ADD COLUMN wiki_deleted_timestamp BINARY(14) NULL AFTER wiki_deleted;

## 2019-01-16 

* 21:40 Southparkfan: removed packages proxysql and mysql-client from test1
* 20:51 Southparkfan: install proxysql package on test1
* 20:33 Southparkfan: 'usermod -a -G ssl-cert www-data' on test1

## 2019-01-14 

* 01:19 Southparkfan: CentralAuthUser::newFromId( 20792 )->quickInvalidateCache(); (previous redis purge didn't work)
* 01:16 Southparkfan: deleted key WANCache✌️global:centralauth-user:79eda1a42924fbb966df82627046c9fe from redis to force cache purge
* 00:23 paladox: doing a emergency restart of mariadb

## 2019-01-13 

* 19:56 MacFan4000: deleted permission cache files for weatherwiki
* 19:52 MacFan4000: DELETE FROM mw_permissions WHERE perm_dbname='weatherwiki' AND perm_group='interface-admin'
* 19:26 paladox: running lc on mw* and test1
* 16:51 paladox: running lc on mw* and test1

## 2019-01-12 

* 22:27 paladox: running script on misc4 to remove all files that have ttl != null
* 21:54 paladox: bin/storage optimise on misc4
* 17:39 Reception123: DELETED FROM CW_WIKIS and DROPPED cuttingroomwiki uas5wiki testdeletewiki
* 17:34 Southparkfan: dropped all database matching pattern southparkfan(11111|123|12345|[3-6])wiki (were created for CW issues)
* 17:33 paladox: reboot misc4 to see if it will erase temp files
* 17:27 paladox: uninstalling lizardfs from misc4
* 16:47 paladox: unmounting /mnt/mediawiki-static (images will start disapearing)
* 16:37 paladox: depool mw1
* 15:09 paladox: stopping phd on misc4

## 2019-01-11 

* 23:05 paladox: /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist modifyGroupPermission.php --addperms="editsitecss,editsitejs,editsitejson" sysop on mw1
* 22:17 paladox: deleting files on misc4
* 20:46 paladox: restarted puppetserver (semmed stuck on 100% cpu)
* 15:05 Southparkfan: enabled puppet on misc2 again
* 15:03 Southparkfan: deleted all redis keys matching pattern *:highlight:*
* 14:57 Southparkfan: deleted all redis keys matching pattern *:diff:*
* 14:56 paladox: 14:15:14  <+paladox>    !log reboot misc2 to clean ram
* 14:55 Southparkfan: 15:50:27 <+SPF|Cloud> !log disable puppet on misc2 to resolve redis trouble
* 14:52 paladox: 14:15:14  <+paladox>    !log reboot misc2 to clean ram
* 14:21 paladox: [14:15:14]  <+paladox>	!log reboot misc2 to clean ram
* 14:17 paladox: reboot misc2 to clean ram
* 06:53 paladox: ran modifyGroupPermission.php to add editsite* to all users in sysop group
* 06:19 paladox: adding "editinterface" to default on sysop group
* 05:37 paladox: [03:10:04]  <+paladox>    !log repool mw3
* 05:37 paladox: [02:50:04]  <+paladox>    !log repool mw2
* 05:37 paladox: [02:27:34]  <+paladox>    !log repooling mw1 and depool mw2 and mw3
* 05:37 paladox: [00:36:33]  <+MacFan4000>    !log changing default branch for @miraheze/mediawiki to REL1_32
* 05:37 paladox: [00:14:16]  <+paladox>    !log upgrading all wiki's to 1.32
* 05:37 paladox: [00:10:15]  <+paladox>    !log upgrading metawiki to 1.32
* 05:37 paladox: [00:06:41]  <+paladox>    !log putting all wiki's into read only - pending upgrade to 1.32
* 05:37 paladox: [23:29:43]  <+paladox>    !log depool mw1
* 05:36 paladox: [03:10:04]  <+paladox>	!log repool mw3
* 05:36 paladox: [02:50:04]  <+paladox>	!log repool mw2
* 05:36 paladox: [02:27:34]  <+paladox>	!log repooling mw1 and depool mw2 and mw3
* 05:35 paladox: [00:36:33]  <+MacFan4000>	!log changing default branch for @miraheze/mediawiki to REL1_32
* 05:35 paladox: [00:14:16]  <+paladox>	!log upgrading all wiki's to 1.32
* 05:35 paladox: [00:10:15]  <+paladox>	!log upgrading metawiki to 1.32
* 05:35 paladox: [00:06:41]  <+paladox>	!log putting all wiki's into read only - pending upgrade to 1.32
* 05:35 paladox: [23:29:43]  <+paladox>	!log depool mw1
* 00:06 paladox: putting all wiki's into read only - pending upgrade to 1.32

## 2019-01-10 

* 23:29 paladox: depool mw1
* 18:39 paladox: Renaming svwiki to psl631testwiki per T3967

## 2019-01-09 

* 01:40 Southparkfan: dropped southparkfan[2-5]wiki wikis
* 01:34 Southparkfan: executed once again
* 01:19 Southparkfan: executed previous queries again
* 01:16 Southparkfan: MariaDB [metawiki]> delete from echo_notification where notification_timestamp like '20190109%' and notification_user = 2;
* 01:16 Southparkfan: MariaDB [metawiki]> delete from echo_event where event_type = 'wiki-creation';
* 00:18 Southparkfan: testing changes in CreateWiki on mw1

## 2019-01-08 

* 01:50 MacFan4000: deleting iwwiki

## 2019-01-07 

* 23:46 paladox:  sudo chmod -R 0770 /etc/puppetlabs/puppet/ssl-keys
* 23:45 MacFan4000: (paladox) sudo chmod 0770 /etc/puppetlabs/puppet/ssl-keys on puppet1
* 23:43 paladox: sudo chmod 0700 /etc/puppetlabs/puppet/ssl-keys on puppet1
* 22:31 MacFan4000: macfan@mw1:/$ sudo -u www-data php /srv/mediawiki/w/maintenance/dumpBackup.php --wiki tesminadventureswiki --full --output gzip:/mnt/mediawiki-static/dumps/tesminadventureswiki.xml.gz
* 12:29 MacFan4000: DELETE FROM mw_namespaces WHERE ns_dbname='xedwiki' AND ns_namespace_name='Greek_talk'; (per stewards noticeboard)
* 12:29 MacFan4000: DELETE FROM mw_namespaces WHERE ns_dbname='xedwiki' AND ns_namespace_name='Greek'; (per stewards noticeboard)
* 12:28 MacFan4000: DELETE FROM mw_namespaces WHERE ns_dbname='xedwiki' AND ns_namespace_name='English_talk'; (per stewards noticeboard)
* 12:28 MacFan4000: DELETE FROM mw_namespaces WHERE ns_dbname='xedwiki' AND ns_namespace_name='English'; (per stewards noticeboard)

## 2019-01-06 

* 17:00 paladox: running lc on mw* and test1
* 14:48 paladox: importing mw dump on bigcartoonwiki (on mw1)
* 14:45 paladox: importing mw dump for nowchesswiki
* 14:06 paladox: /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/maintenance/sql.php /srv/mediawiki/w/extensions/GlobalBlocking/globalblocking.sql on mw3
* 04:09 paladox: repool mw1
* 04:04 paladox: delete from mw_namespaces where ns_dbname = 'metawiki' and ns_namespace_name = 'TestHello_talk';
* 04:04 paladox: delete from mw_namespaces where ns_dbname = 'metawiki' and ns_namespace_name = 'TestHello';
* 00:55 paladox: running lc on mw*

## 2019-01-05 

* 17:10 paladox: depool mw1
* 01:56 paladox: upgrading phabricator on misc4

## 2019-01-04 

* 20:44 Southparkfan: stop jobrunner on mw3
* 20:32 Southparkfan: install iftop on mw[1-3]
* 00:26 Southparkfan: ran update cw_requests set cw_user = 44876 where cw_id = 6919;

## 2019-01-03 

* 23:48 paladox: running update set commands on db4 to fix cw_user for requests that have the wrong id.
* 23:36 paladox: update cw_requests set cw_user = 44922 where cw_dbname = 'giantesswiki'; on db4
* 23:35 paladox:  update cw_requests set cw_user = 44929 where cw_dbname = 'dawsontechboothwiki'; on db4
* 23:28 paladox: ALTER TABLE cw_comments MODIFY cw_comment_user INT(10) NOT NULL; on db4
* 23:27 paladox: ALTER TABLE cw_requests MODIFY cw_user INT(10) NOT NULL; on db4
* 16:04 paladox: sudo -u www-data php scriptMira2.php --wiki=nonciclopediawiki on mw1
* 15:49 paladox: sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist maint*/manageJobs.php --action=delete --type="LocalGlobalUserPageCacheUpdateJob" on mw1
* 04:26 paladox: sudo -u www-data /usr/bin/nice -19 /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist maint*/manageJobs.php --action=delete --type="LocalGlobalUserPageCacheUpdateJob" on mw1
* 03:46 paladox: creating MacFan4000 on icingaweb2
* 03:40 paladox: creating Voidwalker on icingaweb2
* 02:38 paladox: recreating namespace Guide and Guide_talk for wiki paliwikiwiki
* 02:33 paladox: delete from mw_namespaces where ns_dbname = 'paliwikiwiki' and ns_namespace_id = 3001; on db4
* 02:33 paladox: delete from mw_namespaces where ns_dbname = 'paliwikiwiki' and ns_namespace_id = 3000; on db4
* 01:15 paladox: MatomoAnalytics::addSite( 'untrashwiki' ) on mw1

## 2019-01-02 

* 00:15 paladox: update mw_namespaces set ns_aliases = '["Image_talk"]' where ns_dbname = 'metawiki' and ns_namespace_name = 'File_talk'; on db4
* 00:14 paladox: update mw_namespaces set ns_aliases = '["Image"]' where ns_dbname = 'metawiki' and ns_namespace_name = 'File'; on db4

## 2019-01-01 

* 21:17 paladox: repool mw1
* 21:07 paladox: delete all namespaces cdb files on mw*
* 18:00 Reception123: MariaDB [phabricator_herald]> UPDATE herald_rule SET isDisabled = '1' WHERE id = '10'; (inactive user)
* 17:59 Reception123: MariaDB [phabricator_herald]> UPDATE herald_rule SET isDisabled = '1' WHERE id = '28'; (inactive user)
* 16:23 MacFan4000: macfan@mw3:~$ sudo service jobrunner restart && sudo service jobchron restart
* 16:21 MacFan4000: running jobs everywhere in a screen on mw1
* 16:19 paladox: running scriptMira2.php on mw1 (it creates a local account on metawiki and loginwiki)
* 15:05 paladox: run UPDATE globaluser SET gu_email = 'xxx' WHERE gu_name = 'Revenant Lord'; (where xxx is a email)
* 15:01 paladox: depool mw1

----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:Server_admin_log/2019)**