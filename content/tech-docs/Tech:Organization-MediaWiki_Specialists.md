---
title: Tech:Organization/MediaWiki Specialists
---

This is a guide for all [MediaWiki Specialists](/tech-docs/techorganization#mediawiki-specialist). MediaWiki Specialists have access to servers: [mw151](/tech-docs/techmw151), [mw152](/tech-docs/techmw152), [mw153](https://meta.miraheze.org/wiki/Tech:Mw153), [mw154](https://meta.miraheze.org/wiki/Tech:Mw154), [mw161](/tech-docs/techmw161), [mw162](/tech-docs/techmw162), [mw163](https://meta.miraheze.org/wiki/Tech:Mw163), [mw164](https://meta.miraheze.org/wiki/Tech:Mw164), [mw171](/tech-docs/techmw171), [mw172](/tech-docs/techmw172), [mw173](https://meta.miraheze.org/wiki/Tech:Mw173), [mw174](https://meta.miraheze.org/wiki/Tech:Mw174), [mw181](/tech-docs/techmw181), [mw182](/tech-docs/techmw182), [mw183](https://meta.miraheze.org/wiki/Tech:Mw183), [mw184](https://meta.miraheze.org/wiki/Tech:Mw184), [mwtask151](https://meta.miraheze.org/wiki/Tech:Mwtask151), [mwtask161](https://meta.miraheze.org/wiki/Tech:Mwtask161), [mwtask171](/tech-docs/techmwtask171), [mwtask181](/tech-docs/techmwtask181), [test151](/tech-docs/techtest151), and [jobchron171](/tech-docs/techjobchron171)

In case of any doubts regarding a command or configuration change, MediaWiki Specialists should ask either another member of the [Technology team](/tech-docs/techvolunteers) before going through with it. In addition, MediaWiki Specialists should test any new changes on test151 before adding them to production.

## Rules 

   *See also: [Tech:Conduct Policy](/tech-docs/techconduct_policy)*

* Be respectful to other volunteers and users. You represent the project.
* Don't suddenly change big parts of the MediaWiki infrastructure (e.g., way how things are done in the current style) without discussing it with the other members of the Technology team.
* Don't use the servers for unrelated purposes.
* Don't put abnormally high load(s) on the server(s) if avoidable. ([Grafana](/tech-docs/techgrafana) can be used for more details)
* Respect privacy. Don't publish access logs, IP addresses, content of private wikis, or other personally identifiable information. *If in doubt, ask before publishing. Publishing any such content is likely to be a violation of your non-disclosure agreement (NDA) with the WikiTide Foundation.*
* Don't publish database passwords, private keys, etc as well.
* When in doubt, ask questions first, act second.
 `{{ {{note}} }}` Violation of these rules can result in warnings or revocation of access.

## Maintenance scripts 

* They should typically only be run on an mwtask server.
* Always run them as www-data (prefix command with `sudo -u www-data`).
* Always `!log` maintenance script runs in #miraheze-tech-ops (unless you were running puppet or were using sql.php, and did **not** execute any queries that changed the database (e.g. SELECT/DESCRIBE queries)
   * You can optionally use the [mwscript](/tech-docs/techmediawiki_appserver#mwscript) wrapper to automatically log these.
* If you need to run a script on all wikis, use the *foreachwikiindblist* wrapper:
* `sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/databases.json /srv/mediawiki/<version>/maintenance/yourscript.php --put-your-parameters --here`
* update.php is evil. It should absolutely never be ran in production.
   * SQL files should be added to the CreateWiki config setting so that tables are automatically added to all new wikis. See [Tech:Adding a new extension](/tech-docs/techadding_a_new_extension) for enabling extensions or adding tables to existing wikis.

### Accessing the mhglobal database 

If you need to do work on the `mhglobal` database (where the CentralAuth and OATHAuth tables are, among others), but you don't have access to the db* servers, the recommended way is to run `sql.php` with `loginwiki` as the wiki and give it the `--wikidb=mhglobal` option. You'll then have access to `mhglobal`.

## Installing and enabling new extensions 

See [Tech:Adding a new extension](/tech-docs/techadding_a_new_extension).

## Pushing configuration changes 

* Ensure the PHP syntax is correct, you want to avoid deploying files with syntax errors.
   * Although everyone makes mistakes sometimes, try to avoid them in the first place and be aware of how the changes you make can affect the entire site.
   * If a syntax error should occur, push a fixing-commit to the repo(s) and manually run [mwdeploy](/tech-docs/techmwdeploy) or [puppet](/tech-docs/techpuppet) (`sudo puppet agent -tv`) on mwtask181.
   * The CIs will almost always catch the more simple syntax errors as well, so it is recommended to let those finish before pushing commits.
* When a configuration variable is changed, you should be completely aware what it does, and how it could impact a wiki security-wise.
* There is more stuff in LocalSettings.php than just configuration variables, like [this](https://github.com/miraheze/mw-config/blob/d9b720ba7a19fd77d7dc7c08a9e3f640cb6c9b0f/LocalSettings.php#L2905-L3028). You are allowed to edit such stuff, but if you are not familiar with its functionality, it's not recommended to touch it (or to merge pull requests that make changes to this area).
See [#Deployment](#deployment) for the rest.

## Deployment 

* When deploying a configuration change or extension, you are **required** to closely watch the change going live.
* After committing a change to the mediawiki or mw-config repo (and being sure it should work), run `mwdeploy --config --pull=config --servers=all` or `sudo puppet agent -tv` on mwtask181. It can take up to 30 minutes before the change is actually deployed automatically.
* Watch the error logs: [#Monitoring errors](#monitoring-errors).

## Monitoring errors 

Follow the instructions at [Tech:Graylog](/tech-docs/techgraylog).

## Debugging 

* Look at the [error logs](#monitoring-errors).
* Either use the [WikiTideDebug](https://github.com/miraheze/WikiTideDebug) extension for Chrome or try to send the failing HTTP request to one of the MediaWiki servers with the header `X-WikiTide-Debug: (mw1[5678][1234]|test151|mwtask1[5678]1).wikitide.net` (replace with the desired server), it could be an error that is cached in [Varnish](/tech-docs/techvarnish) or [Cloudflare](/tech-docs/techcloudflare).
   * `X-WikiTide-Debug` also requires an access key sent via `X-WikiTide-Debug-Access-Key`, unless the request is made from a server from our own internal infrastructure (from one of our own IP ranges). If you don't have this access key, please ask another member of the Technology team.
* You can also use the [MediaWikiDebugJS](https://github.com/miraheze/MediaWikiDebugJS) extension for Chrome to debug MediaWiki response times, or what backend MediaWiki and/or cache proxy servers you are connecting to.

## Categories

* [Category:Technology guidelines and guides](https://meta.miraheze.org/wiki/Category:Technology_guidelines_and_guides)



----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:Organization/MediaWiki_Specialists)**