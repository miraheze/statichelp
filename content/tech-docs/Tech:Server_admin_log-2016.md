---
title: Tech:Server admin log/2016
---

`{{ {{TOC right}} }}`
## 2016-12-31 

* 16:57 Reception|away: /srv/mediawiki/w/maintenance sudo -u www-data php rebuildLocalisationCache.php --wiki extloadwiki on mw*

## 2016-12-30 

* 14:06 John: clears /tmp on misc1
* 05:24 PuppyKun: ndkilla@cp1: removed two files from /srv/mediawiki-static/bgowiki/ at the request of boardgame-online.com staff (reason: personal/inappropriate use of photographs)

## 2016-12-29 

* 08:51 Reception|away: DELETE FROM cw_wikis WHERE wiki_dbname = 'prpwiki'; (requested T1217)

## 2016-12-27 

* 10:49 Reception|away: Mw1: /mnt/mediawiki-static sudo -u www-data rm -rf stoutofreachwiki (deleted per DP)

## 2016-12-26 

* 15:59 Reception123: reception@mw1:/srv/mediawiki/w/extensions/MirahezeMagic/maintenance$ sudo -u www-data php manageInactiveWikis.php --wiki metawiki --warn --close
* 07:58 Reception123: DELETE FROM cw_wikis senowiki shoppingwiki shorshonewiki siagewiki siqwiki sirahwiki soltysiwiki soundinteractivewiki sourcesecurewiki spaceinquisitionwiki specialeducationwiki (DP)
* 8:00 Reception123: sudo -u www-data php /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/removeDeletedWikis.php --wiki metawiki
* 8:06 Reception123: DELETE FROM cw_wikis sptv2wiki spython01wiki starlineprocesswiki toutofreachwiki streetwiki swtorsofwiki
* 8:06 Reception123: sudo -u www-data php /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/removeDeletedWikis.php --wiki metawiki

## 2016-12-24 

* 09:56 labster: sudo service jobrunner restart

## 2016-12-22 

* 19:12 Southparkfan: deployed preload for HSTS on *.miraheze.org

## 2016-12-21 

* 21:28 John: restarted jobrunner

## 2016-12-20 

* 16:25 John: MariaDB [phabricator_project]> UPDATE project SET editPolicy = "users" WHERE name = "ManageWiki";

## 2016-12-19 

* 19:44 John: restart phabricator daemons
* 15:27 Southparkfan: unlocked several event policies (phabricator)
* 13:18 Reception|away: reception@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php updateSpecialPages.php --wiki zgradetenniswiki

## 2016-12-17 

* 17:55 John: Deleted our local Comments extension repo - upstream in use
* 17:46 John: git reset --hard origin/REL1_28 on mw*
* 12:35 PuppyKun: root@misc1:/tmp# rm phabricator-server/* & phabricator-setup/*

## 2016-12-11 

* 19:21 John: upgrade done, rebuilding phabricator searchindex per changes to InnoDB
* 19:19 John: upgrading phabricator
* 15:05 John: deleted static files for deleted wikis
* 14:47 John: dropping databases for deleted wikis
* 13:19 Reception|away: sudo -u www-data php /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/removeDeletedWikis.php --wiki metawiki
* 13:19 Reception|away: DELETE FROM cw_wikis WHERE wiki_dbname = 'wigallwiki';

## 2016-12-10 

* 23:33 John: changing all users preferences for math from source -> png
* 23:32 John: changing all users preferences for math from mathml -> png
* 19:48 John: deleted rouge ProtectSite directory on mw*, causing config changes to take 2 minutes to deploy
* 19:45 John: added EducationProgram sql tables to all wikis
* 10:40 Reception123: copied /avatars and /awards to lezar224wiki

## 2016-12-08 

* 12:43 PuppyKun: php createAndPromote --force --sysop --wiki metawiki Pup

## 2016-12-07 

* 16:25 Reception|away: sudo -u www-data php rebuildLocalisationCache.php --wiki extloadwiki on mw*

## 2016-12-06 

* 20:56 Southparkfan: reinstalling db2
* 06:46 Southparkfan: booted db2

## 2016-12-04 

* 17:31 PuppyKun: ndkilla@mw1~ php resetUserEmail.php Amanda --email--
* 15:27 Southparkfan: running du -sh /srv/mediawiki-static/* in a screen on cp1
* 15:10 John: rm'd stray DB file volumes on bacula1

## 2016-12-03 

* 20:22 Southparkfan: installed php5-xhprof on mw1
* 19:47 John: deleted null volume in bacula
* 14:49 Reception|away: sudo -u www-data php /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/removeDeletedWikis.php --wiki metawiki
* 14:49 Reception|away: DELETE FROM cw_wikis WHERE wiki_dbname = 'anduinwiki';

## 2016-12-02 

* 21:38 John: deleted SectionHide repository - all users converted to HideSection
* 21:31 John: changed default branch for MediaWiki to REL1_28
* 21:25 John: restarted jobrunner
* 19:28 John: made SQL changes to centralauth for 1.28
* 03:24 PuppyKun: reloaded nginx on appservers

## 2016-12-01 

* 03:01 labster: steward edit to [https://wikicanada.miraheze.org/wiki/Main_Page](https://wikicanada.miraheze.org/wiki/Main_Page) per IRC request

## 2016-11-30 

* 18:26 labster: sudo service jobrunner restart
* 18:17 labster: ran runJobs.php on allthetropeswiki
* 02:17 PuppyKun: renamed adiapediawiki to elarawiki and moved images directory
* 02:03 PuppyKun: ndkilla@misc2:~$ restarted redis-server

## 2016-11-28 

* 21:12 John: disabled puppet on me*
* 17:27 John: upgraded phabricator

## 2016-11-25 

* 19:58 Reception|away: sudo -u www-data php /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/removeDeletedWikis.php --wiki metawiki
* 19:57 Reception|away: DELETE FROM cw_wikis WHERE wiki_dbname = 'calgary38wiki' and 'wikijokewiki'; (requested at SN)
* 16:52 Reception|away: sudo -u www-data php rebuildLocalisationCache.php --wiki extloadwiki on mw*
* 15:54 John: phabricator upgraded
* 15:53 John: upgrading phav

## 2016-11-24 

* 17:26 Reception|away: sudo -u www-data php /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/removeDeletedWikis.php --wiki metawiki
* 17:25 Reception|away: DELETE FROM cw_wikis WHERE wiki_dbname = 'wikiarchitecturewiki';

## 2016-11-20 

* 17:50 Reception|away: reception@mw1:/srv/mediawiki/w/extensions/MirahezeMagic/maintenance$ sudo -u www-data php manageInactiveWikis.php --wiki metawiki --warn --close

## 2016-11-19 

* 13:39 Southparkfan: NLCVZE5-1 is low on space, impacting db2. RamNode staff is working on it
* 13:24 Reception123: sudo -u www-data php /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/removeDeletedWikis.php --wiki metawiki
* 13:23 Reception123: DELETE FROM CW_WIKIS rylnbgwiki s3cre7ninjawiki saltypigeonwiki sanalysiswiki sancatwiki saudewiki scheerswiki scwikiwiki sdawiki seniorendoppelwiki (DP)
* 13:03 Reception123: sudo -u www-data php /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/removeDeletedWikis.php --wiki metawiki
* 13:01 Reception123: DELETE FROM CW_WIKIS rezeptewiki rfdinternalwiki ricwiki rigelwiki riotdevjiawiki rodintestonewiki rofwiki ronaldwiki ronuoswiki rosaswiki rosierlibrariuswiki rwbyfrwiki (DP)
* 12:55 Reception123: sudo -u www-data php /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/removeDeletedWikis.php --wiki metawiki
* 12:54 Reception|away: DELETE FROM cw_wikis repressionwiki reriawiki restreamwiki (DP)
* 12:44 Reception|away: DELETED FROM CW_WIKIS portlandmarketgardenprojectwiki posawikiwiki poupaswiki preiliwiki presencewiki pruebaapinfowiki qsswiki radis0radiswiki rahbanwiki ravniciapiawiki reflexiconwiki reinventandolasorganizacioneswiki (DP)
* 09:55 Reception|away: sudo -u www-data php /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/removeDeletedWikis.php --wiki metawiki
* 09:54 Reception|away: DELETE FROM cw_wikis WHERE dbname = wikibridgewiki
* 09:54 Reception|away: DELETE FROM cw_wikis WHERE wiki_dbname = '

## 2016-11-18 

* 21:19 Southparkfan: repooled mw1
* 20:17 Southparkfan: depooled mw1 for debugging T1036
* 17:29 Reception123: sudo -u www-data php /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/removeDeletedWikis.php --wiki metawiki (DP)
* 17:28 Reception123: DELETE FROM cw_wikis pclwikiwiki pflanzenwiki philchariowiki photography101wiki pifusaswiki piraeuswiki pnpwiki polotnowiki (DP)
* 17:21 Reception123: sudo -u www-data php /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/removeDeletedWikis.php --wiki metawiki (DP)
* 17:20 Reception123: DELETE FROM cw_wikis onepracticewiki oolwiki opexwiki otherdropswiki otherstuffwiki pactewiki paicamwiki pamuxwiki paratwiki (DP)

## 2016-11-17 

* 16:53 John: ./bin/auth strip --user NDKilla --all-types

## 2016-11-15 

* 21:38 Southparkfan: restarted rsyslog
* 18:48 Reception|away:  sudo -u www-data php rebuildLocalisationCache.php --wiki extloadwiki on mw*

## 2016-11-14 

* 20:18 Southparkfan: regenerated SSH keypair for private git

## 2016-11-13 

* 19:54 John: phabricator upgraded - enjoy the curves
* 19:52 John: upgrading phabricator
* 18:03 Southparkfan: dropping mindladlewiki for recovery
* 17:55 Southparkfan: and for msnhinet8wiki mt2bwiki mundanapediawiki myocodesharewiki nddbwiki nddbwiki neonetwiki nhshguidewiki nidda23wiki nonplussedultrawiki novahistoriaewiki nuccdcwiki nuestraqueridafamiliawiki oacwiki
* 17:55 Southparkfan: same for lyingseawiki makewiki materialsdatabasewiki mathsclubwiki matogewiki mbarwiki mecanonwiki mediaconflictwiki melvinsamuelwiki mgarciawiki mikecurtinworkwiki minoxrigawiki mmgwiki mmittewiki mojavestormwiki momiwiki mosaicschoolwiki mpaqwiki ms43wiki msibattlegroundwiki
* 17:55 Southparkfan: same for indexwiki insteadwiki instylewiki ioncontainerswiki iqtwiki ironspherewiki isswiki jbkwwiki jeanfredericwiki jeranwiki jeremysrpgswiki johnsonfamilycookbookwiki jricwiki knowlabwiki lasenallawiki lclwikiwiki learningskillswiki learnthegeekwiki lifelinewiki liutaiwikiwiki llwwiki log4techwiki lugjuwiki
* 17:55 Southparkfan: as well for gemwikiwiki geramaxwiki golanghowtowiki grtitreprovisoirewiki gumedienwiki gympawikiwiki gyrobotwiki habitatpartageboulonnaiswiki haftpflichtheldenwiki harserwiki hexaversewiki hokifywiki homewiki hubmakerswiki iaccswiki ibdwiki iblwiki imagewiki imgopowiki
* 17:54 Southparkfan: deleted the databases and static files of: encscheckinwiki enlotwiki entitreprovisoirewiki entropediawiki envsciwiki epsolawiki escawiki etec510wiki evolawiki f14swiki familytreewiki fenaloniawiki fms23wiki fmu82wiki fonehelpwiki forgottenwiki francisfranckwiki freedgewiki freeswitchwiki frtitreprovisoirewiki fvcwikiwiki gamesfortuttiwiki gappswiki
* 16:57 Reception|away: /srv/mediawiki/w/maintenance$ sudo -u www-data php rebuildLocalisationCache.php --wiki extloadwiki on mw*
* 16:35 Reception|away: /srv/mediawiki/w/maintenance$ sudo -u www-data php rebuildLocalisationCache.php --wiki extloadwiki on mw*
* 16:28 Reception|away: mw2: sudo -u www-data foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/maintenance/sql.php /srv/mediawiki/w/extensions/Newsletter/sql/nl_subscriptions.sql
* 16:22 Reception|away: mw2: sudo -u www-data foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/maintenance/sql.php /srv/mediawiki/w/extensions/Newsletter/sql/nl_publishers.sql
* 16:17 Reception|away: mw2: sudo -u www-data foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/maintenance/sql.php /srv/mediawiki/w/extensions/Newsletter/sql/nl_newsletters.sql
* 16:16 Reception|away: mw1: sudo -u www-data foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/maintenance/sql.php /srv/mediawiki/w/extensions/Newsletter/sql/nl_issues.sql
* 10:50 Southparkfan: ran refreshImageMetadata.php and rebuildImages.php on noalatalawiki

## 2016-11-12 

* 14:36 Reception123:  sudo -u www-data php rebuildLocalisationCache.php --wiki extloadwiki on mw*
* 14:31 Reception123:  sudo -u www-data php /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/removeDeletedWikis.php --wiki metawiki
* 14:30 Reception123: DELETED FROM cw_wikis nddbwiki neonetwiki nhshguidewiki nidda23wiki nonplussedultrawiki novahistoriaewiki nuccdcwiki nuestraqueridafamiliawiki oacwiki (DP)
* 14:29 Southparkfan: ran insert into cw_wikis values ('mychartwiki', 'Music Charts', 'es', 0, 0, NULL); - Reception123 accidentally thought this wiki was eligible for deletion
* 14:23 Reception123: DELETE FROM cw_wikis mpaqwiki ms43wiki msibattlegroundwiki msnhinet8wiki mt2bwiki mundanapediawiki mychartwiki myocodesharewiki nddbwiki (DP)
* 14:07 Reception123: mw1: sudo -u www-data php /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/removeDeletedWikis.php --wiki metawiki
* 14:06 Reception123: DELETED FROM cw_wikis materialsdatabasewiki  mathsclubwiki matogewiki mbarwiki mecanonwiki mediaconflictwiki melvinsamuelwiki mgarciawiki mikecurtinworkwiki mindladlewiki minoxrigawiki mmgwiki mmittewiki mojavestormwiki momiwiki mosaicschoolwiki (DP)
* 13:59 Reception123: reception@mw1:~$ sudo -u www-data php /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/removeDeletedWikis.php --wiki metawiki
* 13:58 Reception123: DELETED FROM cw_wikis johnsonfamilycookbookwiki jricwiki knowlabwiki lasenallawiki lclwikiwiki learningskillswiki learnthegeekwiki lifelinewiki liutaiwikiwiki llwwiki log4techwiki lugjuwiki lyingseawiki makewiki (DP)
* 13:52 Reception123: mw1: sudo -u www-data php /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/removeDeletedWikis.php --wiki metawiki
* 13:51 Reception123: DELETE FROM cw_wikis insteadwiki  instylewiki ioncontainerswiki iqtwiki ironspherewiki isswiki jbkwwiki jeanfredericwiki jeranwiki jeremysrpgswiki (DP)
* 13:37 Reception|away: reception@mw1:/srv/mediawiki/w/extensions/MirahezeMagic/maintenance$ sudo -u www-data php manageInactiveWikis.php --wiki metawiki --warn --close

## 2016-11-11 

* 16:52 Southparkfan: applied Parsoid security update
* 14:59 Reception|away: sudo -u www-data php rebuildLocalisationCache.php --wiki extloadwiki on mw*
* 09:20 Reception|away: sudo -u www-data php /srv/mediawiki/w/maintenance rebuildLocalisationCache.php --wiki extloadwiki on mw*

## 2016-11-09 

* 19:18 Southparkfan: restarted jobrunner and jobchron on mw1
* 18:19 Southparkfan: deleted all redis keys matching '*:filerepo:wikimediacommons:*' and '*:diff:version:*' to check memory impact

## 2016-11-08 

* 19:48 Reception|away: mw1: sudo -u www-data php /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/removeDeletedWikis.php --wiki metawiki
* 19:47 Reception|away: DELETED FROM cw_wikis hexaversewiki hokifywiki homewiki hubmakerswiki iaccswiki ibdwiki iblwiki imagewiki  imgopowiki indexwiki
* 19:32 Reception|away: mw1: sudo -u www-data php /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/removeDeletedWikis.php --wiki metawiki
* 19:31 Reception|away: DELETE FROM cw_wikis golanghowtowiki grtitreprovisoirewiki gumedienwiki gympawikiwiki gyrobotwiki habitatpartageboulonnaiswiki haftpflichtheldenwiki harserwiki
* 14:19 Southparkfan: ran find /tmp/ -mtime +5 -delete on misc1

## 2016-11-07 

* 19:31 John: rm dbperformance.log* on mw*

## 2016-11-05 

* 17:37 PuppyKun: mv /srv/mediawiki-static/kaydadegerwiki /srv/mediawiki-static/vukfwiki on cp1, confirmed file permissions
* 17:36 PuppyKun: updated metawiki.cw_wikis, centralauth.localuser, centralauth.localnames
* 17:34 PuppyKun: created vukufwiki; source /home/ndkilla/kaydadegerwiki.sql
* 17:33 PuppyKun: dumped kaydadegerwiki to /home/ndkilla/kaydadegerwiki.sql
* 11:13 Southparkfan: restarted jobchron and jobrunner on mw1
* 10:36 Reception|away: reception@mw1:/srv/mediawiki/w/extensions/Translate/scripts$ sudo -u www-data php createMessageIndex.php --wiki nvcwiki

## 2016-11-04 

* 18:45 Reception123: sudo -u www-data foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/maintenance/sql.php /srv/mediawiki/w/extensions/FlaggedRevs/backend/schema/mysql/FlaggedRevs.sql on mw*
* 18:10 Southparkfan: restarted adminbot on misc1
* 19:02 Reception123: /srv/mediawiki/w/maintenance$ sudo -u www-data php rebuildLocalisationCache.php --wiki extloadwiki on mw*

## 2016-11-01 

* 16:56 Reception123: mw1: sudo -u www-data php /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/removeDeletedWikis.php --wiki metawiki
* 16:55 Reception123: DELETE FROM cw_wikis forgottenwiki francisfranckwiki freedgewiki freeswitchwiki frtitreprovisoirewiki fvcwikiwiki gamesfortuttiwiki gappswiki gemwikiwiki geramaxwiki (DP)
* 16:47 Reception123: mw1: sudo -u www-data php /srv/mediawiki/w/extensions/MirahezeMagic/ maintenance/removeDeletedWikis.php --wiki metawiki
* 16:47 Reception123: DELETE FROM cw_wikis encscheckinwiki enlotwiki entitreprovisoirewiki entropediawiki envsciwiki epsolawiki escawiki etec510wiki evolawiki f14swiki familytreewiki fenaloniawiki fms23wiki fmu82wiki fonehelpwiki (DP)

## 2016-10-31 

* 18:45 Southparkfan: upgraded mw1 and mw2. restarted ganglia-monitor on all mwservers

## 2016-10-30 

* 19:02 Southparkfan: properly deleted CA rows for cajadeherramientaswiki
* 17:25 Southparkfan: same for easyspecwiki edmbotwiki eenfwiki elainarmuawiki elderwoodwiki elsiesworldwiki emswiki zepaltusprojectwiki
* 17:25 Southparkfan: same for czechmodwikiwiki d4rkst4rwiki dacopancmwiki datasciencewiki decrypticwiki deernswiki devpostwiki dewelcomewiki diem25ocwiki dieselpunk1936wiki digigridwiki dishonesttruthwiki diylifewiki dofowikiwiki dokuwiki dpwwikiwiki dreamlineswiki drunkenpeasantswikiwiki dzcommunitywiki easy2rolwiki
* 17:25 Southparkfan: same for bizmowiki blogaversewiki bobhtwiki bogwidwiki bsg78wiki cajadeherramientaswiki capitaluwiki cardanoleakswiki carraratorswiki cbcwiki chandruswethswiki chessypigwiki codependwiki cogdevsocwiki cogdevsocwiki coldtownewiki communityofdissentwiki compendiumwiki compmathwiki convoywiki coonetwiki crackingrockwiki creersonarbrewiki cs422wiki
* 17:24 Southparkfan: deleted the following wikis (mysql/static): ackbwiki ujhswiki hylerwiki aflinluuundwiki alfster2012wiki winprohelpwiki aiplcwiki albawiki anicarpediawiki apgwikiwiki ariawiki armonianwiki artelwiki ashtabulawiki asylothekwiki atchayamwiki atlantisgamemodewiki azadiwiki bcuwiki beloitwiki biaxwiki bibliographywiki bilgigonulluleriwiki biomedefensewiki
* 17:23 Reception|away: sudo -u www-data php /srv/mediawiki/w/extensions/MirahezeMagic/                                                                                        maintenance/removeDeletedWikis.php --wiki metawiki
* 17:07 Reception|away: reception@mw1:~$ sudo -u www-data php /srv/mediawiki/w/extensions/MirahezeMagic/                                                                                        maintenance/removeDeletedWikis.php --wiki metawiki
* 16:57 Reception|away: DELETE FROM cw_wikis WHERE wiki_dbname = 'zepaltusprojectwiki'; (DP)

## 2016-10-29 

* 17:14 Reception|away: DELETE FROM cw_wikis (drunkenpeasantswikiwiki dzcommunitywiki easy2rolwiki easyspecwiki edmbotwiki eenfwiki elainarmuawiki elderwoodwiki elsiesworldwiki emswiki)
* 17:08 Reception|away: DELETE FROM cw_wikis (digigridwiki dishonesttruthwiki diylifewiki dofowikiwiki dokuwiki dpwwikiwiki dreamlineswiki) (DP)
* 10:52 Reception123: DELETE FROM cw_wikis (compendiumwiki compmathwiki convoywiki coonetwiki crackingrockwiki creersonarbrewiki cs422wiki czechmodwikiwiki d4rkst4rwiki dacopancmwiki datasciencewiki decrypticwiki deernswiki devpostwiki dewelcomewiki diem25ocwiki dieselpunk1936wiki)

## 2016-10-28 

* 17:39 Reception123: DELETE FROM cw_wikis ( capitaluwiki cardanoleakswiki carraratorswiki cbcwiki chandruswethswiki chessypigwiki codependwiki cogdevsocwiki cogdevsocwiki coldtownewiki communityofdissentwiki) (DP)
* 17:32 Reception123: DELETE FROM cw_wikis (bcuwiki beloitwiki biaxwiki bibliographywiki bilgigonulluleriwiki biomedefensewiki bizmowiki blogaversewiki bobhtwiki bogwidwiki bsg78wiki cajadeherramientas) (DP)
* 17:25 Reception123: DELETE FROM cw_wikis ( artelwiki, ashtabulawiki, asylothekwiki, atchayamwiki, atlantisgamemodewiki, azadiwiki) (DP)
* 17:19 Reception123: DELETED FROM cw_wikis (aiplcwiki, albawiki, anicarpediawiki, apgwikiwiki, ariawiki, armonianwiki) (DP)
* 17:08 Reception123: DELETE FROM cw_wikis WHERE wiki_dbname = 'winprohelpwiki'; (DP)
* 17:04 Reception123: DELETE FROM cw_wikis WHERE wiki_dbname = 'alfster2012wiki'; (DP)
* 17:01 Reception123: DELETE FROM cw_wikis WHERE wiki_dbname = 'aflinluuundwiki'; (DP)

## 2016-10-27 

* 20:22 PuppyKun: purged applewiki.tk from varnish
* 19:44 PuppyKun: depooled cp2, stopped varnish, messing around with nginx
* 19:19 PuppyKun: reloaded nginx on all appservers
* 19:02 PuppyKun: reloaded nginx on all appservers for applewiki.tk ssl
* 17:45 Reception123: reception@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php populateCategory.php --wiki anduinwiki
* 15:08 John: phabricator upgraded
* 15:05 John: upgrading phabricator
* 14:34 John: changed permissions of avatar/awards to www-data
* 14:30 John: restarted phabricator daemons
* 14:25 John: created databases tables on applebranchwiki which weren't created despite they exist on every other wiki
* 13:58 John: restarted jobrunner on mw1

## 2016-10-26 

* 21:14 Southparkfan: reboot bacula1 for kernel upgrade
* 18:52 Reception|away: DELETE FROM cw_wikis WHERE wiki_dbname = 'hylerwiki';
* 13:40 Reception|away: copied /awards and /avatars to applebranchwiki (SocialProfile)
* 13:06 Reception|away: DELETE FROM cw_wikis WHERE wiki_dbname = 'ujhswiki';

## 2016-10-25 

* 19:13 Reception|away: DELETE FROM cw_wikis WHERE wiki_dbname = 'ackbwiki'; (DP)
* 18:53 Reception|away: reception@mw2:/srv/mediawiki/w/maintenance$ sudo -u www-data php importDump.php --wiki corydoctorowwiki /home/reception/corydoctorow_pages_current_241016.xml/corydoctorow_pages_current_241016.xml

## 2016-10-22 

* 18:32 Reception123: reception@mw2:/srv/mediawiki/w/extensions/MirahezeMagic/maintenance$ sudo -u www-data php manageInactiveWikis.php --wiki metawiki --warn --close
* 18:26 Southparkfan: repooled mw1
* 18:03 Southparkfan: depooling mw1
* 15:23 Reception123: sudo -u www-data php rebuildLocalisationCache.php --wiki extloadwiki on mw*

## 2016-10-21 

* 18:54 Southparkfan: cancelled previous job and deleted associated volumes. switched bacula to db2 server-side (GH down), queued job again
* 18:43 Southparkfan: Bacula: deleted corrupt(?) backups of database, queued a job for a new backup run

## 2016-10-20 

* 15:56 John: removed nice on LC on mw1
* 15:54 Reception123: nice rebuildLC cache 10
* 15:53 Reception123: sudo -u www-data php rebuildLocalisationCache.php --wiki extloadwiki on mw1
* 15:40 Reception123: reception@mw2:/srv/mediawiki/w/maintenance$ sudo -u www-data php importDump.php --wiki fiqnwiki /home/reception/Wikipedia-20160930221558.xml
* 15:39 Reception123: sudo -u www-data php rebuildLocalisationCache.php --wiki extloadwiki on mw*
* 15:09 Reception123: sudo -u www-data php rebuildLocalisationCache.php --wiki extloadwiki on mw*

## 2016-10-19 

* 22:41 John: removed deleted databases from centralauth

## 2016-10-18 

* 15:55 John: restarted ganglia-monitor on all servers, ganglia is back
* 14:13 John: restarted jobrunner

## 2016-10-16 

* 21:05 Southparkfan: restarted gmetad on misc2, and restarted gmond on all servers
* 17:49 Reception|away: copied /avatars and /awards to takethatwikiwiki
* 15:42 Reception123: DELETE FROM cw_wikis WHERE wiki_dbname = 'simplukarropediawiki';

## 2016-10-15 

* 21:34 Southparkfan: restarting ganglia-monitor on all hosts for the 3rd time
* 20:48 Southparkfan: restarted ganglia-monitor on all hosts. network maintenance seems to have impacted ganglia monitoring for several hosts
* 14:11 Reception123: DELETE FROM cw_wikis WHERE wiki_dbname = 'etpowiki';

## 2016-10-14 

* 18:47 Reception|away: sudo -u www-data foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/maintenance/sql.php /srv/mediawiki/w/extensions/ArticleFeedbackv5/sql/ArticleFeedbackv5.sql (mw2)
* 17:54 Reception|away: sudo -u www-data foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/maintenance/sql.php /srv/mediawiki/w/extensions/ArticleRatings/ratings.sql
* 06:50 John: rebooted mw1, mw2 and misc2
* 01:14 PuppyKun: restarted both mh bots

## 2016-10-13 

* 16:37 Southparkfan: ran populateCategory.php on anduinwiki

## 2016-10-12 

* 18:37 Reception|away: sudo -u www-data php rebuildLocalisationCache.php --wiki extloadwiki on mw*

## 2016-10-11 

* 19:01 Reception123: sudo -u www-data php rebuildLocalisationCache.php --wiki extloadwiki
* 18:36 Southparkfan: cp1 depooled from traffic. Stopping Varnish

## 2016-10-10 

* 17:18 Reception|away: sudo -u www-data php rebuildLocalisationCache.php --wiki extloadwiki on mw*

## 2016-10-09 

* 14:43 PuppyKun: ndkilla@mw2: sudo -u www-data foreachwikiindblist /srv/mediawiki/dblistall.dblist /srv/mediawiki/w/maintenance/sql.php /srv/mediawiki/w/extensions/MediaWikiChat/sql/chat_users.sql
* 14:35 PuppyKun: ndkilla@mw2: sudo -u www-data foreachwikiindblist /srv/mediawiki/dblistall.dblist /srv/mediawiki/w/maintenance/sql.php /srv/mediawiki/w/extensions/MediaWikiChat/sql/chat.sql
* 08:58 Southparkfan: wiped everything in /tmp on misc1
* 08:58 Southparkfan: restarted apache2

## 2016-10-08 

* 18:24 Reception|away: reception@mw2:/srv/mediawiki/w/maintenance$ sudo -u www-data php importDump.php --wiki applewikiwiki /home/reception/ipod_pages_full.xml
* 14:42 Reception|away: reception@mw2:/srv/mediawiki/w/extensions/MirahezeMagic/maintenance$ sudo -u www-data php manageInactiveWikis.php --wiki metawiki --warn --close
* 09:00 Reception123: sudo -u www-data php rebuildLocalisationCache.php --wiki extloadwiki  on mw*
* 01:42 PuppyKun: restarted nginx on all appservers
* 01:39 PuppyKun: restarted nginx on all appservers
* 01:36 PuppyKun: restarted nginx on all appservers
* 01:35 PuppyKun: restarted mh logbot and icinga-miraheze (the first was on accident, the second was dead)
* 01:31 PuppyKun: restarted nginx on all appservers
* 01:27 PuppyKun: restarted nginx on all appservers
* 01:08 PuppyKun: dropped addawiki database
* 01:06 PuppyKun: moved /srv/mediawiki-static/addawiki to /srv/mediawiki-static/imperiuswiki
* 01:00 PuppyKun: renamed addawiki to imperiuswiki in centralauth.localuser and centralauth.localnames
* 00:59 PuppyKun: renamed addawiki to imperiuswiki in cw_wikis
* 00:59 PuppyKun: sqldump'd addawiki and sourced it into imperiuswiki

## 2016-10-07 

* 21:17 Southparkfan: started mysql on db1

## 2016-10-06 

* 18:15 Southparkfan: wiped varnish storage on cp1 and restarted varnish
* 16:45 John: rebooting mw2, unresponsive
* 13:28 Southparkfan: killed a ping6 process on misc2 that was running for almost 3 months

## 2016-10-05 

* 21:54 NDKilla: removeDeletedWikis.php --wiki metawiki (deleted local users from testingpleaseignorewiki, yggdrasilwiki, throisarwiki)
* 21:07 John: estimated uptime for db1 on cancellation, 457 days. That's impressive. 457 days since Miraheze began on Oct 22nd too then.
* 21:05 John: logged a cancellation request for db1 to be completed on OCT 22nd
* 20:50 John: stopping MySQL on db1
* 20:47 John: db1->db2 is complete
* 17:10 John: phabricator and piwik are now on db2
* 13:01 Reception|away: /srv/mediawiki/w/maintenance$ sudo -u www-data php rebuildLocalisationCache.php --wiki extloadwiki on mw*

## 2016-10-04 

* 22:01 John: stopping phd daemons
* 21:58 Southparkfan: Ran git reset --hard origin/master for puppet git on all cache proxies. Ran puppet on cp1 (which restarted Varnish), now fighting with a lack of RAM on cp2 to run puppet there too...
* 21:53 John: for puppet, to clarify
* 21:53 John: protected "master" branch in GitHub
* 15:38 John: upgraded
* 15:37 John: upgrading phabricator
* 15:23 John: SocialProfile SQL changes on all wikis
* 01:59 PuppyKun: PLEASE FOR THE LOVE OF GOD UPDATE THE SSL SCRIPT AND THE DIRECTIONS THIS ENTIRE ISSUE WAS CAUSED BY PUSHING THE WRONG KEY TO PRIVATE-GIT BECAUSE THERE WERE 3 ATT KEYS
* 01:59 PuppyKun: puppet force-push put mw1 back in production, worked anyways
* 00:18 PuppyKun: sudo /root/ufw-fix on cp2

## 2016-10-03 

* 18:11 Reception123: reception@mw2:~$ sudo -u www-data cp /home/reception/techeducationwiki03102016.xml /mnt/mediawiki-static/dumps
* 18:10 Reception123: sudo -u www-data php dumpBackup.php --wiki techeducationwiki --full > /home/reception/techeducationwiki03102016.xml

## 2016-10-02 

* 12:05 Reception|away: reception@mw1:/mnt/mediawiki-static/dumps$ sudo -u www-data rm -rf nissanecuwiki28092016.xml (0 byte file)
* 12:02 Reception|away: sudo -u www-data cp /home/reception/nissanecuwiki02102016.xml /mnt/mediawiki-static/dumps
* 12:01 Reception|away: reception@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php dumpBackup.php --wiki nissanecuwiki --full > /home/reception/nissanecuwiki02102016  (not done correctly the first time.)

## 2016-09-30 

* 18:51 PuppyKun: purged 7 mysql binlogs
* 18:05 PuppyKun: copied SocialProfile images to allthetropeswiki
* 17:08 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance importDump.php --wiki fiqnwiki /home/reception/Wikipedia-20160930163843.xml
* 17:07 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance importDump.php --wiki fiqnwiki /home/reception/Wikipedia-20160930163829.xml
* 17:07 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance importDump.php --wiki fiqnwiki /home/reception/Wikipedia-20160930163715.xml
* 16:41 PuppyKun: rename idtestwiki to trexwiki in centralauth.localuser and centralauth.localnames
* 16:31 PuppyKun: cp1: sudo -u www-data mv /srv/mediawiki-static/idtestwiki /srv/mediawiki-static/trexwiki
* 16:29 PuppyKun: copied idtestwiki db to trexwiki db, updated cw_wikis, then DROPPED DATABASE idtestwiki;

## 2016-09-28 

* 14:39 Reception123: sudo -u www-data cp /home/reception/nissanecuwiki28092016.xml /mnt/mediawiki-static/dumps
* 14:36 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance dumpBackup.php --wiki nissanecuwiki --full > /home/reception/nissanecuwiki28092015.xml
* 14:33 Reception123: DELETE FROM cw_wikis WHERE wiki_dbname = 'throisarwiki'; (T803)
* 14:18 Reception123: sudo -u www-data nice -n 10 php /srv/mediawiki/w/maintenance/rebuildLocalisationCache.php --wiki extloadwiki

## 2016-09-27 

* 23:00 PuppyKun: service icingabot restart

## 2016-09-24 

* 17:30 PuppyKun: root@cp1:/srv/mediawiki-static# chown -R www-data applewikiwiki
* 16:33 Reception123: copied /avatars and /awards to /mnt/mediawiki-static/applewikiwiki
* 09:02 Reception|away: sudo -u www-data nice -n 19 php /srv/mediawiki/w/maintenance/importImages.php --wiki ayrshirewiki --search-recursively /home/reception/images1 (failed the first time; internet problem)

## 2016-09-23 

* 19:12 Reception|away: sudo -u www-data nice -n 19 php /srv/mediawiki/w/maintenance/importImages.php --wiki ayrshirewiki --search-recursively /home/reception/images1   (mw1)
* 19:01 Reception|away: reception@mw1:/srv/mediawiki/w/extensions/MirahezeMagic/maintenance$ sudo -u www-data php manageInactiveWikis.php --wiki metawiki --warn --close
* 16:37 John: [SECURITY] upgraded MariaDB
* 16:18 Reception123: sudo -u www-data nice -n 10 php /srv/mediawiki/w/maintenance/rebuildLocalisationCache.php --wiki extloadwiki

## 2016-09-21 

* 19:16 PuppyKun: 3952 (process ID) old priority 15, new priority 19
* 19:04 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildLocalisationCache.php --wiki extloadwiki on mw*
* 17:01 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildLocalisationCache.php --wiki extloadwiki on mw*
* 16:41 Reception123: reception@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data nice -n 10 php importDump.php --wiki anduinwiki /home/reception/KGV20160911-full.xml

## 2016-09-20 

* 15:55 Reception|away: reception@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php rebuildrecentchanges.php --wiki supernamuwiki

## 2016-09-19 

* 22:46 PuppyKun: reverted edits to php.ini and /etc/hosts and 'service apache2 force-reload' on misc1
* 22:01-22:46: Lots of random edits to apache and phabricator on misc1 trying to debug `arc download`
* 22:01 PuppyTemp: temporarily enabled Phabricator registration via GitHub then disabled it
* 19:22 John: phabricator upgraded
* 19:21 John: upgrading phabricator

## 2016-09-18 

* 16:39 Reception|away: renice10 on import process
* 16:37 Reception|away: reception@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php importDump.php --wiki supernamuwiki /home/reception/oriwiki20160725.xml

## 2016-09-17 

* 15:51 Southparkfan: purged a lot of binlogs to free up space on db1
* 15:47 Southparkfan: restarted icingabot

## 2016-09-16 

* 17:00 Reception123: reception@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php updateSpecialPages.php --wiki jayuwikiwiki

## 2016-09-14 

* 16:51 John: restarted jobrunner
* 15:51 John: running jobs
* 01:43 PuppyKun: manually ran jobs on cpiwiki

## 2016-09-13 

* 17:03 John: rm /tmp/* (full of importImages junk)

## 2016-09-12 

* 16:40 John: phabricator updated
* 16:38 John: upgrading phabricator

## 2016-09-11 

* 15:55 Reception123: reception@mw1:/srv/mediawiki/w/extensions/MirahezeMagic/maintenance$ sudo -u www-data php manageInactiveWikis.php --wiki metawiki --warn --close
* 15:50 Reception123: reception@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php rebuildrecentchanges.php --wiki anduinwiki (after import)
* 15:35 Reception123: reception@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php importDump.php --wiki anduinwiki /home/reception/KGV20160911-full.xml (nice 10)
* 13:50 Reception123: renice 10 on import process
* 13:31 Reception123: reception@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php importDump.php --wiki anduinwiki /home/reception/KGV20160911-full.xml

## 2016-09-05 

* 19:31 Southparkfan: mw1 repooled, back in service
* 18:55 Southparkfan: depooled mw1

## 2016-09-04 

* 16:07 Southparkfan: re-enabled puppet
* 15:46 Southparkfan: disabled puppet on cp2
* 03:08 PuppyKun: restarted adminbot service on misc1

## 2016-09-03 

* 15:51 Southparkfan: killed ping6 process on cp1 running since July 19
* 15:51 Southparkfan: enabled 5xx Varnish logging on all cps: varnishlog -D -q "RespStatus >= 500" -w /var/log/varnish/varnish50x.log

## 2016-09-02 

* 22:30 John: deleted 9G static.gz file owned by Southparkfan from January
* 17:55 John: deleted db1 binlogs
* 16:34 John: restarted ganglia-monitor on bacula1

## 2016-09-01 

* 17:03 Southparkfan: upgraded cp1. Restarted ganglia-monitor
* 16:58 PuppyKun: updated cachet api token in private git
* 16:56 PuppyKun: regenerated NDKilla's api token on cachet

## 2016-08-30 

* 16:59 John: added wiki_settings column to cw_wikis, self-made query, SPF never published his
* 16:57 John: running an ALTER on cw_wikis

## 2016-08-29 

* 16:19 Southparkfan: attempting to run cw_wikis schema change again
* 15:57 PuppyKun: restarted nginx on (mw|cp)[12]
* 15:55 Reception123: sudo -u www-data nice -n19 php /srv/mediawiki/w/maintenance/importImages.php --wiki ayrshirewiki --search-recursively /home/reception/images
* 15:47 PuppyKun: ran /root/ufw-fix on cp2
* 15:21 Reception|away: reception@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php rebuildrecentchanges.php --wiki ayrshirewiki (import done)
* 14:36 Southparkfan: set nice 19 on above mentioned importDump.php process
* 14:31 Southparkfan: set nice 10 on importDump.php process (mw1) making Miraheze slower
* 01:48 PuppyKun: restarted jobrunner

## 2016-08-28 

* 18:03 John: dropped users: johnflewis@%, johnflewis@localhost, limesurvey@% and gerrit2@% from db1
* 17:56 John: removed global port access to an unknown IP on db1
* 17:53 John: removed bacula testing port on parsoid1
* 17:51 John: deleted several old DDoS related firewall rules on mw1
* 17:47 John: stopped and uninstalled gdnsd on misc2
* 15:25 Southparkfan: also deleted image directories for the following wikis: makedoniumwiki moonmanwikiwiki mot94wiki ndtestwiki parsoidwiki poserdazfreebiestestwiki putinwiki pxgprojectwiki quantixwiki robloxscriptorswiki rowelcomewiki rtcsnipwiki spiraltestwiki theestablishmentmapwiki tuwelcomewiki unnawiki wikiacawiki wikifuturewiki yggdrasilwiki
* 15:24 Southparkfan: deleted image directories for following wikis: advancedazrielangelwiki arwelcomewiki bzduropediawiki castironcookwiki chavezwiki cinemawiki cittanostraunserestadtwiki creedwiki dpwiki drspwiki drunkenpeasantswiki enwelcomewiki frwelcomewiki gameswiki grwelcomewiki imedroneswiki itwelcomewiki jubeatwikithwiki lidianowiki livinginicelandwiki
* 12:03 Reception123: reception@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php rebuildrecentchanges.php --wiki pluspiwiki (not updated)
* 10:27 John: ran importImages for pluspiwiki
* 09:59 John: rm /tmp/* on mw1

## 2016-08-27 

* 19:52 PuppyKun: ndkilla@mw2:/home/johnflewis$ sudo rm pluspi.xml
* 14:51 Reception123: ran sudo -u www-data php importDump.php --wiki pluspiwiki --uploads /home/reception/pluspi.xml/ (not all uploads were done; requested by user)
* 08:53 Reception|away: reception@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php importDump.php --wiki pluspiwiki --uploads /home/reception/pluspi.xml/ on mw1

## 2016-08-26 

* 21:40 PuppyKun: Starting "php importImages.php --wiki pluspiwiki /home/reception/images" on mw1
* 21:38 PuppyKun: imported pluspi wiki xml (for the 3rd time) with --debug --report 100, ran php rebuildrecentchanges.php --wiki pluspiwiki
* 15:45 Reception|away: reception@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php rebuildrecentchanges.php --wiki pluspiwiki (import done)
* 10:36 Reception|away: reception@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php importDump.php --wiki pluspiwiki /home/reception/pluspi.xml/pluspi.xml on mw1

## 2016-08-25 

* 21:25 John: ran ufw-fix on cp1
* 13:32 Reception|away: DELETE FROM cw_wikis WHERE wiki_dbname = 'yggdrasilwiki'; (requested; already in deleted.dblist)
* 00:08 John: deleted files in /home/ndkilla on cp1

## 2016-08-24 

* 21:28 John: ran ufw-fix on cp2
* 20:04 John: MariaDB [allthetropeswiki]> DROP TABLE _searchindex_old;
* 14:55 Reception123: ran sudo -u www-data php dumpBackup.php --wiki sterbalssundrystudieswikiwiki --full > /home/reception/sterbalssundrystudieswiki24082016.xml
* 12:49 Reception123: ran sudo -u www-data php dumpBackup.php --wiki maiasongcontestwiki --full > /home/reception/maiasongcontest24082016.xml
* 07:27 Reception123: ran sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildLocalisationCache.php --wiki extloadwiki on mw* (new ext)

## 2016-08-23 

* 23:02 John: rebuilding /srv/mediawiki on mw2, bad git history left over from original upgrade
* 01:00 John: restarted jobrunner and jobchron on mw1 - DB issue earlier caused the services to fail

## 2016-08-22 

* 22:20 John: fixed firewall on cp1
* 17:33 Southparkfan: JohnLewis ran rebuildall.php to fix imagelinks table (T644)

## 2016-08-21 

* 21:47 Southparkfan: restarted Varnish on cp2 to free memory for puppet
* 17:51 Reception|away: ran sudo -u www-data php updateSpecialPages.php --wiki amaninfowiki (UnusedFiles not working) on mw*

## 2016-08-18 

* 18:01 Reception|away: add yggdrasilwiki to deleted.dblist and remove from all.dblist
* 04:48 Reception123: added testingpleaseignorewiki to deleted.dblist (was created in error)

## 2016-08-17 

* 03:19 Reception123: ran reception@mw1:/srv/mediawiki/w/extensions/MirahezeMagic/maintenance$ sudo -u www                                                                                        -data php manageInactiveWikis.php --wiki metawiki --warn --close

## 2016-08-15 

* 20:17 PuppyKun: dropped coreyeswiki, lomithradienwiki, and tanakiwiki databases; 122, 131, and 131 rows respectively.
* 20:13 PuppyKun: removeDeletedWikis.php 3 local names removed from coreyeswiki, 6 removed from lomithradienwiki, 2 removed from tanakiwiki
* 20:08 PuppyKun: MariaDB [metawiki]> DELETE FROM cw_wikis WHERE wiki_dbname="tanakiwiki";
* 20:08 PuppyKun: MariaDB [metawiki]> DELETE FROM cw_wikis WHERE wiki_dbname="lomithradienwiki";

## 2016-08-14 

* 17:06 John: upgraded Phabricator
* 16:20 John: creating wikibase tables on all wikis
* 15:06 Reception|away: ran sudo -u www-data php dumpBackup.php --wiki testwiki --full > /home/reception/testwiki14082016.xml (not done properly the first time)
* 15:02 Reception|away: ran sudo -u www-data php dumpBackup --wiki testwiki --full > /tmp/testwiki14082016.xml
* 12:54 John: added wb tables to extloadwiki
* 11:07 John: ran jobqueue per type for sizing estimations
* 11:06 Reception123: reception@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php rebuildrecentchanges.php --wiki botwikirecoverywiki (import done)
* 10:06 Reception123: reception@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php importDump.php --wiki botwikirecoverywiki < /tmp/botwikirecoverywiki.xml
* 04:19 Reception123: ran sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/maintenance/runJobs.php on mw*
* 04:05 Reception123: ran sudo -u www-data php importDump.php --wiki botwikirecoverywiki /tmp/botwikirecoverywiki.xml (but failed)

## 2016-08-13 

* 01:35 PuppyKun: marked redis as operational on cachet

## 2016-08-12 

* 14:07 PuppyKun: deleted 2096 resourceloader keys, will check to see if these keep getting created
* 04:06 Reception123: ran sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/maintenance/runJobs.php
* 04:05 Reception123: sudo service jobrunner restart

## 2016-08-11 

* 17:34 Reception123: ran sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/maintenance/runJobs.php
* 17:23 Reception123: sudo service jobrunner start
* 14:15 PuppyKun: restarted redis (with a lower max memory)
* 03:38 PuppyKun: deleted 1645 diff keys
* 03:19 PuppyKun: deleted 1582 resourceloader keys
* 02:36 PuppyKun: nohup sudo -u www-data bash -c "/usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/maintenance/runJobs.php > /var/log/mediawiki/cron/jobqueue.log" &
* 02:03 PuppyKun: ensured runJobs cron creation on mw1
* 02:02 PuppyKun: stopped jobrunner on mw1
* 01:26 PuppyKun: restarted redis-server (OOM at 0043 server time)
* 00:51 labster: ran php /srv/mediawiki/w/maintenance/showJobs.php --group --wiki allthetropeswiki and it took two whole hours thanks to me editing a template

## 2016-08-10 

* 20:45 labster: running sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/maintenance/runJobs.php
* 15:39 PuppyKun: deleted ~3000 diff keys (res+virt mem usage over limit)
* 12:44 PuppyKun: restarted icinga
* 11:41 PuppyKun: deleted 145 *:diff:* redis keys
* 11:28 PuppyKun: deleted 114 "*:diff:*" keys in redis
* 11:21 PuppyKun:  sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/maintenance/runJobs.php
* 11:18 PuppyKun: restarted redis (OOM'd at 1010 server time)

## 2016-08-09 

* 21:49 PuppyKun: restarted jobrunner
* 21:49 PuppyKun: restarted redis
* 21:13 PuppyKun: restarted redis on misc2 (oom)
* 17:28 Reception123: ran  sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/maintenance/runJobs.php
* 17:27 Reception123: sudo service jobrunner restart
* 16:04 PuppyKun: restarted jobrunner on mw1
* 14:20 Southparkfan: force-run of runJobs.php on all wikis
* 14:09 Southparkfan: restarted jobrunner on mw1. Not in failed state (unlike previous failures)
* 10:45 Reception123: ran sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/maintenance/runJobs.php (restarting jobrunner service has no effect)
* 10:44 Reception123: restarted jobrunner on mw1 (still doesn't work)
* 10:09 Reception123: restarted jobrunner on mw1 (T621, SPF)
* 04:42 Reception123: ran sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/maintenance/runJobs.php on mw* (NOTE: I know that I shouldn't have done this, but there was no other sysadmin and this issue is urgent to resolve as more people were complaining about it.)
* 04:20 Reception123: ran sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildLocalisationCache.php --wiki extloadwiki (error with categories; making sure it's not because of this)

## 2016-08-08 

* 18:06 Reception123: ran sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildLocalisationCache.php --wiki extloadwiki on mw*
* 11:14 PuppyKun: restarted redis-server on misc2. Not sure what affect this has on current logins but the service stopped unexpectedly roughly 13 hours ago
* 09:57 Reception123: ran sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildLocalisationCache.php --wiki extloadwiki on mw* (attempting to fix error with extension)

## 2016-08-07 

* 22:28 John: restarted jobrunner (again...)
* 16:39 John: restarting jobrunner, segfualt'd yesterday noon.
* 11:43 John: manually queueing all bacula jobs to be ran
* 11:42 John: remove mapping of bacula1.miraheze.org->127.0.1.1 on bacula1
* 04:51 Reception123: ran sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildLocalisationCache.php --wiki extloadwiki
* 04:27 Reception123: ran sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildLocalisationCache.php --wiki extloadwiki on mw*

## 2016-08-06 

* 07:41 Reception123: !ran sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildLocalisationCache.php --wiki extloadwiki on mw*
* 05:59 PuppyKun: fixed john breaking things
* 05:55 PuppyKun: abandoned local config changes on mw1 (took ATT out of readonly)
* 02:58 John: an... eventful MediaWiki 1.27 upgrade has now completed.
* 02:19 John: changed miraheze/mediawiki's default branch to REL1_27
* 02:14 John: MW 1.27 tables on all wikis, jobrunner disabled on mw1, running jobs to ensure completion right now

## 2016-08-05 

* 23:14 John: disable puppet on mw1 + make allthetropeswiki readonly
* 23:06 John: updated parsoid to 0.5.1
* 22:01 John: removing mediawiki on mw2, re-running puppet to check all changes are in git, potential MW1.27 upgrade shortly
* 21:23 John: silences mw2 in icinga for 2 hours
* 21:16 John: applying REL1_27 code on mw2, monitoring mw1 just in case
* 21:13 John: removing local commits to Widget extension, causing excessive puppet runs...
* 05:08 Reception123: ran sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildLocalisationCache.php --wiki extloadwiki on mw*

## 2016-08-04 

* 21:05 Southparkfan: disabling puppet on misc2
* 19:17 Reception123: ran sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildLocalisationCache.php --wiki extloadwiki on mw*
* 13:23 PuppyKun: sudo chown -R www-data:www-data /srv/mediawiki/w/extensions/Widgets/compiled_templates on mw*

## 2016-08-03 

* 18:48 John: removed manifests in private git - entirely hiera ran
* 17:56 John: renamed existing private hiera variables to new ones
* 17:50 John: converted all private information to hiera [internal note]
* 17:18 Southparkfan: restarted gmond on all servers
* 17:15 John: restart ganglia-monitor on all servers
* 16:52 John: restarted gmetad on misc2
* 16:19 John: removed binlogs on db1
* 15:45 PuppyKun: ran removeDeletedWikis.php after deleting the database, removed 18 local users
* 13:59 PuppyKun: created password for user ndkilla in icinga
* 13:45 Reception123: ran reception@mw1:/srv/mediawiki/w/extensions/MirahezeMagic/maintenance$ sudo -u www-data php manageInactiveWikis.php --wiki metawiki --warn --close
* 13:33 PuppyKun: ensured Reception123's shell account was created
* 12:45 PuppyKun: dropped database for ayudasocialwiki and removed it from deleted.dblist
* 12:42 PuppyKun: restarted nginx again
* 12:26 PuppyKun: MariaDB [metawiki]> delete from cw_wikis where wiki_dbname="ayudasocialwiki";
* 12:16 PuppyKun: purged www and non-www thinkingliquid.org domains from cache
* 12:14 PuppyKun: restarted nginx on appservers
* 11:56 PuppyKun: dropped database nddbwiki
* 11:56 PuppyKun: deleted nddbwiki from cw_wikis

## 2016-08-02 

* 18:03 Southparkfan: wiped ganglia data for vultr.guest + bacula1
* 16:24 PuppyKun: attempted to drop easygovewiki database, didn't exist. emptying deleted.dblist
* 16:24 PuppyKun: MariaDB [(none)]> DROP DATABASE pulsarwiki; Query OK, 123 rows affected
* 16:19 PuppyKun: MariaDB [(none)]> DROP DATABASE gameswiki; Query OK, 123 rows affected
* 16:17 PuppyKun: MariaDB [(none)]> DROP DATABASE quantixwiki; Query OK, 123 rows affected
* 16:12 PuppyKun: MariaDB [metawiki]> delete from cw_wikis where wiki_dbname="gameswiki";
* 16:09 PuppyKun:  MariaDB [metawiki]> delete from cw_wikis where wiki_dbname="quantixwiki";
* 03:52 PuppyKun: deleted cw_wikis entry for pulsarwiki per founder request on my talk page

## 2016-08-01 

* 18:36 John: all private repos reference git-private.miraheze.org now, not misc1.miraheze.org / misc1's IP

## 2016-07-31 

* 20:20 John: phabricator upgraded
* 20:17 John: upgrading phabricator
* 13:28 John: started phd daemons
* 09:34 Southparkfan: restarted ganglia-monitor on bacula1

## 2016-07-30 

* 22:02 John: reinstalled bacula1
* 21:21 John: taking bacula1 down for reinstall
* 21:20 Southparkfan: restarted php5-fpm to pick up config changes

## 2016-07-29 

* 16:08 PuppyKun: restarted nginx on (mw|cp)[12]

## 2016-07-27 

* 11:26 Southparkfan: installed security updates on mwservers

## 2016-07-26 

* 22:03 Southparkfan: purged some binlogs on db1
* 21:57 Southparkfan: restarted php5-fpm on both mwservers

## 2016-07-25 

* 20:31 penguinstyles: imported xml dump for 'dwplivewiki' per request (T547) && rebuilt recent changes for 'dwplivewiki'
* 17:28 Southparkfan: starting Piwik upgrade
* 13:28 PuppyKun: varnish purge thelonsdalebattalion.(miraheze.org|co.uk)
* 13:24 PuppyKun: restarted nginx on (mw|cp)[12]
* 12:16 John: rebooting mw2, unresponsive
* 11:33 John: rebooting bacula1
* 05:00 penguinstyles: imported xml dump for 'starsetonlinewiki' per request (T540)

## 2016-07-23 

* 13:16 Southparkfan: imported dump for droneregulationwiki

## 2016-07-22 

* 19:12 Southparkfan: ran sudo varnishadm 'ban req.http.Host == wiki.dwplive.com && req.url ~ "^/w/load.php"' on cp2
* 15:14 John: MariaDB [(none)]> DROP DATABASE easygovwiki;
* 12:35 Southparkfan: restarted ganglia-monitor on bacula1 after reboot for unknown reason

## 2016-07-20 

* 21:38 Southparkfan: truncated l10n_cache for loginwiki too
* 21:32 Southparkfan: truncated metawiki.l10n_cache. Saved approximately 873MB of space
* 21:16 Southparkfan: removed STATIC-0011 volume to regain space
* 10:50 Southparkfan: ran updateArticleCount.php for lomithradienwiki with --update

## 2016-07-19 

* 18:46 Southparkfan: started jobrunner on mw1
* 18:44 John: rebooted cp1; fixed networking
* 18:43 John: rebooted mw1; fixed networking
* 16:24 John: rm allthetropes-images.gz on cp1; +2.2G
* 13:47 Southparkfan: restarted mysql, was flapping

## 2016-07-18 

* 15:58 John: rm'd MySQL bin logs -16G on db1
* 12:33 PuppyKun: ndkilla@mw1:/srv/mediawiki/w/extensions/MirahezeMagic/maintenance$ sudo php manageInactiveWikis.php --wiki metawiki --warn --close (466 warned, 0 closed)

## 2016-07-17 

* 11:52 Southparkfan: created @cp1:/srv/mediawiki-static/1year for some CSS assets

## 2016-07-16 

* 23:24 John: updated Phabricator
* 22:13 John: removed local commits on mw1 for 5 extensions that are old, no longer necessary or otherwise
* 20:27 John: all wikis should be consistent with database tables now.
* 20:19 John: ensured all databases (1143) have MsCalendar database tables
* 20:14 John: ensured all databases (943) have AJAXPoll database tables
* 20:05 John: ensured all databases (943) have VoteNY database tables
* 20:00 John: ensured all databases (779) have Comments database tables
* 19:55 John: ensured all databases (655) have WikiLove database tables
* 19:51 John: ensured all databases (651) have WikiForum database tables
* 19:45 John: ensured all databases (652) have SocialProfile database tables
* 19:15 John: ensured all databases (146) have PageTriage database tables
* 19:10 John: ensured all databases (6) have Flow database tables
* 19:08 John: ensured all databases (4) have Translate database tables
* 19:04 John: ensured all databases (1) have BetaFeatures database tables
* 19:03 John: ensured all databases (1) have Poll database tables
* 19:02 John: ensured all databases (4) have TimedMediaHandler database tables
* 18:59 John: ensured all databases (4) have TitleKey database tables

## 2016-07-15 

* 17:41 Southparkfan: increased HSTS for miraheze.org to 6 months
* 11:58 PuppyKun: ran update.php twice on jbkwwiki (first run failed because of global_block_whitelist table or whatever that common thing is)

## 2016-07-14 

* 22:37 Southparkfan: installed security updates on mw1 & mw2
* 19:42 Southparkfan: varnishadm 'ban req.http.Host == southparkfan.miraheze.org' @ cp1

## 2016-07-13 

* 10:09 Southparkfan: wiped everything in /tmp on misc1

## 2016-07-12 

* 22:55 Southparkfan: import finished & ran rebuildrecentchanges.php for wisdomsandboxwiki
* 22:28 Southparkfan: running southparkfan@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php importDump.php --wiki wisdomsandboxwiki /tmp/wisdomwiki.xml on mw1

## 2016-07-11 

* 20:28 Southparkfan: restarted jobrunner on mw1, it was stuck
* 18:30 Southparkfan: ran ufw-fix on cp1
* 05:26 John: remounted static on mw2
* 05:26 John: started jobrunner on mw1
* 05:24 John: remounted static on mw1
* 05:21 John: rebooting mw1
* 03:40 PuppyKun: 11:03:58 PM <icinga-miraheze> RECOVERY - Host Cache Proxy 1 is UP: PING OK - Packet loss = 0%, RTA = 0.47 ms

## 2016-07-10 

* 22:55 John: disabled uploads globally
* 22:24 John: rebooting cp1, NFS will have to manage after

## 2016-07-09 

* 22:54 John: ran manageInactiveWikis.php with --warn
* 20:36 John: rebooting mw2, unresponsive
* 14:13 PuppyKun: wisdomwikiwi> update page set page_namespace=1656 where page_namespace=1632;
* 14:12 PuppyKun: wisdomwikiwi> update page set page_namespace=1654 where page_namespace=1630;

## 2016-07-08 

* 18:59 John: reloaded nginx on cp[12]
* 13:42 PuppyKun: sudo php rebuildLocalisationCache.php --wiki extloadwiki on mw*

## 2016-07-07 

* 17:20 Southparkfan: restarted jobrunner on mw1
* 16:49 John: >UPDATE cw_wikis SET wiki_private = 1 WHERE wiki_dbname = "offensivesivewiki";
* 16:00 PuppyKun: > update cw_wikis set wiki_language="en" where wiki_dbname="exerionwiki";

## 2016-07-06 

* 15:53 PuppyKun: puppet run on mw* after [https://git.io/vKLXL](https://git.io/vKLXL)
* 12:28 PuppyKun: update cw_wikis set wiki_closed=0 where wiki_dbname="atplwiki";

## 2016-07-05 

* 14:29 John: ran update.php on new M[Ss]Calendar wikis

## 2016-07-04 

* 17:03 Southparkfan: all mwservers repooled, puppet re-enabled everywhere
* 16:09 Southparkfan: disabled puppet on mwservers

## 2016-07-03 

* 22:02 labster: [allthetropeswiki]> drop table time_zone; drop table time_zone_leap_second; drop table time_zone_name; drop table time_zone_transition; drop table time_zone_transition_type;
* 20:55 John: MariaDB [allthetropeswiki]> DROP TABLE event,general_log,procs_priv,proxies_priv,servers,tables_priv;
* 20:48 John: MariaDB [allthetropeswiki]> DROP TABLE proc;
* 14:37 John: update phabricator to stable
* 08:56 John: rm /bacula/backups/STATIC-0004 /bacula/backups/STATIC-0008 on bacula1
* 08:34 John: MariaDB [allthetropeswiki]> DROP TABLE host;
* 08:34 John: MariaDB [allthetropeswiki]> DROP TABLE columns_priv, func, db;

## 2016-07-01 

* 19:43 John: delete wikis: jubeatwikithwiki, chavezwiki, putinwiki, ndtestwiki ,lupawiki
* 18:11 PuppyKun: ran cleanupTitles.php --wiki testwiki to fix issues with TestWiki_talk:Request_permissions
* 17:45 John: reopened madgendersciencewiki
* 13:51 PuppyKun: finished manageInactive wikis, 104 wikis warned, 6 closed
* 13:44 PuppyKun: forced puppet run on mw1 after "mediawiki/REL1_26 b86bf96", running manageInactiveWikis.php
* 13:30 PuppyKun: sudo rm findInactiveWikis.php on mw1
* 11:44 John: made seldirwiki public

## 2016-06-30 

* 12:31 Southparkfan: reopened wikiconstitucio.miraheze.org

## 2016-06-29 

* 15:03 PuppyKun: deleted lupawiki per founder request

## 2016-06-28 

* 18:37 Southparkfan: reopened ackbwiki
* 06:34 Southparkfan: still not responding to reboot, opened ticket with VPS provider
* 06:28 Southparkfan: bacula1 crashed, trying to reboot, server / control panel not responding to actions

## 2016-06-27 

* 13:22 Southparkfan: re-enabled puppet on misc2
* 13:03 Southparkfan: disabled puppet on misc2

## 2016-06-26 

* 09:43 Southparkfan: issued varnishadm 'ban req.http.Host == wisdomwiki.org' on all cache proxies

## 2016-06-23 

* 12:10 Southparkfan: depooled mw1 @ cp2
* 11:21 Southparkfan: taking down cp1 for maintenance

## 2016-06-21 

* 14:13 Southparkfan: MariaDB [metawiki]> update cw_wikis set wiki_closed=0 where wiki_dbname='ggdrwiki'; per request

## 2016-06-19 

* 03:49 PuppyKun: > delete from cw_wikis where wiki_dbname='ndtestwiki';

## 2016-06-18 

* 23:37 PuppyKun: > update cw_wikis set wiki_private=1 where wiki_dbname='biblicalwikiwiki';
* 19:09 PuppyKun: sudo php runJobs.php --wiki metawiki
* 19:09 PuppyKun: sudo php runJobs.php --wiki loginwiki
* 18:59 PuppyKun: > update cw_wikis set wiki_closed=0 where wiki_dbname='biblicalwikiwiki';

## 2016-06-16 

* 18:24 Southparkfan: > update cw_wikis set wiki_language = 'fr' where wiki_dbname = 'evawiki';
* 17:56 John: reopened biblicalwikiwiki

## 2016-06-15 

* 20:56 Southparkfan: renewed *.miraheze.org certificate. Apache and nginx on all cache proxies, appservers and misc. servers have been reloaded

## 2016-06-14 

* 02:33 PuppyKun: varnish purge [https://downhillderelicts.miraheze.org](https://downhillderelicts.miraheze.org) on cp*
* 02:32 PuppyKun: varnish> purge wiki.downhillderelicts.com on cp*

## 2016-06-13 

* 19:33 PuppyKun: varnish> ban req.http.Host == metatrek.miraheze.org on cp*
* 18:53 John: php /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/manageInactiveWikis.php --wiki metawiki --warn
* 18:45 Southparkfan: varnish> ban req.http.Host == meta.trek.tk to fix custom domain

## 2016-06-11 

* 07:57 Southparkfan: ran FlowUpdateWorkflowPageId.php for All The Tropes ([https://phabricator.wikimedia.org/T137594](https://phabricator.wikimedia.org/T137594))

## 2016-06-10 

* 23:06 PuppyKun: merge mw-config #523 and run puppet on mw*
* 22:43 PuppyKun: ensured git clone /srv/mediawiki/config on mw*
* 22:14 PuppyKun: someone started log bot

## 2016-06-05 

* 18:52 Southparkfan: adminbot now runs as irc user
* 16:23 John: removed HHVM references/files from private git

## 2016-06-03 

* 23:01 SPF|Cloud: test if Python ignores errors
* 22:57 PuppyKun: Thank [User:Southparkfan](https://meta.miraheze.org/wiki/User:Southparkfan) for working log not
* 22:49 labster: channel spam
* 22:49 SPF|Cloud: and another one
* 22:49 SPF|Cloud: another test
* 22:48 SPF|Cloud: test
* 21:10 Southparkfan: MariaDB [allthetropeswiki]> update page set page_content_model = 'flow-board' where  page_namespace = 3 and page_title not like '%/%' and page_content_model = 'wikitext'; to fix [https://phabricator.miraheze.org/T340](https://phabricator.miraheze.org/T340)

## 2016-05-23 

* 17:27 JohnLewis: undeployed and removed HHVM from mw2 completely. It is no more.
* 17:23 JohnLewis: undeployed and removed HHVM from mw1 completely.
* 01:07 revi: `revi@mw1:~$ sudo service hhvm restart`, 502 everywhere.

## 2016-04-22 

* 22:24 Southparkfan: MariaDB [allthetropeswiki]> truncate ipblocks; to fix [https://phabricator.miraheze.org/T229](https://phabricator.miraheze.org/T229)

## 2016-04-20 

* 17:12: NDKilla: > update cw_wikis set wiki_private=1 where wiki_dbname='evawiki'; per founder request

## 2016-04-12 

* 16:23: NDKilla closed lupawiki (cw_wikis wiki_closed=1) per founder request

## 2016-03-27 

* 19:48 Southparkfan: resetted password for user 'O'. Sent email to user with new password.
* ~19:45 Southparkfan: ran deleteEmptyAccounts.php --wiki metawiki --fix --migrate --safe-migrate and checkLocalUser.php --delete on some wikis
* 17:31 JohnLewis: deleted several wikis. See dormancy page history for a list. +internalwiki

## 2016-03-26 

* 20:13 JohnLewis: deleted bzduropediawiki

## 2016-03-25 

* 13:47 Southparkfan: php deleteEmptyAccounts.php --wiki metawiki --fix --safe-migrate --migrate

## 2016-03-15 

* 5:30 NDKilla: UPDATE cw_wikis SET wiki_closed=1 WHERE wiki_dbname="internalwiki"; (via mw1 maintenance/sql.php)

## 2016-03-12 

* 15:44 Southparkfan: /srv/mediawiki/w/extensions/CentralAuth/maintenance# php deleteEmptyAccounts.php --wiki metawiki --fix --safe-migrate to delete global acocunts without any attached users
* 15:16 Southparkfan: foreachwikiindblist /srv/mediawiki/dblist/all.dblist maintenance/checkLocalUser.php --verbose 1 --delete > ~/tmp-ca.log at mw1 to fix annoying "Could not find user data for" MWExceptions

## 2016-03-11 

* 19:01 JohnLewis: UPDATE cw_wikis SET wiki_private = "0" WHERE wiki_dbname = "aevumkathwiki";

## 2016-03-08 

* 22:12 JohnLewis: deleted spiraltestwiki and allthetropestestwiki
* 19:53 JohnLewis: DROP DATABASE (for following: poserdazfreebiestestwiki, gameswiki, wikiacawiki)
* 19:47 JohnLewis: DELETE FROM cw_wikis WHERE wiki_dbname = "wikiacawiki";
* 05:25 revi: `sudo service hhvm restart`, icinga crying for varnish backend problems

## 2016-03-07 

* 22:41 JohnLewis: root@ns3 relays: The system is going down for power-off at Mon 2016-03-07 22:41:14 UTC!
* 22:40 JohnLewis: root@ns3:~# shutdown -P

## 2016-02-26 

* 17:56 JohnLewis:  UPDATE cw_wikis SET wiki_private="1",wiki_sitename="LBS Global Energy Summit" WHERE wiki_dbname="lbsgeswiki";

## 2016-02-24 

* 19:19 JohnLewis: /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist  /srv/mediawiki/w/maintenance/patchSql.php <br /> /srv/mediawiki/w/extensions/BetaFeatures/sql/create_counts.sql

## 2016-02-22 

* 22:16 JohnLewis: UPDATE cw_wikis SET wiki_language = "es" WHERE wiki_dbname = "ricwiki";
* 20:45 JohnLewis: reboot servers for security updates relating to core system files.

## 2016-02-16 

* 16:28 Southparkfan: deleted thoughtonomywikiwiki dumps

## 2016-02-03 

* 15:50 JohnLewis: UPDATE cw_wikis SET wiki_closed=0,wiki_private=1 WHERE wiki_dbname='quantixwiki';

## 2016-01-20 

* 16:29 SPF|Cloud: ran checkLocalNames.php and checkLocalUser.php on spiralwiki with --delete option. ([https://github.com/miraheze/mw-config/issues/264](https://github.com/miraheze/mw-config/issues/264))

## 2016-01-18 

* 17:10 SPF|Cloud: deleted gameswiki database
* 17:05 SPF|Cloud: deleted gameswiki database
* 16:46 SPF|Cloud: deleted emptysetwiki database per NDKilla's request
* 16:35 PuppyKun: restarted HHVM (process was "active (exited)" with fatal errors)

## 2016-01-16 

* 02:06 PuppyKun: ran SQL query "UPDATE cw_wikis SET wiki_closed=1 WHERE wiki_dbname='quantixwiki' OR wiki_dbname='catboxwiki' or wiki_dbname='emptysetwiki';" on mw1
* 02:05 PuppyKun: Manually restarted HHVM on mw1 ~10 mins ago

## 2016-01-10 

* 17:17 PuppyKun: manually run puppet on mw1 and run namespaceDupes.php --wiki adnovumwiki --fix

## 2016-01-09 

* 01:46 PuppyKun: manually ran update.php  on adnovumwiki. failed the first time due to global blocking table already existing (this usually doesn't cause it to fail?) running it again finished successfully in 0.7s

## 2016-01-07 

* 15:09 SPF|Cloud: ran removeDeletedWikis.php to delete poserdazfreebiestestwiki + removed it from cw_wikis

----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:Server_admin_log/2016)**