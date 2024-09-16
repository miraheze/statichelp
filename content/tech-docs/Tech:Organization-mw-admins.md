---
title: Tech:Organization/mw-admins
---

This is a guide for all MediaWiki admins. MediaWiki admins have access to Miraheze servers: [mw151](https://meta.miraheze.org/wiki/Tech:Mw151), [mw152](https://meta.miraheze.org/wiki/Tech:Mw152), [mw161](https://meta.miraheze.org/wiki/Tech:Mw161), [mw162](https://meta.miraheze.org/wiki/Tech:Mw162), [mw171](https://meta.miraheze.org/wiki/Tech:Mw171), [mw172](https://meta.miraheze.org/wiki/Tech:Mw172), [mw181](https://meta.miraheze.org/wiki/Tech:Mw181), [mw182](https://meta.miraheze.org/wiki/Tech:Mw182), [mwtask171](https://meta.miraheze.org/wiki/Tech:Mwtask171), [mwtask181](https://meta.miraheze.org/wiki/Tech:Mwtask181), [test151](https://meta.miraheze.org/wiki/Tech:Test151), and [jobchron171](https://meta.miraheze.org/wiki/Tech:Jobchron171).

In case of any doubts regarding a command or configuration change, mw-admins should ask either another mw-admin, or Site Reliability Engineering before going through with it. In addition, mw-admins should test any new changes on test151 before adding them to production.

## Rules 

* Be respectful to other volunteers and users. You represent the Miraheze project.
* Don't suddenly change big parts of the MediaWiki infrastructure (e.g., way how things are done in the current style) without discussing it with the other sysadmins.
* Don't use the servers for non-Miraheze purposes.
* Don't put abnormally high load(s) on the server(s) if avoidable. ([Grafana](https://meta.miraheze.org/wiki/Tech:Grafana) can be used for more details)
* Respect privacy. Don't publish access logs, IP addresses, content of private wikis, or other personally identifiable information. *If in doubt, ask before publishing. Publishing any such content is likely to be a violation of your non-disclosure agreement (NDA) with the WikiTide Foundation, or Miraheze Limited if your NDA predates the merger.*
* Don't publish database passwords, private keys, etc as well.
* When in doubt, ask questions first, act second.
 `{{ {{note}} }}` Violation of these rules can result in warnings or revocation of access.

## Maintenance scripts 

* They should typically only be run on mwtask181 or mwtask171.
* Always run them as www-data (prefix command with `sudo -u www-data`).
* Always `!log` maintenance script runs in #miraheze-tech-ops (unless you were running puppet or were using sql.php, and did **not** execute any queries that changed the database (e.g. SELECT/DESCRIBE queries)
   * You can optionally use the [mwscript](https://meta.miraheze.org/wiki/Tech:MediaWiki_appserver#mwscript) wrapper to automatically log these.
* If you need to run a script on all wikis, use the *foreachwikiindblist* wrapper:
* `sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/databases.json /srv/mediawiki/<version>/maintenance/yourscript.php --put-your-parameters --here`
* update.php is evil. If you need to run it while you're not doing a MediaWiki upgrade, then something is really wrong.
   * maintenance/update.php just automatically creates all required database tables on the wiki(s) it is run on. SQL files should be added to the CreateWiki config setting so that tables are automatically added to all new wikis. See [Tech:Adding a new extension](https://meta.miraheze.org/wiki/Tech:Adding_a_new_extension) for enabling extensions or adding tables to existing wikis.
### Accessing the mhglobal database 

If you need to do work on the `mhglobal` database (where the CentralAuth and OATHAuth tables are, among others), but you don't have access to the db* servers, the recommended way is to run `sql.php` with `loginwiki` as the wiki and give it the `--wikidb=mhglobal` option. You'll then have access to `mhglobal`.

## Installing and enabling new extensions 

See [Tech:Adding a new extension](https://meta.miraheze.org/wiki/Tech:Adding_a_new_extension).

## Pushing configuration changes 

* Ensure the PHP syntax is correct, you want to avoid deploying files with syntax errors.
   * Although everyone makes mistakes sometimes, try to avoid them in the first place and be aware of how the changes you make can affect the entire site.
   * If a syntax error should occur, push a fixing-commit to the repo(s) and manually run puppet (`sudo puppet agent -t`) on mwtask181.
* When a configuration variable is changed, you should be completely aware what it does, and how it could impact a wiki security-wise.
* There is more stuff in LocalSettings.php than just configuration variables, like [this](https://github.com/miraheze/mw-config/blob/d9b720ba7a19fd77d7dc7c08a9e3f640cb6c9b0f/LocalSettings.php#L2905-L3028). You are allowed to edit such stuff, but if you are not familiar with its functionality, it's not recommended to touch it (or to merge pull requests that make changes to this area).
See [#Deployment](#Deployment) for the rest.

## Deployment 

* When deploying a configuration change or extension, you are **required** to closely watch the change going live.
* After committing a change to the mediawiki or mw-config repo (and being sure it should work), run `sudo puppet agent -t` on mwtask181. It can take a while before the change is actually deployed.
* Watch the error logs: [#Monitoring errors](#Monitoring errors).

## Monitoring errors 

Follow the instructions at [Tech:Graylog](https://meta.miraheze.org/wiki/Tech:Graylog).

## Debugging 

* Look at the [error logs](#Monitoring errors).
* Try to send the failing HTTP request to one of the mw servers with the header `X-Miraheze-Debug: (mw1[5678][12]|test151|mwtask181).wikitide.net` (replace with the desired server), it could be an error that is cached in Varnish.

[Category:Technology guidelines and guides](https://meta.miraheze.org/wiki/Category:Technology_guidelines_and_guides)

----
**Source**: [https://meta.miraheze.org/wiki/Tech:Organization/mw-admins](https://meta.miraheze.org/wiki/Tech:Organization/mw-admins)