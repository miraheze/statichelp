---
title: Tech:Nginx
---

[NGINX](https://nginx.org/en/) is a high-performance web server which [Miraheze](https://meta.miraheze.org/wiki/Miraheze) uses for all of our services that use HTTP.

## Adding a new site 

Adding a new site to NGINX is relatively easy but also depends on what you want to do.

### New Site 

To add a new site, you add a .conf file in `/etc/nginx/sites-available/<name>.conf` and then symlink `/etc/nginx/sites-enabled/<name>.conf to` `/etc/nginx/sites-available/<name>.conf`

With the contents:

(This redirects from domain a to domain b)

```
server {
	listen 80;
	listen [::]:80;
	listen 443 ssl http2;
	listen [::]:443 ssl http2;

	server_name <site_name>;
	root <path>;

	ssl_certificate <cert>;
	ssl_certificate_key <cert>;

	ssl_trusted_certificate /etc/ssl/certs/GlobalSign.crt; # path to trusted certificate

	add_header Strict-Transport-Security "max-age=2419200";

	location / {
		rewrite ^(.*)$ https://<domain>$1;
	}
}
```

## Debugging 

Debugging NGINX can be configured in multiple ways.

### Syntax Checking 

To check nginx syntax you run:

`nginx -t`

Which tells you if the syntax passes.

### Access Logs 

The access logs are useful to tell you either if someone is causing huge traffic to the site or which URL is failing.

You can view the access log at:

`/var/log/nginx/access.log`

### Error Log 

The error log is located at by default:

`/var/log/nginx/error.log`

You can configure the error log to include debugging information by doing:

`error_log /var/log/nginx/error.log debug;`

## Finding out resource abuse 

You can do the following:

`cat access.log | awk '{print $1}' | sort | uniq -c | sort -nr |head -3`

Which will print the most frequent IP and how many times it's listed. This will give you an indicator if someone is abusing the resources (You should check the User Agent too).

You can also cat the access log (or varnish log) to see if there's a pattern (e.g a specific URL showing up more than once, or user agent).

## See Also 

* [Debugging NGINX](https://docs.nginx.com/nginx/admin-guide/monitoring/debugging/)

[Category:Services](https://meta.miraheze.org/wiki/Category:Services)

----
**Source**: [https://meta.miraheze.org/wiki/Tech:Nginx](https://meta.miraheze.org/wiki/Tech:Nginx)