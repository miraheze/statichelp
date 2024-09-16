---
title: Tech:Cloudflare
---

Miraheze is in the process of migrating to Cloudflare as a replacement of [Varnish](Tech:Varnish.md).

Currently, wikis on all Miraheze-owned domains (except for *.wikitide.net/*.wikitide.org) and custom domain wikis not using Miraheze's DNS servers (but rather [CNAME](https://meta.miraheze.org/wiki/w:CNAME)s or [ANAME](https://meta.miraheze.org/wiki/w:ANAME)s) use Cloudflare.

## Load balancing

MediaWiki traffic is load balanced by Cloudflare on all subdomains of miraheze.org that don't have a record in the DNS, which is all of them except issue-tracker, blog, and reports.

There's only one pool configured, `FiberState-MediaWiki`, with all mw* servers added to it. Cloudflare monitors the health of all endpoints by calling `https://health.wikitide.net/check` on all of them every 60 seconds looking for a 204 response code. It will email cf-admins `{{ {{@}} }}`wikitide.org if any servers fail the check.

Keep in mind that this check is done over HTTPS and that Cloudflare is verifying the certificate, so the check will not only fail if the server does not return a 204, but also if it has an expired wikitide.net certificate.

### Adding new endpoints

* Go to Websites -> miraheze.org -> Traffic-> Load Balancing. This page has the load balancing configuration.
* Click on the dropdown for `*` and edit the `FiberState-MediaWiki` pool.
* Go to the end of the endpoints section, and click "Add Endpoint". Input the server name, public IPv6 address and a weight of 1, **unless** you have a reason to give it a separate weight value.
* Click save at the bottom of the page and you're done.

----
**Source**: [https://meta.miraheze.org/wiki/Tech:Cloudflare](https://meta.miraheze.org/wiki/Tech:Cloudflare)