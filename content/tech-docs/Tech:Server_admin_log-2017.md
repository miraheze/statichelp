---
title: Tech:Server admin log/2017
---

`{{ {{TOC right}} }}`
## 2017-12-31 

* 20:39 Reception|away: archived 2017 Jul-Dec and created 2018 Ja n-Jun
* 04:51 PuppyKun: deleted /var/tmp/phd/log/daemons.log on misc1 to free up disk space (critical)

## 2017-12-30 

* 16:14 Reception|away: DROPPED all wikis mentioned below
* 16:09 Reception|away: sudo -u www-data php /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/removeDeletedWikis.php --wiki metawiki
* 16:09 Reception|away: DELETED FROM cw_wikis aagwikiwiki aasdwiki aatechwiki abubwiki acyclopediawiki adamsaiwiki advancedazrielangelwiki adventurebookwiki afterspyredemowiki agwehlingwiki airqualitycivtechwiki akwikiwiki alhandbookwiki alkawikiwiki allbanks2wiki alphamonkeywiki altecwiki (DP)
* 15:58 Reception|away: DELETED FROM cw_wikis  wikibluewiki wikinexthotelsaleswiki xenimusiwiki xofwiki yoptimawiki 10bhwiki 1719wiki 19702wiki 21germanwiki 2309bwiki 346wiki 47thabwiki 4guys4sledswiki 7cupstestwiki (DP)
* 15:31 Reception|away: > DELETE FROM cw_wikis WHERE wiki_dbname = 'blackhatwiki'; (DP; messing with the script)
* 15:30 Reception|away: reception@mw1:/srv/mediawiki/w/extensions/MirahezeMagic/maintenance$ sudo -u www-data php manageInactiveWikis.php --wiki metawiki --warn --close
* 15:29 Reception|away: > DELETE FROM cw_wikis WHERE wiki_dbname = 'betternewswiki'; (DP, messing with the script)

## 2017-12-29 

* 19:53 PuppyKun: MariaDB [metawiki]> delete from cw_wikis where wiki_dbname="navaversewiki"; (Query OK, 1 row affected (0.00 sec))
* 17:37 Reception|away: DROP DATABASE wikiletraswiki;
* 17:35 Reception|away: > DELETE FROM cw_wikis WHERE wiki_dbname = 'wikiletraswiki';
* 16:48 Reception|away: upgraded phabricator
* 16:30 revi: added "**Wiki URL:** (replace here with link to your wiki)" in phab maniphest form 7
* 16:20 Reception|away: moved to db3 and dropped on db2 aleenghawiki ciudadciclistawiki jacksonheightswiki pathfinderwiki pluspiwiki r2wiki sdiywiki sentrieswiki worldpediawiki
* 16:17 Reception|away: re-enabled puppet on db3
* 15:53 Reception|away: disabled puppet on db3
* 10:03 Reception|away: purge binary logs before '2017-12-29 00:00:00';

## 2017-12-27 

* 13:09 Reception|away: purge binary logs before '2017-12-27 12:00:00';

## 2017-12-23 

* 08:14 Reception123: upgraded phabricator
* 08:00 Reception123: purge binary logs before '2017-12-23 05:00:00';

## 2017-12-21 

* 16:23 Reception123: sudo -u www-data php reassignEdits.p --wiki ciptamediawiki Ivonne 06Ivonne
* 16:20 Reception123: sudo -u www-data php reassignEdits.php --wiki ciptamediawiki Francisca Ludmilla.Williyanti
* 16:20 Reception123: sudo -u www-data php reassignEdits.php --wiki ciptamediawiki Danial Danial.Indrakusuma
* 16:16 Reception123: sudo service icignabot restart

## 2017-12-20 

* 12:54 Reception123: UPDATE revision SET rev_user = '18' WHERE rev_user_text = 'Suci' AND rev_user = '0'; (ciptamediawiki)_
* 12:54 Reception123: UPDATE revision SET rev_user = '17' WHERE rev_user_text = 'Sarinah' AND rev_user = '0'; (ciptamediawiki)
* 12:54 Reception123: UPDATE revision SET rev_user = '16' WHERE rev_user_text = 'Rubby' AND rev_user = '0'; (ciptamediawiki)
* 12:53 Reception123: UPDATE revision SET rev_user = '15' WHERE rev_user_text = 'Heychael' AND rev_user = '0'; (ciptamediawiki)
* 12:52 Reception123: > UPDATE revision SET rev_user = '13' WHERE rev_user_text = 'Danial' AND rev_user = '0';  (ciptamediawiki)
* 12:52 Reception123: > UPDATE revision SET rev_user = '14' WHERE rev_user_text = 'Francisca' AND rev_user = '0'; (ciptamediawiki)
* 12:50 Reception123: > UPDATE revision SET rev_user = '12' WHERE rev_user_text = 'Hendra' AND rev_user = '0'; on ciptamediawiki
* 12:48 Reception123: created local accounts for users mentioned in T2535
* 12:00 Reception123: reception@mw1:/srv/mediawiki/w/extensions/CentralAuth/maintenance$ sudo -u www-data php migrateAccount.php --wiki metawiki --userlist /home/reception/ciptamediaaccount.txt --auto

## 2017-12-19 

* 18:02 Reception|away: sudo -u www-data php reassignEdits.php --wiki ciptamediawiki Biyan Biyanto
* 17:59 Reception|away: sudo -u www-data php reassignEditshp --wiki ciptamediawiki RachmatWahidi Rachmat04

## 2017-12-18 

* 20:03 Reception|away: depool mw3 and disable puppet on mw3

## 2017-12-17 

* 19:18 Reception123: reception@mw1:/srv/mediawiki/w/extensions/MirahezeMagic/maintenance$ sudo -u www-data php manageInactiveWikis.php --wiki metawiki --warn --close
* 19:02 Reception123: moved houseofettlingarfreyuwiki miraewiki ordiswiki tiandiwiki to db3 and dropped on db2
* 18:58 Reception123: re-enabled puppet on db3
* 18:55 Reception123: disabled puppet on db3

## 2017-12-16 

* 16:55 Reception123: repool mw1
* 16:43 Reception123: clear out /srv/mediawiki/ and reclone on mw1 due to puppet taking 2 mins+
* 16:43 Reception123: depool mw1
* 16:43 Reception123: repool mw2
* 16:38 Reception123: clear out /srv/mediawiki/ and reclone on mw2 due to puppet taking 2 mins+
* 16:30 Reception123: depool mw2
* 16:30 Reception123: repool mw3
* 16:21 Reception123: clear out /srv/mediawiki/ and reclone on mw3 due to puppet taking 2 mins+
* 16:20 Reception123: depool mw3
* 10:27 Reception123: upgraded phabricator

## 2017-12-14 

* 21:53 PuppyKun: cleared the varnish cache for maiasongcontest.miraheze.org on cp1/cp2/cp4
* 21:45 PuppyKun: ran sudo -u www-data php composer.phar update --no-dev in /srv/mediawiki/w/extensions/Wikibase/vendor on mw*
* 10:33 revi: Disable Issue/Wiki on Youtube repo on GitHub
* 10:33 revi: Disabled Wiki on CustomHeader repo on GitHub
* 10:32 revi: Disabled Wiki on GitHub CreateWiki repo
* 10:32 revi: disabled issue and wiki on GitHub ManageWiki repo (no open/closed issue)
* 10:30 revi: disabled Issues and Wiki on GitHub SSL repository

## 2017-12-13 

* 04:17 revi: sudo -u www-data php initSiteStats.php --wiki shortwikiwiki --update on mw2

## 2017-12-12 

* 20:19 Reception123: sudo -u www-data php mergeMessageFileList.php --output /srv/mediawiki/config/ExtensionMessageFiles.php --wiki test1wiki and rebuild LC on mw*
* 20:08 Reception123: made default branch on @miraheze/mediawiki REL1_30
* 02:02 PuppyKun: MariaDB [metawiki]> DELETE FROM cw_wikis WHERE wiki_dbname="embersghostsquadwiki";

## 2017-12-11 

* 19:03 Reception123: upgraded Piwik
* 18:55 Reception123: updating piwik database (/srv/piwik/console core:update)

## 2017-12-09 

* 20:36 Reception123: UPDATE revision SET rev_user = '12' WHERE rev_user_text = 'Otherunicorn' AND rev_user = '0'; on sdiywiki
* 20:35 Reception123: UPDATE revision SET rev_user = '9' WHERE rev_user_text = 'Xyzzy' AND rev_user = '0'; on sdiywiki
* 15:15 revi: Created Form for #security and disabled view/edit policy editing for Files/Paste
* 15:10 revi: created Form 9, disabled view/edit policy editing on form 8 (Phabricator Calendar)
* 15:09 Reception123: creating SQL dump for Piwik (backup); upgrading
* 10:59 Reception123: sudo -u www-data php importDump.php --wiki testarkclswiki /home/reception/arkcls-wiki-20171208.xml on mw2
* 07:11 Reception123: reception@mw1:/srv/mediawiki/w/extensions/MirahezeMagic/maintenance$ sudo -u www-data php manageInactiveWikis.php --wiki metawiki --warn --close

## 2017-12-06 

* 16:16 Reception123: restarted phab daemons
* 02:50 PuppyKun: restarted icingabot.

## 2017-12-05 

* 19:06 Reception123: reception@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php initSiteStats.php --wiki metawiki --update

## 2017-12-04 

* 17:58 Reception123: upgraded Phabricator

## 2017-12-03 

* 16:47 revi: Deploy [https://github.com/probot/autoresponder](https://github.com/probot/autoresponder) into puppet/mw-config/dns
* 16:27 Reception123: made revi GH admin (per request)
* 16:25 Reception123: added @translatewikinet to i18n repo
* 16:25 Reception123: added CreateWiki and ManageWiki repos to already created (by revi) team i18n

## 2017-11-30 

* 20:18 Reception123: ran update.php on test1wiki
* 04:08 PuppyKun: made Reception123 a github org owner

## 2017-11-29 

* 23:24 PuppyKun: granted miraheze/operations admin access to 4 repositories
* 03:50 PuppyKun: finished running all jobs
* 03:21 PuppyKun: running all jobs globally.

## 2017-11-27 

* 18:58 Reception123: added pull request + branch creations/deletions to Notifico notifications webhook for all production repos

## 2017-11-26 

* 20:13 Reception123: upgraded phabricator
* 20:08 Reception123: sudo -u www-data php importDump.php --wiki metawiki /home/reception/Wikipedia-20171125170249.xml on mw2
* 19:11 PuppyKun: finished setting up notifico webhooks and disabled the 'irc' service on all miraheze gh repos

## 2017-11-25 

* 11:50 Reception123: removed spam from cw_requests

## 2017-11-24 

* 16:55 Reception123: reception@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php rebuildall.php --wiki ashinawiki
* 16:18 Reception123: moved to db3 and dropped on db2: arefepvawiki altaussieruleswiki ballaratpubswiki bqwiki calexitwiki fcuwiki mikrodevwiki ourmxfestwiki podpediawiki sidemwiki speleowiki testwiki wikivywiki zhdelwiki
* 16:06 Reception123: re-enabled puppet on db3
* 15:52 Reception123: disabled puppet on db3

## 2017-11-23 

* 18:39 PuppyKun: Granted @miraheze/operations admin access to the miraheze/ssl repo

## 2017-11-19 

* 16:26 Reception123: sudo -u www-data cp -r /srv/mediawiki/w/extensions/SocialProfile/avatars & awards /mnt/mediawiki-static/picardwiki

## 2017-11-17 

* 15:20 Reception123: stripped AlvaroMolina 2FA from Phabricator

## 2017-11-16 

* 06:02 Reception123: sudo -u www-data php mergeMessageFileList.php --output /srv/mediawiki/config/ExtensionMessageFiles.php --wiki test1wiki and rebuild LC on mw*
* 05:58 Reception123: sudo -u www-data php importDump.php --wiki adadevelopersacademywiki /home/reception/adadevelopersacademy.wiki.Dump.xml on mw1
* 05:39 Reception123: sudo -u www-data php rebuildLocalisationCache.php --wiki test1wiki on mw*

## 2017-11-15 

* 20:24 Reception123: repool mw1
* 20:15 Reception123: refresh /srv/mediawiki on mw1
* 20:15 Reception123: depool mw1
* 20:15 Reception123: repool mw2
* 20:05 Reception123: refresh /srv/mediawiki on mw2
* 20:05 Reception123: depool mw2
* 20:05 Reception123: repool mw3
* 19:55 Reception123: refresh /srv/mediawiki on mw3
* 19:54 Reception123: depool mw3
* 19:04 Reception123: reception@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php initSiteStats.php --wiki unionnorteamericanawiki --update
* 18:41 Reception123: refreshing /srv/mediawiki on test1wiki for test

## 2017-11-14 

* 16:28 Reception123: > DELETE FROM cw_wikis WHERE wiki_dbname = 'bonobowiki'; (T2428)

## 2017-11-13 

* 19:33 Reception123: sudo -u www-data php importDump.php --wiki podpediawiki /home/reception/Stationery+Wiki-20171112165212.xml
* 19:20 Reception123: manually run jobs on mw2
* 19:03 Reception123: sudo -u www-data php importDump.php --wiki podpediawiki /home/reception/Wikipedia-20171113013816.xml on mw1
* 18:56 Reception123: reception@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php updateArticleCount.php --wiki oecumenewiki --update

## 2017-11-12 

* 20:33 Reception123: sudo -u www-data php importImages.php --wiki oecumenewiki --search-recursively /home/reception/images  on mw2
* 12:33 Reception123: sudo -u www-data php importDump.php --wiki oecumenewiki /home/reception/import1.xml
* 12:22 Reception123: sudo -u www-data php dumpBackup.php --wiki import1wiki --full --uploads > /home/reception/import1.xml on mw1

## 2017-11-11 

* 16:18 Reception123: sudo service ircrcbot restart
* 11:09 Reception123: sudo -u www-data php importDump.php --wiki sdiywiki /home/reception/sdiyinfo_w-20171111-history.xml on mw1
* 11:02 Reception123: sudo -u www-data php importImages.php --wiki sdiywiki --search-recursively /home/reception/sdiywiki on mw1
* 08:09 Reception123: upgraded phabricator
* 08:00 Reception123: made myself Piwik administrator (to be able to update)

## 2017-11-10 

* 19:34 Reception123: sudo -u www-data php dumpBackup.php --wiki metawiki --full > /home/reception/metawiki.xml on mw1
* 15:16 Reception123: moved ayrshirewiki bgowiki meregoswiki mikrodevwiki lionhearttaleswiki plasticssongcontestwiki sirikotwiki spiralwiki wikiversitywiki to db3 and dropped on db2
* 15:07 Reception123: re-enabled puppet on db3
* 14:55 Reception123: disabled puppet on db3
* 14:41 Reception123: deleted unmadewiki from CW_WIKIS and DROPPED (T2397)
* 14:39 Reception123: renamed hellointernetwiki to podpediawiki, moved files (T2397)
* 14:16 Reception123: renamed aristidewiki to pfl2wiki and moved images (T2408)

## 2017-11-09 

* 18:21 Reception|away: DROP DATABASE novayawiki;
* 18:20 Reception|away: DROP DATABASE appswiki;
* 17:35 Reception|away: DELETE FROM cw_wikis WHERE wiki_dbname = 'novayawiki';
* 06:23 Reception|away: UPDATE revision SET rev_user = '6' WHERE rev_user_text = 'Siska' AND rev_user = '0'; on ciptamediawiki
* 06:22 Reception|away: sudo -u www-data php createLocalAccount.php Siska --wiki ciptamediawiki

## 2017-11-07 

* 18:36 Reception|away: sudo -u www-data foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/maintenance/sql.php /srv/mediawiki/w/extensions/Cargo/sql/Cargo.sql
* 17:23 Reception|away: sudo -u www-data php mergeMessageFileList.php --output /srv/mediawiki/config/ExtensionMessageFiles.php --wiki test1wiki and rebuild LC on mw*

## 2017-11-06 

* 18:18 Reception|away: repool mw3
* 18:05 Reception|away: clear out /srv/mediawiki on mw3 (puppet issues)
* 18:05 Reception|away: depool mw3
* 18:05 Reception|away: repool mw2
* 17:52 Reception|away: clear out /srv/mediawiki on mw2 (puppet issues)
* 17:51 Reception|away: depool mw2

## 2017-11-05 

* 14:23 Reception123: repool mw3
* 14:20 Reception123: changed IPv6 for mw3 and reconfigured networking
* 14:20 Reception123: depool mw3
* 08:21 Reception123: > DELETE FROM cw_wikis WHERE wiki_dbname = 'appswiki'; (T2386)

## 2017-11-04 

* 12:16 Southparkfan: repooled mw2
* 12:07 Southparkfan: depooled mw2
* 11:43 Reception123: DROPPED wikis mentioned below
* 11:40 Reception123:  sudo -u www-data php /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/removeDeletedWikis.php --wiki metawiki
* 11:40 Reception123: DELETED FROM cw_wikis ttditoastmastersclubwiki txdigitalwiki ubuntuwiki umcwiki umodwiki uncomputingwiki understandingthebrainwiki unitychwiki universecppswiki upsangwiki vehsgardwiki verdenwiki versewiki vikaswiki vl6180xwiki vnreviewdbwiki waeljidwiki wakapediawiki webaspxwiki webitwiki wikia22wiki (DP)

## 2017-11-03 

* 21:18 Southparkfan: runnin varnishlog daemon on cp* for debugging purposes: varnishlog -g raw -i Backend_health -a -w /var/log/varnish/varnish-backend.log -D
* 19:00 Southparkfan: deleted all redis keys matching  "*allthetropeswiki:revisiontext*"
* 09:49 Reception123: sudo rm -rf /var/lib/puppet/reports on puppet1 (disk space running out)
* 09:45 revi: sudo -u www-data php resetUserEmail.php --wiki=metawiki Revibot revibot@kumul.pe.kr

## 2017-11-02 

* 18:19 Reception123: sudo -u www-data php mergeMessageFileList.php --output /srv/mediawiki/config/ExtensionMessageFiles.php --wiki test1wiki and rebuild LC on mw3
* 17:47 Reception123: removed /srv/mediawiki/config on mw3 (recloning)
* 17:20 Reception123: sudo -u www-data php importImages.php --wiki ciptamediawiki --search-recursively /mnt/mediawiki-static/private/temp on test1wiki
* 17:12 Reception123: sudo -u www-data php importDump.php --wiki ciptamediawiki /home/reception/dump.xml
* 17:07 Reception123: sudo -u www-data php importDump.php --wiki ciptamediawiki /home/reception/log-dump.xml on mw2
* 17:05 Reception123: sudo -u www-data php createLocalAccount.php Jayvdb --wiki ciptamediawiki
* 16:49 Reception123: deleted and dropped ciptamediawiki on db3
* 16:48 Southparkfan: killed 2 idling connections preventing database deletion on db3
* 13:53 Southparkfan: restarted ganglia-monitor on:  db2 mw2 nfs1 ns1 parsoid1
* 13:46 Reception123: sudo -u www-data php dumpBackup.php --wiki speleowiki --full --uploads > /home/reception/speleowiki02112017.xml on mw1
* 12:10 Reception123: manually run jobs on mw2
* 12:06 Reception123: clear out /srv/mediawiki and reclone on test1
* 11:58 Reception123: restarted gmetad
* 11:56 Reception123: restarted ganglia-monitor on misc2
* 11:45 Reception123: started gmetad
* 11:45 Reception123: removed cp1 from ganglia
* 11:45 Reception123: removed old bacula1 from ganglia
* 11:44 Reception123: stopped gmetad
* 11:17 Reception123: upgraded phabricator

## 2017-11-01 

* 18:49 Reception123: reception@mw2:/srv/mediawiki/w/maintenance$ sudo -u www-data php importImages.php --wiki ciptamediawiki --search-recursively /mnt/mediawiki-static/private/temp
* 18:18 Reception123: mv /home/reception/images /srv/mediawiki-static/private/ciptamediawiki on nfs1
* 17:11 Reception123: reception@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php refreshLinks.php --wiki bpwiki
* 15:56 Southparkfan: ran alter table cw_wikis add wiki_dbcluster varchar(5) default 'c1'; on cw_wikis/metawiki
* 15:08 Southparkfan: upgraded nfs1 (+ restarted ganglia-monitor)
* 14:32 Southparkfan: deleted all redis keys matching '*ciptamediawiki:jobqueue:htmlCacheUpdate*'

## 2017-10-31 

* 19:59 Reception123: sudo service ircrcbot restart
* 19:23 Reception123: sudo -u www-data php mergeMessageFileList.php --output /srv/mediawiki/config/ExtensionMessageFiles.php --wiki test1wiki and rebuild LC on mw*
* 18:36 Reception123: sudo -u www-data php rebuildLocalisationCache.php --wiki loginwiki on mw*
* 16:18 Reception123: sudo -u www-data php importDump.php --wiki ciptamediawiki /home/reception/dump.xml on mw2
* 16:17 Reception123: moved ciptamediawiki to db3 after being created
* 16:16 Reception123: re-enabled puppet on db3
* 16:12 Reception123: disabled puppet on db3
* 16:11 Reception123: DELETED FROM cw_wikis and DROPPED DATABASE ciptamediawiki; (re-importing)
* 15:28 Reception123: repool mw2
* 15:18 Reception123: clear out /srv/mediawiki on mw2 - puppet fails
* 15:18 Reception123: depool mw2
* 06:08 Reception123: re-enable puppet on mw2

## 2017-10-30 

* 17:15 Southparkfan: repooled mw2
* 17:00 Southparkfan: depool mw2 manually
* 16:34 Reception123: changed create calendar event back to "All Users"
* 16:20 Reception123: MariaDB [phabricator_calendar]> UPDATE calendar_event SET isCancelled="1" WHERE id = '11'; (ILB event)
* 14:53 Reception123: repool mw2
* 14:45 Reception123: clear out /srv/mediawiki on mw2 (causing puppet to run in 2.5 mins)
* 14:44 Reception123: depool mw2
* 14:09 Reception123: testwikiforianwiki theastraeafilecabinetwiki thecannapediawiki thecodewiki theotherterrawiki thesexiestwiki timbawiki tinkerinwiki toklandwiki totumwiki traumapediawiki truehoopwiki tstwiki mawikimaisonwiki
* 14:09 Reception123: DROPPED DATABASE historiaalternativawiki mywikiversitywiki wikisahabawiki discussionwiki tdnwikiwiki teachyogawiki testauthorprotectwiki testlalawiki
* 13:38 Reception123: moved appswiki christipediawiki ciptamediawiki diggywikipolskawiki platprojectwiki yoavfreundwiki yourosongcontestwiki to db3 and dropped on db2
* 13:32 Reception123: re-enabled puppet on db3
* 13:16 Reception123: disabled puppet on db3 (database migration)
* 11:49 Reception123: re-enabled puppet on db3
* 11:36 Reception123: disabled puppet on db3 (db migration)

## 2017-10-29 

* 19:48 Reception123: moved vandalwiki to db3, dropped vandalwiki on db2
* 19:34 PuppyKun: disabled puppet on db3
* 16:16 Reception123: created reception icinga user
* 14:59 Reception123: sudo -u www-data php /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/removeDeletedWikis.php --wiki metawiki
* 14:58 Reception123: DELETE FROM cw_wikis WHERE wiki_dbname = 'mawikimaisonwiki'; (T2353)
* 09:53 Reception123: renamed partupwiki to r2wiki (T2344)

## 2017-10-28 

* 19:51 Reception123: MariaDB [phabricator_herald]> UPDATE herald_rule SET isDisabled="1" WHERE id = '11';
* 19:51 Reception123: MariaDB [phabricator_herald]> UPDATE herald_rule SET isDisabled="1" WHERE id = '13';
* 19:51 Reception123: MariaDB [phabricator_herald]> UPDATE herald_rule SET isDisabled="1" WHERE id = '20';
* 19:51 Reception123: MariaDB [phabricator_herald]> UPDATE herald_rule SET isDisabled="1" WHERE id = '19';
* 18:57 PuppyKun: made Reception123 a phabricator instance administrator
* 18:46 PuppyKun: added reception123 to the @miraheze/operations team and removed them from @miraheze/mediawiki-admins and @miraheze/puppet-users
* 18:31 PuppyKun: rm'd the oldest binary log on db2 and edited the log index manually, unable to start server with 0 bytes df

## 2017-10-27 

* 14:55 Reception123: DELETED FROM cw_wikis tdnwikiwiki teachyogawiki testauthorprotectwiki testlalawiki testwikiforianwiki theastraeafilecabinetwiki thecannapediawiki thecodewiki theotherterrawiki thesexiestwiki timbawiki tinkerinwiki toklandwiki totumwiki traumapediawikitruehoopwiki tstwiki (DP)
* 14:15 Reception123: sudo -u www-data cp -r /srv/mediawiki/w/extensions/SocialProfile/avatars & awards /mnt/mediawiki-static/puzzlewiki
* 06:00 Reception123: manually running jobs on test1 and mw2
* 06:00 Reception123: restarted jobrunner (>10k jobs)

## 2017-10-26 

* 21:18 PuppyKun: super hackily renewed the phab.miraheze.wiki crt again

## 2017-10-25 

* 18:34 Reception123: sudo -u www-data php importDump.php --wiki vandalwiki /home/reception/kowiki-latest-pages-articles.xml on mw2

## 2017-10-23 

* 12:30 Reception123: /srv/mediawiki/w/extensions/MirahezeMagic/maintenance$ sudo -u www-data php manageInactiveWikis.php --wiki metawiki --warn --close

## 2017-10-21 

* 12:18 Reception123: sudo -u www-data cp -r /srv/mediawiki/w/extensions/SocialProfile/avatars & awards /mnt/mediawiki-static/unmadewiki
* 12:02 Reception123: sudo -u www-data cp -r /srv/mediawiki/w/extensions/SocialProfile/avatars & awards /mnt/mediawiki-static/peopleshararamwiki

## 2017-10-16 

* 17:37 Reception123: manually running jobs on mw2; test1 down
* 15:36 PuppyKun: submitted ticket with RN regarding test1/misc1 connectivity
* 04:57 Reception123: sudo -u www-data php importDump.php --wiki puzzlewiki /home/reception/Wikipedia-20171015235107.xml on mw2

## 2017-10-15 

* 07:42 Reception123: sudo -u www-data php dumpBackup.php --wiki rootsandlimbswiki --full --uploads --include-files > /home/reception/rootsandlimbswiki15102017.xml on mw1

## 2017-10-13 

* 18:36 Southparkfan: moved puppet_hosts.cfg and puppet_services.cfg to other locations. if you let them regenerate, old hosts will be purged
* 16:42 Southparkfan: purged all binlogs older than 5 days (db2)

## 2017-10-12 

* 21:53 PuppyKun: reniced phabricator daemon to normal priority
* 21:53 PuppyKun: Marked activity "reindex" as completed.
* 21:40 PuppyKun: reniced all phabricator daemon processes
* 21:36 PuppyKun: queued 20,612 document(s) for background indexing [phabricator full-text search index]
* 21:32 PuppyKun: rebuilding the phabricator full-text search indexs

## 2017-10-10 

* 15:46 Reception|away: sudo -u www-data php /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/removeDeletedWikis.php --wiki metawiki
* 15:45 Reception|away: > DELETE FROM cw_wikis WHERE wiki_dbname = 'discussionwiki'; (request)
* 15:43 Reception|away: > DELETE FROM cw_wikis WHERE wiki_dbname = 'wikisahabawiki';
* 15:42 Reception|away: > DELETE FROM cw_wikis WHERE wiki_dbname = 'mywikiversitywiki'; (request)

## 2017-10-08 

* 21:50 PuppyKun: restarted icingabot and adminbot on misc1
* 16:35 Reception123: restarted jobrunner on test1
* 16:30 Reception123: manually run jobs on mw2
* 16:29 Reception123: running manually sudo -u www-data foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/maintenance/runJobs.php on mw1

## 2017-10-07 

* 21:26 PuppyKun: upgraded phab
* 21:23 PuppyKun: updating phab
* 13:50 Reception123:  reception@mw2:/srv/mediawiki/w/maintenance$ sudo -u www-data php importDump.php --wiki wikisahabawiki /home/reception/[NON-ASCII characters]-20171007134137.xml
* 05:59 Reception123: DELETE FROM cw_wikis WHERE wiki_dbname = 'historiaalternativawiki'; (T2257)

## 2017-10-05 

* 17:41 Southparkfan: repooled mw1
* 17:31 Southparkfan: regenerated all puppet certs
* 15:57 Southparkfan: depooled mw1 for investigation
* 15:54 Southparkfan: depooled mw1 for cp4 traffic
* 13:52 PuppyKun: ran puppet on mw1 and ensured static remounted
* 13:50 PuppyKun: booting mw1 in solus
* 13:33 PuppyKun: running all jobs using test1, reniced the jobs process

## 2017-10-04 

* 19:04 Southparkfan: re-installing bacula1
* 18:14 Southparkfan: restarted jobchron + jobrunner on mw1
* 18:09 Southparkfan: upgraded nginx to 1.12.1
* 14:16 Southparkfan: purge binary logs before '2017-09-30 00:00:00'; on db3
* 13:51 Southparkfan: dropped some wikis: [https://phabricator.miraheze.org/T2258](https://phabricator.miraheze.org/T2258)

## 2017-10-02 

* 05:58 labster: DELETE FROM allthetropeswiki.logging WHERE log_type = 'patrol' AND log_timestamp < '20170301000000';

## 2017-10-01 

* 05:19 Reception123: DELETE FROM cw_wikis WHERE wiki_dbname = 'modularwiki'; (temporary delete, as database was (wrongly) dropped and is causing login issues)

## 2017-09-30 

* 14:11 PuppyKun: dropped modularwiki and yugiohtestwiki databases
* 14:08 PuppyKun: chowned deleted.dblist to www-data
* 14:06 PuppyKun: killed the import job on mw2
* 06:02 Reception123: restarted jobrunner and manually running jobs on mw1/mw2
* 05:44 Reception123: sudo -u www-data php /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/removeDeletedWikis.php --wiki metawiki
* 05:43 Reception123: DELETE FROM cw_wikis starsetonlinewiki startupfiascoswiki stigwiki stormfmwiki suchubtestprivatewiki swiftwiki sylwiki syuksyukwiki tallermultimedialujanwiki tasakaalwiki (DP)

## 2017-09-29 

* 17:27 Reception123: sudo -u www-data php /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/removeDeletedWikis.php --wiki metawiki
* 17:26 Reception123: DELETE FROM cw_wikis satalinmlwiki satalinwiki scribexwiki sebkbwiki seclientwiki sertwiki sextherapywiki sfgwiki sfyimbywiki sharethisbookwiki shifuwiki shojowiki  siggeneratorwiki siliconwiki sinoustalkwiki sipmwiki sistemasgrupo1wiki sjuhabitatwiki smbxwikiwiki somhandbookwiki soswikiwiki ssbarrotawiki (DP)
* 17:09 Reception123: sudo -u www-data php /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/removeDeletedWikis.php --wiki metawiki
* 17:09 Reception123: DELETE FROM cw_wikis projecttaleswiki prueba2016wiki psychgradwiki purpanrangueiluswiki raxincwiki redercjwiki rocketleaguequebecwiki rpcharacterswiki rubywikiwiki saad2039wiki sadkidwikiwiki sanonstepguidewiki (DP)
* 16:32 Reception123: restart import --wiki yugiohtestwiki /home/ndkilla/yugioh_pages_current.xml on mw2
* 15:55 Reception123: reception@mw1:/srv/mediawiki/w/extensions/MirahezeMagic/maintenance$ sudo -u www-data php manageInactiveWikis.php --wiki metawiki --warn --close

## 2017-09-27 

* 15:10 Reception123: sudo -u www-data cp -r /srv/mediawiki/w/extensions/SocialProfile/avatars + awards /mnt/mediawiki-static/appswiki
* 00:45 PuppyKun: restarted dead import job on mw2

## 2017-09-26 

* 02:39 PuppyKun: running importdump --wiki yugiohtestwiki

## 2017-09-25 

* 18:43 Southparkfan: ran purgeParserCache.php on appswiki and optimized appswiki's objectcache table
* 17:30 Southparkfan: dropped part3wiki pbmwiki pbxwiki pdswiki peoplecanprogramwiki perpuswiki philmontwiki pillewiki plasticswiki pmwikiwiki porpwiki prarchivewiki programmingreferencewiki projectkiwiwiki westmarcheswiki applewikiwiki lothuailethwiki

## 2017-09-24 

* 22:53 PuppyKun: restarted #miraheze-feed bot
* 09:32 Reception123: sudo -u www-data php dumpBackup.php --wiki christianmusicwiki --full --uploads --include-files > /home/reception/christianmusic.xml && sudo -u www-data php importDump.php --wiki christianmusictempwiki /home/reception/christianmusic.xml on mw2
* 05:52 Reception123: sudo -u www-data php dumpBackup.php --wiki linenwiki --full --uploads --include-files > /home/reception/linenwiki24092017.xml on mw1

## 2017-09-23 

* 06:24 Reception123: sudo -u www-data php importDump.php --wiki appswiki /home/reception/Wikipedia-20170920193243.xml

## 2017-09-20 

* 18:11 Reception|away: restarted jobrunner and manually running jobs
* 17:38 Reception|away: sudo -u www-data php importImages.php --wiki yoavfreundwiki --search-recursively /home/reception/yoavfreund on mw2
* 16:50 Reception|away: running jobs on mw2 to alleviate jobqueue
* 16:20 Reception|away: running jobs on mw2 to alleviate jobqueue
* 14:33 Reception|away: sudo -u www-data php importDump.php --wiki ciptamediawiki /home/reception/ciptamediawiki.xml
* 14:23 Reception|away: sudo -u www-data php importDump.php --wiki christianmusicwiki /home/reception/christianmusic_pages_full.xml on mw1
* 05:20 Reception|away: sudo -u www-data php importDump.php --wiki yoavfreundwiki /home/reception/dump.xml on mw1

## 2017-09-18 

* 16:57 Reception123: sudo -u www-data php /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/removeDeletedWikis.php --wiki metawiki
* 16:56 Reception123: > DELETE FROM cw_wikis WHERE wiki_dbname = 'lothuialethwiki';
* 16:55 Reception123: > DELETE FROM cw_wikis WHERE wiki_dbname = 'applewikiwiki';

## 2017-09-16 

* 08:19 revi: sudo -u www-data php importDump.php --wiki=metawiki /home/revi/import.xml

## 2017-09-15 

* 20:01 PuppyKun: ensured [translation] configuration changes applied on mw*
* 19:56 PuppyKun: forced puppet runs on mw* to immediately apply configuration changes

## 2017-09-10 

* 17:05 John: rebuilding phabricator search index for new search engine
* 17:03 John: upgraded phabricator
* 16:27 John: upgraded parsoid

## 2017-09-08 

* 16:56 John: DROP DATABASE centralauth on db2

## 2017-09-02 

* 16:45 Southparkfan: deleting all thumbs of tmewiki to free up space
* 15:51 Reception123: sudo -u www-data php dumpBackup.php --wiki cpudevwiki --full --uploads --include-files > /home/reception/cpudev02092017.xml on mw1
* 12:59 Reception123: removed old dumps
* 12:56 Reception123: removed zgradetenniswiki static file (wiki deleted a few months ago)
* 10:03 Reception123: sudo -u www-data php mergeMessageFileList.php --output /srv/mediawiki/config/ExtensionMessageFiles.php --wiki test1wiki  and rebuild LC on mw*/test1

## 2017-09-01 

* 16:42 Reception123: re-import bpwiki images
* 05:26 Reception123: updated ExtensionMessagesFiles.php and rebuild LC on mw1 and test1 (for some reason mw2 is the only one to have a PHP fatal with another unrelated extension)

## 2017-08-31 

* 16:51 Reception123: sudo -u www-data php rebuildLocalisationCache.php --wiki test1wiki on mw*/test1wiki
* 16:44 Reception123: re-enabled puppet on mw*
* 16:25 Reception123: disabled puppet on mw* to test extension message file change

## 2017-08-30 

* 17:57 Reception123: sudo -u www-data php /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/removeDeletedWikis.php --wiki metawiki
* 17:56 Reception123: DELETE FROM cw_wikis WHERE wiki_dbname = 'westmarcheswiki'
* 16:23 Reception123: sudo -u www-data php dumpBackup.php --wiki westmarcheswiki --full --uploads --include-files > /home/reception/westmarcheswiki30082017.xml on mw2

## 2017-08-29 

* 14:19 John: runJobs.php on mw2 to alleviate job queue
* 10:18 Reception123: sudo -u www-data php rebuildLocalisationCache.php --wiki extloadwiki on mw*

## 2017-08-28 

* 13:46 Southparkfan: depool mw1

## 2017-08-27 

* 22:08 PuppyKun: enabled macfan4000's phabricator account at request

## 2017-08-26 

* 02:00 PuppyKun: restarted icingabot

## 2017-08-25 

* 12:39 John: destroyed E42
* 12:35 Reception123: sudo -u www-data php dumpBackup.php --wiki allthetropeswiki --full --uploads --include-files > /home/reception/allthetropeswiki25082017.xml on mw2
* 07:02 Reception123: populated content model for Flow on nenawikiwiki

## 2017-08-24 

* 12:48 Reception123: sudo -u www-data php rebuildLocalisationCache.php --wiki extloadwiki on mw*

## 2017-08-23 

* 17:45 Reception123: ran patch-moderation.sql and patch-moderation_block.sql on all wikis
* 17:25 Reception123:  sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildLocalisationCache.php --wiki extloadwiki on mw*
* 13:26 John: deleting volume STATIC-0003 (for some reason two backups were made within an hour of each other which blocks all backups until September)
* 05:43 Reception123: attached unattached account listed at [https://phabricator.miraheze.org/P36](https://phabricator.miraheze.org/P36)

## 2017-08-22 

* 16:45 Southparkfan: upgraded mw2
* 08:54 Reception123: sudo -u www-data php /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/removeDeletedWikis.php --wiki metawiki
* 08:53 Reception123: DELETED FROM cw_wikis part3wiki pbmwiki pbxwiki pdswiki  peoplecanprogramwiki perpuswiki philmontwiki pillewiki  plasticswiki pmwikiwiki  porpwiki prarchivewiki programmingreferencewiki projectkiwiwiki (DP)
* 06:45 Reception123: ran CentralNotice.sql on metawiki

## 2017-08-21 

* 19:21 Reception123: sudo -u www-data php dumpBackup.php --wiki claneuphoriawiki --full --uploads --include-files > /home/reception/claneuphoriawiki21082017.xml on mw1
* 17:49 John: ran migrateAccount.php for all users of savagewikiwiki
* 17:05 John: depool mw1 for /srv/mediawiki/ clear out
* 08:26 Reception123: reception@mw1:/srv/mediawiki/w/extensions/MirahezeMagic/maintenance$ sudo -u www-data php manageInactiveWikis.php --wiki metawiki --warn --close

## 2017-08-16 

* 17:42 John: restarted mysql on db3
* 17:38 John: restarted dovecot on misc1

## 2017-08-15 

* 14:32 John: deleted several wikis from cw_wikis which were never deleted but marked as deleted
* 00:50 John: deleted oneclanwiki from cw_wikis. wiki was in deleted.dblist but wasn't deleted when added

## 2017-08-14 

* 22:50 John: made 3 tasks public in phab from history
* 20:24 John: attaching all accounts on all wikis
* 19:49 John: deleting wikis in deleted.dblsit
* 19:36 John: upgrade phabricator
* 13:17 John: chown root:puppet /etc/puppet/private resolves T1949

## 2017-08-13 

* 22:51 PuppyKun: removed Reception123 as an admin of the @miraheze/ssl repo, added @miraheze/Operations to the ssl repo with push access
* 22:37 John: put mw2 back in prod
* 22:31 John: cleared binlogs on db2
* 22:29 John: made REL1_29 the default branch in GH
* 22:02 John: switched depools. quickly.
* 18:59 John: depooled mw1
* 17:39 John: disabled puppet agents on mw*
* 14:32 John: running ALTERs on all wikis

## 2017-08-10 

* 05:44 Reception123: removed spam from cw_requests

## 2017-08-09 

* 15:09 Reception123: ran update.php on test1wiki again (dbquerry error when logging in)
* 04:59 Reception123: ran removedeletedwikis script
* 04:58 Reception123: DELETE FROM cw_wikis WHERE wiki_dbname = 'cosmoswiki';
* 01:09 PuppyKun: deleted tufuswiki from cw_wikis (abusive)

## 2017-08-08 

* 07:03 Reception123: reception@mw2:/srv/mediawiki/w/maintenance$ sudo -u www-data php importDump.php --wiki worlduniversityandschoolwiki /home/reception/worlduniversity_pages_full.xml

## 2017-08-07 

* 17:48 Reception123: disabled puppet on test1 for live hacks

## 2017-08-06 

* 12:59 Reception123: update.php on test1wiki

## 2017-08-03 

* 18:54 Reception123: sudo -u www-data php /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/removeDeletedWikis.php --wiki metawiki
* 18:52 Reception123: DELETE FROM cw_wikis WHERE wiki_dbname = 'modelusgovwiki'; (requested)

## 2017-08-02 

* 16:02 Southparkfan: re-enabled puppet on mw*

## 2017-08-01 

* 14:57 Reception123: sudo -u www-data php rebuildLocalisationCache.php --wiki extloadwiki on mw*

## 2017-07-31 

* 15:49 Reception123: created puppet-users team (should've been done before)

## 2017-07-30 

* 15:05 Reception123: cleared /tmp on mw2
* 14:05 PuppyKun: told ramnode it's okay to shutdown test1.mh.o to enable nfs setup

## 2017-07-29 

* 20:01 PuppyKun: apt install build-essential on test1
* 19:54 PuppyKun: disabled root logins on db3 and re-enabled puppet agent
* 19:51 PuppyKun: (niced) recalculating disk usage on db*
* 19:46 PuppyKun: dropped databases (piwik, thelonsdalebattalionwiki, bpwiki, bigforestwiki) after moving them to db3
* 19:19 PuppyKun: dumping bpwiki
* 19:10 PuppyKun: apt install texvc on test1.mh.o
* 18:19 PuppyKun: ensured the removal of corey's shell account from mw*
* 18:10 PuppyKun: copying piwik database dump to db3
* 15:44 PuppyKun: purged binary logs on db2 freeing 4% disk space
* 05:22 Reception123: restarted jobrunner and manually running jobs

## 2017-07-27 

* 16:37 Reception123: reception@mw2:/srv/mediawiki/w/maintenance$ sudo -u www-data php populateCategory.php --wiki thelonsdalebattalionwiki

## 2017-07-26 

* 22:46 PuppyKun: reloaded apache2 config on misc1 to test a live hack
* 08:40 Reception123: sudo -u www-data php /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/removeDeletedWikis.php --wiki metawiki
* 08:39 Reception123: > DELETE FROM cw_wikis WHERE wiki_dbname = 'rimworldwiki'; (request)

## 2017-07-25 

* 09:12 Reception123: sudo -u www-data php dumpBackup.php --wiki thelonsdalebattalionwiki --full --uploads --include-files > /home/reception/thelonsdalebattalionwiki25072017.xml on mw2
* 06:48 Reception123: zip bigforest images to static/dumps
* 06:42 Reception123: sudo -u www-data php dumpBackup.php --wiki bigforestwiki --full --uploads --include-files > /home/reception/bigforestwiki25072017.xml on mw2

## 2017-07-24 

* 11:02 Reception123: sudo -u www-data php dumpBackup.php --wiki aerosswiki --full > /home/reception/aerosswiki.xml and sudo -u www-data php importDump.php --wiki magnaversewiki /home/reception/aerosswiki.xml on mw1
* 06:10 Reception123: sudo -u www-data php rebuildLocalisationCache.php --wiki extloadwiki on mw*

## 2017-07-23 

* 07:39 Reception123: sudo -u www-data php dumpBackup.php --wiki linenwiki --full --uploads --include-files > /home/reception/linenwiki23072017.xml on mw1

## 2017-07-22 

* 16:36 Reception123: sudo -u www-data php /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/removeDeletedWikis.php --wiki metawiki

## 2017-07-21 

* 07:53 Reception123: lgproduktsupportwiki lucilekbtwiki minecraftaddonswiki mylogicwiki mywiki ndnwiki oneclanwiki orbiswikiwiki (DP)
* 07:53 Reception123: (before previous script obviously) DELETED FROM cw_wikis dragonwiki dsiguidewiki elo131wiki englishlanguagewikiwiki evlerwiki fcswiki filowiki  fluxwiki h2751903wiki hendrickswiki hivemindwiki hrodrwiki humanumwiki jakeperswiki joongs14wiki juliesnoteswiki
* 07:52 Reception123: sudo -u www-data php /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/removeDeletedWikis.php --wiki metawiki

## 2017-07-20 

* 01:27 PuppyKun: changed the solus vm password, resolving T1831
* 00:23 PuppyKun: moved /etc/icinga/config/puppet_services.cfg to a backup file then ran puppet to regenerate the list of services

## 2017-07-19 

* 15:52 Reception123: reception@mw1:/srv/mediawiki/w/extensions/CentralAuth/maintenance$ sudo -u www-data php migrateAccount.php --wiki bpwiki --username "Crisco 1492" --auto
* 15:48 Reception123: ^Creception@mw1:/srv/mediawiki/w/extensions/CentralAuth/maintenance$ sudo -u www-data php migrateAccount.php --wiki bpwiki --username Kumincir --auto
* 15:47 Reception123: reception@mw1:/srv/mediawiki/w/extensions/CentralAuth/maintenance$ sudo -u www-data php migrateAccount.php --wiki bpwiki --username Cahyo --auto
* 08:46 Reception123: sudo -u www-data php rebuildLocalisationCache.php --wiki extloadwiki on mw*

## 2017-07-18 

* 02:35 PuppyKun: restarted jobchron on mw1
* 02:34 PuppyKun: ndkilla@mw1: foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/maintenance/runJobs.php (>2400 jobs)
* 02:19 PuppyKun: restarted icingabot

## 2017-07-17 

* 12:34 PuppyKun: granted mw-admins push access to @miraheze/Math

## 2017-07-16 

* 23:37 PuppyKun: ndkilla@db2 purged binlogs
* 22:54 PuppyKun: ndkilla@db2 sudo -u mysql /usr/bin/nice -n19 /usr/bin/du -sh /srv/mariadb/* > du.output
* 22:52 PuppyKun: ndkilla@cp1 sudo -u www-data /usr/bin/nice -n19 /usr/bin/du -sh /srv/mediawiki-static/* > du.output
* 20:05 PuppyKun: deleted static content for dropped databases
* 20:00 PuppyKun: dropped 17huberkwiki 2l1v3swiki 5awiki adwiki aevumkathwiki anatoruswiki anet3dwiki asellwiki ashishwiki boss429wiki buswikiwiki casualtywiki cats11thstreetwiki cerhisdevwiki chgkirkwiki citywiki criptanawiki csstestwiki datawiki daudtwikiwiki dh8257wiki dndwiki nationstateswiki conworldwiki
* 20:00 PuppyKun: dropped teachingsecondswiki telegramvtwiki tennisdbwiki testrbcmdoewiki thamilwiki theseabeneathwiki tiddlywikiwiki tumblenetwiki videogameswiki vifakswiki vvwiki warbinwiki wcwiki weeglifewiki wethepediawiki wijoumedwiki wikislandswiki wikixrlianwiki xyzwiki yourovisionwiki zaffwltestwiki zonwiki zuersnetwiki zvtwiki wiki1776wiki
* 19:18 PuppyKun: ndkilla@db3: restarted bacula-fd
* 15:46 PuppyKun: upgraded phabricator
* 15:44 PuppyKun: upgrading phabricator
* 15:32 PuppyKun: ndkilla@mw1 restarted jobrunner and manually running all jobs [job queue 5500+]
* 01:47 PuppyKun: ndkilla@misc1 ran phabricator/bin/auth verify [redacted email]

## 2017-07-15 

* 08:24 Reception123: restarted php5-fpm on mw*
* 06:27 Reception123: sudo -u www-data php rebuildLocalisationCache.php --wiki extloadwiki on mw*

## 2017-07-13 

* 11:25 Reception123: sudo -u www-data php /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/removeDeletedWikis.php --wiki metawiki (readded superfighterswiki to deleted.dblist)
* 08:47 Reception123: emptied /tmp on mw2

## 2017-07-10 

* 23:59 PuppyKun: dropped databases and removed static content for testwikiwiki sentinelwiki sslabswiki superfighterswiki tachyonwiki tdwebstewiki
* 23:26 PuppyKun: dropped databases and removed static content for revisionhistorymodelwiki rhythmwiki robloxscripterswiki rudinwiki ruvowikiwiki sambodiawiki sample1113wiki sbbehzadiwiki scatranslatorswiki scbcwiki sdeuropewiki
* 23:25 PuppyKun: dropped databases and removed static content for planeteswiki popupwiki professionaldevelopmentwiki rafambienterowiki rainfallwiki rcprobusitwiki readingclubwiki reizowiki resetwiki
* 21:58 PuppyKun: dropped databases and removed static content for wikirailwiki omwiki openconstitutionwiki passtestwiki pavelwiki pittawiki
* 21:48 PuppyKun: deleted libertywiki from cw_wikis and ran removeDeletedWikis.php (since I created a local account again)
* 21:38 PuppyKun: created an xml dump and static content zip of libertywiki and saved it in /home/revi on mw1
* 21:32 PuppyKun: recreated the cw_wikis entry for libertywiki (T1987#37042)
* 21:19 PuppyKun: purged puppet reports from puppet1 and forced recheck of puppet1 diskspace

## 2017-07-09 

* 16:16 Reception123: sudo -u www-data php /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/removeDeletedWikis.php --wiki metawiki
* 16:14 Reception123: > DELETE FROM cw_wikis WHERE wiki_dbname = 'conworldwiki' (requested)
* 16:14 Reception123: > DELETE FROM cw_wikis WHERE wiki_dbname = 'nationstateswiki' (requested)
* 14:51 PuppyKun: restarted icingabot

## 2017-07-08 

* 19:42 PuppyKun: switched phab from local branch "test" to stable, tracking origin/stable
* 19:42 PuppyKun: upgraded phabricator
* 19:40 PuppyKun: upgrading phabricator

## 2017-07-07 

* 06:50 Reception123: sudo -u www-data php /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/removeDeletedWikis.php --wiki metawiki
* 06:48 Reception123: DELETED FROM cw_wikis cats11thstreetwiki cerhisdevwiki chgkirkwiki citywiki criptanawiki csstestwiki datawiki daudtwikiwiki dh8257wiki dndwiki (DP)
* 06:40 Reception123: DELETED FROM cw_wikis 17huberkwiki 2l1v3swiki 5awiki adwiki aevumkathwiki anatoruswiki anet3dwiki asellwiki ashishwiki  boss429wiki  buswikiwiki casualtywiki (DP)
* 05:59 Reception123: /srv/mediawiki/w/extensions/Echo/maintenance$ sudo -u www-data php processEchoEmailBatch.php --wiki [multiple]

## 2017-07-03 

* 06:18 Reception123: reception@mw2:/srv/mediawiki/w/maintenance$ sudo -u www-data php importDump.php --wiki bigforestwiki /home/reception/Jayu_Backup.xml
* 06:11 Reception123: sudo -u www-data php dumpBackup.php --wiki jayuwikiwiki --full --uploads --include-files > /home/reception/jayuwiki03072017.xml on mw2

## 2017-07-02 

* 09:05 Reception123: sudo -u www-data php rebuildLocalisationCache.php --wiki extloadwiki on mw*

## 2017-07-01 

* 18:48 Reception123: reception@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php importImages.php --wiki geomasterywiki --search-recursively /mnt/mediawiki-static/jjmodwiki
* 17:09 Reception123: reception@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php importDump.php --wiki geomasterywiki /home/reception/jjmodwiki2.xml
* 17:08 Reception123: reception@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php dumpBackup.php --wiki jjmodwiki --full --uploads --include-files > /home/reception/jjmodwiki2.xml

## 2017-06-30 

* 20:43 PuppyKun: messing with /etc/puppet/ssl-keys perms on puppet1
* 13:05 Reception123: reception@mw1:/srv/mediawiki/w/extensions/Flow/maintenance$ sudo -u www-data php convertNamespaceFromWikitext.php Overleg --wiki christipediawiki
* 12:15 Reception123: /srv/mediawiki/w/maintenance$ sudo -u www-data php populateContent                                                                                        Model.php [different settings] --wiki christipediawiki

## 2017-06-29 

* 10:26 Reception123: removed 2016 dumps from static/dumps (process was "remove after 6 months" and more have passed)
* 10:08 Reception123: copied allthetropes from mediawiki-static and zipped for backup
* 08:36 Reception123: /srv/mediawiki/w/maintenance$ sudo -u www-data php rebuildLocalisationCache.php --wiki extloadwiki on mw*
* 08:16 Reception123: /srv/mediawiki/w/maintenance$ sudo -u www-data php rebuildLocalisationCache.php --wiki extloadwiki on mw*
* 07:38 Reception123: /srv/mediawiki/w/maintenance$ sudo -u www-data php rebuildLocalisationCache.php --wiki extloadwiki on mw*
* 07:25 Reception123: sudo -u www-data php /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/removeDeletedWikis.php --wiki metawiki
* 07:25 Reception123: DELETE FROM cw_wikis WHERE wiki_dbname = 'simonjonwiki'; (T1943)
* 07:23 Reception123: DELETE FROM cw_wikis WHERE wiki_dbname = 'wiki1776wiki'; (T1944)
* 07:20 Reception123: sudo -u www-data php dumpBackup.php --wiki setonwiki --full > /home/reception/setonwiki29062017.xml on mw1

## 2017-06-28 

* 19:20 Reception123: copy static files from jjmodwiki to geomasterywiki
* 17:43 Reception123: dumped backup and imported from jjmodwiki to geomasterywiki
* 14:00 Reception123: sudo -u www-data php importDump.php --wiki kingkillerwiki /home/reception/nameofthewind_pages_full.xml on mw2

## 2017-06-27 

* 18:30 Reception123: reception@mw2:/srv/mediawiki/w/maintenance$ sudo -u www-data php initSiteStats.php --wiki isvwiki --update
* 05:53 Reception123: reception@mw1:/srv/mediawiki/w/extensions/MirahezeMagic/maintenance$ sudo -u www-data php manageInactiveWikis.php --wiki metawiki --warn --close
* 03:40 PuppyKun: ndkilla@mw1 extensions/CentralAuth/Maintenance migrateAccount --auto DelaineArnold and createLocalAccount --wiki loginwiki DelaineArnold

## 2017-06-26 

* 21:16 PuppyKun: ndkilla@misc1: Stripped totp authentication from NDKilla's phabricator account
* 08:12 revi: revi@mw2:/srv/mediawiki/w/maintenance$ sudo -u www-data php dumpBackup.php --wiki bigforestwiki --full > /home/revi/bigforestwiki20170626.xml
* 02:52 PuppyKun: restarted rpcbind and nfs-kernel-server on cp1 after mw* refused to mount nfs

## 2017-06-25 

* 20:08 PuppyKun: restarted mw* via terminal
* 20:07 PuppyKun: kill -9'd 3 procs on mw1 and 2 procs on mw2 after puppet hung
* 01:36 PuppyKun: ndkilla@mw2 refreshLinks.php --wiki ildrilwiki

## 2017-06-24 

* 13:54 Reception123: sudo -u www-data php updateArticleCount.php --wiki ildrilwiki on mw1

## 2017-06-21 

* 21:34 PuppyKun: purged binary logs on db2 freeing 5% disk space ;-;

## 2017-06-20 

* 16:49 Reception123: wiped /tmp on mw2
* 00:25 PuppyKun: forced view and edit policies for T1925, T1926, T1928, T1929

## 2017-06-18 

* 17:26 Reception123: created ssl repo on GitHub
* 15:14 Reception123: sudo -u www-data php importDump.php --wiki bigforestwiki /home/reception/Jayu_Upload.xml on mw2

## 2017-06-17 

* 18:17 PuppyKun: rebooting puppet1 [host offline]

## 2017-06-15 

* 18:41 Southparkfan: before previous action, stopped php5-fpm on mw2
* 18:40 Southparkfan: restarted php5-fpm on mw1

## 2017-06-13 

* 20:25 PuppyKun: upgraded phabricator
* 20:22 PuppyKun: upgrading phabricator

## 2017-06-12 

* 19:08 imbophil: sudo -u www-data php rebuildLocalisationCache.php --wiki extloadwiki on MW1 and MW2

## 2017-06-10 

* 22:17 labster: restarted jobrunner
* 07:30 Reception123: manually run jobs an all wikis (not running for 1 hour+)

## 2017-06-09 

* 16:02 Reception123: restarted jobrunner
* 16:02 Reception123: run jobs for all wikis (jobrunner not working, very slow)
* 15:59 Reception123: manually ran jobs for sterbalfamilyrecipeswiki (slow jobrunner)

## 2017-06-08 

* 18:12 Reception|away: removed spam from cw_requests
* 16:56 imbophil: sudo -u www-data php rebuildLocalisationCache.php --wiki extloadwiki on MW1 and MW2
* 16:22 imbophil: sudo -u www-data php rebuildLocalisationCache.php --wiki extloadwiki on MW1 and MW2

## 2017-06-07 

* 16:34 Reception|away: removed spam from cw_requests

## 2017-06-06 

* 17:38 Reception|away: sudo -u www-data php updateArticleCount.php --wiki wiki1776wiki
* 17:38 Reception|away: sudo -u www-data php updateSpecialPages.php --wiki wiki1776wiki

## 2017-06-05 

* 18:37 Reception123: sudo -u www-data php rebuildLocalisationCache.php --wiki extloadwiki on mw*
* 09:01 Reception123: UPDATE revision SET rev_user = '9' WHERE rev_user_text = 'Biyanto' AND rev_user = '0'; on bpwiki
* 05:40 Reception123: sudo -u www-data php attachAccount.php --wiki bpwiki --userlist /home/reception/bp.txt
* 05:25 Reception123: removed spam from cw_requests

## 2017-06-04 

* 19:34 PuppyKun: root@mw1:/mnt/mediawiki-static# sudo -u www-data mv omnipediawiki omniversaliswiki
* 19:34 PuppyKun: ndkilla@db3 update centralauth.localuser and centralauth.localnames per db rename
* 19:34 PuppyKun: ndkilla@db2: MariaDB [metawiki]> UPDATE cw_wikis SET wiki_dbname="omniversaliswiki" WHERE wiki_dbname="omnipediawiki";
* 19:33 PuppyKun: ndkilla@db2: dumped and imported omnipediawiki to omniversaliswiki
* 19:22 PuppyKun: ensured puppet runs on mw* for readonly omnipediawiki
* 17:30 Reception123: sudo -u www-data php rebuildLocalisationCache.php --wiki extloadwiki on mw*

## 2017-06-03 

* 16:25 Reception123: sudo -u www-data php /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/removeDeletedWikis.php --wiki metawiki
* 16:24 Reception123: DELETED FROM cw_wikis warbinwiki wcwiki weeglifewiki wethepediawiki wijoumedwiki wikislandswiki wikixrlianwiki xyzwiki yourovisionwiki zaffwltestwiki zonwiki zuersnetwiki zvtwiki (DP)
* 16:13 Reception123: tumblenetwiki videogameswiki vifakswiki vvwiki (DP)
* 16:13 Reception123: DELETED FROM cw_wikis sentinelwiki sslabswiki superfighterswikki tachyonwiki tdwebstewiki teachingsecondswiki telegramvtwiki tennisdbwiki testrbcmdoewikithamilwiki theseabeneathwikki tiddlywikiwiki
* 10:15 Reception123: reception@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php updateSpecialPages.php --wiki bpwiki

## 2017-06-02 

* 22:05 PuppyKun: ndkilla@db3 MariaDB [phabricator_maniphest]> UPDATE maniphest_task SET editPolicy="users" WHERE id BETWEEN 1852 AND 1859;
* 22:00 PuppyKun: ndkilla@db3 MariaDB [phabricator_maniphest]> UPDATE maniphest_task SET editPolicy="public" WHERE id BETWEEN 1852 AND 1859;
* 21:33 PuppyKun: ndkilla@db3 MariaDB [phabricator_maniphest]> UPDATE maniphest_task SET viewPolicy="public" WHERE id BETWEEN 1852 AND 1859;
* 16:07 Reception123: removed spam from cw_requests as blocking queue

## 2017-06-01 

* 20:16 Southparkfan: restart ganglia-monitor on mw1 (after upgrade)
* 15:43 Southparkfan: ran core:archive for piwik

## 2017-05-29 

* 18:20 Reception123: sudo -u www-data php /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/removeDeletedWikis.php --wiki metawiki
* 18:20 Reception123: > DELETE FROM cw_wikis WHERE wiki_dbname = 'testwikiwiki'; (LTA)
* 15:34 Southparkfan: deleted Piwik users Corey and johnflewis
* 15:32 Southparkfan: stopped/started dovecot and removed user account 'john' on misc1

## 2017-05-28 

* 19:07 Reception123: > UPDATE revision SET rev_user = '10' WHERE rev_user_text = 'IJzeren Jan'; on isvwiki
* 18:39 Reception123: SET rev_user = '22' WHERE rev_user_text = 'Siska'; on bpwiki
* 18:39 Reception123:  SET rev_user = '8' WHERE rev_user_text = 'Rachmat04'; on bpwiki

## 2017-05-27 

* 17:25 Reception123: reception@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php updateSpecialPages.php --wiki bpwiki

## 2017-05-26 

* 06:37 Reception|away: ran rebuildall.php --wiki bpwiki (tried to fix contribs issue)

## 2017-05-24 

* 17:16 Reception123: sudo -u www-data php /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/removeDeletedWikis.php --wiki metawiki
* 17:15 Reception123: DELETED FROM cw_wikis ruvowikiwiki sambodiawiki sample1113wiki sbbehzadiwiki scatranslatorswiki scbcwiki sdeuropewiki (DP)
* 17:08 Reception123: DELETE FROM cw_wikis rainfallwiki rcprobusitwiki readingclubwiki reizowiki reriawiki resetwiki revisionhistorymodelwiki rhythmwiki robloxscripterswiki rudinwiki (DP)
* 17:00 Reception123: DELETED FROM cw_wikis omwiki openconstitutionwiki passtestwiki pavelwiki pittawiki planeteswiki popupwiki professionaldevelopmentwiki rafambienterowiki (DP)
* 16:16 Reception123: sudo -u www-data php /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/removeDeletedWikis.php --wiki metawiki
* 16:15 Reception123: > DELETE FROM cw_wikis WHERE wiki_dbname = 'wikirailwiki';
* 16:15 Reception123: DELETEROM cw_wikis WHERE wiki_dbname = 'libertywiki';
* 16:13 Reception123: > DELETE FROM cw_wikis WHERE wiki_dbname = 'metaautonomywiki';
* 14:31 Reception123: reception@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php updateArticleCount.php --wiki isvwiki --update
* 14:20 Reception123: reception@mw2:/srv/mediawiki/w/maintenance$ sudo -u www-data php dumpBackup.php --wiki armsinstitutewiki --full > /home/reception/armsinstitute.xml
* 14:18 Reception123: updated local email from "madciclistawiki" to match "metawiki" for Jlgallego

## 2017-05-21 

* 18:44 John: dropping databases deleted previously
* 18:36 Reception123:  sudo -u www-data php /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/removeDeletedWikis.php --wiki metawiki on mw1
* 18:33 Reception123: > reception@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php dumpBackup.php --wiki wikicanadawiki --full > /home/reception/wikicanada.xml
* 18:17 Reception123: reception@mw2:/srv/mediawiki/w/maintenance$ sudo -u www-data php importDump.php --wiki isvwiki /home/reception/isvorainorg_w-20150809-history.xml/isvorainorg_w-20150809-history.xml
* 16:14 Reception123: reception@mw1:~$ sudo -u www-data php /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/removeDeletedWikis.php --wiki metawiki
* 16:12 Reception123: DELETE FROM cw_wikis WHERE wiki_dbname = 'rtwiki'; (requested by revi)
* 16:12 Reception123: DELETE FROM cw_wikis WHERE wiki_dbname = 'wikicanadawiki'; (LTA)
* 05:51 Reception123: sudo -u www-data php importImages.php --wiki nenawikiwiki --search-recursively /home/reception/nenawiki1 on mw2

## 2017-05-20 

* 19:28 revi: extend length of Amanda ban to indefinite, just logging
* 19:00 Reception123: reception@mw2:/srv/mediawiki/w/maintenance$ sudo -u www-data php importDump.php --wiki nenawikiwiki /home/reception/NENAWiki-20170520182214.xml
* 10:46 Reception123: sudo -u www-data php rebuildLocalisationCache.php --wiki extloadwiki on mw*
* 10:38 Reception123: forked Reception123/CustomHeader
* 08:16 Reception123: sudo -u www-data php /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/removeDeletedWikis.php --wiki metawiki
* 08:15 Reception123: DELETED FROM cw_wikis medaidwiki menkoiwiki momnyangwiki msswiki musictabswiki myclubwiki nadot2017wiki neuromodulationwiki newcrewwiki nighthawkwiki occultwikiwikawiki olliewiki (DP)
* 08:07 Reception123: DELETED FROM cw_wikis hostelworldisdangerouswiki ilockedwiki inmomentappwikiwiki inmomentwiki interhistorypediawiki internalmedicinewiki israelianswerswiki jestermaxddwiki joeygeenwiki kutlaswiki lbhealthwiki locograndewiki lsferreirawiki medaidwiki (DP)
* 07:55 Reception123: DELTED FROM cw_wikis flowfusionwiki fundacjapileckiegowiki genspediawiki geschichtinemwiki ghgwiki glafoxwiki globalrcruwiki globalwiki gvorsterwiki hattiesburgpbiswiki hausprojektwiki hertapewiki hfhofficewiki (DP)
* 05:32 Reception123: reception@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php updateArticleCount.php --wiki ayrshirewiki --update
* 05:29 Reception123: sudo -u www-data php /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/removeDeletedWikis.php --wiki metawiki
* 05:28 Reception123: DELETE FROM cw_wikis WHERE wiki_dbname = 'lymernilwiki';

## 2017-05-17 

* 16:37 Reception|away: reception@mw1:~$ sudo -u www-data php /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/removeDeletedWikis.php --wiki metawiki
* 16:36 Reception|away: > DELETE FROM cw_wikis WHERE wiki_dbname = 'arasuithielwiki';
* 04:36 revi: revi@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php dumpBackup.php --wiki bchwiki --full > /home/revi/bchwiki20170517.xml

## 2017-05-14 

* 16:50 Reception123: reception@mw1:/srv/mediawiki/w/extensions/MirahezeMagic/maintenance$ sudo -u www-data php manageInactiveWikis.php --wiki metawiki --warn --close
* 16:45 Reception123: sudo -u www-data php rebuildLocalisationCache.php --wiki extloadwiki on mw*
* 06:12 Reception123: sudo -u www-data php rebuildLocalisationCache.php --wiki extloadwiki on mw*

## 2017-05-13 

* 19:46 John: cleared all storeconfigs for "bacula1" node
* 18:25 John: continuous problems with bacula software wise after recent job restructuring, reinstalling bacula1
* 18:13 Reception123: deleted random espiral.org.csr from /mnt/mediawiki-static
* 17:16 Reception123: sudo -u www-data php dumpBackup.php --wiki ayrshirewiki --full > /home/reception/ayrshirewiki13052017.xml on mw1
* 17:10 Reception123: deleted mediawiki-extensions-NewSignupPage repo as unneeded
* 10:16 John: rebooted mw2
* 08:31 Reception123: sudo -u www-data php rebuildLocalisationCache.php --wiki extloadwiki on mw*
* 07:44 Reception123: sudo -u www-data php rebuildLocalisationCache.php --wiki extloadwiki on mw*

## 2017-05-10 

* 19:03 imbophil: sudo -u www-data php rebuildLocalisationCache.php --wiki extloadwiki on MW1 and MW2
* 13:39 Reception|away: sudo -u www-data php dumpBackup.php --wiki scruffywiki --full > /home/reception/scruffywiki10052017.xml on mw1

## 2017-05-08 

* 19:15 imbophil: sudo -u www-data php rebuildLocalisationCache.php --wiki extloadwiki on MW1 and MW2
* 14:19 Reception123: > UPDATE page SET page_content_model = "wikitext" WHERE page_content_model = "flow-board"; on wikicanadawiki
* 08:14 Reception123: sudo -u www-data php rebuildLocalisationCache.php --wiki extloadwiki on mw*
* 06:35 Reception123: sudo -u www-data php rebuildLocalisationCache.php --wiki extloadwiki on mw*

## 2017-05-07 

* 14:17 Reception123: sudo -u www-data php rebuildLocalisationCache.php --wiki extloadwiki on mw*

## 2017-05-06 

* 18:57 John: upgrade phabricator
* 18:00 revi: revi@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php dumpBackup.php --wiki testwiki --full > /home/revi/testwiki20170506.xml
* 17:55 revi: revi@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php dumpBackup.php --wiki librewiki --full > /home/revi/librewiki20170506.xml
* 17:50 revi: revi@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php dumpBackup.php --wiki maiasongcontestwiki --full > /home/revi/maiasongcontestwiki20170506.xml
* 17:47 revi: revi@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php dumpBackup.php --wiki jayuwikiwiki --full > /home/revi/jayuwiki20170506.xml
* 17:39 Reception123: nice 10 for below
* 17:39 Reception123: sudo -u www-data php dumpBackup.php --wiki allthetropeswiki --full > /home/reception/allthetropes20170506.xml on mw2
* 17:35 revi: revi@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php dumpBackup.php --wiki metawiki --full > /home/revi/metawiki20170506.xml
* 17:26 revi: sudo -u www-data php dumpBackup.php --wiki reviwiki --full > /home/revi/reviwiki20170507.xml (nobody might care but I executed it)
* 10:17 John: manually ran failed GlobalRename job
* 06:36 Reception123: sudo -u www-data php rebuildLocalisationCache.php --wiki extloadwiki on mw*

## 2017-05-03 

* 17:16 John: deleted ganglia and acme bacula pools
* 16:07 revi: Disabled phabricator account Amanda, temporary: 2 months.
* 16:00 John: made some security tasks public in line with reasonable disclosure (1 misc, 1 intended design and 1 resolved security task)
* 15:51 John: changed view policy for T1747

## 2017-05-01 

* 14:00 John: upgrading phab
* 13:24 John: create bot_passwords on centralauth
* 13:17 John: created echo_unread_wikis table on metawiki
* 11:07 Reception123: temporarily added google HTML verification to /srv/mediawiki
* 11:03 Reception123: reception@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php deleteBatch.php --wiki bigforestwiki /home/reception/nuke.txt
* 10:27 Reception123: reception@mw1:~$ sudo -u www-data php /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/removeDeletedWikis.php --wiki metawiki
* 10:25 Reception123: > DELETE FROM cw_wikis WHERE wiki_dbname ='guarothwiki';
* 09:08 Reception123: > DELETE FROM cw_wikis WHERE wiki_dbname = 'dtswiki';

## 2017-04-28 

* 18:55 Reception123: sudo -u www-data php dumpBackup.php --wiki scruffywiki --full > /home/reception/scruffywiki28042017.xml

## 2017-04-23 

* 17:59 John: deleted Miraheze Widgets GitHub repo
* 08:40 Reception123: sudo -u www-data php rebuildLocalisationCache.php --wiki extloadwiki on mw*
* 07:48 Reception123: sudo -u www-data php rebuildLocalisationCache.php --wiki extloadwiki on mw*
* 05:38 Reception123: sudo -u www-data php rebuildLocalisationCache.php --wiki extloadwiki on mw*

## 2017-04-22 

* 10:23 Reception123: reception@mw1:/srv/mediawiki/w/extensions/MirahezeMagic/maintenance$ sudo -u www-data php manageInactiveWikis.php --wiki metawiki --warn --close

## 2017-04-20 

* 17:33 Reception123: reception@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php deleteBatch.php -u Reception123 --wiki testwiki home/reception/delete.txt (and more deletions to come)

## 2017-04-19 

* 10:56 Reception123: > DELETE FROM cw_wikis WHERE wiki_dbname = 'bereawiki';

## 2017-04-18 

* 20:53 John: removed PrivateSettings.php from private repo
* 16:14 John: moved uptime robot from sysadmin email account to operations + added staff as alert contact
* 15:44 John: ./bin/files integrity --compute --all + phab upgrade
* 06:27 Reception123: sudo -u www-data php rebuildLocalisationCache.php --wiki extloadwiki on mw*
* 06:03 Reception123: sudo -u www-data php rebuildLocalisationCache.php --wiki extloadwiki on mw*

## 2017-04-17 

* 14:18 Reception123: sudo -u www-data php rebuildLocalisationCache.php --wiki delete1wiki on mw* (testing extension)
* 09:08 Reception123: sudo -u www-data php rebuildLocalisationCache.php --wiki extloadwiki (remaining undefined magic word)
* 08:36 Reception123: sudo -u www-data php rebuildLocalisationCache.php --wiki metawiki on mw*

## 2017-04-16 

* 16:41 John: changed task edit policy
* 06:05 Reception123: sudo -u www-data php rebuildLocalisationCache.php --wiki extloadwiki on mw*

## 2017-04-15 

* 11:36 Reception123: sudo -u www-data php rebuildLocalisationCache.php --wiki extloadwiki on mw*

## 2017-04-14 

* 20:28 PuppyKun: rebooting cp2 "Failed to get D-Bus connection: No such file or directory"
* 13:56 Reception123: sudo -u www-data php rebuildLocalisationCache.php --wiki extloadwiki on mw*
* 04:45 Reception|away: reception@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php dumpBackup.php --wiki calexitwiki --full > /home/reception/calexitwiki14042017.xml
* 00:29 PuppyKun: ndkilla@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php deleteBatch.php --wiki scruffywiki --r=" [https://phabricator.miraheze.org/T1660](https://phabricator.miraheze.org/T1660)" /home/ndkilla/scruffydelete

## 2017-04-11 

* 22:53 John: deleted binlogs

## 2017-04-10 

* 17:48 Reception123: sudo -u www-data php /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/removeDeletedWikis.php --wiki metawiki
* 17:46 Reception123: > DELETE FROM cw_wikis WHERE wiki_dbname = 'deltaquadtestwiki'; (LTA)
* 17:46 Reception123: DELETED FROM cw_wikis delete[*-6]wiki

## 2017-04-09 

* 17:41 PuppyKun: MariaDB [phabricator_calendar]> update calendar_event set editPolicy="users" where id=21; and canceled the event
* 17:35 PuppyKun: stripped phabricator MFA from NDKilla
* 14:51 Reception123: reception@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php deleteBatch.php --wiki bigforestwiki /home/reception/nuke.txt
* 14:40 Reception123: > DELETE FROM cw_wikis WHERE wiki_dbname = 'scruffy2wiki';
* 09:29 Southparkfan: restarted phd

## 2017-04-07 

* 16:53 John: forced umount on mw1
* 16:35 Reception123: reception@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php dumpBackup.php --wiki modularwiki --full > /home/reception/modularwiki07042017.xml
* 16:34 Reception123: reception@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php dumpBackup.php --wiki scruffywiki --full > /home/reception/scruffywiki07042017.xml

## 2017-04-05 

* 14:05 Reception123: sudo -u www-data php /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/removeDeletedWikis.php --wiki metawiki
* 14:01 Reception123: DELETED FROM cw_wikis breakthegamewiki cisowiki comedyspaceshowwiki compendiumwiki dakadwiki datadefswiki deguwiki ep4wiki exerionwiki ezdmfwiki fabiowiki facebookhostwiki (DP)
* 13:53 Reception123: reception@mw1:/srv/mediawiki/w/extensions/MirahezeMagic/maintenance$ sudo -u www-data php manageInactiveWikis.php --wiki metawiki --warn --close
* 13:47 Reception123: DELETED FROM cw_wikis 3kwiki abilityandmeaningwiki aegyptiacawiki afswiki agrartechnikwiki agrocitewiki antitimerwiki aucelewiki aurcusonlinewiki authentiqwiki berlinwiki blackwaterregionallibrarywiki bleaguewiki borilowiki (DP)

## 2017-04-04 

* 14:27 PuppyKun: ndkilla@misc1:~$ sudo service icingabot restart && sudo service adminbot restart
* 05:28 Reception|away: removed spam from cw_wikis+declined reqs

## 2017-04-03 

* 20:07 John: finally closed a task by using the database because edit policy was way too restrictive
* 16:32 Reception|away: reception@mw2:/srv/mediawiki/w/maintenance$ sudo -u www-data php importDump.php --wiki modularwiki /home/reception/localhost_muff-20130102-history.xml
* 16:21 Reception|away: removed spam from cw_requests
* 16:10 Reception|away: reception@mw2:/srv/mediawiki/w/maintenance$ sudo -u www-data php importImages.php --wiki modularwiki --search-recursively /home/reception/images

## 2017-04-02 

* 19:03 Southparkfan: restarted php5-fpm process on mw1 and mw2

## 2017-03-31 

* 16:52 John: upgraded phabricator
* 16:28 John: dropped modularwiki
* 16:07 John: reclaimed more space on db2

## 2017-03-28 

* 21:02 PuppyKun: ndkilla@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php updateArticleCount.php --wiki bgowiki --update
* 15:34 PuppyKun: ndkilla@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php deleteBatch.php --wiki bgowiki --r="deleteBatch.php: Mass deletion of pages in Category:Pages_flagged_for_deletion" --u="NDKilla" /home/ndkilla/pages-to-delete2.txt"
* 15:24 PuppyKun: ndkilla@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php deleteBatch.php --wiki bgowiki --r="deleteBatch.php: Mass deletion of pages in Category:Pages_flagged_for_deletion" --u="NDKilla" /home/ndkilla/pages-to-delete.txt"
* 05:29 Reception|away: removed spam from cw_requests

## 2017-03-27 

* 16:36 Reception|away: reception@mw2:/srv/mediawiki/w/maintenance$ sudo -u www-data php importDump.php --wiki bereawiki /home/reception/BereaWiki-20170318210125.xml

## 2017-03-26 

* 19:28 Southparkfan: purged several binlogs on db2
* 08:39 Reception123: removed spam from cw_requests

## 2017-03-25 

* 20:14 Reception123: reception@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php  rebuildrecentchanges.php --wiki modularwiki
* 20:08 Reception123: reception@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php importDump.php --wiki modularwiki /home/reception/localhost_muff-20130102-history.xml
* 15:26 Reception123: reception@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php deleteBatch.php --wiki modularwiki /home/reception/deleted.txt
* 10:19 Reception123: sudo -u www-data php rebuildLocalisationCache.php --wiki extloadwiki on mw* (run again)
* 10:03 Reception123: sudo -u www-data php rebuildLocalisationCache.php --wiki metawiki on mw* (was not rebuild after CW LC changes)
* 08:59 Reception123: sudo -u www-data php rebuildLocalisationCache.php --wiki extloadwiki on mw*

## 2017-03-24 

* 19:41 Reception123: reception@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php rebuildall.php --wiki metawiki ( `{{ {{NOW}} }}` not updating for a few days)
* 19:36 Reception123: reception@mw2:/srv/mediawiki/w/maintenance$ sudo -u www-data php importImages.php --wiki modularwiki --search-recursively /home/reception/muffwigglerimages
* 19:33 Reception123: sudo -u www-data php /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/removeDeletedWikis.php --wiki metawiki
* 19:32 Reception123: DELETE FROM cw_wikis quamplexitywiki qwwiki refugeepathwayswiki sandeepucreatewiki secondcirclewiki sibcolombiawiki steellegionswikiwiki storyofaryonwiki technoteswiki ujimawiki vmbrawiki wikibharalwiki wikichineserockwiki wikinalyticswiki yadanbiadwiki (DP)
* 19:21 Reception123: DELETED FROM cw_wikis itsmwikiitwikiwiki jaunepluswiki jjffjjwiki liftwiki liquidcablewiki lludrigawiki manyethriwiki masterwiki mpatwiki munankerdurshcilwiki notlandswiki offensivewiki plantwiki pnatcwiki ppluswiki (DP)
* 19:11 Reception123: ... fairytailwiki falkewiki gastronomicapediawiki gbnavaparawiki  geekkidswiki ggukvolunteerswiki girardfxwiki guitartopconstructionwiki i3wikiwiki interwikiwiki (DP)
* 19:11 Reception123: DELETED FROM cw_wikis dddandtwikiwiki demokraciawiki diepiowiki dpauldwiki dsdocswiki dswiki ezybfowiki
* 18:57 Reception123: > DELETE FROM cw_wikis WHERE wiki_dbname = 'leagueswiki'; (LTA)
* 18:57 Reception123: DELETED FROM cw_wikis academywiki adrianwiki alphadekelwiki anitrapavkawiki apexwiki augustinianumwiki b3wwiki brocktoncatholicwiki brunurbwiki cbmediawiki creativeartswiki ctrlaltdelpovertywiki cubeonwiki (DP)
* 17:43 Reception123: reception@mw2:/srv/mediawiki/w/maintenance$ sudo -u www-data php importDump.php --wiki modularwiki /home/reception/wikimuffwigglercom-20121222-history.xml
* 06:10 Reception|away: removed cw_requests spam

## 2017-03-23 

* 20:24 John: importing bp.org images (again)
* 19:46 John: restart jobrunner
* 18:22 John: running "CREATE INDEX ar_usertext_timestamp ON archive (ar_user_text,ar_timestamp);" on all wikis
* 16:09 PuppyKun: ndkilla@misc2:~$ sudo service redis-server restart (non-0 exit code)

## 2017-03-22 

* 21:31 PuppyKun: ndkilla@misc1:~$ sudo service icingabot restart
* 19:50 Reception|away: removed spam from cw_requests
* 19:06 John: moved uncommitted code to /home/southparkfan/ from /srv/mediawiki/w

## 2017-03-21 

* 17:34 Reception|away: > DELETE FROM cw_wikis WHERE wiki_dbname = 'wiki'; (created in error; pointless)

## 2017-03-18 

* 16:12 Reception123: deleted spam wiki requests
* 15:14 Reception123: removed spam from cw_requests as it spammed RequestQueue
* 15:11 Reception123: sudo -u www-data php /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/removeDeletedWikis.php --wiki metawiki
* 15:10 Reception123: > DELETE FROM cw_wikis WHERE wiki_dbname = 'wikihubwiki'; and wikisciencewiki (LTA)
* 11:59 Reception123:  sudo -u www-data php rebuildLocalisationCache.php --wiki extloadwiki

## 2017-03-17 

* 17:35 Reception|away: reception@mw2:/srv/mediawiki/w/extensions/MirahezeMagic/maintenance$ sudo -u www-data php manageInactiveWikis.php --wiki metawiki --warn --close
* 16:55 Southparkfan: restarted ganglia-monitor on parsoid1

## 2017-03-16 

* 21:21 John: rolling restart of ganglia-monitor on servers

## 2017-03-14 

* 19:09 imbophil: sudo -u www-data php rebuildLocalisationCache.php --wiki extloadwiki on MW1 and MW2

## 2017-03-12 

* 18:49 John: creating pr_index table on all wikis
* 17:59 John: importing images to bpwiki

## 2017-03-10 

* 17:20 Reception123: reception@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php dumpBackup.php --wiki meeusenwiki --full > /home/reception/meeusenwiki100302017.xml
* 17:13 Southparkfan: hard reboot cp2, puppet fails, unresponsive to /usr/sbin/service and reboot commands

## 2017-03-07 

* 17:58 John: phabricator updated

## 2017-03-06 

* 18:04 Reception123: sudo -u www-data php /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/removeDeletedWikis.php --wiki metawiki
* 18:01 Reception123: > DELETE FROM cw_wikis WHERE wiki_dbname = 'wikiyangtzewiki'; (LTA)
* 18:00 Reception123: > DELETE FROM cw_wikis WHERE wiki_dbname = 'americanopediawiki'; (LTA)
* 17:59 Reception123: > DELETE FROM cw_wikis WHERE wiki_dbname = 'internalwiki'; (IRC request)

## 2017-03-05 

* 16:29 Southparkfan: deleted sagan4wiki
* 16:01 Southparkfan: performing database maintenance on sagan4wiki
* 11:59 Reception123: rebuilt recentchanges on Meta (testing something)

## 2017-03-04 

* 20:08 Reception123: removed spam from cw_requests (requests queue is flooded)
* 16:25 Southparkfan: deleted southparkfan{2..5}wiki
* 16:25 imbophil: sudo -u www-data php rebuildLocalisationCache.php --wiki extloadwiki on MW1 and MW2
* 16:19 Southparkfan: rebuilt RC on metawiki

## 2017-03-03 

* 18:31 John: umount /mnt/mediawiki-static on mw1
* 18:19 John: rebooting mw1, mount issues
* 15:39 Southparkfan: dropped southparkfan{2..9}wiki
* 15:30 Southparkfan: rebuilding recentchanges on metawiki
* 14:38 Southparkfan: restarted phd
* 13:46 Reception123: reception@mw2:/srv/mediawiki/w/maintenance$ sudo -u www-data php dumpBackup.php --wiki anothertimeline2120wiki --full > /home/reception/anothertimeline2120.xml & reception@mw2:/srv/mediawiki/w/maintenance$ sudo -u www-data php importDump.php --wiki particracywikiwiki /home/reception/anothertimeline2120wiki.xml
* 13:32 Reception123: reception@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php rebuildall.php --wiki bigforestwiki and jayuwiki

## 2017-03-02 

* 23:53 PuppyKun: ndkilla@misc1$ service ircrcbot restart

## 2017-03-01 

* 20:08 imbophil: sudo -u www-data php rebuidLocalisationCache.php --wiki extloadwiki on MW1 and MW2

## 2017-02-25 

* 15:08 Reception123: removed spam from cw_requests

## 2017-02-24 

* 20:30 Southparkfan: upgraded piwik to 2.17.1, ran archive script
* 20:08 Southparkfan: restarted ganglia daemon on db2
* 18:35 John: stripped 2FA from phabricator account for John
* 17:43 Reception123: sudo -u www-data php rebuildall.php --wiki lothuialethwiki and arasuithielwiki on mw1
* 17:33 Reception123: DELETE FROM cw_wikis WHERE wiki_dbname = 'zgradetenniswiki'; (requested)
* 17:02 Reception|away: sudo -u www-data php dumpBackup.php --wiki zgradetenniswiki --full > /home/reception/zgradetennis.xml on mw1

## 2017-02-23 

* 20:08 John: dropping databases in deleted.dblist
* 19:57 Reception|away: sudo -u www-data php /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/removeDeletedWikis.php --wiki metawiki
* 19:56 Reception|away: DELETE FROM cw_wikis WHERE wiki_dbname = 'freedomopennesswiki'; (DP, making db space)
* 17:50 John: phabricator upgraded
* 17:49 John: upgrading phabricator

## 2017-02-22 

* 19:25 John: attached all unattached global accounts
* 07:25 Reception|away: removed spam from cw_requests

## 2017-02-21 

* 19:32 Reception|away:  sudo -u www-data php /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/removeDeletedWikis.php --wiki metawiki
* 19:31 Reception|away: DELETE FROM cw_wikis (mainwiki nemesiswiki theinternetemowiki)
* 16:34 PuppyKun: restarted jobrunner on mw1

## 2017-02-20 

* 23:46 John: moved metawiki back to db2 - CreateWiki limitations
* 20:34 John: rebooting mw2
* 18:23 John: setting centralauth and loginwiki databases to read only
* 17:31 John: restarted jobrunner
* 17:02 Reception123: DELETED FROM cw_wikis (elementswiki, picturepediawiki, mountainpediawiki) (ban evasion; community imposed)
* 15:34 John:  php attachAccount.php --wiki loginwiki --userlist /home/johnflewis/list [attaching JBridgwood to global account]
* 07:20 Reception|away: reception@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php updateArticleCount.php --wiki tharranarothwiki --update (didn't work the first time)

## 2017-02-19 

* 15:00 Reception|away:  reception@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php updateArticleCount.php --wiki tharranarothwiki

## 2017-02-18 

* 21:28 John: killing icinga-bot, icinga changes coming up
* 08:19 Reception123: sudo -u www-data php /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/removeDeletedWikis.php --wiki metawiki
* 08:18 Reception123: DELETED FROM cw_wikis civicvwiki dadisawikiwiki edwardravenwoodwiki gamestartwiki gibswiki ideatwiki lastpodcastwiki micropediawiki portalwiki psikiwiki realmswiki recherchesdocumentaireswiki retrowikiwiki securitieswiki senadowiki singstarwikiwiki tanodswiki testdocumentationwiki witsacademywiki worldnewswiki (DP)
* 07:54 Reception123: /srv/mediawiki/w/maintenance$ sudo -u www-data php rebuildLocalisationCache.php --wiki extloadwiki on mw*

## 2017-02-17 

* 17:55 John: parsoid updated
* 17:22 John: upgrading parsoid involving breaking changes

## 2017-02-15 

* 16:54 Reception123: sudo -u www-data php /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/removeDeletedWikis.php --wiki metawiki
* 16:52 Reception123: DELETED FROM cw_wikis walthamstowlabourwiki wikielectronicawiki wikihuertawiki wikingswiki wikiniscemiwiki wikiturawiki writinggallerywiki wsudmswiki ytwiki (DP)
* 16:44 Reception123:  sudo -u www-data php /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/removeDeletedWikis.php --wiki metawiki
* 16:42 Reception123: DELETE FROM cw_wikis topchoicewiki trtitreprovisoirewiki tsaristwiki turkcesozlukwiki tyrolmountainswiki ultracomboswiki unibloxwiki urho3dwiki valentinawikiwiki vandwellingwiki velhocoiotewiki villanoswiki votcwiki voyagewiki vozquadwiki vrgowiki (DP)
* 16:25 Reception123: sudo -u www-data php /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/removeDeletedWikis.php --wiki metawiki
* 16:21 Reception123: DELETED FROM cw_wikis taylorwiki tdkwwikiwiki testelitewiki testforspoonwiki thedangeloteamwiki thefuturewiki thepeoplegeekwiki thestarwarsarchiveswiki theworldofvailnoffwiki titreprovisoirewiki todosobreukwiki
* 15:47 Reception123: > DELETE FROM cw_wikis WHERE wiki_dbname = 'atheiwiki' and ircaffiliateswiki ;

## 2017-02-14 

* 17:12 John: converted misc* to puppet agent
* 17:08 John: converted mw* to puppet agent
* 16:56 John: converted db* to puppet agent
* 16:52 John: converted cp* to puppet agent -- we really need to upgrade cp2
* 16:50 John: converted bacula1 to puppet agent
* 16:00 John: converted ns1.miraheze.org to a puppet agent
* 12:45 John: changed viewPolicy on two tickets via mysql

## 2017-02-13 

* 21:08 labster: restarted jobqueue
* 19:34 John: rebooting mw2, unresponsive

## 2017-02-12 

* 17:23 John: restarted IRCRC bot about 4 days of its being down

## 2017-02-11 

* 20:15 Reception123: /srv/mediawiki/w/maintenance$ sudo -u www-data php rebuildLocalisationCache.php --wiki extloadwiki on mw*
* 19:38 Reception123: removed threats/harassment from 4 wiki requests (sql.php)
* 11:25 Reception123: /srv/mediawiki/w/maintenance$ sudo -u www-data php rebuildLocalisationCache.php --wiki extloadwiki on mw*
* 11:05 Reception123: reception@mw1:/srv/mediawiki/w/extensions/MirahezeMagic/maintenance$ sudo -u www-data php manageInactiveWikis.php --wiki metawiki --warn --close

## 2017-02-10 

* 19:08 Reception123: reception@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php deleteBatch.php /home/reception/testpage.txt --wiki claneuphoriawiki --r Not_responsive_._ Error. --u Reception123
* 14:27 Reception123: moved bigforestwikipediawiki files to bigforeswiki (mediawiki-static)
* 09:21 Reception123: ran same again after restore fail
* 09:20 Reception123: reception@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php deleteBatch.php /home/reception/testpage.txt --wiki claneuphoriawiki --r Not responsive. Gives error. --u Reception123

## 2017-02-09 

* 20:01 imbophil: sudo -u www-data php rebuildLocalisationCache.php --wiki extloadwiki on mw1 and mw2

## 2017-02-08 

* 16:09 John: renamed bigforestwikipediawiki -> bigforestwiki

## 2017-02-07 

* 11:03 revi: at mw1.
* 11:03 revi: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki unjeongwiki /home/revi/unjungwiki_dump_20161016.xml

## 2017-02-05 

* 20:26 imbophil: sudo -u www-data php rebuildLocalisationCache.php --wiki extloadwiki on MW1 and MW2

## 2017-02-04 

* 09:17 Reception123: reception@mw2:/srv/mediawiki/w/maintenance$ sudo -u www-data php /srv/mediawiki/w/maintenance/importImages.php --wiki bigforestwikipediawiki --search-recursively /home/reception/images

## 2017-02-03 

* 19:08 John: phabricator upgraded - new favourites menu
* 19:05 John: upgrading phabricator
* 17:45 Reception123: sudo -u www-data php importDump.php --wiki bigforestwikipediawiki /home/reception/dump1.xml on mw2

## 2017-02-02 

* 17:36 John: cleared /srv/mediawiki/{w|config} on mw1 for refresh - long puppet runs caused by inconsistencies in git

## 2017-01-31 

* 15:06 John: restarted MySQL on db3 to have new tmp directory change take place
* 14:55 John: cleared /tmp/ on db3

## 2017-01-28 

* 10:05 Reception|away: sudo -u www-data php importDump.php --wiki bigforestwikipediawiki /home/reception/dump.xml on mw2

## 2017-01-27 

* 19:34 John: dropped help_{topic,relation,keyword,category} on allthetropeswiki
* 19:30 John: dropped plugin, ndb_binlog_index and slow_log on allthetropeswiki

## 2017-01-23 

* 12:08 Southparkfan: restarted ganglia daemon on all servers (excluding misc2/db3)

## 2017-01-22 

* 21:03 John: dropped attwiki and phabricator databases on db2
* 19:11 John: killing apache on misc1, easiest way to stop phab being writable

## 2017-01-21 

* 14:22 Reception123: reception@mw1:/mnt/mediawiki-static/dumps/2016$ sudo -u www-data rm -rf maiasongcontestwiki.tgz
* 14:21 Reception123: reception@mw1:/mnt/mediawiki-static/dumps$ sudo -u www-data rm -rf bgowiki-2016-07-26-full.xml
* 14:17 Reception123: reception@mw1:/mnt/mediawiki-static/dumps$ sudo -u www-data rm -rf sterbalssundrystudieswiki24082016.zip
* 14:17 Reception123: reception@mw1:/mnt/mediawiki-static/dumps$ sudo -u www-data rm -rf lexique.xml
* 14:16 Reception123: reception@mw1:/mnt/mediawiki-static/dumps$ sudo -u www-data rm -rf poserdazfreebiesorainorg_w-20150808-history.xml
* 14:16 Reception123: reception@mw1:/mnt/mediawiki-static/dumps$ sudo -u www-data rm -rf permanentfuturelabwiki.xml
* 14:16 Reception123: reception@mw1:/mnt/mediawiki-static/dumps$ sudo -u www-data rm -rf izanagiwiki-2016-03-15.xml.gz
* 14:16 Reception123: reception@mw1:/mnt/mediawiki-static/dumps$ sudo -u www-data rm -rf izanagiwiki-20160216-full.xml
* 14:15 Reception123: reception@mw1:/mnt/mediawiki-static/dumps$ sudo -u www-data rm -rf softwarecrisiswiki-2016-05-03.xml
* 14:15 Reception123: reception@mw1:/mnt/mediawiki-static/dumps$ sudo -u www-data rm -rf szkwiki.xml.gz
* 14:15 Reception123: reception@mw1:/mnt/mediawiki-static/dumps$ sudo -u www-data rm -rf bgowiki-2016-05-03.xml

## 2017-01-18 

* 17:41 John: disabled innodb_adaptive_hash_index

## 2017-01-13 

* 17:54 John: updated phabricator
* 17:37 imbophil: sudo -u www-data php rebuildLocalisationCache.php --wiki extloadwiki on MW1 and MW2

## 2017-01-11 

* 15:06 John: rm#'d /tmp on db2

## 2017-01-10 

* 20:35 John: DELETE FROM user_email WHERE id = "347";
* 20:28 John:  DELETE FROM user_externalaccount WHERE id = "368";

## 2017-01-07 

* 05:50 PuppyKun: MariaDB [trexwiki]> delete from user_groups where ug_user=30; query ok, 1 row affected. Remove `Ceo` from `IT Office` a non-existent user and a globally locked account

## 2017-01-06 

* 23:59 labster: restarted jobrunner
* 13:39 Southparkfan: rebooting cp2, unresponsive to NRPE, sshd unresponsive, serial console not available due to lack of memory

## 2017-01-04 

* 19:56 imbophil: sudo -u www-data php rebuildLocalisationCache.php --wiki extloadwiki on Mw1 and Mw2

## 2017-01-02 

* 21:59 John: running SQL on all wikis
* 21:09 John: fully deleted 19 wikis
* 21:00 John: deleting wikicanadawiki

## 2017-01-01 

* 19:16 John: installed php5-apcu on misc1 for phabricator
* 19:08 John: phabricator upgraded
* 19:07 John: phabricator upgrades coming
* 15:01 Reception123: srv/mediawiki/w/maintenance sudo -u www-data php rebuildLocalisationCache.php --wiki extloadwiki on mw*
## Information 

All times are in **UTC+0**/ **GMT**.

Archives: [2015](https://meta.miraheze.org/wiki//2015), [2016](https://meta.miraheze.org/wiki//2016)

----
**Source**: [https://meta.miraheze.org/wiki/Tech:Server_admin_log/2017](https://meta.miraheze.org/wiki/Tech:Server_admin_log/2017)