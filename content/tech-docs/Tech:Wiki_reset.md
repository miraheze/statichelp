---
title: Tech:Wiki reset
---

A wiki can be reset with the following command on a MediaWiki task server.
```bash
mwscript MirahezeMagic:ResetWiki loginwiki --dbname=<database name> --requester=<username of requesting bureaucrat>
```
A wiki reset often comes with strange errors. Some common issues and solutions are documented below:
* [Tech:Fixing slot roles and content models](/tech-docs/techfixing_slot_roles_and_content_models)
* [Tech:Matomo](/tech-docs/techmatomo)
* Swift backend error. Run `CreateWiki:SetContainersAccess`.

----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:Wiki_reset)**