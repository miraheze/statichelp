---
title: Tech:Icinga/MediaWiki Monitoring
---

This page is used to provide monitoring guidance for MediaWiki-related services if an alert goes off.

## JobChron Service 

* *Why does this check exist? What does it monitor?***This check monitors whether the JobChron service is up and running.**
* *Is an alert a bad thing?***Yes, JobChron should always be running on the redis servers.**
* *If its warning/critical, how do we fix it?***It may be possible to resolve by either manually starting the JobChron service (`sudo service jobchron start`), or restarting it (`sudo service jobchron restart`). You can also try and see why it failed to start by viewing the service status (`sudo service jobchron status`). If you don't have access to the relevant server(s), a task on Phorge should be filed and those with access should be alerted to be able to assist.**

## Redis Service 

* *Why does this check exist? What does it monitor?***This check simply monitors whether the Redis service is up and running.**
* *Is an alert a bad thing?***Yes, Redis should always be running.**
* *If it's warning/critical, how do we fix it?***A task on Phorge should be filed immediately and everyone (including Infrastructure) should be pinged to investigate why it is down and resolve.**

## PHP-FPM 

* *Why does this check exist? What does it monitor?***This check monitors whether PHP-FPM processes are up and running.**
* *Is an alert a bad thing?***Yes, PHP-FPM should always be running.**
* *If it's warning/critical, how do we fix it?***It may be possible to resolve by either manually starting the php-fpm service (`sudo service php-fpm start`), or restarting it (`sudo service php-fpm restart`). You can also try and see why it failed to start, by viewing the service status (`sudo service php-fpm status`). If you are unable to resolve the issue, then a Phorge task, triaged as "Unbreak Now" should be filed, and the relevant technical team members alerted to assist. If this alert is given, chances are users may receive errors on their end with PHP-FPM down. If that's the case, an incident report should also be filed for the issue.**

## Memcached 

* *Why does this check exist? What does it monitor?***This check simply monitors whether the memcached service is up and running.**
* *Is an alert a bad thing?***Yes, memcached should always be running.**
* *If it's warning/critical, how do we fix it?***A Phorge task should be created, triaged as "Unbreak Now" until the issue is resolved. While in theory the MediaWiki Team manages, since only Reception123 has access, Infrastructure should also be alerted to be able to assist.**

## Nutcracker 

* *Why does this check exist? What does it monitor?***This check monitors whether the nutcracker service is running.**
* *Is an alert a bad thing?***Yes, nutcracker should always be running.**
* *If it's warning/critical, how do we fix it?***It may be possible to resolve by either manually starting the nutcracker service (`sudo service nutcracker start`), or restarting it (`sudo service nutcracker restart`). You can also try to see why it failed to start, by viewing the service status (`sudo service nutcracker status`). If you are unable to immediately resolve this, a Phorge task should be created, triaged as "Unbreak Now" until the issue is resolved.**

## JobRunner Service 

* *Why does this check exist? What does it monitor?***This check monitors whether the jobrunner process is running correctly.**
* *Is an alert a bad thing?***Yes, unless done intentionally by a member of SRE, jobrunner should be running on all designated servers at all times.**
* *If it's warning/critical, how do we fix it?***If the jobrunner is not running on a server, it can be restarted by doing `sudo service jobrunner restart`. If there is an error when restarting, that must be investigated. You can try to see what error occured using `sudo service jobrunner status`.**

## MediaWiki Rendering 

* *Why does this check exist? What does it monitor?***This check monitors whether MediaWiki is accessible.**
* *Is an alert a bad thing?***Yes, it means MediaWiki may be down, and users may be receiving errors on their end.**
* *If it's warning/critical, how do we fix it?***If the issue persists and users are reporting errors such as 502 or 503, then a Phorge task should be created, triaged as "Unbreak Now" until the issue is resolved for users. To attempt to resolve it, restarting PHP-FPM (`sudo service php8.2-fpm restart`) could help under some circumstances. If you have root access, you could also try restarting the relevant server(s). If that still doesn't work, try looking at logs, to determine the cause of the outage. Chances are it will resolve itself after some time if you're unable to. If the outage was user-facing, an incident report should also be filed for it.**

## WikiTideRenewSSL 

* *Why does this check exist? What does it monitor?***This check monitors whether the SSL renewal services is up and running.**
* *Is an alert a bad thing?***Yes, this must be investigated.**
* *If it's warning/critical, how do we fix it?***If the service is down it should be restarted. If it cannot be restarted/is not functional, that should be further investigated.**

## SSL Validity Checks 

* *Why does this check exist? What does it monitor?***This check monitors whether SSL certificates are set to expire in the next 15 days.**
* *Is an alert a bad thing?***Usually no, WikiTideSSLBot will renew non-wildcard certs. If it is CRITICAL, however, there might be a problem with the bot, so that needs reporting.**
* *If it's warning/critical, how do we fix it?***If it is critical (and non-wildcard) the reason for why the bot is not auto-generating should be investigated. If it cannot be figured out in time, the certs should be [manually renewed](/tech-docs/techssl_certificates.md). For wildcards certs, they need to be renewed manually in any case once there is a warning.**

## Reverse DNS Checks 

* *Why does this check exist? What does it monitor?***This check performs a reverse DNS lookup to determine domains that have been pointed to us are still pointing to us**
* *Is an alert a bad thing?***Yes, if not just a temporary issue that resolves itself, it is a problem.**
* *If it's warning/critical, how do we fix it?***The person who requested the custom domain (or other wiki bureaucrats) should be notified and asked to point their domains to us again. If there is no response and/or they fail to do so in a reasonable time (not less than a week) the custom domain and SSL certificate should be removed until the issue is resolved.**

[Category:Technology guidelines and guides](https://meta.miraheze.org/wiki/Category:Technology_guidelines_and_guides)

----
**Source**: [https://meta.miraheze.org/wiki/Tech:Icinga/MediaWiki_Monitoring](https://meta.miraheze.org/wiki/Tech:Icinga/MediaWiki_Monitoring)