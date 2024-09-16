---
title: Tech:DNS
---

Miraheze's DNS is self-hosted, on two servers: [ns1](https://meta.miraheze.org/wiki/Tech:Ns1) and [ns2](https://meta.miraheze.org/wiki/Tech:Ns2). [GDNSD](//github.com/gdnsd/gdnsd) is the software used for this task, and we chose it because GDNSD is open-source, fast, and easy.

## Configuration 

Our GDNSD configuration can be found at [GitHub](//github.com/miraheze/dns), and can be edited by staff with global root access. That doesn't mean though no one can improve our configuration because everyone is welcome to create pull requests.

### config 

[config](https://github.com/miraheze/dns/blob/master/config) is the file that contains GDNSD configuration. There is a stanza in it that can be used to load balance the main traffic to multiple servers (e.g. servers running HAProxy). More information about the available options in this file can be found [here](https://github.com/gdnsd/gdnsd/wiki/GdnsdConfig).

### zones 

DNS records (for one domain name) are stored in a zone (e.g. https://raw.githubusercontent.com/miraheze/dns/master/zones/wikitide.net).

## Deployment 

Code is deployed automatically through puppet. This allows code to be merged and put into production within a short time frame and aids quick development cycles as the TTL means a record can be live within 15 minutes to all users. This does, however, bring issues in that deployment is not monitored and a failure (whilst very visible) can cause service issues.

The system should be moved to manual at some point, though there is not enough risk to justify this yet.

[Category:Services](https://meta.miraheze.org/wiki/Category:Services)

----
**Source**: https://meta.miraheze.org/wiki/Tech:DNS