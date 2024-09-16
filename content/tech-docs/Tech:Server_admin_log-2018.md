---
title: Tech:Server admin log/2018
---

`{{ {{TOC right}} }}`
## 2018-12-31 

* 22:01 paladox: depool mw1
* 20:59 paladox: repool mw1
* 20:11 paladox: depool mw1
* 00:38 paladox: started electron on misc3
* 00:24 paladox: stopping electron on misc3 temporarily to deploy a change

## 2018-12-30 

* 20:16 paladox:  INSERT INTO mw_namespaces(`ns_dbname`, `ns_namespace_id`, `ns_namespace_name`, `ns_searchable`, `ns_subpages`, `ns_content`, `ns_protection`, `ns_aliases`, `ns_core`) VALUES ('metawiki', 0, 'Main', 0, 0, 0, *, '[]', 1); on db4
* 20:14 paladox: INSERT INTO mw_namespaces(`ns_dbname`, `ns_namespace_id`, `ns_namespace_name`, `ns_searchable`, `ns_subpages`, `ns_content`, `ns_protection`, `ns_aliases`, `ns_core`) VALUES ('metawiki', -2, 'Media', 0, 0, 0,* , '[]', 1); on db4
* 19:56 paladox: depool mw2
* 19:52 paladox: repool mw1
* 19:51 paladox: /srv/mediawiki/w/cache/managewiki# rm -rf * on mw*
* 19:33 paladox: depooling mw1
* 17:36 John: running jobs on mw1 and test1
* 16:22 paladox: MacFan4000 deleted these wiki's scottybweyywiki, sdoricawiki, secretsofgrindeawiki, serialetv15wiki, serifkayawiki, sevemontpellierwiki, sexedlankawiki, shinseiwiki, shippingandmetawiki, showmedicinawiki, sikhwikitestwiki, silenytewiki, silverkettlewiki, silzkindwiki, sireentjewiki, sitelenwiki, skfoundationwiki, slimewikiwiki, smallelephantswiki, smfdoesathingwiki, macfantestwiki
* 16:22 MacFan4000: deleting wikis in deleted.dblist on mw1
* 15:27 John: populating namespaces
* 01:01 paladox: running lc on all mw*
* 00:29 paladox: delete wiki's scottybweyywiki, sdoricawiki, secretsofgrindeawiki, serialetv15wiki, serifkayawiki, sevemontpellierwiki, sexedlankawiki, shinseiwiki, shippingandmetawiki, showmedicinawiki, sikhwikitestwiki, silenytewiki, silverkettlewiki, silzkindwiki, sireentjewiki, sitelenwiki, skfoundationwiki, slimewikiwiki, smallelephantswiki, smfdoesathingwiki
* 00:23 paladox: and 2 more stwmnwiki, sugarysdiscordearthvisionwiki
* 00:23 paladox: delete wiki's socrateswiki, songfestivalwiki, sonicfanswikiwiki, sosunwundowiki, soverigntribewiki, soyaincwiki, soylunawiki, spevtwiki, splatteamswiki, spqrwiki, spsextonwiki, ssggwiki, starcrosswiki, steenekenlabwiki, stellachronicawiki, steloballwiki, sthomaspriwiki, stigmergyfamilystudiowiki, stopdeschuldenwiki, storiesbythefirewiki, storyofseasonswiki, stoutheartswiki, stratospherewiki, studiodouzevingtquatrewiki, studyanythingwiki,
* 00:20 paladox: delete wiki's sumerrawiki, supereroiswiki, supportdrivenwiki, surderienwiki, surewiki, sw3g005carlistwiki, syscoopwiki, tacitleaguewiki, taigowiki, taisaku777wiki, tallerdeticswiki, tanvirwiki, tausurvivalwiki, tcrtailswiki, teamwizardrywiki, techeducationwiki, telemedicinewiki, teleswikiwiki, tellestriawiki, tempestwiki
* 00:15 paladox: delete wiki's tensorflowlearningwiki, testarkclswiki, testwikidiggywiki, texwikiwiki, thegamedatabasewiki, themfbclubwiki, theneworderwiki, therubyserverwiki, thorwiki, tierklinikleitfadenwiki, tigerpediawiki, tin242wiki, tjelectronicswiki, tmrwiki, tokyoghoulwiki, toolboxrpwiki, toppsdigitalcardtraderwiki, unabwiki, universaliswiki, valetiawiki, wgamingwiki, wikilopwiki, wikimoddingsnakewiki, yaalwiki

## 2018-12-29 

* 23:58 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki loginwiki on mw*
* 17:45 paladox: TRUNCATE TABLE gnf_files; on db4
* 17:40 Southparkfan: MariaDB [mhglobal]> alter table gnf_files modify column files_timestamp binary(14) not null;
* 16:17 Southparkfan: install nethogs on mw[1-3]
* 15:58 Southparkfan: run 'vnstat -l -i venet0' in screen on mw[1-3]
* 15:57 Southparkfan: install vnstat on mw1 and mw2
* 00:43 paladox: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=baobabarchiveswiki --report=1 starwars_pages_full.xml on mw1
* 00:15 paladox: swapoff -a && swapon -a on db4

## 2018-12-28 

* 23:48 Southparkfan: running 'vnstat -l -i venet0' in screen on mw3; pid 8665
* 23:29 Southparkfan: install vnstat on mw3
* 15:28 paladox: upgrade phabricator on misc4
* 08:02 Reception123: reception@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php runJobs.php --wiki modesofdiscoursewiki
* 01:10 paladox: upgrading phabricator on misc4

## 2018-12-27 

* 00:53 paladox: downtiming sslhost for 2 hours due to network issues
* 00:42 paladox: /usr/bin/nice -19 /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/maint*/runJobs.php on mw1

## 2018-12-26 

* 21:24 paladox: deleting wiki wsmwiki ref T3899
* 21:20 paladox: deleting wiki's virtualcommunitywiki and thisrealitywiki ref T3913
* 17:18 Reception123: stripped 2FA from Reception123 on Phab
* 15:23 paladox: reboot cp5 for kernel upgrade
* 02:36 paladox: repool mw1
* 02:15 paladox: depool mw1

## 2018-12-25 

* 22:47 paladox: upgrade puppet1 to puppet6
* 22:00 paladox: disabling puppet everywhere

## 2018-12-23 

* 20:26 paladox: depooling mw1
* 16:54 paladox: rebooted test1 to clear ram
* 16:15 paladox: repool mw1
* 16:11 paladox: depool mw1
* 01:40 paladox: rebooted misc2 as redis is unresponsive

## 2018-12-22 

* 14:28 paladox: recreating wiki cristianopedia per T3895#74986
* 09:05 Reception123: sudo -u www-data php refreshLinks.php --wiki metawiki (external links not working)

## 2018-12-21 

* 23:28 John: enabled GH's beta issue deletion on Miraheze
* 17:19 paladox: install puppetserver on test1 (also disconnected it from puppet1 temporarily)
* 15:44 paladox: importing puppetlabs apt key on test1
* 02:25 paladox: imported other wiki dumps into baobabarchiveswiki ref T3850
* 02:18 paladox: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=baobabarchiveswiki --report=1 "Baobab_Archives_Export_(1).xml" on mw1

## 2018-12-20 

* 19:52 paladox: reboot puppet1 to clean any ram
* 18:11 paladox: running lc on all mw*
* 13:16 paladox: recreating wiki shroudedpathwiki;
* 13:01 paladox: recreating wiki moralmeatwiki
* 00:32 paladox: delete wiki tosmafiawiki, toswiki, tpirwiki, trafficwiki, trafficwikiwiki, travailcollaboratifwiki, triforcewikiwiki, triggerhappywiki, trilobyteswiki, truewikiwiki, tsaipediawiki, turbografx16wiki, turingtewiki, turingwiki, tvnowhdwikiwiki, twelvethfleetwiki, twswiki, tyelabwiki, ubcrocketwiki
* 00:14 paladox: delete wiki uniguiwiki, universfultonwiki, unjeongwiki, uppwiki, uqteamwiki, uratarouwiki, urgentsharewiki, usedcarguidewiki, usrwiki, utavowikiwiki, valsatrascoutwiki, vanderbiltentwiki, vaporwavewiki, vaswiki, velayatwiki, veronikyasongcontestwiki, vesperwiki, vidliiwiki, vmbraopswiki, voidholewiki, vorakwiki, vragwiki
* 00:14 paladox: delete wiki ucscospwiki, undisclosedwiki, uniguiwiki, universfultonwiki, unjeongwiki, uppwiki, uqteamwiki, uratarouwiki, urgentsharewiki, usedcarguidewiki, usrwiki, utavowikiwiki, valsatrascoutwiki, vanderbiltentwiki, vaporwavewiki, vaswiki, velayatwiki, veronikyasongcontestwiki, vesperwiki, vidliiwiki, vmbraopswiki, voidholewiki, vorakwiki, vragwikiucscospwiki, undisclosedwiki,
* 00:14 paladox: delete wiki ucscospwiki, undisclosedwiki, uniguiwiki, universfultonwiki, unjeongwiki, uppwiki, uqteamwiki, uratarouwiki, urgentsharewiki, usedcarguidewiki, usrwiki, utavowikiwiki, valsatrascoutwiki, vanderbiltentwiki, vaporwavewiki, vaswiki, velayatwiki, veronikyasongcontestwiki, vesperwiki, vidliiwiki, vmbraopswiki, voidholewiki, vorakwiki, vragwikiucscospwiki, undisclosedwiki, uniguiwiki, universfultonwiki, unjeongwiki, uppwiki, uqteamwiki,
* 00:05 paladox: delete wiki vwiki waenwiki, wakeupsuperwiki, wandererswiki, wayzataapbiofinalwiki, weryskokistestingwikiwiki, wessonderwiki, wherecollegefundsgowiki, whsapushwiki, wifispesialistenwiki, wiinfwiki, wikapediawiki, wikiakademiibiznesuwiki, wikibadawiki, wikibalsanwiki, wikidoloxywiki, wikigtscwiki, wikiimprovementwiki and wikimojawiki

## 2018-12-19 

* 23:58 paladox: deleting wiki's wikinventwiki, wikipeddawiki, wikipixelwiki, wikipoliticuswiki, wikisaintoiswiki, wikiversitywiki, winecrestgameswiki, wisdomsandboxwiki, wixosswiki   , wkupwiki     , wmwiki       , wokeipediawiki, wokeusbwiki, wonderiawiki, worwiki, wrocwiki, x3wikiwiki, xjtluwiki, xofwiki, xorshidwiki and xylphwiki
* 23:54 paladox: deleting wiki yogabooktechnicalwiki, yoganomiconwiki, youniquebynereawiki, yourtechnicalservicewiki, youtauwiki, youtubewiki, zanwiki, zentrendswiki, zharkunuwiki, zolotwiki and zunderscorewiki
* 23:52 paladox: deleting wiki yiqiyangwiki
* 23:49 paladox: deleting wiki kingkiller ref T3901
* 19:15 paladox: stopping puppetdb on puppet1
* 19:13 paladox: dropping puppetdb on postgresql (on db4)
* 15:16 paladox: [15:01:53]  <@paladox>    !log upgrading db4 to debian 9.6 and also mariadb to 10.2.19

## 2018-12-18 

* 20:28 John: renamed mhglobal table from gfn_files to gnf_files
* 20:07 paladox: deleting cristianopediawiki and tallerdecristianopedia wiki's ref T3895

## 2018-12-17 

* 17:57 paladox:  sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=visewiki --report=1 visetestwiki.xml on mw1 ref T3865
* 17:28 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki loginwiki on mw*

## 2018-12-16 

* 22:48 paladox: upgrade phabricator on misc4
* 19:25 paladox: repool mw3 (also ignore the reinstall log, it was never reinstalled due to a issue)
* 17:44 paladox: reinstall mw3
* 17:29 paladox: depool mw3

## 2018-12-15 

* 21:07 paladox: repool mw1
* 20:51 paladox: depool mw1
* 17:28 paladox: repool mw3
* 17:25 paladox: depool mw3
* 17:24 paladox: repool mw2
* 17:19 paladox: depool mw2
* 17:14 paladox: repool mw1
* 17:11 paladox: depool mw1
* 00:13 John: deleted maiascwiki in line with Content Policy

## 2018-12-14 

* 17:15 paladox: upgrade node-exporter on all servers
* 16:07 paladox: upgrading prometheus on misc2 from 1.x to 2.x (from stretch backports)
* 15:38 paladox: rebooted misc2 (seems it had a OOM)

## 2018-12-13 

* 23:26 paladox: (not enforcing 2fa as it breaks the api) but all staff will still be required to use it
* 23:17 paladox: enforcing 2FA on matomo.miraheze.org for all staff.
* 23:04 paladox: ./console twofactorauth:disable-2fa-for-user --login=MacFan4000 on misc2
* 21:34 paladox: install "Force SSL" matomo plugin on misc2
* 21:32 paladox: install GoogleAuthenticator matomo plugin (for 2fa) on misc2
* 20:07 paladox: dropping psiconauta account on phabricator

## 2018-12-12 

* 15:56 paladox: repool mw3
* 15:49 paladox: depool mw3
* 15:28 paladox: repool mw2
* 15:24 paladox: depool mw2
* 15:24 paladox: repool mw1
* 14:33 paladox: switching on new php module on mw1
* 14:30 paladox: depooling mw1
* 11:19 paladox: testing php7.3 on test1
* 10:10 paladox: enabling new php module on test1

## 2018-12-09 

* 20:01 paladox: root@mw1:/srv/mediawiki/w/maintenance# php deleteBatch.php --wiki=nonsensopediawiki text

## 2018-12-08 

* 16:01 paladox: upgrade php to 7.2.13 on mw*
* 03:47 paladox: switch puppet1 back to master
* 03:02 paladox: checkout icinga-refactor on puppet1 to test refactor
* 02:55 paladox: switched puppet1 back to master
* 02:33 paladox: checkout icinga-refactor on puppet1 to test refactor
* 01:00 paladox: sudo -u www-data php ../maintenance/importImages.php --wiki=s23wiki --overwrite --search-recursively /home/paladox/test/images on mw1
* 00:39 paladox: dropping database vachnamrutwiki
* 00:37 paladox: dropping database tbrwiki
* 00:37 paladox: dropping database rimstockwiki
* 00:36 paladox: dropping database qtbookwiki;
* 00:35 paladox: dropping database newhudsoniawiki
* 00:34 paladox: dropping database netculturewiki
* 00:33 paladox: dropping database edcwiki;
* 00:32 paladox: dropping domaxwiki
* 00:31 paladox: dropping catalogodesantaswiki
* 00:30 paladox: dropping animangamespnpwiki
* 00:29 paladox: dropping scruffy2wiki
* 00:27 paladox: dropping atomicpancakeswiki and tochkiwiki
* 00:24 paladox: dropping breakthegamewiki and simonjonwiki
* 00:14 paladox: repool mw1

## 2018-12-07 

* 23:36 paladox: hacked ExternalUserNames.php#L77 on mw1
* 21:01 paladox: depool mw1
* 19:54 paladox: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=s23wiki --report=1 --uploads s23wiki_20181207.xml on mw1
* 17:21 paladox: dropping db rezeroswiki (wiki was deleted a while ago)
* 17:18 paladox: dropping db metaautonomywiki (wiki was deleted a while ago)
* 17:09 paladox: dropping db centriswiki the wiki was removed a year ago under the DP

## 2018-12-06 

* 22:22 paladox: running Comment table schema migration script on all wikis

## 2018-12-03 

* 17:43 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki loginwiki on mw*
* 17:27 paladox: applying grants on db4 for [https://phabricator.miraheze.org/T3621](https://phabricator.miraheze.org/T3621)

## 2018-12-02 

* 02:03 paladox: /usr/bin/nice -19 /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/generateMirahezeSitemap.php on mw1 in a screen

## 2018-12-01 

* 23:10 paladox: deleting backups on bacula1 for it to backup in less then 1 hour
* 23:00 PuppyKun: stripped multifactor authentication for NDKilla's wiki account (ndkilla@mw1:/srv/mediawiki/w/extensions/OATHAuth/maintenance$ sudo -u www-data php disableOATHAuthForUser.php --wiki metawiki NDKilla)
* 22:57 PuppyKun: stripped authentication factors for NDKilla's phabricator account (ndkilla@misc4:/srv/phab/phabricator/bin$ ./auth strip --user NDKilla --all-types)
* 17:09 paladox: upgrading phabricator on misc4

## 2018-11-30 

* 21:47 paladox: sudo -u www-data php /srv/mediawiki/w/maintenance/deleteBatch.php --wiki=nonsensopediawiki ./pages on mw1
* 21:42 paladox: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=baobabarchiveswiki --report=1 HoloNetWiki20181130033010.xml on mw3
* 21:29 paladox: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=abdldatabasewiki --report=1 abdl_pages_full.xml on mw2
* 21:22 paladox: running files import on mw1 for americangirldollswiki

## 2018-11-29 

* 01:58 paladox: revoking certificate on taotac.info
* 00:37 John: enabled GUP on reviwikiwiki and running jobs for reviwikiwiki on mw2

## 2018-11-28 

* 23:55 paladox: running rebuildall.php on nonciclopediawiki on mw1
* 21:34 paladox: applying exporter grants on db4
* 21:12 paladox: installing prometheus-mysqld-exporter on db4
* 17:54 paladox:  delete from page WHERE page_title LIKE 'NonDizionario:%' and page_namespace=0; on db4

## 2018-11-27 

* 21:04 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki loginwiki on mw*
* 19:58 paladox: UPDATE page SET page_title = REPLACE(page_title, 'Discussioni_test:', *), page_namespace = 2015 WHERE page_title LIKE 'Discussioni_test:%' AND page_namespace=0; on db4
* 19:57 paladox: UPDATE page SET page_title = REPLACE(page_title, 'Discussioni_manuali:',* ), page_namespace = 2019 WHERE page_title LIKE 'Discussioni_manuali:%' AND page_namespace=0; on db4
* 19:51 paladox: UPDATE page SET page_title = REPLACE(page_title, 'Discussioni_NonDizionario:', *), page_namespace = 2013 WHERE page_title LIKE 'Discussioni_NonDizionario:%' AND page_namespace=0; on db4
* 19:34 paladox: UPDATE page SET page_title = REPLACE(page_title, 'NonNotizie:',* ), page_namespace = 2006 WHERE page_title LIKE 'NonNotizie:%' AND page_namespace=0; on db4
* 18:51 paladox: php rebuildall.php --wiki=nonciclopediawiki on mw1
* 18:35 paladox: UPDATE page set page_title = concat('Discussioni_template:', page_title), page_namespace = 2005 WHERE page_namespace = 11 NOT LIKE 'Discussioni_template:%'; on db4
* 18:34 paladox: UPDATE page set page_title = concat('Template:', page_title), page_namespace = 2004 WHERE page_namespace = 10 NOT LIKE 'Template:%'; on db4
* 16:40 paladox: UPDATE page SET page_title = REPLACE(page_title, 'NonPoesie:', *), page_namespace = 2016 WHERE page_title LIKE 'NonPoesie:%' AND page_namespace=0; on db4 T3754
* 00:54 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki loginwiki on mw*

## 2018-11-26 

* 17:58 Southparkfan: enable puppet on cp4
* 16:48 Southparkfan: disabled puppet on cp4

## 2018-11-25 

* 06:42 Reception123: DROP DATABASE pirategalaxywiki
* 06:42 Reception123: DROP DATABASE vanishwiki
* 06:41 Reception123: deleted pirategalaxywiki from CW_WIKIS (T3834)
* 06:36 Reception123: deleted vanishwiki from CW_WIKIS (T3822)
* 00:36 paladox: upgrade phabricator on misc4

## 2018-11-24 

* 20:07 paladox: switched orain to a wildcard cert
* 18:33 paladox: switching mw1 to certbot
* 14:54 paladox: upgrading ns1 to debian 9.6
* 14:52 paladox: repool cp4
* 14:52 paladox: depool cp4
* 14:49 paladox: upgrade cp4 to debian 9.6
* 14:47 paladox: depool cp4

## 2018-11-23 

* 23:53 paladox: repool cp2
* 23:45 paladox: depooling cp2 for upgrade to debian 9.6
* 22:33 John: depool mw2
* 01:39 paladox: upgraded icingaweb2 to 2.6.2-1 on misc1
* 00:10 MacFan4000: (for transparency) using pywikibot to delete broken redirects on nonsensopediawiki per request

## 2018-11-22 

* 17:52 MacFan4000: sudo -u www-data php /srv/mediawiki/w/maintenance/deleteBatch.php --wiki nonsensopediawiki -r "Deleting per request on phab" list.txt
* 00:01 paladox: depool mw1 (testing new cert framework)

## 2018-11-21 

* 22:16 paladox: recreating suginamisannekiwiki
* 22:10 paladox: recreating techbestpracticewiki
* 20:42 paladox: sudo apt-get install certbot -t stretch-backports on mw1
* 20:42 paladox: apt-get --purge remove python-certbot*
* 20:32 paladox: sudo apt-get install python-certbot-nginx -t stretch-backports on mw1 for T3822
* 17:54 paladox: apt-get --purge remove mysql* on mw1
* 17:40 John: remove MariaDB* on mw1
* 15:06 MacFan4000: renaming anothertimeline2120wiki to megrezwiki

## 2018-11-20 

* 22:09 paladox: restarting mysql on db4 (from [17:49:05] UTC)
* 22:08 paladox: rebooted bacula1
* 22:07 MacFan4000: running jobs on all wikis
* 18:26 John: depool mw2
* 17:31 paladox: re doing backups for private git and phabstatic
* 17:25 paladox: ran migrateActor on atlasinternationalwiki to fix flow issue
* 16:17 John: MariaDB [atlasinternationalwiki]> UPDATE actor SET actor_name = "Void~old" WHERE actor_id = "4";
* 16:08 John: MariaDB [atlasinternationalwiki]> UPDATE actor SET actor_name = "Ohallora~old" WHERE actor_user = "1";
* 02:07 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki loginwiki on mw*

## 2018-11-19 

* 23:27 paladox: php deleteBatch.php --wiki=nonsensopediawiki text on mw1
* 20:47 paladox: regenerating backups on bacula1
* 18:17 paladox: cleaning up matmo git dir (was dirty)
* 18:01 paladox: repool mw1
* 17:44 paladox: depool mw1 for a experiment
* 12:20 John: fixing directory perms for noncilopediawiki

## 2018-11-18 

* 23:50 paladox: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=americangirldollswiki --report=1 --files americangirlwikiacom-20181102-history.xml on mw1

## 2018-11-17 

* 23:21 paladox: UPDATE page SET page_title = REPLACE(page_title, 'Test:', ''), page_namespace = 2025 WHERE page_title LIKE 'Test:%' AND page_namespace=1; on db4
* 23:21 paladox: UPDATE page SET page_title = REPLACE(page_title, 'Test:', ''), page_namespace = 2024 WHERE page_title LIKE 'Test:%' AND page_namespace=0; on db4
* 23:20 paladox: UPDATE page SET page_title = REPLACE(page_title, 'NonCitazioni:', ''), page_namespace = 2021 WHERE page_title LIKE 'NonCitazioni:%' AND page_namespace=1; on db4
* 23:20 paladox: UPDATE page SET page_title = REPLACE(page_title, 'NonCitazioni:', ''), page_namespace = 2020 WHERE page_title LIKE 'NonCitazioni:%' AND page_namespace=0; on db4
* 23:18 paladox: UPDATE page SET page_title = REPLACE(page_title, 'Manuali:', ''), page_namespace = 2028 WHERE page_title LIKE 'Manuali:%' AND page_namespace=0; on db4
* 23:17 paladox: UPDATE page SET page_title = REPLACE(page_title, 'NonRicette:', ''), page_namespace = 2029 WHERE page_title LIKE 'NonRicette:%' AND page_namespace=1; on db4
* 23:17 paladox: UPDATE page SET page_title = REPLACE(page_title, 'NonRicette:', ''), page_namespace = 2028 WHERE page_title LIKE 'NonRicette:%' AND page_namespace=0; on db4
* 23:14 paladox: UPDATE page SET page_title = REPLACE(page_title, 'NonPoesie:', ''), page_namespace = 2027 WHERE page_title LIKE 'NonPoesie:%' AND page_namespace=1; on db4
* 23:13 paladox: UPDATE page SET page_title = REPLACE(page_title, 'NonPoesie:', ''), page_namespace = 2026 WHERE page_title LIKE 'NonPoesie:%' AND page_namespace=0; on db4
* 23:05 paladox: UPDATE page SET page_title = REPLACE(page_title, 'NonLibri:', ''), page_namespace = 2026 WHERE page_title LIKE 'NonLibri:%' AND page_namespace=0; on db4
* 23:01 paladox: UPDATE page SET page_title = REPLACE(page_title, 'Discussione:NonFiabe:', ''), page_namespace = 2027 WHERE page_title LIKE 'Discussione:NonFiabe:%' AND page_namespace=0; on db4
* 01:18 paladox: repool mw1

## 2018-11-16 

* 19:45 paladox: mkdir /mnt/mediawiki-static/sitemaps

## 2018-11-15 

* 23:28 paladox: depool mw1 to apply some hacks
* 20:16 paladox: repool mw1
* 20:11 paladox: depool mw1
* 20:09 paladox: repool mw2
* 20:05 paladox: depool mw2
* 20:03 paladox: repool mw3
* 19:57 paladox: upgrading mw* to debian 9.6
* 19:56 paladox: depool mw3
* 19:49 paladox: rm /home/reception/NonciclopediaDump_2018-08-18.zip on mw2
* 19:48 paladox: rm -rf /home/reception/NonciclopediaDump_2018-08-18 on mw2 (24gb)
* 15:25 paladox: upgrade grafana on misc1 to 5.3.4
* 15:25 paladox: upgrade icinga2 on misc1 to 2.10.2

## 2018-11-12 

* 21:06 paladox: depool mw1 to roll out full write actor mode
* 21:00 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki loginwiki on mw*

## 2018-11-11 

* 00:46 paladox: php importImages.php /home/paladox/test/images --overwrite --search-recursively --wiki=nonciclopediawiki --user='Maintenance script' on mw1

## 2018-11-10 

* 17:31 paladox: restarted db4 to reduce load and cpu as it was quite high (warnings from icinga too)
* 13:55 paladox: upgraded bacula1 to debian 9.6
* 13:55 paladox: updated debian on misc* to 9.6
* 13:55 paladox: upgraded redis on misc2 to 5.0

## 2018-11-09 

* 21:18 paladox: deleting LizardFS-chunkserver1,  LizardFS-chunkserver2, Static1 and Static2 (they are now known as Static), LizardFS-master from bacula1
* 21:13 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki loginwiki on mw*
* 16:36 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki loginwiki on test1
* 16:36 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki loginwiki on mw*

## 2018-11-08 

* 19:33 paladox: repool mw1
* 18:23 paladox: depool mw1
* 02:12 John: added cw_visibility and droped cw_status_{comment,comment_user,comment_timestamp} on cw_requests on metawiki
* 01:39 paladox: nice -n -19 php /srv/mediawiki/test/maintenance/importDump.php --wiki=nonciclopediawiki --report=1 --uploads --no-updates /mnt/med*/private/test/nonciclopediawikiacom-20180818-history.xml on test1
* 01:23 paladox: drop and recreate nonciclopediawiki wiki

## 2018-11-07 

* 21:21 paladox: restarted adminbot (icinga-miraheze never rejoined after leaving so restarted service)
* 20:44 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki loginwiki on mw*
* 18:27 paladox: php extensions/TitleKey/rebuildTitleKeys.php --wiki=monarchistswiki on mw1
* 18:21 paladox: php /srv/mediawiki/w/maintenance/sql.php --wiki=zymonicwiki /srv/mediawiki/w/maintenance/archives/patch-actor-table.sql on mw1

## 2018-11-05 

* 22:36 paladox: /usr/bin/nice -19 /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist migrateActors.php on mw1 in a screen
* 22:36 paladox: migrating all wikis to actor
* 19:33 paladox: php migrateActors.php --wiki=metawiki on mw1
* 19:32 paladox: migrating metawiki to actor
* 11:42 Reception123: running wikibackups (./test.sh /home/reception/allpublic.dblist /srv/mediawiki/w/maintenance/dumpBackup.php)

## 2018-11-04 

* 23:45 paladox: deleting jokepastawiki wiki per [https://phabricator.miraheze.org/T3763](https://phabricator.miraheze.org/T3763)

## 2018-11-03 

* 19:00 paladox: php cleanupUsersWithNoId.php --wiki=nonciclopediawiki --assign --prefix="" on mw1
* 03:03 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki loginwiki on mw*
* 02:28 paladox: running php assignImportedEdits.php --wiki=nonciclopediawiki on mw1

## 2018-11-02 

* 20:00 paladox: enabling puppet on mw*
* 19:55 paladox: disabling puppet on mw*
* 19:46 paladox: DELETE FROM cw_wikis WHERE wiki_dbname = ""; on db4
* 16:27 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki loginwiki on mw*
* 03:52 paladox: ./bin/remove destroy @Xenic on misc4
* 01:30 paladox: ALTER TABLE cw_wikis ADD COLUMN wiki_creation BINARY(14) NULL AFTER wiki_private on db4

## 2018-11-01 

* 23:28 paladox: sudo -u www-data /usr/bin/nice -19 /usr/bin/php /srv/mediawiki/w/extensions/CreateWiki/maintenance/manageInactiveWikis.php --wiki loginwiki --warn --close on mw3
* 22:24 paladox: live hacking manageInactiveWikis.php on mw3
* 21:52 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki loginwiki on mw*
* 17:08 paladox: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=privadowiki --report=1 --no-updates Taller_Wiki-20181024160736.xml.4 on mw1
* 17:07 paladox: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=mediatecawiki --report=1 --no-updates Taller_Wiki-20181024160736.xml.3 on mw1
* 17:05 paladox: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=centralwiki --report=1 --no-updates Taller_Wiki-20181024160736.xml.2 on mw1
* 17:03 paladox: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=greatestmovieswiki --report=1 --no-updates greatestmovies_pages_full.xml on mw1
* 16:52 paladox: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=apunteswiki --report=1 --no-updates Taller_Wiki-20181024160736.xml on mw1
* 16:46 paladox: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=infowiki --report=1 Taller_Wiki-20181024160736.xml.1 on mw1
* 16:02 paladox: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=americangirldollswiki --report=1 americangirl_pages_full.xml on mw1
* 15:58 paladox: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=youtubepoopwiki --report=1 youtubepoop_pages_full.xml on mw1
* 03:27 paladox: php maintenance/importImages.php --wiki=nonciclopediawiki --extensions=gif,ico,jpeg,jpg,ogg,png,svg,pdf,djvu,JPG --search-recursively --skip-dupes /home/paladox/images/ on mw1
* 01:22 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki loginwiki on test1
* 01:22 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki loginwiki on mw*
* 00:24 paladox: php rebuildall.php --wiki=nonciclopediawiki on mw1

## 2018-10-30 

* 22:41 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki loginwiki on test1
* 22:41 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki loginwiki on mw*
* 20:58 paladox: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=americangirldollswiki --report=1 American+Girl+Wiki-20181021003500.xml on mw1

## 2018-10-29 

* 23:49 paladox: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=ucroniaswiki --report=1 Taller_Wiki-20181024160736.xml on mw1
* 14:43 Reception123: reception@mw2:/srv/mediawiki/w/maintenance$ sudo -u www-data php importDump.php --wiki americangirldollswiki /home/reception/American+Girl+Wiki-20181021003500.xml
* 14:43 Reception123: reception@mw2:/srv/mediawiki/w/maintenance$ sudo -u www-data php importDump.php --wiki americangirldollswiki /home/reception/American+Girl+Wiki-20181021003912.xml
* 14:43 Reception123: reception@mw2:/srv/mediawiki/w/maintenance$ sudo -u www-data php importDump.php --wiki americangirldollswiki /home/reception/American+Girl+Wiki-20181021003633.xml
* 00:32 paladox: stopping script (it will run by cron in a few days time)
* 00:12 paladox: running /usr/bin/nice -19 /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/extensions/RottenLinks/maintenance/updateExternalLinks.php in a screen on mw3

## 2018-10-28 

* 23:53 paladox: reboot mw3
* 23:53 paladox: reboot mw2 to stop RottenLinks maint script at 23:45:55 UTC
* 23:52 paladox: reboot mw1 to stop RottenLinks maint script at 23:45:00 utc
* 20:54 paladox: rm -rf /home/reception/bpwiki (saves another 11g)
* 20:52 paladox: rm /home/reception/nonsensopediawiki31072018.xml on mw1
* 19:13 paladox: upgrading phabricator on misc4
* 14:42 paladox: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=destinoswiki --report=1 Taller_Wiki-20181024160736.xml on mw1

## 2018-10-27 

* 22:28 paladox: php updateExternalLinks.php --wiki=sdiywiki on mw2
* 20:00 paladox: php importImages.php /home/paladox/mnt --search-recursively --wiki=psiconautawiki on mw2
* 16:02 paladox: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=psiconautawiki --report=1 /home/paladox/wiki2.xml on mw2
* 15:42 paladox: php dumpBackup.php --full --include-files --uploads --output=gzip:/home/paladox/wiki2.xml.gz --wiki=checkinwiki on mw2

## 2018-10-26 

* 20:15 John: dropping all comments tables on wikis that doesn't use comments (2815/2915)
* 19:51 John: dropping all quizgame tables on wikis that doesn't use quizgame (2887/2915)
* 19:36 paladox: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=nonciclopediawiki --report=1 nonciclopediawikiacom-20180818-history.xml on mw1
* 19:31 John: dropping all wikiforum tables on wikis that doesn't use wikiforum (2837/2915)
* 19:13 John: dropping all newsletter tables on wikis that doesn't use newsletter (2890/2915)
* 19:02 paladox: UPDATE mw_permissions SET perm_permissions = '["autocreateaccount","createaccount","read","edit","createpage","createtalk", "writeapi","viewmywatchlist","editmywatchlist","viewmyprivateinfo", "editmyprivateinfo","editmyoptions","abusefilter-log","abusefilter-log-detail", "abusefilter-view","autocreateaccount","centralauth-merge", "oathauth-enable"]' WHERE perm_dbname = "utamacrosswiki" and perm_group = "*" and perm_permissions = 'perm_permissio
* 19:00 John: dropping all pagetriage tables on wikis that doesn't use pagetriage (2887/2915)
* 17:57 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki loginwiki on mw*
* 15:04 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki loginwiki on mw*
* 09:56 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/storage/compressOld.php openhatchwiki -t gzip --wiki openhatchwiki on mw1
* 09:44 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/storage/compressOld.php buswiki -t gzip --wiki buswiki on mw1
* 09:32 paladox: sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildall.php --wiki=nonciclopediawiki on mw1
* 03:01 paladox: DELETE FROM global_group_permissions WHERE ggp_permission='centralauth-autoaccount'; on db4
* 01:16 paladox: rm cache files in /mnt/mediawiki/static/cdb/** (to invalidate cache) (they will regenerate)
* 01:12 paladox: UPDATE mw_permissions SET perm_permissions = REPLACE('perm_permissions', 'centralauth-autoaccount', 'autocreateaccount') WHERE perm_permissions LIKE '%centralauth-autoaccount%'; on db4
* 01:10 paladox: UPDATE mw_permissions SET perm_permissions = REPLACE('perm_permissions', 'centralauth-autoaccount', 'autocreateaccount') WHERE field LIKE '%centralauth-autoaccount%'; on db4
* 00:55 John: dropping all flow tables on wikis that doesn't use flow (2842/2915)
* 00:27 paladox: repooling cp2
* 00:21 paladox: depooling cp2
* 00:19 John: dropping all flaggedrevs tables on wikis that doesn't use flaggedrevs (2892/2915)

## 2018-10-25 

* 23:34 John: dropping all educationprogram tables on wikis that doesn't use educationporgram (2899/2915)
* 22:52 John: dropping all socialprofile tables on wikis that doesn't use socialprofile (2866/2915)
* 19:58 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/storage/compressOld.php nonsensopediawiki -t gzip --wiki nonsensopediawiki on mw2
* 19:54 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/storage/compressOld.php nonciclopediawiki -t gzip --wiki nonciclopediawiki on mw1
* 18:52 paladox: PURGE BINARY LOGS BEFORE '2018-10-25 19:52:00'; on db4
* 17:25 John: for reference, the last log action resulted in a 3GB disk space gain on db4
* 17:25 John: dropping all wikibase tables on wikis that doesn't use wikibase (2870/2915)

## 2018-10-24 

* 09:51 paladox: PURGE BINARY LOGS BEFORE '2018-10-24 10:46:00'; on db4
* 09:51 paladox: rebooted misc2 (to try and reduce load)
* 09:51 paladox: rebooted puppet1

## 2018-10-23 

* 13:41 paladox: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=americangirldollswiki --report=1 American+Girl+Wiki-20181021003912.xml on mw1 ref T3716
* 13:41 paladox: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=americangirldollswiki --report=1 American+Girl+Wiki-20181021003633.xml on mw1 ref T3716
* 13:39 paladox: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=americangirldollswiki --report=1 American+Girl+Wiki-20181021003500.xml on mw1 ref T3716

## 2018-10-22 

* 21:57 paladox: php /srv/mediawiki/w/extensions/CreateWiki/maintenance/renameWiki.php --wiki=loginwiki --rename hypotheticalencyclopediawiki hypopediawiki paladox on mw1
* 12:13 paladox: PURGE BINARY LOGS BEFORE '2018-10-22 13:13:00'; on db4

## 2018-10-21 

* 21:48 paladox: applying 2 security fixes ([https://gerrit.wikimedia.org/r/#/c/mediawiki/core/+/468846/](https://gerrit.wikimedia.org/r/#/c/mediawiki/core/+/468846/) and [https://gerrit.wikimedia.org/r/#/c/mediawiki/core/+/468849/](https://gerrit.wikimedia.org/r/#/c/mediawiki/core/+/468849/))
* 16:52 paladox: PURGE BINARY LOGS BEFORE '2018-10-21 17:51:00'; on db4

## 2018-10-20 

* 21:29 paladox: php populateWikiSettings.php --wiki=metawiki --sourcelist=test --wgsetting=wgShowArchiveThumbnails
* 21:19 paladox: php populateWikiSettings.php --wiki=metawiki --sourcelist=test --wgsetting=wgCopyUploadsFromSpecialUpload
* 17:33 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki loginwiki on mw*

## 2018-10-19 

* 21:23 MacFan4000: rebuilding LC on test1
* 21:13 paladox: dropping table transcache from test1wiki and also backing the db up before i drop

## 2018-10-18 

* 17:04 paladox: upgrading matomo to 3.6.1
* 15:13 paladox: upgrade icinga2 to 2.10.1 (bug fix)
* 14:55 paladox: PURGE BINARY LOGS BEFORE '2018-10-18 15:55:00'; on db4

## 2018-10-17 

* 17:55 paladox: branching REL1_32 in [https://github.com/miraheze/mediawiki](https://github.com/miraheze/mediawiki)

## 2018-10-14 

* 23:42 paladox: upgrade phabricator on misc4
* 22:13 paladox: upgrade php7.2.10 to php7.2.11
* 21:53 paladox: PURGE BINARY LOGS BEFORE '2018-10-14 22:52:00'; on db4
* 20:52 paladox: deleted twilightforestwiki per JohnLewis and because it's eligible for deletion.
* 20:32 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki loginwiki on test1
* 20:17 paladox: deleting therhizomewiki wiki per founder closed it in june.
* 16:34 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki loginwiki on test1
* 14:53 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki loginwiki on mw*

## 2018-10-13 

* 02:46 John: creating rottenlinks table on all wikis

## 2018-10-12 

* 23:19 paladox: PURGE BINARY LOGS BEFORE '2018-10-13 00:18:00'; on db4
* 19:06 paladox: upgrade cp5 kernel to 4.18 (performance/security reasons)
* 18:14 paladox: upgrading icinga2 to 2.10 and grafana

## 2018-10-11 

* 22:27 paladox: PURGE BINARY LOGS BEFORE '2018-10-11 23:27:00'; on db4
* 21:38 paladox: rm /mnt/mediawiki-static/dumps/* on mw1 (regenerating current wiki dumps)
* 16:33 paladox: restarted icingabot and adminbot on misc1

## 2018-10-10 

* 22:52 paladox: PURGE BINARY LOGS BEFORE '2018-10-10 23:51:00'; on db4
* 16:41 Reception123: sudo service icingabot restart

## 2018-10-09 

* 22:37 paladox: PURGE BINARY LOGS BEFORE '2018-10-09 23:37:00'; on db4

## 2018-10-07 

* 20:46 paladox: upgrade phabricator on misc4
* 17:48 paladox: rebooted bacula1 due to high load (no backups were in progress)

## 2018-10-06 

* 23:22 paladox: sudo -u www-data php /srv/mediawiki/w/maintenance/importImages.php images --overwrite --wiki=nonciclopediawiki --skip-dupes on mw1
* 23:11 paladox: sudo -u www-data php /srv/mediawiki/w/maintenance/importImages.php images --overwrite --wiki=nonciclopediawiki on mw1
* 23:05 paladox: started xml import for nonciclopediawiki
* 22:35 paladox: php /srv/mediawiki/w/extensions/CreateWiki/maintenance/deleteWikis.php --wiki=loginwiki --delete paladox (deleting 1cewiki indytechfixwiki kuonsamwiki mwmwiki optimathofficialwikiwiki peopleshararamwiki sovereignwiki wesleycollegewiki)
* 22:30 paladox: PURGE BINARY LOGS BEFORE '2018-10-06 23:30:00'; on db4
* 22:29 paladox: php /srv/mediawiki/w/extensions/CreateWiki/maintenance/deleteWikis.php --wiki=loginwiki --delete paladox on mw1 (deleting wmaucommwiki per [https://phabricator.miraheze.org/T3576](https://phabricator.miraheze.org/T3576))
* 14:33 paladox: install prometheus-blackbox-exporter on ns1
* 10:51 MacFan4000: sudo -u www-data php importDump.php --wiki tallerwiki /home/macfan/tallerwiki.xml

## 2018-10-05 

* 22:03 MacFan4000: sudo -u www-data php importDump.php --wiki tallerwiki /home/macfan/wikipedia.xml on mw2 in a screen
* 17:07 paladox: php /srv/mediawiki/w/extensions/CreateWiki/maintenance/deleteWikis.php --wiki=loginwiki --delete paladox (deleting wikis: centralwiki apunteswiki repositoriowiki destinoswiki mexicopediawiki tallercentralwiki ucroniawiki wiki1776wiki)

## 2018-10-04 

* 21:44 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki loginwiki on test1
* 19:21 paladox: apt-get install python3-flask on mw1
* 13:07 paladox: upgraded phabricator on misc4
* 01:00 John: updating SA rules
* 00:05 MacFan4000: running jobs everywhere

## 2018-10-03 

* 23:38 paladox: PURGE BINARY LOGS BEFORE '2018-10-04 00:37:00'; on db4
* 23:23 paladox: dbCreate.sh on db4
* 23:15 paladox: ^^ reason is deleting inactive + closed wikis
* 23:13 paladox: php /srv/mediawiki/w/extensions/CreateWiki/maintenance/deleteWikis.php --wiki=loginwiki --delete paladox on mw1
* 22:45 paladox: php populateWikiSettings.php --wiki=metawiki --sourcelist=source --wgsetting=wgUseInstantCommons on mw1
* 22:27 paladox: php populateWikiSettings.php --wiki=metawiki --sourcelist=source --wgsetting=wgAllowSlowParserFunctions on mw1
* 21:16 paladox: disabled puppet on mw*
* 20:47 paladox: php populateWikiSettings.php --wiki=metawiki --sourcelist=source --wgsetting=wgPFEnableStringFunctions on mw1
* 17:30 paladox: PURGE BINARY LOGS BEFORE '2018-10-03 18:30:00'; on db4

## 2018-10-02 

* 22:58 paladox: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=greatcharacterswikiwiki --report=1 greatcharacters_pages_full.xml on mw1
* 15:41 paladox: repool mw3
* 15:30 paladox: depool mw3
* 15:30 paladox: repool mw2
* 15:23 paladox: depool mw2
* 15:23 paladox: repool mw1
* 15:17 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki loginwiki --force on mw*
* 15:16 paladox: depool mw1 as force rebuilding lc
* 15:16 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/mergeMessageFileList.php --output /srv/mediawiki/config/ExtensionMessageFiles.php --wiki loginwiki on mw*

## 2018-10-01 

* 23:10 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki on mw*
* 22:52 paladox: php populateWikiSettings.php --sourcelist=source --wgsetting=wgVisualEditorEnableWikitext --wiki=metawiki on mw1
* 22:49 paladox: php populateWikiSettings.php --sourcelist=source --wgsetting=wgPopupsBetaFeature --wiki=metawiki on mw1
* 22:22 paladox: php populateWikiSettings.php --sourcelist=source --wgsetting=wgMediaViewerIsInBeta --wiki=metawiki on mw1
* 22:21 MacFan4000: macfan@mw2:/srv/mediawiki/w/maintenance$ sudo -u www-data php dumpBackup.php --full --wiki iconswiki > /home/macfan/iconswiki.xml
* 22:16 paladox: php populateWikiSettings.php --sourcelist=source --wgsetting=MediaViewerIsInBeta on mw1
* 15:59 paladox: upgrade to php7.2.10 on mw*

## 2018-09-30 

* 19:32 paladox: install some python3 packages that [https://git.io/fxJTk](https://git.io/fxJTk) will add to misc1
* 17:51 Reception123: restarted icingabot
* 17:46 Reception123: restarted icingabot
* 16:18 paladox: PURGE BINARY LOGS BEFORE '2018-09-30 17:18:00'; on db4
* 13:36 paladox: rm -rf * in /var/lib/puppet/reports (saves 23gb) on puppet1

## 2018-09-29 

* 15:01 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki on mw*
* 06:38 Reception123: DROP DATABASE nerdzonewiki
* 06:37 Reception123: reception@mw1:~$ sudo -u www-data php /srv/mediawiki/w/extensions/CreateWiki/maintenance/deleteWikis.php --wiki=nerdzonewiki --delete Reception123

## 2018-09-28 

* 21:39 paladox: (allthetropeswiki) TRUNCATE objectcache; on db4
* 21:21 paladox: PURGE BINARY LOGS BEFORE '2018-09-28 22:21:00'; on db4
* 14:20 paladox: install git update on *
* 14:20 paladox: install python2.7 update on *

## 2018-09-26 

* 22:58 paladox: upgraded icinga to icinga 2.9.2 on misc1

## 2018-09-24 

* 20:33 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki on test1
* 16:22 paladox: PURGE BINARY LOGS BEFORE '2018-09-24 17:22:00'; on db4

## 2018-09-23 

* 19:40 paladox: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=starmetalwiki --report=1 user%27s+Wiki%21-20180919040615.xml on mw1 in a screen
* 12:31 paladox: started static backup on bacula1 because it seems a job was not run at 12am?
* 02:16 paladox: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=nonciclopediawiki --report=1 nonciclopediawiki09102018.xml on mw1
* 02:10 paladox: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=besttvshowswiki --report=1 besttvshows938_pages_full.xml on mw1 in a screen
* 02:08 paladox: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=starmetalwiki --report=1 user%27s+Wiki%21-20180919040553.xml on mw1 in a screen

## 2018-09-22 

* 22:04 paladox: delete and recreated lizardfs-chunkserver* and lizardfs-master from bacula1
* 21:43 paladox: recreating STATIC* backup on bacula1
* 20:52 paladox: restarting db4 (it's a emergency to get the new cert)
* 14:54 paladox: recreating db4 backup on bacula1
* 14:53 Southparkfan: deleted all dummy wikis from matomo table and matomo SitesManager
* 14:41 paladox: PURGE BINARY LOGS BEFORE '2018-09-22 15:41:00'; on db4
* 14:41 Southparkfan: above entry also deleted in matomo SitesManager
* 14:37 Southparkfan: MariaDB [mhglobal]> delete from matomo where matomo_id = 3246; (dummy entry)
* 14:31 paladox: recreating LIZARDFS1-CHUNKSERVER* backup on bacula1
* 14:29 paladox: recreating phabstatic backup on bacula1
* 13:18 paladox: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=starmetalwiki --report=1 user%27s+Wiki%21-20180919040511.xml on mw1

## 2018-09-21 

* 16:15 paladox: fixing microtonalwiki in mw_permissions on db4.
* 14:56 paladox: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=awfulmovieswiki --report=1 awfulmovies_pages_full.xml on mw1 in a screen

## 2018-09-20 

* 21:40 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki on mw*

## 2018-09-19 

* 21:54 paladox: /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/maintenance/sql.php /srv/mediawiki/w/extensions/ApprovedRevs/sql/ApprovedRevs.sql on mw1
* 21:26 paladox: PURGE BINARY LOGS BEFORE '2018-09-19 22:25:00'; on db4
* 19:07 paladox: upgrade phabricator on misc4
* 18:26 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki on mw* and test1
* 16:24 paladox: sudo -u www-data php /srv/mediawiki/w/maintenance/importImages.php /home/paladox/_Images --wiki=wikiageingwiki --search-recursively on mw1
* 15:18 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki on mw* and test1

## 2018-09-18 

* 23:09 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki on mw*
* 22:11 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki on mw*
* 18:30 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki on mw*

## 2018-09-17 

* 19:15 John: deleted all redis keys matching *:ManageWiki:*

## 2018-09-16 

* 15:41 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki on mw* and test1
* 00:18 paladox: drop table logging on metawiki;
* 00:02 paladox: drop database centralauth has been moved to a new db (again part 2)

## 2018-09-15 

* 23:55 paladox: drop database centralauth has been moved to a new db
* 23:53 paladox: drop tables cw_wikis, cw_requests, cw_comments, mw_permissions and matomo from metawiki;
* 23:17 paladox: create mhglobal db
* 23:16 paladox: apply new mediawiki grants
* 15:34 paladox: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=loathsomecharacterswiki --report=1 loathsomecharacters_pages_full.xml on mw1 in a screen

## 2018-09-14 

* 22:47 paladox: upgrade phabricator on misc4
* 18:12 paladox: PURGE BINARY LOGS BEFORE '2018-09-14 19:12:00'; on db4
* 18:05 paladox: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=atrociousyoutuberswiki --report=1 atrociousyoutubers_pages_full.xml on mw1 in a screen

## 2018-09-13 

* 21:02 MacFan4000: running jobs everywhere
* 20:29 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki on mw* and test1
* 19:39 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki on mw* and test1
* 19:34 paladox: /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/maintenance/sql.php /srv/mediawiki/w/extensions/ApprovedRevs/sql/ApprovedRevs.sql on mw1 in a screen
* 18:00 Reception123: reception@mw2:~/NonciclopediaDump_2018-08-18$ sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=nonciclopediawiki /home/reception/NonciclopediaDump_2018-08-18/nonciclopediawikiacom-20180818-history.xml
* 17:55 Reception123: reception@mw2:/srv/mediawiki/w/maintenance$ sudo -u www-data php importImages.php --wiki nonciclopediawiki --search-recursively /home/reception/NonciclopediaDump_2018-08-18/images
* 16:29 paladox: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=terribletvshowswiki --report=1 terribletvandwebshows_pages_full.xml on mw1 in a screen
* 14:55 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki on mw*
* 13:20 paladox: repool mw3
* 12:41 paladox: depool mw3

## 2018-09-12 

* 22:11 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki on mw*
* 21:45 MacFan4000: xUPDATE cw_requests SET cw_status='declined' WHERE cw_url='imsaiki.miraheze.org';
* 21:44 MacFan4000: UPDATE cw_requests SET cw_custom='[SPAM]' WHERE cw_url='imsaiki.miraheze.org';
* 21:43 MacFan4000: UPDATE cw_requests SET cw_sitename='[SPAM]' WHERE cw_url='imsaiki.miraheze.org';
* 21:40 MacFan4000: UPDATE cw_requests SET cw_comment='[SPAM]' WHERE cw_custom='I'm sexy and I know it. I'm sexy and you know it. So how bout this: I'll take my shirt off'; (spam)
* 21:17 paladox: recreating howtograde wiki
* 21:03 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki on mw*
* 17:13 John: rerunning populateGroupPermissions.php on all wikis
* 16:50 paladox: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=wmaucommwiki --report=1 commwiki-pages.xml on mw1
* 16:43 Reception123: reception@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php importImages.php --wiki wmaucommwiki --search-recursively /home/reception/wmau/commwiki_2018-09-12/images
* 16:34 Reception123: reception@mw3:/srv/mediawiki/w/maintenance$ sudo -u www-data php importDump.php --wiki awesomegameswiki /home/reception/awesomegames993_pages_full.xml
* 16:02 paladox: deleted managewiki cdb file on mw*

## 2018-09-11 

* 22:27 John: populatingGroupPermissions for all wikis
* 22:10 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki on test1
* 20:53 John: removed master branch restrictions on mw-config, wasn't approved and I was heavily against it
* 17:21 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki on mw*
* 00:14 MacFan4000: running jobs everywhere in a screen

## 2018-09-10 

* 19:22 MacFan4000: UPDATE cw_requests SET cw_status='declined' WHERE cw_custom='sexy'; (spam)
* 17:52 John: running jobs on mw1
* 17:50 paladox: upgrade php7.2 on misc4
* 17:47 paladox: upgrade php7.2 on misc2
* 17:47 paladox: upgrade grafana and php7.2 on misc1
* 17:43 paladox: upgrading php7.2 on mw* and test1*
* 13:25 Reception123: DROP DATABASE nonciclopediawiki
* 13:25 Reception123: > DELETE FROM cw_wikis WHERE wiki_dbname = 'nonciclopediawiki';
* 10:39 Reception123: removed spam from cw_requests
* 02:49 PuppyKun: MariaDB [crappygameswiki]> delete from page where page_id=3878 or page_id=42585;
* 02:48 PuppyKun: (read only) searched for a bunch of pages by title and page id, didnt find anything useful
* 02:48 PuppyKun: populated content model for all namespaces archive/page/revision tables on crappygameswiki
* 02:48 PuppyKun: did a bunch of stuff on crappygames.mh.o / db trying to find corrupted flow pages

## 2018-09-09 

* 20:53 MacFan4000: stopped running jobs and restarted in a screen
* 20:46 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki on test1
* 20:44 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki on mw*
* 20:41 MacFan4000: macfan@mw2:~$ sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/maintenance/runJobs.php --type=LocalGlobalUserPageCacheUpdateJob
* 19:03 Southparkfan: deleted ALL LocalGlobalUserPageCacheUpdateJob and htmlCacheUpdate jobs for ALL wikis
* 18:56 Southparkfan: mw2: /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/maintenance/runJobs.php --type=LocalGlobalUserPageCacheUpdateJob
* 18:51 Southparkfan: restarted jobrunner on mw3 + kill runJobs.php process
* 18:47 Southparkfan: killed runJobs.php on mw2
* 18:34 Southparkfan: deleted another 5k htmlCacheUpdate jobs for microtonalwiki
* 18:29 Southparkfan: clear 63k htmlCacheUpdate jobs for crappygameswiki; deleted all redis keys matching "crappygameswiki:jobqueue:htmlCacheUpdate:*"
* 17:37 Reception123: sudo -u www-data foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/maintenance/runJobs.php on all mw wikis and test1wiki (huge queue)
* 16:43 paladox: fixed duplicates in mw_permissions for testwiki T3574
* 16:36 paladox: fixed duplicates in mw_permissions for wiki1776wiki T3574
* 14:05 paladox: fixed duplicates in mw_permissions for weatherwiki T3574
* 13:46 paladox: fixed duplicates in mw_permissions for metawiki T3574
* 13:44 paladox: fixed duplicates in mw_permissions for test1wiki T3574
* 10:57 Reception123: /srv/mediawiki/w/maintenance && sudo -u www-data php rebuildLocalisationCache.php --wiki test1wiki on mw*

## 2018-09-08 

* 16:28 paladox: upgrade phabricator on misc4
* 15:56 paladox: SET GLOBAL general_log = 'OFF'; on db4
* 15:00 paladox: SET GLOBAL query_cache_size = 1000000; on db4
* 14:48 paladox: SET GLOBAL general_log = 'ON'; on db4
* 14:19 paladox: restarting mysql on db4 due to high cpu / load
* 12:26 paladox: PURGE BINARY LOGS BEFORE '2018-09-08 13:26:00'; on db4
* 11:26 paladox: drop databse cpprwiki;
* 11:23 paladox: renaming wiki from cpprwiki to leyesprwiki
* 01:07 paladox: remove php-tideways from test1

## 2018-09-07 

* 21:36 John: populating usergroup on all wikis in mw_permissions
* 18:59 paladox: repool mw3
* 18:40 paladox: reboot mw3
* 18:35 paladox: depool mw3 because of high load
* 14:21 paladox: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=crappygameswiki --report=1 crappygames_pages_full.xml per [https://phabricator.miraheze.org/T3565](https://phabricator.miraheze.org/T3565)
* 14:07 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki on test1
* 14:05 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki on mw*

## 2018-09-06 

* 22:08 John: added defaults
* 18:16 paladox: drop database pmspacewiki
* 18:14 paladox: renaming pmspacewiki to ourmetawiki per [https://phabricator.miraheze.org/T3544](https://phabricator.miraheze.org/T3544)
* 17:23 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki on test1
* 16:34 paladox: testing things on puppet1
* 15:30 paladox: repool cp5
* 14:15 paladox: depool cp5 for reimage
* 12:43 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki on mw*

## 2018-09-05 

* 17:32 paladox: apache2 removed from misc1
* 16:38 paladox: drop database wulfmaerwiki from db4
* 16:37 paladox: deleting wulfmaerwiki wiki per [https://phabricator.miraheze.org/T3560](https://phabricator.miraheze.org/T3560)

## 2018-09-04 

* 18:39 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki on test1
* 18:37 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki on mw*

## 2018-09-03 

* 21:20 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki on mw* and test1

## 2018-09-02 

* 22:45 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki on test1
* 22:43 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki on mw*
* 22:26 paladox: PURGE BINARY LOGS BEFORE '2018-09-02 23:26:00'; on db4
* 21:25 paladox: starting BackupStaticLizardfs1 and BackupStaticLizardfs2 on bacula
* 21:20 paladox: deleting static bacula files (will restart the backup)
* 21:18 paladox: deleting static bacula files (will restart the backup)
* 21:06 paladox: php deleteBatch.php --wiki=2b2twiki test on mw1 for T3548
* 19:01 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki on mw*
* 18:51 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki on test1
* 17:54 paladox: upgrade php7.2 and grafana on misc1
* 04:43 PuppyKun: force changed the passwd for ndkilla on misc1
* 03:35 John: populateGroupPermissions.php on weatherwiki and wiki1776wiki
* 00:48 John: things look like they're correct on testwiki, no restrictive groups have moved over. restricted rights have moved over, so they can't be removed from the groups (intentional) but can't be added and so on.
* 00:45 John: ran populateGroupPermissions.php on testwiki

## 2018-09-01 

* 19:24 Reception123: srv/mediawiki/w/maintenance/dumpBackup.php --wiki bootstrappingwiki --logs --full --uploads > /mnt/mediawiki-static/dumps/bootstrappingwiki01092018.xml
* 17:46 paladox: upgrade phabricator on misc4
* 17:40 paladox: upgrade to php 7.2.9 (from 7.2.8) on mw* and test1*
* 15:02 Reception123: re-enabled puppet on cp*
* 11:11 Reception123: disabled Puppet on cp*

## 2018-08-31 

* 19:34 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki on mw* and test1
* 16:23 paladox: restarting puppetdb on puppet1
* 15:30 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki on mw*
* 13:50 John: see [https://phabricator.miraheze.org/P102](https://phabricator.miraheze.org/P102) for list of wikis for when reversion happens
* 13:49 John: disabled TimedMediaHandler on all wikis
* 13:49 John: MariaDB [metawiki]> UPDATE cw_wikis SET wiki_extensions = REPLACE( wiki_extensions, ',timedmediahandler',* ) WHERE wiki_extensions LIKE '%timedmediahandler%';

## 2018-08-30 

* 21:58 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki on mw*
* 21:17 Southparkfan: install php-tideways on test1
* 20:49 Southparkfan: enable puppet on cp4
* 20:37 Southparkfan: disable cp4 puppet
* 20:35 Southparkfan: sudo salt -E 'cp.*' cmd.run "sudo varnishadm 'ban req.http.Host == matomo.miraheze.org'"
* 19:24 Southparkfan: delete wrong allow rule on mw[1-3]
* 19:09 Southparkfan: remove non strict firewall rules from mw[1-3] per [https://git.io/fAcuR](https://git.io/fAcuR)
* 16:53 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki on mw* and test1
* 15:49 paladox: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=electowikiwiki --report=1 fix.xml on mw1 in a screen
* 15:42 paladox: actually doin't need to backup as i have the dump
* 15:38 paladox: mysql electowikiwiki > /home/paladox/electowiki.sql on db4
* 15:36 paladox: deleting electowiki and recreating per T3537
* 10:27 Reception123: sudo -u www-data foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/maintenance/runJobs.php on mw1
* 06:25 Reception123: reception@mw3:/srv/mediawiki/w/maintenance$ sudo -u www-data php importDump.php --wiki electowikiwiki /home/reception/Electowiki-20180826232629_ovr.xml
* 00:57 paladox: git checkout 632cafec8 due to a error on the master branch that needs fixing (phabricator (misc4))

## 2018-08-29 

* 22:26 paladox: switching phabricator to nginx
* 20:30 Southparkfan: puppet enabled on misc2
* 20:20 Southparkfan: disable puppet on misc2 again
* 19:52 Southparkfan: migrating piwik to nginx, intermittent service for now
* 19:05 Southparkfan: disable misc2 puppet
* 18:31 Reception123: sudo -u www-data php rebuildLocalisationCache.php --wiki test1wiki on mw*
* 18:02 Southparkfan: enable puppet on cp4 and misc2
* 17:51 Southparkfan: restarted misc2 apache
* 17:28 Southparkfan: disable puppet on misc2
* 17:27 Southparkfan: disable puppet on cp4
* 15:35 John: storing sql dump of mussmanwissenwiki and removing from Miraheze & ban.req on cp* for the domain
* 07:14 Reception123: reception@mw3:/srv/mediawiki/w/maintenance$ sudo -u www-data php importDump.php --wiki electowikiwiki /home/reception/Electowiki-20180826232629.xml

## 2018-08-28 

* 15:38 paladox: running php /srv/mediawiki/w/extensions/CreateWiki/maintenance/manageInactiveWikis.php --wiki=metawiki --warn --close on mw1
* 15:05 paladox: PURGE BINARY LOGS BEFORE '2018-08-28 16:05:00'; on db4
* 14:38 paladox: reboot puppet1 to see if it fixes puppet compilations problems
* 13:31 Reception123: added jadtechwiki to hiera for DiscordNotifications
* 13:13 paladox: upgrade phabricator on misc4

## 2018-08-27 

* 22:27 Southparkfan: MariaDB [weatherwiki]> truncate nl_newsletters; truncate nl_publishers; truncate nl_subscriptions; delete from archive where ar_id in (257, 258);
* 21:35 Southparkfan: MariaDB [weatherwiki]> update nl_newsletters set nl_active = 1 where nl_id = 1;
* 13:37 Reception123: REVOKED DROP from wikiadmin
* 13:36 John: REVOKE SELECT, INSERT, UPDATE, DELETE, CREATE, DROP, INDEX, ALTER, CREATE VIEW ON `%wik%`.* FROM 'wikiadmin'@'%';
* 13:36 John: REVOKE SELECT, INSERT, UPDATE, DELETE, CREATE, DROP, INDEX, ALTER, CREATE VIEW ON `%wik%`.* FROM 'mediawiki'@'%';
* 06:24 Reception123: running wikibackups for public wikis
* 01:55 John: emailing disclosure emails to all users on jawp2chwiki
* 00:26 MacFan4000: deleting test1deletewiki and test11deletewiki (mine)

## 2018-08-26 

* 22:38 John: running resetGlobalUserTokens.php for [https://phabricator.miraheze.org/T3520](https://phabricator.miraheze.org/T3520)
* 21:17 John: added mw_permissions to metawiki database and run populateGroupPermissions.php for test1wiki
* 08:52 Reception123: sudo service icingabot restart

## 2018-08-25 

* 08:43 Reception123: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=rottenwebsiteswiki /home/reception/rottenwebsites_pages_full.xml on mw3

## 2018-08-24 

* 11:03 Reception123: renamed ourjokewiki to unpediawiki (in CW_WIKIS, CentralAuth, db and static)

## 2018-08-23 

* 06:48 Reception123: sudo -u www-data php rebuildLocalisationCache.php --wiki test1wiki on mw*

## 2018-08-22 

* 16:21 paladox: php rebuildAll.php on mw1 for altversewiki
* 16:13 paladox: restarted icingabot
* 16:05 Reception123: sudo -u www-data foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/maintenance/runJobs.php on mw1,mw2,test1
* 15:39 paladox: apt-get upgrade openssh (security update) on *

## 2018-08-21 

* 06:27 Reception123: DELETE AND DROP hiawawiki

## 2018-08-20 

* 12:58 MacFan4000: sudo -u www-data php rebuildLocalisationCache.php --wiki loginwiki on mw*

## 2018-08-18 

* 00:11 paladox: upgrade phabricator on misc4
* 00:02 paladox: restarting mariadb to apply config change

## 2018-08-17 

* 23:49 paladox: PURGE BINARY LOGS BEFORE '2018-08-18 00:48:00'; on db4
* 00:36 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki on mw*

## 2018-08-16 

* 22:24 paladox: upgrade phabricator on misc4
* 19:56 paladox: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=weatherwiki --report=1 Wikipedia-20180816191454.xml on mw1
* 14:18 Reception123: rebuild LC on test1wiki
* 13:48 Reception123: sudo -u www-data php importImages.php --wiki quranwiki --search-recursively /home/reception/archive_unzipped

## 2018-08-15 

* 20:21 paladox: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=asheeshscratchwiki --report=1 /home/paladox/test.xml on mw1
* 18:03 paladox: remove CookieWarning hack from mw* and apply commit that has the fix
* 17:40 paladox: applying CookieWarning hack to mw3
* 17:30 paladox: applying CookieWarning hack to mw2
* 17:11 paladox: hacking CookieWarning on mw1 to apply hot fix
* 15:38 Reception123: sudo service ircrcbot restart
* 14:35 Reception123: reception@mw3:/srv/mediawiki/w/maintenance$ sudo -u www-data php importImages.php --wiki quranwiki --search-recursively /home/reception/QP2
* 13:56 Reception123: sudo -u www-data php importImages.php --wiki quranwiki --search-recursively /home/reception/QP on mw3
* 01:11 paladox: apt-get upgrade on all *

## 2018-08-14 

* 23:03 paladox: upgrading mariadb on db4 - brief service interuption (also rebooting for kernel update)
* 22:58 paladox: reboot cp5 for kernel upgrade
* 22:21 paladox: reboot bacula1 for kernel update

## 2018-08-13 

* 23:06 paladox: reboot misc3 to clear unused ram from mathoid
* 21:49 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki on test1
* 12:57 paladox: sudo -u www-data php /srv/med*/w/maint*/importDump.php --wiki wikiageingwiki --report=1 /home/paladox/wikiageingorg-20180813-history.xml on mw1

## 2018-08-12 

* 19:31 PuppyKun: added Paladox as a designated admin on the linked in page, or something
* 18:08 Reception123: MOVED adventuretimewiki to digimonwiki
* 15:03 Reception123: reception@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php importDump.php --wiki wikiageingwiki /home/reception/wikiageingorg-20180805-history.xml
* 10:04 Reception123: disabled Rappy_4187

## 2018-08-11 

* 16:42 paladox: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=mexicopediawiki --report=1 TallerCentral-20180807182946.xml on mw1
* 16:42 paladox: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=ucroniawiki --report=1 TallerCentral-20180807182946.xml on mw1
* 16:28 paladox: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=mexicopediawiki --report=1 Wikipedia-20180729190338.xml.1 on mw1
* 16:26 paladox: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=ucroniawiki --report=1 Wikipedia-20180729190338.xml on mw1
* 15:58 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki on mw*
* 15:53 paladox: PURGE BINARY LOGS BEFORE '2018-08-11 16:53:00'; on db4
* 15:41 paladox: /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/maintenance/sql.php /srv/mediawiki/w/extensions/PollNY/sql/poll.sql on mw1 in a screen
* 15:22 paladox: ./bin/repository rebuild-identities --all on misc4
* 15:16 paladox: upgrade phabricator on misc4
* 00:23 paladox: apt-get upgrade on *

## 2018-08-10 

* 21:02 paladox: upgrade postgresql on db4
* 00:49 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki on mw* and test1
* 00:08 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki on test1 and mw*

## 2018-08-09 

* 23:05 John: UPDATE cw_wikis SET wiki_inactive=0,wiki_inactive_timestamp=NULL WHERE wiki_closed = 1 AND wiki_inactive = 1;
* 22:56 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki on mw*

## 2018-08-08 

* 01:10 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/importImages.php /home/paladox/wiki/images --search-recursively --wiki=openhatchwiki on mw1

## 2018-08-07 

* 14:01 paladox: repool mw1
* 13:52 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki on mw*
* 11:32 John: depool mw1
* 11:19 paladox: PURGE BINARY LOGS BEFORE '2018-08-07 12:18:00'; on db4
* 02:08 paladox: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=openhatchwiki --report=1 /home/paladox/test.xml on mw1
* 00:43 paladox: /home/paladox/create_account.sh on db4

## 2018-08-06 

* 22:35 John: root@mw3:/srv/mediawiki/w/extensions/CentralAuth/maintenance# php migrateAccount.php --username TodaracSeven --wiki loginwiki --auto
* 21:28 paladox: reboot cp5 for kernel update
* 18:59 paladox: reboot bacula1
* 18:59 paladox: upgrade bacula1 kernel

## 2018-08-05 

* 20:34 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki on test1
* 20:31 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki on mw*
* 19:59 MacFan4000: sudo -u www-data php rebuildLocalisationCache.php --wiki test1wiki on mw*
* 16:51 paladox: one final mariadb restart for conf to take affect
* 13:47 paladox: PURGE BINARY LOGS BEFORE '2018-08-05 14:47:00'; on db4
* 01:08 paladox: upgrade phabricator on misc4

## 2018-08-04 

* 00:21 paladox: PURGE BINARY LOGS BEFORE '2018-08-04 01:21:00'; on db4

## 2018-08-03 

* 21:38 paladox: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=tallercentralwiki --report=1 Wikipedia-20180731213556.xml on mw2
* 14:19 MacFan4000: macfan@mw1:/srv/mediawiki/w/extensions/ManageWiki/maintenance$ sudo -u www-data php populateWikiSettings.php --wgsetting=wgAppleTouchIcon --sourcelist=/home/macfan/appletouch.txt --wiki metawiki
* 13:48 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki on test1
* 13:46 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki on mw*
* 13:16 MacFan4000: on mw1
* 13:16 MacFan4000: sudo -u www-data php deleteBatch.php -r "Deleteing per request on phab" --listfile /home/macfan/delete.txt --wiki 2b2twiki

## 2018-08-02 

* 20:06 paladox: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=destinoswiki --report=1 Wikiviajes-20180729190427.xml on mw1
* 14:17 Reception123: sudo -u www-data php /srv/mediawiki/w/extensions/CreateWiki/maintenance/removeDeletedWikis.php --wiki metawiki
* 14:16 Reception123: > DELETE FROM cw_wikis WHERE wiki_dbname = 'unionwiki'; T3408
* 14:06 Reception123: reception@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php importDump.php --wiki tallercentralwiki /home/reception/Wikipedia-20180731213556.xml
* 12:43 paladox: PURGE BINARY LOGS BEFORE '2018-08-02 13:38:00'; on db4.
* 10:29 Reception123: created a Matomo account for MacFan4000
* 09:15 Reception123: > UPDATE page SET page_content_model='wikitext' WHERE page_content_model='flow-board'; on warapediawiki
* 00:15 paladox: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=tanukipediawiki --report=1 jatanukipedia_pages_full.xml on mw1 in a screen

## 2018-08-01 

* 23:25 paladox: reset password for Saper, spoke to the user in #mediawiki
* 22:04 paladox: reboot mw1 to reduce load on db4
* 17:29 paladox: rebooted mw1 to reduce load on db4
* 14:20 John: updated Lincode email from ops@ -> labster's personal email
* 01:56 paladox: /mode #miraheze +r (to prevent the spam going around freenode). remove +r if you see this message and haven't done so
* 01:36 paladox: reboot cp5
* 00:52 paladox: depool and reboot mw1
* 00:52 paladox: repool mw2
* 00:49 paladox: reboot mw2
* 00:49 paladox: depool mw2
* 00:49 paladox: repool mw3
* 00:46 paladox: reboot mw3
* 00:46 paladox: depool mw3

## 2018-07-31 

* 22:53 paladox: repool mw1
* 22:53 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki on mw1
* 20:44 paladox: upgrade phabricator on misc4
* 20:23 paladox: depool mw1
* 20:12 paladox: repool mw2
* 20:09 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki on mw2
* 19:50 paladox: depool mw2
* 19:35 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki on mw3
* 19:30 paladox: php namespaceDupes.php --wiki= nonsensopedia wiki on mw3
* 19:16 paladox: repool mw3
* 18:59 paladox: depool mw3
* 18:57 Reception123: sudo -u www-data foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/maintenance/runJobs.php on mw2
* 18:41 Reception123: sudo -u www-data foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/maintenance/runJobs.php on test1
* 18:38 Reception123: sudo -u www-data foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/maintenance/runJobs.php on mw1
* 18:27 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki on test1
* 18:08 John: delete stray DB4-0003 on bacula1
* 17:57 Reception123: reception@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php dumpBackup.php --wiki nonsensopediawiki --full > /home/reception/nonsensopediawiki31072018.xml
* 14:39 paladox: reboot cp2
* 14:07 Reception123: sudo service icingabot restart
* 11:45 Reception123: restarted bots on misc1

## 2018-07-30 

* 22:49 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki on mw*
* 21:53 John: removed simplicitysolutionsgroupwiki from cw_wikis
* 15:00 Reception123: sudo -u www-data foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/maintenance/runJobs.php on mw1
* 14:59 paladox: PURGE BINARY LOGS BEFORE '2018-07-30 15:59:00'; on db4
* 14:55 Reception123: DROP DATABASE tallerwiki;
* 14:55 Reception123: DROP DATABASE unidoswiki;
* 14:54 Reception123: DROP DATABASE simplicitysolutionsgroupwiki;
* 14:53 Reception123: > DELETE FROM cw_wikis WHERE wiki_dbname = 'mexicopediawiki'; and DROP DATABASE mexicopediawiki
* 14:30 Reception123: reception@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php importDump.php --wiki ucroniawiki /home/reception/Wikipedia-20180729190338.xml
* 08:21 Reception123: sudo service ircrcbot restart
* 05:55 Reception123: reception@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php importDump.php --wiki mexicopediawiki /home/reception/Wikipedia-20180729190338.xml

## 2018-07-29 

* 22:52 paladox: upgrade icinga to icinga2 on misc1
* 13:38 paladox: reboot cp2

## 2018-07-28 

* 20:44 paladox: PURGE BINARY LOGS BEFORE '2018-07-28 21:43'; on db4
* 18:17 paladox: reboot cp2 to regain ram
* 11:23 Reception123: /srv/mediawiki/w/extensions/CreateWiki/maintenance/removeDeletedWikis.php --wiki testwiki on mw1
* 11:20 Reception123: > DELETE FROM cw_wikis WHERE wiki_dbname = 'unidoswiki'; and > DELETE FROM cw_wikis WHERE wiki_dbname = 'tallerwiki'; T3409 T3410
* 07:42 Reception123: reception@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php dumpBackup.php --wiki allthetropeswiki --full > /home/reception/allthetropeswiki27072018.xml

## 2018-07-27 

* 13:18 paladox: reboot cp2 (to regain some mem)

## 2018-07-26 

* 23:13 paladox: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=2b2twiki --report=1 imaspeedrunner_pages_full_07-08-2018.xml on mw2
* 09:41 Reception123: runJobs.php on all wikis on test1 as well to alleviate queue
* 09:39 Reception123: sudo -u www-data foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/maintenance/runJobs.php on mw1
* 00:16 paladox: upgrade phabricator on misc4
* 00:12 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki on mw* and test1

## 2018-07-25 

* 23:11 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki loginwiki on mw* and test1
* 22:56 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki loginwiki on test1
* 22:53 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki loginwiki on mw*
* 22:44 paladox: reboot cp2
* 21:43 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki loginwiki on mw*
* 13:53 John: running runJob.php on all wikis across mw1 and mw2, restarting jobrunner on mw3
* 04:46 PuppyKun: running all jobs on all wikis (average of 2 jobs per wiki but they seem to not be going down and ~20 wikis have more)

## 2018-07-24 

* 17:10 Reception123: ./test.sh /home/reception/allpublic.dblist /srv/mediawiki/w/maintenance/dumpBackup.php (backups for public wikis)

## 2018-07-23 

* 21:27 paladox: redis-cli KEYS "allthetropeswiki:*" | xargs redis-cli  DEL on misc2.
* 19:44 Reception123: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki on mw*
* 19:10 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki on mw1
* 18:40 paladox: PURGE BINARY LOGS BEFORE '2018-07-23 00:00:00'; on db4
* 18:39 paladox: rm -rf /srv/backup on db4 (mw1 backup that is no longer needed for now)
* 16:15 John: looping MatomoAnalytics::addSite( $wgDBname)
* 15:23 paladox: repool mw1
* 14:51 paladox: reboot mw1
* 14:50 paladox: depool mw1
* 14:49 John: added matomo.sql to metawiki and prepopulated IDs 2 (allthetropeswiki), 3 (nonbinarywiki) and 14 (testwiki)
* 14:48 Southparkfan: ran update-rc.d ssh defaults on mw1
* 00:21 Southparkfan: running varnishlog daemon on cp4: varnishlog -g raw -i Backend_health -a -w /var/log/varnish/debug-spf.log -D

## 2018-07-22 

* 23:19 Southparkfan: repooled mw1
* 23:14 Southparkfan: depooled mw1 on cp4
* 23:07 Southparkfan: chmod 755 /var/log/icinga/icinga.log on misc1

## 2018-07-21 

* 19:46 paladox: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=riptowiki --report=1 /home/paladox/imaspeedrunner_pages_full_07-08-2018.xml on mw2

## 2018-07-20 

* 22:57 paladox: repool mw1
* 21:28 paladox: reinstalling mw1
* 15:00 paladox: depool mw1
* 14:38 paladox: rebooted mw1 due to high load (seeing if this will help relieve it)
* 12:38 paladox: rm /srv/phab/images/images.tar.gz on misc4
* 12:09 MacFan4000: paladox is rebuilding LC on mw*
* 03:08 paladox: reimaging mw3 due to it stopping all services instead of them comming back on boot
* 02:39 paladox: depool mw3 to reclone mw
* 01:41 paladox: rm -rf /srv/node on swift[12]
* 01:07 paladox: repool mw1

## 2018-07-19 

* 22:03 paladox: deleting "static" pool from bacula
* 12:00 paladox: depool mw1
* 01:50 paladox: update cp5, cp4, cp2 to stretch 9.5 (point release) (and reboot them one by one)

## 2018-07-15 

* 23:46 paladox: [23:59:35]  <+paladox>	!log upgrading mariadb and stretch to 9.5 point release (and also reboot)
* 23:46 paladox: [23:57:09]  <+paladox>	!log stopping mysql on db4
* 22:48 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki on test1
* 21:43 paladox: reboot swift2
* 20:43 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki on mw*
* 16:58 paladox: upgrade misc1 to stretch 9.5 (point release) and reboot
* 13:18 paladox: rebooting misc4, swift and test1 to gain FUSE.
* 00:14 paladox: upgrade arcanist on misc4
* 00:12 paladox: upgrade misc4 to stretch 9.5 and reboot
* 00:08 paladox: upgrading swift1 and swift2 to stretch 9.5 point release (and a reboot)

## 2018-07-14 

* 20:33 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki on mw*
* 19:31 paladox: upgrade to stretch 9.5 (point release) on test1 and restart
* 19:17 paladox: upgrading puppet1 to stretch 9.5 point release (also reboot)
* 19:15 paladox: upgrading bacula1 to stretch 9.5 point release (also reboot)
* 19:09 paladox: upgrading misc2 to stretch 9.5 point release (also reboot)
* 19:07 paladox: upgrading misc3 to stretch 9.5 point release (also reboot)
* 19:04 paladox: depool mw3, update mw3 to stretch 9.5 (point release), restart mw3 and repool mw3
* 18:58 paladox: depool mw2, update mw2 to stretch 9.5 (point release), restart mw2 and repool mw2
* 18:53 paladox: repool mw1
* 18:52 paladox: reboot mw1 for point update.
* 18:50 paladox: upgrade mw1 to stretch 9.5 (point update)
* 18:50 paladox: depool mw1

## 2018-07-13 

* 19:15 paladox: rebooted swift1 to reduce ram.
* 18:07 MacFan4000: macfan@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php importDump.php --wiki vsfanwiki /home/macfan/dump.xml in a screen
* 00:11 paladox: reboot swift* OOM

## 2018-07-12 

* 15:40 paladox: /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/maintenance/sql.php /srv/mediawiki/w/extensions/Newsletter/sql/nl_newsletters-add-subscriber_count.sql on mw1

## 2018-07-11 

* 23:56 Southparkfan: created /srv/mediawiki/opcache.php on mw1, will be removed soon (not worth puppetising), only contains non-private opcache information
* 23:25 Southparkfan: cleared a mysql log file with :>/proc/1614/fd/442
* 22:12 MacFan4000: on mw*
* 22:12 MacFan4000: sudo -u www-data php rebuildLocalisationCache.php --wiki test1wiki
* 20:58 paladox: restarted php7.2-fpm on mw2
* 19:48 paladox:  swift post -r '.r:*' jawp2chwiki-mw
* 18:42 MacFan4000: macfan@test1:/srv/mediawiki/w/maintenance$ sudo -u www-data php rebuildLocalisationCache.php --wiki test1wiki
* 17:21 Reception123: rm -rf /srv/mediawiki on test1
* 15:09 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki on mw*
* 07:27 Reception123: sudo -u www-data php rebuildLocalisationCache.php --wiki test1wiki on mw*
* 00:53 MacFan4000: sudo -u www-data php rebuildLocalisationCache.php --wiki test1wiki on mw*

## 2018-07-10 

* 02:50 paladox: sudo /srv/phab/phabricator/bin/auth strip --all-types --user Samwilson on misc4

## 2018-07-09 

* 12:57 paladox: PURGE BINARY LOGS BEFORE DATE(NOW() - INTERVAL 0 DAY) + INTERVAL 0 SECOND; on db4
* 08:15 Reception123: sudo -u www-data php importDump.php --wiki xenharmonicwiki /home/reception/current.xml on mw1

## 2018-07-07 

* 21:55 paladox: delete wiki ironsagawiki per request [https://phabricator.miraheze.org/T3325#62858](https://phabricator.miraheze.org/T3325#62858)
* 11:56 Reception123: sudo -u www-data php /srv/mediawiki/w/maint*/mergeMessageFileList.php --output /srv/mediawiki/config/ExtensionMessageFiles.php --wiki test1wiki and and rebuild LC

## 2018-07-06 

* 22:04 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki on mw*
* 13:49 paladox: pooling swift2 with weight of 25
* 01:24 paladox: reinstalling nfs1 as a swift cluster
* 01:23 John: purged binlogs on db4
* 01:17 John: removed phabricator from misc1

## 2018-07-05 

* 02:44 paladox: upgrade phabricator on misc1

## 2018-07-03 

* 13:54 John: UPDATE cw_wikis SET wiki_inactive=0,wiki_inactive_timestamp=NULL WHERE wiki_inactive = 1 AND wiki_closed = 1;
* 13:44 MacFan4000: macfan@mw1:/srv/mediawiki/w/extensions/CreateWiki/maintenance$ sudo -u www-data php manageInactiveWikis.php --wiki metawiki --close --warn
* 00:48 John: learned SA some more, 35/200 messages examined before SA can be fully deployed without issue

## 2018-07-02 

* 20:27 paladox: depool mw1 for one final swift sync
* 15:24 paladox: PURGE BINARY LOGS BEFORE DATE(NOW() - INTERVAL 1 DAY) + INTERVAL 0 SECOND; on db4
* 14:26 paladox: repool mw1 after swift upload
* 06:55 Reception123: reception@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php dumpBackup.php --wiki atlantisboardwiki --full > /home/reception/atlantisboard02072018.xml

## 2018-07-01 

* 21:29 paladox: depooling mw1 to try and reduce load when running load intensive script
* 05:32 PuppyKun: closed ticket with bacula after acknowledging response and confirming i could ping and ssh the host
* 05:03 PuppyKun: opened support ticket with backupsy (bacula1.mh.o host)
* 00:01 paladox: ./upload.sh /srv/mediawiki/dblist/all.dblist on test1 (this will upload /mnt/mediawiki-static wiki containers to the container created.

## 2018-06-30 

* 19:35 MacFan4000: macfan@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php importDump.php --wiki templatewiki /home/macfan/Wikipedia-20180630172333.xml
* 13:25 Reception123: sudo -u www-data php /srv/mediawiki/w/maint*/mergeMessageFileList.php --output /srv/mediawiki/config/ExtensionMessageFiles.php --wiki test1wiki and and rebuild LC
* 01:21 paladox: applied custom hack in /srv/mediawiki/config for swift file backend on test1
* 01:15 paladox: /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/setZoneAccess.php in a screen on test1

## 2018-06-29 

* 21:51 MacFan4000: paladox stopped icinga
* 21:47 paladox: test
* 19:06 paladox: systemctl enable ircrcbot on misc1 so that ircrcbot service starts on boot
* 19:06 paladox: rebooted misc1

## 2018-06-28 

* 14:00 paladox: PURGE BINARY LOGS TO 'mysql-bin.000399'; PURGE BINARY LOGS TO 'mysql-bin.000400'; PURGE BINARY LOGS TO 'mysql-bin.000401'; PURGE BINARY LOGS TO 'mysql-bin.000402'; on db4
* 13:56 paladox: PURGE BINARY LOGS BEFORE DATE(NOW() - INTERVAL 1 DAY) + INTERVAL 0 SECOND; on db4
* 01:28 paladox: signing swift1.miraheze.org puppet key on puppet1

## 2018-06-27 

* 14:55 paladox: rm -rf /srv/mariadb on bacula1
* 14:55 paladox: removed mariadb from bacula1 as it kept crashing
* 14:44 paladox: upgrading mariadb on bacula1
* 14:40 paladox: upgrading phabricator
* 14:39 paladox: upgrading grafana to 5.2
* 05:36 Reception123: reception@mw2:/srv/mediawiki/w/maintenance$ sudo -u www-data php importDump.php --wiki jordepediawiki /home/reception/jorde_pages_full.xml

## 2018-06-26 

* 01:25 paladox: rebooting cp4 to clear ram
* 00:55 paladox: disabled [https://phabricator.miraheze.org/H34](https://phabricator.miraheze.org/H34)

## 2018-06-25 

* 20:25 MacFan4000: that is also in a screen
* 20:25 MacFan4000: running jobs on all wikis
* 20:00 paladox: apt-get --purge remove memcached on mw*
* 19:58 paladox: apt-get --purge remove memcached on mw1
* 19:20 paladox: repool mw1
* 19:18 paladox: depool mw1
* 19:18 paladox: reboot mw1
* 18:48 paladox: restarting php7.2-fpm and nginx on mw1
* 18:26 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki on mw3
* 18:25 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki on mw2
* 18:25 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki on mw1

## 2018-06-24 

* 22:33 paladox: reboot cp4 due to OOM
* 14:08 Reception123: manually run sudo -u www-data foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/maintenance/runJobs.php on mw1 to alleviate queue
* 14:07 Reception123: restarted mw2 jobrunner
* 12:39 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki on mw*
* 12:35 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki on mw3

## 2018-06-22 

* 17:00 MacFan4000: restarted mw3 JobRunner and running jobs on all wikis
* 15:54 MacFan4000: sudo -u www-data php rebuildLocalisationCache.php --wiki test1wiki on mw* and test1

## 2018-06-20 

* 18:08 paladox: installed openstack swift on nfs1 (will create a puppet class in the future to do this)

## 2018-06-19 

* 15:11 paladox: /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/maintenance/cleanupUsersWithNoId.php --prefix=m --assign on mw1
* 15:09 paladox: /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/maintenance/cleanupUsersWithNoId.php --prefix=m on mw1
* 15:05 paladox: /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/maintenance/cleanupUsersWithNoId.php --prefix=prefix on mw1
* 12:41 MacFan4000: test
* 12:41 paladox: reboot cp4
* 01:12 John: archived H29, will not work as intended

## 2018-06-18 

* 22:50 John: dropped extloadwiki
* 21:13 John: MariaDB [metawiki]> UPDATE cw_wikis SET wiki_category = "education" WHERE wiki_dbname LIKE "wright%";
* 19:26 paladox: clearing ram on cp4 by rebooting
* 16:20 Southparkfan: rebooting msic2
* 15:55 Southparkfan: @misc2:/sbin# mv init init2 && ln -s /lib/systemd/system init && systemctl daemon-reload
* 15:46 Southparkfan: removed redis-tools from misc2, reinstalled redis-server
* 15:38 paladox: fixing up misc2 seems to be using init.d services instead of systemd

## 2018-06-17 

* 20:53 paladox: /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/maintenance/sql.php /srv/mediawiki/w/extensions/PageTriage/sql/PageTriageTagsPatch.sql on test1 preperation change for mw 1.31
* 12:28 MacFan4000: macfan@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php importDump.php --wiki project772wiki /home/macfan/Wikipedia-20180616192948.xml in a screen

## 2018-06-16 

* 23:06 paladox: reboot cp4 to try and regain some memory

## 2018-06-15 

* 20:46 MacFan4000: stopped and restarted in screen
* 20:41 MacFan4000: test
* 16:40 paladox: rebooting test1 to see if that will bring down cpu usage.
* 16:17 paladox: upgrading redis on misc2 (package updates available)

## 2018-06-14 

* 20:54 paladox: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=wkupwiki --report=1 dump.xml on mw1 T3235
* 20:42 paladox: create paladox db (fake db to import and then export as a xml) on db4
* 17:26 paladox: /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/maintenance/sql.php /srv/mediawiki/w/extensions/Math/db/patches/mathoid.add_png.mysql.sql on test1 (preperations for mw 1.31)

## 2018-06-12 

* 18:40 paladox: upgrading php7.2 on test1
* 17:22 paladox: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=tapestrywiki --report=1 Wikipedia-20180612165309.xml on mw1

## 2018-06-11 

* 22:21 paladox: deleting uptimerobot account as moved to hund.io
* 18:23 John:  UPDATE cw_wikis SET wiki_inactive = 0 WHERE wiki_closed = 1;

## 2018-06-10 

* 23:48 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki on mw3
* 23:39 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki on mw2
* 23:27 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki on mw1
* 16:48 paladox: rebooting cp4 to free mem

## 2018-06-09 

* 23:23 paladox: upgrading phabricator
* 00:09 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki on test1

## 2018-06-08 

* 21:11 Southparkfan: disable mw1 puppet
* 20:34 Southparkfan: disregard previous action
* 20:33 Southparkfan: disable puppet on mw1
* 18:45 Reception123: > UPDATE cw_wikis SET wiki_closed = '0' WHERE wiki_dbname = 'domusaureawiki'
* 17:00 paladox: running  sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildall.php --wiki=nonsensopediawiki on mw2
* 01:14 paladox: restarting sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=nonsensopediawiki --report=1 nonsensopedia_pages_full.xml on mw2 in screen

## 2018-06-07 

* 23:12 paladox: restarting sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=nonsensopediawiki --report=1 nonsensopedia_pages_full.xml on mw2 in screen
* 22:51 John: further purged from last 24 hours
* 22:48 John: as an fyi ~40G gained back on db4
* 22:48 John: removed binlogs before June 4th
* 20:14 MacFan4000: macfan@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php rebuildrecentchanges.php --wiki wikinationswiki
* 20:13 MacFan4000: macfan@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php initSiteStats.php --wiki wikinationswiki --update
* 18:58 paladox: restarted varnish on cp4 to get puppet running
* 18:17 MacFan4000: running manageInactiveWikis.php on test1
* 17:55 MacFan4000: macfan@test1:/srv/mediawiki/w/maintenance$ sudo -u www-data php rebuildLocalisationCache.php --wiki test1wiki
* 15:26 John: running manageInactiveWikis.php
* 15:04 MacFan4000: stopped and restarted in a screen
* 14:58 MacFan4000: macfan@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php importDump.php --wiki wikinationswiki /home/macfan/carrington_pages_current.xml

## 2018-06-06 

* 22:52 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki on mw3
* 22:43 paladox: repool mw3
* 22:29 paladox: depool mw3
* 22:28 paladox: repool mw2
* 22:28 paladox: depool mw2
* 22:28 paladox: repool mw2
* 22:27 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki on mw2
* 22:24 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki on mw1
* 22:13 paladox: depool mw2
* 22:13 paladox: repool mw1
* 21:52 paladox: depooling mw1
* 21:47 paladox: re cloning mediawiki on mw* to fix a submodule
* 20:48 paladox: stopping script as it needs to be run only once!
* 20:21 paladox: running /usr/local/bin/foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/extensions/CentralAuth/maintenance/resetGlobalUserTokens.php on mw1
* 15:40 paladox:  restarting sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=nonsensopediawiki --report=1 nonsensopedia_pages_full.xml on mw2 in screen

## 2018-06-05 

* 22:30 paladox: test
* 20:56 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki on mw[23]
* 20:17 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki on mw1
* 18:46 paladox: fixing mw* starting with mw1 for T3204
* 01:03 paladox: restarted sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=nonsensopediawiki --report=1 --file=/home/revi/nonsensopedia_pages_full.xml on mw2 (as mw2 was close to using all of it's ram)

## 2018-06-04 

* 23:15 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki on test1
* 21:46 MacFan4000: macfan@mw1:~$ sudo -u www-data cp -R /srv/mediawiki/w/extensions/SocialProfile/avatars /srv/mediawiki/w/extensions/SocialProfile/awards /mnt/mediawiki-static/popnmusicwiki
* 21:13 MacFan4000: macfan@test1:/srv/mediawiki/w/maintenance$ sudo -u www-data php rebuildLocalisationCache.php --wiki test1wiki
* 20:57 paladox: upgrading test1wiki to 1.31
* 13:55 paladox: reboot cp2 to clean ram
* 13:35 paladox: reboot cp4 to clean mem

## 2018-06-03 

* 23:10 paladox: install SecurityInfo on piwik
* 19:59 paladox: restarting  sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=nonsensopediawiki --report=1 nonsensopedia_pages_full.xml on mw2 in screen
* 10:39 Reception123: reception@mw1:/srv/mediawiki/w/extensions/MirahezeMagic/maintenance$ sudo -u www-data php manageInactiveWikis.php --wiki metawiki --warn --close

## 2018-06-02 

* 22:40 MacFan4000: macfan@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php initSiteStats.php --wiki pirategalaxywiki --update
* 22:02 MacFan4000: macfan@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php importDump.php --wiki pirategalaxywiki /home/macfan/pirategalax_pages_full.xml

## 2018-06-01 

* 23:40 paladox: rm -rf amaninfowiki/thumb/6/6a/Camera.jpg on nfs1
* 23:35 paladox: varnish> ban req.http.Host == static.miraheze.org && req.url ~ "^/amaninfowiki/6/6a/Camera.jpg" on cp*
* 23:33 paladox: varnish> ban req.http.Host == aman.info.tm && req.url ~ "^/w/load.php" on cp*
* 23:30 paladox: rm -rf /srv/mediawiki-static/amaninfowiki/6/6a/Camera.jpg on nfs1
* 17:53 paladox: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=nonsensopediawiki --report=1 nonsensopedia_pages_full.xml on mw2 in screen
* 11:50 paladox: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=nonsensopediawiki --report=1 nonsensopedia_pages_full.xml on mw2 in screen

## 2018-05-31 

* 23:49 MacFan4000: sudo -u www-data php rebuildLocalisationCache.php --wiki test1wiki on mw* and test1
* 22:12 paladox: sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=nonsensopediawiki --report=1 nonsensopedia_pages_full.xml on mw2 in a screen
* 17:57 revi: restarted nonsensopedia import
* 15:06 paladox: composer require geoip2/geoip2 on mw* and also install [http://geolite.maxmind.com/download/geoip/database/GeoLite2-City.tar.gz](http://geolite.maxmind.com/download/geoip/database/GeoLite2-City.tar.gz) in /srv/
* 12:27 revi: revi@mw2:~$ `sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=nonsensopediawiki --report=1 nonsensopedia_pages_full.xml` again
* 12:24 revi: did `sudo -u www-data php /srv/mediawiki/w/maintenance/runJobs.php --wiki=nonsensopediawiki` on mw2
* 12:15 revi: `sudo service jobrunner restart` on mw2 and mw3
* 00:09 paladox: restart apache on puppet1
* 00:09 paladox: restart puppetdb on puppet1

## 2018-05-30 

* 23:16 Southparkfan: installing mariadb-backup-10.2 on bacula1
* 22:11 revi: revi@mw2:~$ `sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=nonsensopediawiki --report=1 nonsensopedia_pages_full.xml`
* 21:22 paladox: sudo -u www-data php deleteBatch.php --wiki pokemondustwiki -r "Per request via email" -i /home/macfan/delete.list.txt mw1
* 21:09 paladox: composer install under OAuth ext on mw*
* 18:30 paladox: sudo chown -R www-data:www-data /srv/mediawiki-static/pirategalaxywiki/avatars/
* 18:29 paladox: mkdir /srv/mediawiki-static/pirategalaxywiki/avatars/
* 18:29 paladox: sudo chown -R www-data:www-data /srv/mediawiki-static/pirategalaxywiki/
* 18:29 paladox: mkdir /srv/mediawiki-static/pirategalaxywiki/
* 15:35 Southparkfan: another attempt to import db4->bacula1 repl

## 2018-05-29 

* 23:22 paladox: upgrading git on all servers "salt -E ".*" cmd.run "apt-get -t stretch-backports install git -y"" per [https://phabricator.miraheze.org/T3162](https://phabricator.miraheze.org/T3162)
* 21:53 Southparkfan: another attempt to import db4 on bacula1
* 17:46 Southparkfan: deleted redis keys "*:translate-groups*" "*:gadgets-definition*" "*:flow*" " "*:LESS*"  "*:template*" "*:file*"  "*:textextracts*" "*:revision*" "*:page*"
* 17:35 Southparkfan: deleted redis keys matching patterns "*:resourceloader*", "*:MessageBlobStore*"
* 17:21 Southparkfan: deleted redis keys matching patterns "*:diff:version:*", "*:filerepo:*"
* 17:18 Southparkfan: restarted salt-minion on mw1
* 14:32 paladox: disabling puppet on mw1 and misc1 to test some ssl changes (auto renewing ssl tests)
* 11:02 paladox: restarted jobchron and jobrunner on mw 2 and mw3
* 01:28 John: eventually moved wgFavicon to ManageWiki

## 2018-05-28 

* 23:11 John: cleared /backup/ on db4
* 22:49 Southparkfan: installed package 'pv' on bacula1
* 21:02 paladox: apt-get -t stretch-backports install redis-server on misc2
* 20:31 paladox: stopping mysql on db4 pending db update
* 20:12 paladox: install python3-mwclient on misc1
* 17:53 John: restart jobchron and jobrunner on mw2 and mw3
* 17:49 MacFan4000: running jobs manually on nltramswiki
* 17:39 MacFan4000: macfan@mw3:/srv/mediawiki/w/maintenance$ sudo -u www-data php runJobs.php --wiki test1wiki
* 17:36 MacFan4000: restarted JobRunner on mw3
* 17:21 Southparkfan: running mysqldump --skip-lock-tables --single-transaction --flush-logs --master-data=2 --all-databases | pigz | ssh -i /home/dbcopy/dbcopy/id_rsa dbcopy@bacula1.miraheze.org 'cat > /home/dbcopy/db4.sql.gz'
* 16:51 Southparkfan: same for expire-logs-days
* 16:50 Southparkfan: set db4's server_id dynamically (to avoid mysql restart)
* 10:48 paladox: restarted jobrunner and jobcron on mw[23]
* 02:00 paladox: running sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki test1
* 02:00 paladox: running sudo -u www-data php /srv/mediawiki/w/maint*/mergeMessageFileList.php --output /srv/mediawiki/config/ExtensionMessageFiles.php --wiki test1wiki test1
* 01:55 MacFan4000: macfan@test1:/srv/mediawiki/w/maintenance$ sudo -u www-data php rebuildLocalisationCache.php --wiki test1wiki
* 00:08 MacFan4000: paladox unlocked policy for some spammy phab tasks

## 2018-05-27 

* 21:22 revi: revi@mw3:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildrecentchanges.php --wiki=anglishwiki
* 21:21 revi: revi@mw3:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/initSiteStats.php --wiki=anglishwiki
* 14:50 revi: revi@mw3:~$ `sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=anglishwiki --report=1 anglish_pages_full.xml`
* 13:54 revi: halted previous operation
* 12:33 revi: revi@mw3:~$ `sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=anglishwiki --report=50 anglish_pages_full.xml `

## 2018-05-26 

* 18:14 revi: revi@mw1:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/initSiteStats.php --wiki=metawiki
* 18:13 revi: revi@mw1:~$ sudo -u www-data php /srv/mediawiki/w/maintenance/rebuildrecentchanges.php --wiki=metawiki
* 18:07 revi: `sudo -u www-data php /srv/mediawiki/w/maintenance/importDump.php --wiki=metawiki Meta-20180526175920.xml`
* 17:10 paladox: updating piwik to use geoip2 as geoip is now discontinued ([https://matomo.org/faq/how-to/#faq_163](https://matomo.org/faq/how-to/#faq_163))
* 15:40 paladox: cleaning ram on misc3
* 15:38 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki mw3
* 15:38 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/mergeMessageFileList.php --output /srv/mediawiki/config/ExtensionMessageFiles.php --wiki test1wiki mw3
* 15:27 paladox: depool mw3
* 15:25 paladox: repool mw2
* 15:24 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki mw2
* 15:24 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/mergeMessageFileList.php --output /srv/mediawiki/config/ExtensionMessageFiles.php --wiki test1wiki mw2
* 15:08 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki on mw1
* 15:08 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/mergeMessageFileList.php --output /srv/mediawiki/config/ExtensionMessageFiles.php --wiki test1wiki on mw1
* 15:04 paladox: depool mw2
* 15:04 paladox: repool mw1
* 14:36 paladox: depool mw1

## 2018-05-25 

* 20:49 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki on mw*
* 17:55 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki on mw*
* 17:55 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/mergeMessageFileList.php --output /srv/mediawiki/config/ExtensionMessageFiles.php --wiki test1wiki on mw*
* 17:54 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki on test1
* 17:54 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/mergeMessageFileList.php --output /srv/mediawiki/config/ExtensionMessageFiles.php --wiki test1wiki on test1
* 16:52 John: moved wiki.ciptimedia.org backups from nfs1->bacula1

## 2018-05-24 

* 22:08 paladox: updating matomo (piwik) to 3.5.0
* 11:43 MacFan4000: sudo -u www-data cp -R /srv/mediawiki/w/extensions/SocialProfile/avatars /srv/mediawiki/w/extensions/SocialProfile/awards /mnt/mediawiki-static/credcowiki
* 01:55 John: added MirahezeSSLBot as a collaborator to miraheze/ssl
* 00:35 MacFan4000: CORRECTION: on puppet1
* 00:32 MacFan4000: ... on ns1*
* 00:31 paladox: clean up /var/lib/puppet/reports/ (was 28gb)

## 2018-05-23 

* 19:48 MacFan4000: macfan@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php importDump.php --wiki lexwikiwiki /home/macfan/lexwiki_23-05-2018.xml

## 2018-05-22 

* 17:39 paladox: upgrade phabricator
* 16:25 John: delete "app" repo (fork of all of Wikias code)
* 16:13 paladox: manually updating prometheus-varnish-exporter on cp* following [https://github.com/jonnenauha/prometheus_varnish_exporter/issues/29#issuecomment-391045216](https://github.com/jonnenauha/prometheus_varnish_exporter/issues/29#issuecomment-391045216)
* 15:55 paladox: rm -rf /var/lib/ganglia*
* 15:53 paladox: removing ganglia from misc2
* 15:41 MacFan4000: paladox and I invited all other ops as admins
* 15:41 paladox: <+MacFan4000>	!log created admin account for me using the account "admin"
* 14:48 John: running estimates on bacula1 for all existing jobs to maximise disk usage as we currently backup more than we physically can
* 14:48 John: DB3 pool on bacula1 as well
* 14:46 John: deleting DB pool on bacula1
* 14:31 revi: updated form 7 [https://meta.miraheze.org/w/index.php?title=Tech:Phabricator/Form/Maniphest/7&diff=47923&oldid=47922](https://meta.miraheze.org/w/index.php?title=Tech:Phabricator/Form/Maniphest/7&diff=47923&oldid=47922)
* 11:35 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki on test1
* 02:21 paladox: running sudo -u www-data php rebuildLocalisationCache.php --wiki test1wiki and sudo -u www-data php mergeMessageFileList.php --output /srv/mediawiki/config/ExtensionMessageFiles.php --wiki test1wiki on mw*
* 02:17 John: running manageInactiveWikis.php

## 2018-05-21 

* 23:19 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki mw*
* 23:19 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki on mw1
* 22:33 paladox: running sudo -u www-data php rebuildLocalisationCache.php --wiki test1wiki on test1
* 22:11 paladox: removing puppet from db2 following steps at [https://meta.miraheze.org/wiki/Tech:Puppet#Removing_puppet_agent_.28server.29_on_the_Puppetmaster](https://meta.miraheze.org/wiki/Tech:Puppet#Removing_puppet_agent_.28server.29_on_the_Puppetmaster)
* 15:33 paladox: migrating cp5 from 20gb to 25gb
* 01:12 Southparkfan: reversed previous ufw change
* 00:53 Southparkfan: allow cp4.miraheze.org:9131 (ufw) from misc2
* 00:28 Southparkfan: trying to reset grafana password

## 2018-05-20 

* 21:25 paladox: apt upgrade lilypond lilypond-data on mw*

## 2018-05-19 

* 21:09 paladox: upgrade phabricator

## 2018-05-17 

* 18:39 revi: Labster `Added repositories to the Travis CI integration.` in GitHub

## 2018-05-15 

* 21:43 John: made 1 security task (not security) public
* 21:43 paladox: sudo -u www-data php rebuildLocalisationCache.php --wiki test1wiki on test1
* 20:29 paladox: sudo -u www-data php rebuildLocalisationCache.php --wiki test1wiki on mw*
* 17:04 paladox: rebooted misc3 to relive memory presure
* 15:05 paladox: restarted misc3 to clear the ram
* 14:03 John: scratch that
* 13:58 John: moving ciptimedia.org data to bacula1 from nfs1
* 13:45 John: removed old dumps from nfs1
* 12:32 John: includes reinstall to Deb9, no puppet association, will be a loan server
* 12:31 John: claiming db3 as mine for testing pot. new service in a non prod environment
* 11:08 paladox: rebooting cp2 (to see if that fixes "CRITICAL - 1 datacenter is down: 2604:180:0:33b::2/cpweb")
* 05:14 Reception123: sudo service icingabot restart
* 00:16 paladox: systemctl mask mysql on db2

## 2018-05-14 

* 23:58 paladox: rebooted test1
* 23:44 MacFan4000: sudo -u www-data php rebuildLocalisationCache.php --wiki test1wiki on mw*
* 23:36 John: looping INSERT INTO cw_comments ( cw_id, cw_comment, cw_comment_timestamp, cw_comment_user ) SELECT cw_id, cw_status_comment, cw_status_comment_timestamp, cw_status_comment_user FROM cw_requests WHERE cw_id = $id; between all missing IDs to find troublesome ID
* 23:29 paladox: upgrading debian on db2 to latest jessie point release
* 23:29 John: MariaDB [metawiki]> UPDATE cw_requests SET cw_status_comment = 'empty' WHERE cw_status_comment = '';
* 23:28 paladox: stopped mysql on db2
* 22:57 paladox: switching wikis from db2 to db4 [https://git.io/vpQyD](https://git.io/vpQyD)
* 21:50 paladox: restoring db backups to db4 dbBackup.sh
* 21:11 paladox: starting db2 -> db4 migration
* 20:47 John: trained SA with my junk inbox
* 19:18 paladox: delete db extloadwiki and loginwiki and testwiki on db2 as they were migrated to db4
* 16:06 paladox: reboot misc3 to see if it will reclaim ram
* 15:29 paladox: delete db airwiki aistudywiki aiswiki aklassewiki aktposwiki alacritysimwiki alaexploitdbwiki alberhillwiki albionwebwiki albustestwiki alewiki alfrescowiki algopediawiki alifloktawiki alittletroutywiki allsamemonsterswiki allthingswikiwiki almanachdebauswicwiki altenpflegewiki alternatehistorywiki alternatesporthistorywiki alterwikiwiki althistoriawiki altruniversewiki altversewiki alwikiwiki amaninfowiki ambirtestwiki amcdlwiki ameciclowiki amicitiawiki amicsdesmuseucawiki amicsdesmuseuwiki amirampwiki amntwiki amxwikiwiki analogypediawiki anchorhrgwiki andreasalexanderulrichwiki animangamespnpwiki from db2 (was migrated to db4)
* 14:56 paladox: delete db afictionalworldonawiki, africavisionwiki, afrwiki, afterworldwiki, ag7732wiki, agathachristiewiki, agathinonwiki, ageloniawiki, ageofenlightenmentwiki, ageofwushuwiki, agriwikiwiki, agropediawiki, ahabariwiki, ahdwiki, ahmsaqibwiki, aibowiki, aidorupediawiki, aidyllicwiki, aimciawiki, airportsofwings900wiki from db2 (was migrated to db4)
* 13:58 paladox: delete db activistresourceswiki, adadevelopersacademywiki, adamwiki, adantewiki, addicteddadswiki, adiaprojectwiki, adminbookclubwiki, adminbuswiki, adnovumwiki, advantagewiki, advisingwiki, aemanualwiki, aenasanwiki, aeromwiki, aerossprimewiki, aerowikiwiki, aesbasewiki, aescapeswiki, aetheriawiki from db2 (was migrated to db4)
* 13:46 paladox: delete db adiapediawiki on db2 and db4 (was renamed to elerawiki) [https://phabricator.miraheze.org/rMWCFe41b685975cabaed803b42452dee5cfc7150d020](https://phabricator.miraheze.org/rMWCFe41b685975cabaed803b42452dee5cfc7150d020)
* 12:51 paladox: delete db 8stationwiki, 99pdwikiwiki, a360wiki, aapwiki, aaupaftlocal6075wiki, abainnovationwiki, abhirupghoshwiki, abitaregeawiki, absurdopediawiki, abundancewiki, abzewiki, acasrbijawiki, accademiadellebirrewiki, access7wiki, accorderiewiki, accountingwiki, acewikiwiki, achancetopursuewiki, actartletraswiki from db2 was migrated to db4 a few days ago and no issues reported
* 12:41 paladox: delete db 690squadronwiki from db2 was migrated to db4 a few days ago and no issues reported
* 12:41 paladox: delete db 4mindswiki from db2 was migrated to db4 a few days ago and no issues reported
* 12:41 paladox: delete db 3dprinterscncwiki from db2 was migrated to db4 a few days ago and no issues reported
* 12:40 paladox: delete db 2cvcupfrancewiki from db2 was migrated to db4 a few days ago and no issues reported
* 12:40 paladox: delete db 1sttractionbrigadewiki from db2 was migrated to db4 a few days ago and no issues reported
* 12:39 paladox: delete db 1cewiki from db2 was migrated to db4 a few days ago and no issues reported
* 12:38 paladox: delete db 161647y2awiki from db2 was migrated to db4 a few days ago and no issues reported
* 12:37 paladox: delete db 131parkhurstwiki from db2 was migrated to db4 a few days ago and no issues reported
* 12:36 paladox: delete db 0x1winwiki from db2 was migrated to db4 a few days ago and no issues reported
* 12:20 paladox: PURGE BINARY LOGS BEFORE '2018-05-14 13:20:26'; on db2
* 00:08 MacFan4000: macfan@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php dumpBackup.php --wiki podpediawiki --full  > /home/macfan/podpedia.xml

## 2018-05-13 

* 08:04 Reception123: sudo -u www-data php dumpBackup.php --current --wiki atlantisboardwiki > /home/reception/atlantisboardwiki13052018.xml on mw3

## 2018-05-12 

* 22:41 paladox: upgrade phabricator
* 21:18 paladox: sudo -u www-data php rebuildLocalisationCache.php --wiki test1wiki on mw* and test1
* 19:04 paladox: rebooted cp4 to try and gain more ram
* 15:00 Reception123: sudo -u www-data php rebuildLocalisationCache.php --wiki test1wiki on mw*
* 12:44 paladox: sudo -u www-data php rebuildLocalisationCache.php --wiki test1wiki on mw*
* 12:40 paladox: sudo -u www-data php rebuildLocalisationCache.php --wiki test1wiki on test1
* 11:24 John: MariaDB [metawiki]> UPDATE cw_wikis SET wiki_extensions=CONCAT(wiki_extensions,',zzzz');
* 01:37 PuppyKun: force changed passwd for ndkilla@misc1
* 00:49 paladox: puppet disabled on mw1 and mw2 by JohnLewis.

## 2018-05-11 

* 23:21 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki on test1`
* 22:56 John: fixed stylings of wiki_extension entries using MySQL replace()
* 22:29 John: populated wiki_extensions with transferred extensions data
* 22:04 paladox: restarted parsoid after icinga message
* 21:37 paladox: manually installed python-diamond and diamond debs on db2 and db3 as it's only in stretch dist. We are migrating to db4 which is stretch so this is not a problem.
* 21:29 paladox: rolling python-diamond to all hosts using salt -E ".*" cmd.run "puppet agent -tv"

## 2018-05-10 

* 19:54 paladox: upgrading php on test1 to php7.2
* 15:08 paladox: dbBackup.sh on db4 restoring backups
* 15:07 paladox: dbMigration.sh on db2 (mgirating dbs to db4)
* 13:45 paladox: rm -rf /srv/backup-root-mw1
* 13:44 paladox: rm -rf /srv/backup-root-misc1
* 13:43 paladox: rm -rf /srv/backup-home-mw1 (it was backed up to mw1)
* 13:41 paladox: rm -rf /srv/backup-home-misc1
* 13:40 paladox: deleted db backups on db4 in /home/dbcopy (have been working successfully for over a week)
* 09:36 paladox: sudo -u www-data php rebuildLocalisationCache.php --wiki test1wiki on mw* and test1*
* 01:13 paladox: composer install in /srv/mediawiki/w and /srv/mediawiki/w/extensions/Wikibase and /srv/mediawiki/w/extensions/Flow
* 00:11 paladox: sudo -u www-data php rebuildLocalisationCache.php --wiki test1wiki on test1

## 2018-05-09 

* 23:51 MacFan4000: sudo -u www-data php rebuildLocalisationCache.php --wiki test1wiki on test1 earlier than when paladox did it
* 23:48 paladox: sudo -u www-data php rebuildLocalisationCache.php --wiki test1wiki on test1
* 23:38 MacFan4000: sudo -u www-data php update.php --wiki test1wiki --force on test1
* 23:13 MacFan4000: php createLocalAccount.php --wiki testwiki --username NDKilla (going to assign rights on testwiki)
* 22:03 MacFan4000: composer update on test1
* 21:59 paladox: upgrading test1wiki to mediawiki 1.31 for testing
* 21:46 MacFan4000: php createLocalAccount.php --wiki testwiki --username Example5
* 21:46 MacFan4000: php createLocalAccount.php --wiki testwiki --username Example4
* 21:41 MacFan4000: php createLocalAccount.php --wiki testwiki --username Example3
* 18:14 paladox: upgraded phabricator

## 2018-05-08 

* 21:15 paladox: test
* 18:26 paladox: sudo -u www-data php rebuildLocalisationCache.php --wiki test1wiki on mw*
* 13:57 John: converting all RequestWiki comments from old table to new table, will be a while!
* 13:45 John: INSERT INTO cw_comments ( cw_id, cw_comment, cw_comment_timestamp, cw_comment_user ) SELECT cw_id, cw_status_comment, cw_status_comment_timestamp, cw_status_comment_user FROM cw_requests WHERE cw_id = 1; (request building from John here, logging because this is going to be ran a couple thousand times probably)
* 13:42 John: created cw_comments on metawiki

## 2018-05-07 

* 21:48 paladox: delete test3wiki from db2 and also delete wiki following [https://meta.miraheze.org/wiki/Tech:Delete_a_wiki](https://meta.miraheze.org/wiki/Tech:Delete_a_wiki)
* 21:46 paladox: deleted test2wiki from db2
* 18:00 MacFan4000: adminbot was restarted on misc1
* 01:48 PuppyKun: misc1: service icingabot restart

## 2018-05-05 

* 16:40 MacFan4000: sudo -u www-data cp -R /srv/mediawiki/w/extensions/SocialProfile/avatars /srv/mediawiki/w/extensions/SocialProfile/awards /mnt/mediawiki-static/test1wiki
* 14:21 MacFan4000: sudo -u www-data php rebuildLocalisationCache.php --wiki test1wiki on test1
* 12:51 MacFan4000: sudo -u www-data php rebuildLocalisationCache.php --wiki test1wiki on mw*

## 2018-05-04 

* 22:36 paladox: upgraded phabricator
* 00:39 MacFan4000: sudo -u www-data php rebuildLocalisationCache.php --wiki test1wiki on mw*
* 00:15 paladox: repool mw2
* 00:03 paladox: repool mw1

## 2018-05-03 

* 23:52 paladox: depool mw1
* 23:51 paladox: repool mw3
* 23:36 paladox: depool mw3
* 23:35 paladox: repool mw2
* 23:27 paladox: depool mw2
* 23:26 paladox: repool mw1
* 23:18 paladox: depool mw1
* 20:05 paladox:  sudo -u www-data php rebuildLocalisationCache.php --wiki test1wiki on mw*
* 17:31 Reception123: dropped newmanwiki and argpwiki T2886 T2960
* 17:28 Reception123: > DELETE FROM cw_wikis WHERE wiki_dbname = 'newmanwiki';
* 17:28 Reception123: > DELETE FROM cw_wikis WHERE wiki_dbname = 'argpwiki';
* 11:21 Reception123: sudo -u www-data php dumpBackup.php --current --wiki allthetropeswiki > /home/reception/allthetropeswiki03052018.xml on mw3
* 07:26 Reception123: sudo -u www-data php rebuildLocalisationCache.php --wiki test1wiki on mw*
* 00:07 MacFan4000: sudo -u www-data php rebuildLocalisationCache.php --wiki test1wiki on test1

## 2018-05-02 

* 20:53 paladox:  sudo -u www-data php rebuildLocalisationCache.php --wiki test1wiki on mw*
* 10:33 Reception123: sudo -u www-data php rebuildLocalisationCache.php --wiki test1wiki
* 07:34 Reception123: sudo -u www-data php refreshLinks.php --wiki allthetropeswiki on mw1

## 2018-05-01 

* 19:40 paladox: reinstalling misc3 (sudo is not working)
* 14:55 paladox: clean logs on cp*

## 2018-04-30 

* 16:22 paladox: reboot db3
* 16:19 paladox: upgraded db3 to latest jessie point release (made sure it had no stretch dist)
* 16:18 paladox: removed mysql db3 service from icinga manually
* 15:49 paladox: sudo service mysql stop on db3
* 14:30 paladox: delete db backups on db4 /home/dbcopy (no reports of wikis braking)
* 12:09 paladox: apt-get install python-pip on  misc3 (i will puppitise this later)

## 2018-04-29 

* 23:25 paladox:  sudo -u www-data php rebuildLocalisationCache.php --wiki test1wiki on mw*
* 22:41 paladox:  sudo -u www-data php rebuildLocalisationCache.php --wiki test1wiki on test1wiki

## 2018-04-28 

* 23:31 paladox: restarted puppetdb on puppet1 for config change

## 2018-04-27 

* 19:50 MacFan4000: macfan@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php importDump.php --wiki podpediawiki /home/macfan/Wikipedia-20180202192828.xml
* 19:44 MacFan4000: macfan@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php importDump.php --wiki podpediawiki /home/macfan/roosterteeth_pages_current.xml
* 18:07 paladox: clean up logs in /var/log/** on cp5
* 16:14 paladox:  sudo chown -R www-data:www-data ../repos on misc1 (/srv/phab/repos)
* 16:12 paladox: upgrade phabricator
* 13:38 Reception123: reception@mw3:/srv/mediawiki/w/maintenance$ sudo -u www-data php importDump.php --wiki testwiki /home/reception/backups4/home/reception/wikibackups/testwiki.xml
* 12:33 Reception123: DROP DATABASE testwiki; (re-importing)
* 12:33 Reception123: DELETE FROM cw_wikis WHERE wiki_dbname = 'testwiki'; (re-importing)
* 12:31 Reception123: sudo -u www-data php dumpBackup.php --wiki testwiki --full --uploads > /home/reception/testwiki_feb.xml on mw3
* 11:53 Southparkfan: chmod 777 /tmp on bacula1
* 10:30 Southparkfan: installed percona-xtrabackup-24_2.4.11-1.stretch_amd64.deb on db4
* 00:14 PuppyKun: freed up ~5.6 GB on mw1

## 2018-04-26 

* 23:57 PuppyKun: wget february testwiki xml dumps to mw1 / import
* 22:29 paladox: delete db testwiki from db4
* 22:29 paladox: /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/removeDeletedWikis.php --wiki testwiki on mw1
* 22:28 paladox: DELETE FROM cw_wikis WHERE wiki_dbname = "testwiki"; on db2
* 22:20 paladox: delete networksdatabasewiki nextlevelwikiwiki nonbinarywiki nvcwiki omnipediawiki ordiswiki ourmxfestwiki plasticssongcontestwiki platprojectwiki pluspiwiki pocketmonsterswiki podpediawiki r2wiki recentiawiki revitwiki scruffy2wiki sdiywiki sentrieswiki sidemwiki sirikotwiki songcontestswiki speleowiki spiralwiki spritopiawiki summerolympicswiki sumroletaericwiki templatewik teriawiki from db3
* 22:18 paladox: delete omnipediawiki from db3 and db4
* 22:18 paladox: delete saganbackup from db3 and db4
* 21:37 paladox: drop db testdeletewiki from db2 (is on db4 now)
* 20:24 paladox: rm *.sql in /home/dbcopy on db4. Everything is working fine!
* 20:12 paladox: delete db centralauth and loginwiki from db3 (it's now on db4)
* 17:40 Reception123: re-created reception user on icinga (again)
* 17:31 paladox: delete testdeletewiki and thegreatwarwiki and thelonsdalebattalionwiki and tiandiwiki and truecapitalistwiki and ubrwikiwiki and uncyclopediawiki and unionwiki and ussewiki and utamacrosswiki and valentinaprojectwiki and viagroupiawiki and whentheycrywiki and wiki1776wiki and wikiversitywiki and wikivywikiand worldpediawiki and ylscwiki and yoavfreundwiki and yourosongcontestwiki and zendariwiki and zhdelwiki from db3 (they are now on db4)
* 17:16 Reception123: removed labster and imbophil from Phabricator Security group
* 17:12 Reception123: removed ImBoPhil from @miraheze org
* 16:23 paladox: deleting testdelete1wiki from db3 (wiki does not exist anymore)
* 16:17 paladox: drop puppet from db3 (not needed anymore since we went with puppetdb)
* 16:11 paladox: delete ciudadciclistawiki and constwiki and cpiwiki from db3 (it's on db4 now)
* 16:09 paladox: delete christianmusictempwiki from db3 (it's on db4 now)
* 16:09 paladox: delete christianmusicwiki from db3 (it's on db4 now)
* 16:08 paladox: delete calexitwiki from db3 (it's on db4 now)
* 16:08 paladox: delete bqwiki from db3 (it's on db4 now)
* 16:07 paladox: delete bgowiki from db3 (it's on db4 now)
* 16:07 paladox: delete beatstationwiki from db3 (it's on db4 now)
* 16:07 paladox: delete ballaratpubswiki from db3 (it's on db4 now)
* 16:06 paladox: delete ayrshirewiki from db3 (it's on db4 now)
* 16:06 paladox: delete arefepvawiki from db3 (it's on db4 now)
* 16:05 paladox: delete altaussieruleswiki from db3 (it's on db4 now)
* 16:05 paladox: delete aleenghawiki from db3 (it's on db4 now)
* 11:04 Reception123: moved cargodb from db3 to db4 and dropped on db3
* 10:17 John: restarted phd

## 2018-04-25 

* 22:56 paladox: reboot misc1 to free up memory
* 22:33 paladox: added some manual patches to /usr/share/php/Icinga/** for php7.2 ([https://github.com/Icinga/icingaweb2/commit/5d100779ce8557095e0cfe1768780086b5865adf](https://github.com/Icinga/icingaweb2/commit/5d100779ce8557095e0cfe1768780086b5865adf) and [https://github.com/Icinga/icingaweb2/commit/72ec132f25c868d9510e6d36a2d5c92fc8dd59d1](https://github.com/Icinga/icingaweb2/commit/72ec132f25c868d9510e6d36a2d5c92fc8dd59d1))
* 20:24 paladox: re enabling puppet on misc1 to upgrade to icinga2
* 20:19 paladox: disabling puppet on misc1 in preperation for icinga1 -> icinga2 migration
* 16:31 paladox: upgraded phabricator
* 15:45 Reception123: re-create my mail account as reception123 (deleted with the reinstall)
* 11:20 Reception123: sudo -u www-data php importDump.php --wiki conworldwiki /home/reception/conworld_pages_current.xml on mw3
* 00:06 paladox: composer install on mw*

## 2018-04-24 

* 21:42 John: ensured all rDNS is correct for servers
* 14:17 paladox:  sudo -u www-data php rebuildLocalisationCache.php --wiki test1wiki on mw* and test1
* 08:51 Reception123: UPDATE cw_wikis SET wiki_language = 'no' WHERE wiki_dbname = 'ecypewiki'; (issue with ManageWiki_)
* 05:37 Reception123: sudo -u www-data php dumpBackup.php --wiki safiriawiki --full --uploads > /home/reception/safiriawiki240402018.xml on mw2

## 2018-04-23 

* 22:17 paladox: sudo -u www-data php /srv/mediawiki/w/maint*/rebuildLocalisationCache.php --wiki test1wiki on mw* and test1
* 07:49 Reception123: sudo -u www-data php rebuildLocalisationCache.php --wiki test1wiki on mw*

## 2018-04-21 

* 19:03 paladox:  sudo -u www-data php rebuildLocalisationCache.php --wiki test1wiki on mw*
* 17:22 paladox: drop phabricator db from db3
* 17:01 paladox: delete database conworldwiki on db3, it's on db4

## 2018-04-20 

* 22:02 paladox: ran drop database poserdazfreebieswiki; on db3
* 21:36 paladox: rm piwik.sql on db4
* 21:34 paladox: drop database testwiki on db3, it's on db4
* 21:31 paladox: drop database piwik from db3, it's now on db4.
* 21:03 paladox: deleted conworldwiki.sql backup from db4
* 21:01 paladox: sudo service apache2 stop on misc2 for migration of piwik to db4
* 19:44 paladox: rm -rf /srv/mediawiki-static/unionnorteamericanawiki on nfs1
* 19:43 paladox: ran DROP DATABASE unionnorteamericanawiki; on db3
* 19:42 paladox: ran /srv/mediawiki/w/extensions/MirahezeMagic/maintenance/removeDeletedWikis.php --wiki unionnorteamericanawiki on mw1
* 19:41 paladox: ran DELETE FROM cw_wikis WHERE wiki_dbname = "unionnorteamericanawiki"; on db2
* 19:12 paladox: drop database conworldwiki from db2 after being migrated to db4
* 19:01 paladox: removed backup backup.sql.gz from db4
* 19:00 paladox: remove backups ciptamediawiki.sql and  buswiki.sql and bpwiki.sql and jawp2chwiki.sql from db4.
* 19:00 Reception123: upgraded phabricator

## 2018-04-19 

* 18:13 paladox: delete db bpwiki on db3 after migration to db4
* 18:13 paladox: delete db buswiki on db3 after migration to db4.
* 18:12 paladox: delete db ciptamediawiki on db3 after migration to db4
* 18:12 paladox: delete db jawp2chwiki on db3 after migration to db4
* 17:38 paladox: backing up bpwiki buswiki ciptamediawiki jawp2chwiki from db3 to db4 then will migrate to db4.

## 2018-04-18 

* 23:28 paladox: deleting backup-srv-nfs1 on db4 to clear space up
* 22:38 paladox: migrating test1wiki to db4
* 19:19 paladox: reboot cp2
* 18:48 paladox: upgrading php on test1 to php7.2
* 17:49 paladox: sudo chown -R www-data:www-data * in /srv/mediawiki-static on nfs1
* 16:51 paladox: re mount /mnt/mediawiki-static as nfs1 has come back up.
* 16:50 paladox: unmount /mnt/mediawiki-static on mw* for nfs1 reboot
* 16:44 paladox: reboot nfs1 to see if that will fix custom images
* 16:32 Reception123: running dumpBackup.php for all wikis (in batches) on test1wiki
* 15:40 Southparkfan: disabled puppet on cp4
* 15:28 paladox: delete backup-root-nfs1
* 15:28 paladox: delete backup-home-nfs1 on db4
* 14:40 paladox: upgrade nginx to 1.14 on cp4
* 14:39 paladox: upgrade nginx to 1.14 on cp2
* 14:39 paladox: upgrade nginx to 1.14 on cp5
* 14:37 paladox: upgraded nginx to 1.14 on misc3
* 14:36 paladox: upgraded nginx to 1.14 on test1
* 14:27 paladox: repool mw3
* 14:27 paladox: upgrade to nginx to 1.14 on mw3
* 14:26 paladox: depool mw3
* 14:26 paladox: repool mw2
* 14:23 paladox: upgrade to nginx to 1.14 on mw2
* 14:23 paladox: depool mw2
* 14:23 paladox: repool mw1
* 14:20 paladox: upgrade nginx on mw1 to 1.14
* 14:20 paladox: depool mw1
* 13:47 paladox: re enable puppet on mw* but keeping file uploads disabled until backup restored complete
* 13:30 paladox: syncing nfs1 backup on db4 back to nfs1.
* 12:56 paladox: reinstall nfs1 as stretch
* 12:52 paladox: salt -E "mw.*" cmd.run "umount /mnt/mediawiki-static"
* 12:52 paladox: downtiming nfs1 in icinga
* 12:49 paladox: disabled puppet on mw*
* 12:32 paladox: update piwik plugin LoginLdap to 4.0.4
* 12:16 paladox: taking one last backup of /srv on nfs1
* 00:50 paladox: rsync -avz --delete -e "ssh -i /home/paladox/id_rsa" /srv/ dbcopy@db4.miraheze.org:/srv/backup-srv-nfs1/ on nfs1 in a screen

## 2018-04-17 

* 23:54 paladox: restoring all backups onto nfs1, will use rsync
* 21:54 paladox: deleting allthetropeswiki from nfs1 as it's backed up on db4
* 20:58 Southparkfan: installed php-memcached on mw1
* 20:35 paladox: rm -rf aktposwiki on nfs1 backup on db4
* 17:26 paladox: rebooted nfs1
* 16:57 paladox: apt-get upgrade on nfs1
* 16:44 paladox: rm -rf * in /var/lib/puppet/clientbucket on db3 to clean some space
* 16:43 paladox: rm -rf * in /var/lib/puppet/clientbucket on db2 to clean some space
* 16:41 paladox: rm -rf * in /var/lib/puppet/clientbucket on nfs1 to clean some space
* 16:39 paladox: removed apt public key EF0F382A1A7B6500 from nfs1, was warnning with "There is no public key available for the following key IDs:"
* 16:36 paladox: installing puppet4 on nfs1
* 16:30 paladox: upgrading puppet to puppet 4 on db3 and db2
* 15:40 paladox: created database icingaweb2 on db4 for icingaweb2
* 15:37 paladox: created database icinga on db4 for icinga2

## 2018-04-16 

* 22:23 paladox: updating acme-tiny in /root on  mw1
* 20:33 paladox: run sudo -u www-data php rebuildLocalisationCache.php --wiki test1wiki for mw* on misc3
* 19:34 paladox: deleted backup backup-repos-misc1 on db4, phabricator may have recreated this as it was working in the ui and there is repos listed.
* 19:33 paladox: deleted backup "backup-mail-misc1" on db4, was synced when we upgraded misc1 last week.
* 19:33 paladox: deleted backup "backup-misc2-home" on db4, was synced just now to misc2
* 19:23 paladox: deleted backup "backup-images-misc1" on db4, was synced to misc1 last week when we upgraded misc1
* 19:22 paladox: deleted backup "backup-misc2-ganglia" was synced to misc2 on sunday
* 19:06 paladox: deleted backup backup-misc2-root from db4, i've just synced it to misc2
* 15:55 paladox: upgraded piwiki plugin "VisitorGenerator" to 3.1.0
* 15:55 paladox: upgraded piwik plugin "QueuedTracking" to 3.2.0
* 15:54 paladox: upgraded piwik to 3.4.0 (no db updates so safe to update)

## 2018-04-15 

* 21:44 paladox: clean up puppet cert for bacula1 pending reinstall
* 21:42 John: installed bacula1 again with more than 20G allocated to / and about 500GB less to /home
* 20:22 paladox: rebooted bacula1
* 16:00 paladox: salt -E 'mw.*' cmd.run 'puppet agent -tv' on misc3
* 16:00 paladox: salt -E 'mw.*' cmd.run 'puppet agent -tv' on mw*
* 15:50 paladox: downtimed misc2 in icinga for maint at 4pm utc
* 15:05 paladox: rebooting puppet1
* 15:04 paladox: upgrading puppet1 to stretch 9.4
* 14:57 paladox: rebooting db4 for kernel upgrade
* 14:52 paladox: reboot db4
* 14:44 paladox: reboot db4 to test mysql starts up
* 14:42 paladox: reboot db4 to see if hostname changes correctly
* 14:30 paladox: rebooting db4 to see if mysql comes back up
* 13:14 paladox: rebooting db4
* 12:43 Reception123: deleted temporary user from bacula1
* 12:24 Reception123: signed bacula1.miraheze.org cert on puppet1

## 2018-04-14 

* 23:53 paladox: downtimed bacula1 until 5:52am
* 19:15 Reception123: re-imaging bacula1 with Debian 9
* 19:14 paladox: Reception123 is reinstalling bacula1 as stretch
* 19:12 paladox: removed bacula1.miraheze.org puppet cert pending reinstall to stretch
* 18:12 paladox: installing salt-master on misc3 to see if i can get a pub key for puppet
* 14:40 paladox:  sudo -u www-data php rebuildLocalisationCache.php --wiki test1wiki mw*
* 14:40 paladox:  sudo -u www-data php rebuildLocalisationCache.php --wiki test1wiki on mw3
* 13:43 paladox: reboot puppet1 to try and clear ram
* 12:30 paladox: created user guest in icinga
* 12:29 Reception123: restarted icinga
* 12:26 Reception123: recreated user 'reception' for icinga
* 00:48 paladox: upgraded test1 to stretch 9.4
* 00:48 paladox: rebooting test1

## 2018-04-13 

* 23:52 Southparkfan: test
* 23:52 paladox:  <+JohnLewis>    !log changed mailname for misc1 to miraheze.org
* 19:49 paladox: reimaging misc1 to stretch
* 14:26 paladox: repool mw2
* 14:19 paladox: rebooting mw2
* 14:14 paladox: upgrading mw2 to stretch 9.4
* 14:14 paladox: depooling mw2
* 14:13 paladox: repooling mw3
* 14:09 paladox: rebooting mw3
* 14:08 paladox: upgrade mw3 to stretch 9.4
* 14:07 paladox: depool mw3
* 01:54 paladox: rebooting misc3
* 01:50 paladox: upgrading misc3 to 9.4 (apt-get upgrade) also upgrade to nginx

## 2018-04-12 

* 23:31 paladox: reimaging cp5 to stretch
* 22:56 paladox: reimaging cp2 as stretch
* 22:36 paladox: reinstalling cp4 as stretch
* 21:59 paladox: reimaging ns1 to stretch
* 21:52 paladox: repooling mw1
* 21:44 paladox:  sudo -u www-data php rebuildLocalisationCache.php --wiki test1wiki on mw1
* 20:52 paladox: reimaging mw1 as stretch
* 20:51 paladox: depooling mw1
* 20:42 MacFan4000: paladox ran puppet on mw* (logging failed the first time)
* 20:11 Southparkfan: created backup of /root and /home on mw1, stored on db4 in /srv/backup-{home,root}-mw1
* 19:52 paladox: rebooting misc1
* 19:31 paladox: restarting puppetdb on puppet1
* 19:28 paladox: restarting apache on misc1
* 19:09 paladox: disabled visualeditor on metawiki due to when using it on the main page it causes an outage
* 19:00 paladox: downgrading parsoid to 0.8 on misc3
* 17:24 paladox: repooling mw2
* 17:21 paladox: depooling mw2
* 17:19 paladox:  sudo -u www-data php rebuildLocalisationCache.php --wiki test1wiki on mw2
* 17:13 paladox: repooling mw2
* 17:11 paladox: sudo -u www-data php rebuildLocalisationCache.php --wiki test1wiki on mw3
* 17:03 Southparkfan: depool mw1 [emergency]
* 16:41 Reception123: signed puppet cert for mw2
* 16:32 Reception123: reinstall mw2 on deb 9
* 16:30 paladox: depooling mw2 from cp[245]
* 16:26 Reception123: repool mw3
* 15:41 Reception123: reinstall mw3
* 15:39 Reception123: depool mw3
* 04:48 Reception123: sudo -u www-data cp -R /srv/mediawiki/w/extensions/SocialProfile/avatars /srv/mediawiki/w/extensions/SocialProfile/awards /mnt/mediawiki-static/avalicearchiveswiki/

## 2018-04-11 

* 20:42 paladox: sudo service icingabot restart
* 19:48 PuppyKun: made paladox a github org owner
* 19:19 paladox: restart icinga
* 19:19 paladox: removing parsoid1 from icinga on misc1
* 19:04 paladox: sudo chown -R www-data:www-data /srv/mediawiki/w/cache/l10n/ on mw3
* 17:53 paladox: running  sudo -u www-data php rebuildLocalisationCache.php --wiki test1wiki on mw*
* 17:51 paladox: running  sudo -u www-data php rebuildLocalisationCache.php --wiki test1wiki on mw1
* 16:41 paladox: running puppet on mw*
* 16:03 Reception123: upgraded phabricator
* 15:45 paladox: running sudo -u www-data php rebuildLocalisationCache.php --wiki test1wiki
* 15:45 paladox: running "sudo -u www-data php mergeMessageFileList.php --output /srv/mediawiki/config/ExtensionMessageFiles.php --wiki test1wiki"
* 14:58 paladox: redoing  sudo -u www-data php rebuildLocalisationCache.php --wiki test1wiki
* 14:58 paladox: sudo -u www-data php mergeMessageFileList.php --output /srv/mediawiki/config/ExtensionMessageFiles.php --wiki test1wiki
* 14:56 paladox: sudo -u www-data php rebuildLocalisationCache.php --wiki test1wiki
* 14:18 Reception123: made paladox a phabricator administrator
* 14:17 Reception123: added Paladox to @miraheze
* 00:41 PuppyKun: added john / John Lewis / john `{{ {{@}} }}`miraheze.org as a Matamo superuser.

## 2018-04-10 

* 23:56 John: parsoid1->misc3, misc3->stretch, parsoid->0.9.0, revert-count->big, error-count->less-than-earlier, success?->questionable-but-it-works

## 2018-04-09 

* 22:17 John: made H29 only act once
* 22:13 John: rebuilding LC on mw3
* 18:45 Reception123: sudo -u www-data php rebuildLocalisationCache.php --wiki test1wiki
* 16:33 John: restarted jobrunner on mw2,3
* 16:31 John: running jobs

## 2018-04-08 

* 20:28 John: deleted Mkraheze/Math

## 2018-04-06 

* 18:10 Reception123: repool mw1
* 18:09 Reception123: clear out /srv/mediawiki/config on mw1 for reclone
* 18:09 Reception123: depool mw1
* 18:09 Reception123: repool mw3
* 18:08 Reception123: clear out /srv/mediawiki/config for reclone
* 18:08 Reception123: depool mw3
* 17:49 Reception123: ran check_procs for php7.0-fpm
* 14:43 Reception123: reboot test1
* 13:52 Reception123: reinstall test1 on Debian 9
* 13:46 Reception|away: reception@mw2:/srv/mediawiki/w/extensions/Flow/maintenance$ sudo -u www-data php convertNamespaceFromWikitext.php --wiki isvwiki <multiple NS>
* 13:05 Reception|away: reception@mw2:/srv/mediawiki/w/maintenance$ sudo -u www-data php populateContentModel.php --wiki isvwiki --ns all --table revision

## 2018-04-05 

* 15:31 Reception|away: sudo service icingabot restart
* 15:28 Reception|away: restarted puppetdb on puppet1
* 13:37 John: db4 has SSL capabilities now

## 2018-04-04 

* 23:21 John: installed db4 as stretch
* 22:47 John: reinstall db4 as stretch
* 22:43 John: unsigned db4 from puppet1
* 17:19 Reception123: sudo -u www-data php rebuildLocalisationCache.php --wiki test1wiki on mw*

## 2018-04-03 

* 19:35 Southparkfan: restart ganglia-monitor on puppet1
* 19:23 John: restart ganglia-monitor on mw1
* 14:02 John: add cw_custom to cw_requests on metawiki
* 13:20 John: rebooted db2, excessive server load and CPU usage
* 09:07 revi: add @miraheze/i18n group to WikiDiscover repo

## 2018-04-02 

* 19:25 revi: changed phabricator global timezone settings to UTC instead of Europe/London
* 18:44 Reception123: added mw-admins team to @miraheze/WikiDiscover
* 18:36 Reception123: added IRC webhook to @miraheze/WikiDiscover
* 14:45 Reception123: repooled mw3
* 14:36 Reception123: sudo -u www-data php mergeMessageFileList.php --output /srv/mediawiki/config/ExtensionMessageFiles.php --wiki test1wiki and rebuild LC on mw1 and mw2
* 14:21 Reception123: clear /srv/mediawiki/config on mw3
* 14:21 Reception123: depool mw3
* 14:21 Reception123: repool mw2
* 14:20 Reception123: manually pull changes on misc1
* 13:57 Reception123: clear /srv/mediawiki/w on mw2
* 13:57 Reception123: depool mw2
* 13:57 Reception123: repool mw1
* 12:08 Reception123: cleared /srv/mediawiki/w on mw1
* 12:07 Reception123: depool mw1

## 2018-04-01 

* 19:49 Reception123: disabled puppet on puppet1
* 19:19 Reception123: signed certs for all servers on puppet1 except mw* and cp*
* 15:59 Reception123: reinstalling puppet1 on Debian 9
* 13:41 Reception123: signed cp5 cert on puppet1
* 06:54 Reception123: sudo -u www-data cp -r /srv/mediawiki/w/extensions/SocialProfile/avatars & awards /mnt/mediawiki-static/garrettcountyguidewiki

## 2018-03-31 

* 21:31 John: running manageInactiveWikis.php to close old wikis and mark inactive wikis as wiki_inactive
* 14:56 Reception123: reinstall test1 to test puppet1 install
* 06:33 Reception123:  sudo -u www-data php mergeMessageFileList.php --output /srv/mediawiki/config/ExtensionMessageFiles.php --wiki test1wiki and rebuild LC on mw*
* 05:32 Reception123: sudo -u www-data php importDump.php --wiki wiki1776wiki /home/reception/Wikipedia-20180216182614.xml && sudo -u www-data php importDump.php --wiki unionwiki /home/reception/Wikipedia-20180313163344.xml && sudo -u www-data php importDump.php --wiki wiki1776wiki /home/reception/Wikipedia-20180313163344.xml on mw3

## 2018-03-30 

* 22:40 John: made security task public
* 19:38 Reception123: made John a phab admin
* 08:38 Reception123: reception@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php importDump.php --wiki loraldwiki /home/reception/lorald_pages_current.xml
* 08:04 Reception123: upgraded phabricator

## 2018-03-29 

* 17:54 Reception123: manually removed "debian" and "db5" from services file

## 2018-03-27 

* 16:21 revi: latest command for T2904
* 16:21 revi: revi@mw3:/srv/mediawiki/w/maintenance$ sudo -u www-admin php namespaceDupes.php --fix --wiki=tmewiki
* 15:57 revi: sudo puppet agent -t on mw(1-3)

## 2018-03-25 

* 14:48 Reception123: cleared /tmp on mw2

## 2018-03-24 

* 18:57 Reception123: sudo -u www-data php rebuildLocalisationCache.php --wiki test1wiki  on mw*
* 07:28 Reception123: repool mw1
* 06:59 Reception123: refresh /srv/mediawiki on mw1
* 06:59 Reception123: depool mw1

## 2018-03-23 

* 16:47 Reception123: restarted nginx on mw1

## 2018-03-21 

* 19:54 Reception123: upgraded phabricator
* 19:51 Reception123: restarted icinga

## 2018-03-20 

* 07:12 Reception123: MariaDB [phabricator_herald]> UPDATE herald_rule SET isDisabled = '1' WHERE id = '24';

## 2018-03-12 

* 17:44 revi: revi@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php initSiteStats.php --update --wiki=reviwikiwiki
* 17:35 Reception|away: reception@mw3:/srv/mediawiki/w/maintenance$ sudo -u www-data php importDump.php --wiki reviwikiwiki /home/reception/reviwiki.xml
* 17:28 Reception|away: DELETED from cw_wikis and DROPPED reviwikiwiki (recreation)

## 2018-03-11 

* 12:49 revi: make [https://phabricator.miraheze.org/H31](https://phabricator.miraheze.org/H31) stricter

## 2018-03-10 

* 16:51 revi: phab project import was created while ago, forgot to log
* 15:41 Reception123: created [https://phabricator.miraheze.org/H32](https://phabricator.miraheze.org/H32) for secure mail

## 2018-03-09 

* 17:05 Southparkfan: fixed ownership of www-data on mw1

## 2018-03-08 

* 17:20 Southparkfan: create global_preferences table on centralauth db, drop global_preferences table from metawiki db
* 17:11 Reception123: ran /srv/mediawiki/w/extensions/GlobalPreferences/schema.sql on metawiki
* 16:24 Reception123: sudo -u www-data php mergeMessageFileList.php --output /srv/mediawiki/config/ExtensionMessageFiles.php --wiki test1wiki and rebuild LC on mw*
* 12:35 Reception123: reception@mw3:/srv/mediawiki/w/extensions/CentralAuth/maintenance$ sudo -u www-d                                                                                        ata php migrateAccount.php --wiki metawiki --userlist /home/reception/whsapushli                                                                                        st.txt --auto

## 2018-03-07 

* 19:46 Reception123: deleted and dropped testdeletewiki
* 15:22 Reception123: restart jobrunners on mw2 and mw3 and manually run jobs on mw1
* 12:19 Reception123: sudo -u www-data foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/maintenance/runJobs.php on mw1
* 09:40 Reception123: sudo -u www-data php /srv/piwik/console core:archive on misc2

## 2018-03-06 

* 11:50 Reception123: sudo -u www-data php mergeMessageFileList.php --output /srv/mediawiki/config/ExtensionMessageFiles.php --wiki test1wiki and rebuild LC on mw*
* 06:23 Reception123: upgraded phabricator

## 2018-03-05 

* 08:09 Reception123: repool mw1
* 08:06 Reception123: sudo -u www-data php importDump.php --wiki magnaversewiki [and enigmawiki] /home/reception/Infoboxes for Magnaverse - 1.xml
* 07:53 Reception123: clear out /srv/mediawiki on mw1 and re-run puppet (failing to pull mediawiki)
* 07:53 Reception123: depool mw1
* 07:42 Reception123: on sudo -u www-data php importDump.php --wiki almanachdebauswicwiki /home/reception/Gelo+e+Fogo+wiki-20180303164425.xml mw2
* 07:42 Reception123: sudo -u www-data php importDump.php --wiki almanachdebauswicwiki /home/reception/Gelo+e+Fogo+wiki-20180303163927.xml on mw3

## 2018-03-03 

* 22:22 Southparkfan: restoring bacula's db3 backup on db4

## 2018-03-01 

* 21:52 Southparkfan: removed nginx from nfs1
* 21:02 Southparkfan: replicating db3 to db4 (without read lock, to prevent downtime)
* 20:14 Southparkfan: downtimed db4 in icinga, moved spfwiki from db4 to db2
* 00:55 Southparkfan: db2 was holding (deleted) 20GB file mysql-slow.log.1 open. truncated it to reclaim 20GB space
* 00:52 Southparkfan: db2 was holding file mysql-slow.log.1 open. by truncating it using ":>/proc/763/fd/54" I reclaimed 12GB space
* 00:29 Southparkfan: purged binary logs @ db3
* 00:14 Southparkfan: drop db southparkfanwiki on db2

## 2018-02-28 

* 23:52 Southparkfan: reboot db4 after kernel upgrade
* 23:42 Southparkfan: reboot db4
* 17:28 Reception123: removed db5 and "debian" from storeconfigs on puppet and moved /etc/icinga/config/puppet_services.cfg to a backup file then ran puppet to regenerate the list of services
* 16:43 Reception123: stopped then started apache2 on misc1
* 16:38 Reception123: removed /var/lib/apt/lists/* and regenerated with apt-get update
* 16:26 Reception123: sudo service icingabot restart
* 10:14 Reception123: manually edit (renew) phab.miraheze.wiki on misc1

## 2018-02-27 

* 21:18 Southparkfan: sysctl vm.swappiness=1 on db4
* 21:12 Southparkfan: restarted jobrunners
* 18:55 Reception123: manually run sudo -u www-data foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/maintenance/runJobs.php on mw1 to alleviate queue
* 16:58 Southparkfan: truncate allthetropeswiki.objectcache

## 2018-02-26 

* 14:26 Reception123: chowned /etc/icinga/config/puppet_services.cfg to icinga:icinga
* 14:15 Reception123: retry moving /etc/icinga/config/puppet_services.cfg to a backup file then ran puppet to regenerate the list of services
* 08:38 Reception123: > UPDATE cw_wikis SET wiki_closed = '0' WHERE wiki_dbname = '131parkhurstwiki'; (requested, ManageWiki broken)

## 2018-02-25 

* 19:56 Southparkfan: ALTER TABLE cw_wikis ADD COLUMN wiki_inactive_timestamp BINARY(14) AFTER wiki_inactive;
* 19:26 Southparkfan: ALTER TABLE cw_wikis ADD COLUMN wiki_closed_timestamp BINARY(14) AFTER wiki_closed; and ALTER TABLE cw_wikis ADD COLUMN wiki_inactive smallint(6) AFTER wiki_closed_timestamp;
* 18:55 Southparkfan: deleted the following wikis: [https://phabricator.miraheze.org/P43](https://phabricator.miraheze.org/P43)
* 17:57 Reception123: manually restarted icinga as well (required for the changes to take effect)
* 17:56 Reception123: manually reloaded icinga
* 17:52 Reception123: moved /etc/icinga/config/puppet_services.cfg to a backup file then ran puppet to regenerate the list of services
* 17:18 Southparkfan: decommissioned db4
* 09:32 Reception123: sudo -u www-data php dumpBackup.php --wiki testwiki --full > /home/reception/testwiki25022018.xml on mw3
* 09:31 Reception123: sudo -u www-data php dumpBackup.php --wiki metawiki --full > /home/reception/metawiki25022018.xml on mw2
* 06:40 Reception123: reception@mw3:/srv/mediawiki/w/maintenance$ sudo -u www-data php importDump.php --wiki templatewiki /home/reception/Wikipedia-20180224165206.xml

## 2018-02-24 

* 14:38 Reception123: sudo service icingabot restart
* 13:23 Reception123: sudo -u www-data php importDump.php --wiki templatewiki /home/reception/Wikipedia-20180224132217.xml on mw3

## 2018-02-23 

* 22:39 Southparkfan: restarted ganglia-monitor on parsoid1+bacula1
* 21:53 Southparkfan: cleaned db entries, dropped databases and removed nfs dirs for wikis: [https://phabricator.miraheze.org/P42](https://phabricator.miraheze.org/P42)
* 21:18 Southparkfan: cleaned db entries, dropped databases and removed nfs dirs for wikis: [https://phabricator.miraheze.org/P41](https://phabricator.miraheze.org/P41)
* 20:40 Southparkfan: cleaned db entries, dropped databases and removed nfs dirs for wikis: [https://phabricator.miraheze.org/P40](https://phabricator.miraheze.org/P40)
* 20:15 Southparkfan: cleaned db entries, dropped databases and removed nfs dirs for wikis: [https://phabricator.miraheze.org/P39](https://phabricator.miraheze.org/P39)
* 16:52 Reception123: reinstalling test1 (for further testing)
* 16:05 Reception123: added grants for icinga on db4
* 14:32 Reception123: sudo -u www-data php mergeMessageFileList.php --output /srv/mediawiki/config/ExtensionMessageFiles.php --wiki test1wiki and rebuild LC on mw*
* 09:42 Reception123: purge binary logs before '2018-02-23 00:00:00'; on db3
* 07:36 Reception123: sudo service icingabot restart
* 06:28 Reception123: moved to db3; dropped on db2 aerosswiki diagnostikwiki encyclopaediawiki networksdatabasewiki pocketmonsterswiki scruffy2wiki summerolympicswiki ussewiki

## 2018-02-22 

* 18:08 Reception123: DELETED from cw_wikis and DROPPED on db2 contextwiki  contigoconnectwiki conuconwiki  coopwiki coorwiki coreywiki cpswiki crwikiwiki crxtrdudewiki cswiki ctuvnwiki cubewiki cultofparetowiki customerdesignwiki cwlagusawiki

## 2018-02-20 

* 20:30 Reception|away: purge binary logs before '2018-02-20 20:00:00'; on db2
* 09:02 revi: create [https://phabricator.miraheze.org/H31](https://phabricator.miraheze.org/H31) to autoclose spam
* 06:19 Reception|away: purge binary logs before '2018-02-20 03:00:00'; on db3

## 2018-02-19 

* 18:12 Reception|away: DELETED FROM cw_wikis and DROPPED on db2 childrensinstitutewiki chocowiki chromiumrosewiki chronicleswiki cinquiemesaisonwiki clarifirewiki clarkfamilywiki classroomsonelightglobalwiki clearicewiki clementsworldbuildingwiki cmpcrswiki cobwebmudwiki code7wiki codebaseclubwiki cofradiawiki cognitowiki colaboratoriowiki colfaxknightswiki collarwiki columbiasjpiwki comidawiki commonsensewiki composerohswiki concertpowerswiki
* 05:57 Reception123: moved to db3 and dropped on db2 revitwiki unionwiki wiki1776wiki

## 2018-02-17 

* 19:59 Southparkfan: purged binary logs on dbx
* 12:37 Reception123: sudo service icingabot restart
* 07:47 Reception123: brokenworldwiki brooklynrfbwiki  brxdwiki bssentialswiki bsuirwiki budgetenvywiki bulldogsracingtestwiki burnoutwiki bzdetopediawikibzswiki cagencywikiwiki cancerwiki cantelli25wiki casinotermswiki caspwiki cassallenwiki  casswiki cbecwiki cecwiki celuwiki chakorduvorwiki chaldunwiki cherryitwiki
* 07:47 Reception123: DELETED FROM CW_WIKIS and DROPPED bobwiki boftwiki bookswiki bootstrapwiki bottlefarmwiki answerswiki boytvofwiki braindumpwiki bremenwikiwiki bribriwiki  broadwaveswiki brofactorywiki

## 2018-02-16 

* 06:13 Reception|away: cleared /tmp on mw2
* 05:47 Reception|away: DELETED FROM cw_wikis and DROPPED automotivewiki avidkbwiki azurawiki backyardsportsfanonwiki2wiki banglawiki barigawiki bcmschinawiki beckleynotebookwiki becuzwiki beezerwiki begawktdwiki bellmarewiki bertelwiki besselingwiki bhenuawiki bialowiezawiki bibliowiki bilatwiki bimbowiki bio10a2016garwiki bitphoriawiki bizmodsimwiki blackdesertfanonwiki blackstumpwiki blindfoldstudioswiki

## 2018-02-15 

* 18:17 Reception|away: reception@mw2:/srv/mediawiki/w/maintenance$ sudo -u www-data php importDump.php --wiki templatewiki /home/reception/Wikipedia-20180215181624.xml
* 18:01 Reception|away: moved to db3 and dropped on db2 nextlevelwikiwiki recentiawiki teriawiki zendariwiki
* 17:40 Reception|away: moved supernamuwiki from db3 to (temporary) db4, dropped from db3

## 2018-02-14 

* 19:31 Reception|away: DELETED from CW_WIKIS and dropped ictjudikaturawiki (T2724)
* 19:17 Reception|away: moved templatewiki and mc2wiki to db3 and dropped on db2

## 2018-02-12 

* 11:12 revi: [https://phabricator.miraheze.org/H30](https://phabricator.miraheze.org/H30) updated to automatically subscribe CoCC members

## 2018-02-11 

* 06:57 Reception123: purge binary logs before '2018-02-11 06:00:00'; on db2
* 06:52 Reception123: sudo -u www-data foreachwikiindblist /srv/mediawiki/dblist/all.dblist /srv/mediawiki/w/maintenance/sql.php /srv/mediawiki/w/extensions/QuizGame/sql/quizgame.sql
* 06:48 Reception123: sudo -u www-data php mergeMessageFileList.php --output /srv/mediawiki/config/ExtensionMessageFiles.php --wiki test1wiki and rebuild LC on mw*

## 2018-02-10 

* 12:03 Reception123: DROPPED wikis below
* 10:56 Reception123: DELETED FROM CW_WIKIS altenpflegewiki altwiki amningwiki amparodenaswiki annuwikiwiki anon4wiki antoinewiki apenlinjewiki apituwiki apparchitectwiki apslaxwiki  aptotecwiki aquivawiki arabudlandwiki arbabilowiki archipediawiki argentinachicagowiki arguwikiwiki arkheonwiki armlaptopwiki askerwiki astawiki atkinswiki atplwiki audiowikiwiki autismadminswiki
* 07:31 Reception123: sudo -u www-data php importDump.php --wiki podpediawiki /home/reception/roosterteeth_pages_current.xml on mw2

## 2018-02-08 

* 20:58 Southparkfan: mw1 repooled
* 19:12 Southparkfan: mw1 emergency depool
* 19:10 Reception123: purge binary logs before '2018-02-08 16:00:00'; on db2
* 18:47 Southparkfan: on cp4: varnishlog -g raw -i Backend_health -a -w /var/log/varnish/varnish-backend.log -D
* 16:37 Southparkfan: ran git submodule update --init in /srv/piwik

## 2018-02-06 

* 06:46 Reception123: moved liberartwiki to libreartwiki

## 2018-02-04 

* 13:27 Reception123: moved mistralcupwiki from db4 to db2 (created when metawiki was moved to db4; not declared in Database.php)
* 09:40 Reception123: moved to db3 and dropped on db2 ctswiki fourleafficswiki karniarutheniawiki madciclistawiki nvcwiki songcontestswiki unionnorteamericanawiki valentinaprojectwiki
* 05:55 Reception123: moved metawiki back to db2 (has to be on default or else there are CW errros)

## 2018-02-03 

* 23:53 Southparkfan: dropped worlduniversityandschoolwiki, tmewiki and vandalwiki, all wikis have been transferred to c3
* 22:44 Southparkfan: moved metawiki to c3, dropped database on db2. backup is in /home/dbcopy for emergencies
* 18:19 Reception123: upgraded phabricator

## 2018-02-02 

* 20:04 Reception123: purge binary logs before '2018-02-02 18:00:00'; on db2
* 18:28 Southparkfan: MariaDB [metawiki]> update cw_wikis set wiki_dbcluster = 'c3' where wiki_dbname = 'testwiki';
* 15:48 PuppyKun: destroyed db5 last night

## 2018-02-01 

* 22:03 PuppyKun: root@mw1:/srv/mediawiki/w/extensions/CentralAuth/maintenance# sudo -u www-data php fixStuckGlobalRename.php --wiki=maiasongcontestwiki --logwiki=metawiki "WEMO666" "Chriskk01b"
* 21:55 PuppyKun: MariaDB [centralauth]> delete from renameuser_status where ru_wiki="lothuialethwiki"; (query ok, 1 row affected)
* 21:44 PuppyKun: removeDeletedWikis for lothuialethwiki
* 18:59 Southparkfan: cleaned puppet certificate info about db5
* 18:48 PuppyKun: hard rebooting db5
* 17:29 revi: update phabricator maniphest form 14 ( [https://phabricator.miraheze.org/transactions/editengine/maniphest.task/view/14/](https://phabricator.miraheze.org/transactions/editengine/maniphest.task/view/14/) ) preamble
* 02:12 PuppyKun: rebooted db5
* 02:05 PuppyKun: rebooted db5
* 02:00 PuppyKun: started hard reboot of db5.miraheze.org (unresponsive to ssh)
* 01:48 PuppyKun: doing first puppet run on db5.cloud.online.net (??? that was the name that showed up when i did --wait-for-cert on db5.mh.o and the fingerprint matched)

## 2018-01-29 

* 10:27 revi: create #spam in Phabricator, for spammy tasks

## 2018-01-28 

* 18:59 Reception123: moved to db3 and dropped on db2 madgendersciencewiki ubrwikiwiki nonbinarywiki linenwiki beatstationwiki daesocialwiki uncyclopediawiki musicarchivewiki thegreatwarwiki christianmusictempwiki hellointernetwiki christianmusicwiki spritopiawiki magnaversewiki
* 18:24 Reception123: disabled puppet on db3
* 15:33 Reception123: revi added to @miraheze puppet-users team

## 2018-01-27 

* 20:36 Reception123: purge binary logs before '2018-01-27 15:00:00'; on db2

## 2018-01-25 

* 17:04 Reception|away: installed db4 and signed cert on puppet1

## 2018-01-24 

* 18:48 Reception|away: upgraded phabricator

## 2018-01-23 

* 06:45 Reception|away: purge binary logs before '2018-01-23 00:00:00';

## 2018-01-22 

* 20:26 Reception|away: sudo rm -rf /var/lib/puppet/reports on puppet1 (disk space running out)

## 2018-01-21 

* 10:50 Reception123: sudo -u www-data php mergeMessageFileList.php --output /srv/mediawiki/config/ExtensionMessageFiles.php --wiki test1wiki and rebuild LC on mw*
* 08:31 Reception123: archived H2 (no longer used)

## 2018-01-20 

* 08:09 Reception123:  sudo -u www-data php dumpBackup.php --wiki metawiki --full > /home/reception/metawiki.xml on mw3

## 2018-01-19 

* 18:22 Reception123: rebooted test1 (puppetmaster)
* 17:43 Reception123: sudo -u www-data php importDump.php --wiki pwikiwiki /home/reception/arkcls-wiki-20180117.xml on mw1

## 2018-01-18 

* 17:54 Reception123: re-enabled puppet on db3
* 17:54 Reception123: moved databases to db3 and dropped on db2 dariawikiwiki  viagroupiawiki truecapitalistwiki emulationwiki cpiwiki ylscwiki hirapediawiki whentheycrywiki utamacrosswiki sumroletaericwiki
* 17:30 Reception123: disabled puppet on db3

## 2018-01-16 

* 06:37 Reception123: renewed phab.miraheze.wiki on misc1

## 2018-01-09 

* 06:49 Reception123: upgraded Phabricator

## 2018-01-08 

* 06:02 Reception123: restarted Phabricator daemons

## 2018-01-07 

* 02:33 PuppyKun: rebooted mw2 to fix puppet hangs?

## 2018-01-06 

* 16:19 Reception123: reinstalling bacula1 (size change; backups not running)

## 2018-01-05 

* 01:34 PuppyKun: MariaDB [centralauth]> update globaluser set gu_hidden="suppressed" where gu_id in (9192,9193,9188,9190,13117,13118,13119,13140,12407,12405,12404,11327,12293,11296,11292,11280,11481,11716,11717,11196,11197,11198,11199,11201,11202,11203,11204,11205); Query OK, 28 rows affected (0.01 sec)

## 2018-01-04 

* 18:23 Reception123: sudo -u www-data php importImages.php --wiki dariawikiwiki --search-recursively /home/reception/images on mw1
* 08:41 Reception123: re-reinstall test1 on debian 9

## 2018-01-03 

* 16:47 Reception123: reinstalling test1 on debian 9

## 2018-01-02 

* 15:13 Reception123: started jobrunner on mw2 (moved from test1)
* 15:09 Reception123: restarted phabricator daemons
* 08:24 Reception123: sudo -u www-data php rebuildLocalisationCache.php --wiki test1wiki on mw*

## 2018-01-01 

* 23:26 PuppyKun: renewed publictestwiki.com
* 15:05 Reception123: cleared /tmp of mw2 (full)
* 09:08 Reception|away: sudo -u www-data php importDump.php --wiki dariawikiwiki /home/reception/DariaWikiDump_12.31.17.xml on mw2

## Information 

All times are in **UTC+0**/**GMT**.

Archives: [2015](https://meta.miraheze.org/wiki//2015), [2016](https://meta.miraheze.org/wiki//2016), [2017](https://meta.miraheze.org/wiki//2017)

----
**Source**: [https://meta.miraheze.org/wiki/Tech:Server_admin_log/2018](https://meta.miraheze.org/wiki/Tech:Server_admin_log/2018)