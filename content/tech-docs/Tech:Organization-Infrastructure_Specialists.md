---
title: Tech:Organization/Infrastructure Specialists
---

This is a guide for all [Infrastructure Specialists](/tech-docs/techorganization#infrastructure-specialist). They have access to all servers and GitHub repositories (see [Tech:Volunteers](/tech-docs/techvolunteers)), and they are responsible for maintaining all servers and internal infrastructure and making sure they function smoothly.

## Rules 

   *See also: [Tech:Conduct Policy](/tech-docs/techconduct_policy)*

* Be respectful to other volunteers and users. You represent the Miraheze project.
* Don't suddenly change big parts of the infrastructure (MediaWiki, Varnish, Bacula, etc.) (e.g., way how things are done in the current style) without discussing it with the other members of the Technology team.
* Be **VERY** careful when manipulating sensitive data (such as db* or nfs*) as it could lead to data loss.
* Don't use the servers for unrelated purposes.
* Don't put abnormally high load(s) on the server(s) if avoidable. ([Grafana](/tech-docs/techgrafana) can be used for more details).
* Respect privacy. Don't publish access logs, IP addresses, content of private wikis, or other personally identifiable information. If in doubt, ask before publishing. Publishing any such content is likely to be a violation of your non-disclosure agreement (NDA) with the WikiTide Foundation.
* Don't publish database passwords, private keys, etc as well.
 `{{ {{note}} }}` Violation of these rules can result in warnings or revocation of access.

## Deployment 

* When deploying a change (SSL certificate, database rename, etc.), you are **required** to closely watch the change going live.
* After committing a change to any repo (and being sure it should work), run `sudo puppet agent -tv` on the server involved. It can take a while before the change is actually deployed.
* Watch the error logs: [#Monitoring errors](#monitoring-errors).

*Further specifics to be filled in by Technology team*

## Monitoring errors 

Follow the instructions at [Tech:Graylog](/tech-docs/techgraylog) for most errors.

## Debugging 

* Look at the [error logs](#monitoring-errors).
* Either use the [WikiTideDebug](https://github.com/miraheze/WikiTideDebug) extension for Chrome or try to send the failing HTTP request to one of the MediaWiki servers with the header `X-WikiTide-Debug: (mw1[5678][1234]|test151|mwtask1[5678]1).wikitide.net` (replace with the desired server), it could be an error that is cached in [Varnish](/tech-docs/techvarnish) or [Cloudflare](/tech-docs/techcloudflare).
   * `X-WikiTide-Debug` also requires an access key sent via `X-WikiTide-Debug-Access-Key`, unless the request is made from a server from our own internal infrastructure (from one of our own IP ranges). If you don't have this access key, please ask another member of the Technology team.

## See also 

* [MediaWiki Specialists guide](/tech-docs/techorganization-mediawiki_specialists)

## Categories

* [Category:Technology guidelines and guides](https://meta.miraheze.org/wiki/Category:Technology_guidelines_and_guides)

----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:Organization/Infrastructure_Specialists)**