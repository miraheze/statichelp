---
title: Tech:Server admin log/2020
---

`{{ {{TOC right}} }}`
## 2020-12-31 

* 23:17 paladox: move piwik db to db12
* 23:10 paladox: root@jobrunner1:/srv/mediawiki/w/maintenance/storage# sudo -u www-data php compressOld.php --wiki bluepageswiki --type gzip
* 23:10 paladox: root@jobrunner1:/srv/mediawiki/w/maintenance/storage# sudo -u www-data php compressOld.php --wiki bluepageswiki -t gzip
* 23:06 paladox: root@jobrunner1:/srv/mediawiki/w/maintenance/storage# sudo -u www-data php compressOld.php --wiki gyaanipediawiki --type gzip
* 23:03 paladox: drop chakuwikiwiki  on db13
* 23:01 paladox: root@jobrunner1:/srv/mediawiki/w/extensions/CreateWiki/maintenance# sudo -u www-data php changeDBCluster.php --wiki chakuwikiwiki --db-cluster c3
* 22:53 paladox: move chakuwikiwiki database to db12
* 22:52 Universal_Omega: UPDATE mw_settings SET s_settings = REPLACE(s_settings, ': ", ', ': "", ');
* 22:41 paladox: root@jobrunner2:/home/paladox# kill -9 6278 (import)
* 22:41 paladox: root@jobrunner2:/home/paladox# kill -9 6277 (import)
* 19:17 Universal_Omega: UPDATE mw_settings SET s_settings = REPLACE(REPLACE(REPLACE(REPLACE(REPLACE(JSON_REPLACE(s_settings, '$.wmgDefaultRobotPolicy', CONCAT('["', REPLACE(JSON_EXTRACT(s_settings, '$.wmgDefaultRobotPolicy'), ',', '","'), '"]')), '"[', '['), ']"', ']'),'\\"', '"'), '," ', ', "'), '""', '"');
* 19:17 Universal_Omega: UPDATE mw_settings SET s_settings = JSON_INSERT(s_settings, '$.wmgDefaultRobotPolicy', JSON_EXTRACT(s_settings, '$.wgDefaultRobotPolicy'));
* 17:07 Universal_Omega: sudo -u www-data mv /mnt/mediawiki-static/historiadevisagemwiki /mnt/mediawiki-static/encyclopediavisagicawiki
* 16:56 Universal_Omega: wfGetDB( DB_MASTER, [], $wgEchoSharedTrackingDB )->update( 'echo_unread_wikis', '*', [ 'euw_wiki' => 'encyclopediavisagicawiki' ], [ 'euw_wiki' => 'historiadevisagemwiki' ] ); using eval.php
* 16:38 Reception123: renamed historiadevisagemwiki to encyclopediavisagicawiki
* 16:35 Reception123: reception@jobrunner2:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --report=1 --wiki chakuwikiwiki /home/reception/chakuwiki-full.xml --namespaces="0|1|4|5|6|7|8|9|10|11|12|13|14|15"  --uploads --no-local-users
* 10:20 Universal_Omega:  sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildLocalisationCache.php --wiki loginwiki on mw*, jbr*, and test2
* 10:12 Universal_Omega: sudo -u www-data /usr/local/bin/foreachwikiindblist /home/universalomega/wikiforum.json /home/universalomega/updateWikiForumTables.php (drops 28 database columns on every wiki with WikiForum enabled) - see the full script [here](https://meta.miraheze.org/wiki/github:miraheze/mediawiki/pull/805)
* 09:56 Universal_Omega: sudo -u www-data /usr/local/bin/foreachwikiindblist /home/universalomega/wikiforum.json /srv/mediawiki/w/extensions/WikiForum/maintenance/migrateOldWikiForumUserColumnsToActor.php && sudo -u www-data /usr/local/bin/foreachwikiindblist /home/universalomega/wikiforum.json /srv/mediawiki/w/extensions/WikiForum/maintenance/migrateOldWikiForumTimestampColumnToNew.php (migrates existing WikiForum database columns over to new columns)
* 09:52 Universal_Omega: sudo -u www-data /usr/local/bin/foreachwikiindblist /home/universalomega/wikiforum.json /home/universalomega/updateWikiForumTables.php (adds 16 database columns on every wiki with WikiForum enabled) - see the full script [here](https://meta.miraheze.org/wiki/github:miraheze/mediawiki/pull/805)
* 05:36 Universal_Omega: sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildLocalisationCache.php --wiki loginwiki on mw*, jbr*, and test2
* 05:11 Universal_Omega: sudo -u www-data /usr/local/bin/foreachwikiindblist /home/universalomega/translate.json /srv/mediawiki/w/maintenance/sql.php /home/universalomega/translate_cache.sql
* 04:50 Universal_Omega: sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildLocalisationCache.php --wiki loginwiki on test2
* 04:50 Universal_Omega: sudo -u www-data php /srv/mediawiki/w/maint*/mergeMessageFileList.php --output /srv/mediawiki/config/ExtensionMessageFiles.php --wiki loginwiki on test2
* 04:48 Universal_Omega: reinstall mediawiki on test2
* 02:36 Zppix: sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildLocalisationCache.php --wiki loginwiki on test2
* 02:25 Universal_Omega: sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildLocalisationCache.php --wiki loginwiki on mw* and jbr*

## 2020-12-30 

* 19:03 Reception123: sudo -u www-data php /srv/mediawiki/w/extensions/CreateWiki/maintenance/deleteWikis.php --wiki=loginwiki Reception123 --delete
* 19:02 Zppix: rebuildLC on test2 (hasnt been done for a long time)
* 18:44 Reception123: bash ./delbackups.sh /home/reception/backupwikis.dblist /srv/mediawiki/w/maintenance/dumpBackup.php (delbackups)
* 06:45 Reception123: renamed scvcreationswiki to caliburcreationswiki
* 06:40 Universal_Omega: sudo -u www-data php /srv/mediawiki/w/maintenance/initSiteStats.php --update --wiki chibirobowiki
* 06:38 Reception123: reception@jobrunner1:/srv/mediawiki/w/maintenance$ sudo -u www-data php /srv/mediawiki/w/maintenance/cleanupTitles.php --wiki minecraftathomewiki
* 06:19 Universal_Omega: universalomega@jobrunner1:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --report=1 --wiki chibirobowiki /home/universalomega/chibirobo_pages_full.xml
* 00:42 Universal_Omega: universalomega@jobrunner1:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/runJobs.php --wiki =testwiki

## 2020-12-29 

* 23:16 paladox: upgrade tzdata on puppet2
* 23:12 paladox: set puppet2 cpu to 3
* 22:54 Universal_Omega: sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildLocalisationCache.php --wiki loginwiki on mw* and jbr*
* 22:54 Universal_Omega: sudo -u www-data php /srv/mediawiki/w/maintenance/mergeMessageFileList.php --output /srv/mediawiki/config/ExtensionMessageFiles.php --wiki loginwiki on mw* and jbr*
* 21:38 Southparkfan: accidentally broke redis-server on rdb1, therefore causing a cache wipe (people are likely logged out...)
* 21:37 Southparkfan: performed a test on rdb1
* 21:27 Southparkfan: restart citoid & restbase on services1
* 21:23 paladox: root@jobrunner1:/home/paladox# sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/w/cache/databases.json /srv/mediawiki/w/maintenance/sql.php /home/paladox/remove_globalblocks_table.sql
* 21:18 paladox: root@jobrunner1:/home/paladox# sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/w/cache/databases.json /srv/mediawiki/w/maintenance/sql.php /srv/mediawiki/w/extensions/GlobalBlocking/sql/patch-global_block_whitelist-use-varbinary.sql
* 21:16 paladox: root@jobrunner1:/home/paladox# sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/w/cache/databases.json /srv/mediawiki/w/maintenance/sql.php /srv/mediawiki/w/extensions/GlobalBlocking/sql/patch-global_block_whitelist-reason-length.sql
* 21:13 paladox: root@jobrunner1:/home/paladox# sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/w/cache/databases.json /srv/mediawiki/w/extensions/GlobalBlocking/sql/patch-global_block_whitelist-reason-length.sql
* 21:11 paladox: apply patch-globalblocks-reason-length.sql to mhglobal.globalblocking
* 20:10 Reception123: running GDPR script
* 19:40 Zppix: rebuildRC and initSiteStats following completed import
* 19:40 Zppix: importDump.php to restore a deleted wiki per request on jobrunner1
* 18:12 Universal_Omega: UPDATE mw_settings set s_settings = JSON_REMOVE(s_settings, '$.wgCookieWarningMoreUrl');

## 2020-12-28 

* 18:39 Reception123: reception@jobrunner1:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/storage/compressOld.php --wiki chakuwikiwiki --type gzip
* 07:28 Reception123: running wikibackups on jobrunner1 (bash ./wikibackups.sh /home/reception/backupwikis.dblist /srv/mediawiki/w/maintenance/dumpBackup.php)

## 2020-12-27 

* 22:52 paladox: restarted varnish on cp6
* 22:18 paladox: upgrade kernel and tzdata on cp[67]
* 22:17 paladox: ignore previous log only tzdata was updated
* 22:15 paladox: upgrade kernel and tzdata on bacula2
* 22:14 paladox: upgrade gluster on jobrunner[12]
* 22:11 paladox: upgrade tzdata on mw* and jobrunner*
* 22:07 paladox: upgrading gluster and debian to 10.7 on gluster[12] & also reboot
* 18:32 paladox: install security updates on all servers
* 12:42 John: reopening all wikis closed today
* 08:11 PuppyKun: ndkilla@mw5.mh.o: sudo chown -R www-data:www-data /srv/mediawiki/w/.git (some files in .git/objects/** were owned by root, git pulls failed with error: insufficient permission for adding an object to repository database .git/objects)
* 06:00 Universal_Omega: Migrate $wgForeignFileRepos to  ManageWiki on nbdbwiki, ndgwiki, gyaanipediawiki, higyaanipediawiki, mrgyaanipediawiki, pagyaanipediawiki, tuscriaturaswiki, yourcreatureswiki, and wildterra2enwiki
* 00:48 Universal_Omega: migrated $wgForeignFileRepos to ManageWiki

## 2020-12-26 

* 21:55 Southparkfan: started graylog processing
* 21:44 Southparkfan: save test
* 21:38 Southparkfan: temporarily disabled graylog message processing for performance test
* 21:35 Southparkfan: due to the recent maintenance, the backlog in graylog has climbed to over 3 million messages. graylog processes about 215k messages per 10 minutes, so let's be patient
* 21:31 paladox: root@jobrunner1:/home/paladox# sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/w/cache/databases.json /srv/mediawiki/w/maintenance/runJobs.php
* 21:26 paladox: restart jobrunner on jobrunner[12]
* 20:44 Southparkfan: stop jobrunner/jobchron
* 18:57 Reception123: reception@jobrunner2:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/importImages.php --wiki=elgeiswiki --search-recursively --skip-dupes /home/reception/lgsmc/lgsmcfandomcom-20201226-wikidump/images
* 16:29 Southparkfan: puppet on cp/mw may be enabled/disabled at any time until further notice
* 15:51 Southparkfan: disable puppet on mw/cp
* 15:21 Reception123: reception@jobrunner2:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki elgeiswiki /home/reception//lgsmc/lgsmcfandomcom-20201226-wikidump/lgsmcfandomcom-20201226-history.xml
* 13:16 Reception123: reception@jobrunner1:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki batmanwiki /home/reception/Batman_Wiki-20201226121435.xml
* 09:04 Reception123: reception@jobrunner1:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki hypewiki /home/reception/hypewiki.xml
* 07:03 Reception123: reception@jobrunner1:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki allatrawiki /home/reception/delbackups/allatrawiki.xml

## 2020-12-25 

* 23:38 Southparkfan: and disable puppet for cp/mw again
* 22:34 Southparkfan: disable puppet on mw/cp
* 22:16 paladox: remove old letsnecrypt certificates from /etc/letsencrypt
* 21:08 Southparkfan: enable puppet on db servers
* 21:00 Southparkfan: disable puppet on db servers
* 20:05 Southparkfan: commit new private key for wildcard cert in ssl-keys repo

## 2020-12-24 

* 20:15 Universal_Omega:  UPDATE content SET content_model = (SELECT model_id FROM content_models WHERE model_name = 'Scribunto') WHERE content.content_sha1 IN (SELECT rev_sha1 FROM revision JOIN page ON revision.rev_page = page.page_id WHERE page.page_namespace = 828); on nonciclopediawiki
* 20:14 Universal_Omega: UPDATE `page` SET page_content_model = 'Scribunto' WHERE page_namespace = 828; on nonciclopediawiki
* 18:15 Universal_Omega:  INSERT INTO content_models (model_id, model_name) VALUES (5, 'json'); on doctorwhofanfilmsdatabasewiki
* 18:15 Universal_Omega:  INSERT INTO content_models (model_id, model_name) VALUES (4, 'Scribunto'); on doctorwhofanfilmsdatabasewiki
* 18:14 Universal_Omega:  INSERT INTO content_models (model_id, model_name) VALUES (3, 'javascript'); on doctorwhofanfilmsdatabasewiki
* 18:14 Universal_Omega:  INSERT INTO content_models (model_id, model_name) VALUES (2, 'css'); on doctorwhofanfilmsdatabasewiki
* 18:14 Universal_Omega:  INSERT INTO content_models (model_id, model_name) VALUES (1, 'wikitext'); on doctorwhofanfilmsdatabasewiki
* 13:56 Reception123: progressive continuation of T6626 spread out on jbr1/jbr2
* 10:25 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki callipediawiki /home/reception/Wikipedia-20201201210042.xml --report 1
* 10:25 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki callipediawiki /home/reception/Wikipedia-20201201185723.xml --report 1
* 10:25 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki callipediawiki /home/reception/Wikipedia-20201201205808.xml --report 1

## 2020-12-23 

* 22:39 paladox: reinstalling test2
* 19:21 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki callipediawiki /home/reception/Wikipedia-20201201185556.xml --report 1
* 19:21 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki callipediawiki /home/reception/Wikipedia-20201201185410.xml --report 1
* 15:58 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki callipediawiki /home/reception/Wikipedia-20201201185020.xml --report 1 on jbr2
* 15:48 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki callipediawiki /home/reception/Wikipedia-20201201185128.xml --report 1 on jbr2
* 15:43 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki callipediawiki /home/reception/Wikipedia-20201201184920.xml --report 1 on jb1
* 15:37 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki callipediawiki /home/reception/Wikipedia-20201201184744.xml --report 1 on jbr1
* 15:37 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki callipediawiki /home/reception/Wikipedia-20201201184643.xml --report 1
* 15:30 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki callipediawiki /home/reception/Wikipedia-20201201182023.xml --report 1 on jbr1
* 15:27 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki callipediawiki /home/reception/Wikipedia-20201201231120.xml --report 1
* 15:27 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki callipediawiki /home/reception/Wikipedia-20201201184533.xml --report 1 on jbr2
* 15:27 Reception123:  sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki callipediawiki /home/reception/Wikipedia-20201201182334.xml --report 1 on jbr2
* 15:26 Reception123: restarted logbot on mon1
* 04:20 Universal_Omega: sudo -u www-data /usr/local/bin/foreachwikiindblist /home/universalomega/widgets.json /srv/mediawiki/w/extensions/ManageWiki/maintenance/toggleExtension.php widgets --disable on jobrunner1
* 03:32 paladox: depool/repool mw4 (decrease core by 1 to 5)
* 03:06 paladox: repool mw7
* 02:08 paladox: depool, downtimed, remove from puppet, rm -rf /root /etc/ssl/private /var/log, reinstalled and repool mw7
* 01:24 Southparkfan: set downtime in icinga for test2
* 01:24 Southparkfan: shutdown test2
* 01:15 paladox: repool mw6
* 01:09 paladox: reinstall mw5
* 00:59 Southparkfan: temporarily restored mwlogtemp key on bacula2, now removed again
* 00:33 paladox: reinstall mw6
* 00:28 paladox: rm -rf /root /etc/ssl/private /var/log on mw6
* 00:28 paladox: remove mw6.miraheze.org from puppet
* 00:22 paladox: downtime mw6
* 00:22 paladox: depool mw6
* 00:21 paladox: repool mw4
* 00:13 Southparkfan: kill nginx & fw rules on mw5

## 2020-12-22 

* 23:39 paladox: reinstall mw4 using a fresh debian copy
* 23:38 paladox: shutdown mw4
* 23:37 paladox: rm -rf /root /etc/ssl/private /var/log on mw4
* 23:36 paladox: remove mw4.miraheze.org from puppet
* 23:36 paladox: downtimed mw4
* 23:35 paladox: depool mw4
* 22:55 paladox: depool/repool mw4 and increase its core by one to 6
* 22:31 paladox: rebuild lc on mw* and jobrunner*
* 22:25 paladox: rm -rf /srv/mediawiki/w/extensions/Widgets/compiled_templates/** - mw*/jobrunner*/test2
* 15:07 paladox: depool/repool mw7 (recloning mediawiki)
* 14:48 paladox: depool/repool mw6 (recloning mediawiki)
* 14:29 paladox: recloning mediawiki on jobrunner[12]
* 14:28 paladox: depool/repool mw5 (recloning mediawiki)
* 14:09 paladox: depool/repool mw4 (recloning mediawiki)
* 00:51 paladox: set cp6/7 cores to 3
* 00:36 paladox: depool mw[67] and repool, also increase core by 1 (so 5 instead of 4) experimenting to seem if that'll help with the load
* 00:24 paladox: depool mw[45] and repool, also increase core by 1 (so 5 instead of 4) experimenting to seem if that'll help with the load
* 00:18 paladox: root@gluster1:/home/paladox# gluster volume set mvol performance.nl-cache off

## 2020-12-21 

* 23:14 paladox: rebuild lc on mw* and jobrunner*
* 21:09 paladox: root@jobrunner1:/var/spool/cron/crontabs# /usr/local/bin/foreachwikiindblist /srv/mediawiki/w/cache/databases.json /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/generateMirahezeSitemap.php
* 15:46 RhinosF1: run x2 due to memory usage causing failure
* 15:43 RhinosF1: rhinos@jobrunner1:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/runJobs.php --wiki=metawiki

## 2020-12-20 

* 17:08 Southparkfan: remove atop from test2
* 16:46 paladox: set php childs to 18 on mw[4567] (experimenting with different settings)
* 16:42 Southparkfan: install fatrace as well on test2
* 16:38 Southparkfan: install atop on test2
* 16:38 paladox: depooled/repooled mw[45] (experimenting with 20 rather than 26 php childs to see if it'll help the load)
* 16:13 paladox: root@gluster1:/home/paladox# gluster volume set mvol performance.nl-cache on
* 16:11 paladox: shutdown -r on db7

## 2020-12-19 

* 21:21 Southparkfan: varnish ban all load.php requests for metawiki (campaign custom JS)
* 10:52 Reception123: added reviwikiwiki discord webhook

## 2020-12-18 

* 18:28 paladox: root@jobrunner1:/home/paladox# sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/w/cache/databases.json /srv/mediawiki/w/maintenance/cleanupUploadStash.php
* 17:04 paladox: deleted files in temp folder for att and metawiki on gluster
* 16:50 paladox: remove timeline_ and php* files on mw[67] - /tmp
* 16:49 paladox: remove timeline_ and php* files on mw[45] - /tmp
* 15:54 paladox: upgrade elasticsearch on graylog1
* 15:36 paladox: upgrade mathoid on mw[4567], test2 and jobrunner[12]
* 15:19 paladox: set retention to 30 indexes on graylog (so delete old indexes if the indexes go >30)
* 14:49 paladox: upgrade other packages too on test2
* 14:49 paladox: upgrade kernel on test2
* 14:36 paladox: depool mw[4567] and repool
* 02:13 paladox: increase graylog1 disk by 100gb

## 2020-12-17 

* 22:32 paladox: remount /mnt/mediawiki-static on mw* and jobrunner*

## 2020-12-16 

* 16:55 paladox: cp9: varnish> ban obj.status == 301 && req.http.Host == varch.miraheze.org
* 13:49 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki vanataswiki /home/reception/Wikipedia-20201215181825.xml --report 1
* 13:49 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki vanataswiki /home/reception/Wikipedia-20201215175034.xml --report 1
* 13:48 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki vanataswiki /home/reception/Wikipedia-20201215160248.xml --report 1
* 06:10 Reception123: renamed lingnlangwiki to linglotwiki.
* 06:05 Reception123: reception@jobrunner1:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki robinsonowiewiki /home/reception/Nightwood-20201117181730.xml --report 1

## 2020-12-15 

* 06:14 Reception123: reception@jobrunner1:/srv/mediawiki/w/extensions/ManageWiki/maintenance$ sudo -u www-data php populateGroupPermissionsWithDefaults.php --wiki vmcodexwiki --overwrite

## 2020-12-14 

* 22:10 paladox: stop replica on db7 for a day
* 21:53 Southparkfan: hard blocked an IP in ufw on cache proxies (see staffwiki)
* 20:48 Reception123: ran GDPR removal script
* 20:45 paladox: install sysstat on db13
* 20:30 paladox: upgrade db7 to debian 10.7 and upgrade mariadb to 10.4.17
* 20:21 paladox: reboot db13
* 20:19 paladox: upgrade db13 to debian 10.7 and upgrade mariadb to 10.4.17
* 19:46 paladox: kill long running puppet process on db13
* 19:26 paladox: depool mw[67] and repool
* 18:25 paladox: stopped mysql on db7 - experimenting
* 17:22 paladox: set gluster1 cores to 3
* 17:15 paladox: set gluster i/o threads to 8
* 15:15 paladox: root@test2:/srv/mediawiki/w/extensions/ManageWiki/maintenance# sudo -u www-data php populateGroupPermissionsWithDefaults.php --wiki pkvastwiki --overwrite

## 2020-12-13 

* 18:44 paladox: upgrade rdb2 to debian 10.7
* 18:38 paladox: upgrade rdb1 to debian 10.7
* 18:22 Southparkfan: accidentally killed redis on rdb2
* 17:39 paladox: root@jobrunner1:/srv/mediawiki/w/maintenance# /usr/local/bin/foreachwikiindblist /srv/mediawiki/w/cache/databases.json /srv/mediawiki/w/maintenance/rebuildmessages.php
* 17:01 paladox: rebuild lc on mw* and jobrunner*
* 16:54 paladox: rebuild lc on test2
* 11:56 Reception123: added batfamilywiki discord webhook
* 11:54 Reception123: added snapwikiwiki discord webhook
* 06:12 Reception123: reception@jobrunner1:/srv/mediawiki/w/maintenance$ sudo -u www-data php deleteBatch.php --wiki greatestmovieswiki --r "Requested (T6586)" /home/reception/greatestmovies.txt
* 06:04 Reception123: reception@jobrunner2:/srv/mediawiki/w/maintenance$ sudo -u www-data php deleteBatch.php --wiki awfulmovieswiki --r "Requested (T6586)" /home/reception/awfulmovies.txt

## 2020-12-12 

* 23:31 paladox: restart mysql on db13 as it lost connection when running a query thus breaking it
* 22:00 paladox: upgrade grafana on mon1
* 21:49 paladox: restart nginx & php7.3-fpm on mw* and jobrunner. php being slow.
* 21:30 paladox: killed a varnish process on cp9 as the varnish service wasn't maintaining it causing the service to fail when restarting.
* 19:51 Reception123: reception@jobrunner1:/srv/mediawiki/w/maintenance$ sudo -u www-data php rebuildImages.php --wiki schizoidnightmareswiki
* 10:45 Reception123: chown www-data:www-data /mnt/mediawiki-static/yazzwiki
* 09:19 Reception123: stripped 2FA from a user on phabricator

## 2020-12-10 

* 15:18 paladox: disable queued tracker on matomo
* 12:25 paladox: root@jobrunner1:/home/paladox# sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/w/cache/databases.json /srv/mediawiki/w/maintenance/runJobs.php

## 2020-12-09 

* 17:42 Reception123: removed bugs@ mail redirect from sre@
* 17:40 Reception123: deleted emails from PhabricatorManiphestApplication, no longer in use
* 00:59 Universal_Omega: sudo -u www-data rm /srv/mediawiki/w/cache/lggyaanipediawiki.json on mw* and jobrunner*
* 00:37 Universal_Omega: INSERT INTO slot_roles (role_id, role_name) VALUES (1, 'main'); on limpdwiki

## 2020-12-08 

* 21:49 Universal_Omega: universalomega@jobrunner1:~$ sudo -u www-data php /srv/mediawiki/w/extensions/Wikibase/repo/maintenance/rebuildItemTerms.php --wiki nbdbwiki
* 21:49 Universal_Omega: universalomega@jobrunner1:~$ sudo -u www-data php /srv/mediawiki/w/extensions/Wikibase/repo/maintenance/rebuildPropertyTerms.php --wiki nbdbwiki
* 21:48 Universal_Omega: universalomega@jobrunner1:~$ sudo -u www-data php /srv/mediawiki/w/extensions/Wikibase/repo/maintenance/rebuildTermSqlIndex.php --wiki nbdbwiki --entity-type=property --rebuild-all-terms
* 21:48 Universal_Omega: universalomega@jobrunner1:~$ sudo -u www-data php /srv/mediawiki/w/extensions/Wikibase/repo/maintenance/rebuildTermSqlIndex.php --wiki nbdbwiki --entity-type=item --rebuild-all-terms
* 21:41 paladox: rebuild lc on test2
* 21:21 paladox: rebuild lc on mw[4567] and jobrunner[12]
* 21:20 paladox: depool, repool mw[4567]
* 20:34 paladox: rebuild lc on test2
* 16:28 paladox: depool and repool mw[4567] for kernel upgrade
* 16:25 paladox: upgrade phab1 to debian 10.7
* 16:22 Reception123: apt-get upgrade on cp[67] and reboot both
* 16:20 paladox: upgrade ns1 to debian 10.7
* 16:19 paladox: upgrade ns2 to debian 10.7
* 16:15 paladox: upgrade services[12] to debian 10.7
* 16:14 paladox: upgrade mon1 to debian 10.7
* 16:13 paladox: upgrade graylog1 to debian 10.7
* 16:12 Reception123: apt-get upgrade and reboot cp9
* 16:10 paladox: upgrade mail1 to debian 10.7
* 16:08 paladox: upgrade ldap1 to debian 10.7
* 16:04 Reception123: apt-get upgrade and reboot cp3
* 15:45 Reception123: reception@jobrunner2:/srv/mediawiki/w/maintenance$ sudo -u www-data php resetUserEmail.php KitaXitDelta <redacted> --wiki loginwiki (T6561 - identity confirmed via Discord verified account)
* 15:27 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildLocalisationCache.php --wiki loginwiki on mw* and jbr*
* 15:26 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/mergeMessageFileList.php --output /srv/mediawiki/config/ExtensionMessageFiles.php --wiki loginwiki (requested by UO) on mw* and jbr*
* 15:12 Reception123: apt-get upgrade, reboot jobrunner2
* 15:09 Reception123: apt-get upgrade, reboot jobrunner1
* 15:02 Reception123: repool mw7
* 15:01 Reception123: apt-get upgrade, depool mw7, reboot mw7
* 14:58 Reception123: repool mw6
* 14:57 Reception123: apt-get upgrade, depool mw6, reboot mw6
* 14:53 Reception123: repool mw5
* 14:52 Reception123: apt-get upgrade, depool mw5, reboot mw5
* 14:49 Reception123: repool mw4
* 14:49 Reception123: apt-get upgrade, depool mw4, reboot mw4
* 12:49 Reception123: unmount and mount gluster on test2
* 06:54 Reception123: upgraded test2 to deb 10.7 + reboot
* 02:51 paladox: increase puppet2 cores to 4
* 02:46 paladox: rm /var/spool/cron/crontabs/root on all servers
* 00:04 paladox: set mw[45] cores to 4
* 00:04 paladox: set puppet2 cores to 3

## 2020-12-07 

* 23:23 paladox: rebuild lc on mw[4567] and jobrunner[12]
* 22:49 Universal_Omega: universalomega@jobrunner2:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --report=1 --wiki callipediawiki /home/universalomega/import7.xml
* 19:32 Universal_Omega: universalomega@jobrunner2:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki callipediawiki /home/universalomega/import6.xml
* 17:29 paladox: salt-ssh -E "mw.*|jobrunner.*" cmd.run "rm /srvawiki/w/cache/chimerawiki.json"
* 15:56 paladox: rebuild lc on mw[4567] and jobrunner[12]
* 14:48 Universal_Omega: universalomega@jobrunner2:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki callipediawiki /home/universalomega/import5.xml
* 02:01 Universal_Omega: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --report=1 --wiki callipediawiki /home/universalomega/import4.xml
* 01:47 Universal_Omega: universalomega@jobrunner1:~$ sudo -u www-data /usr/local/bin/foreachwikiindblist /home/universalomega/commentstreams.json /srv/mediawiki/w/maintenance/sql.php /home/universalomega/addCommentId.sql
* 00:40 paladox: rebuild lc on mw[4567] and jobrunner[12]
* 00:08 paladox: deleted loginwiki & testwiki in rdb2

## 2020-12-06 

* 23:52 paladox: reset a user token on loginwiki
* 23:07 Universal_Omega: universalomega@jobrunner1:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/refreshLinks.php --wiki nonciclopediawiki
* 23:00 Universal_Omega:  sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --report=1 --wiki callipediawiki /home/universalomega/import3.xml on Jobrunner2
* 22:53 Universal_Omega: universalomega@jobrunner2:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --report=1 --wiki callipediawiki /home/universalomega/import2.xml
* 22:03 Universal_Omega: sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/w/cache/databases.json /home/paladox/resetWikiCaches.php on jobrunner1
* 22:03 Universal_Omega: UPDATE mw_settings set s_settings = JSON_REMOVE(s_settings, '$.wgAllowImageTag');
* 21:37 paladox: reboot bacula2
* 21:36 paladox: upgrade bacula2 to debian 10.7
* 21:25 paladox: refresh backups on bacula2
* 19:53 Reception123: added dmehus to stewards@ mail list
* 19:51 Reception123: added mrjaroslavik back to cvt@ mail list
* 19:23 Southparkfan: removed posixaccount class from my ldap account
* 17:40 paladox: repooled mw7
* 11:56 Reception123: added discord webhook for mcpirevivalwiki
* 06:24 Universal_Omega:  sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildLocalisationCache.php --wiki loginwiki on mw* and Jbr*

## 2020-12-05 

* 23:45 Universal_Omega: universalomega@jobrunner1:/srv/mediawiki/w/maintenance$ sudo -u www-data php deleteBatch.php --wiki allthetropeswiki --r "Requested (T6228)" /home/universalomega/deletebatch.txt
* 23:25 Universal_Omega: DELETE FROM oldimage WHERE oi_archive_name=*
**using sql.php on allthetropeswiki**

* 23:21 Universal_Omega: DELETE FROM oldimage WHERE oi_name='145828282445.png'; using sql.php on allthetropeswiki
* 20:18 Universal_Omega: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --report=1 --wiki callipediawiki /home/universalomega/import1.xml on Jobrunner1
* 19:51 Universal_Omega: DROP TABLE IF EXISTS thread,thread_history,thread_pending_relationship,thread_reaction,historical_thread,user_message_state; using sql.php (allthetropeswiki)
* 19:27 Reception123: created ldap/mail account for bots-noreply
* 18:48 Universal_Omega: INSERT INTO content_models (model_id, model_name) VALUES (5, 'json'); using sql.php on jobrunner1 on mcuwiki
* 18:47 Universal_Omega: INSERT INTO content_models (model_id, model_name) VALUES (4, 'Scribunto'); using sql.php on jobrunner1 on mcuwiki
* 18:47 Universal_Omega: INSERT INTO content_models (model_id, model_name) VALUES (3, 'javascript'); using sql.php on jobrunner1 on mcuwiki
* 18:46 Universal_Omega: INSERT INTO content_models (model_id, model_name) VALUES (2, 'css'); using sql.php on jobrunner1
* 18:46 Universal_Omega: INSERT INTO content_models (model_id, model_name) VALUES (1, 'wikitext'); using sql.php on jobrunner1
* 01:54 paladox: set mw[4567] cores at 5; set puppet2 cores to 2
* 01:34 paladox: depool; repool; mw[67]
* 00:53 paladox: depool; repool; mw[45]

## 2020-12-04 

* 21:34 John: requested cancellation of misc1
* 21:29 John: removed misc1 from puppetserver
* 21:16 John: stopped postfix/dovecot on misc1
* 17:03 paladox: experimenting with different cores for puppet2
* 12:55 paladox: set puppet2 cpu cores to 3 (down from 4)
* 12:30 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildLocalisationCache.php --wiki loginwiki on mw* and jbr*
* 11:20 paladox: depool mw[67], change cpu cores to 4 and repool
* 11:09 paladox: increase puppet2 cores to 4 and ram to 6gb
* 11:06 paladox: decrease graylogs cores to 2
* 10:51 paladox: depool mw[45], change cpu cores to 4 and repool
* 07:18 Reception123: sudo -u www-data rm /srv/mediawiki/w/cache/planetnomadswiki.json on mw*
* 07:00 Reception123: $cw = new CreateWikiJson( 'planetnomadswiki' ); $cw->resetWiki();
* 06:40 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildLocalisationCache.php --wiki loginwiki on mw* and jbr*

## 2020-12-03 

* 18:55 Universal_Omega: universalomega@jobrunner1:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/initEditCount.php --wiki snapwikiwiki
* 18:49 Universal_Omega: universalomega@jobrunner1:/srv/mediawiki/w/extensions/MirahezeMagic/maintenance$ sudo -u www-data php assignImportedEdits.php --wiki snapwikiwiki
* 18:24 paladox: rm /srv/mediawiki/w/cache/aboutoflinuxwiki.json on mw[4567] and jobrunner[12]
* 17:50 paladox: increase mw[45] cores to 5 each.
* 17:43 paladox: increase mw[67] cores to 5 each.
* 16:58 paladox: depool mw[67] & increase ram to 4gb & repool
* 16:50 paladox: depool mw[45] & increase ram to 4gb & repool
* 16:40 paladox: lower services[12] cpus to 1 each. They do not need 2 each.
* 16:26 paladox: increase graylog1 cpu by (so 3)
* 13:11 Reception123: reception@jobrunner2:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --report=1 --wiki tripartitewiki /home/reception/bloodandsoil_pages_full.xml
* 13:07 Reception123: reception@jobrunner2:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --report=1 --wiki snapwikiwiki /home/reception/Snap_Wiki_Dump.xml
* 06:33 Reception123: deleted F916211, F679416, F986734, F987605
* 06:13 Reception123: deleted F869771 on phabv
* 06:07 Reception123: deleted F1136416 on phabricator
* 05:56 Reception123: deleted phabricator files F875891 F876846 F935556 F944621 F983497 F1014421 F1081385 (T6541)
* 05:53 Reception123: deleted phabricator files F827754, F737704, F853444 (T6541)

## 2020-12-02 

* 21:29 paladox: rm /srv/mediawiki/w/cache/nicegachatuberswikiwiki.json on mw[4567] and jobrunner[12]
* 21:29 paladox: root@test2:/srv/mediawiki/w/extensions/ManageWiki/maintenance# sudo -u www-data php toggleExtension.php --wiki nicegachatuberswikiwiki templatedata
* 21:28 paladox: rm /srv/mediawiki/w/cache/marvelwiki.json on mw[4567] and jobrunner[12]
* 21:28 paladox: root@test2:/srv/mediawiki/w/extensions/ManageWiki/maintenance# sudo -u www-data php toggleExtension.php --wiki marvelwiki templatedata
* 21:27 paladox: rm /srv/mediawiki/w/cache/choralforumwiki.json on mw[4567] and jobrunner[12]
* 21:27 paladox: root@test2:/srv/mediawiki/w/extensions/ManageWiki/maintenance# sudo -u www-data php toggleExtension.php --wiki choralforumwiki templatedata
* 21:26 paladox: rm /srv/mediawiki/w/cache/choralwiki.json on mw[4567] and jobrunner[12]
* 21:26 paladox: root@test2:/srv/mediawiki/w/extensions/ManageWiki/maintenance# sudo -u www-data php toggleExtension.php --wiki choralwiki templatedata
* 21:25 paladox: rm /srv/mediawiki/w/cache/keisariyparxiwiki.json on mw[4567] and jobrunner[12]
* 21:25 paladox: root@test2:/srv/mediawiki/w/extensions/ManageWiki/maintenance# sudo -u www-data php toggleExtension.php --wiki keisariyparxiwiki templatedata
* 21:25 paladox: rm /srv/mediawiki/w/cache/yandrosswiki.json on mw[4567] and jobrunner[12]
* 21:24 paladox: root@test2:/srv/mediawiki/w/extensions/ManageWiki/maintenance# sudo -u www-data php toggleExtension.php --wiki yandrosswiki templatedata
* 21:23 paladox: rm /srv/mediawiki/w/cache/slscificonventionwiki.json on mw[4567] and jobrunner[12]
* 21:23 paladox: root@test2:/srv/mediawiki/w/extensions/ManageWiki/maintenance# sudo -u www-data php toggleExtension.php --wiki slscificonventionwiki templatedata
* 21:22 paladox: rm /srv/mediawiki/w/cache/frmblmswiki.json on mw[4567] and jobrunner[12]
* 21:22 paladox: root@test2:/srv/mediawiki/w/extensions/ManageWiki/maintenance# sudo -u www-data php toggleExtension.php --wiki frmblmswiki templatedata
* 21:20 paladox: rm /srv/mediawiki/w/cache/securitylogwikiwiki.json on mw[4567] and jobrunner[12]
* 21:20 paladox: root@test2:/srv/mediawiki/w/extensions/ManageWiki/maintenance# sudo -u www-data php toggleExtension.php --wiki securitylogwikiwiki templatedata
* 21:18 paladox: rm /srv/mediawiki/w/cache/ddlcmodswiki.json on mw[4567] and jobrunner[12]
* 21:18 paladox: root@test2:/srv/mediawiki/w/extensions/ManageWiki/maintenance# sudo -u www-data php toggleExtension.php --wiki ddlcmodswiki templatedata
* 21:14 paladox: rm /srv/mediawiki/w/cache/undumpedwiki.json on mw[4567] and jobrunner[12]
* 21:14 paladox: root@test2:/srv/mediawiki/w/extensions/ManageWiki/maintenance# sudo -u www-data php toggleExtension.php --wiki undumpedwiki templatedata
* 20:47 paladox: root@mail1:/srv/roundcubemail/skins/elastic# npm install -g less
* 19:56 John: letting dns traffic move from misc1 -> mail1 for mail
* 19:09 Reception123: DELETED and DROPPED mcuwiki
* 14:22 Reception123: sudo apt-get upgrade on mw5/mw6/test2
* 08:38 Reception123: reception@jobrunner1:/srv/mediawiki/w/maintenance$ sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --report=1 --wiki ascotwiki /home/reception/delbackups3/ascotwiki.xml
* 08:34 Reception123: reception@jobrunner2:/srv/mediawiki/w/maintenance$ sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --report=1 --wiki thehorriblemusicandsongswikiawiki /home/reception/horriblemusicandsongs_pages_full.xml
* 08:31 Reception123: renamed sephsfunnieswiki to sephspacewiki
* 00:34 paladox: curl -XPUT " [http://localhost:9200/_all/_settings](http://localhost:9200/_all/_settings)" -d '{ "index" : { "max_result_window" : 90000000 } }' -H 'Content-Type: application/json'
* 00:33 paladox: root@graylog1:/home/paladox# curl -XPUT " [http://localhost:9200/_all/_settings](http://localhost:9200/_all/_settings)" -d '{ "index" : { "max_result_window" : 900000 } }' -H 'Content-Type: application/json'

## 2020-12-01 

* 15:50 paladox: root@graylog1:/home/paladox# curl -XPUT " [http://localhost:9200/_settings](http://localhost:9200/_settings)" -d '{ "index" : { "max_result_window" : 90000 } }' -H 'Content-Type: application/json'
* 06:43 Reception123: reception@jobrunner1:/srv/mediawiki/w/maintenance$ sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --report=1 --wiki callipediawiki /home/reception/Vital4.xml

## 2020-11-30 

* 23:53 paladox: reboot jobrunner1
* 21:32 paladox: root@jobrunner1:/srv/mediawiki/w# /usr/local/bin/foreachwikiindblist /srv/mediawiki/w/cache/databases.json /srv/mediawiki/w/maintenance/runJobs.php
* 21:30 paladox: rm /srv/mediawiki/w/cache/starwarswiki.json on mw[4567] and jobrunner[12]
* 21:01 Reception123: deleted and dropped [https://phabricator.miraheze.org/P355](https://phabricator.miraheze.org/P355)
* 19:11 paladox: root@gluster2:/home/paladox# gluster volume set mvol rebal-throttle normal
* 18:33 Reception123: deleted @Verne on Phabricator
* 17:15 paladox: root@gluster2:/home/paladox# gluster volume set mvol rebal-throttle lazy
* 17:02 Reception123: sudo -u www-data php /srv/mediawiki/w/extensions/CreateWiki/maintenance/deleteWikis.php --wiki=loginwiki Reception123 --delete
* 16:25 Reception123: bash ./delbackups.sh /home/reception/backupwikis.dblist /srv/mediawiki/w/maintenance/dumpBackup.php (delbackups)
* 15:28 paladox: root@phab1:/srv/phab# rm -rf libphutil
* 15:28 paladox: upgrade phabricator
* 15:24 paladox: upgrade base-files libpq5 libx11-6 libx11-data tzdata on ns2
* 15:23 paladox: upgrade base-files libpq5 libx11-6 libx11-data tzdata on ns1
* 15:12 paladox: reboot ns1 - freezing - high load
* 14:19 paladox: root@gluster2:/home/paladox# gluster volume rebalance mvol start

## 2020-11-29 

* 21:37 Southparkfan: run pveperf on cloud1
* 16:59 paladox: reset users token on linguapediawiki
* 16:30 Reception123: reception@jobrunner1:/srv/mediawiki/w/maintenance$ sudo -u www-data php runJobs.php --wiki metawiki
* 09:32 Reception123: renamed customromwiki to androidwiki
* 09:28 Reception123: renamed lexipediawiki to linguapediawiki

## 2020-11-28 

* 21:46 paladox: root@gluster2:/home/paladox# gluster volume set mvol rebal-throttle lazy
* 21:42 paladox: root@gluster2:/home/paladox# gluster volume set mvol rebal-throttle aggressive
* 21:14 paladox: rm /srv/mediawiki/w/cache/terreanwiki.json on mw[4567] and jobrunner[12]
* 20:04 paladox: rm /srv/mediawiki/w/cache/badomainwiki.json on mw[4567] and jobrunner[12]
* 19:48 Southparkfan: restart varnishncsa on cp9
* 17:47 Universal_Omega: sudo -u www-data php /srv/mediawiki/w/extensions/ManageWiki/maintenance/toggleExtension.php --wiki schizoidnightmareswiki urlshortener --disable
* 17:47 Universal_Omega: sudo -u www-data php /srv/mediawiki/w/extensions/ManageWiki/maintenance/toggleExtension.php --wiki macfan4000wiki urlshortener --disable
* 17:43 Universal_Omega: sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/w/cache/databases.json /srv/mediawiki/w/extensions/ManageWiki/maintenance/toggleExtension.php urlshortener on Jobrunner1
* 14:54 paladox: rebuild lc on mw[4567] and jobrunner[12]
* 14:42 paladox: upgrade graylog-server to 4.0.1
* 14:18 paladox: root@test2:/srv/mediawiki/w/extensions/ManageWiki/maintenance# sudo -u www-data php toggleExtension.php --wiki tualatinbasewiki Bootstrap --disable
* 14:18 paladox: root@test2:/srv/mediawiki/w/extensions/ManageWiki/maintenance# sudo -u www-data php toggleExtension.php --wiki trashepisodeswiki Bootstrap --disable
* 14:17 paladox: root@test2:/srv/mediawiki/w/extensions/ManageWiki/maintenance# sudo -u www-data php toggleExtension.php --wiki libraryofanamwiki Bootstrap --disable
* 14:17 paladox: root@test2:/srv/mediawiki/w/extensions/ManageWiki/maintenance# sudo -u www-data php toggleExtension.php --wiki cristianopediawiki Bootstrap --disable
* 14:12 paladox: root@test2:/home/paladox# /usr/local/bin/foreachwikiindblist /home/paladox/templatewizard.json /srv/mediawiki/w/extensions/ManageWiki/maintenance/toggleExtension.php templatedata
* 12:54 John: remounted mediawiki-static on mw5
* 03:56 Universal_Omega: sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildLocalisationCache.php --wiki loginwiki on mw* and jobrunner*
* 03:03 Universal_Omega: sudo -u www-data /usr/local/bin/foreachwikiindblist /home/universalomega/mobilefrontend.json /srv/mediawiki/w/extensions/ManageWiki/maintenance/toggleExtension.php minervaneue on Jobrunner1
* 00:27 Universal_Omega: sudo -u www-data /usr/local/bin/foreachwikiindblist /home/universalomega/visualeditor.json /srv/mediawiki/w/extensions/ManageWiki/maintenance/toggleExtension.php templatedata on Jobrunner1

## 2020-11-27 

* 23:15 Universal_Omega: sudo -u www-data /usr/local/bin/foreachwikiindblist /home/universalomega/templatewizard.json /srv/mediawiki/w/extensions/ManageWiki/maintenance/toggleExtension.php templatedata on jobrunner1
* 22:53 Universal_Omega: sudo -u www-data /usr/local/bin/foreachwikiindblist /home/universalomega/translate.json /srv/mediawiki/w/extensions/ManageWiki/maintenance/toggleExtension.php universallanguageselector on Jobrunner1
* 22:33 Universal_Omega: sudo -u www-data /usr/local/bin/foreachwikiindblist /home/universalomega/gettingstarted.json /srv/mediawiki/w/extensions/ManageWiki/maintenance/toggleExtension.php guidedtour on Jobrunner1
* 19:18 Reception123: MariaDB [metawiki]> DELETE FROM echo_unread_wikis WHERE euw_user = '19';
* 19:14 Reception123: MariaDB [metawiki]> DELETE FROM echo_unread_wikis WHERE euw_user = '6758';
* 18:48 Universal_Omega: sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildLocalisationCache.php --wiki loginwiki on mw* and jobrunner*
* 18:41 Reception123: MariaDB [staffwiki]> UPDATE echo_notification SET notification_read_timestamp = '20201127183900' WHERE notification_user = '15' AND notification_event = '61';
* 07:40 Universal_Omega: sudo -u www-data php /srv/mediawiki/w/maintenance/initEditCount.php --wiki dcmultiversewiki on Jobrunner1
* 07:25 Universal_Omega: sudo -u www-data php /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/assignImportedEdits.php --wiki dcmultiversewiki on Jobrunner1
* 06:45 Reception123: repool mw7
* 06:41 Reception123: reboot mw7
* 06:40 Reception123: depool mw7

## 2020-11-26 

* 21:45 paladox: root@gluster2:/home/paladox# gluster volume rebalance mvol fix-layout start
* 21:33 paladox: increase gluster2 disk by 100gb
* 20:44 Reception123: reception@jobrunner1:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/initSiteStats.php --update --wiki moviepediawiki
* 20:14 paladox: rebuild lc on jobrunner*
* 19:47 paladox: rebuild lc on mw[4567]
* 19:43 paladox: depool mw[4567] and repool
* 15:13 Reception123: reception@jobrunner1:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/initSiteStats.php --update --wiki gyaanipediawiki
* 08:20 Reception123: running wikibackups on jobrunner1 (bash ./wikibackups.sh /home/reception/backupwikis.dblist /srv/mediawiki/w/maintenance/dumpBackup.php)
* 08:06 Reception123: reception@jobrunner1:/srv/mediawiki/w/maintenance$ sudo -u www-data php recountCategories.php --mode=pages --wiki mylittleponywiki
* 06:49 Reception123: reception@jobrunner1:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/importImages.php --wiki=minelandwiki --search-recursively --skip-dupes /home/reception/minelandimg

## 2020-11-25 

* 20:35 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --report=1 --wiki minelandwiki /home/reception/mineland.xml

## 2020-11-24 

* 17:08 Reception123: changed metawiki discord webhook (for a user's personal server)
* 16:10 paladox: root@graylog1:/home/paladox# curl -H 'Content-Type: application/json' -XPUT ' [http://localhost:9200/_all/_settings'](http://localhost:9200/_all/_settings') -d '{"index.codec" : "default"}'
* 16:00 John: $wr = new WikiRequest( 15358 ); $wr->decline( 'No subdomain specified', User::newFromName( 'John' ) );
* 12:31 Reception123: reception@jobrunner2:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/importImages.php --wiki=dragalialostwiki --search-recursively --skip-dupes /home/reception/dragalialostgamepediawiki/images

## 2020-11-23 

* 19:13 Reception123: disabled BlackWidowMovieEditor on phab
* 17:17 paladox: rebuild lc on mw* and jobrunner*
* 17:06 paladox: root@jobrunner1:/home/paladox# sudo -u www-data php /srv/mediawiki/w/extensions/CreateWiki/maintenance/renameWiki.php --wiki=loginwiki --rename ashinawiki iolrathenerewiki paladox
* 11:22 Reception123: reception@jobrunner1:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/initSiteStats.php --update --wiki gyaanipediawiki
* 07:03 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildLocalisationCache.php --wiki loginwiki on mw* and jbr*
* 00:26 paladox: rebuild lc on mw* and jobrunner*

## 2020-11-22 

* 23:17 Southparkfan: install security updates (mainly krb5)
* 23:10 Southparkfan: remove all php* files in /tmp on mediawiki servers
* 22:53 Southparkfan: restart jobrunner/jobchron for syslog test
* 21:29 Southparkfan: remove allow 443 on graylog1
* 17:23 Universal_Omega: universalomega@jobrunner1:~$ sudo -u www-data /usr/local/bin/foreachwikiindblist /home/universalomega/popups.json /srv/mediawiki/w/extensions/ManageWiki/maintenance/toggleExtension.php textextracts
* 16:58 Universal_Omega: universalomega@jobrunner1:~$ sudo -u www-data /usr/local/bin/foreachwikiindblist /home/universalomega/popups.json /srv/mediawiki/w/extensions/ManageWiki/maintenance/toggleExtension.php pageimages
* 04:20 Universal_Omega: sudo -u www-data php /srv/mediawiki/w/maintenance/initSiteStats.php --update --wiki mcuwiki on Jobrunner1
* 04:16 Universal_Omega: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --report=1 --wiki mcuwiki /home/universalomega/mcuwiki/mcuwiki[1-16].xml (16 XML files) on jobrunner1
* 02:33 paladox: graylog1: delete all data in elasticsearch
* 02:19 paladox: graylog1: enable best_compression for index on elasticsearch
* 01:33 paladox: rebuild lc on mw* and jobrunner*

## 2020-11-21 

* 23:38 paladox: $cw = new RemoteWiki( 'vsfanwiki' ); $cw->setServerName(* ); $cw->commit(); - jobrunner1
* 23:18 paladox: delete vsfanwiki redis key on jobrunner1
* 22:44 paladox: root@jobrunner1:/srv/mediawiki/w/maintenance# /usr/local/bin/foreachwikiindblist /srv/mediawiki/w/cache/databases.json /srv/mediawiki/w/maintenance/runJobs.php
* 22:31 Zppix: update status for wiki request #15316 to  declined  via sql.php on jobrunner1
* 21:45 paladox: upgrade some packages on graylog1
* 16:56 paladox: upgrade tzdata on graylog1
* 16:42 paladox: rebuild lc on test2
* 07:28 Reception123: reception@jobrunner1:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/initSiteStats.php --update --wiki gyaanipediawiki

## 2020-11-20 

* 20:42 paladox: revert depool/repool. Seems the change works without having to do that.
* 20:42 paladox: rebuild lc on mw* and jobrunner*
* 20:39 paladox: depool mw[4567] and repool
* 15:15 Reception123: MariaDB [phabricator_dashboard]> UPDATE dashboard SET status = "archived" WHERE id = '27';
* 12:17 Reception123: on jobrunner2
* 12:17 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --report=1 --wiki gyaanipediawiki /home/reception/gyaanipedia_pages_full.xml

## 2020-11-19 

* 22:19 paladox: fix content_models on ucroniaswiki
* 22:14 paladox: MariaDB [ucroniaswiki]> INSERT INTO content_models (model_id, model_name) VALUES (1, 'wikitext');
* 19:56 Reception123: MariaDB [phabricator_dashboard]> UPDATE dashboard SET status = "archived" WHERE id = '35';
* 19:56 Reception123: MariaDB [phabricator_dashboard]> UPDATE dashboard SET status = "archived" WHERE id = '36';
* 19:36 Universal_Omega: sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildLocalisationCache.php --wiki loginwiki on mw* and jbr*
* 19:35 Universal_Omega: sudo -u www-data php /srv/mediawiki/w/maintenance/mergeMessageFileList.php --output /srv/mediawiki/config/ExtensionMessageFiles.php --wiki loginwiki on mw* and jbr*
* 18:28 Reception123: re-enable BlackWidowMovieEditor on Phab
* 01:48 Universal_Omega: universalomega@jobrunner1:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/initSiteStats.php --update --wiki mcuwiki
* 00:28 Universal_Omega: universalomega@jobrunner1:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/storage/compressOld.php --wiki mcuwiki --type gzip

## 2020-11-18 

* 22:36 Universal_Omega:  sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --report=1 --wiki mcuwiki /home/universalomega/mcuwiki2.xml on Jobrunner2
* 22:35 Universal_Omega:  sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --report=1 --wiki mcuwiki /home/universalomega/mcuwiki1.xml on Jobrunner1
* 21:30 Universal_Omega: universalomega@jobrunner1:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/deleteOldRevisions.php --wiki=allthetropeswiki --delete --page_id 229563
* 16:37 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildLocalisationCache.php --wiki loginwiki on mw* and jbr*
* 16:37 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/mergeMessageFileList.php --output /srv/mediawiki/config/ExtensionMessageFiles.php --wiki loginwiki on mw* and jbr*
* 11:05 paladox: root@jobrunner1:/srv/mediawiki/w/extensions/ManageWiki/maintenance# /usr/local/bin/foreachwikiindblist /srv/mediawiki/w/cache/databases.json /srv/mediawiki/w/extensions/ManageWiki/maintenance/modifyGroupPermission.php user --removeperms=translate-review
* 10:53 paladox: upgrade libldap-common grafana on mon1
* 10:50 paladox: upgrade openldap on ldap1
* 02:23 Universal_Omega: sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildLocalisationCache.php --wiki loginwiki on mw* and jbr*
* 02:22 Universal_Omega: sudo -u www-data php /srv/mediawiki/w/maintenance/mergeMessageFileList.php --output /srv/mediawiki/config/ExtensionMessageFiles.php --wiki loginwiki on mw* and jbr*

## 2020-11-17 

* 23:07 Universal_Omega: universalomega@jobrunner1:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/sql.php --wiki=metawiki --query="update cw_requests set cw_status = 'declined' where cw_id = 15237;"
* 23:06 paladox: MariaDB [hispano76wiki]> INSERT INTO content_models (model_id, model_name) VALUES (1, 'wikitext');
* 21:22 Reception123: MariaDB [metawiki]> UPDATE cw_requests SET cw_status = 'declined' WHERE cw_id = '15235';
* 18:27 Reception123: renamed valentinaprojectwiki to seamlywiki
* 07:40 Reception123: DELETED and DROPPED hispano76wiki
* 07:38 Reception123: DELETED and DROPPED ucroniaswiki

## 2020-11-16 

* 18:47 paladox: MariaDB [mhglobal]> update cw_wikis set wiki_closed_timestamp = NULL where wiki_closed = 0 and wiki_closed_timestamp >= 20201116000000; - updated 1691 rows.
* 18:20 paladox: reset wiki cache for all wikis using resetWikiCache script
* 17:34 Reception123: UPDATE cw_wikis SET wiki_closed = '0' AND wiki_closed_timestamp = 'NULL' WHERE wiki_closed_timestamp >= 20201116000000;
* 15:39 paladox: upgrade phabricator
* 14:35 paladox: rebuild lc on test2, jobrunner* and mw*
* 01:21 PuppyKun: ndkilla@db11.miraheze.org MariaDB [moviepediawiki]> delete from user_board where ub_id=2; Query OK, 1 row affected (0.002 sec) (per Terms of Use)

## 2020-11-15 

* 20:14 Reception123: /usr/bin/newaliases on misc1
* 20:12 Reception123: added universal omega to tech@ alias on misc1
* 20:05 Reception123: created LDAP account for Universal Omega
* 19:53 Reception123: added Universal Omega to @miraheze GH project
* 19:53 Reception123: created mail account for Universal Omega

## 2020-11-14 

* 17:05 paladox: root@test2:/srv/mediawiki/w/maintenance# sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/w/cache/databases.json /srv/mediawiki/w/maintenance/fixT260485.php --messages='/srv/mediawiki/output.json' --start='2019-09-10' --end='2020-11-25'
* 16:43 paladox: root@test2:/srv/mediawiki/w/maintenance# sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/w/cache/databases.json /srv/mediawiki/w/maintenance/fixT260485.php --messages='/srv/mediawiki/output.json' --start='2019-09-10' --end='2020-08-25'
* 16:38 paladox: root@test2:/srv/mediawiki/w/maintenance# sudo -u www-data php fixT260485.php --wiki test2wiki --messages /srv/mediawiki/output.json --start 2019-09-10 --end 2020-08-25

## 2020-11-13 

* 23:56 paladox: upgrade puppet-agent on ldap1
* 23:55 paladox: upgrade puppet-agent on ns*, mail1, gluster* and graylog*.
* 23:52 paladox: upgrade puppet-agent on cloud* and services*
* 23:51 paladox: upgrade puppet-agent on db*
* 23:50 paladox: upgrade puppet-agent on phab1 and rdb*
* 23:49 paladox: upgrade mariadb-client-10.4 mariadb-client-core-10.4 mariadb-common mysql-common libmariadb3 puppet-agent on mon1
* 23:47 paladox: upgrade grafana on mon1
* 23:45 paladox: upgrade puppet-agent on cp[367]
* 23:44 paladox: upgrade puppet-agent on mw*, jobrunner* and test2
* 23:39 paladox: upgrade puppet-agent on cp9
* 23:37 paladox: upgrade puppet-agent puppetdb puppetdb-termini puppetserver on puppet2
* 17:06 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --report=1 --wiki dragalialostwiki /home/reception/dragalialostgamepediacom-20201105-history-2.xml
* 17:05 Reception123: reception@jobrunner1:/srv/mediawiki/w/extensions/ManageWiki/maintenance$ sudo -u www-data php populateGroupPermissionsWithDefaults.php --wiki idleonwiki --overwrite

## 2020-11-12 

* 08:40 Reception123: reception@jobrunner2:~$ sudo -u www-data /usr/local/bin/foreachwikiindblist /home/reception/graph.json /srv/mediawiki/w/extensions/ManageWiki/maintenance/toggleExtension.php codeeditor
* 07:01 Reception123: reception@jobrunner2:~$ sudo -u www-data /usr/local/bin/foreachwikiindblist /home/reception/graph.json /srv/mediawiki/w/extensions/ManageWiki/maintenance/toggleExtension.php jsonconfig

## 2020-11-11 

* 22:04 paladox: rebuild lc on mw* and jobrunner*
* 21:53 paladox: root@jobrunner1:/var/spool/cron/crontabs# sudo -u www-data php  /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/generateMirahezeSitemap.php --wiki snapwikiwiki
* 21:12 paladox: MariaDB [rotompediawiki]> INSERT INTO slot_roles (role_id, role_name) VALUES (1, 'main');
* 20:28 Southparkfan: running test backup on db7
* 19:52 Southparkfan: create temp mydumper user on db7 to test backups
* 13:16 paladox: root@jobrunner1:/srv/mediawiki/w/maintenance# sudo -u www-data php deleteArchivedRevisions.php --wiki ashinawiki --delete
* 13:15 paladox: root@jobrunner1:/srv/mediawiki/w/maintenance# sudo -u www-data php deleteOldRevisions.php --wiki ashinawiki --delete
* 13:15 paladox: root@jobrunner1:/srv/mediawiki/w/maintenance# sudo -u www-data php deleteOldRevisions.php --wiki ashinawiki

## 2020-11-10 

* 18:18 paladox: root@jobrunner1:/srv/mediawiki/w/extensions/ManageWiki/maintenance# sudo -u www-data php populateWikiSettings.php --wiki loginwiki --sourcelist=setting --wgsetting=wgArticleCountMethod
* 14:35 paladox: change dns resolver on cloud[13] to 8.8.8.8 & 8.8.4.4
* 14:32 paladox: change dns resolver on cloud2 to 8.8.8.8 & 8.8.4.4

## 2020-11-09 

* 01:42 paladox: rebuild lc on mw* and jobrunner*
* 00:09 paladox: reset wiki cache for waniliawiki
* 00:07 paladox: MariaDB [mhglobal]> update cw_wikis set wiki_url = NULL where wiki_dbname = 'waniliawiki';

## 2020-11-08 

* 23:04 paladox: root@jobrunner1:/srv/mediawiki/w/extensions/ManageWiki/maintenance# /usr/local/bin/foreachwikiindblist /srv/mediawiki/w/cache/databases.json /home/paladox/resetWikiCaches.php
* 23:03 paladox: MariaDB [mhglobal]> update mw_settings set s_settings = REPLACE(s_settings,'wmgFlaggedRevsLowProfile', 'wgFlaggedRevsLowProfile');
* 23:03 paladox: MariaDB [mhglobal]> update mw_settings set s_settings = REPLACE(s_settings,'wmgSimpleFlaggedRevsUI', 'wgSimpleFlaggedRevsUI');
* 23:03 paladox: MariaDB [mhglobal]> update mw_settings set s_settings = REPLACE(s_settings,'wmgFlaggedRevsRestrictionLevels', 'wgFlaggedRevsRestrictionLevels');
* 23:02 paladox: MariaDB [mhglobal]> update mw_settings set s_settings = REPLACE(s_settings,'wmgFlaggedRevsAutoReview', 'wgFlaggedRevsAutoReview');
* 23:02 paladox: MariaDB [mhglobal]> update mw_settings set s_settings = REPLACE(s_settings,'wmgFlaggedRevsAutopromote', 'wgFlaggedRevsAutopromote');
* 23:01 paladox: MariaDB [mhglobal]> update mw_settings set s_settings = REPLACE(s_settings,'wmgFlaggedRevsTagsAuto', 'wgFlaggedRevsTagsAuto');
* 23:01 paladox: MariaDB [mhglobal]> update mw_settings set s_settings = REPLACE(s_settings,'wmgFlaggedRevsTagsRestrictions', 'wgFlaggedRevsTagsRestrictions');
* 23:00 paladox: MariaDB [mhglobal]> update mw_settings set s_settings = REPLACE(s_settings,'wmgFlaggedRevsTags', 'wgFlaggedRevsTags');
* 23:00 paladox: MariaDB [mhglobal]> update mw_settings set s_settings = REPLACE(s_settings,'wmgFlaggedRevsProtection', 'wgFlaggedRevsProtection');
* 22:59 paladox: MariaDB [mhglobal]> update mw_settings set s_settings = REPLACE(s_settings,'wmgTranslateDocumentationLanguageCode', 'wgTranslateDocumentationLanguageCode');
* 22:58 paladox: MariaDB [mhglobal]> update mw_settings set s_settings = REPLACE(s_settings,'wmgTranslateTranslationServices', 'wgTranslateTranslationServices');
* 22:58 paladox: MariaDB [mhglobal]> update mw_settings set s_settings = REPLACE(s_settings,'wmgTranslateBlacklist', 'wgTranslateBlacklist');
* 22:57 paladox: MariaDB [mhglobal]> update mw_settings set s_settings = REPLACE(s_settings,'wmgMFAutodetectMobileView', 'wgMFAutodetectMobileView');
* 22:56 paladox: MariaDB [mhglobal]> update mw_settings set s_settings = REPLACE(s_settings,'wmgWebChatClient', 'wgWebChatClient');
* 22:56 paladox: MariaDB [mhglobal]> update mw_settings set s_settings = REPLACE(s_settings,'wmgWebChatChannel', 'wgWebChatChannel');
* 22:55 paladox: MariaDB [mhglobal]> update mw_settings set s_settings = REPLACE(s_settings,'wmgWebChatServer', 'wgWebChatServer');

## 2020-11-06 

* 21:02 paladox: restart restbase on services[12]
* 20:48 paladox: cd /srv/mathoid ; rm -rf node_modules ; rm package-lock.json ; sudo -u root npm install on mw* and jobrunner*
* 20:39 paladox: cd /srv/3d2png ; rm package-lock.json ; rm -rf node_modules ; sudo -u root npm install - on mw* and jobrunner*
* 15:57 Reception123: added feedingfrenzy discord webhook
* 06:17 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --report=1 --wiki dragalialostwiki /home/reception/dragalialostgamepediacom-20201105-history.xml
* 06:00 Reception123: DELETED and DROPPED rotompediawiki

## 2020-11-05 

* 23:40 paladox: root@jobrunner1:/srv/mediawiki/w/extensions/ManageWiki/maintenance# /usr/local/bin/foreachwikiindblist /srv/mediawiki/w/cache/databases.json /srv/mediawiki/w/extensions/ManageWiki/maintenance/toggleExtension.php Bootstrap --disable
* 16:16 Reception123: added discord webhook for luigifan53wiki

## 2020-11-04 

* 09:32 paladox: cd /srv/mediawiki/w/cache && rm databases.json ; sudo -u www-data php /srv/mediawiki/w/maint*/mergeMessageFileList.php --output /srv/mediawiki/config/ExtensionMessageFiles.php --wiki loginwiki on jobrunner* (simply because the file wasn't updating thus csydeswiki using another dbcluster)
* 09:21 paladox: cd /srv/mediawiki/w/cache && rm databases.json ; sudo -u www-data php /srv/mediawiki/w/maint*/mergeMessageFileList.php --output /srv/mediawiki/config/ExtensionMessageFiles.php --wiki loginwiki on mw* (simply because the file wasn't updating thus csydeswiki using another dbcluster)
* 09:11 paladox: ignore the above, appeared to have worked (was a warning)
* 09:11 paladox: update cw_wikis set wiki_dbcluster = 'c4' where wiki_dbname = 'csydeswiki'; (couldn't use script as a fatal was occuring)
* 07:43 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildmessages.php --wiki loginwiki on mw* and jbr*
* 07:39 Reception123: $cWJ = new CreateWikiJson( 'csydeswiki' ); $cWJ->resetWiki();
* 07:14 Reception123: rm /srv/mediawiki/w/cache/csydeswiki.json  on mw* and jbr*

## 2020-11-03 

* 17:23 paladox: remove /srv/mediawiki/w/cache/solarawiki.json on mw* and jobrunner*

## 2020-11-01 

* 19:49 paladox: rm /srv/mediawiki/w/cache/testwiki.json on mw* & jobrunner*
* 19:42 Reception123: reception@jobrunner1:/srv/mediawiki/w/maintenance$ sudo -u www-data php rebuildall.php --wiki testwiki
* 13:19 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildLocalisationCache.php --wiki loginwiki' on mw* and jbr*
* 13:19 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/mergeMessageFileList.php --output /srv/mediawiki/config/ExtensionMessageFiles.php --wiki loginwiki on mw* and jbr*
* 01:58 Zppix: run jobs for metawiki on jobrunner2 (over 100 jobs were pending)

## 2020-10-31 

* 17:44 Reception123: sudo apt-get upgrade on cp7
* 15:55 Reception123: MariaDB [metawiki]> UPDATE cw_requests SET cw_status = 'declined' WHERE cw_id = '14998';
* 14:55 paladox: blank redis.log / redis.log.1 on mw* and jobrunner*.
* 14:26 paladox: clear managewiki cache
* 14:21 paladox: root@test2:/home/paladox# /usr/local/bin/foreachwikiindblist /home/paladox/kartographer.json /srv/mediawiki/w/extensions/ManageWiki/maintenance/toggleExtension.php jsonconfig
* 14:16 paladox: enable jsonconfig on christipediawiki required by Kartographer
* 14:15 paladox: enable jsonconfig on uaschoolswikiwiki required by Kartographer
* 14:10 paladox: enable jsonconfig on polskajestwiki required by Kartographer
* 14:03 paladox: remove crossreference from citronhatwiki, communitycentralbympteamwiki, dannywiki, educationpediyawiki, guiacatolicawiki, limpdwiki and tetsudouwiki
* 14:01 paladox: enable jsonconfig on dannywiki required by Kartographer
* 13:59 Southparkfan: (and I have removed the docker packages from mon1 as well)
* 13:59 Southparkfan: enable puppet on mon1
* 12:52 Southparkfan: disable puppet on mon1 & install (--no-install-recommends) docker/docker-compose on mon1
* 12:50 Reception123: reception@jobrunner2:~$ sudo -u www-data /usr/local/bin/foreachwikiindblist /home/reception/kartographer.json /srv/mediawiki/w/extensions/ManageWiki/maintenance/toggleExtension.php jsonconfig
* 12:01 John: create basic LDAP accounts for all mail users (no mail settings)
* 11:47 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildLocalisationCache.php --wiki loginwiki on mw* and jbr*
* 11:46 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/mergeMessageFileList.php --output /srv/mediawiki/config/ExtensionMessageFiles.php --wiki loginwiki on mw* and jbr*
* 11:18 Reception123: sudo umount /mnt/mediawiki-static and mount /mnt/mediawiki-static on jbr1
* 11:17 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildLocalisationCache.php --wiki loginwiki on mw* and jbr*
* 11:17 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/mergeMessageFileList.php --output /srv/mediawiki/config/ExtensionMessageFiles.php --wiki loginwiki on mw* and jbr*
* 10:56 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildLocalisationCache.php --wiki loginwiki on mw* and jbr*
* 10:56 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/mergeMessageFileList.php --output /srv/mediawiki/config/ExtensionMessageFiles.php --wiki loginwiki on mw* and jbr*
* 10:37 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildLocalisationCache.php --wiki loginwiki' on mw* and jbr*
* 10:36 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/mergeMessageFileList.php --output /srv/mediawiki/config/ExtensionMessageFiles.php --wiki loginwiki'

## 2020-10-30 

* 23:16 paladox: MariaDB [mhglobal]> update mw_namespaces set ns_content_model = 'wikitext' where ns_namespace_name = 'Module' and ns_dbname = 'default';
* 22:52 paladox: change ns_content_model to wikitext for namespace Module for all wikis
* 21:04 paladox: depool mw[4567] (in order) and also repool
* 15:46 paladox: apply schema for globalusage to commonswiki
* 15:33 paladox: MariaDB [mhglobal]> update mw_settings set s_settings = REPLACE(s_settings, 'wmgWikibasePropertuNamespaceID', 'wmgWikibasePropertyNamespaceID');
* 01:50 paladox: install gdb on test2

## 2020-10-29 

* 14:38 paladox: ban req.http.Host == static.miraheze.org  && req.url ~ "^/socdemwikiwiki/3/3c/Icon_debate.svg" - cp[67]

## 2020-10-28 

* 21:18 paladox: root@jobrunner2:/srv/mediawiki/w/extensions/Wikibase/repo/maintenance# sudo -u www-data php rebuildTermSqlIndex.php --wiki nbdbwiki --entity-type=property --rebuild-all-terms
* 20:44 paladox: rebuild lc on jobrunner*
* 19:17 paladox: inserted babel sql into wikibeatswiki
* 19:08 paladox: enable massmessage on aafiamovementwiki, aafiamovementwiki, aiytfwiki, gpwwiki, magicwiki, thetripletswiki, wikibeatswiki as it's now required by translationnotifications
* 16:44 Reception123: added bayonettawiki discord webhook
* 02:33 paladox: root@jobrunner1:/home/paladox# /usr/local/bin/foreachwikiindblist /home/paladox/pagetriage.json /srv/mediawiki/w/maintenance/sql.php /home/paladox/pagetriage.sql
* 02:26 paladox: root@jobrunner1:/home/paladox# /usr/local/bin/foreachwikiindblist /home/paladox/wikibaserepository.json /srv/mediawiki/w/maintenance/sql.php /srv/mediawiki/w/extensions/Wikibase/repo/sql/AddNormalizedTermsTablesDDL.sql
* 02:09 paladox: root@jobrunner1:/home/paladox# /usr/local/bin/foreachwikiindblist /home/paladox/babel.json /srv/mediawiki/w/maintenance/sql.php /home/paladox/babel.sql
* 02:08 paladox: root@jobrunner1:/home/paladox# /usr/local/bin/foreachwikiindblist /home/paladox/babel.json /srv/mediawiki/w/maintenance/sql.php /srv/mediawiki/w/extensions/Babel/babel.sql
* 01:46 paladox: inserted oauth sql into metawiki
* 01:26 paladox: rebuilding managewiki cache on mw*

## 2020-10-27 

* 21:54 paladox: create babel table on dreamversewiki
* 21:26 paladox: depool mw7
* 21:26 paladox: repool mw6
* 21:05 paladox: depool mw6
* 21:04 paladox: repool mw5
* 20:39 paladox: depool mw5
* 20:39 paladox: repool mw4
* 20:17 paladox: depool mw4
* 20:02 paladox: stop jobrunner and jobchron on jobrunner[12]
* 17:10 paladox: upgrade mariadb-client-10.3 mariadb-client-core-10.3 mariadb-common npm  - mail1
* 13:03 Reception123: rebooted mw4
* 05:59 Reception123: renamed animatedfeetwiki to drawnfeetwiki

## 2020-10-26 

* 19:17 Reception123: reception@jobrunner1:/srv/mediawiki/w/maintenance$ sudo -u www-data php rebuildall.php --wiki testwiki
* 19:11 Reception123: reception@jobrunner1:/srv/mediawiki/w/maintenance$ sudo -u www-data php initSiteStats.php --update --active --wiki testwiki
* 17:02 Reception123: MariaDB [mhglobal]> UPDATE globaluser SET gu_home_db = 'metawiki' WHERE gu_name = 'Universal Omega';
* 15:18 Reception123: ran jobs again
* 14:57 Reception123: reception@jobrunner1:/srv/mediawiki/w/maintenance$ sudo -u www-data php runJobs.php --wiki testwiki
* 00:03 Spookreeeno: ran jobs on meta from jbr2
* 00:00 paladox: run runJobs.php on jobrunner1 in a loop for all wikis

## 2020-10-25 

* 23:59 paladox: deleted CreateWikiJob from redis on jobrunner1
* 23:46 Spookreeeno: rhinos@jobrunner2:/var/log/mediawiki/debuglogs$ sudo -u www-data php /srv/mediawiki/w/maintenance/runJobs.php --wiki=metawiki
* 21:40 paladox: rebuild lc on mw* and jobrunner*
* 21:05 John: disable puppet1 on misc1

## 2020-10-24 

* 18:21 Southparkfan: ban all URLs containing 'MyLanguage' on cache proxies

## 2020-10-23 

* 09:05 Reception123: reception@jobrunner1:/srv/mediawiki/w/maintenance$ sudo -u www-data php rebuildall.php --wiki snapwikiwiki
* 08:22 Reception123: reception@jobrunner1:/srv/mediawiki/w/maintenance$ sudo -u www-data php updateSpecialPages.php --wiki snapwikiwiki
* 06:45 Reception123: reception@jobrunner1:/srv/mediawiki/w/maintenance$ sudo -u www-data php initSiteStats.php --update --active --wiki snapwikiwiki

## 2020-10-22 

* 19:21 paladox: sudo unattended-upgrade - accross all hosts.
* 19:09 paladox: update mariadb-common on ldap1
* 19:08 paladox: update mariadb-common on gluster[12]
* 19:07 paladox: update mariadb-common on jobrunner[12] and mw[4567]
* 19:06 paladox: update npm on jobrunner[12] and mw[4567]
* 19:04 paladox: update gluster on gluster[12], jobrunner[12] and mw[4567]

## 2020-10-21 

* 14:46 Reception123: reception@jobrunner1:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --report=1 --wiki passitonwiki /home/reception/delbackups2/passitonwiki.xml

## 2020-10-20 

* 13:42 John: reset an account token

## 2020-10-19 

* 20:48 paladox: clear circleyverse redis cache
* 15:05 Reception123: renamed travelguidemirawiki to travelguidesworldwiki
* 15:04 Reception123: reception@jobrunner1:~$ sudo -u www-data php /srv/mediawiki/w/extensions/CreateWiki/maintenance/renameWiki.php --wiki=loginwiki --rename travelguidemirawiki travelguidesworldwiki Reception123

## 2020-10-18 

* 22:13 paladox: apply schema updates to test2
* 17:25 paladox: upgrade grafana - mon1
* 17:21 paladox: upgrade icinga2 - mon1
* 16:51 paladox: upgrade graylog-server
* 16:37 Southparkfan: revert hosts hack
* 16:31 Southparkfan: local hack in /etc/hosts @test2 to test mariadb connection latency
* 14:50 Southparkfan: reinstall syslog-ng on test2 (rsyslog is being reinstalled randomly?)
* 06:52 Reception123: reception@jobrunner2:/srv/mediawiki/w/maintenance$ sudo -u www-data php deleteBatch.php --wiki besttvshowswiki --r "Requested - T6320" /home/reception/btsdel.txt
* 06:47 Reception123: reception@jobrunner1:/srv/mediawiki/w/maintenance$ sudo -u www-data php deleteBatch.php --wiki terribletvshowswiki --r "Requested - T6320" /home/reception/ttsdel.txt

## 2020-10-17 

* 21:48 paladox: fix content_models and slot_roles table on circleyversewiki
* 21:34 paladox: delete circleyversewiki permanently

## 2020-10-14 

* 17:21 paladox: rebuild lc on mw* and jobrunner*
* 16:38 paladox: upgrade test2 to 1.35
* 15:32 paladox: fix content_models on cfdwiki
* 05:53 Reception123: MariaDB [csydeswiki]> UPDATE nl_newsletters SET nl_active = 0 WHERE nl_name = 'Newsletter2';
* 05:52 Reception123: MariaDB [csydeswiki]> UPDATE nl_newsletters SET nl_main_page_id = 2 WHERE nl_name = 'Newsletter2';
* 05:48 Reception123: reception@jobrunner1:/srv/mediawiki/w/maintenance$ sudo -u www-data php deleteBatch.php --wiki testwiki --r "Requested - [T6307](https://meta.miraheze.org/wiki/phab:T6307)" /home/reception/testwikidel.txt

## 2020-10-13 

* 20:18 paladox: start replication on db7
* 20:12 paladox: [21:08:22]  <+paladox> !log stop mysql on db13 & upgrade
* 20:12 paladox: [21:05:27]  <+paladox> !log stop mysql on db12 & upgrade
* 20:12 paladox: [21:02:18]  <+paladox> !log stop mysql on db11 & upgrade
* 20:00 paladox: stop mysql replication on db7
* 20:00 paladox: starting database maintenance on db[11-13] & db7
* 19:59 paladox: downtimed db* & sslhost in icinga
* 17:43 Reception123: reception@jobrunner2:~$  sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --report=1 --wiki minecraftathomewiki /home/reception/Wikipedia-20201013131148.xml

## 2020-10-12 

* 12:56 Reception123: reception@jobrunner1:/srv/mediawiki/w/maintenance$ sudo -u www-data php initSiteStats.php --update --active --wiki metawiki

## 2020-10-10 

* 18:52 Reception123: added intercriaturaswiki discord webhook
* 13:31 paladox: upgrade bacula on phab1
* 13:28 paladox: upgrade bacula on gluster1 and db*
* 13:27 paladox: upgrade bacula and postgresql on puppet2
* 13:25 paladox: upgrade bacula on bacula2
* 13:20 paladox: regenerate backups on bacula2
* 02:30 Southparkfan: fixed db7 replication after an hour of struggling. lesson: do not point db7's master to db7 itself ;)
* 01:04 Southparkfan: restart transfer again, ALTER TABLEs may cause backup problems
* 00:48 Southparkfan: db7 could not be set up as replica due to server-id error, wiped db7 /srv/mariadb and trying again

## 2020-10-09 

* 23:19 Southparkfan: repopulating mariadb on db7
* 23:09 Southparkfan: silence db7 alerts regarding mariadb for reinstall of mariadb
* 22:52 Southparkfan: performed [https://phabricator.miraheze.org/T6095](https://phabricator.miraheze.org/T6095) schema changes on db13 now as well; started replica process on db7 to catch up
* 22:48 Southparkfan: performed schema changes on db7, now doing on db13
* 22:21 Southparkfan: applying schema changes for rottenlinks PK on db7
* 21:52 Southparkfan: stop db7 replication to alter tables for [https://phabricator.miraheze.org/T6095](https://phabricator.miraheze.org/T6095)
* 17:44 Reception123: reception@jobrunner2:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --report=1 --wiki callipediawiki /home/reception/Wikipedia-20200917231201.xml
* 17:41 Reception123: reception@jobrunner1:/srv/mediawiki/w/maintenance$ sudo -u www-data php initSiteStats.php --wiki callipediawiki --update

## 2020-10-08 

* 20:57 paladox: rebuild lc on mw* and jobrunner*
* 17:49 Reception123: added marvelcinematicuniversewiki webhook
* 14:52 paladox: root@jobrunner1:/srv/mediawiki/w/maintenance# /usr/local/bin/foreachwikiindblist /srv/mediawiki/w/cache/databases.json /srv/mediawiki/w/maintenance/runJobs.php
* 14:37 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildLocalisationCache.php --wiki loginwiki on mw* and jbr*
* 14:35 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/mergeMessageFileList.php --output /srv/mediawiki/config/ExtensionMessageFiles.php --wiki loginwiki on mw* and jbr*
* 12:38 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildLocalisationCache.php --wiki loginwiki on mw* and jbr*
* 12:37 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/mergeMessageFileList.php --output /srv/mediawiki/config/ExtensionMessageFiles.php --wiki loginwiki on mw* and jbr*
* 11:15 paladox: $cWJ = new CreateWikiJson( 'metawiki' ); $cWJ->resetWiki();

## 2020-10-07 

* 11:10 Reception123: sudo service ircrcbot restart

## 2020-10-06 

* 20:00 Reception123: created mail account for noreply-bots (T6186)
* 12:45 Reception123: sudo /usr/bin/tar --exclude /mnt/mediawiki-static/allthetropeswiki/archive --exclude /mnt/mediawiki-static/allthetropeswiki/deleted --exclude /mnt/mediawiki-static/allthetropeswiki/lockdir --exclude /mnt/mediawiki-static/allthetropeswiki/temp --exclude /mnt/mediawiki-static/allthetropeswiki/thumb -zcvf /mnt/mediawiki-static/dumps/allthetropeswiki06102020.zip /mnt/mediawiki-static/allthetropeswiki/
* 12:12 Reception123: added tuscriaturaswiki discord webhook
* 10:58 John: restarted Parsoid on services[12]
* 01:02 paladox: upgrade grafana - mon1

## 2020-10-05 

* 20:46 paladox: fix perm table for test2wiki (*)
* 20:31 paladox: update metawiki perm group entries to remove empty strings from the permission column
* 20:30 paladox: MariaDB [mhglobal]> update mw_permissions set perm_permissions = '["translate"]' where perm_group = 'translator' and perm_dbname = 'metawiki';
* 20:29 paladox: MariaDB [mhglobal]> update mw_permissions set perm_permissions = '[]' where perm_group = 'wikicreator' and perm_dbname = 'metawiki';
* 20:28 paladox: MariaDB [mhglobal]> delete from mw_permissions where perm_dbname = '2b2twiki' and perm_group = 'president';
* 17:50 Reception123: added discord webhook
* 17:13 paladox: cd /srv/mediawiki/w ; sudo -u www-data git pull ; sudo -u www-data git reset --hard origin/REL1_34 ; sudo -u www-data git submodule sync ; sudo -u www-data git submodule update - mw* and jobrunner*

## 2020-10-04 

* 18:21 Southparkfan: disable puppet on test2 for syslog-ng work
* 13:54 paladox: dropped cfdwiki and recreated
* 11:02 Reception123: reception@jobrunner2:/srv/mediawiki/w/maintenance$ sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --report=1 --wiki tuscriaturaswiki /home/reception/Wikipedia-20201004104840.xml
* 01:22 paladox: upgrade phabricator on phab1

## 2020-10-03 

* 23:59 paladox: root@gluster1:/mnt/mediawiki-static/private/dumps# rm ourfoodchainwiki/zi1IuJ9A
* 23:58 paladox: root@gluster1:/mnt/mediawiki-static/private/dumps# rm thefinalrumblewiki/ziw6CqZT
* 22:11 paladox: MariaDB [mhglobal]> update mw_permissions set perm_permissions = '[]' where perm_dbname = 'metawiki' and perm_group = 'cvt'
* 19:53 paladox: root@gluster1:/mnt/mediawiki-static# gluster volume set mvol locks.mandatory-locking forced
* 19:14 paladox: restarted glusterd on gluster1, for some reason it stopped?
* 19:10 paladox: gluster set io threads to 12
* 17:11 Reception123: zipping individual att image directories
* 15:26 Southparkfan: disable puppet2's puppet agent and disable git pull for puppet repo
* 12:09 Southparkfan: disable puppet on test2
* 11:56 Southparkfan: silenced icinga check for cp9 http error rate
* 07:13 Reception123: reception@jobrunner1:/srv/mediawiki/w/maintenance$ sudo -u www-data php deleteBatch.php --wiki testwiki --r "Requested - [T6260](https://meta.miraheze.org/wiki/phab:T6260)" /home/reception/testwikidel.txt
* 03:16 Southparkfan: add ufw rule on ldap1 to allow graylog1 -> ldap1 port 636 (to be puppetised)
* 01:43 Southparkfan: reboot graylog1 for memory upgrade

## 2020-10-02 

* 22:19 Southparkfan: force-reload gdnsd on ns1
* 22:08 Southparkfan: disable puppet on cp7 to work on a fix for T6146
* 10:58 Reception123: manually copying image files at a time from static/allthetropeswiki to static/dumps

## 2020-10-01 

* 22:43 paladox: root@jobrunner1:/home/paladox# /usr/local/bin/foreachwikiindblist /srv/mediawiki/w/cache/databases.json /srv/mediawiki/w/maintenance/runJobs.php
* 22:17 John: made sensitive comments on Phabricator visible to only Reception123 (public task)
* 21:49 paladox: reboot jobrunner1
* 21:37 paladox: depool, reboot and repool mw[4567]
* 21:30 paladox: root@jobrunner1:/home/paladox# sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=csydeswiki --report=1 C.Sydes+Wiki-20200317015034.xml
* 21:29 paladox: root@jobrunner1:/home/paladox# sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=csydeswiki --report=1 C.Sydes+Wiki-20200312083144.xml
* 21:22 paladox: root@jobrunner1:/home/paladox# sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=csydeswiki --report=1 C.Syde_s_Wiki-20200106000305.xml
* 20:47 paladox: reboot jobrunner2
* 20:24 paladox: restart postgresql on puppetdb
* 20:24 paladox: restart postgresql on puppet2
* 20:21 Southparkfan: restart postfix on all servers to resolve mailer-daemon spam
* 20:01 Southparkfan: enable puppet on mon1
* 19:57 Southparkfan: enable puppet on mail1
* 19:55 Southparkfan: disable puppet on mail1 to verify change
* 19:42 Southparkfan: disable puppet on mon1 to verify change
* 12:11 paladox: set i/o threads to 4 on gluster
* 09:22 Reception123: reception@jobrunner1:~$ sudo /usr/bin/zip /mnt/mediawiki-static/dumps/allthetropeswiki/allthetropeswiki.zip -r /mnt/mediawiki-static/allthetropeswiki/ -x mnt/mediawiki-static/allthetropes/archive/ -x mnt/mediawiki-static/allthetropes/deleted/ -x mnt/mediawiki-static/allthetropes/lockdir/ -x mnt/mediawiki-static/allthetropes/temp/ -x mnt/mediawiki-static/allthetropes/thumb/
* 07:05 Reception123: reception@jobrunner1:~$ sudo /usr/bin/zip /mnt/mediawiki-static/dumps/allthetropeswiki/allthetropeswiki.zip -r /mnt/mediawiki-static/allthetropeswiki/
* 06:16 Reception123: reception@jobrunner1:/srv/mediawiki/w/maintenance$ sudo -u www-data php dumpBackup.php --current --wiki allthetropeswiki > /home/reception/allthetropes01102020.xml

## 2020-09-30 

* 13:12 Reception123: reception@jobrunner1:/srv/mediawiki/w/maintenance$ sudo -u www-data php rebuildall.php --wiki snapwikiwiki
* 12:58 Reception123: reception@jobrunner1:/srv/mediawiki/w/maintenance$ sudo -u www-data php updateSpecialPages.php --wiki snapwikiwiki
* 12:55 Reception123: reception@jobrunner1:/srv/mediawiki/w/maintenance$ sudo -u www-data php initSiteStats.php --wiki snapwikiwiki --update

## 2020-09-29 

* 18:54 Reception123: add toaqwiki discord hook

## 2020-09-28 

* 20:32 paladox: GDPR removal
* 15:14 Reception123: MariaDB [astonishingscratcherswiki]> DELETE FROM logging WHERE log_title = '<REDACTED>'; (3 times)
* 15:08 Reception123: GDPR script and attaching unattached accounts
* 11:28 Reception123: reception@jobrunner1:/srv/mediawiki/w/maintenance$ sudo -u www-data php updateSpecialPages.php --wiki metawiki
* 05:50 Reception123: GDPR script

## 2020-09-27 

* 19:47 paladox: reboot ldap1
* 19:27 paladox: root@jobrunner1:/home/paladox# /usr/local/bin/foreachwikiindblist /srv/mediawiki/w/cache/databases.json /srv/mediawiki/w/maint*/runJobs.php
* 19:26 paladox: rebuild lc on mw* and jobrunner*
* 16:43 paladox: root@gluster1:/home/paladox# gluster volume set mvol network.compression off
* 16:13 paladox: root@gluster1:/home/paladox# gluster volume set mvol network.inode-lru-limit 10000
* 16:10 paladox: root@gluster1:/home/paladox# gluster volume set mvol network.compression on
* 16:09 paladox: root@gluster1:/home/paladox# gluster volume set mvol network.ping-timeout 60
* 16:07 paladox: root@gluster1:/home/paladox# gluster volume set mvol performance.least-prio-threads 8
* 16:07 paladox: root@gluster1:/home/paladox# gluster volume set mvol performance.low-prio-threads 8
* 16:07 paladox: root@gluster1:/home/paladox# gluster volume set mvol performance.normal-prio-threads 8
* 16:06 paladox: root@gluster1:/home/paladox# gluster volume set mvol performance.high-prio-threads 8
* 16:05 Reception123: reception@jobrunner1:/srv/mediawiki/w/maintenance$ sudo -u www-data php dumpBackup.php --current --filter=namespace:6 --include-files --wiki allthetropeswiki > /home/reception/allthetropes26092020_filenamespace.xml
* 16:04 paladox: root@gluster1:/home/paladox# gluster volume set mvol performance.io-thread-count 8

## 2020-09-26 

* 21:14 paladox: root@gluster1:/home/paladox# gluster volume set mvol performance.open-behind on
* 21:09 paladox: upgrade gluster to 8.2 on test2
* 21:02 paladox: upgrade gluster to 8.2 on mw* and jobrunner*
* 21:00 paladox: upgrade gluster to 8.2 on gluster[12]
* 13:02 Reception123: reception@jobrunner1:~$ sudo /usr/bin/zip /mnt/mediawiki-static/dumps/allthetropeswiki/allthetropeswiki.zip -r /mnt/mediawiki-static/allthetropeswiki/
* 06:28 Reception123: reception@jobrunner1:/srv/mediawiki/w/maintenance$ sudo -u www-data php dumpBackup.php --full --filter=namespace:6 --include-files --wiki allthetropeswiki > /home/reception/allthetropes26092020_filenamespace.xml

## 2020-09-25 

* 05:37 Reception123: reception@jobrunner1:/srv/mediawiki/w/maintenance$ sudo -u www-data php updateCollation.php --wiki holidayswiki --force
* 05:29 Reception123: deleted and dropped wikis listed [https://phabricator.miraheze.org/P346](https://phabricator.miraheze.org/P346) (db11 & db12)
* 05:21 Reception123: $cWJ = new CreateWikiJson( 'commonswiki' ); $cWJ->resetWiki();
* 05:20 Reception123: MariaDB [mhglobal]> delete from mw_permissions where perm_dbname = 'commonswiki' and perm_group = 'imterface-admin';

## 2020-09-24 

* 21:44 paladox: rebuild lc on mw*
* 21:08 paladox: root@test2:/srv/mediawiki/w/extensions/MirahezeMagic# sudo -u www-data php maintenance/createWiki.php --wiki loginwiki
* 20:49 paladox: MariaDB [(none)]> create database ldapwikiwiki; - db11
* 20:34 Zppix: same for 14412 & 14300
* 20:27 Zppix: UPDATE cw_requests SET cw_status = 'approved' WHERE cw_id = '14402'; on jobrunner1 using sql.php
* 16:37 paladox: rebuild lc on mw* and jobrunner*
* 16:22 paladox: depool mw[45678] and repool
* 13:48 Reception123: reception@jobrunner1:~$ sudo -u www-data php /srv/mediawiki/w/extensions/CreateWiki/maintenance/deleteWikis.php --wiki=loginwiki Reception123 --delete
* 09:27 Reception123: GDPR script

## 2020-09-23 

* 22:02 Zppix: UPDATE cw_requests SET cw_status = 'approved' WHERE cw_id = '14391'; on jobrunner1 using sql.php
* 18:23 Reception123: MariaDB [metawiki]> UPDATE cw_requests SET cw_status = 'approved' WHERE cw_id = '14369';
* 14:47 paladox: change bots password for mail
* 09:42 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildLocalisationCache.php --wiki loginwiki on mw* and jbr*

## 2020-09-22 

* 07:09 Reception123: reception@jobrunner1:/srv/mediawiki/w/maintenance$  sudo -u www-data php initSiteStats.php --wiki pinheirensewiki --update
* 06:20 Reception123: reception@jobrunner1:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/importImages.php --wiki=pinheirensewiki --search-recursively --skip-dupes /home/reception/pinheirenseimages

## 2020-09-21 

* 05:40 Reception123: wikibackups of top 10 public wikis on jobrunner2

## 2020-09-20 

* 07:14 Reception123: running wikibackups on jobrunner1 (bash ./wikibackups.sh /home/reception/backupwikis.dblist /srv/mediawiki/w/maintenance/dumpBackup.php)

## 2020-09-19 

* 20:41 paladox: rebuild lc on mw* and jobrunner*
* 18:50 Reception123: sudo service ircrcbot restart
* 05:09 Reception123: reception@jobrunner2:/srv/mediawiki/w/maintenance$ sudo -u www-data php deleteBatch.php --wiki testwiki --r "Requested - T6197" /home/reception/testwikidel.txt

## 2020-09-18 

* 05:49 Reception123: reception@jobrunner1:/srv/mediawiki/w/maintenance$ sudo -u www-data php deleteBatch.php --wiki callipediawiki --r "Requested - T6193" /home/reception/callipedadel.txt
* 05:39 Reception123: reception@jobrunner2:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --report=1 --wiki callipediawiki /home/reception/Wikipedia-20200917231201.xml
* 02:32 PuppyKun: GDPR removal

## 2020-09-16 

* 19:35 paladox: root@jobrunner1:/srv/mediawiki/w/maintenance# sudo -u www-data php deleteOldRevisions.php --delete --wiki ashinawiki
* 19:35 paladox: root@jobrunner1:/srv/mediawiki/w/maintenance# sudo -u www-data php maintenance/deleteOldRevisions.php --delete --wiki ashinawiki
* 16:37 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/mergeMessageFileList.php --output /srv/mediawiki/config/ExtensionMessageFiles.php --wiki loginwiki
* 16:32 Reception123: umount and then mount static on jobrunner2
* 06:36 Reception123: reception@mw7:~$ sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/w/cache/databases.json /srv/mediawiki/w/maintenance/runJobs.php
* 06:30 Reception123: running GDPR script 3 times
* 05:39 Reception123: > $cWJ = new CreateWikiJson( 'dcmultiversewiki' ); $cWJ->resetWiki();
* 05:37 Reception123: MariaDB [mhglobal]> delete from mw_permissions where perm_dbname = 'dcmultiverse                                                                             wiki' and perm_group = 'founder';
* 05:37 Reception123: MariaDB [mhglobal]> delete from mw_permissions where perm_dbname = 'dcmultiverse                                                                             wiki' and perm_group = 'content_moderators';
* 05:37 Reception123: MariaDB [mhglobal]> delete from mw_permissions where perm_dbname = 'dcmultiverse                                                                             wiki' and perm_group = 'reviewer';
* 05:37 Reception123: MariaDB [mhglobal]> delete from mw_permissions where perm_dbname = 'dcmultiverse                                                                             wiki' and perm_group = 'automoderated';

## 2020-09-15 

* 09:59 Zppix: rebuildRC and InitSiteStats for callipediawiki after import
* 08:11 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildLocalisationCache.php --wiki loginwiki on mw* and jbr*
* 05:01 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --report=1 --wiki blitzwiki /home/reception/wotblitz_pages_full.xml on jbr1

## 2020-09-14 

* 18:16 paladox: root@jobrunner1:/var/spool/cron/crontabs# /usr/local/bin/foreachwikiindblist /srv/mediawiki/w/cache/databases.json /srv/mediawiki/w/maint*/runJobs.php
* 17:29 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildLocalisationCache.php --wiki loginwiki on mw* and jbr*
* 05:47 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --report=1 --wiki callipediawiki /home/reception/Wikipedia-20200914030813.xml on jbr2
* 05:47 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --report=1 --wiki callipediawiki /home/reception/Wikipedia-20200914030849.xml on jbr2

## 2020-09-13 

* 07:01 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --report=1 --wiki callipediawiki /home/reception/Wikipedia-20200912220015.xml on jbr2

## 2020-09-11 

* 14:14 paladox: depool mw[4567] and reboot and repool

## 2020-09-10 

* 20:07 paladox: root@jobrunner1:/srv/mediawiki/w/maintenance# sudo -u www-data php initEditCount.php --wiki=darkangelwiki
* 19:30 paladox: restarted parsoid on services1
* 18:01 Reception123: MariaDB [mhglobal]> UPDATE cw_wikis SET wiki_category = 'electronics' WHERE wiki_category = 'eletronics';
* 14:33 paladox: root@gluster1:/home/paladox# gluster volume set mvol open-behind off
* 14:12 paladox: root@gluster1:/home/paladox# gluster volume set mvol performance.readdir-ahead off
* 14:12 paladox: root@gluster1:/home/paladox# gluster volume set mvol performance.parallel-readdir off

## 2020-09-09 

* 20:50 paladox: rebuild lc on mw* and jobrunner*
* 17:12 paladox: rebuild lc on mw* and jobrunner*
* 16:04 paladox: upgrade gluster-client on jobrunner2
* 15:49 paladox: upgrade gluster-client on mw[4567]
* 15:37 paladox: upgrade gluster-client on test2
* 15:35 paladox: update puppet-agent on gluster2
* 15:35 paladox: upgrading gluster to version 8 on gluster2
* 15:29 paladox: update puppet-agent on gluster1
* 15:29 paladox: upgrading gluster to version 8 on gluster1
* 12:55 Reception123: same for reverserottenwebsiteswiki
* 12:40 Reception123: updated circleyverse hebook

## 2020-09-08 

* 23:32 paladox: deleted some pages on pseudocienciawiki using deleteBatch script
* 23:25 paladox: MariaDB [doctorwhofanfilmsdatabasewiki]> INSERT INTO slot_roles (role_id, role_name) VALUES (1, 'main');
* 23:05 paladox: update puppet-agent on phab1
* 22:36 paladox: apply [https://github.com/miraheze/DataDump/blob/master/sql/data_dump.sql](https://github.com/miraheze/DataDump/blob/master/sql/data_dump.sql) to zymonicwiki
* 22:07 paladox: root@jobrunner1:/home/paladox# /usr/local/bin/foreachwikiindblist /srv/mediawiki/w/cache/databases.json /srv/mediawiki/w/maintenance/sql.php /srv/mediawiki/w/extensions/DataDump/sql/patches/patch-dumps_size-bigint.sql
* 18:35 paladox: root@gluster1:/home/paladox# gluster volume set mvol network.inode-lru-limit 5000
* 17:33 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildLocalisationCache.php --wiki loginwiki on mw* and jbr*
* 17:32 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/mergeMessageFileList.php --output /srv/mediawiki/config/ExtensionMessageFiles.php --wiki loginwiki on mw* and jbr*
* 16:51 Reception123: (on db12)
* 16:51 Reception123: MariaDB [(none)]> DROP DATABASE miiwiki;
* 16:01 paladox: gluster volume set mvol features.cache-invalidation-timeout 600 (set earlier)
* 15:16 paladox: depool mw4 and repool (reboot)
* 14:16 paladox: update puppet-agent on jobrunner1
* 14:16 paladox: update puppet-agent on jobrunner2
* 14:15 paladox: update puppet-agent on test2
* 14:14 paladox: update libzmq5 puppet-agent on mw6
* 14:00 paladox: update puppet-agent on mw5
* 14:00 paladox: update libzmq5 puppet-agent on mw5
* 13:55 paladox: reboot mw6 - seems stuck
* 13:26 paladox: reboot mw4 - seems to have been stuck for 12h?
* 13:23 paladox: update libzmq5 puppet-agent on mw4
* 13:20 paladox: update puppetserver, puppetdb and puppet-agent on puppet2
* 05:23 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildLocalisationCache.php --wiki loginwiki on mw* and jbr*
* 05:23 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/mergeMessageFileList.php --output /srv/mediawiki/config/ExtensionMessageFiles.php --wiki loginwiki  on mw* and jbr*

## 2020-09-07 

* 16:30 paladox: up gluster2 storage by 50G
* 16:18 paladox: root@gluster1:/home/paladox# gluster volume set mvol cluster.rebal-throttle lazy
* 16:16 paladox: root@gluster1:/home/paladox# gluster volume set mvol cluster.rebal-throttle normal
* 16:11 paladox: up gluster2 storage by 100G

## 2020-09-05 

* 19:29 Southparkfan: installing security fixes to resolve icinga alerts
* 16:22 Reception123: cosmoswiki not loginwiki for previous
* 16:21 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildmessages.php --wiki loginwiki on mw* and jbr*
* 15:24 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildLocalisationCache.php --wiki loginwiki on mw* and jbr*
* 15:23 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/mergeMessageFileList.php --output /srv/mediawiki/config/ExtensionMessageFiles.php --wiki loginwiki on mw* and jbr*
* 13:23 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildLocalisationCache.php --wiki loginwiki on mw* and jbr*
* 13:23 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/mergeMessageFileList.php --output /srv/mediawiki/config/ExtensionMessageFiles.php --wiki loginwiki on mw* and jbr*
* 04:38 paladox: rebuild lc on jobrunner* and test2
* 04:03 paladox: rebuild lc on mw*

## 2020-09-04 

* 07:04 Reception123: $cWJ = new CreateWikiJson( circleyversefanonwiki ); $cWJ->resetWiki();
* 06:59 Reception123: MariaDB [mhglobal]> delete from mw_permissions where perm_dbname = 'circleyversefanonwiki' and perm_group = 'automoderated';
* 06:59 Reception123: MariaDB [mhglobal]> delete from mw_permissions where perm_dbname = 'circleyversefanonwiki' and perm_group = 'moderator';
* 06:56 Reception123: delete from mw_permissions where perm_dbname = 'circleyversefanonwiki' and perm_permissions = 'automoderated'; (and moderated) ; did nothing
* 06:46 Reception123: /usr/bin/zip /mnt/mediawiki-static/private/dumps/speleowiki/speleowiki.zip /mnt/mediawiki-static/speleowiki/

## 2020-09-03 

* 15:54 Reception123: GDPR script
* 07:14 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildLocalisationCache.php --wiki loginwiki
* 07:14 Reception123: udo -u www-data php /srv/mediawiki/w/maintenance/mergeMessageFileList.php --output /srv/mediawiki/config/ExtensionMessageFiles.php --wiki loginwiki on mw* and jbr*
* 06:05 Reception123: reception@jobrunner1:/srv/mediawiki/w/maintenance$ sudo -u www-data php deleteBatch.php --wiki marionetworkwiki --r "Requested - T6132" /home/reception/marionetworkdel.txt

## 2020-09-02 

* 14:43 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildLocalisationCache.php --wiki loginwiki on mw* and jbr*
* 14:42 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/mergeMessageFileList.php --output /srv/mediawiki/config/ExtensionMessageFiles.php --wiki loginwiki on mw* and jbr*

## 2020-09-01 

* 18:38 paladox: INSERT INTO slot_roles (role_id, role_name) VALUES (1, 'main');
* 18:37 paladox: MariaDB [hispanowiki]> INSERT INTO content_models (model_id, model_name) VALUES (5, 'json');
* 18:37 paladox: MariaDB [hispanowiki]> INSERT INTO content_models (model_id, model_name) VALUES (4, 'Scribunto');
* 18:37 paladox: MariaDB [hispanowiki]> INSERT INTO content_models (model_id, model_name) VALUES (3, 'javascript');
* 18:37 paladox: MariaDB [hispanowiki]> INSERT INTO content_models (model_id, model_name) VALUES (2, 'css');
* 18:36 paladox: MariaDB [hispanowiki]> INSERT INTO content_models (model_id, model_name) VALUES (1, 'wikitext');
* 18:05 paladox: MariaDB [hispano76wiki]> INSERT INTO content_models (model_id, model_name) VALUES (4, 'Scribunto');
* 18:05 paladox: MariaDB [hispano76wiki]> INSERT INTO content_models (model_id, model_name) VALUES (3, 'javascript');
* 18:05 paladox: MariaDB [hispano76wiki]> INSERT INTO content_models (model_id, model_name) VALUES (5, 'json');
* 18:04 paladox: MariaDB [hispano76wiki]> INSERT INTO content_models (model_id, model_name) VALUES (2, 'css');
* 18:03 paladox: MariaDB [hispano76wiki]> INSERT INTO content_models (model_id, model_name) VALUES (1, 'wikitext');
* 15:06 Reception123: reception@jobrunner1:/srv/mediawiki/w/maintenance$ sudo -u www-data php runJobs.php --wiki metawiki
* 15:04 RhinosF1: 16:00:56 <+Reception123>  !log reception@jobrunner1:/srv/mediawiki/w/maintenance$ sudo -u www-data php runJobs.php --wiki metawiki
* 05:49 Reception123: discord webhook for sagcraftwiki

## 2020-08-31 

* 21:22 RhinosF1: !log actually clean up security testing done last week re CA (attempted by Reception unsuccessfully, see tests done on my accounts and email from SPF regarding bug we were testing)
* 14:37 Reception123: add discord webhook for iceriawiki

## 2020-08-30 

* 08:50 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --report=1 --wiki thelastsovereignwiki /home/reception/thelastsovereign_pages_full.xml
* 06:58 Reception123: reception@jobrunner1:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/populateContentTables.php --wiki hispano76wiki --table all

## 2020-08-29 

* 21:38 paladox: root@gluster1:/home/paladox# gluster volume set mvol performance.client-io-threads on
* 17:25 PuppyKun: sudo -u www-data php populateGroupPermissionsWithDefaults.php --wiki nevillepediawiki --overwrite
* 06:43 Reception123: deleted and dropped hispano76wiki and hispanowiki (reset req)
* 00:43 paladox: restarted nginx on cp3
* 00:34 paladox: restarted nginx on cp6
* 00:32 paladox: restarted nginx on cp9
* 00:30 paladox: restarted nginx on cp7

## 2020-08-27 

* 15:34 Reception123: deleted and dropped doctorwhofanfilmsdatabasewiki (recreation)
* 05:55 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildLocalisationCache.php --wiki loginwiki on mw* and jbr*
* 05:54 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/mergeMessageFileList.php --output /srv/mediawiki/config/ExtensionMessageFiles.php --wiki loginwiki on mw* and jbr*

## 2020-08-26 

* 15:11 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --report=1 --wiki aoc2wiki /home/reception/Wikimedia_-_Infobox_templates_relating_to_country%2C_game%2C_government%2C_and_settlement.xml
* 14:04 Reception123: reception@jobrunner1:/srv/mediawiki/w/extensions/MatomoAnalytics/maintenance$ sudo -u www-data php modifyMatomo.php --wiki metawiki
* 12:14 Reception123: ran GDPR script
* 05:35 Reception123: reception@jobrunner1:/srv/mediawiki/w/maintenance$ sudo -u www-data php initSiteStats.php --wiki marionetworkwiki --update

## 2020-08-25 

* 12:14 Reception123: add discord webhook for marvelousvyonderswiki
* 11:52 Reception123: added discord webhook for horriblevyonderswiki
* 09:49 Reception123: also done on testwiki/loginwiki/quircwiki
* 09:49 Reception123: MariaDB [metawiki]> DELETE FROM ipblocks WHERE ipb_address OR ipb_user = "RF1_Bot"; (security verification completed)
* 06:23 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildLocalisationCache.php --wiki loginwiki on mw* and jbr*
* 06:23 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/mergeMessageFileList.php --output /srv/mediawiki/config/ExtensionMessageFiles.php --wiki loginwiki on mw* and jbr*

## 2020-08-24 

* 22:43 Southparkfan: restart slave thread on db7
* 22:24 Southparkfan: apply sec patch (see mail) on servers with mediawiki installation in /srv/mediawiki/w
* 21:32 Southparkfan: create bots account on misc1 for mailbox purposes
* 16:04 Reception123: hid an account on meta to test a possible security issue

## 2020-08-23 

* 05:40 Reception123: created phab board for universal omega

## 2020-08-22 

* 18:27 Zppix: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --report=1 --wiki saramorawiki /home/zppix/Wikipedia-20200822105028.xml on jobrunner2 ([phab:T6083](https://meta.miraheze.org/wiki/phab:T6083))
* 13:54 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildLocalisationCache.php --wiki loginwiki on mw* and jbr*
* 09:20 Reception123: reception@mw6:~$ sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/w/cache/databases.json /srv/mediawiki/w/maintenance/runJobs.php
* 01:42 PuppyKun: in the process of running jobs globally (rip starting 2 renames while jobs were super backlogged)
* 01:23 PuppyKun: manually ran 4500 jobs on metawiki

## 2020-08-21 

* 13:28 Reception123: dropped all wikis listed at [https://phabricator.miraheze.org/P344](https://phabricator.miraheze.org/P344)
* 13:12 Zppix: initSiteStats (ran on jobrunner2) and rebuildRC (ran on jobrunner1) for ficreationwiki following import completion (T6067)
* 10:11 Reception123: reception@jobrunner1:/srv/mediawiki/w/extensions/CreateWiki/maintenance$ sudo -u www-data php deleteWikis.php --wiki loginwiki --delete Reception123
* 08:02 Reception123: MariaDB [phabricator_herald]> UPDATE herald_rule SET isDisabled = true WHERE id = '35'; (User resigned)
* 06:27 Reception123: reception@jobrunner2:/srv/mediawiki/w/maintenance$ sudo -u www-data php deleteBatch.php --wiki rottenwebsiteswiki --r "Requested - T6068" /home/reception/rottenwebsitesdel.txt
* 06:26 Reception123: reception@jobrunner1:/srv/mediawiki/w/maintenance$ sudo -u www-data php deleteBatch.php --wiki awesomegameswiki --r "Requested - T6068" /home/reception/awesomegamesdel.txt
* 06:08 Reception123: renamed gloriusdawnwiki to gloriousdawnwiki.
* 05:50 Reception123: added discord webhook for ficreationwiki
* 04:03 paladox: root@jobrunner2:/home/paladox# sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/w/cache/databases.json /srv/mediawiki/w/maintenance/sql.php /srv/mediawiki/w/extensions/Cargo/sql/cargo_tables.patch.field_helper_tables.sql - T6070
* 03:48 paladox: rebuild lc on mw* and jobrunner*
* 03:38 paladox: root@jobrunner2:/home/paladox# sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/w/cache/databases.json /srv/mediawiki/w/maintenance/sql.php /srv/mediawiki/w/extensions/Cargo/sql/cargo_tables.patch.field_helper_tables.mssql.sql - T6070
* 03:23 paladox: reduce jobrunner1 cores by 1 (so 3 cores in total)
* 03:13 paladox: reduce jobrunner2 cores by 1 (so 3 cores in total)

## 2020-08-20 

* 20:49 Zppix: Run importDump.php for ficreationwiki (T6067)
* 15:38 Southparkfan: remove wrk from cp6, repool cp9
* 15:31 Southparkfan: enable puppet on cp9
* 14:58 Southparkfan: install wrk on cp6
* 14:47 Southparkfan: disable puppet on cp9

## 2020-08-19 

* 03:44 paladox: upgrade icingaweb2 on mon1
* 02:42 paladox: set puppet2 cores to 3

## 2020-08-18 

* 18:32 Southparkfan: force logrotate for nginx on cp[79]
* 17:52 Southparkfan: forcing nginx logrotate on cp6
* 17:42 Southparkfan: forcing a logrotate job for nginx and varnish logs on cp3
* 16:13 Southparkfan: downtime cp3 services in icinga
* 16:00 Southparkfan: delete varnishlog [4567] from cp3 to free up space
* 13:10 RhinosF1: fixing puppet on test2

## 2020-08-16 

* 15:48 Reception|away: restarted rc bot
* 12:46 Reception|away: umount/mount static on gluster1

## 2020-08-14 

* 08:35 RhinosF1: tried running populateSites on jbr2, failing see T6044

## 2020-08-13 

* 22:34 Zppix: rebuildLC on jobrunner*/mw*

## 2020-08-11 

* 22:31 paladox: root@gluster1:/home/paladox# gluster volume set mvol performance.client-io-threads off
* 07:19 Reception123: GDPR script
* 04:44 Reception123: reception@jobrunner1:/srv/mediawiki/w/maintenance$ sudo -u www-data php deleteBatch.php --wiki xedwiki --r "Requested - T6023" /home/reception/xeddel.txt

## 2020-08-10 

* 11:55 Reception123: ran GDPR script
* 00:16 paladox: upgrade phabricator
* 00:11 paladox: upgrade phab1 debian to 10.5

## 2020-08-09 

* 23:59 paladox: regenerate backups on bacula2
* 23:42 paladox: upgrade bacula2 debian to 10.5
* 23:38 paladox: upgrade mail1 debian to 10.5
* 21:34 paladox: increase puppet2 cores to 6 (as an experiment)
* 20:45 paladox: upgrade grafana to 7.1 on mon1
* 20:44 paladox: upgrade icinga2 to 2.12 on mon1
* 20:43 paladox: upgrade debian to 10.5 on mon1 & reboot
* 20:36 paladox: upgrade debian to 10.5 on ldap1 & reboot
* 20:28 paladox: upgrade debian to 10.5 on test2 & reboot
* 20:25 paladox: upgrade debian to 10.5 on services[12] & reboot
* 20:23 paladox: reboot jobrunner1
* 20:18 paladox: repool sg (cp3)
* 20:11 paladox: upgrade cp3 to debian 10.5 & reboot
* 20:04 paladox: upgrade cp9 to debian 10.5 & reboot
* 20:01 paladox: depool ca (cp9)
* 19:57 paladox: reboot ns2
* 19:54 paladox: upgrade ns[12] to debian 10.5
* 19:54 paladox: repool cp[67]
* 19:47 paladox: reboot cp[67]
* 19:46 paladox: upgrade cp[67] to debian 10.5
* 19:44 paladox: depool cp7
* 19:39 paladox: depool cp6
* 11:53 Reception123: reception@jobrunner1:/srv/mediawiki/w/maintenance$ sudo -u www-data php deleteBatch.php --wiki crappygameswiki --r "Requested - T6028" /home/reception/cgwdel2.txt

## 2020-08-08 

* 19:08 paladox: upgrade debian to 10.5 on rdb1 and reboot
* 19:05 paladox: upgrade mw[4567] to debian 10.5
* 19:04 paladox: depool mw[4567] & reboot and repool
* 19:02 paladox: upgrade puppetdb puppetdb-termini - puppet2
* 18:51 paladox: reboot rdb2
* 18:51 paladox: apt-get dist-upgrade - rdb2
* 18:48 paladox: apt-get upgrade - jobrunner1 (debian update)
* 18:26 paladox: MariaDB [wizpedia101wiki]> update content set content_model = 1 where content_model = 2; - db11
* 17:56 paladox: rebuild lc on test2
* 16:54 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=vilaryawiki /home/reception/Wikipedia-20200802155856.xml on jobrunner1
* 12:08 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildLocalisationCache.php --wiki loginwiki on mw* and jbr*
* 12:07 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/mergeMessageFileList.php --output /srv/mediawiki/config/ExtensionMessageFiles.php --wiki loginwiki' on mw* and jbr*
* 11:59 Reception123: reception@jobrunner1:/srv/mediawiki/w/maintenance$ sudo -u www-data php deleteBatch.php --wiki crappygameswiki --r "Requested - T6028" /home/reception/cgwdel.txt
* 11:51 Reception123: sudo umount /mnt/mediawiki-static and then mount on gluster1

## 2020-08-06 

* 23:55 Southparkfan: create account for user 'Selak' on sailingwiki

## 2020-08-04 

* 15:23 Reception123: running GDPR script

## 2020-08-03 

* 22:19 RhinosF1: INSERT INTO slot_roles (role_id, role_name) VALUES (1, 'main'); on same wiki
* 22:19 RhinosF1: populate content_models for wizpedia101
* 20:15 paladox: set cpu type to host for puppet2
* 20:09 paladox: reboot puppet2
* 20:08 paladox: upgrade puppet2 to debian 10.5
* 20:06 paladox: revert decrease
* 20:00 paladox: reduce puppet2 cores by 1 (so 2 cores instead of 3)
* 19:48 paladox: restarted puppetserver
* 19:14 paladox: upgrade phabricator
* 18:16 Southparkfan: deleted firewall rule 'allow from any to 6379' from rdb[12]
* 16:22 Reception123: re-run the GDPR scripts
* 05:59 Reception123: re-run GDPR scripts
* 05:57 Reception123: nice -5 for the import logged above
* 04:39 Reception123: reception@jobrunner1:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=vilaryawiki /home/reception/Wikipedia-20200802155856.xml
* 04:32 Reception123: reception@jobrunner1:/srv/mediawiki/w/extensions/ManageWiki/maintenance$ sudo -u www-data php populateGroupPermissionsWithDefaults.php --wiki=xhoriawiki --overwrite

## 2020-08-02 

* 21:36 RhinosF1: enforce GDPR
* 20:58 Zppix: GDPR action
* 15:35 Reception123: runJobs on mw7 with specific type
* 14:20 Reception123: GDPR removal

## 2020-08-01 

* 09:58 Reception123: sudo apt-get remove lilypond on mw*/jbr/test2
* 04:50 Reception123: reception@jobrunner1:/srv/mediawiki/w/maintenance$ sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=wizpedia101wiki /home/reception/Wizpedia101-20200730225328.xml
* 04:44 Reception123: reception@jobrunner1:/srv/mediawiki/w/maintenance$ sudo -u www-data php deleteBatch.php --wiki reallifevillainswiki --r "Requested - T5997" /home/reception/rlv5.txt

## 2020-07-31 

* 20:52 RhinosF1: run jobs on metawiki via jobrunner1
* 18:11 RhinosF1: add a runJobs for htmlCacheUpdate in my screen on jobrunner1
* 17:48 Reception123: runJobs.php on meta
* 15:38 Reception123: sudo apt-get upgrade on gluster1/services1/db13/mw5/jobrunner1/rdb1/cp9/mail1/puppet2/db12
* 15:32 Zppix: same for loginwiki
* 15:32 Reception123: reception@jobrunner1:/srv/mediawiki/w/maintenance$ sudo -u www-data php runJobs.php --wiki metawiki
* 12:07 RhinosF1: runJobs on meta+login to ensure backlog stays low
* 10:47 Reception123: reception@mw6:~$ sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/w/cache/databases.json /srv/mediawiki/w/maintenance/runJobs.php --type='LocalGlobalUserPageCacheUpdateJob' on mw6 (backlog is still clogged)
* 10:41 Reception123: manually runJobs on metawiki and loginwiki
* 10:35 Reception123: reception@jobrunner1:/srv/mediawiki/w/maintenance$ sudo -u www-data php deleteBatch.php --wiki reallifevillainswiki --r "Requested - T5987"  /home/reception/rlv4.txt
* 10:32 Reception123: deleted and dropped wizpedia101wiki for recreation
* 09:27 RhinosF1: reset git to remove previous hack
* 09:23 RhinosF1: cherry-picked 3d42d3d onto test2 (will reset after merge)
* 09:07 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildLocalisationCache.php --wiki loginwiki on mw* and jbr1
* 09:05 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/mergeMessageFileList.php --output /srv/mediawiki/config/ExtensionMessageFiles.php --wiki loginwiki' on mw* and jbr1
* 07:43 RhinosF1: jobrunner backlog is critical and being monitored
* 07:04 Reception123: sudo apt-get upgrade on services2
* 06:16 RhinosF1: forcing a manual run of jobs on all wikis to clear backlog as the job runner hasn't crashed yet
* 05:59 Reception123: rebooted jobrunner1
* 05:45 RhinosF1: restart jobrunner (again)
* 05:31 RhinosF1: rhinos@jobrunner1:/var/log/mediawiki$ sudo -u www-data php /srv/mediawiki/w/maintenance/runJobs.php --wiki=wright009wiki
* 05:25 RhinosF1: rhinos@jobrunner1:/var/log/mediawiki$ sudo -u www-data php /srv/mediawiki/w/maintenance/runJobs.php --wiki='wright009wiki' --type='LocalGlobalUserPageCacheUpdateJob' --maxtime='60' --memory-limit='192M' --result=json
* 05:23 Zppix: manually run metawikijobs on jobrunner1
* 05:23 Zppix: manually run loginwiki jobs on jobrunner1
* 05:18 Reception123: sudo service jobrunner restart on jobrunner1
* 05:18 Reception123: sudo service redis-server restart on jobrunner1
* 04:46 RhinosF1: restarted jobrunner service
* 03:01 Zppix: '/usr/local/bin/foreachwikiindblist /srv/mediawiki/w/cache/databases.json /srv/mediawiki/w/maintenance/runJobs -- Jobrunner1 is  not running jobs automatically

## 2020-07-30 

* 17:07 Reception123: sudo apt-get upgrade on services1
* 13:48 John: pull in security updates
* 12:46 Reception123: sudo apt-get upgrade on mw4
* 12:24 RhinosF1: rhinos@jobrunner1:~$ sudo -u www-data nice -19 usr/local/bin/foreachwikiindblist /srv/mediawiki/w/cache/databases.json /srv/mediawiki/w/extensions/GlobalUsage/maintenance/refreshGlobalimagelinks.php --pages=existing,nonexisting
* 12:17 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildLocalisationCache.php --wiki loginwiki on mw* and jbr1
* 12:16 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/mergeMessageFileList.php --output /srv/mediawiki/config/ExtensionMessageFiles.php --wiki loginwiki on mw* and jbr1
* 12:15 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/sql.php --wiki commonswiki /srv/mediawiki/w/extensions/GlobalUsage/sql/GlobalUsage.sql
* 12:06 Reception123: sudo apt-get upgrade on phab1
* 09:26 Reception123: sudo apt-get upgrade on cp7
* 06:52 Reception123: sudo apt-get upgrade on ldap1
* 06:52 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=tuscriaturaswiki /home/reception/Wikipedia-20200709122726.xml
* 06:39 Reception123: reception@jobrunner1:/srv/mediawiki/w/maintenance$ sudo -u www-data php cleanupTitles.php --wiki reallifevillainswiki
* 06:30 Reception123: reception@jobrunner1:/srv/mediawiki/w/maintenance$ sudo -u www-data php namespaceDupes.php --wiki reallifevillainswiki --fix
* 06:28 Reception123: sudo apt-get upgrade on bacula2
* 06:14 Reception123: sudo apt-get upgrade on cp3
* 05:33 Reception123: sudo apt-get upgrade on test2
* 05:18 Reception123: sudo -u www-data php deleteBatch.php --wiki reallifevillainswiki --r "Requested - T5987"  /home/reception/rlv.txt
* 05:09 Reception123: sudo apt-get upgrade on ns2/mw6/cp6/services2/puppet2/gluster2
* 05:05 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildLocalisationCache.php --wiki loginwiki on mw* and jbr1
* 05:05 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/mergeMessageFileList.php --output /srv/mediawiki/config/ExtensionMessageFiles.php --wiki loginwiki

## 2020-07-29 

* 19:20 Southparkfan: install python3-dnspython on mon1
* 18:50 Southparkfan: disable puppet on mon1 for new check

## 2020-07-28 

* 17:17 Reception123: add pcpartswiki discord webhook
* 13:32 Reception123: add discord webhook for reverseunfavorablewikisanduserswiki

## 2020-07-27 

* 18:13 RhinosF1: ban a page in google search console on moviepedia wiki because despite a previous request to clear its cache they still don't understand what a 404 is
* 09:46 Reception123: sudo apt-get upgrade on puppet2
* 07:28 Reception123: sudo apt-get upgrade on misc1

## 2020-07-26 

* 23:13 Southparkfan: added another 3G of swap on db12
* 15:44 RhinosF1: blacklist moviepedia.mh.o/w/index.php? from search console due to duplicate results
* 06:40 Reception123: sudo apt-get upgrade on cp3

## 2020-07-25 

* 22:39 paladox: depool and repool mw7
* 22:37 paladox: depool and repool mw6
* 22:34 paladox: depool and repool mw5
* 22:29 paladox: depool and repool mw4
* 21:42 RhinosF1: drop a bunch of never indexed sitemaps from search console, add the new master index. Will drop all in use ones excluding master once google decide to index the master sitemap.
* 16:39 Reception123: reception@jobrunner1:/srv/mediawiki/w/maintenance$ sudo -u www-data php runJobs.php --wiki yablestudiowiki
* 14:03 paladox: depool and repool mw5
* 14:03 paladox: repool mw4
* 14:02 paladox: restart nginx & php7.3-fpm on mw4
* 14:02 paladox: depool mw4
* 10:35 Reception123: added --active to the above command
* 10:33 Reception123: reception@jobrunner1:/srv/mediawiki/w/maintenance$ sudo -u www-data php initSiteStats.php --update --wiki erislywiki
* 06:32 Reception123: sudo apt-get upgrade on rdb1
* 06:30 Reception123: sudo apt-get upgrade on cp9

## 2020-07-24 

* 22:20 paladox: change cpu units on mw4/5/puppet2 to 1024
* 20:59 paladox: DROP DATABASE wikicubiawiki;
* 20:59 paladox: DROP DATABASE lousyreceptionwikiswiki;
* 20:59 paladox: DROP DATABASE bigbrotherwikiwiki;
* 20:58 paladox: DROP DATABASE abominablememefandomswiki;
* 20:57 paladox: root@jobrunner1:/srv/mediawiki/w/extensions/CreateWiki/maintenance# sudo -u www-data php deleteWikis.php --wiki loginwiki --delete paladox
* 19:46 paladox: rebuild lc on test2, mw* and jobrunner1
* 19:36 paladox: root@jobrunner1:/var/log/mediawiki/debuglogs# rm /tmp/mw-UID*
* 18:00 Reception123: disabled a user on phab
* 10:20 Reception123: added a discord webhook for erislywiki
* 00:16 paladox: root@jobrunner1:/srv/mediawiki/w/maintenance# sudo -u www-data php emptyUserGroup.php --wiki moviepediawiki Wiki_Staff

## 2020-07-23 

* 21:02 paladox: delete editor & employee groups from moviepediawiki

## 2020-07-22 

* 22:54 paladox: set max-active-instances to 3 on puppet2
* 22:43 paladox: increased how many cpus puppetserver can used
* 22:06 paladox: upgrade gluster & puppet-agent on jobrunner1 & test2
* 22:01 paladox: upgrade phabricator on phab1
* 21:59 paladox: upgrade gluster & puppet-agent on mw 4,5,6,7
* 21:57 paladox: upgrade puppet-agent on gluster 1 & 2
* 21:56 paladox: upgrade gluster to 7.7 on gluster 1 & 2
* 21:34 paladox: MariaDB [incidents]> update incidents set i_published = NULL where i_id = 33; - db11
* 21:14 paladox: rebuild lc on mw* and jobrunner1
* 06:10 Reception123: renamed animewiki to shihouwik
* 01:07 Southparkfan: set up 2G swap on db11, non-persistent

## 2020-07-20 

* 19:55 paladox: MariaDB [mhglobal]> delete from matomo where matomo_wiki = 'test1wiki'; - db11
* 19:54 paladox: root@jobrunner1:/srv/mediawiki/w/extensions/MatomoAnalytics/maintenance# sudo -u www-data php modifyMatomo.php --wiki test2wiki
* 19:52 paladox: root@jobrunner1:/srv/mediawiki/w/extensions/MatomoAnalytics/maintenance# sudo -u www-data php modifyMatomo.php --wiki loginwiki
* 18:58 paladox: increase mon1 by 10gb
* 17:46 paladox: root@gluster1:/mnt# gluster volume set mvol performance.open-behind on
* 17:43 paladox: repool mw4
* 17:41 paladox: depool mw4
* 17:37 paladox: set i/o threads to 12 on gluster
* 16:48 paladox: restarted gluster on glusterfs2
* 16:21 paladox: set i/o threads at 9 on gluster
* 15:30 paladox: install gdb on mw4
* 15:04 paladox: root@jobrunner1:/home/paladox# ./foreachwikiindblist /home/paladox/all.dblist /srv/mediawiki/w/maintenance/refreshLinks.php
* 14:39 paladox: root@jobrunner1:/home/paladox# ./foreachwikiindblist /home/paladox/7wikis.dblist /srv/mediawiki/w/maintenance/recountCategories.php --mode=files
* 14:39 paladox: root@jobrunner1:/home/paladox# ./foreachwikiindblist /home/paladox/7wikis.dblist /srv/mediawiki/w/maintenance/recountCategories.php --mode=subcats
* 14:39 paladox: root@jobrunner1:/home/paladox# ./foreachwikiindblist /home/paladox/7wikis.dblist /srv/mediawiki/w/maintenance/recountCategories.php --mode=pages
* 14:02 paladox: reboot mw4 too
* 14:02 paladox: depool and repool mw4
* 13:45 paladox: root@jobrunner1:/home/paladox# ./foreachwikiindblist /home/paladox/all.dblist /srv/mediawiki/w/maintenance/rebuildrecentchanges.php
* 13:33 paladox: root@jobrunner1:/home/paladox# /usr/local/bin/foreachwikiindblist /srv/mediawiki/w/cache/databases.json /srv/mediawiki/w/maintenance/runJobs.php
* 13:10 paladox: killed redis-server and started up (had to kill -9 it as it was just hanging on sudo service redis-server stop) - jobrunner1
* 12:58 RhinosF1: Mediawiki & Redis logs are flooded with errors related to [https://phabricator.miraheze.org/T5939](https://phabricator.miraheze.org/T5939), cause currently unknown.
* 00:48 paladox: reboot jobrunner1 - gluster mount
* 00:44 paladox: root@gluster1:/var/log/glusterfs# gluster volume set mvol open-behind off
* 00:33 Southparkfan: db12: set table_(definition|open)_cache to 4000
* 00:13 Southparkfan: db12 high on mem usage, added 2G swap + entry in /etc/fstab
* 00:03 Southparkfan: start bacula-fd on gluster1

## 2020-07-19 

* 23:58 Southparkfan: stop bacula-fd on gluster1 so I can restart glusterfs (NOT glusterfsd)
* 23:52 Southparkfan: saved memory dump of gluster, tried to do another one but without luck (file stays empty)
* 23:28 Southparkfan: sent SIGUSR1 to glusterfs process on gluster1, per [https://github.com/gluster/glusterfs/issues/1370#issuecomment-658744547](https://github.com/gluster/glusterfs/issues/1370#issuecomment-658744547)
* 16:46 paladox: root@jobrunner1:/srv/mediawiki/w/maintenance# sudo -u www-data php rebuildrecentchanges.php --wiki mini1wiki
* 16:43 paladox: MariaDB [mini1wiki]> delete from logging where log_type = 'comments'; - db11
* 16:33 paladox: drop table Comments and recreate on mini1wiki
* 16:29 paladox: MariaDB [mini1wiki]> delete from Comments where Comment_actor = 0; - db11
* 16:28 paladox: MariaDB [mini1wiki]> delete from Comments where Comment_actor != 0; - db11
* 16:26 paladox: MariaDB [mini1wiki]> delete from Comments where Comment_actor = 0 and Comment_Page_ID = 22; - db11
* 16:25 paladox: MariaDB [mini1wiki]> delete from Comments where Comment_actor = 0 and Comment_Page_ID = 7; -db11
* 16:13 paladox: drop nonsensopediawiki on - db13, not in cw_wikis & [https://phabricator.miraheze.org/T5128](https://phabricator.miraheze.org/T5128)
* 16:04 paladox: root@jobrunner1:/srv/mediawiki/w/maintenance/storage# sudo -u www-data php compressOld.php --wiki ranchstorywiki --type gzip

## 2020-07-18 

* 22:01 RhinosF1: run makeTestEdits.php to test RC Feed
* 19:10 RhinosF1: blacklist [https://moviepedia.miraheze.org/wiki/Once_Upon_a](https://moviepedia.miraheze.org/wiki/Once_Upon_a) in search console
* 14:54 paladox: upgrade puppet-agent puppetdb puppetdb-termini puppetserver - puppet2
* 14:51 paladox: upgrade libnss3 on services*
* 14:51 paladox: upgrade libnss3 on puppet2
* 14:49 paladox: upgrade libnss3 on mw*
* 12:17 Reception123: sudo service ircrcbot start
* 12:15 Reception123: sudo service ircrcbot stop

## 2020-07-17 

* 13:46 paladox: restart logrcbot
* 00:18 paladox: root@jobrunner1:/srv/mediawiki/w/extensions/MatomoAnalytics/maintenance# sudo -u www-data php modifyMatomo.php --wiki dcmultiversewiki
* 00:18 paladox: root@jobrunner1:/srv/mediawiki/w/extensions/MatomoAnalytics/maintenance# sudo -u www-data php modifyMatomo.php --wiki metawiki

## 2020-07-16 

* 19:16 Reception123: reception@jobrunner1:/srv/mediawiki/w/maintenance$ sudo -u www-data php deleteBatch.php --wiki metawiki --r "Requested by MrJaroslavik, accidental import" --u Reception123 /home/reception/metadel.txt
* 18:13 paladox: delete cp8 vps
* 18:08 paladox: rm -rf / - cp8
* 18:08 paladox: rm -rf /etc - cp8
* 18:06 paladox: root@cp8:/home/paladox# wipe /dev/sda1
* 17:37 Southparkfan: installed python3.5 security updates on misc1
* 15:18 paladox: lower cpu units to 900 for puppet2
* 14:06 paladox: revoked cp8 puppet cert
* 13:51 paladox: restart ircrcbot on mon1
* 13:44 paladox: depool, repool and reboot mw4 & 5
* 13:24 paladox: only changed cpu units on mw 4,5 not 6,7
* 13:17 paladox: set cpu to 2 for puppet2
* 13:14 paladox: revert that change
* 13:13 paladox: set cpu cores to 2 for puppet2
* 13:09 paladox: increase cpu units to 2048 on mw 4,5,6,7
* 04:11 paladox: fixed content_models on doctorwhofanfilmsdatabasewiki
* 04:11 paladox: MariaDB [doctorwhofanfilmsdatabasewiki]> INSERT INTO content_models (model_id, model_name) VALUES (5, 'json'); -db11
* 04:08 paladox: MariaDB [doctorwhofanfilmsdatabasewiki]> INSERT INTO slot_roles (role_id, role_name) VALUES (1, 'main'); -db11
* 00:44 paladox: shutdown cp8
* 00:09 paladox: stopped mysql on db9
* 00:08 paladox: sudo -u www-data php changeDBCluster.php --wiki loginwiki --db-cluster c2 --file batch

## 2020-07-15 

* 22:30 paladox: sudo -u www-data php changeDBCluster.php --wiki loginwiki --db-cluster c2 --file batch2
* 22:30 paladox: sudo -u www-data php changeDBCluster.php --wiki loginwiki --db-cluster c2 --file batch
* 15:52 paladox: root@gluster1:/home/paladox# gluster volume set mvol performance.cache-max-file-size 20MB
* 15:50 paladox: increase i/o threads to 40 on gluster
* 15:41 paladox: root@gluster1:/home/paladox# gluster volume set mvol network.inode-lru-limit 600
* 15:08 Southparkfan: removed nagios-plugins-contrib, does not support raid checks for mdadm
* 15:05 Southparkfan: install nagios-plugins-contrib on mon1
* 14:00 Southparkfan: enable puppet on mon1
* 13:38 Southparkfan: disable puppet on mon1 to test a new check
* 00:00 Southparkfan: install security updates for chromium chromium-common chromium-sandbox on test1, restarted proton service

## 2020-07-14 

* 23:51 Southparkfan: cp8 is depooled, replaced by cp9. however, since cp8 is still receiving traffic, and server has been paid for until July, I'll leave nginx/varnish running overnight - if traffic does not stop after 24h (to allow rogue DNS caches to be refreshed), services can be shutdown
* 23:33 paladox: update /usr/share/GeoIP/GeoLite2-Country.mmdb on ns1 & ns2 and restart gdnsd
* 22:25 Southparkfan: installing cp9
* 21:19 Southparkfan: enable flap detection on 'cp8 Current Load'
* 20:04 paladox: root@gluster1:/mnt/mediawiki-static# gluster volume set mvol performance.write-behind on
* 19:50 paladox: root@gluster1:/home/paladox# gluster volume set mvol performance.cache-max-file-size 6MB
* 19:47 paladox: root@gluster1:/home/paladox# gluster volume set mvol performance.cache-refresh-timeout 4
* 19:46 paladox: root@gluster1:/home/paladox# gluster volume set mvol performance.cache-max-file-size 2MB
* 19:28 paladox: install fio on gluster1
* 19:24 paladox: regenerating sitemaps
* 19:21 paladox: root@gluster1:/home/paladox# gluster volume set mvol performance.write-behind off
* 19:20 paladox: root@gluster1:/home/paladox# gluster volume set mvol performance.io-cache off
* 18:09 paladox: restart mariadb on db7
* 10:16 Reception123:  sudo umount /mnt/mediawiki-static and then mount on gluster1

## 2020-07-13 

* 18:25 Zppix: rebuildLC on jobrunner1
* 09:14 RhinosF1: testing and running generateSitemapIndex on jobrunner1
* 00:11 Southparkfan: deleted ufw rule from mon1: allow from 185.52.1.76 to any port 9090 proto tcp

## 2020-07-12 

* 18:00 paladox: fixed .git directory permissions in /srv/mediawiki/w on jobrunner1. Also fixed dirty checkout of Lingo.
* 17:58 paladox: fixed .git directory permissions in /srv/mediawiki/w on mw 4,5,6,7. Also fixed dirty checkout of Lingo.

## 2020-07-11 

* 20:49 paladox: rebuild lc on jobrunner1
* 20:40 paladox: $cw = new CreateWikiJson( 'loginwiki' ); $cw->resetDatabaseList();
* 19:53 Southparkfan: dropped SELECT privilege for exporter@localhost on all database server
* 19:47 Southparkfan: dropped SELECT privilege for exporter@localhost on db9 for testing
* 19:43 Southparkfan: db11: clean up broken sql user, added icinga user
* 19:39 Southparkfan: db9: clean up old sql users, fix icinga user
* 18:08 paladox: varnish> ban req.http.Host == dcmultiverse.miraheze.org - cp8
* 18:07 Southparkfan: set protection for custom variables in icingaweb2
* 17:36 paladox: dropping all closed wikis on db9 - all migrated to db12
* 16:26 Reception123: renamed Carp_Universum to Universal_Omega
* 16:11 Southparkfan: fixed grants for icinga and exporter on db12
* 14:10 Southparkfan: set wiki_dbcluster to NULL for all wikis
* 14:07 Southparkfan: MariaDB [mhglobal]> update cw_wikis set wiki_dbcluster='c4' where wiki_dbname IN('allthetropeswiki', 'nonciclopediawiki');
* 13:16 Southparkfan: ran 'keys WANCache:*' on rdb2 to clean up expired keys,  see [https://grafana.miraheze.org/d/HZGjmu_Zz/redis?orgId=1&from=1594472416500&to=1594473328591&var-instance=rdb2.miraheze.org:9121](https://grafana.miraheze.org/d/HZGjmu_Zz/redis?orgId=1&from=1594472416500&to=1594473328591&var-instance=rdb2.miraheze.org:9121)
* 00:55 Southparkfan: install goaccess on cp3

## 2020-07-10 

* 20:37 paladox: apt-get dist-upgrade - services 1/2
* 19:52 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildLocalisationCache.php --wiki loginwiki on mw* and jbr1
* 19:52 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/mergeMessageFileList.php --output /srv/mediawiki/config/ExtensionMessageFiles.php --wiki loginwiki on mw* and jbr1
* 18:38 Reception123: renamed dcwiki to dcmultiversewiki
* 18:35 Reception123: deleted and dropped dcmultiversewiki (making way for rename)
* 17:55 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildLocalisationCache.php --wiki loginwiki on mw* and jbr1
* 17:54 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/mergeMessageFileList.php --output /srv/mediawiki/config/ExtensionMessageFiles.php --wiki loginwiki on mw* and jbr1
* 14:08 paladox: ALTER TABLE /*_*/cw_comments MODIFY COLUMN cw_comment VARCHAR(2000) NOT NULL; - db9

## 2020-07-09 

* 19:53 paladox: remove empty strings from group * permissions at collegelifewiki
* 17:26 paladox: root@jobrunner1:/srv/mediawiki/w/extensions/ManageWiki/maintenance# sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/extensions/ManageWiki/maintenance/toggleExtension.php syntaxhighlight_geshi
* 15:29 paladox: restart php7.3 on mw7
* 15:29 paladox: mw7 - rm -rf /tmp ; sudo mkdir -m 1777 /tmp
* 15:26 paladox: restart php7.3 on mw5
* 15:26 paladox: mw5 - rm -rf /tmp ; sudo mkdir -m 1777 /tmp
* 13:38 RhinosF1: that's on jobrunner1
* 13:37 RhinosF1: run puppet, manually run generateSitemapIndex, update search console
* 10:50 Reception123: sudo apt-get upgrade on rdb2
* 10:50 Reception123: sudo apt-get upgrade on puppet2
* 10:49 Reception123: sudo apt-get upgrade on mon1 and services2
* 09:19 Reception123: deleted bot-admins and bot-users on GH
* 09:18 Reception123: transferred @bots-pip-auto, @MirahezeBots, @bots-web to the MirahezeBots org + deleted "AntiSpamSopel
* 09:10 Reception123: deleted @miraheze/snitchbot
* 07:36 Reception123: reboot cp6

## 2020-07-08 

* 23:34 RhinosF1: add [https://static.miraheze.org/sitemaps/sitemap.xml](https://static.miraheze.org/sitemaps/sitemap.xml) to GSC, will purge old one's in the morning
* 23:08 paladox: upgrade some packages on mw* and jobrunner1
* 22:58 paladox: rebuild lc test2
* 22:57 paladox: rebuild lc on mw* and jobrunner1
* 21:50 Southparkfan: restarted mysqld exporter on all  servers
* 21:49 Southparkfan: restart mysqld exporter on db9
* 21:29 RhinosF1: blacklisted a page in search console & submitted rechecks for a number of errors
* 21:25 RhinosF1: removed or replaced all broken sitemaps on SearchConsole
* 21:17 Southparkfan: enabled puppet on jobrunner1 and restarted job services
* 20:43 Southparkfan: set pct to 0
* 20:29 Southparkfan: db9: set global innodb_max_dirty_pages_pct = 1;
* 20:18 Southparkfan: added 2GB swapfile on db9 to avoid mariadb OOM - emergency restart planned to reduce mem usage
* 15:14 paladox: root@gluster1:/mnt# gluster volume set mvol network.inode-lru-limit 9000
* 14:36 paladox: root@gluster1:/home/paladox# gluster volume set mvol performance.high-prio-threads 24
* 14:36 paladox: root@gluster1:/home/paladox# gluster volume set mvol performance.normal-prio-threads 24
* 14:36 paladox: root@gluster1:/home/paladox# gluster volume set mvol performance.low-prio-threads 24
* 14:35 paladox: root@gluster1:/home/paladox# gluster volume set mvol performance.cache-size 112MB
* 14:34 paladox: root@gluster1:/home/paladox# gluster volume set mvol network.inode-lru-limit 1000
* 01:23 paladox: apt-get upgrade - db7 (mariadb/kernel and some other packages)

## 2020-07-07 

* 22:46 Southparkfan: applied php7.3 security patches on cluster - for reference: salt-ssh -E '<servers you want to patch>' cmd.run "export DEBIAN_FRONTEND=noninteractive && apt-get install --only-upgrade php7.3* -yq"
* 22:45 paladox: applied php7.3 security patches on cluster - SPF|Cloud
* 22:40 paladox: up rdb1 ram to 8gb
* 22:31 paladox: up rdb2 ram to 8gb
* 22:27 Southparkfan: apply php security updates on test2 for testing
* 22:24 paladox: delete db6 from proxmox
* 22:21 paladox: decom db6
* 22:10 paladox: stop slave on db6
* 22:02 paladox: take db13 out of read only including stopping it being a replica
* 22:01 paladox: MariaDB [(none)]> set global read_only=1; - db7
* 17:07 Reception123: added @The-Voidwalker to bot-admins
* 17:06 Reception123: removed @RhinosF1 from bot-users (redundant)
* 17:04 Reception123: added MacFan4000 to bot-users
* 16:26 Southparkfan: on db6 (replica): delete from phabricator_daemon.daemon_log where id=95166; in order to let that server catch up again
* 16:22 Southparkfan: fixed phabricator_daemon.daemon_log id=95166 entry on db6, start slave, but still not working - exploring other solutions
* 16:19 Southparkfan: stop db6 slave to fix error
* 16:11 Southparkfan: set global read_only=1; on db6
* 13:41 paladox: MariaDB [mhglobal]> update mw_permissions set perm_permissions = '[]' where perm_dbname = 'moviepediawiki' and perm_group = 'assistant'; - db9
* 12:44 RhinosF1: runJobs on all wikis
* 12:08 RhinosF1: test2 has [https://git.io/JJtep](https://git.io/JJtep) cherry-picked to it
* 01:22 Southparkfan: install vmtouch on test2

## 2020-07-06 

* 21:44 paladox: root@jobrunner1:/home/paladox# sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/maintenance/runJobs.php
* 18:52 paladox: remove python3-jinja2 from misc1
* 18:39 paladox: install fio on db12
* 18:07 Reception123: reception@jobrunner1:/srv/mediawiki/w/maintenance$ sudo -u www-data php deleteBatch.php --wiki gdfzwiki /home/reception/delete.txt
* 11:45 Reception123: umount /mnt/mediawiki-static and remount on gluster1
* 10:32 RhinosF1: runJobs
* 01:45 paladox: revert grants
* 01:42 paladox: insert grants temporary so mariabackup can access db9 remotely.
* 01:23 paladox: install sysbench on cloud3
* 01:21 paladox: install sysbench on db11

## 2020-07-05 

* 07:14 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=reallifevillainswiki /home/reception/reallifevillains_pages_full.xml
* 00:37 paladox: regenerating backups on bacula2

## 2020-07-04 

* 23:29 Southparkfan: install sysstat on db9
* 16:18 paladox: echo "" > php-error.log on mw 4,5,6,7 (file size is 3gb plus)
* 15:39 paladox: deleted redis keys for nynthidbwiki & cleared objectcache table
* 13:42 paladox: and repool
* 13:42 paladox: depool mw 4,5,6,7
* 09:39 Reception123: sudo chmod 777 /tmp on mw[57]
* 09:29 Reception123: recreate /tmp on mw[567]
* 09:25 RhinosF1: <correction> [4-7] not [47]
* 09:24 Reception123: cleared /tmp on mw[4-7]
* 07:10 Reception123: /usr/bin/nice -19 /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/generateMirahezeSitemap.php

## 2020-07-03 

* 19:39 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildLocalisationCache.php --wiki loginwiki on jbr1/mw*
* 19:38 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/mergeMessageFileList.php --output /srv/mediawiki/config/ExtensionMessageFiles.php --wiki loginwiki
* 17:58 paladox: depool and repool mw7
* 17:57 paladox: depool and repool mw6
* 17:56 paladox: depool and repool mw5
* 17:56 paladox: depool and repool mw4
* 17:27 paladox: dropping openenventorywikiwiki, pixelsonascreenwiki, popnbookswiki, principatoabbazialedimontesantowiki, reallifeheroeswiki, reallifevillainswiki, reversecrummyscratcherswiki, scratchpadwiki, seleniawiki, streamelementswiki, szkalownicywiki, twitch1wiki, twitchwiki, vapidscratchstudioswiki, wikilirikwiki and yunawiki
* 17:24 paladox: dropping 1920swiki, 4005wikim, anihilatorwiki, assistivecyberneticswiki, awesomewikiwiki, bushcraftpediawiki, bwrwiki, crappyscratchprojectswiki, crummyscratcherswiki, cyclonepediawiki, fnafcommunitywiki, granprincipatodimontesantowiki, heavymetalwiki, incworldwiki and lousyfanfictionswikiwiki
* 16:13 paladox: root@jobrunner1:/srv/mediawiki/w/extensions# php /srv/mediawiki/w/extensions/CreateWiki/maintenance/deleteWikis.php --wiki=loginwiki  paladox --delete

## 2020-07-02 

* 23:41 paladox: update reviewer group on perm_permissions to remove empty strings from the permission table
* 23:40 paladox: update user group on perm_permissions to remove empty strings from the permission table
* 23:38 paladox: update sysop group on perm_permissions to remove empty strings from the permission table
* 23:35 paladox: MariaDB [mhglobal]> update mw_permissions set perm_permissions = '[]' where perm_dbname = 'moviepediawiki' and perm_group = 'autopatrolled'; - db9
* 23:33 paladox: delete rollbacker on moviepediawiki
* 23:26 paladox: delete groups _volunteer_developers, content_moderator, staff_member, autoreview and interface_administrators on moviepediawiki
* 23:24 paladox: delete from mw_permissions where perm_dbname = 'moviepediawiki' and perm_permissions = 'content_team'; - db9 (should probably use managewikiperm object for future deletion)
* 22:04 RhinosF1: some users may experience issues connection to cp3 via indonesian ISPs. We can not help this, We may be blocked, Logging this for the record so people know who to question. Please advise users to complain to their ISP.
* 09:45 RhinosF1: initSiteStats and rebuild RC for the two wikis with finished imports

## 2020-07-01 

* 23:17 Southparkfan: add 2G of swap on db9
* 23:07 paladox: killed matomo on mon1 (archive script)
* 20:47 paladox: MariaDB [wizpedia101wiki]> INSERT INTO slot_roles (role_id, role_name) VALUES (1, 'main'); - db9
* 13:21 paladox: upgrade ca-certificates puppet-agent - phab1
* 13:20 paladox: upgrade ca-certificates imagemagick-6-common libmagickcore-6.q16-6 libmagickwand-6.q16-6 - mail1
* 13:17 paladox: upgrade puppet-agent - ns2
* 13:17 paladox: upgrade ca-certificates puppet-agent - cp3
* 13:16 paladox: upgrade puppet-agent - cp7
* 13:15 paladox: upgrade puppet-agent - cp6
* 13:14 paladox: upgrade puppet-agent - cp8
* 13:14 paladox: upgrade ca-certificates - services2
* 13:13 paladox: upgrade ca-certificates - services1
* 13:12 paladox: upgrade ca-certificates puppet-agent - ldap1
* 13:11 paladox: upgrade imagemagick-6-common libmagickcore-6.q16-6 libmagickwand-6.q16-6 - mon1
* 13:10 paladox: upgrade icingaweb2 - mon1
* 13:09 paladox: upgrade grafana - mon1
* 13:08 paladox: apt-get upgrade - test2 & jobrunner1
* 13:06 paladox: apt-get upgrade - mw[567]
* 13:04 paladox: apt-get upgrade - ns1
* 13:03 paladox: apt-get upgrade - mw4
* 12:15 paladox: switch off TUN on ns1 and reboot
* 07:05 Reception123: reception@jobrunner1:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/dumpBackup.php --wiki tmewiki --full > /home/reception/tmewiki01072020.xml (wikibackups)

## 2020-06-30 

* 09:05 RhinosF1: import botswiki dumps
* 08:13 Reception123: reception@jobrunner1:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/dumpBackup.php --wiki zhdelwiki --full > /home/reception/zhdelwiki30062020.xml (wikibackups)

## 2020-06-29 

* 19:55 Reception123: added a discord webhook
* 18:46 Reception123: reception@jobrunner1:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/dumpBackup.php --wiki nltramswiki --full > /home/reception/nltramswiki29062020.xml  (part of wikibackups)
* 17:32 paladox: gluster volume set mvol diagnostics.latency-measurement on ; gluster volume set mvol diagnostics.count-fop-hits on - gluster1
* 17:28 paladox: gluster volume set mvol client.event-threads 7 - gluster1
* 17:28 paladox: gluster volume set mvol server.event-threads 7 - gluster1
* 17:27 paladox: gluster volume set mvol diagnostics.latency-measurement off - gluster1
* 17:27 paladox: gluster volume set mvol diagnostics.count-fop-hits off - gluster1
* 17:05 paladox: gluster volume set mvol features.cache-invalidation-timeout 60 - gluster1
* 17:03 paladox: gluster volume set mvol client.event-threads 5 - gluster1
* 17:02 paladox: gluster volume set mvol server.event-threads 5 - gluster1
* 15:58 paladox:  gluster volume set mvol network.inode-lru-limit 100000 - gluster1
* 15:57 paladox: gluster volume set mvol performance.io-thread-count 12 - gluster1
* 15:54 paladox: gluster volume set mvol performance.cache-refresh-timeout 1 - gluster1
* 15:52 paladox: gluster volume set mvol performance.cache-size 32MB - gluster1
* 15:29 paladox: install salt-ssh on puppet2
* 15:28 paladox: upgrade ca-certificates on puppet2
* 13:02 RhinosF1: run createLocalAccount.php on all wikis for ZppixBot to hopefully make it less likely as wikis are added to say login error if there's no account.
* 11:01 RhinosF1: importDump.php for T5831
* 10:56 RhinosF1: importDump.php for T5829
* 08:00 Reception123: umount /mnt/mediawiki-static on mw4
* 05:37 Reception123: deleted and dropped doctorwhofanfilmsdatabasewiki

## 2020-06-28 

* 16:17 RhinosF1: runJobs done
* 15:16 RhinosF1: runJobs on all wikis
* 14:39 Southparkfan: earlier today, cp6 crashed due to [https://github.com/varnishcache/varnish-cache/issues/2814](https://github.com/varnishcache/varnish-cache/issues/2814). no evidence was found cp6 exhausted the available threads. if this occurs again, we want to consider applying the workaround?
* 11:59 paladox: restart varnish on cp6
* 11:58 paladox: restart sunnel4 and nginx on cp6

## 2020-06-27 

* 21:29 paladox: run runJobs for all wikis on jobrunner1
* 16:39 paladox: populated yourcreatureswiki sites table
* 16:37 paladox: populated tuscriaturaswiki sites table
* 16:35 paladox: populated intercriaturaswiki sites table
* 12:38 paladox: remounted /mnt/mediawiki-static on mw*
* 12:11 paladox: installing tcptrack on mw6
* 12:00 paladox: varnish> ban req.http.Host == static.miraheze.org - cp[3678]
* 11:43 paladox: restarted glusterd on gluster[12] and also restart ircecho on mon1

## 2020-06-26 

* 23:24 paladox: depool, repool and restart nginx mw[4567]
* 22:02 paladox: restarted jobrunner on jobrunner1
* 22:02 paladox: restarted jobchron on jobrunner1
* 22:00 paladox: root@jobrunner1:/srv/mediawiki/w/maintenance# sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/maintenance/runJobs.php
* 19:43 paladox: restarted icinga2
* 19:43 paladox: root@mon1:/etc/icinga2# cp /var/lib/icinga2/ca//ca.crt /var/lib/icinga2/certs//ca.crt
* 19:27 paladox: remove icinga* from mon1 - accidentally removed just realised (thought it was misc1)
* 19:23 paladox: upgrade grafana - mon1
* 19:22 paladox: upgrade  ca-certificates - bacula2
* 16:17 paladox: remounted /mnt/mediawiki-static on mw6
* 15:42 paladox: upgrade ca-certificates - gluster2
* 15:41 paladox: upgrade ca-certificates - gluster1
* 14:29 paladox: increase jobrunner1 disk by 10g
* 14:24 paladox: increase jobrunner1 disk by 10g
* 12:34 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/dumpBackup.php --wiki allthetropeswiki --full > /home/reception/allthetropeswiki26062020.xml (part of wikibackups)
* 09:17 Reception123: umount /mnt/mediawiki-static on mw4/6/7 (mounted automatically after)

## 2020-06-25 

* 09:11 RhinosF1: rebuildlc on jbr1,test1,mw[4-6]

## 2020-06-24 

* 23:19 paladox: rebuild lc on mw* and jobrunner1
* 22:32 paladox: migrating jobrunner1 to cloud1 and test2 to cloud2 (even out the load)
* 20:53 paladox: migrating test2 to cloud1
* 20:36 paladox: upgrade icinga2
* 20:34 paladox: upgrade grafana on mon1
* 20:24 paladox: migrate jobrunner1 to cloud2 to reduce some preasure
* 19:56 paladox: drop grafana from db6 (migrated to db9)
* 19:47 paladox: restarted phd
* 19:33 paladox: MariaDB [uncyclopediawiki]> truncate objectcache; - db6
* 17:54 paladox: rebuild lc on mw* and jobrunner1
* 11:58 RhinosF1: rhinos@jobrunner1:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildall.php --wiki=thefinalrumblewiki and initSiteStats after mass deletion
* 10:46 RhinosF1: running delete batch for another 28 pages that didn't pick up
* 08:29 RhinosF1: delete labster[at]miraheze.org from active status.miraheze.wiki invites
* 08:26 RhinosF1: rhinos@jobrunner1:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/deleteBatch.php --i=3 --r="Requested in [phab:T5794](https://meta.miraheze.org/wiki/phab:T5794)" --wiki=thefinalrumblewiki /home/rhinos/t5794.txt
* 06:26 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildall.php --wiki testwiki
* 02:38 paladox: restart gdnsd on ns1
* 02:38 paladox: root@ns1:/etc/gdnsd# git reset --hard origin/master - modified files, reset.
* 02:25 paladox: apt-get --purge remove nginx* - ldap1
* 02:25 paladox: apt-get --purge remove python3-setuptools - ldap1
* 01:46 paladox: upgrade phabricator on phab1

## 2020-06-23 

* 18:50 paladox: root@jobrunner1:/home/paladox# sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/maintenance/runJobs.php
* 09:10 RhinosF1: also update our email to tech@
* 09:05 RhinosF1: remove my own email from status subscribers and switch staff@ to point to tech@

## 2020-06-22 

* 23:49 RhinosF1: sudo -u www-data php /srv/mediawiki/w/maintenance/changePassword.php --user=ZppixBot --password=<redacted> --wiki=loginwiki (per request of MacFan)
* 22:51 RhinosF1: both done
* 22:50 RhinosF1: rhinos@mw4:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/refreshLinks.php  --namespace=6 --category=Videos --wiki=thefinalrumblewiki
* 22:23 RhinosF1: rhinos@mw4:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/deleteBatch.php --r="Requested on Discord" --i=2 --wiki=thefinalrumblewiki /home/rhinos/catvid.txt
* 21:36 RhinosF1: run rhinos@mw4:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/purgeList.php --namespace=2 --wiki=rf1botwiki to test my access (without --purged and only one page)
* 20:49 paladox: root@misc1:/var/mail# chown -R rhinosf1:rhinosf1 /home/rhinosf1/
* 20:39 Reception123: created mail account for rhinosf1@
* 20:30 Reception123: added RhinosF1 to @miraheze GitHub project as mw-admins

## 2020-06-21 

* 01:43 paladox: reinstall ldap on ldap1

## 2020-06-20 

* 19:13 Reception123: manually reset password for a user
* 19:07 Reception123: deleted an entry from bot_passwords
* 15:57 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildLocalisationCache.php --wiki loginwiki on mw*/jbr1
* 14:37 John: reduce test2's vCPU to 2 (from 4)
* 07:13 Reception123: gzip access.log.3 on cp8 (lack of disk space)

## 2020-06-19 

* 11:14 Reception123: running wikibackups on jobrunner1 (bash ./wikibackups.sh /home/reception/backupwikis.dblist /srv/mediawiki/w/maintenance/dumpBackup.php)
* 10:38 Reception123: MariaDB [factoriomodswiki]> INSERT INTO content_models (model_id, model_name) VALUES (4, 'Scribunto');
* 10:38 Reception123: MariaDB [factoriomodswiki]> INSERT INTO content_models (model_id, model_name) VALUES (2, 'css');
* 10:38 Reception123: MariaDB [factoriomodswiki]> INSERT INTO content_models (model_id, model_name) VALUES (3, 'javascript');
* 10:38 Reception123: MariaDB [factoriomodswiki]> INSERT INTO content_models (model_id, model_name) VALUES (5, 'json');
* 10:38 Reception123: MariaDB [factoriomodswiki]> INSERT INTO content_models (model_id, model_name) VALUES (1, 'wikitext');

## 2020-06-18 

* 16:12 John: fixing stuck global rename (Tarbiz)
* 05:34 Reception123: renamed navywiki to militarywiki

## 2020-06-17 

* 17:34 paladox: restarted cp6
* 17:32 paladox: revert that change for now
* 17:31 paladox: change cpu type to kvm64 & lower cores to 3 on cp6
* 17:30 paladox: that's on db6
* 17:30 paladox: restarted prometheus-mysqld-exporter earlier

## 2020-06-16 

* 22:25 Southparkfan: install apache2-utils on cp6 and cp7
* 22:21 paladox: apt-get upgrade (puppet-agent) - misc1
* 22:18 paladox: reboot misc1
* 21:27 paladox: reboot cp7
* 21:27 paladox: change cpu type to host on cp7
* 21:25 paladox: up cp7 cores to 4
* 21:18 Southparkfan: enable puppet on cp6, instead locally applied change to puppet2's git
* 21:10 Southparkfan: disable puppet on cp6 for T5762
* 20:54 paladox: increase cp6 ram to 3gb matches cp7
* 20:50 paladox: apt-get install ca-certificates - ns2
* 20:47 paladox: change cp6 cpu to host
* 20:47 paladox: increase cp6 cores to 4 and reboot
* 18:20 Reception123: reception@jobrunner1:/srv/mediawiki/w/maintenance$ sudo -u www-data php refreshLinks.php --wiki=tuscriaturaswiki
* 16:36 Reception123: sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/maintenance/runJobs.php
* 16:05 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=wizpedia101wiki --report=1 Wizpedia101-20200615213415.xml
* 10:40 Reception123: deleted and dropped wizpedia101wiki
* 10:21 paladox: root@jobrunner1:/srv/mediawiki/w/extensions/ManageWiki/maintenance# sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/extensions/ManageWiki/maintenance/modifyGroupPermission.php --all --removeperms oathauth-api-all

## 2020-06-15 

* 18:34 Zppix: rebuildRC and initsitestats on wizpedia101wiki after completion of T5760
* 16:00 paladox: varnish> ban req.http.Host == allthetropes.org && req.url ~ "^/wiki/File:Pain5.jpg" - cp8
* 15:07 paladox: varnish> ban req.http.Host == static.miraheze.org && req.url ~ "^/allthetropeswiki/4/4e/Pain5.jpg" - cp8
* 05:50 Reception123: renamed feralworthwikiwiki to feraltradinghandbookwiki

## 2020-06-14 

* 23:18 paladox: root@jobrunner1:/home/paladox# sudo -u www-data php resetWikiCaches.php --wiki=prodlegendsdiscussionwiki
* 23:18 paladox: MariaDB [mhglobal]> update mw_permissions set perm_autopromote = NULL where perm_dbname = 'prodlegendsdiscussionwiki' and perm_group = 'wig_(gacha_w1z4rd)'; - db9
* 22:50 paladox: root@jobrunner1:/home/paladox# sudo -u www-data php resetWikiCaches.php --wiki=2b2twiki
* 22:50 paladox: MariaDB [mhglobal]> update mw_permissions set perm_autopromote = NULL where perm_dbname = '2b2twiki' and perm_group = 'president'; - db9
* 11:51 Reception123: deleted wiki and dropped factoriomodswiki
* 08:54 Reception123: renamed thecorporationwiki to corpcartographywiki

## 2020-06-12 

* 19:45 paladox: restarted php7.3-fpm on mw4
* 14:28 paladox: MariaDB [mhglobal]> update mw_permissions set perm_autopromote = NULL where perm_dbname = 'moviepediawiki' and perm_group = 'staff'; - db9
* 13:44 paladox: MariaDB [mhglobal]> update mw_permissions set perm_autopromote = NULL where perm_group = '高位管理者' and perm_dbname = 'warshipswiki'; - db9
* 07:33 Reception123: renamed encyclopediamiraheziawiki to encycmhwiki.

## 2020-06-11 

* 23:00 paladox: stopping mysql on db8, moving block storage to db9 and start mysql up on db9
* 18:05 paladox: root@jobrunner1:/srv/mediawiki/w# sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/maintenance/sql.php /srv/mediawiki/w/extensions/Echo/db_patches/patch-increase-varchar-echo_unread_wikis-euw_wiki.sql

## 2020-06-10 

* 19:57 paladox: ran manual update command to remove blacklisted perm from twitchwiki
* 19:26 paladox: cancelled the above, not needed, already done
* 19:25 paladox: root@jobrunner1:/home/paladox# sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /home/paladox/resetWikiCaches.php (at 19:22 utc)
* 18:53 paladox: run modifyGroupPermission.php on jobrunner1 (removing blacklisted perm)

## 2020-06-09 

* 20:24 paladox: MariaDB [mhglobal]> update mw_permissions set perm_autopromote = NULL where perm_dbname = 'toramwiki' and perm_group = 'autoconfirmed'; - db8 & T5725
* 17:26 Zppix: UPDATE oauth_registered_consumer SET oarc_callback_url=' [https://iabot.toolforge.org/oauthcallback.php'](https://iabot.toolforge.org/oauthcallback.php') WHERE oarc_callback_url=' [https://tools.wmflabs.org/iabot/oauthcallback.php'](https://tools.wmflabs.org/iabot/oauthcallback.php'); using sql.php on jobrunner1

## 2020-06-07 

* 22:30 paladox: apt-get upgrade - test2
* 22:30 paladox: sudo -u www-data php composer.phar install in /srv/mediawiki/w/extensions/Widgets on mw* and jobrunner1 and test2
* 19:25 paladox: started replica on db7
* 16:48 paladox: upgrade ca-certificates libgnutls30 puppet-agent on rdb[12]
* 15:59 paladox: recreate slave on db7
* 15:55 paladox: package upgrade not available on cp3
* 15:54 paladox: upgrade ca-certificates libgnutls30 on cp[3678]
* 15:51 paladox: upgrade ca-certificates libgnutls30 on dbt1, db[67]
* 15:49 paladox: upgrade ca-certificates libgnutls30 on mw[4567]
* 15:44 paladox: upgrade ca-certificates libgnutls30 on jobrunner1
* 15:24 paladox: depool mw7, and repool (deploying strict firewall)
* 15:22 paladox: depool mw6, and repool (deploying strict firewall)
* 15:16 paladox: depool mw5, and repool (deploying strict firewall)
* 15:11 paladox: depool mw4, and repool (deploying strict firewall)
* 03:43 paladox: apt-get upgrade - mail1 (libgnutls30)
* 03:42 paladox: apt-get upgrade - bacula2 (libgnutls30 puppet-agent)
* 03:35 paladox: regenerating backups on bacula2

## 2020-06-06 

* 23:31 paladox: depool, repool and change cpu to host on jobrunner1
* 23:27 paladox: depool, repool and change cpu to host on mw6
* 23:27 paladox: depool, repool and change cpu to host on mw7
* 23:22 paladox: rebuild lc on mw* and jobrunner1
* 22:55 paladox: rebuild lc on mw* & jobrunner1
* 22:45 paladox: depool and repool mw[67]
* 22:43 paladox: depool and repool mw[45]
* 22:13 paladox: depool mw5, repool and also change cpu type to host
* 21:55 paladox: depool mw4, repool and also change cpu type to host
* 20:50 paladox: upgrade libgnutls30 on test2
* 20:49 paladox: set cpu to host on test2 & reboot
* 14:49 paladox: running runJobs in foreach on jobrunner1
* 14:43 paladox: npm install on mw* & jobrunner1 & test2 in /srv/mathoid
* 14:35 paladox: upgrade nodejs on mw[4567] & test2 & jobrunner1
* 13:52 paladox: upgrade nodejs & puppet-agent on services[12]
* 13:50 paladox: upgrade nodejs & puppet-agent on mail1

## 2020-06-04 

* 23:50 paladox: MariaDB [mhglobal]> update mw_permissions set perm_addgroups = '[]', perm_removegroups = '[]' where perm_addgroups = 'null' and perm_removegroups = 'null' and perm_dbname = 'arefem2wiki';
* 23:49 paladox: MariaDB [mhglobal]> update mw_permissions set perm_addgroups = '[]', perm_removegroups = '[]' where perm_addgroups = 'null' and perm_removegroups = 'null' and perm_dbname = 'ccewiki';
* 23:49 paladox: MariaDB [mhglobal]> update mw_permissions set perm_addgroups = '[]', perm_removegroups = '[]' where perm_addgroups = 'null' and perm_removegroups = 'null' and perm_dbname = 'crappyscratchprojectswiki';
* 23:48 paladox: MariaDB [mhglobal]> update mw_permissions set perm_addgroups = '[]', perm_removegroups = '[]' where perm_addgroups = 'null' and perm_removegroups = 'null' and perm_dbname = 'dndsrdplwiki';
* 23:48 paladox: MariaDB [mhglobal]> update mw_permissions set perm_addgroups = '[]', perm_removegroups = '[]' where perm_addgroups = 'null' and perm_removegroups = 'null' and perm_dbname = 'femthbingenwiki';
* 23:47 paladox: MariaDB [mhglobal]> update mw_permissions set perm_addgroups = '[]', perm_removegroups = '[]' where perm_addgroups = 'null' and perm_removegroups = 'null' and perm_dbname = 'landsofbjortolfiawiki';
* 23:47 paladox: MariaDB [mhglobal]> update mw_permissions set perm_addgroups = '[]', perm_removegroups = '[]' where perm_addgroups = 'null' and perm_removegroups = 'null' and perm_dbname = 'modularwiki';
* 23:47 paladox: MariaDB [mhglobal]> update mw_permissions set perm_addgroups = '[]', perm_removegroups = '[]' where perm_addgroups = 'null' and perm_removegroups = 'null' and perm_dbname = 'reversecrummyscratcherswiki';
* 23:46 paladox: MariaDB [mhglobal]> update mw_permissions set perm_addgroups = '[]', perm_removegroups = '[]' where perm_addgroups = 'null' and perm_removegroups = 'null' and perm_dbname = 'sylvsongcontestwiki';
* 23:46 paladox: MariaDB [mhglobal]> update mw_permissions set perm_addgroups = '[]', perm_removegroups = '[]' where perm_addgroups = 'null' and perm_removegroups = 'null' and perm_dbname = 'tomswiki';
* 23:45 paladox: MariaDB [mhglobal]> update mw_permissions set perm_addgroups = '[]', perm_removegroups = '[]' where perm_addgroups = 'null' and perm_removegroups = 'null' and perm_dbname = 'tomwiki';
* 23:01 paladox: MariaDB [mhglobal]> update mw_permissions set perm_addgroups = '[]', perm_removegroups = '[]' where perm_addgroups = 'null' and perm_removegroups = 'null' and perm_dbname = 'test2wiki';
* 22:38 paladox: root@jobrunner1:/home/paladox# sudo -u www-data php resetWikiCaches.php --wiki=worldtrainwikiwiki
* 22:37 paladox: MariaDB [mhglobal]> update mw_permissions set perm_addgroups = '[]', perm_removegroups = '[]' where perm_addgroups = 'null' and perm_removegroups = 'null' and perm_dbname = 'worldtrainwikiwiki';
* 22:32 paladox: root@jobrunner1:/home/paladox# sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/maintenance/runJobs.php
* 18:50 Reception123: added discord webhook for dothrakiwiki
* 14:08 paladox: upgrade packages on test2 & jobrunner1 (gluster and a bunch of other packages)
* 14:02 paladox: upgrade packages on mw[4567] (gluster and a bunch of other packages)
* 13:59 paladox: upgrade puppet-agent puppetdb puppetdb-termini puppetserver - puppet2
* 13:58 paladox: apt-get upgrade - gluster1/glustet2 (gluster, puppet-agent and a few other packages)
* 12:16 Reception123: renamed neobulbawiki to marionetworkwiki. (db+script)

## 2020-06-03 

* 20:14 paladox: MariaDB [test2wiki]> truncate objectcache; - db6 & db7
* 20:12 paladox: MariaDB [(none)]> CHANGE MASTER TO MASTER_SSL_CA='/etc/ssl/certs/Sectigo.crt', MASTER_SSL_CERT='/etc/ssl/certs/wildcard.miraheze.org.crt', MASTER_SSL_KEY='/etc/ssl/private/wildcard.miraheze.org.key'; - db7
* 20:07 paladox: reload nginx on mw*, jobrunner1 & cp*
* 19:01 paladox: restarting mysql on dbt1 & db6
* 18:22 paladox: rebuild lc on test2
* 15:48 paladox: MariaDB [test2wiki]> truncate objectcache; - db7
* 15:45 paladox: MariaDB [test2wiki]> truncate objectcache; - db6
* 14:24 paladox: reboot db7
* 14:20 paladox: stopping mysql on db7 (service mysql stop)
* 13:50 Southparkfan: delete port 3307 rule on dbt1
* 13:48 paladox: upgrade grafana on mon1
* 13:23 Southparkfan: disable puppet on test2 to test TLS chain change

## 2020-06-02 

* 16:33 paladox: root@jobrunner1:/srv/mediawiki/w/extensions/ManageWiki/maintenance# sudo -u www-data php toggleExtension.php --wiki=test2wiki templatedata --disable
* 08:18 Reception123: $cWJ = new CreateWikiJson( metawiki); $cWJ->resetWiki();
* 07:59 Reception123: MariaDB [mhglobal]> UPDATE cw_wikis SET wiki_url = " [https://meta.miraheze.org](https://meta.miraheze.org)" WHERE wiki_dbname = 'metawiki';
* 07:51 Reception123: MariaDB [mhglobal]> UPDATE cw_wikis SET wiki_url = 'NULL' WHERE wiki_dbname = 'metawiki';

## 2020-06-01 

* 14:40 paladox: root@jobrunner1:/home/paladox# sudo -u www-data php resetWikiCaches.php --wiki=gat398suwiki
* 14:39 paladox: MariaDB [mhglobal]> update mw_permissions set perm_autopromote = NULL where perm_group = 'gat398_class' and perm_dbname = 'gat398suwiki';
* 13:00 Reception123: UPDATE cw_requests SET cw_status = "approved" WHERE cw_id = "12404";

## 2020-05-31 

* 16:28 paladox: root@jobrunner1:/srv/mediawiki/w/extensions/MirahezeMagic/maintenance# sudo -u www-data php addExtension.php --wiki=loginwiki

## 2020-05-30 

* 22:50 paladox: restart dovecot on misc1
* 22:49 paladox: restart postfix on misc1
* 22:49 paladox: nginx reload on m[4567], jobrunner1 & test2 - does not automatically reload on wildcard.miraheze.org.crt changes
* 22:39 paladox: nginx reload on cp[368] - does not automatically reload on wildcard.miraheze.org.crt changes
* 22:35 paladox: nginx reload on cp7 - does not automatically reload on wildcard.miraheze.org.crt changes
* 14:08 Southparkfan: manually inserting a log entry for fswahlen does not seem to be possible via logEntry() in WikiManager when executed from eval.php, due to wrong context
* 14:07 Southparkfan: ran the following due to partially failed creation: $wm = new WikiManager( 'fswahlenwiki' ); $wm->notificationsTrigger( 'creation', 'fswahlenwiki', [ 'siteName' => 'Foodsharing - AG Wahlen' ], 'Heinz' );
* 14:01 Southparkfan: manually promoted requested for fswahlenwiki to sysop/bureaucrat, created main page
* 13:55 Southparkfan: ran MatomoAnalytics::addSite( 'fswahlenwiki' );
* 13:43 Southparkfan: change TLS settings for db7 replication to reflect changes: [https://meta.miraheze.org/wiki/Tech:MariaDB#Replicate_from_master](https://meta.miraheze.org/wiki/Tech:MariaDB#Replicate_from_master)
* 13:27 Southparkfan: remove stunnel package from test2 and enable puppet
* 13:27 Southparkfan: disable puppet on db7 to apply patch there too

## 2020-05-29 

* 16:35 paladox: root@dbt1:/home/paladox# ip addr del fe80::f816:3eff:fe5d:3eae/64 dev eth0

## 2020-05-28 

* 22:26 paladox: upgrade libunbound8 on mail1
* 17:44 paladox: root@jobrunner1:/home/paladox# sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=traentorwiki --report=1 Wikipedia-20200527085130.xml -  T5665
* 17:43 paladox: root@jobrunner1:/home/paladox# sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=traentorwiki --report=1 Wikipedia-20200527085418.xml -  T5665

## 2020-05-27 

* 19:34 paladox: upgrade grafana libunbound8 - mon1
* 19:04 paladox: MatomoAnalyticsHooks::wikiCreation( 'loginwiki' ); (using eval on jobrunner1)
* 16:04 paladox: root@jobrunner1:/srv/mediawiki/w/extensions/MirahezeMagic/maintenance# sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/removeColumnSP.php
* 15:49 paladox: root@jobrunner1:/srv/mediawiki/w/extensions/MirahezeMagic/maintenance# sudo -u www-data php updateSP.php --wiki=degreesoflewditywiki
* 15:22 paladox: root@jobrunner1:/srv/mediawiki/w/extensions/ManageWiki/maintenance# sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/extensions/ManageWiki/maintenance/toggleExtension.php news --disable
* 13:32 paladox: MariaDB [mhglobal]> update mw_permissions set perm_removegroups = '[]' where perm_removegroups = 'null';
* 13:32 paladox: root@jobrunner1:/home/paladox# sudo -u www-data php resetWikiCaches.php --wiki=nerdzonewiki
* 13:31 paladox: MariaDB [mhglobal]> update mw_permissions set perm_addgroups = '[]' where perm_addgroups = 'null';
* 06:47 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki loginwiki /home/reception/Meta-20200527061010.xml

## 2020-05-26 

* 23:58 paladox: MariaDB [mhglobal]> update mw_permissions set perm_removegroups = '[]' where perm_removegroups = 'null';
* 23:58 paladox: MariaDB [mhglobal]> update mw_permissions set perm_addgroups = '[]' where perm_addgroups = 'null';
* 23:54 paladox: MariaDB [mhglobal]> update mw_permissions set perm_autopromote = NULL where perm_autopromote = '{"add":null}' and perm_dbname = 'gmindwiki';
* 23:54 paladox: MariaDB [mhglobal]> update mw_permissions set perm_autopromote = NULL where perm_autopromote = '{"add":null}' and perm_dbname = 'foxdenwiki';
* 23:54 paladox: MariaDB [mhglobal]> update mw_permissions set perm_autopromote = NULL where perm_autopromote = '{"add":null}' and perm_dbname = 'congqiyuanwiki';
* 23:50 paladox: MariaDB [mhglobal]> update mw_permissions set perm_autopromote = NULL where perm_autopromote = '{"add":null}' and perm_dbname = 'almaworldwiki'; - dbt1
* 23:45 paladox: root@jobrunner1:/home/paladox# sudo -u www-data php resetWikiCaches.php --wiki=gvdswiki
* 23:45 paladox: MariaDB [mhglobal]> update mw_permissions set perm_autopromote = NULL where perm_autopromote = '{"add":null}' and perm_dbname = 'gvdswiki'; - dbt1
* 18:01 paladox: root@jobrunner1:/var/log/mediawiki/debuglogs# sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/maintenance/runJobs.php
* 14:24 paladox: MariaDB [mhglobal]> update mw_permissions set perm_autopromote = NULL where perm_dbname = 'awiconwiki' and perm_autopromote = '{"add":null}';

## 2020-05-25 

* 20:40 paladox: root@jobrunner1:/srv/mediawiki/w/extensions/ManageWiki/maintenance# sudo -u www-data php populateGroupPermissionsWithDefaults.php --wiki=thefifthcyclerpgwiki --overwrite
* 20:39 paladox: MariaDB [mhglobal]> delete from mw_permissions where perm_dbname = 'thefifthcyclerpgwiki' and perm_group = 0; - dbt1
* 16:53 paladox: rebuild lc on jobrunner1
* 16:53 paladox: rebuild lc on mw*
* 13:06 Reception123: add discord webhook for superwikiwiki
* 12:17 Reception123: reception@jobrunner1:/srv/mediawiki/w/maintenance$ sudo -u www-data php importDump.php --wiki traentorwiki /home/reception/Wikipedia-20200504044331.xml

## 2020-05-24 

* 23:21 paladox: root@jobrunner1:/srv/mediawiki/w# sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/maintenance/sql.php /srv/mediawiki/w/extensions/Flow/db_patches/patch-increase-varchar-flow_wiki_ref-ref_src_wiki.sql
* 23:21 paladox: root@jobrunner1:/srv/mediawiki/w# sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/maintenance/sql.php /srv/mediawiki/w/extensions/Flow/db_patches/patch-increase-varchar-flow_ext_ref-ref_src_wiki.sql
* 09:09 Reception123: added DS webhook for bttmbookswiki
* 05:40 Reception123: reception@jobrunner1:/srv/mediawiki/w/maintenance$ sudo -u www-data php importDump.php --wiki mercstoriawiki /home/reception/mercstoriaenglish_pages_full.xml

## 2020-05-23 

* 18:35 paladox: root@jobrunner1:/srv/mediawiki/w/maintenance# sudo -u www-data php rebuildtextindex.php --wiki=trollpastawikiwiki
* 18:34 paladox: MariaDB [trollpastawikiwiki]> ALTER TABLE /*_*/searchindex MODIFY si_title MEDIUMTEXT NOT NULL; - db6
* 15:55 paladox: upgrade phabricator on phab1
* 15:52 paladox: reinstall php & nginx on phab1
* 15:51 paladox: upgrade libicu63 on phab1
* 12:56 paladox: root@jobrunner1:/srv/mediawiki/w/extensions/MirahezeMagic/maintenance# sudo -u www-data php updateSP.php --wiki=rotompediawiki
* 12:46 paladox: root@jobrunner1:/home/paladox# sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /home/paladox/resetWikiCaches.php
* 12:44 paladox: MariaDB [mhglobal]> update mw_permissions set perm_addgroups = '[]' where perm_addgroups = 'null'; - dbt1
* 12:43 paladox: MariaDB [mhglobal]> update mw_permissions set perm_removegroups = '[]' where perm_removegroups = 'null'; - dbt1
* 12:31 Reception123: sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/extensions/ManageWiki/maintenance/toggleExtension.php --disable sitescout

## 2020-05-22 

* 21:27 paladox: rebuild lc on mw*
* 20:43 paladox: root@jobrunner1:/home/paladox# sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/maintenance/sql.php /srv/mediawiki/w/extensions/Comments/sql/patches/actor/drop-cb_user_id-index.sql
* 20:42 paladox: root@jobrunner1:/home/paladox# sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/maintenance/sql.php /srv/mediawiki/w/extensions/Comments/sql/patches/actor/drop-Comments_Vote_user_id_index.sql
* 20:40 paladox: root@jobrunner1:/home/paladox# sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/maintenance/sql.php /srv/mediawiki/w/extensions/Comments/sql/patches/actor/drop-Comment_Vote_user_id-index.sql
* 20:33 paladox: MariaDB [crummyscratcherswiki]> DROP INDEX /*i*/wiki_user_name ON /*_*/Comments; - dbt1
* 20:33 paladox: MariaDB [crummyscratcherswiki]> ALTER TABLE /*_*/Comments_block DROP COLUMN cb_user_name_blocked; - dbt1
* 20:32 paladox: MariaDB [crummyscratcherswiki]> ALTER TABLE /*_*/Comments_block DROP COLUMN cb_user_name; - dbt1
* 20:32 paladox: MariaDB [crummyscratcherswiki]> ALTER TABLE /*_*/Comments_block DROP COLUMN cb_user_id; - dbt1
* 20:31 paladox: MariaDB [crummyscratcherswiki]> ALTER TABLE /*_*/Comments_block DROP COLUMN cb_user_id_blocked; - dbt1
* 20:30 paladox: MariaDB [crummyscratcherswiki]> DROP INDEX /*i*/cb_user_id ON /*_*/Comments_block; - dbt1
* 20:30 paladox: MariaDB [crummyscratcherswiki]> DROP INDEX /*i*/Comments_Vote_user_id_index ON /*_*/Comments_Vote; - dbt1
* 20:30 paladox: MariaDB [crummyscratcherswiki]> ALTER TABLE /*_*/Comments DROP COLUMN Comment_user_id; - dbt1
* 20:29 paladox: MariaDB [crummyscratcherswiki]> ALTER TABLE /*_*/Comments_Vote DROP COLUMN Comment_Vote_user_id; - dbt1
* 20:24 paladox: MariaDB [crummyscratcherswiki]> DROP INDEX /*i*/Comment_Vote_user_id ON /*_*/Comments_Vote; - dbt1
* 20:14 Southparkfan: disable puppet on mon1 for T5536
* 19:39 paladox: ALTER TABLE /*_*/searchindex MODIFY si_title MEDIUMTEXT NOT NULL; (crappygameswiki) - db6
* 19:02 paladox: recreate searchindex table on crappygameswiki - db6
* 18:58 paladox: sudo -u www-data php rebuildtextindex.php --wiki=crappygameswiki - jobrunner1
* 12:42 Southparkfan: edited test2's nginx configuration to test a fix for [https://serverfault.com/questions/240476/how-to-force-nginx-to-resolve-dns-of-a-dynamic-hostname-everytime-when-doing-p](https://serverfault.com/questions/240476/how-to-force-nginx-to-resolve-dns-of-a-dynamic-hostname-everytime-when-doing-p)

## 2020-05-21 

* 19:15 Southparkfan: same done for phab1
* 19:14 Southparkfan: downgraded nginx on mon1, mail1, ldap1
* 18:58 Southparkfan: reload nginx on mediawiki server to sees if it fixes  [https://serverfault.com/questions/240476/how-to-force-nginx-to-resolve-dns-of-a-dynamic-hostname-everytime-when-doing-p](https://serverfault.com/questions/240476/how-to-force-nginx-to-resolve-dns-of-a-dynamic-hostname-everytime-when-doing-p)
* 18:15 Southparkfan: repooled mw4 and mw7
* 18:12 Southparkfan: repool mw6 and depool mw4/mw7
* 18:06 Southparkfan: repool mw5 and depool mw6
* 18:02 Southparkfan: depool mw5
* 16:25 Southparkfan: disable puppet on test2
* 07:01 Reception123: reception@jobrunner1:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/delete                                                                                        Batch.php --wiki neobulbawiki -r "Requested - T5625" /home/reception/neobulbadel.txt
* 00:57 paladox: update mw_permissions set perm_addgroupstoself = '[]' where perm_dbname = 'shepecowiki'; -dbt1
* 00:56 paladox: update mw_permissions set perm_removegroups = '[]' where perm_dbname = 'shepecowiki'; -dbt1
* 00:56 paladox: update mw_permissions set perm_addgroups  = '[]' where perm_dbname = 'shepecowiki'; - dbt1
* 00:56 paladox: update mw_permissions set perm_removegroupsfromself = '[]' where perm_dbname = 'shepecowiki'; - dbt1
* 00:56 paladox: update mw_permissions set perm_addgroupstoself = '[]' where perm_dbname = 'shepecowiki'; - dbt1

## 2020-05-20 

* 23:12 paladox: rebuild lc on test2
* 23:09 paladox: rebuild lc on mw* and jobrunner1
* 20:59 paladox: run fixStuckGlobalRename.php on jobrunner1
* 19:38 paladox: remove php, nodejs and nginx from misc1
* 19:12 paladox: drop user 'roundcubemail'@'2a00:d880:6:787::3'; - db6
* 19:12 paladox: drop user roundcubemail@185.52.1.76; - db6
* 18:33 Southparkfan: remove traces of sury repo
* 17:32 paladox: upgrade grafana on mon1
* 16:43 paladox: apt-get upgrade - misc1 (php packages)
* 16:17 paladox: drop user icinga@185.52.1.76; - db6
* 16:06 paladox: revoke grants from exporter@81.4.127.174 - db[67]
* 16:06 paladox: drop user exporter@81.4.127.174 - dbt1, db[67]
* 16:04 paladox: revoke grants from exporter@81.4.127.174 - dbt1
* 13:15 paladox: apt-get upgrade on all hosts

## 2020-05-19 

* 19:43 paladox: root@jobrunner1:/srv/mediawiki/w/extensions/CentralAuth/maintenance# sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/deleted.dblist /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/removePII.php --oldname "<private>" "MirahezeGDPR_61a0f5e7ff63bc91e09c752fe3ebc30f"
* 19:20 paladox: GDPR removal
* 19:17 paladox: root@jobrunner1:/srv/mediawiki/w/maintenance# sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/maintenance/runJobs.php
* 16:26 Reception123: added yandex API key to private repo

## 2020-05-18 

* 09:22 Reception123: MariaDB [test2wiki]> DELETE FROM echo_notification WHERE notification_event = 176 and notification_user = 53;

## 2020-05-17 

* 17:35 paladox: MariaDB [mrjaroslavikwiki]> INSERT INTO slot_roles (role_id, role_name) VALUES (1, 'main');
* 17:33 paladox: MariaDB [mrjaroslavikwiki]> INSERT INTO content_models (model_id, model_name) VALUES (4, 'Scribunto');
* 17:33 paladox: MariaDB [mrjaroslavikwiki]> INSERT INTO content_models (model_id, model_name) VALUES (2, 'css');
* 17:33 paladox: MariaDB [mrjaroslavikwiki]> INSERT INTO content_models (model_id, model_name) VALUES (3, 'javascript');
* 17:33 paladox: MariaDB [mrjaroslavikwiki]> INSERT INTO content_models (model_id, model_name) VALUES (5, 'json');
* 17:33 paladox: MariaDB [mrjaroslavikwiki]> INSERT INTO content_models (model_id, model_name) VALUES (1, 'wikitext');
* 01:16 paladox: rebuilding lc on mw*

## 2020-05-16 

* 23:50 paladox: sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/extensions/SocialProfile/UserProfile/maintenance/migrateOldUserProfileUserColumnToActor.php --force
* 23:44 paladox: sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/maintenance/sql.php /srv/mediawiki/w/extensions/SocialProfile/UserProfile/sql/patches/actor/make-up_actor-primary-key.sql
* 23:43 paladox: root@jobrunner1:/srv/mediawiki/w# sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/maintenance/sql.php /srv/mediawiki/w/extensions/SocialProfile/UserProfile/sql/patches/patch-drop-column-up_id.sql

## 2020-05-15 

* 22:45 paladox: rebuild lc on mw*
* 19:15 paladox: root@test2:/srv/mediawiki/w/extensions/MirahezeMagic/maintenance# sudo -u www-data php populateWikibaseSitesTable.php --wiki=hispanowiki
* 00:15 paladox: root@mw4:/srv/mediawiki/w/extensions/ManageWiki/maintenance# sudo -u www-data php toggleExtension.php --wiki=khatikwiki wikibaseclient
* 00:14 paladox: root@mw4:/srv/mediawiki/w/extensions/ManageWiki/maintenance# sudo -u www-data php toggleExtension.php --wiki=khatikwiki wikibaserepository

## 2020-05-14 

* 17:16 Reception123: repool cp8
* 17:15 Reception123: apt-get dist-upgrade and reboot cp8
* 17:13 Reception123: depool cp8
* 17:13 Reception123: repool cp7
* 17:13 Reception123: apt-get dist-upgrade and reboot cp7
* 17:09 Reception123: depool cp7
* 17:09 Reception123: repool cp3
* 17:08 Reception123: apt-get dist-upgrade and reboot cp3
* 17:03 Reception123: depooled cp3
* 13:10 paladox: startup mw7 using proxmox ui
* 13:02 paladox: restart lobot on mon1
* 12:58 Reception123: depool mw7
* 12:57 Reception123: repool mw6
* 12:57 Reception123: apt-get dist-upgrade and reboot mw6
* 12:55 Reception123: depool mw6
* 12:54 Reception123: repool mw5
* 12:54 Reception123: apt-get dist-upgrade and reboot mw5
* 12:51 Reception123: repool mw4
* 12:50 Reception123: apt-get dist-upgrade and reboot on mw4
* 12:45 Reception123: depool mw4
* 12:35 paladox: reboot mail1
* 12:34 paladox: reboot rdb1
* 12:32 paladox: apt-get dist-upgrade - rdb2
* 12:31 paladox: apt-get dist-upgrade - mail1
* 12:30 paladox: reboot gluster2
* 12:29 paladox: apt-get dist-upgrade - gluster2
* 12:29 paladox: reboot gluster1
* 12:26 paladox: apt-get dist-upgrade - gluster1
* 12:25 paladox: reboot misc1
* 12:24 paladox: apt-get dist-upgrade - misc1
* 12:24 paladox: reboot ldap1
* 12:24 paladox: reboot jobrunner1
* 12:23 paladox: reboot ns1
* 12:22 paladox: apt-get dist-upgrade - ldap1
* 12:21 paladox: apt-get dist-upgrade - ns1
* 12:20 paladox: apt-get dist-upgrade - jobrunner1
* 12:19 paladox: reboot test2
* 12:19 paladox: reboot cp6
* 12:18 paladox: reboot ns2
* 12:18 paladox: apt-get dist-upgrade - test2
* 12:15 paladox: apt-get dist-upgrade - cp6 & ns2
* 12:14 paladox: reboot puppet2, services1
* 12:14 paladox: apt-get dist-upgrade - services2
* 12:14 paladox: apt-get dist-upgrade - services1
* 12:13 paladox: apt-get dist-upgrade - puppet2
* 12:12 paladox: reboot phab1 and bacula2
* 12:11 paladox: apt-get dist-upgrade - bacula2
* 12:09 paladox: apt-get dist-upgrade - phab1
* 12:09 paladox: apt-get dist-upgrade - rdb1
* 12:08 paladox: reboot mon1
* 12:08 paladox: reboot rdb1
* 12:03 paladox: apt-get dist-upgrade - mon1
* 11:58 Reception123: added slack hook for jungegeotechnikerwiki
* 11:03 Reception123: ran messagefiles and rebuild LC on mw*/jbr1
* 08:14 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/deleteBatch.php --wiki awesomegameswiki -r "Requested - T5583" /home/reception/cg2.txt (new)

## 2020-05-13 

* 17:17 paladox: root@jobrunner1:/home/paladox# /usr/bin/nice -19 /usr/local/bin/foreachwikiindblist /home/paladox/dbs /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/populateWikibaseSitesTable.php
* 17:06 paladox: MariaDB [mhglobal]> update mw_permissions set perm_removegroups = '[]' where perm_removegroups = 'null'; -dbt1
* 17:05 paladox: MariaDB [mhglobal]> update mw_permissions set perm_addgroups = '[]' where perm_addgroups = 'null'; - dbt1
* 16:21 paladox: rebuild lc on jobrunner1
* 16:08 paladox: rebuilding lc on mw*
* 14:00 paladox: created a guest account in ldap for icinga
* 08:19 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/deleteBatch.php --wiki awesomegameswiki -r "Requested - T5583" /home/reception/cg2.txt
* 08:11 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/deleteBatch.php --wiki awesomegameswiki -r "Requested - T5583" /home/reception/cg.txt

## 2020-05-11 

* 20:57 paladox: rebuild lc on mw*, jobrunner1 and test2
* 18:14 paladox: increased mon1 disk by 10gb (40gb in total)
* 08:20 Reception123: restarting icingabot
* 00:11 paladox: rebuild lc on mw* and jobrunner1

## 2020-05-10 

* 18:51 Reception123: deleted and dropped [https://phabricator.miraheze.org/P312](https://phabricator.miraheze.org/P312)
* 18:41 Reception123: reception@jobrunner1:~$ sudo -u www-data php /srv/mediawiki/w/extensions/CreateWiki/maintenance/deleteWikis.php --wiki=loginwiki --delete Reception123
* 18:20 Reception123: created ldap account for myself
* 09:51 Reception123: deleted and dropped mrjaroslavikwiki, then recreated

## 2020-05-09 

* 12:47 Reception123: $cw = new CreateWikiJson( 'pruebawiki' ); $cw->resetWiki();
* 11:43 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildLocalisationCache.php --wiki loginwiki  on mw*/jbr1
* 07:22 Reception123: renamed artladderwiki to meshwiki.

## 2020-05-08 

* 23:49 paladox: upgraded puppet-agent on mon1
* 21:20 paladox: mon1>grafana-cli plugins install grafana-image-renderer

## 2020-05-07 

* 17:41 Zppix: rebuildLC on jobrunner1
* 12:02 paladox: install security updates for firefox-esr iceweasel on mw4
* 12:02 paladox: install security updates for firefox-esr iceweasel on mw5
* 12:01 paladox: install security updates for firefox-esr iceweasel on mw6
* 09:14 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildLocalisationCache.php --wiki loginwiki on mw*/jbr1
* 08:19 paladox: install security updates for firefox-esr iceweasel on mw7

## 2020-05-06 

* 23:38 paladox: apt-get dist-upgrade - cloud[12] (upgrading proxmox and puppet-agent)
* 22:34 paladox: depool mw[67], set vcpu to 4 and repool
* 22:33 paladox: repool mw5
* 22:30 paladox: set mw5 vcpu to 4
* 22:30 paladox: depool mw5
* 22:30 paladox: repool mw4
* 22:28 paladox: set mw4 vcpu to 4
* 22:28 paladox: depool mw4
* 22:21 paladox: restarted prometheus on mon1
* 22:14 paladox: restart nginx-prometheus-exporter on mw4
* 21:58 paladox: rebuild lc on mw* and jobrunner1
* 16:13 paladox: apt-get --purge remove apache2* - ns1
* 14:34 paladox: installed libgraphicsmagick++-q16-12 libgraphicsmagick-q16-3 security updates on mw6
* 12:32 John: security updates for libgraphicsmagick++-q16-12 and libgraphicsmagick-q16-3
* 10:58 Reception123: reception@jobrunner1:/srv/mediawiki/w/maintenance$ sudo -u www-data php cleanupT                                                                             itles.php --wiki testwiki
* 05:59 Reception123: reception@jobrunner1:~$ sudo -u www-data php /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/generateMirahezeSitemap.php --wiki closinglogosgroupwiki

## 2020-05-05 

* 20:54 paladox: $cw = new CreateWikiJson( 'infinigwiki' ); $cw->resetWiki();
* 20:51 paladox: MariaDB [mhglobal]> update mw_permissions set perm_addgroups = '[]' where perm_group = 'member' and perm_dbname = 'infinigwiki';
* 19:35 Reception123: disabled a user on Phabricator
* 19:31 Reception123: MariaDB [mhglobal]> UPDATE cw_wikis SET wiki_inactive_timestamp = null WHERE wiki_inactive = 0;
* 19:29 Southparkfan: rebuilding recent changes for atrociousyoutuberswiki
* 18:12 Reception123: > $cWJ = new CreateWikiJson( "dungeonsanddaddieswiki" ); $cWJ->resetWiki();
* 17:59 John: reset email on Maestro venerabile
* 17:46 paladox: MariaDB [atrociousyoutuberswiki]> truncate objectcache;
* 16:13 paladox: delete redis atrociousyoutuberswiki key
* 13:33 paladox: MariaDB [atrociousyoutuberswiki]> update recentchanges set rc_ip = *where rc_ip = '0.0.0.0';
* 12:57 paladox: update flow_revision set rev_user_ip = NULL where rev_user_ip = '0.0.0.0';
* 12:57 paladox: update flow_revision set rev_edit_user_ip = NULL where rev_edit_user_ip = '0.0.0.0';
* 12:57 paladox: update flow_revision set rev_mod_user_ip = NULL where rev_mod_user_ip = '0.0.0.0';
* 12:57 paladox: update flow_tree_revision set tree_orig_user_ip = NULL where tree_orig_user_ip = '0.0.0.0';
* 07:26 Reception123: stopped and started ircecho (icinga)

## 2020-05-04 

* 20:54 paladox: blocked heroku-miraheze from github, confirmed LTA
* 19:44 Reception123: delete from [localnames/localuser] where [lu_wiki/ ln_wiki] = johnflewiswiki bloxcitywiki brgameswiki columbiasjpwiki xenimuswiki
* 19:25 paladox: delete from localuser where lu_wiki = 'asylothekberlinwiki'; - dbt1
* 19:25 paladox: delete from localnames where ln_wiki = 'asylothekberlinwiki'; - dbt1
* 19:14 paladox: delete from localnames where ln_wiki = 'altenpflegewiki'; - dbt1
* 19:08 paladox: MariaDB [mhglobal]> delete from localuser where lu_wiki = 'altenpflegewiki'; - dbt1
* 14:55 paladox: root@jobrunner1:/srv/mediawiki/w/extensions/SocialProfile# sudo -u www-data php UserBoard/maintenance/migrateOldUserBoardUserColumnsToActor.php --wiki=atrociousyoutuberswiki --force
* 01:04 paladox: set table_definition_cache and table_open_cache to 10000 on db6/db7
* 00:38 paladox: re-started backups on bacula2
* 00:38 paladox: upgrade puppet-agent - bacula2

## 2020-05-03 

* 21:31 John: DELETE FROM localuser WHERE lu_wiki = 'navaversewiki';
* 17:46 paladox: upgrade phabricator on phab1
* 17:35 paladox: sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/maintenance/runJobs.php - jobrunner1
* 17:34 Reception123: reception@jobrunner1:/srv/mediawiki/w/maintenance$ sudo -u www-data php checkBadRedirects.php --wiki testwiki
* 17:25 Reception123: dropped rainfallwiki telegrambotswiki templeofdivinitywiki tenlosssyndicatewiki tenniselbowwiki tensorflowglossarywiki terrafractumwiki terredelsolewiki tescommunitywiki testdelete7wiki unionwiki vragwiki xenimuswiki
* 17:22 Reception123: dropped natturkowiki navaversewiki navmedwiki nayan28589wiki neoottomanwiki omnipediawiki pispediawiki pitchwiki pixterwiki placesrobloxwiki pmavwiki podcastswiki poewikiwiki pokemondustwiki pokeonewiki
* 17:18 Reception123: dropped mwpermtestwiki myao93wiki myclassprojectswiki mydevexperiencewiki mymoneywiki mynintendowiki mysummerholydayswiki n2gowiki nafetswiki nagygenitalorszagwiki namudatawiki nanotrixwiki
* 17:13 Reception123: dropped diagnostikwiki dobotswiki feralarchiveswiki hellointernetwiki iwwiki kaydadegerwiki kidalwiki lothuialethwiki metaautonomiawiki metroplexfederationwiki musicpediawiki musicwikiwiki musicworldgamewiki
* 17:06 Reception123: dropped ashesworldwiki astropediawiki parapediawiki asylothekberlinwiki bloxcitywiki bonobowiki brgameswiki columbiasjpwiki deletenowdbwiki
* 15:31 Reception123: dropped altenpflegewiki amcwiki animefurryfeetwiki johnflewiswiki anothertimeline2120wiki antuswiki aqferwiki
* 15:25 Reception123: dropped testdatabasewiki testdelete3wiki testdelete7wiki
* 14:32 Reception123: renamed testkan2020wiki to aeroddwiki
* 12:31 Reception123: rebuild LC on mw*
* 12:31 paladox: dropping securepoll_* table from metawiki
* 12:30 Reception123: reception@jobrunner1:/srv/mediawiki/w/extensions/Flow/maintenance$ sudo -u www-data php FlowCreateTemplates.php --wiki radioscanningtwwiki
* 12:12 paladox: MariaDB [mhglobal]> update mw_settings set s_settings = '[]' where s_dbname = 'wikitheoswiki';
* 12:10 paladox: MariaDB [mhglobal]> INSERT INTO mw_settings (s_dbname, s_settings, s_extensions) VALUES ('wikitheoswiki', '{}', '[]');

## 2020-05-02 

* 22:32 paladox: sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/extensions/Comments/maintenance/migrateOldCommentsVoteUserColumnsToActor.php --force - test2
* 22:30 paladox: sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/extensions/Comments/maintenance/migrateOldCommentsUserColumnsToActor.php - test2
* 22:30 paladox: sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/extensions/Comments/maintenance/migrateOldCommentsBlockUserColumnsToActor.php - test2
* 22:24 paladox: root@test2:/srv/mediawiki/w/extensions/VoteNY# sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/extensions/VoteNY/maintenance/migrateOldVoteUserColumnsToActor.php
* 19:31 paladox: root@test2:/srv/mediawiki/w/extensions/MirahezeMagic/maintenance# sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/updateSP.php
* 19:23 paladox: root@test2:/srv/mediawiki/w/extensions/MirahezeMagic/maintenance# /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/updateSP.php
* 18:23 paladox: root@test2:/srv/mediawiki/w/extensions/MirahezeMagic/maintenance# /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/updateSP.php
* 14:03 John: UPDATE mw_permissions SET perm_autopromote = null WHERE perm_autopromote LIKE '{"add":%';

## 2020-05-01 

* 23:00 John: running LC
* 20:42 paladox: /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/updateSP.php
* 19:57 paladox: /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/updateComments.php
* 18:41 paladox: /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/updateSP.php
* 18:33 paladox: /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/updateSP55.php
* 17:52 paladox: /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/updateSP.php
* 17:22 paladox: root@test2:/srv/mediawiki/w/extensions/SocialProfile/UserStats/maintenance# sudo -u www-data php migrateOldUserStatsUserColumnsToActor.php --wiki=atrociousyoutuberswiki
* 16:40 paladox: disable a user in phabricator
* 15:33 Reception123: restarted certbot
* 11:04 paladox: upgrade puppet-agent puppetdb puppetdb-termini puppetserver salt-common salt-master salt-minion - puppet2
* 10:50 paladox: apt-get dist-upgrade - cp7
* 08:41 John: UPDATE mw_settings SET s_dbname = 'feralworthwikiwiki' WHERE s_dbname = 'feralarchiveswiki';
* 01:14 paladox: /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/updateComments.php
* 01:09 paladox: /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/updateSP.php - test2

## 2020-04-30 

* 17:30 paladox: /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/extensions/SocialProfile/UserStats/maintenance/migrateOldUserStatsUserColumnsToActor.php - test2
* 15:32 paladox: MariaDB [crappygameswiki]> UPDATE Comments_Vote SET Comment_Vote_actor=(SELECT actor_id FROM actor WHERE actor_name=Comment_Vote_Username);
* 14:03 paladox: usermod -a -G ssl-cert www-data - test2
* 02:15 paladox: MariaDB [toxicfandomsandhatedomswiki]> delete from Comments where Comment_Username =* ;
* 01:35 paladox: test2.php contains `ALTER TABLE /*$wgDBprefix*/Comments MODIFY COLUMN Comment_Date datetime NOT NULL default '1970-01-01 00:00:01';`
* 01:35 paladox: test.php contains `ALTER TABLE /*$wgDBprefix*/Comments_Vote MODIFY COLUMN Comment_Vote_Date datetime NOT NULL default '1970-01-01 00:00:01';`
* 01:23 paladox: /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/updateComments4.php
* 01:17 paladox: /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/updateComments3.php
* 01:08 paladox: /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/updateComments.php
* 00:53 paladox: /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/updatePollNY2.php
* 00:52 paladox: /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/updateQuizGame2.php
* 00:47 paladox: rebuild lc on mw* and jobrunner1
* 00:22 paladox: /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/updateAjaxPoll.php
* 00:06 paladox: /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/updateQuizGame.php

## 2020-04-29 

* 23:44 paladox: test.sql is `ALTER TABLE /*$wgDBprefix*/Vote MODIFY COLUMN vote_date datetime NOT NULL default '1970-01-01 00:00:01';`
* 23:39 paladox: /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/updateVoteNY2.php
* 23:33 paladox: /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/updatePollNY.php
* 23:23 paladox: /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/updateVoteNY.php
* 23:08 paladox: /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/updateSP.php - jobrunner1
* 20:31 paladox: MariaDB [test2wiki]> truncate user_profile; - from earlier on db6
* 15:23 paladox: upgrade phabricator on phab1
* 15:22 paladox: delete sourav4 user in phabricator per request
* 14:32 Reception123: added retailpedia discord webhook
* 14:06 paladox: root@cloud2:/home/paladox# swapoff -a
* 14:05 paladox: root@cloud1:/home/paladox# swapoff -a

## 2020-04-28 

* 20:48 paladox: reinstall php on mon1
* 20:47 Southparkfan: apt-get remove php-ldap on mon1
* 19:44 paladox: root@gluster1:/home/paladox# gluster volume set mvol rebal-throttle lazy
* 17:11 paladox: INSERT INTO renameuser_status (ru_oldname, ru_newname, ru_wiki, ru_status) VALUES ('TaakoManTheGameMaster', 'GDPRAccount', 'crappyreceptionwikiswiki', 'failed');
* 17:11 paladox: INSERT INTO renameuser_status (ru_oldname, ru_newname, ru_wiki, ru_status) VALUES ('TaakoManTheGameMaster', 'GDPRAccount', 'crappygameswiki', 'failed');
* 17:11 paladox: INSERT INTO renameuser_status (ru_oldname, ru_newname, ru_wiki, ru_status) VALUES ('TaakoManTheGameMaster', 'GDPRAccount', 'awfulmovieswiki', 'failed');
* 17:03 paladox: update actor set actor_name = 'GDPRAccount2' where actor_name = 'GDPRAccount';
* 17:03 paladox: update user set user_name = 'GDPRAccount2' where user_name = 'GDPRAccount';
* 16:58 paladox: INSERT INTO renameuser_status (ru_oldname, ru_newname, ru_wiki, ru_status) VALUES ('TaakoManTheGameMaster', 'GDPRAccount', 'atrociousyoutuberswiki', 'failed'); - dbt1
* 16:47 paladox: MariaDB [mhglobal]> delete from renameuser_status where ru_newname = 'GDPRAccount'; - dbt1
* 16:21 Reception123: fixStuckGlobalRename.php for GDPR
* 15:52 Reception123: reception@jobrunner1:/srv/mediawiki/w/extensions/ManageWiki/maintenance$ sudo -u www-data php populateGroupPermissionsWithDefaults.php --wiki familiekbrwiki --overwrite
* 15:03 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/mergeMessageFileList.php --output /srv/mediawiki/config/ExtensionMessageFiles.php --wiki loginwiki and rebuild LC on mw*/jbr1
* 13:32 John: ALTER IGNORE TABLE mw_permissions ADD UNIQUE uniqueperm(perm_dbname, perm_group);
* 13:30 John: ALTER IGNORE TABLE mw_namespaces ADD UNIQUE uniquens(ns_dbname, ns_namespace_id);
* 08:50 paladox: root@gluster1:/home/paladox# gluster volume set mvol rebal-throttle normal
* 06:23 Reception123: renamed feralarchiveswiki to feralworthwikiwiki.

## 2020-04-27 

* 23:59 John: rebuildLC after running mergeMessageFileList to bring in calendar extension added earlier
* 21:59 paladox: root@gluster1:/home/paladox# gluster volume set mvol rebal-throttle lazy
* 20:06 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildLocalisationCache.php --wiki loginwiki on mw*/jbr1
* 19:02 paladox: root@gluster1:/home/paladox# gluster volume set mvol rebal-throttle normal
* 18:55 paladox: MariaDB [(none)]> set global table_definition_cache = 5000; - db6 & db7
* 18:54 paladox: MariaDB [(none)]> set global table_open_cache = 5000; - db6 & db7
* 18:52 paladox: root@gluster1:/home/paladox# gluster volume set mvol rebal-throttle lazy
* 18:42 paladox: root@gluster1:/home/paladox# gluster volume set mvol rebal-throttle normal
* 18:15 Reception123: restarted MirahezeRC
* 16:32 paladox: root@gluster1:/home/paladox# gluster volume set mvol rebal-throttle lazy
* 16:30 paladox: root@gluster1:/home/paladox# gluster volume set mvol rebal-throttle aggressive
* 16:27 paladox: upgrade nginx & grafana on mon1
* 16:23 paladox: restart ircrcbot on mon1
* 16:00 paladox: ban req.http.Host == elmetaverse.miraheze.org  - cp6
* 15:58 paladox: ban req.http.Host == elmetaverse.miraheze.org && req.url ~ "^/w/load.php" - cp6
* 15:14 paladox: root@gluster1:/home/paladox# gluster volume set mvol rebal-throttle normal
* 15:03 paladox: root@gluster1:/home/paladox# gluster volume set mvol rebal-throttle aggressive
* 14:54 paladox: root@gluster1:/home/paladox# gluster volume set mvol rebal-throttle lazy
* 14:52 paladox: root@gluster1:/home/paladox# gluster volume set mvol rebal-throttle aggressive
* 14:10 paladox: rebalancing gluster cluster

## 2020-04-26 

* 19:35 paladox: reboot gluster1
* 19:27 paladox: reboot mw[67] (and depool/repool)
* 19:25 paladox: lower gluster1 ram to 5gb - 8gb is too much
* 18:40 paladox: redis-cli -a xxx --scan --pattern *dreamversewiki* | xargs redis-cli -a xxx del - rdb2
* 18:34 paladox: ban req.http.Host == static.miraheze.org && req.url ~ "^/dreamversewiki" - cp8
* 12:59 Reception123: reception@jobrunner1:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/updateSpecialPages.php  --wiki testwiki
* 12:47 Reception123: reception@jobrunner1:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildall.php --wiki testwiki

## 2020-04-25 

* 17:57 paladox: rebuild lc on test2
* 17:53 paladox: rebuild lc on mw* and jobrunner1
* 16:51 paladox: rebuild lc on mw* and jobrunner1

## 2020-04-24 

* 13:15 paladox: rebuild lc on test2
* 09:15 Reception123: reception@jobrunner1:/srv/mediawiki/w/maintenance$ sudo -u www-data php importDump.php --wiki tvwikiwiki /home/reception/Wikipedia-20200424091247.xml

## 2020-04-23 

* 19:38 paladox: rebuilding lc on test2
* 19:35 paladox: rebuilding lc on mw* & jobrunner1
* 13:53 paladox: restart nginx on mw4
* 13:53 paladox: restart php-fpm on mw4
* 00:05 paladox: run /home/paladox/resetWikiCaches.php on jobrunner1
* 00:01 paladox: delete from mw_permissions where perm_dbname = 'ryfusewiki'; - dbt1

## 2020-04-22 

* 23:58 paladox: delete from mw_permissions where perm_dbname = 'i'; - dbt1
* 23:58 paladox: delete from mw_permissions where perm_dbname = 'rontend,cite,citethispage,globaluserpage,mobilefrontend'; - dbt1
* 23:57 paladox: delete from mw_permissions where perm_dbname = 'obilefrontend'; - dbt1
* 23:51 paladox: run lowercaseGroups.php on jobrunner1
* 15:59 paladox: restart ircrcbot
* 15:19 paladox: restarted ircrcbot
* 13:27 paladox: restart ircrcbot restart
* 05:59 Reception123: reception@jobrunner1:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/deleteBatch.php --wiki crappygameswiki -r "Requested - T5461" /home/reception/cgw.txt

## 2020-04-21 

* 21:06 paladox: stopping mysql on dbt1
* 17:31 paladox: restart ircecho
* 14:59 paladox: reinstall db7
* 08:43 paladox: fallover db7 to db6
* 08:23 Reception123: restarted cp7 (same time as the others)
* 08:21 Reception123: restarted db7/mw*

## 2020-04-20 

* 14:26 Reception123: reception@jobrunner1:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/deleteBatch.php --wiki crappygameswiki -r "Requested - T5441" /home/reception/cpgtxt.txt
* 14:19 paladox: restart ircrcbot
* 13:39 Reception123: reception@jobrunner1:/srv/mediawiki/w/maintenance$ sudo -u www-data php rebuildall.php --wiki crappygameswiki
* 11:00 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildLocalisationCache.php --wiki loginwiki on mw*/test2/jbr

## 2020-04-19 

* 20:08 Reception123: restarted RC bot
* 16:56 paladox: add openldap to ssl-cert group on test2
* 05:21 Reception123: reception@jobrunner1:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki kiddancerswiki /home/reception/kiddancers_pages_full.xml
* 00:18 Zppix: un-closing feralarchiveswiki as it was inactive due to technical issues
* 00:13 paladox: remove wgDefaultSkin from feralarchiveswiki

## 2020-04-18 

* 22:17 Zppix: run compressOld.php on libertygamewiki (jobrunner1)
* 16:52 paladox: delete testrenametestwiki
* 16:07 Reception123: renamed kidalwiki to shatteredskieswiki
* 15:32 paladox: MariaDB [mhglobal]> update mw_settings set s_dbname = 'brokenthroneswiki' where s_dbname = 'ashesworldwiki'; - dbt1
* 15:15 Reception123: renamed ashesworldwiki to brokenthroneswiki.(db+cw)
* 09:29 Reception123: rebuildlocalisationcache.php on mw*/jbr

## 2020-04-17 

* 13:30 Reception123: reception@jobrunner1:/srv/mediawiki/w/extensions/CentralAuth/maintenance$ sudo -u www-data php migrateAccount.php --username BroswerStackAccount --wiki loginwiki --auto
* 01:21 paladox: add Topic ns to all wikis that have Flow enabled using hackScript.php
* 01:20 paladox: root@jobrunner1:/home/paladox# sudo -u www-data php hackScript.php --wiki=loginwiki

## 2020-04-16 

* 20:07 Zppix: Close recentiawiki for ToU violations
* 16:44 paladox: enable "Limit to existing users" on mw-config last 24h
* 15:16 paladox: upgrade puppetserver on puppet2
* 14:42 Reception123: added discord hook for cookieclickerwiki
* 13:22 Reception123: $cw = new CreateWikiJson( 'villagecollaborativewiki' ); $cw->resetDatabaseList();
* 05:52 Reception123: reception@jobrunner1:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki avalonwiki /home/reception/Maia+Song+Contest-20200412160644.xml
* 03:45 paladox: upgrade gluster on mw* and jobrunner1 and test2
* 03:44 paladox: apt-get upgrade - gluster1 (git, nodejs & gluster)
* 03:40 paladox: apt-get upgrade - jobrunner1 (git, nodejs)

## 2020-04-15 

* 21:29 paladox: > MatomoAnalyticsHooks::wikiCreation( 'blueoathwiki' ); - jobrunner1
* 19:47 paladox: restarted nginx on services2
* 19:09 paladox: hack /srv/parsoid/node_modules/mediawiki-title/lib/index.js (function canonicalName to add a undefined check)
* 19:02 paladox: /usr/bin/nice -19 /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /home/paladox/resetWikiCaches.php - jobrunner1
* 18:44 paladox: root@mw4:/srv/mediawiki/w/cache# rm awfulmovieswiki.json
* 15:51 paladox: FLUSHDB  - jobrunner1 (redis)
* 15:50 paladox: FLUSHALL ASYNC - jobrunner1 (redis)
* 12:36 Reception123: reception@jobrunner1:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki vivoleko01wiki /home/reception/isuzugemini01_pages_full.xml
* 12:16 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildLocalisationCache.php --wiki loginwiki on mw* and jobrunner1

## 2020-04-14 

* 22:00 paladox: root@jobrunner1:/home/paladox# sudo -u www-data /usr/bin/nice -19 /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/maintenance/runJobs.php
* 20:19 paladox: root@jobrunner1:/home/paladox# /usr/bin/nice -19 /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/maintenance/runJobs.php
* 17:47 paladox: disabling issues on all of our github repos
* 17:35 Reception123: sudo -u www-data php fixStuckGlobalRename.php --wiki=earthvisionwiki --logwiki=metawiki "Kathying" "LTSC1980"
* 12:59 John: insert default mw_settings values for blueoathwiki
* 02:44 Zppix: $cWJ = new CreateWikiJson( solarawiki ); $cWJ->resetWiki();

## 2020-04-13 

* 19:43 John: changed mw_namespaces entries from 'Array' to '[]'
* 18:38 paladox: MariaDB [mhglobal]> update cw_wikis set wiki_closed_timestamp = NULL where wiki_closed = 0; - dbt1
* 18:16 paladox: stopped script
* 18:06 paladox: MariaDB [mhglobal]> UPDATE cw_wikis SET wiki_closed = 0 AND wiki_closed_timestamp = NULL WHERE wiki_closed_timestamp > 20200413000000; - dbt1
* 17:27 paladox: MariaDB [mhglobal]> update cw_wikis set wiki_closed = 0 where wiki_closed = 1 and wiki_dbname = 'yoavfreundwiki'; - dbt1
* 17:17 John: ->resetWiki() for caching reset on all non-English wikis
* 16:44 paladox: unmark yunawiki as closed
* 13:55 John: added mw_namespaces entries for Wikibase to nbdbwiki
* 03:48 paladox: rm -rf /srv/mediawiki/w/cache/managewiki on mw*
* 03:48 paladox: root@mw4:/var/log# rm -rf /srv/mediawiki/w/cache/managewiki
* 01:24 paladox: root@jobrunner1:/home/paladox# /usr/bin/nice -19 /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/maintenance/runJobs.php
* 01:14 paladox: cleaning up redis on jobrunner1 by deleting some wikis from its redis

## 2020-04-12 

* 23:43 paladox: runJobs on loginwiki ; restart jobrunner and restart jobchron on jobrunner1
* 19:54 paladox: upgraded phabricator on phab1
* 19:21 paladox: /usr/bin/nice -19 /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/removeSettings.php --wgsetting=wgServer
* 16:23 paladox: root@mw5:/srv/mediawiki/w/maintenance# sudo -u www-data php invalidateUserSessions.php --wiki=testwiki --user=Voidwalker
* 14:57 Reception123: MariaDB [metawiki]> UPDATE cw_requests SET cw_status = "approved" WHERE cw_id = "11467";
* 14:57 Reception123: MariaDB [metawiki]> UPDATE cw_requests SET cw_status = "approved" WHERE cw_id = "11466";
* 14:33 John: ban req.url ~ "^/w/load.php" on all cp*
* 14:00 paladox: restarted redis on rdb2
* 05:56 Reception123: reception@mw4:~$ sudo -u www-data php /srv/mediawiki/w/extensions/CentralAuth/maintenance/createLocalAccount.php --wiki=paramountsonicwiki Imjustthere
* 05:56 Reception123: reception@mw4:~$ sudo -u www-data php /srv/mediawiki/w/extensions/CentralAuth/maintenance/createLocalAccount.php --wiki=blueoathwiki CptBrown
* 00:11 paladox: rebuilding lc on mw*
* 00:07 paladox: repool mw4

## 2020-04-11 

* 22:50 John: repool mw4 temp
* 22:26 paladox: MariaDB [phabricator_user]> update user_email set address = *where address = 'John@miraheze.org';
* 22:01 John: depool mw4
* 20:16 paladox: root@test2:/srv/mediawiki/w/cache# rm metawiki.json
* 18:40 paladox: decrease puppet2 core by 1 (so 3 cores and 3 vcpu)
* 18:20 paladox: sudo -u www-data php ext*/ManageWiki/maint*/toggleExtension.php --wiki testwiki --disable regexfunctions
* 17:12 Zppix: rebuildlc on jobrunner1
* 16:59 Reception123: added mediawiki::wiki_discord_hooks_url: [] to private hiera
* 13:58 Reception123: rebuildLocalisationCache.php on mw*
* 10:39 Reception123: rebuildLocalisationCache.php on mw*

## 2020-04-10 

* 18:26 paladox: MariaDB [(none)]> SET GLOBAL max_heap_table_size = 1024 * 1024 * 64; - db6
* 18:26 paladox: MariaDB [(none)]> SET GLOBAL tmp_table_size = 1024 * 1024 * 64; - db6
* 18:23 paladox: MariaDB [(none)]> SET GLOBAL max_heap_table_size = 1024 * 1024 * 64; - dbt1
* 18:23 paladox: MariaDB [(none)]> SET GLOBAL tmp_table_size = 1024 * 1024 * 64; - dbt1
* 18:23 Southparkfan: start replication on db6
* 18:23 paladox: MariaDB [(none)]> SET GLOBAL max_heap_table_size = 1024 * 1024 * 64; - db7
* 18:22 paladox: MariaDB [(none)]> SET GLOBAL tmp_table_size = 1024 * 1024 * 64; - db7
* 17:58 Southparkfan: stop db6 mysql
* 16:26 paladox: root@db7:~# mariabackup --backup --slave-info --safe-slave-backup --stream=xbstream | ssh -i /home/dbcopy/.ssh/id_ed25519 dbcopy@db6.miraheze.org "mbstream -x -C /home/dbcopy/backup-db6-10april/"
* 16:25 paladox: root@db6:/srv# rm -rf mariadb
* 16:12 paladox: kill -9 1295 - db6
* 16:11 paladox: stopping mysql on db6
* 13:03 Southparkfan: reboot db6
* 12:51 Southparkfan: stop mysql on db6 to move backup folder
* 00:52 Southparkfan: mariabackup --backup --slave-info --safe-slave-backup --stream=xbstream | ssh -i /home/dbcopy/.ssh/id_ed25519 dbcopy@db6.miraheze.org "mbstream -x -C /home/dbcopy/backup-db6-10april/"
* 00:52 Southparkfan: running mariabackup in screen on db7, for db6 replication, see command below (or above, if you're reading SAL!)
* 00:31 Southparkfan: install mariadb-backup on db6
* 00:29 Southparkfan: install mariadb-backup on db7
* 00:24 paladox: increased db6 ram to 16g

## 2020-04-09 

* 22:09 Zppix: updating stopforumspam blacklist
* 16:09 Reception123: reception@jobrunner1:/srv/mediawiki/w/extensions/Cargo/maintenance$ sudo -u www-data php cargoRecreateData.php --wiki thenationstatewiki --table Political_Parties
* 14:31 paladox: rebuilt lc on mw*

## 2020-04-08 

* 17:46 Reception123: manually delete Wile_E._Coyote from animatedfeetwiki

## 2020-04-07 

* 20:32 paladox: apt-get upgrade - bacula2
* 20:27 paladox: regenerating backups on bacula2
* 08:30 Reception123: enable puppet everywhere
* 08:28 Reception123: repool mw4
* 08:27 Reception123: depool mw4
* 08:08 Reception123: disabled puppet on mw5-7 for testing revert on mw4
* 04:43 paladox: Renaming solarawiki to spcodexwiki
* 04:30 paladox: update page set page_namespace = 0 where page_namespace = 4;
* 03:12 paladox: root@jobrunner1:/var/log/mediawiki/debuglogs# redis-cli -a xxx --scan --pattern *zwaaiwiki* | xargs redis-cli -a xxx unlink
* 03:11 paladox: root@jobrunner1:/var/log/mediawiki/debuglogs# redis-cli -a xxx --scan --pattern *warapediawiki* | xargs redis-cli -a xxx unlink
* 03:11 paladox: root@jobrunner1:/var/log/mediawiki/debuglogs# redis-cli -a xxx --scan --pattern *soratakowiki* | xargs redis-cli -a xxx unlink
* 03:10 paladox: root@jobrunner1:/var/log/mediawiki/debuglogs# redis-cli -a xxx --scan --pattern *schupiewikiwiki* | xargs redis-cli -a xxx unlink
* 03:08 paladox: root@jobrunner1:/var/log/mediawiki/debuglogs# redis-cli -a xxx --scan --pattern *ewscwiki* | xargs redis-cli -a xxx unlink
* 02:42 paladox: chown -R www-data:www-data /srv/mediawiki/w/.git -test2
* 02:41 paladox: sudo -u www-data git reset --hard origin/REL1_34 - test2
* 02:40 paladox: root@test2:/srv/mediawiki/config# sudo -u www-data git reset --hard origin/master ; sudo -u www-data git pull
* 02:36 paladox: repool mw4
* 02:35 paladox: depool mw4
* 02:35 paladox: root@mw4:/srv/mediawiki/config# sudo -u www-data git pull
* 02:35 paladox: root@mw4:/srv/mediawiki/config# sudo -u www-data git reset --hard origin/master
* 02:33 paladox: repool mw7
* 02:32 paladox: depool mw7
* 02:32 paladox: repool mw6
* 02:31 paladox: depool mw6
* 02:31 paladox: repool mw5
* 02:29 paladox: depool mw5
* 02:07 paladox: root@mw4:/srv/mediawiki/w/cache# rm *wiki.json
* 02:05 paladox: root@mw4:/srv/mediawiki/w/cache# rm *wiki.json
* 01:46 paladox: rm * (in /srv/mediawiki/cache) on mw4
* 01:22 paladox: root@mw4:/srv/mediawiki/w/extensions/MirahezeMagic/maintenance# /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/spScript.php

## 2020-04-06 

* 22:51 John: repool mw4 to get real load conditions
* 22:31 John: depool mw4 for isolated deployment
* 19:32 Reception123: reception@jobrunner1:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki mundanapediawiki /home/reception/Mundanapedia-20160208152735.xml
* 17:14 paladox: apt-get upgrade - ns1
* 16:57 paladox: rebooted cp3
* 16:39 paladox: upgrade cp3 to buster
* 16:05 paladox: MariaDB [mhglobal]> UPDATE cw_wikis SET wiki_settings = REPLACE(wiki_settings, '"wgServer":"yukesh.com.np"', null ) WHERE wiki_dbname = 'hamropediawiki';
* 16:04 paladox: MariaDB [mhglobal]> UPDATE cw_wikis SET wiki_settings = REPLACE(wiki_settings, '"wgServer":"wikiverte.pl"', null ) WHERE wiki_dbname = 'wikivertewiki';

## 2020-04-05 

* 22:49 paladox: increase ram on rdb[12] to 4g
* 22:46 paladox: reboot mw5
* 22:44 paladox: reboot mw4
* 22:22 paladox: increase jobrunner1 core by 1
* 22:22 paladox: increase jobrunner1 core by `
* 18:35 paladox: increase jobrunner1 ram to 3gb
* 18:34 paladox: increase puppet2 to 4 cores
* 13:06 Reception123: deleted and dropped [https://phabricator.miraheze.org/P290](https://phabricator.miraheze.org/P290) (DP)
* 12:00 Reception123: reception@jobrunner1:~$ sudo -u www-data php /srv/mediawiki/w/extensions/CreateWiki/maintenance/deleteWikis.php --wiki loginwiki --delete Reception123
* 08:44 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki aeschyluswiki /home/reception/Wikipedia-20200403182927.xml
* 08:44 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki aeschyluswiki /home/reception/Wikipedia-20200402160456.xml
* 08:41 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki aeschyluswiki /home/reception/Wikipedia-20200402213524.xml

## 2020-04-04 

* 17:25 paladox: MariaDB [hispano76wiki]> truncate cargo_pages;
* 17:24 paladox: MariaDB [hispano76wiki]> truncate cargo_tables;
* 17:22 paladox: drop cargo__* from hispano76wiki
* 15:25 paladox: root@mw4:/home/paladox# sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=templatewiki --report=1 Wikipedia-20200404152245.xml
* 13:47 paladox: root@mw4:/home/paladox# sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=templatewiki --report=1 Wikipedia-20200404133925.xml

## 2020-04-03 

* 21:13 paladox: root@puppet2:/home/puppet-users/ssl-keys# chmod -R 0770 /etc/puppetlabs/puppet/ssl-keys
* 21:13 paladox: root@puppet2:/home/puppet-users/ssl-keys# chown -R puppet:puppet-users /etc/puppetlabs/puppet/ssl-keys
* 21:10 paladox: root@puppet2:/home/puppet-users/ssl-keys# chown -R puppet:puppet-users .git
* 21:09 paladox: root@puppet2:/home/puppet-users# chmod -R 0770 ssl-keys
* 21:03 paladox: root@puppet2:/home/puppet-users# chmod 0770 ssl-keys
* 21:03 paladox: root@puppet2:/home/puppet-users# chown puppet:puppet-users ssl-keys
* 21:01 paladox: root@puppet2:/home/puppet-users# chown 0770 ssl-keys
* 19:58 paladox: depool mw[67], reboot and repool
* 19:58 paladox: set mw[67] cores to 5 (5 vcpu)
* 19:52 paladox: depool mw[45], reboot and repool
* 19:51 paladox: depool mw4
* 19:49 paladox: change puppet2 to 3 cores, mw[45] to 5 cores (5 vcpu)
* 18:04 Reception123: redacted PII for T5376
* 10:17 Reception123: reception@jobrunner1:~/images$ sudo -u www-data php /srv/mediawiki/w/maintenance/importImages.php --wiki=housingwikiwiki --search-recursively --skip-dupes /home/reception/images

## 2020-04-02 

* 23:12 paladox: increase cp7 disk by 10g
* 22:44 paladox: increasing cp6 disk by 10g
* 17:23 Reception123: reception@jobrunner1:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki tvwikiwiki /home/reception/Wikipedia-20200402172042.xml
* 10:54 Reception123: reception@jobrunner1:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/deleteBatch.php --wiki gmcwiki -r "Requested - T5284" /home/reception/graaldel.txt
* 10:53 Reception123: removed 2FA from a phab user
* 10:52 paladox: restarted logbot on mon1

## 2020-04-01 

* 06:27 Reception123: reception@jobrunner1:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki housingwikiwiki /home/reception/wiki-yimby_wiki-XML-20200331.xml
* 01:23 paladox: apt-get upgrade - mail1, misc1
* 01:20 paladox: apt-get upgrade - jobrunner1
* 01:14 paladox: upgraded nodejs on test2
* 01:11 paladox: upgraded nodejs on mw[4567]
* 01:10 paladox: upgraded nodejs on services1

## 2020-03-31 

* 23:18 paladox: rm /srv/mediawiki/w/cache/managewiki/*realtimefandubgameswikiwiki* - mw*
* 16:41 paladox: apt-get dist upgrade - misc1
* 13:28 paladox: restart varnish + nginx on cp7
* 12:19 paladox: restart php7.3-fpm on mw4
* 12:18 paladox: restart php7.3-fpm on mw7 and chown php-error.log as www-data
* 12:17 paladox: restart php7.3-fpm on mw6 and chown php-error.log as www-data
* 12:06 paladox: reboot services1
* 12:06 paladox: reboot services2
* 09:45 paladox: stop ircrcbot on misc1
* 06:34 Reception123: reception@jobrunner1:~/wiki/images$ sudo -u www-data php /srv/mediawiki/w/maintenance/importImages.php --wiki=sagan4alphawiki --search-recursively --skip-dupes /home/reception/wiki/images

## 2020-03-30 

* 21:34 Zppix: drop dummy wiki dbs for old infra (DONE: mw[123], db[12345] lizardfs[12345] cp[1245])
* 21:18 Zppix: created dummy wiki dbs to prevent conflict with services/servers (mon1, icinga, grafana, dbt1)
* 01:06 paladox: apt-get dist-upgrade - services2
* 01:04 paladox: apt-get dist-upgrade - services1

## 2020-03-29 

* 23:54 paladox: remove db4 from puppetdb
* 23:45 paladox: remove mw[123] and lizardfs6 from puppetdb
* 23:36 paladox: restart php7.3-fpm on mw*
* 21:45 paladox: apt-get upgrade - mail1
* 20:16 paladox: depool mw7 and repool
* 20:05 paladox: restart php7.3-fpm on mw*
* 19:59 paladox: depool mw6 and repool
* 19:59 paladox: increase mw[67] vpcu by 1
* 19:59 paladox: sudo -u www-data php /srv/mediawiki/w/maintenance/deleteBatch.php --wiki crappygameswiki -r "Requested - T5324" /home/reception/cgwdel.txt - mw4
* 19:59 paladox: repool mw5
* 19:59 paladox: increase mw5 vcpu by 1
* 19:59 paladox: depool mw5
* 19:58 paladox: repool mw4
* 19:58 paladox: increase mw4 vcpu by 1
* 19:55 paladox: depool mw4
* 19:30 Reception123: add alteversewiki webhook for discord
* 17:58 Reception123: added webhook for zoitecwiki
* 17:43 paladox: rm /srv/mediawiki/w/cache/managewiki/*privado* on mw*
* 17:43 paladox: deleting *privado* in redis
* 17:43 paladox: recreating privadowiki
* 17:39 paladox: rm /srv/mediawiki/w/cache/managewiki/* ucronias* on mw*
* 17:38 paladox: deleting * ucronias* in redis
* 17:38 paladox: recreating ucroniaswiki
* 17:35 paladox: rm /srv/mediawiki/w/cache/managewiki/*hispano* on mw*
* 17:32 paladox: deleting *hispano* in redis
* 17:30 paladox: recreating hispanowiki
* 16:40 Southparkfan: ack icinga alerts for decom'ed servers
* 14:55 paladox: repool mw5
* 14:53 paladox: depool mw5
* 14:51 paladox: repool mw4
* 14:50 paladox: depool mw4
* 14:50 paladox: increased mw[45] vpcu by 1
* 14:48 paladox: decrease puppet2 vcpu by one
* 14:25 Reception123: reception@mw4:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/deleteBatch.php --wiki crappygameswiki -r "Requested - T5324" /home/reception/cgwdel.txt
* 07:58 Reception123: reception@mw4:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/importImages.php --wiki=sagan4alphawiki --search-recursively --skip-dupes /home/reception/images
* 04:53 paladox: restart logbot on mon1
* 04:53 paladox: stop mysql on db4
* 02:40 paladox: puppetserver ca clean --certname lizardfs6.m.org/mw3.m.org
* 01:31 paladox: increased puppet2 ram by 1gb and removed swap
* 01:24 paladox: add 1g swap to puppet2
* 01:14 paladox: delete all wikis on db4 that have been migrated to dbt1
* 00:43 paladox: restart php-fpm on mw*

## 2020-03-28 

* 19:20 Reception123: removed a 2FA from a user
* 18:36 Reception123: reception@mw1:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/deleteBatch.php --wiki awesomegameswiki -r "Requested (old fandom accounts) - T5356" /home/reception/agwdel.txt
* 14:09 paladox: restarted php7.3-fpm on mw*
* 02:44 paladox: drop 1.6k wikis on db4 (migrated to dbt1)

## 2020-03-27 

* 23:14 paladox: apt-get upgrade puppet-agent - mw3
* 18:41 paladox: restart php7.3-fpm on mw*

## 2020-03-26 

* 15:39 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildLocalisationCache.php --wiki loginwiki on mw*
* 15:33 paladox: restart logbot on mon1
* 02:24 paladox: install links on test2
* 01:58 paladox: reset extensions/CreateWiki on test2

## 2020-03-25 

* 23:27 paladox: restarted php7.3-fpm on mw*

## 2020-03-24 

* 17:01 Reception123: deleted and dropped testdelete1wiki
* 16:23 Reception123: sudo -u www-data php populateContentTables.php --wiki [hispanowiki/ucroniaswiki/pricadowiki]
* 16:19 Reception123: reception@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php populateContentModel.php --wiki [hispanowiki/ucroniaswiki/pricadowiki] --ns "all" --table page/revision

## 2020-03-23 

* 18:34 paladox: service parsoid stop ; killall -u parsoid ; service parsoid start - services[12]
* 15:32 paladox: that is on nginx
* 15:25 paladox: disable logging on mw[46] as an experiment
* 15:19 paladox: MariaDB [ucroniaswiki]> INSERT INTO slot_roles (`role_id`, `role_name`) VALUES (1, 'main'); - db7
* 15:18 paladox: MariaDB [hispanowiki]> INSERT INTO slot_roles (`role_id`, `role_name`) VALUES (1, 'main'); - db7
* 15:17 paladox: MariaDB [privadowiki]> INSERT INTO slot_roles (`role_id`, `role_name`) VALUES (1, 'main'); - db7

## 2020-03-22 

* 23:29 paladox: MariaDB [privadowiki]> INSERT INTO content_models (`model_id`, `model_name`) VALUES (3, 'javascript'); - db7
* 23:28 paladox: MariaDB [privadowiki]> INSERT INTO content_models (`model_id`, `model_name`) VALUES (4, 'Scribunto'); - db7
* 23:28 paladox: MariaDB [privadowiki]> INSERT INTO content_models (`model_id`, `model_name`) VALUES (5, 'json'); - db7
* 23:28 paladox: MariaDB [privadowiki]> INSERT INTO content_models (`model_id`, `model_name`) VALUES (2, 'css'); - db7
* 21:35 paladox: drop database ndgwiki and nenawikiwiki on db4
* 21:28 Zppix: (paladox): migrated ndg and nena wikis

## 2020-03-21 

* 19:52 paladox: delete ucroniaswiki
* 19:51 paladox: delete hispanowiki
* 16:09 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/deleteBatch.php --wiki rottenwebsiteswiki -r "Requested - T5313" /home/reception/delrt1.txt on mw1
* 16:01 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/dumpBackup.php --wiki aerosswiki --full > /home/reception/aerosswiki21032020.xml
* 15:57 Reception123: renamed magnaversewiki to cnocbridewiki (db+cw)
* 15:13 Reception123: UPDATE cw_wikis SET wiki_closed = 0 AND wiki_closed_timestamp = NULL WHERE wiki_closed_timestamp > 20200321000000 on db4
* 15:03 Reception123: php /srv/mediawiki/w/extensions/CreateWiki/maintenance/manageInactiveWikis.php --wiki loginwiki --write > /var/log/mediawiki/cron/managewikis.log on mw1
* 14:36 Reception123: reception@mw1:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildall.php --wiki rottenwebsiteswiki
* 14:13 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki sagan4alphawiki /home/reception/sagan4wiki.xml
* 13:45 Reception123: manually ran manageInactiveWikis.php
* 13:37 Reception123: manually ran manageInactiveWikis.php
* 12:00 Reception123: reception@mw1:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/deleteBatch.php --wiki rottenwebsiteswiki -r "Requested - T5313" /home/reception/delrt.txt

## 2020-03-20 

* 21:03 paladox: running lc on mw* and test2 and jobrunner1
* 20:08 paladox: upgrade puppetdb, puppetserver and puppet-agent on puppet2
* 06:37 Reception123: reception@jobrunner1:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --no-local-users --username-prefix "import" --wiki pikminfanonwiki /home/reception/pikminfanon.xml

## 2020-03-19 

* 21:18 paladox: reboot test2
* 21:13 paladox: apt-get upgrade - test2
* 21:10 paladox: rename test1wiki to test2wiki
* 20:26 paladox: MariaDB [mhglobal]> UPDATE cw_wikis SET wiki_settings = REPLACE(wiki_settings, '"wgServer":"enc.for.uz"', null ) WHERE wiki_dbname = 'uzencwiki'; - db4
* 16:44 paladox: running lc on mw*

## 2020-03-18 

* 22:53 paladox: depool mw[123]

## 2020-03-17 

* 21:05 paladox: restart php7.3-fpm on mw*
* 21:05 paladox: reboot services2
* 21:04 paladox: reboot services1
* 14:46 Zppix: rebuildrc and initsitestats on libertygamewiki following successful import

## 2020-03-16 

* 17:46 Zppix: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --no-local-users --username-prefix="리버티게임" --wiki libertygamewiki 22115932221_w-20200309-history.xml on jobrunner1
* 15:12 paladox: restart php7.3-fpm on mw*

## 2020-03-15 

* 13:47 paladox: apt-get dist-upgrade - cp7

## 2020-03-14 

* 16:04 paladox: increzse puppet2 disk by 10g

## 2020-03-13 

* 21:03 paladox: rename godaigowiki to brambowiki
* 13:20 paladox: root@puppet2:/opt/puppetlabs/server/data/puppetserver/reports# rm -rf *

## 2020-03-12 

* 20:53 paladox: root@mw1:/srv/mediawiki/w/extensions/CentralAuth/maintenance# sudo -u www-data php fixStuckGlobalRename.php --wiki=abominablememefandomswiki --logwiki=metawiki "LeonTheMonster479519314" "Just Leon"
* 20:06 paladox: root@mw1:/srv/mediawiki/w/extensions/CentralAuth/maintenance# sudo -u www-data php fixStuckGlobalRename.php --wiki=abominablememefandomswiki --logwiki=metawiki "Agent Mace" "Agent Joestar"
* 00:48 Zppix: update cw_requests set cw_status = 'approved' where cw_id = 10991;

## 2020-03-11 

* 15:36 paladox: rm -rf /srv/mediawiki/config and let it reclone, merge conflicts so recloning fresh
* 15:28 paladox: apt-get dist-upgrade - test1
* 15:26 paladox: reboot test1
* 15:11 paladox: root@puppet2:/opt/puppetlabs/server/data/puppetserver/reports# rm -rf *
* 14:08 paladox: increase gluster1 disk to 720G
* 01:25 paladox: increase gluster1 disk by 50g

## 2020-03-10 

* 22:53 paladox: apt-get upgrade - mon1 (icinga2/puppet-agent)
* 22:45 paladox: shutdown misc4
* 22:45 paladox: shutdown cp4
* 22:44 paladox: shutdown puppet1
* 21:59 paladox: MariaDB [browndustwiki]> INSERT INTO content_models (`model_id`,`model_name`) VALUES (4, 'Scribunto'); -db4
* 21:59 paladox: MariaDB [browndustwiki]> INSERT INTO content_models (`model_id`,`model_name`) VALUES (2, 'css'); -db4
* 21:58 paladox: MariaDB [browndustwiki]> INSERT INTO content_models (`model_id`,`model_name`) VALUES (3, 'javascript'); -db4
* 21:58 paladox: MariaDB [browndustwiki]> INSERT INTO content_models (`model_id`,`model_name`) VALUES (5, 'json'); -db4
* 21:58 paladox: MariaDB [browndustwiki]> INSERT INTO content_models (`model_id`,`model_name`) VALUES (1, 'wikitext'); -db4
* 21:46 paladox: MariaDB [browndustwiki]> INSERT INTO slot_roles (`role_id`,`role_name`) VALUES (1,'main'); - db4
* 21:33 paladox: root@lizardfs6:/home/paladox# gluster volume set mvol features.read-only off
* 21:03 paladox: restart jobrunner + jobchron on jobrunner1
* 20:48 paladox: delete *matomo* key in redis
* 20:32 paladox: root@jobrunner1:/srv/mediawiki/w/extensions/MirahezeMagic/maintenance# /usr/bin/nice -19 /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/addMatomo.php
* 20:31 paladox: MariaDB [mhglobal]> delete from matomo; - db4
* 19:53 Zppix: update cw_requests set cw_status = 'approved' where cw_id = 10988;
* 18:52 paladox: set features.read-only to on, on lizardfs6
* 18:17 Zppix: run cargoRecreateData.php and refreshLinks.php on jobrunner1 on hispanowiki per user request on IRC

## 2020-03-09 

* 22:51 paladox: reboot misc1
* 20:51 paladox: apt-get install puppet-agent salt-common salt-minion - cp8

## 2020-03-08 

* 23:58 paladox: started ircecho on misc1
* 13:16 Southparkfan: cancelled migration, dropping databases on db6
* 13:12 Southparkfan: migration started for first batch
* 00:47 paladox: delete db5 - not in use anymore

## 2020-03-07 

* 23:23 paladox: reinstalling ns1 as buster
* 19:26 paladox: upgrade puppet-agent on cloud[12]
* 19:21 paladox: root@cloud1:/var/lib/vz/images/118# rm vm-118-disk-0.qcow2
* 18:38 paladox: upgrade puppet-agent - ns2
* 18:37 paladox: root@cloud1:/var/lib/vz/images/118# mv vm-118-disk-0.row vm-118-disk-0.raw
* 18:34 paladox: root@cloud1:/var/lib/vz/images/118# qemu-img convert vm-118-disk-0.qcow2 vm-118-disk-0.row
* 17:41 paladox: removed prometheus_gdnsd_stats cron from misc1
* 17:39 paladox: stopped gdnsd + purged it from misc1
* 17:21 paladox: MariaDB [(none)]> set global table_open_cache = 10000; - db4
* 17:20 paladox: set global table_definition_cache = 10000; - db4
* 17:17 paladox: apt-get -t stretch-backports install linux-image-amd64 - db5
* 17:10 paladox: apt-get upgrade db5
* 06:35 Reception123: deleted and dropped streamelementswiki (T5307)
* 01:34 paladox: MariaDB [simswiki]> truncate objectcache; - db6
* 00:45 paladox: drop large wiki drops on db4/db5

## 2020-03-06 

* 23:50 Southparkfan: run pveperf on cloud1
* 20:28 paladox: root@db5:/home/paladox# ./move_all.sh
* 19:03 paladox: root@db4:/home/paladox# ./move_all.sh
* 19:02 Zppix: Migration window has started
* 18:38 paladox: sysctl -w net.ipv6.conf.all.disable_ipv6=1 - db5
* 16:52 paladox: upgrade puppet-agent on misc4

## 2020-03-05 

* 17:52 paladox: apt-get upgrade - puppet1 (puppetserver, puppetdb and a few other packages)
* 02:18 paladox: drop phabricator_% on db4
* 02:18 paladox: drop staffwiki on db4
* 01:02 paladox: set write back cache on mon1
* 00:58 paladox: increase phab1 disk by 5g
* 00:54 paladox: sysctl -w net.ipv6.conf.all.disable_ipv6=1 - db4

## 2020-03-03 

* 22:28 paladox: delete from renameuser_status where ru_wiki = 'receptionflamewarswiki'; - db4
* 22:24 paladox: delete receptionflamewarswiki from cw
* 21:06 paladox: stop db7 being a slave temporarily
* 19:38 Reception123: reception@mw1:/srv/mediawiki/w/extensions/CentralAuth/maintenance$ sudo -u www-data php fixStuckGlobalRename.php --wiki=receptionflamewarswiki TaylorSwiftFan "GrilledCheese800" --logwiki=metawiki

## 2020-03-02 

* 19:25 paladox: downgrade php-redis on mw1
* 18:15 paladox: downgraded php on jobrunner1 and upgraded gluster + few other pakcages
* 18:13 paladox: apt-get upgrade - gluster1
* 17:40 paladox: running lc on mw4
* 17:24 paladox: fixing php on mw[4567]
* 16:50 paladox: downgraded php to 7.3.14 on mw[23] lizardfs6 due to a segfault in 7.3.15, mw1 will be out of the pool till it's upgraded to buster.
* 14:30 paladox: reinstalling mw4
* 13:08 paladox: reboot mw4

## 2020-03-01 

* 17:39 paladox: root@mw2:/srv/mediawiki/w/maintenance/storage# sudo -u www-data php compressOld.php --wiki=tmewiki --type=gzip
* 17:35 paladox: root@mw1:/srv/mediawiki/w/maintenance/storage# sudo -u www-data php compressOld.php --wiki=crappygameswiki --type=gzip
* 17:33 paladox: root@mw1:/srv/mediawiki/w/maintenance/storage# sudo -u www-data php compressOld.php --wiki=animatedfeetwiki --type=gzip
* 17:22 paladox: MariaDB [altversewiki]> drop database testwiki; - db5 (on db6 already)
* 17:14 paladox: MariaDB [altversewiki]> drop database ucroniaswiki; - db4 (on db6 already)
* 17:14 paladox: MariaDB [altversewiki]> drop database rotompediawiki; - db4 (on db6 already)
* 17:13 paladox: MariaDB [altversewiki]> drop database proxybotwiki; - db4 (on db6 already)
* 17:13 paladox: MariaDB [altversewiki]> drop database privadowiki; - db4 (on db6 already)
* 17:13 paladox: MariaDB [altversewiki]> drop database onepiecewiki; - db4 (on db6 already)
* 17:13 paladox: MariaDB [altversewiki]> drop database onepiecebountyrushwiki; - db4 (on db6 already)
* 17:12 paladox: MariaDB [altversewiki]> drop database nonbinarywiki; - db4 (on db6 already)
* 17:12 paladox: MariaDB [altversewiki]> drop database nbdbwiki; - db4 (on db6 already)
* 17:12 paladox: MariaDB [altversewiki]> drop database hispanowiki; - db4 (on db6 already)
* 17:11 paladox: MariaDB [altversewiki]> drop database dreamversewiki; - db4 (on db6 already)
* 17:10 paladox: MariaDB [altversewiki]> drop database anotheredenwiki; - db4 (on db6 already)
* 17:10 paladox: root@db5:/home/dbcopy# rm *sql*
* 17:09 paladox: MariaDB [altversewiki]> drop database altversewiki; - db4 (on db6 already)
* 14:47 paladox: root@mw1:/srv/mediawiki/w/maintenance# sudo -u www-data php initSiteStats.php --wiki=hispanowiki --update
* 14:46 paladox: root@mw1:/srv/mediawiki/w/maintenance# sudo -u www-data php updateArticleCount.php --wiki=hispanowiki --update
* 12:50 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/dumpBackup.php --wiki allthetropeswiki --full > /home/reception/allthetropes01032020.xml (part of wikibackups) on mw2
* 11:40 Reception123: running wikibackups (bash ./wikibackups.sh /home/reception/allpublic.dblist /srv/mediawiki/w/maintenance/dumpBackup.php) on mw1
* 11:22 Reception123: moved openhatchwiki from db4 to db5
* 11:03 Reception123: renamed epochlorewiki to mystfalllorewiki (db + script)

## 2020-02-29 

* 21:10 Reception123: PURGE BINARY LOGS BEFORE '2020-02-29 12:00'; on db4
* 00:08 paladox: ip addr del fe80::f816:3eff:fe31:f5f/64 dev ens3 - bacula2
* 00:08 paladox: ip -6 address add 2604:180:f3::382/64 dev ens3 - bacula2

## 2020-02-28 

* 22:34 Southparkfan: reinstall bacula2
* 22:11 Southparkfan: decom bacula1
* 17:43 paladox: reboot mw[45]
* 17:15 paladox: restarted php7.3-fpm on mw1
* 15:24 paladox: restart php7.3-fpm on mw* and lizardfs6
* 15:12 paladox: MariaDB [(none)]> set global innodb_io_capacity_max=3000; - db4
* 15:11 paladox: MariaDB [(none)]> set global innodb_io_capacity=1000; - db4
* 14:36 paladox: MariaDB [(none)]> set global tmp_table_size = 67108864; - db4
* 14:35 paladox: MariaDB [(none)]> set global max_heap_table_size = 67108864; (on db4

## 2020-02-27 

* 23:25 paladox: root@db4:/home/paladox# sysctl -w net.ipv4.tcp_tw_reuse=0
* 23:25 paladox: !log root@db4:/home/paladox# sysctl -w net.ipv4.tcp_fin_timeout=60
* 23:01 paladox: root@db4:/home/paladox# sysctl -w net.ipv4.tcp_tw_recycle=0
* 22:58 paladox: root@db4:/home/paladox# sysctl -w net.ipv4.tcp_tw_recycle=1
* 22:52 paladox: root@db4:/home/paladox# sysctl -w net.ipv4.tcp_fin_timeout=3
* 22:52 paladox: root@db4:/home/paladox# sysctl -w net.ipv4.tcp_tw_reuse=1
* 22:47 paladox: root@db4:/home/paladox# sysctl net.ipv4.tcp_fin_timeout=3
* 22:44 paladox: restart php.7-3-fpm on mw* & lizardfs*
* 22:42 paladox: root@db4:/home/paladox# sysctl net.ipv4.tcp_tw_reuse=1
* 16:04 Reception123: reception@mw2:~/graalmilitary$ sudo -u www-data php /srv/mediawiki/w/maintenance/importImages.php --wiki=gmcwiki --search-recursively --skip-dupes /home/reception/graalmilitary/wikipics
* 11:48 Reception123: moved simswiki from db4 to db5

## 2020-02-26 

* 23:52 paladox: root@cloud2:/var/lib/vz/images/113# rm vm-113-disk-0.qcow2
* 23:45 paladox: root@cloud2:/var/lib/vz/images/113# qemu-img convert vm-113-disk-0.qcow2 vm-113-disk-0.raw
* 23:25 paladox: root@bacula2:/home/paladox# ip addr del fe80::f816:3eff:fe31:f5f/64 dev ens3
* 23:25 paladox: root@bacula2:/home/paladox# ip -6 address add 2604:180:f3::382/64 dev ens3
* 23:18 paladox: apt-get dist-upgrade - phab1
* 20:06 Reception123: move the previous import to jobrunner1 (per redis issues)
* 17:06 paladox: removing old kernel from cp3 using sudo apt autoremove
* 17:04 paladox: reboot cp3 - network felt slow
* 07:26 Reception123: reception@mw1:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki bigbrotherwikiwiki /home/reception/bigbrother_pages_full.xml
* 01:56 paladox: root@cloud2:/var/lib/vz/images/115# qemu-img convert vm-115-disk-0.qcow2 vm-115-disk-0.raw
* 01:45 paladox: root@cloud1:/var/lib/vz/images/111# qemu-img convert vm-111-disk-0.qcow2 vm-111-disk-0.raw
* 01:19 paladox: that's on cp3
* 01:19 paladox: apt-get install linux-image-amd64
* 01:17 paladox: apt-get upgrade - cp3
* 00:57 paladox: varnish> ban req.http.Host == static.miraheze.org (cp8|cp4)
* 00:45 paladox: varnish> ban req.http.Host == messengergeek.miraheze.org (cp4)
* 00:36 paladox: varnish> ban req.http.Host == messengergeek.miraheze.org (cp8)
* 00:25 paladox: root@cloud1:/var/lib/vz/images/107# qemu-img convert vm-107-disk-0.qcow2 vm-107-disk-0.raw
* 00:15 paladox: root@cloud1:/var/lib/vz/images/100# qemu-img convert vm-100-disk-0.qcow2 vm-100-disk-0.raw
* 00:02 paladox: root@cloud1:/var/lib/vz/images/106# qemu-img convert vm-106-disk-0.qcow2 vm-106-disk-0.raw

## 2020-02-25 

* 23:55 paladox: actually 3 in total
* 23:52 paladox: increased jobrunner1 core by 1 (so 4 in total)
* 21:33 paladox: root@cloud1:/var/lib/vz/images/112# qemu-img convert vm-112-disk-0.qcow2 vm-112-disk-0.raw
* 21:20 paladox: root@cloud2:/var/lib/vz/images/119# qemu-img convert vm-119-disk-0.qcow2 vm-119-disk-0.raw
* 21:18 paladox: root@cloud2:/var/lib/vz/images/104# rm vm-104-disk-0.qcow2
* 20:15 paladox: root@db4:/var/log/mysql# sysctl net.ipv4.tcp_tw_reuse=0
* 20:15 paladox: root@db4:/var/log/mysql# sysctl net.ipv4.tcp_fin_timeout=60
* 19:52 paladox: root@cp7:/home/paladox# sysctl net.core.somaxconn=4000
* 19:49 paladox: root@db4:/var/log/mysql# sysctl net.ipv4.tcp_fin_timeout=3
* 19:47 paladox: root@db4:/var/log/mysql# sysctl net.ipv4.tcp_tw_reuse=1
* 18:06 paladox: root@cloud2:/var/lib/vz/images/104# qemu-img convert vm-104-disk-0.qcow2 vm-104-disk-0.raw
* 18:03 paladox: root@cloud1:/var/lib/vz/images/102# rm vm-102-disk-0.qcow2 (it's been converted to raw)
* 17:48 paladox: converting puppet2 to a raw image (qemu-img convert vm-102-disk-0.qcow2 vm-102-disk-0.raw)
* 17:42 paladox: downgrade puppet2 ram back to 4g
* 17:33 paladox: increase puppet2 ram by 1gb (so 5g in total)

## 2020-02-24 

* 23:28 paladox: root@mw4:/var/log# sysctl net.core.somaxconn=512
* 22:06 Southparkfan: restarted php-fpm again
* 22:01 Southparkfan: restart php-fpm again (on mon1)
* 21:58 Southparkfan: restart php-fpm on mon1
* 18:59 paladox: apt-get upgrade - mon1
* 17:40 paladox: set global read_only=0; - db6
* 17:15 paladox: set read_only on db6
* 15:04 paladox: MariaDB [metawiki]> set global table_definition_cache=40000; - db6
* 15:04 paladox: MariaDB [metawiki]> set global table_open_cache=50000; - db6
* 15:04 paladox: MariaDB [metawiki]> set global table_definition_cache=40000; - db5
* 15:04 paladox: MariaDB [metawiki]> set global table_open_cache=50000; - db5
* 14:43 paladox: restart php7.3-fpm on mw* and lizardfs6
* 14:42 paladox: MariaDB [metawiki]> set global table_definition_cache=40000; - db4
* 14:42 paladox: MariaDB [metawiki]> set global table_open_cache=50000; - db4
* 01:02 paladox: restarted mariadb - db4 as ran out of space

## 2020-02-23 

* 22:27 paladox: root@mw4:/srv/mediawiki/w/maintenance# sudo -u www-data php resetUserTokens.php --wiki=onepiecebountyrushwiki
* 21:15 paladox: root@mw1:/srv/mediawiki/w/maintenance# sudo -u www-data php updateArticleCount.php --wiki=hispanowiki --update
* 21:14 paladox: root@mw1:/srv/mediawiki/w/maintenance# sudo -u www-data php updateArticleCount.php --wiki=ucroniaswiki --update
* 20:57 paladox: root@cloud2:/home/paladox# swapoff -a
* 20:56 paladox: root@cloud1:/home/paladox# swapoff -a
* 20:50 Reception123: reception@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php updateArticleCount.php --wiki=hispanowiki --update

## 2020-02-22 

* 02:55 paladox: drop grafana db on db4
* 02:49 paladox: apt-get install puppet-agent mariadb-client-10.1 mariadb-client-core-10.1 mariadb-common - misc2
* 02:43 paladox: remove php/nginx from misc2
* 01:45 paladox: drop database piwik on db5

## 2020-02-21 

* 23:31 paladox: migrating matomo to new infra
* 21:11 paladox: root@mw1:/srv/mediawiki/w/extensions/ManageWiki/maintenance# sudo -u www-data php populateNamespacesWithDefaults.php --wiki=unicodesubsetswiki --overwrite
* 21:10 paladox: MariaDB [mhglobal]> delete from mw_namespaces where ns_dbname = 'unicodesubsetswiki';
* 21:09 paladox: root@mw1:/srv/mediawiki/w/extensions/ManageWiki/maintenance# sudo -u www-data php populateGroupPermissionsWithDefaults.php --wiki=unicodesubsetswiki --overwrite
* 10:04 Reception123: RENAME browndustwiki to braveninewiki (db + script)

## 2020-02-20 

* 01:02 paladox: CHANGE MASTER TO MASTER_HOST='db6.miraheze.org', MASTER_USER='replica', MASTER_PASSWORD='xxxx', MASTER_LOG_FILE='mysql-bin.000004', MASTER_LOG_POS=1044075691; - db6
* 00:51 paladox: GRANT REPLICATION SLAVE ON *.* TO 'replica'@'%' IDENTIFIED BY 'xxxx'; - db6

## 2020-02-18 

* 20:54 paladox: "ip addr del fe80::216:3cff:fe25:9a18/64 dev ens3" - db4
* 20:54 paladox: "ip -6 address add 2a00:d880:5:d6c::2/64 dev ens3" - db4
* 20:25 paladox: added www-data to ssl-cert on mw[23] lizardfs6
* 20:19 paladox: fixed perms on /etc/ssl/private on lizardfs6
* 19:50 paladox: restart redis to see if it will fix the 503s
* 19:33 paladox: restart php7.3-fpm on mw* and lizardfs6
* 19:32 paladox: restart php7.3-fpm on mw1
* 19:11 paladox: enable puppet on jobrunner1
* 16:44 paladox: upgrade mariadb-client on misc1
* 16:43 paladox: upgrade grafana on misc1
* 15:10 paladox: MariaDB [metawiki]> update cw_requests set cw_status = 'approved' where cw_id = 10784;
* 15:10 paladox: MariaDB [metawiki]> update cw_requests set cw_status = 'approved' where cw_id = 10783;
* 15:10 paladox: MariaDB [metawiki]> update cw_requests set cw_status = 'approved' where cw_id = 10782;
* 15:09 paladox: MariaDB [metawiki]> update cw_requests set cw_status = 'approved' where cw_id = 10781;
* 15:08 paladox: MariaDB [metawiki]> update cw_requests set cw_status = 'approved' where cw_id = 10780;
* 15:08 paladox: MariaDB [metawiki]> update cw_requests set cw_status = 'approved' where cw_id = 10778;
* 15:07 paladox: MariaDB [metawiki]> update cw_requests set cw_status = 'approved' where cw_id = 10777;
* 15:07 paladox: MariaDB [metawiki]> update cw_requests set cw_status = 'approved' where cw_id = 10776;
* 15:04 paladox: MariaDB [metawiki]> update cw_requests set cw_status = 'approved' where cw_id = 10775;
* 15:04 paladox: MariaDB [metawiki]> update cw_requests set cw_status = 'approved' where cw_id = 10765;

## 2020-02-17 

* 16:46 paladox: restart nginx on cp4
* 16:24 paladox: ALTER TABLE /*_*/oathauth_users DROP COLUMN secret, DROP COLUMN scratch_tokens;
* 16:12 paladox: renaming kujumwiki to archlinuxfamilyorgwiki per T5241
* 16:04 paladox: renaming endeavourosdewiki to archlinuxfamilywiki per T5242
* 15:39 paladox: sudo -u www-data php populateGroupPermissionsWithDefaults.php --wiki=pcsdscotlandwiki --overwrite
* 12:50 Reception123: disabled PlavorSeol on Phabricator
* 12:04 Reception123: renamed ungamewiki to libertygamewiki (db + script)

## 2020-02-16 

* 23:52 paladox: MariaDB [allthetropeswiki]> truncate objectcache;
* 22:56 Southparkfan: set read_only=1 on db6
* 20:31 Reception123: re-inserted cw_requests from db6 after misclick
* 19:29 Reception123: removed spam from cw_requests (inappropriate comment)
* 14:49 paladox: [14:43:09] <+paladox>	!log hacked lizardfs6 Database.php (added persitents mode and removed)
* 14:44 paladox: hacked lizardfs6 Database.php (added persitents mode and removed)
* 14:43 paladox: [14:41:46] <+paladox>	!log reboot lizardfs6
* 14:31 paladox: restart php on mw[123]

## 2020-02-15 

* 19:48 paladox: depooled mw[4567]
* 18:41 paladox: repool cp4

## 2020-02-14 

* 20:28 paladox: backing up phabricator db
* 20:04 Southparkfan: install atop/iotop/iperf (with fw rule for latter) on db4/db6
* 19:34 paladox: [19:11:31] <+paladox>	!log set gluster file system to read only on lizardfs6
* 19:26 Southparkfan: added firewall rule on db4 to allow traffic from db6 (v4/v6) to port 3306
* 19:26 Southparkfan: dynamically set server_id=4 on db4 and server_id=6 on db6
* 19:26 Southparkfan: dumping db4's databases to db6 in /home/dbcopy
* 18:52 Southparkfan: disable puppet on db[456]
* 14:45 paladox: tried upgrading phabricator to latest on master, failed and rollbacked
* 10:59 Reception123: umount /mnt/mediawiki-static ; mount /mnt/mediawiki-static on mw3
* 02:35 paladox: stopped parsoid, removed /srv/parsoid from misc4
* 02:33 paladox: apt-get upgrade - misc4
* 02:25 paladox: increase puppet2 disk to 15G
* 01:42 Southparkfan: decommissioned misc3
* 01:33 Southparkfan: shutdown misc3 - testing before permanent decom
* 01:27 paladox: drop phabricator_* on db4
* 01:23 Southparkfan: decommission cp2
* 00:56 John: soft depooling of misc1 as ns2 via DNS entry change
* 00:53 Southparkfan: shutdown cp2 nginx for transferring nginx logs to cp7:/root

## 2020-02-13 

* 22:05 paladox|UKInEU: install parted on phab1
* 22:02 paladox|UKInEU: increase phab1 disk to 20g
* 21:31 paladox|UKInEU: increased phab1 cores to 2
* 20:45 paladox|UKInEU: install mariadb-client-10.1 on misc4 (to backup the db)
* 20:43 paladox|UKInEU: stop phd & nginx on misc4. Dump phabricator db, migrate to db6 and migrate phabricator to phab1
* 20:15 paladox|UKInEU: restart php7.3-fpm on mw3
* 18:33 paladox|UKInEU: restarted nginx on mw3
* 01:17 paladox|UKInEU: installed rsync on gluster1
* 00:04 paladox|UKInEU: reboot test1

## 2020-02-12 

* 23:44 paladox|UKInEU: lizardfs6 not 67
* 23:43 paladox|UKInEU: apt-get upgrade - lizardfs67
* 22:34 paladox|UKInEU: beginning migration from lizardfs6 to gluster1
* 20:42 Zppix: create more various dummy dbs to prevent issues with wiki creations
* 16:10 Reception123: move toxicfandomsandhatedomswiki from db4 to db5
* 15:48 Reception123: moved zhdelwiki from db4 to db5
* 15:32 Reception123: PURGE BINARY LOGS BEFORE '2020-02-12 12:00:00'; on db4

## 2020-02-11 

* 23:13 Zppix: created various dummy dbs using sql.php on mw1 to prevent creation of new wikis with existing hostnames to prevent potential issues
* 01:51 paladox|UKInEU: reboot cp2
* 01:33 paladox|UKInEU: MariaDB [mhglobal]> update mw_namespaces set ns_additional = '{"wgNamespacesToPostIn":true,"wgVisualEditorAvailableNamespaces":true}' where ns_dbname = 'civclassicwiki' and ns_namespace_name = '<Main>';
* 01:01 paladox|UKInEU: rm /srv/mediawiki/w/cache/managewiki/** on mw[123], lizardfs6

## 2020-02-10 

* 19:42 Reception123: MariaDB [(none)]> DROP DATABASE isabellafan2wiki;
* 19:42 Reception123: deleted isabellafan2wiki
* 02:22 paladox|UKInEU: probe gluster1 from lizardfs(gluster) but do not add it as a brick

## 2020-02-08 

* 15:29 paladox|UKInEU: rename diaroleplayswiki to sparkleswiki per [https://phabricator.miraheze.org/T5188](https://phabricator.miraheze.org/T5188)
* 15:27 paladox|UKInEU: MariaDB [shiropediawiki]> delete from nl_newsletters where nl_id = 5;
* 15:26 paladox|UKInEU: MariaDB [shiropediawiki]> delete from nl_newsletters where nl_id = 6;
* 15:20 paladox|UKInEU: renaming idiotpediawiki to nocyclopediawiki per [https://phabricator.miraheze.org/T5208](https://phabricator.miraheze.org/T5208)
* 15:15 paladox|UKInEU: delete & drop ewrikiawiki per [https://phabricator.miraheze.org/T5213](https://phabricator.miraheze.org/T5213)
* 15:14 paladox|UKInEU: drop cdwwik, gameshowswiki, glaucuswiki, receptionflamewarswiki, stargazerwikiwiki, thechasewikiwiki, toslawwiki
* 10:14 Reception123: PURGE BINARY LOGS BEFORE '2020-02-08 08:00';

## 2020-02-07 

* 19:22 Zppix: create mw[67]wiki using sql.php
* 19:21 Zppix: created cloud1 and cloud2 dbs using sql.php

## 2020-02-06 

* 01:41 paladox|UKInEU: reboot mw3

## 2020-02-05 

* 19:49 paladox|UKInEU: upgrade php on lizardfs6
* 19:47 paladox|UKInEU: upgrade php on mw1
* 19:46 paladox|UKInEU: upgrade php on mw2
* 19:43 paladox|UKInEU: upgrade php on mw3
* 19:39 paladox|UKInEU: restart php7.3-fpm on mw3
* 19:31 Zppix: initsitestats and rebuildrc for ungamewiki after import

## 2020-02-04 

* 20:47 Southparkfan: locked phab auth config
* 20:41 Southparkfan: unlocked phab auth config (temp)

## 2020-02-03 

* 17:28 paladox|UKInEU: root@mw1:/var/log/mediawiki# rm *.log.*
* 17:27 paladox|UKInEU: rm /var/log/mediawiki/*.log*
* 17:26 paladox|UKInEU: rm /var/log/mediawiki/*.log

## 2020-02-02 

* 15:50 paladox|UKInEU: > MatomoAnalytics::addSite( 'loginwiki' );
* 15:50 paladox|UKInEU: > MatomoAnalytics::deleteSite( 'loginwiki' );
* 15:48 paladox|UKInEU: > MatomoAnalytics::addSite( 'foxmaskeventwiki' );
* 15:48 paladox|UKInEU: > MatomoAnalytics::deleteSite( 'foxmaskeventwiki' );
* 15:48 paladox|UKInEU: > MatomoAnalytics::addSite( 'davshiqwiki' );
* 15:48 paladox|UKInEU: > MatomoAnalytics::deleteSite( 'davshiqwiki' );
* 14:03 paladox|UKInEU: remove hack from cron - db5
* 04:34 paladox|UKInEU: hack /var/spool/cron/crontabs/root and run /home/paladox/purge-binary.sh every 1 minute.
* 00:38 paladox|UKInEU: root@mw1:/srv/mediawiki/w/maintenance# sudo -u www-data php rebuildall.php --wiki=csydeswiki
* 00:02 paladox|UKInEU: drop database piwik on db5; create databse db5 & import from backup. To see if this will reduce the disk space it's using from ~75gb.

## 2020-02-01 

* 23:19 paladox|UKInEU: drop database uncyclomirrorwiki on db4 as migrated to db5
* 22:29 paladox|UKInEU: root@mw1:/srv/mediawiki/w/maintenance/storage# sudo -u www-data php compressOld.php --wiki=metawiki --type=gzip
* 22:23 paladox|UKInEU: root@mw1:/srv/mediawiki/w/maintenance/storage# sudo -u www-data php compressOld.php --wiki=toxicfandomsandhatedomswiki --type=gzip
* 22:18 paladox|UKInEU: root@mw1:/srv/mediawiki/w/maintenance/storage# sudo -u www-data php compressOld.php --wiki=uncyclomirrorwiki --type=gzip
* 22:14 paladox|UKInEU: root@mw1:/srv/mediawiki/w/maintenance/storage# sudo -u www-data php compressOld.php --wiki=altversewiki --type=gzip
* 12:26 Reception123: reception@mw1:/srv/mediawiki/w/extensions/CentralAuth/maintenance$ sudo -u www-data php fixStuckGlobalRename.php --wiki=receptionflamewarswiki Tundra "Just Amelia" --logwiki=metawiki

## 2020-01-31 

* 16:48 paladox|UKInEU: MariaDB [gmcwiki]> INSERT INTO content_models (model_id,model_name) VALUES (4,'Scribunto');
* 16:47 paladox|UKInEU: MariaDB [gmcwiki]> INSERT INTO content_models (model_id,model_name) VALUES (2,'css');
* 16:47 paladox|UKInEU: MariaDB [gmcwiki]> INSERT INTO content_models (model_id,model_name) VALUES (3,'javascript');
* 16:47 paladox|UKInEU: MariaDB [gmcwiki]> INSERT INTO content_models (model_id,model_name) VALUES (5,'json');
* 16:46 paladox|UKInEU: MariaDB [gmcwiki]> INSERT INTO content_models (model_id,model_name) VALUES (1,'wikitext');
* 16:43 paladox|UKInEU: MariaDB [gmcwiki]> INSERT INTO slot_roles (role_id,role_name) VALUES (1,'main');
* 16:37 paladox|UKInEU: root@mw1:/srv/mediawiki/w/maintenance# sudo -u www-data php cleanupUsersWithNoId.php --wiki=gmcwiki --force -p gmcwiki

## 2020-01-30 

* 18:02 paladox: apt-get upgrade - mw[123] (gluster, php and puppet-agent + few other packages)
* 17:55 paladox: apt-get upgrade - lizardfs6 (gluster, php and puppet-agent + few other packages)

## 2020-01-28 

* 23:42 paladox: upgrade puppet-agent & salt on misc1
* 23:41 paladox: upgrade php - misc1
* 23:36 paladox: upgrade grafana - misc1
* 22:00 paladox: root@mw1:/srv/mediawiki/w/maintenance/storage# sudo -u www-data php compressOld.php --wiki=ungamewiki --type=gzip
* 21:58 paladox: MariaDB [mhglobal]> UPDATE cw_wikis SET wiki_settings = REPLACE(wiki_settings, '"wgServer":"https:\/\/guiasdobrasil.com.br "', null ) WHERE wiki_dbname = 'guiaslocaiswiki';
* 19:32 paladox: root@mw1:/srv/mediawiki/w/maintenance# sudo -u www-data php nukeNS.php --wiki=thefinalrumblewiki --all --ns=3001 --delete
* 13:13 Reception123: reception@mw1:/srv/mediawiki/w/extensions/CentralAuth/maintenance$ sudo -u www-data php fixStuckGlobalRename.php --wiki=receptionflamewarswiki Toshinori "Agent Mace" --logwiki=metawiki
* 00:53 paladox: root@mw1:/srv/mediawiki/w/maintenance# sudo -u www-data php recountCategories.php --wiki=ucroniaswiki --mode=files
* 00:52 paladox: root@mw1:/srv/mediawiki/w/maintenance# sudo -u www-data php recountCategories.php --wiki=ucroniaswiki --mode=subcats
* 00:52 paladox: root@mw1:/srv/mediawiki/w/maintenance# sudo -u www-data php recountCategories.php --wiki=ucroniaswiki --mode=pages

## 2020-01-27 

* 22:59 paladox: sync; echo 1 > /proc/sys/vm/drop_caches (lizardfs6 & db4)
* 22:50 paladox: sudo /sbin/sysctl -w vm.drop_caches=3 on lizardfs6 and db4 temporarily
* 22:28 Zppix: zppix@mw1:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --report=1 --no-local-users --username-prefix "백괴게임" --wiki ungamewiki /home/zppix/uncyclogame-full-2019-05-15.xml (T5148)
* 20:02 paladox: root@mw1:/srv/mediawiki/w/maintenance# sudo -u www-data php deleteBatch.php --wiki=thefinalrumblewiki list (Deleting Message_Wall:%)
* 19:57 paladox: root@mw1:/srv/mediawiki/w/maintenance# sudo -u www-data php deleteBatch.php --wiki=thefinalrumblewiki list2 (Deleting User_blog_comment:%)
* 19:55 paladox: root@mw1:/srv/mediawiki/w/maintenance# sudo -u www-data php deleteBatch.php --wiki=thefinalrumblewiki list (Deleting User_blog:%)
* 19:51 paladox: root@mw1:/srv/mediawiki/w/maintenance# sudo -u www-data php nukeNS.php --wiki=thefinalrumblewiki --all --ns=3000 --delete
* 17:28 paladox: root@mw1:/srv/mediawiki/w/extensions/CentralAuth/maintenance# sudo -u www-data php migrateAccount.php --wiki=wikifinanzawiki --userlist=./userlist --homewiki=wikifinanzawiki --attachmissing --auto
* 15:26 Reception123: reception@mw1:/srv/mediawiki/w/extensions/CentralAuth/maintenance$ sudo -u www-data php fixStuckGlobalRename.php --wiki=receptionflamewarswiki ZapperGlaze49 "TheChisatoFan" --logwiki=metawiki

## 2020-01-26 

* 22:15 paladox: revert hack on mw[123] & lizardfs6
* 20:12 paladox: hacked LS on mw[123] & lizardfs6 to switch off wgUseInstantCommons temporarily
* 17:51 Reception123: reception@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php recountCategories.php --wiki=ucroniaswiki --mode=pages/subpages/files
* 17:41 paladox: root@mw2:/srv/mediawiki/w/maintenance# sudo -u www-data php refreshLinks.php --wiki=ucroniaswiki
* 17:41 paladox: root@mw2:/srv/mediawiki/w/maintenance# sudo -u www-data php recountCategories.php --wiki=ucroniaswiki --mode=pages
* 16:48 paladox: revert hack on mw[123] & lizardfs6
* 15:18 paladox: hacked LS on mw[23] & lizardfs6 to switch off wgUseInstantCommons temporarily
* 15:17 paladox: hacked LS on mw1 to switch off wgUseInstantCommons temporarily
* 15:06 paladox: restart php7.3-fpm on mw1 and mw3
* 15:05 paladox: restart php7.3-fpm on mw2 and lizardfs6
* 06:37 Reception123: deleted and dropped gmcwiki (T5150)

## 2020-01-25 

* 18:40 Zppix: sudo -u www-data php /srv/mediawiki/w/maintenance/deleteBatch.php --wiki crappygameswiki -u "Zppix" -r "Requested - T5153" /home/zppix/crappygameswiki_batchdelete.txt
* 18:21 Reception123: reception@mw1:/srv/mediawiki/w/extensions/CentralAuth/maintenance$ sudo -u www-data php fixStuckGlobalRename.php --wiki=receptionflamewarswiki TTyranny "Tarbiz" --logwiki=metawiki
* 17:52 paladox: reinstall php on misc2
* 17:47 paladox: rotate redis.log on misc2
* 15:02 paladox: restart php7.3-fpm && nutcracker on mw3
* 15:00 paladox: restart php7.3-fpm && nutcracker on mw2
* 00:16 paladox: MariaDB [mhglobal]> UPDATE cw_wikis SET wiki_settings = REPLACE(wiki_settings, '"wgServer":"https:\/\/wiki.udia.ca "', null ) WHERE wiki_dbname = 'udiawiki';
* 00:15 paladox: MariaDB [mhglobal]> UPDATE cw_wikis SET wiki_settings = REPLACE(wiki_settings, '"wgServer":"https:\/\/islamkosh.tk "', null ) WHERE wiki_dbname = 'ipediawiki';
* 00:15 paladox: MariaDB [mhglobal]> UPDATE cw_wikis SET wiki_settings = REPLACE(wiki_settings, '"wgServer":"https:\/\/glp.ink "', null ) WHERE wiki_dbname = 'cnwiki';
* 00:14 paladox: MariaDB [mhglobal]> UPDATE cw_wikis SET wiki_settings = REPLACE(wiki_settings, '"wgServer":"https:\/\/wiki.counterculturelabs.org "', null ) WHERE wiki_dbname = 'cclwiki';

## 2020-01-24 

* 23:28 paladox: restart php7.3-fpm on mw3 and lizardfs6
* 23:28 paladox: restart php7.3-fpm on mw2
* 23:27 paladox: restart php7.3-fpm on mw1
* 14:12 paladox: MariaDB [mhglobal]> update mw_permissions set perm_removegroupsfromself = '[]' where perm_removegroupsfromself = 'null';
* 14:10 paladox: Remove abusefilter-hide-log,abusefilter-hidden-log,abusefilter-modify-global,abusefilter-private,abusefilter-private-log,aft-oversighter,autocreateaccount,bigdelete,centralauth-lock,centralauth-oversight,centralauth-rename,centralauth-unmerge,centralauth-usermerge,checkuser,checkuser-log,createwiki,editincidents,editothersprofiles,editothersprofiles-private,flow-suppress,globalblock,globalblock-exempt,globalgroupmembership,globalgrouppermissions,hideuser,interwiki,managewiki-restricted,managewiki-editdefault,moderation-checkuser,mwoauthmanageconsumer,mwoauthmanagemygrants,mwoauthsuppress,mwoauthviewprivate,mwoauthviewsuppressed,oathauth-disable-for-user,oathauth-view-logrenameuser,requestwiki,siteadmin,stopforumspam,suppressionlog,suppressrevision,usermerge,userrights,userrights-interwiki,viewglobalprivatefiles,viewpmlog,viewsuppressed from all wikis.
* 14:04 paladox: MariaDB [mhglobal]> update mw_permissions set perm_addgroupstoself = '[]' where perm_addgroupstoself = 'null';
* 14:02 paladox: rm -rf /srv/mediawiki/w/cache/managewiki/** on mw* and lizardfs6
* 14:01 paladox: MariaDB [mhglobal]> update mw_permissions set perm_removegroupsfromself = '[]' where perm_removegroupsfromself = 'null';
* 14:01 paladox: MariaDB [mhglobal]> update mw_permissions set perm_removegroups = '[]' where perm_removegroups = 'null';
* 14:01 paladox: MariaDB [mhglobal]> update mw_permissions set perm_addgroups = '[]' where perm_addgroups = 'null';
* 13:59 paladox: MariaDB [mhglobal]> update mw_permissions set perm_addgroupstoself = '[]' where perm_addgroupstoself = 'null';
* 13:38 paladox: remove oathauth-disable-for-user from all groups.

## 2020-01-23 

* 00:29 paladox_UK_IN_EU: root@mw1:/home/paladox# sudo -u www-data php /srv/mediawiki/w/maintenance/importImages.php --wiki=spectrobeswiki --search-recursively --skip-dupes ./Spectrobes_Wiki_Images

## 2020-01-22 

* 23:54 paladox: apt-get upgrade cp3
* 22:51 paladox: remove oathauth-disable-for-user from all wikis
* 19:29 paladox_UK_IN_EU: remove oauthauth-disable-for-user from all wikis
* 18:31 paladox: root@mw1:/home/paladox# sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=spectrobeswiki --report=1 spectrobes_pages_full.xml - per request through email
* 18:31 paladox: root@mw1:/home/paladox# sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=spectrobeswiki --report=1 spectrobes_pages_full.xml.7z - per request through email
* 06:52 Reception123: reception@mw1:/srv/mediawiki/w/extensions/CentralAuth/maintenance$ sudo -u www-data php fixStuckGlobalRename.php --wiki=receptionflamewarswiki WageUglyDollandMarlaPlaymobil12 "Just Wage" --logwiki=metawiki

## 2020-01-21 

* 21:29 paladox: restart nutcracker on mw1
* 14:53 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=wiesepediawiki /home/reception/Wiesepedia-Datadump[0,A-D] on mw1
* 14:47 Reception123: PURGE BINARY LOGS before '2020-01-20 22:00:00' on db4
* 14:46 Reception123: manually remove custom domain for hypewiki
* 14:37 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=gmcwiki /home/reception/graalmilitary_pages_full.xml on mw3
* 14:33 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=spectrobeswiki /home/reception/spectrobes_pages_full.xml on mw3

## 2020-01-20 

* 17:05 paladox: ALTER TABLE /*_*/searchindex MODIFY COLUMN si_title TEXT BINARY NOT NULL; - simswiki
* 16:59 paladox: ran ./2.sh on db4 (basically finding all titles that are in User Blog Comment on wikia and setting ns id to 3007 from 0)
* 16:54 Zppix: UPDATE cw_wikis SET wiki_settings = REPLACE(wiki_settings, '"wgServer":"https:\/\/nonsensopedia.org "', null ) WHERE wiki_dbname = 'nonsensopediawiki'; on mw1 using sql.php
* 01:07 paladox: ALTER TABLE /*_*/searchindex MODIFY COLUMN si_title varchar(300) BINARY NOT NULL default* ; - simswiki (applying
* 00:49 paladox: MariaDB [simswiki]> update page set page_namespace = 3007 where page_namespace = 3008;
* 00:42 paladox: remove hack from mw1
* 00:39 paladox: ALTER TABLE /*_*/searchindex MODIFY COLUMN si_title TEXT BINARY NOT NULL; (applying [https://gerrit.wikimedia.org/r/#/c/mediawiki/core/+/565765/8](https://gerrit.wikimedia.org/r/#/c/mediawiki/core/+/565765/8) to simswiki)
* 00:11 paladox: MariaDB [simswiki]> update page set page_namespace = 3008 where page_namespace = 3007;

## 2020-01-19 

* 22:30 paladox: hacked rebuildtextindex.php on mw1 to output some debugging info
* 21:45 paladox: root@mw1:/srv/mediawiki/w/maintenance# sudo -u www-data php rebuildall.php --wiki=simswiki
* 21:44 paladox: ALTER TABLE /*_*/searchindex MODIFY COLUMN si_title varchar(255) BINARY NOT NULL default ''; - simswiki (fixing an issue when rebuilding search index)
* 21:38 paladox: root@mw1:/srv/mediawiki/w/maintenance# sudo -u www-data php /srv/mediawiki/w/maintenance/deleteBatch.php --wiki=hispanowiki batch2 - T5122
* 21:37 paladox: root@mw1:/srv/mediawiki/w/maintenance# sudo -u www-data php /srv/mediawiki/w/maintenance/deleteBatch.php --wiki=ucroniaswiki batch - T5122
* 21:34 paladox: root@mw1:/srv/mediawiki/w/extensions/ManageWiki/maintenance# sudo -u www-data php populateGroupPermissionsWithDefaults.php --wiki=toastycraftwiki --overwrite -T5119
* 21:34 paladox: root@mw1:/srv/mediawiki/w/extensions/ManageWiki/maintenance# sudo -u www-data php populateGroupPermissionsWithDefaults.php --wiki=aranziaronzowiki --overwrite -T5119
* 17:45 paladox: root@mw1:/srv/mediawiki/w/maintenance# sudo -u www-data php /srv/mediawiki/w/maintenance/deleteBatch.php --wiki=hispanowiki batch2
* 17:34 paladox: root@mw1:/srv/mediawiki/w/maintenance# sudo -u www-data php /srv/mediawiki/w/maintenance/deleteBatch.php --wiki=ucroniaswiki batch
* 15:05 paladox: root@mw1:/home/paladox# sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=loginwiki --report=1 Wikipedia-20200119150417.xml
* 14:57 paladox: root@mw1:/home/paladox# sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=loginwiki --report=1 Wikipedia-20200119145611.xml
* 13:54 paladox: root@mw1:/srv/mediawiki/w/maintenance# sudo -u www-data php rebuildall.php --wiki=simswiki
* 08:51 Reception123: reception@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php deleteBatch.php --wiki=thefinalrumblewiki /home/reception/deletebatch.txt
* 01:23 paladox: restart php7.3-fpm on lizardfs6
* 00:25 paladox: root@mw1:/home/paladox# sudo -u www-data php /srv/mediawiki/w/maintenance/importImages.php --wiki=thefinalrumblewiki --skip-dupes --search-recursively TFR_Wikia_Images/ (per request on discord)

## 2020-01-18 

* 22:15 paladox: root@mw1:/home/paladox# sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=simswiki --report=1 --no-updates sims_pages_full.xml
* 22:09 paladox: root@mw1:/srv/mediawiki/w/maintenance# sudo -u www-data php deleteBatch.php --wiki=thefinalrumblewiki batch - per request on discord
* 20:46 paladox: root@mw1:/home/paladox# sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=simswiki --report=1 sims_pages_full.xml
* 17:09 paladox: that script is adding "urlshortener-create-url" to * for all wikis
* 17:08 paladox: root@mw1:/home/paladox# ./foreachwikiindblist /srv/mediawiki/dblist/all.dblist
* 16:58 paladox: delete from mw_permissions where perm_dbname = '131parkhurstwiki' and perm_group = "all.dblist";
* 15:44 paladox: delete from mw_permissions where perm_dbname = '131parkhurstwiki' and perm_group = "\\*" LIMIT 1;
* 15:44 paladox: delete from mw_permissions where perm_dbname = '00sretrolivingwiki' and perm_group = "\\*" LIMIT 1;
* 15:44 paladox: delete from mw_permissions where perm_dbname = '131parkhurstwiki' and perm_group = "\\*" LIMIT 1;
* 15:44 paladox: delete from mw_permissions where perm_dbname = '131parkhurstwiki' and perm_group = "\\*" LIMIT 1;
* 15:44 paladox: delete from mw_permissions where perm_dbname = '00sretrolivingwiki' and perm_group = "\\*" LIMIT 1;
* 15:43 paladox: delete from mw_permissions where perm_dbname = '00sretrolivingwiki' and perm_group = "\*" LIMIT 1;
* 15:43 paladox: delete from mw_permissions where perm_dbname = '00sretrolivingwiki' and perm_group = '\*' LIMIT 1;
* 15:43 paladox:  delete from mw_permissions where perm_dbname = '00sretrolivingwiki' and perm_group = '+' LIMIT 1;
* 15:43 paladox: delete from mw_permissions where perm_dbname = '00sretrolivingwiki' and perm_group = '+' LIMIT 1;
* 15:43 paladox: delete from mw_permissions where perm_dbname = '1920swiki' and perm_group = '+' LIMIT 1;
* 15:43 paladox: delete from mw_permissions where perm_dbname = '1920swiki' and perm_group = '"*"' LIMIT 1;
* 15:43 paladox:  delete from mw_permissions where perm_dbname = '131parkhurstwiki' and perm_group = '"*"' LIMIT 1;
* 15:43 paladox: delete from mw_permissions where perm_dbname = '131parkhurstwiki' and perm_group = '\*' LIMIT 1;
* 15:43 paladox: delete from mw_permissions where perm_dbname = '00sretrolivingwiki' and perm_group = '\*' LIMIT 1;
* 15:42 paladox: delete from mw_permissions where perm_dbname = '00sretrolivingwiki' and perm_group = '"*"' LIMIT 1;
* 14:16 Reception123: manually remove custom domain from teessidehackspacewiki

## 2020-01-17 

* 19:10 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=thefinalrumblewiki /home/reception/thefinalrumble_pages_full.xml
* 02:11 paladox: rm -rf /srv/mediawiki/w/cache/manage*/** on mw* and lizardfs6
* 01:48 paladox: restoring mw_permissions from a newish backup (after running "delete from mw_permissions where perm_group = "\*";" which seemed to updated 4,000 results)
* 01:43 paladox: update mw_permissions set perm_permissions = '["autocreateaccount","createaccount","edit","createpage","createtalk", "writeapi","viewmywatchlist","editmywatchlist","viewmyprivateinfo", "editmyprivateinfo","editmyoptions","abusefilter-log","abusefilter-log-detail", "abusefilter-view","autocreateaccount","centralauth-merge", "oathauth-enable","urlshortener-create-url"]' where perm_group = '*' and perm_dbname = 'default';
* 00:12 paladox: apt-get upgrade - misc2

## 2020-01-16 

* 23:53 paladox: /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/extensions/ManageWiki/maintenance/modifyGroupPermission.php --addperms="urlshortener-create-url,urlshortener-manage-url" sysop
* 23:47 paladox: update mw_permissions set perm_permissions = '["editsitecss","upload_by_url","editsitejson","editsitejs","skipcaptcha","block","createaccount","delete","deletedhistory","deletedtext","undelete","editinterface","editusercss","edituserjson","edituserjs","import","importupload","move","move-subpages","move-rootuserpages","move-categorypages","patrol","autopatrol","protect","editprotected","rollback","upload","reupload","reupload-shared","unwatchedpages","autoconfirmed","editsemiprotected","ipblock-exempt","blockemail","markbotedits","apihighlimits","browsearchive","noratelimit","movefile","unblockself","suppressredirect","mergehistory","managechangetags","deletechangetags","abusefilter-modify","abusefilter-modify-restricted","abusefilter-revert","deletelogentry","deleterevision","abusefilter-log-detail","override-antispoof","globalblock-whitelist","massmessage","nuke","tboverride","titleblacklistlog", "delete-dump","generate-dump","view-dump","urlshortener-create-url","urlshortener-manage-url"]' where perm_group = 'sysop' and perm_dbname = 'default';
* 02:34 paladox: reboot misc4
* 02:15 paladox: downgraded puppetdb on puppet1 - broke ssl connection to postgresql
* 01:48 paladox: root@db4:/home/paladox# sudo service postgresql restart
* 01:44 paladox: on puppet1
* 01:44 paladox: apt-get upgrade puppet-agent puppetdb puppetdb-termini puppetserver salt-common salt-minion
* 01:43 paladox: upgrade puppet-agent on cp4

## 2020-01-15 

* 08:26 Reception123: sudo -u www-data php fixStuckGlobalRename.php --wiki=receptionflamewarswiki AnimalLovingGuy "ScrewSociety" --logwiki=metawiki

## 2020-01-14 

* 23:10 paladox: reinstall cp2 as debian buster
* 23:09 paladox: restart php7.3-fpm on mw2 for config change
* 23:09 paladox: turn TUN off on cp2
* 23:06 paladox: restart php7.3-fpm on mw3 for config change
* 22:59 paladox: rebuild lc on mw* and lizardfs6
* 17:39 paladox: apt-get upgrade - lizardfs6
* 01:43 paladox: sudo -u www-data php update.php --wiki=sagan4wiki --quick --force - mw1
* 01:21 paladox: MariaDB [sagan4wiki]> ALTER TABLE /*_*/cargo_tables ADD field_helper_tables text NOT NULL;

## 2020-01-13 

* 15:32 paladox: MariaDB [mhglobal]> UPDATE cw_wikis SET wiki_settings = REPLACE(wiki_settings, '"wgServer":"https:\/\/wintermoor.net "', null ) WHERE wiki_dbname = 'wintermoorwiki';

## 2020-01-12 

* 23:29 paladox: removed redis from all mediawiki servers
* 15:25 paladox: repooled lizardfs6
* 15:15 paladox: temporarily depool lizardfs6
* 08:32 Reception123: reception@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php purgeList.php --all --purge --wiki twinkletestwiki + rebuildall.php
* 08:06 Reception123: ran rebuildall on twinkletestwiki

## 2020-01-11 

* 23:35 paladox: [23:30:52]  <+paladox>	!log switched TUN off on misc2
* 23:34 paladox: apt-get upgrade on misc2
* 22:52 paladox: upgrade nodejs on misc3
* 22:48 paladox: resizing misc3 - [https://clientarea.ramnode.com/index.php?rp=/announcements/431/More-SSD-for-Standard-KVM.html](https://clientarea.ramnode.com/index.php?rp=/announcements/431/More-SSD-for-Standard-KVM.html)
* 17:04 paladox: apt-get upgrade - bacula1
* 16:58 paladox: root@bacula1:/bacula/backup# rm DB*
* 16:57 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildLocalisationCache.php --wiki loginwiki  on mw* and lizardfs6
* 14:59 Reception123: DELETED and DROPPED dbs [https://phabricator.miraheze.org/P247](https://phabricator.miraheze.org/P247)
* 14:52 Reception123: reception@mw1:~$ sudo -u www-data php /srv/mediawiki/w/extensions/CreateWiki/maintenance/deleteWikis.php --wiki loginwiki --delete Reception123
* 11:12 Reception123: reception@mw1:/srv/mediawiki/w/extensions/CentralAuth/maintenance$ sudo -u www-data php fixStuckGlobalRename.php --wiki=receptionflamewarswiki GasMask0217 "KP619" --logwiki=metawiki
* 10:29 Reception123: run fixStuckGlobalRename.php on all wikis for username above
* 10:18 Reception123: sudo -u www-data php fixStuckGlobalRename.php --wiki=aawikiwiki PaperClip "FireBarrier101" --logwiki=metawiki
* 04:25 paladox: repool lizardfs6
* 04:18 paladox: depool lizardfs6
* 04:18 paladox: repool mw3
* 04:12 paladox: depool mw3
* 04:12 paladox: repool mw2
* 04:08 paladox: depool mw2
* 04:07 paladox: repool mw1
* 04:04 paladox: depool mw1

## 2020-01-09 

* 22:07 paladox: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=inforevivalwiki --report=1 Wiki-20200109132453.xml
* 21:20 paladox: rebuild lc on mw* and lizardfs6
* 19:34 paladox: ALTER TABLE /*$wgDBprefix*/matomo ADD INDEX matomo_wiki (matomo_wiki); - db4
* 19:17 paladox: MariaDB [mhglobal]> ALTER TABLE /*$wgDBprefix*/cw_wikis ADD INDEX wiki_dbname (wiki_dbname); -db4
* 18:59 paladox: MariaDB [mhglobal]> ALTER TABLE /*$wgDBprefix*/mw_namespaces ADD INDEX ns_dbname (ns_dbname); -db4
* 18:59 paladox: MariaDB [mhglobal]> ALTER TABLE /*$wgDBprefix*/mw_permissions ADD INDEX perm_dbname (perm_dbname); - db4
* 00:57 paladox: restart php7.3-fpm on mw2

## 2020-01-08 

* 21:37 paladox: restart mysql on db4
* 21:33 paladox: restart mysql on db5
* 19:56 paladox: restart php7.3-fpm on lizardfs6 and mw*
* 17:16 paladox: SET GLOBAL thread_cache_size = 100; - (db4|db5)
* 16:52 paladox: MariaDB [(none)]> SET GLOBAL thread_cache_size = 80;
* 16:33 paladox: MariaDB [(none)]> SET GLOBAL thread_pool_stall_limit = 10;
* 16:14 paladox: MariaDB [(none)]> SET GLOBAL slow_query_log = 'OFF';
* 16:10 paladox: MariaDB [(none)]> SET GLOBAL long_query_time = 10;
* 16:04 paladox: MariaDB [(none)]> SET GLOBAL long_query_time = 15;
* 16:04 paladox: MariaDB [(none)]> SET GLOBAL slow_query_log = 'ON';
* 15:30 paladox: restart php7.3-fpm on mw* and lizardfs6
* 15:21 Reception123: purge binary logs BEFORE '2020-01-08 08:00'

## 2020-01-07 

* 17:16 paladox: root@mw1:/srv/mediawiki/w/extensions/CentralAuth/maintenance# sudo -u www-data php fixStuckGlobalRename.php --wiki=receptionflamewarswiki --logwiki=metawiki ErtasVideos Hendicted

## 2020-01-06 

* 20:22 Reception123: reception@mw2:/srv/mediawiki/w/maintenance$ sudo -u www-data php importDump.php --wiki testwiki /home/reception/Wikipedia-20200106202002.xml

## 2020-01-05 

* 19:47 paladox: rebuild lc on mw* and lizardfs6
* 00:25 paladox: ./bin/auth strip --user Paladox --all-types (misc4)

## 2020-01-04 

* 10:13 Reception123: reception@mw3:/srv/mediawiki/w/maintenance$ sudo -u www-data php importDump.php --wiki loginwiki /home/reception/TestWiki-20200104100040.xml

## 2020-01-02 

* 18:48 paladox: depool, repool and restart php7.3-fpm on mw3
* 18:44 paladox: depool, repool and restart php7.3-fpm on mw2
* 18:43 paladox: restart php7.3-fpm on mw1
* 18:31 paladox: root@mw1:/home/paladox# sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=radioscanningtwwiki --report=1 X.xml
* 03:10 paladox: rm -rf /srv/mediawiki/w/cache/managewiki/** on mw* and lizardfs6
* 03:01 paladox: root@test1:/srv/mediawiki/w/extensions/StopForumSpam/maintenance# sudo -u www-data php  updateBlacklist.php --wiki=sdiywiki
* 02:44 paladox: upgrade phabricator on misc4
* 02:42 paladox: MariaDB [(none)]> drop database uncyclopediakrwiki;
* 02:30 paladox: root@mw1:/home/paladox# sudo -u www-data php /srv/mediawiki/w/extensions/CreateWiki/maintenance/renameWiki.php --wiki=loginwiki --rename uncyclopediakrwiki truthwiki paladox

## 2020-01-01 

* 17:49 paladox: root@misc1:/home/paladox# deluser labster
* 15:53 Reception123: sudo -u www-data php fixStuckGlobalRename.php --wiki=200xwiki PaperClip "FireBarrier101" --logwiki=metawiki
* 14:24 Reception123: MariaDB [phabricator_herald]> UPDATE herald_rule SET isDisabled = '1' WHERE id = '21'; (empty)
* 04:36 paladox: root@mw1:/srv/mediawiki/w# /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/maintenance/sql.php /srv/mediawiki/w/extensions/QuizGame/sql/patches/patch-add-default-choice_answer_count.sql
* 00:37 paladox: restart varnish cp2,cp4

----
**Source**: [https://meta.miraheze.org/wiki/Tech:Server_admin_log/2020](https://meta.miraheze.org/wiki/Tech:Server_admin_log/2020)