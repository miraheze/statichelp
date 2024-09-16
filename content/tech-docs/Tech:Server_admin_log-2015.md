---
title: Tech:Server admin log/2015
---

`{{ {{TOC right}} }}`
## 2015-12-30 

* 18:44 SPF|Cloud: ran update.php on indexwiki and entropediawiki

## 2015-12-26 

* 10:46 Southparkfan: powercycle cp2 due to "Failed to get D-Bus connection: no such file or directory" errors
* 04:20 NDKilla: @mw1 php maintenance/rebuildrecentchanges.php --wiki tyrolmountainswiki (didn't fix [issue 234](https://github.com/miraheze/mw-config/issues/234)) -- Cheers, [NDKilla](https://meta.miraheze.org/wiki/User:NDKilla)( [Talk](https://meta.miraheze.org/wiki/User_talk:NDKilla) • [Contribs](https://meta.miraheze.org/wiki/Special:Contributions/NDKilla) ) 04:22, 26 December 2015 (UTC)

## 2015-12-19 

* 18:15 Southparkfan: @cp1 & cp2: varnish> ban req.http.Host == 'static.miraheze.org'

## 2015-12-13 

* 23:06 SPF|Cloud: ran "update cw_wikis set wiki_private = 1 where wiki_dbname = 'southparkfanwiki';" on db1

## 2015-11-26 

* 15:10 SPF|Cloud: disabled puppet on mw1 to fix my stupidness

## 2015-11-24 

* 15:40 SPF|Cloud: ran update.php @ micropediawiki

## 2015-11-23 

* 20:53 SPF|Cloud: enabled puppet on db1. This is what disabling ufw logging causes to dmesg: [https://www.irccloud.com/pastebin/7BBXjkOF/](https://www.irccloud.com/pastebin/7BBXjkOF/)

## 2015-11-21 

* 16:11 SPF|Cloud: running importDump.php on poserdazfreebiestestwiki
* 16:11 SPF|Cloud: imported stuff for poserdazfreebiestestwiki

## 2015-11-20 

* 16:39 SPF|Cloud: disabled puppet on db1 for troubleshooting

## 2015-11-12 

* 17:43 SPF|Cloud: importing first batch of ATT images

## 2015-11-11 

* 14:56 JohnFLewis: deleted stale duping jobqueue keys for allthetropeswiki from redis -- down from 502 to 2

## 2015-11-09 

* 19:10 SPF|Cloud: root@mw1:/srv/mediawiki/w/maintenance# ufw allow from 185.52.1.76 to any
* 18:47 JohnFLewis: gradually killing allthetropeswiki job queue, expect few performance issues
* 18:04 SPF|Cloud: dropped southparkfan2wiki until southparkfan11wiki

## 2015-11-08 

* 11:59 SPF|Cloud: manually ran runJobs.php on all wikis. Because ATT has over 7000 jobs, I'm doing that wiki now manually.

## 2015-11-07 

* 18:24 SPF|Cloud: running following script now (takes a very long time!): southparkfan@mw1:/srv/mediawiki/w/maintenance$ sudo -u www-data php /srv/mediawiki/w/maintenance/deleteBatch.php --wiki allthetropeswiki -r 'Prepare for another image import (--Southparkfan)' /home/southparkfan/att-missing.txt
* 15:53 SPF|Cloud: issued "ban req.url ~ /" command to Varnish on cp2

## 2015-11-06 

* 17:20 JohnFLewis: removed firewall rules on servers for IP 185.34.216.183
* 17:12 JohnFLewis: remove DDoS IP from mw1
* 14:07 SPF|Cloud: restarted parsoid on parsoid1 to avoid possible OOM

## 2015-11-04 

* 17:44 SPF|Cloud: on misc1 in /var/lib/ganglia/rrds: $ find ./ -type f -name '*sintr*' -delete, and: $ find ./ -type f -name '*steal*' -delete
* 11:01 JohnFLewis: rebooted misc1 - memory issues need to be resolved asap

## 2015-11-03 

* 19:11 SPF|Cloud: root@db1:/etc/rsyslog.d# sudo service rsyslog restart, to fetch change to ufw file in rsyslog.d
* 15:51 SPF|Cloud: disabled ufw logging on db1

## 2015-11-01 

* 12:31 SPF|Cloud: reverted ganglia changes (see SAL entry 7 minutes earlier)
* 12:24 SPF|Cloud: installed ganglia-monitor-python on cp1 and restarted ganglia-monitor

## 2015-10-28 

* 15:49 JohnFLewis: shutting down cp2; fail over test for dns
* 15:43 JohnFLewis: digging ns1: ns1: cp2, ns2: cp1, ns3: cp2, me: cp1
* 15:41 JohnFLewis: loading geodns data into ns1 nameserver; ns2/3 staying weighted

## 2015-10-27 

* 19:08 SPF|Cloud: manually downgraded GDNSD to 2.1.2-1~deb8u1 on ns1 (the upgrade to the stretch version was unpuppetized, and we don't want to deploy that puppet change until tomorrow)

## 2015-10-26 

* 22:26 JohnFLewis: changed IPv6 address for cp2
* 17:36 SPF|Cloud: ran >update cw_wikis set wiki_private = 0 where wiki_dbname = 'walthamstowlabourwiki';
* 13:37 JohnFLewis: renamed undisconnectwiki to heistwiki
* 13:29 JohnFLewis: converted 8stationwiki wikitext pages to Flow

## 2015-10-23 

* 19:36 JohnFLewis: deleted an attwiki dump from /home/revi
* 11:26 SPF|Cloud: purged Varnish cache to ensure 404 wiki not found errors are gone
* 11:19 JohnFLewis: reverts database lists back to how they were pre-DB managed CreateWiki
* 11:12 JohnFLewis: rebooted m1, unresponsive

## 2015-10-22 

* 16:57 Southparkfan: restarted ganglia-monitor on mw1
* 10:52 SPF|Cloud: root@mw1:/etc/apache2/sites-enabled# apt-get --purge remove apache2
* 10:46 SPF|Cloud: mw1 got rebooted for an unknown reason, Apache started (took precedence over nginx), downtime on farm. Killed Apache and restarted nginx
* 04:15 revi: restarted hhvm, as usual, 502.

## 2015-10-21 

* 17:40 SPF|Cloud: shutdown cp1 for reinstall
* 14:02 JohnFLewis: restarted HHVM
* 4:24 revi: sudo service hhvm restart, 502

## 2015-10-20 

* 17:40 JohnFLewis: install traceroute on mw1 [should perhaps install by default?] -- networking issues
* 15:15 SPF|Cloud: restarted Redis

## 2015-10-19 

* 22:45 JohnFLewis: rebooting ns1
* 21:48 JohnFLewis: set DNS for main app. wikis and mw1 to non-filtered. fallback to filtered in place for wikis but NOT mw1
* 3:25 revi: sudo /root/puppet-run -f, my stupid pushing without auditing.

## 2015-10-18 

* 7:05 revi: restarted hhvm; gh#188
* 4:44 revi: restarted HHVM, gh#188.

## 2015-10-11 

* 4:22 revi : restarted HHVM at 04:22 UTC, forgot to log. (-added by Reception123 as mhlogbot currently not working)

## 2015-10-05 

* 14:03 JohnFLewis: stricter controls added by Black Lotus for mw1
* 04:16 revi: restarted HHVM, 502

## 2015-10-04 

* 16:56 SPF|Cloud: imported bgowiki
* 09:12 SPF|Cloud: restarted MariaDB

## 2015-10-03 

* 18:16 SPF|Cloud: killed one runJobs.php process, and set nice +19 on the other running one
* 11:39 revi: imported szkwiki

## 2015-10-02 

* 20:25 SPF|Cloud: restarted HHVM
* 15:00 revi: imported wikiconstituciowiki
* 12:18 SPF|Cloud: restarted MariaDB

## 2015-10-01 

* 23:58 mutante: restarted nginx on mw1
* 16:47 SPF|Cloud: issued SIGKILL to all HHVM processes, afterwards service hhvm restart
* 15:55 SPF|Cloud: restarted nginx
* 14:12 JohnFLewis: converted all talk pages to flow on permanentfuturelabwiki
* 06:08 revi: imported batch 1 of poserdazfreebieswiki, 5 imported (batch 3: 3 imported) closing #141.
* 06:05 revi: imported batch 3 of poserdazfreebieswiki 3 mins ago
* 04:25 revi: restart HHVM, 502 again

## 2015-09-30 

* 19:24 SPF|Cloud: update page set page_namespace = 1621 where page_namespace = 521; for ATT
* 19:24 SPF|Cloud: update page set page_namespace = 1620 where page_namespace = 520; for ATT
* 11:11 JohnFLewis: restarted hhvm, disable extension causing segfault *NOT* OOM
* 10:08 revi: restarted HHVM hour ago (...) 502
* 10:00 JohnFLewis: rebooting mw1 (mem leak.)
* 01:14 NDK|Cloud: Restarted hhvm, 502 ( `{{ {{Ping|John|Southparkfan}} }}` [https://www.irccloud.com/pastebin/bGOaVBVy/](https://www.irccloud.com/pastebin/bGOaVBVy/) )

## 2015-09-29 

* 21:05 JohnFLewis: rebooted mw1; monitoring swap usage
* 20:24 SPF|Cloud: HHVM restarted
* 19:08 JohnFLewis: restarted hhvm again
* 17:03 SPF|Cloud: restarted HHVM
* 16:05 JohnFLewis: restarted MariaDB (crashed searchindexes again)
* 14:50 JohnFLewis: MariaDB [(none)]> drop database cinemawiki;
* 10:37 SPF|Cloud: Session issues, restarted Redis. Seems fixed now.
* 03:22 revi: restarted HHVM  4mins ago (yes, 502)

## 2015-09-28 

* 16:04 SPF|Cloud: restart HHVM for [https://github.com/miraheze/puppet/commit/6d1dfa48866ecd1afbd70a4479a0f3edf28e7d6a](https://github.com/miraheze/puppet/commit/6d1dfa48866ecd1afbd70a4479a0f3edf28e7d6a)
* 02:12 revi: restarted HHVM, 502
* 01:26 revi: restarted HHVM, 502

## 2015-09-27 

* 15:25 SPF|Cloud: installed security updates on mw1
* 14:13 SPF|Cloud: restarted MariaDB
* 13:00 SPF|Cloud: imported second batch of ATT images
* 12:28 SPF|Cloud: rebooted mw1. HHVM was not started automatically, so did this manually.
* 11:18 revi: restarted HHVM
* 08:56 JohnFLewis: restarted hhvm
* 04:33 revi: restarted HHVM, was generating 502

## 2015-09-26 

* 11:22 revi: imported izanagiwiki (/home/revi/dumps/izanagiwiki.xml) and ran rebuildrecentchanges.php
* 10:33 JohnFLewis: restarted MariaDB on db1
* 02:46 revi: permanentfuturelabwiki imported (yesterday, forgot to log)

## 2015-09-25 

* 16:45 SPF|Cloud: import of ATT images done
* 12:32 revi: php importImages.php --wiki poserdazfreebieswiki /home/southparkfan/poserdazfreebieswiki-images --skip-dupes JPG JPEG PNG SVG GIF gif svg png jpg jpeg
* 12:28 revi: php importImages.php --wiki poserdazfreebieswiki /home/revi/images/Images --skip-dupes JPG JPEG PNG SVG GIF gif svg png jpg jpeg
* 12:26 revi: php importImages.php --wiki poserdazfreebieswiki /home/revi/images/2 --skip-dupes JPG JPEG PNG SVG GIF gif svg png jpg jpeg

## 2015-09-24 

* 15:45 JohnFLewis: restarting MariaDB -- far too many searchindex crashes to work with

## 2015-09-23 

* 20:49 JohnFLewis: restart nginx to catch UA block for Wordpress -- will commit shortly
* 13:07 SPF|Cloud: MariaDB crashed; restarted it

## 2015-09-22 

* 20:55 JohnFLewis: purged bin logs on db1; gains ~20GB
* 18:48 SPF|Cloud: dropped ATT database
* 17:37 SPF|Cloud: ran removeDeletedWikis.php for ATT

## 2015-09-21 

* 18:34 SPF|Cloud: ran following query on ATT database: update revision set rev_user = 7, rev_user_text = 'DocColress' where rev_id = 303275;
* 15:49 JohnFLewis: restarted MariaDB on db1

## 2015-09-20 

* 09:25 SPF|Cloud: dropped allthetropeswiki database for import

## 2015-09-19 

* 22:33 SPF|Cloud: Poser and Daz Free Resources import running in screen now, this time without issues
* 22:29 SPF|Cloud: deleted poserdazfreebieswiki database, to make sure the import goes without issues.
* 22:22 SPF|Cloud: Poserdaz and Freebies Wiki import running in screen
* 19:26 SPF|Cloud: restarted ganglia-monitor on all servers
* 17:22 SPF|Cloud: ran importImages.php on 8stationwiki

## 2015-09-18 

* 20:52 SPF|Cloud: killed runJobs.php again
* 20:46 SPF|Cloud: killed the remaining instances of runJobs.php on mw1
* 20:43 SPF|Cloud: killed 4 instances of runJobs.php on mw1

## 2015-09-17 

* 22:31 JohnFLewis: backwards compatibility exists after a restart it seems
* 22:29 JohnFLewis: upgrading parsoid; serious lack of any documentation. complete removal of setInterwiki
* 00:08 JohnFLewis: quickly provisioned mw1 DDoS filtered IP

## 2015-09-16 

* 22:17 JohnFLewis: rebooted mw1, strange memory patterns

----
**Source**: [https://meta.miraheze.org/wiki/Tech:Server_admin_log/2015](https://meta.miraheze.org/wiki/Tech:Server_admin_log/2015)