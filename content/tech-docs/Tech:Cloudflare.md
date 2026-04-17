---
title: Tech:Cloudflare
---

Miraheze is in the process of migrating to Cloudflare as a replacement of [Varnish](/tech-docs/techvarnish).

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

## Caching

Cloudflare's cache rules are stackable, from [the documentation](https://developers.cloudflare.com/cache/how-to/cache-rules/order/):

If several matching rules set a value for the same setting, the value in the last matching rule wins.
For conflicting settings (for example, bypass cache versus eligible for cache), the last matching rule wins.

Therefore, the first rule always says bypass cache for all pages so that nothing is cached unless an explicit rule says otherwise . A rule in the middle (call it M) says bypass cache for logged-in users. Any caching rule that goes above M will only be applied to logged-out users because the cache status of logged-in requests will always be set to no cache once they reach M. Any caching rule that goes below M will be applied to all users. The latter should be used with extreme caution: only requests whose reponse will absolutely not change depending on login status should be cached for everyone.

If a response that depends on user input is accidentally cached, bump `wgAuthenticationTokenVersion` in mw-config by 1 and run `CentralAuth:resetGlobalUserTokens`. This logs everyone out of CentralAuth.

----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:Cloudflare)**