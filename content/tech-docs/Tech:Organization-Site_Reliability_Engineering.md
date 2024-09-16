---
title: Tech:Organization/Site Reliability Engineering
---

This is a guide for all Miraheze Site Reliability Engineers. They have access to Miraheze servers and to Miraheze GitHub repositories (see [Tech:SRE Volunteers](https://meta.miraheze.org/wiki/Tech:SRE_Volunteers)), and they are responsible for maintaining all Miraheze servers and making sure they function smoothly.

## Rules 

* Be respectful to other volunteers and users. You represent the Miraheze project.
* Don't suddenly change big parts of the infrastructure (MediaWiki, Varnish, Bacula, etc.) (e.g., way how things are done in the current style) without discussing it with the other site reliability engineers (and any sysadmins).
* Be **VERY** careful when manipulating sensitive data (such as db* or nfs*) as it could lead to data loss.
* Don't use the servers for non-Miraheze purposes.
* Don't put abnormally high load(s) on the server(s) if avoidable. ([Grafana](Tech:Grafana.md) can be used for more details).
* Respect privacy. Don't publish access logs, IP addresses, content of private wikis, or other personally identifiable information. If in doubt, ask before publishing.
* Don't publish database passwords, private keys, etc as well.
 `{{ {{note}} }}` Violation of these rules can result in warnings or revocation of access.

## Deployment 

* When deploying a change (SSL certificate, database rename, etc.), you are **required** to closely watch the change going live.
* After committing a change to any repo (and being sure it should work), run `sudo puppet agent -tv` on the server involved. It can take a while before the change is actually deployed.
* Watch the error logs: [#Monitoring errors](#Monitoring errors).

*Further specifics to be filled in by SRE*

## Monitoring errors 

*To be filled in for specific servers*

## Debugging 

* Look at the [error logs](#Monitoring errors).
* Try to send the failing HTTP request with the header `X-WikiTide-Debug: 1`, it could be an error that is cached in Varnish.

## See also 

* [mw-admins guide](Tech:Organization-mw-admins.md)

[Category:Technology guidelines and guides](https://meta.miraheze.org/wiki/Category:Technology_guidelines_and_guides)

----
**Source**: [https://meta.miraheze.org/wiki/Tech:Organization/Site_Reliability_Engineering](https://meta.miraheze.org/wiki/Tech:Organization/Site_Reliability_Engineering)