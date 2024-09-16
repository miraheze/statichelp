---
title: Tech:Varnish
---

[Varnish](https://meta.miraheze.org/wiki/wikipedia:Varnish_(software)) is an HTTP cache proxy, which can serve almost anything (including articles) without asking the MediaWiki appservers.

Miraheze is currently migrating to [Cloudflare](https://meta.miraheze.org/wiki/Tech:Cloudflare) as a replacement for Varnish. Varnish currently only serves traffic for wikis on *.wikitide.org/*.wikitide.net wikis and for wikis that use Miraheze's DNS nameservers.

## Basics 

[right|200px|thumb|Miraheze server setup, showing Varnish in front of the MediaWiki appservers](https://meta.miraheze.org/wiki/File:Miraheze_server_setup.png)
Unlike webservers like Apache and NGINX, Varnish *only* caches stuff visited by people, and will pass uncacheable traffic (dynamic pages, e.g., when the user is logged in) to the MediaWiki appservers.

### Configuration 

The [default.vcl](https://github.com/miraheze/puppet/blob/master/modules/varnish/templates/default.vcl) file configures a lot of the stuff, but [/etc/default/varnish](https://github.com/miraheze/puppet/blob/master/modules/varnish/files/varnish/varnish.default) is also critical here. Some things can be done via CLI tools.

### How traffic goes through 

* Client asks [authoritative DNS](https://meta.miraheze.org/wiki/Tech:DNS) for the IP of a cache proxy. GeoDNS returns the IP of the nearest cache proxy, and the client will use that cache proxy server;
* NGINX runs on port 80 (for HTTPS redirect) and 443, terminating SSL/TLS. All traffic is passed to Varnish;
* Varnish will look if the object is (and can be) cached. If yes, traffic will be passed to stunnel (127.0.0.1:8080 for mw151, 127.0.0.1:8081 for mw152). stunnel is needed here because Varnish can't pass traffic to HTTPS backends, that's only for [users that pay](http://info.varnish-software.com/blog/flying-pigs-and-ssl-varnish-cache-plus).

### Using CLI tools 

#### varnishadm 

*Root privileges are required for this tool.*<br />
varnishadm is a tool that gives you an interactive (non-interactive is possible, but personally not preferred) shell prompt for managing the Varnish process. You can ban objects from the cache, show backends, view backend health, change backend health status and more.

#### varnishlog 

varnishlog is a tool that can be used to view real-time web requests. It's main advantages over standard access logs is that it doesn't require disk space, and you can view way more information (all client headers, detailed Varnish debug information, all backend headers, etc.).
Want to monitor all POST requests? `varnishlog -q "ReqMethod ~ POST"` does the trick. Do you want all cache MISSes? `varnishlog -q "VCL_call ~ MISS"` is all you need.

Or, what do you think about combining criteria: `varnishlog -q "ReqHeader:Host ~ allthetropes.org and ReqMethod ~ POST"`

Using the [VSL query language](https://www.varnish-cache.org/docs/4.0/reference/vsl-query.html) this tool is great for monitoring web requests.

#### varnishncsa 

varnishncsa is almost similiar to varnishlog, but it instead formats the output with the [common NCSA log format](https://en.wikipedia.org/wiki/Common_Log_Format), which is the same format used by default by (almost) all major webservers. Like varnishlog, this tool also accepts the VSL query language using the -q switch.

#### varnishstat 

TODO

## Headers and debugging 

### X-Cache 

On each web request by Varnish, we set an X-Cache header. It will look like:
```
X-Cache: cp26 HIT (5)
```
cp26 is the cache proxy who served the request, HIT indicates the request was served from the cache, (5) indicates the amount of times the object was accessed (so in this case the page was served from the cache for the 5th time). If the request was passed to the backend, the header would contain `MISS (0)` instead of `HIT (5)`. This could be useful to see if Varnish could have accidentally cached an error.

***Note: due to [a bug in Varnish](https://www.varnish-cache.org/trac/ticket/1492), obj.hits won't be reset after a ban was applied.***

### X-Miraheze-Debug 

Using the `X-Miraheze-Debug` header, you can force the request to be passed to a certain backend. For example, requests with the header `X-Miraheze-Debug: test151.wikitide.net` will always be passed (regardless of whether it could be served from the cache or not) to test151.

## One-off purges (bans) 

*Credit: [https://wikitech.wikimedia.org/wiki/Varnish](https://wikitech.wikimedia.org/wiki/Varnish)*<br />
Normally, MediaWiki will purge cache objects with the PURGE protocol. However, sometimes you want to purge more than object (or you want an easier way to purge objects across the fleet without using MediaWiki). This can be done using the [banning](https://www.varnish-cache.org/docs/4.0/users-guide/purging.html#bans) feature in varnishadm. Despite its scary name, banning only ensures that all cached objects matching the given criteria (e.g. req.http.Host == meta.miraheze.org) won't be used anymore.

Due to performance concerns, it's recommended that this feature is only used when needed. While Miraheze's appservers can handle the current amount of traffic (warning: this is a dangerous assumption), we should aim for the highest cache hit rate as possible.

While you can supply the ban command and its arguments directly as an argument to varnishadm, I recommend you just open the varnishadm shell prompt: `sudo varnishadm`

Every ban can be supplied with the "ban" command. **This must be done on all cache proxies.** Using the `==` (strict, no regex) and `~` (regex) operators, you can specify the criteria. For example: to ban all `/w/load.php` objects for allthetropes.org:
```
varnish> ban req.http.Host == allthetropes.org && req.url ~ "^/w/load.php"
```

If you remove the `req.http.Host == allthetropes.org && `&nbsp;part, this would match ALL load.php objects, regardless of the wiki.

Or, to remove ALL 301 redirects for meta.miraheze.org:
```
varnish> ban obj.status == 301 && req.http.Host == meta.miraheze.org
```

## Backend health checks 

Varnish uses a Miraheze-configured backend health check (called probes). For Miraheze, it checks (for each appserver) each 5 seconds if [https://meta.miraheze.org/wiki/Miraheze](https://meta.miraheze.org/wiki/Miraheze) loads under 4 seconds. If an appserver fails to serve that page under 4 seconds (or the response does not have HTTP status code 200) for at least 2 out of 5 times, it will be marked as sick, and it will be depooled automatically until it looks healthy again.

Using the `debug.health` and `backend.list` commands in varnishadm, you can view the current health of all appservers.

### Overriding health checks (e.g. depooling an appserver) 

Sometimes, you want to override the health checks, for example, because you want to depool an appserver.

Using the `backend.set_health` command, you can manage the health status of an appserver. For example, to depool mw151 (again, '''please ensure that you run this command on ALL cache proxies):
```
varnish> backend.set_health mw151 sick
```

This will mark the backend as sick (= depooled), and it will stay depooled regardless of the health checks, as long as Varnish wouldn't be restarted (or the health set to good again).

If the health status of the backend should depend on the health checks (i.e., maintenance completed, appserver can be repooled), set the health status to auto:
```
varnish> backend.set_health mw151 auto
```

This allows Varnish probes to manage the backend health state again.

## External links 

* [Varnish 5.0 documentation](https://www.varnish-cache.org/docs/5.0/)

----
**Source**: [https://meta.miraheze.org/wiki/Tech:Varnish](https://meta.miraheze.org/wiki/Tech:Varnish)