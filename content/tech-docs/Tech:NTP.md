---
title: Tech:NTP
---

We use ntpsec to handle our time sync needs across our infra.

## Hacks

Our current deployment is based around the [ntp Puppetlabs module](https://meta.miraheze.org/wiki/github:puppetlabs/puppetlabs-ntp), which is built around Debian Bullseye still as of writing. Thus, it assumes the daemon is the classic NTP daemon, which is not true in Debian Bookworm, which uses ntpsec instead.

Fortunately, [we only need to change a few of the defaults for ntpsec support](https://meta.miraheze.org/wiki/github:miraheze/puppet/commit/1d346d527cee748aa22e9d0bd3b3ec501ce4fbb7). We should monitor development of the module upstream in case these modifications are no longer needed in a future release.



----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:NTP)**