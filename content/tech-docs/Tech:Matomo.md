---
title: Tech:Matomo
---

**Matomo** is a free, open-source software used for analytics, which is running on [matomo151](/tech-docs/techmatomo151.md). It can be found at [https://analytics.wikitide.net](https://analytics.wikitide.net).

Currently, the only people who have access to Matomo are the [Technology team](/tech-docs/techvolunteers.md) members, who each have an individual account. However, we also use Matomo with an extension called MatomoAnalytics which provides the "Special:Analytics" which is publicly accessible.

## Disabling 2FA 

To disable 2FA on a specific user account, ssh into matomo151 and run the following from `/srv/matomo/`:

`./console twofactorauth:disable-2fa-for-user --login=<user>`

[Category:Services](https://meta.miraheze.org/wiki/Category:Services)

----
**Source**: [https://meta.miraheze.org/wiki/Tech:Matomo](https://meta.miraheze.org/wiki/Tech:Matomo)