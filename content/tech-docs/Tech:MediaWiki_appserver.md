---
title: Tech:MediaWiki appserver
---

**MediaWiki application servers** (MediaWiki appserver) is a name given to the stack of software that runs Miraheze wikis. It is made up of several components.

## Maintenance scripts 

Maintenance scripts are used for a variety of different things: imports, maintenance, updating stats, migrations, etc. MediaWiki maintenance scripts are found in `/srv/mediawiki/<version>/maintenance`. MediaWiki maintenance scripts are not the only ones; however, some extensions have their own maintenance scripts which are usually found under `/srv/mediawiki/<version>/extension/[Name]/maintenance`. They should be run on either one of the jobrunner servers.

A full list of maintenance scripts can be found [here](https://meta.miraheze.org/wiki/mediawikiwiki:Manual:Maintenance_scripts#List_of_maintenance_scripts). Below are the maintenance scripts that are most frequently used on Miraheze. Other frequently used maintenance scripts can be found in the specific guides below.

* **importDump.php** – Allows sysadmins to import XML dumps that are too large for Special:Import on-wiki.
   * `sudo -u www-data php /srv/mediawiki/<version>/maintenance/importDump.php --wiki=examplewiki /home/<user>/dump.xml`
   * `--username-prefix "interwiki"` should be used for interwiki imports for proper attribution.

* **initSiteStats.php** – If Special:Statistics isn't updating properly, it's useful to run this.
   * `sudo -u www-data php /srv/mediawiki/<version>/maintenance/initSiteStats.php --update --wiki examplewiki`

* **deleteBatch.php** – To delete a large number of pages based on a text file.
   * ` sudo -u www-data php /srv/mediawiki/<version>/maintenance/deleteBatch.php --wiki=examplewiki --r "[[phab:Txxx|Requested]]" /home/<user>/deletebatch.txt`

* **assignImportedEdits.php** – To reassign contributions for imported users to their Miraheze username.
   * ` sudo -u www-data php /srv/mediawiki/<version>/extensions/MirahezeMagic/maintenance/assignImportedEdits.php --wiki=examplewiki --import-prefix="prefix" --from=import_username`
   * Prefix is without the suffixed `>`.
   * `--from` is the imported username without the prefix.
   * If the imported username is different from the Miraheze username, specify `--to=miraheze_username`
   * If only `--to` is specified, all users with the import prefix would be assigned to the given user.
   * If neither `--to` nor `--from` is given, all users with the given prefix would be assigned to the same username on Miraheze, stripped of the prefix, if the username exists.
   * You should always verify what will be run first by using `--no-run` and verifying the output first.

* **sql.php** – Self explanatory; to run SQL commands.

* **shell.php** – Evaluation of MediaWiki objects and functions.

### foreachwikiindblist 

**Foreachwikiindblist** allows for a maintenance script to be run on all Miraheze wikis.

Usage: ` sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/databases.json /srv/mediawiki/<version>/maintenance/example.php`

### mwscript 

**mwscript** allows for faster running of maintenance scripts and automatic logging. You must type 'Y' and press enter to execute.

* In 1.40 and above, specify `--use-runner` or `--140`
* Usage: `mwscript initSiteStats.php examplewiki --update` to run `sudo -u www-data php /srv/mediawiki/<version>/maintenance/initSiteStats.php --wiki=examplewiki --update`
* Usage: `mwscript extensions/example/script.php examplewiki --extra=blah` to run `sudo -u www-data php /srv/mediawiki/<version>/extensions/example/maintenance/script.php --wiki=examplewiki --extra=blah`
* Usage: `mwscript extensions/example/script.php examplewiki --extra=blah "'/path/to/file'"` to run `sudo -u www-data php /srv/mediawiki/<version>/extensions/example/maintenance/script.php --wiki=examplewiki --extra=blah '/path/to/file'`
 `{{ {{note|Important:}} }}` Note the order of `"'` in the above usage example.

## Jobrunner 

The mwtask servers are responsible for running jobs on MediaWiki. As mentioned above, maintenance scripts should be run on this server.

* To see how many jobs are currently waiting to be run on a wiki, you can use the **showJobs.php** maintenance script (`sudo -u www-data php /srv/mediawiki/<version>/maintenance/showJobs.php --wiki=examplewiki`

* If a large backlog of jobs is created on a wiki, they can be manually run by a sysadmin with the **runJobs.php** maintenance script (`sudo -u www-data php /srv/mediawiki/<version>/maintenance/runJobs.php --wiki=examplewiki`
   * It is possible to specify the types of jobs that you want to run with `--type`. A list of available types can be found [here](https://meta.miraheze.org/wiki/mediawikiwiki:Manual:$wgJobClasses).
   * It is possible to specify the memory limit as well with `--memory-limit`

Jobrunner is a service, so if it is necessary, it may be restarted with `sudo service jobrunner restart`

Metrics regarding the job queue and types of jobs can be viewed [via Grafana](https://grafana.wikitide.net/d/3L3WYylMz/mediawiki-job-queue).

## Nginx 

*See more about Nginx on the main documentation page: [Tech:Nginx](/tech-docs/technginx)*

NGINX is a high-performance web server that Miraheze uses for all of our services that use HTTP.

## Firejail 

There are many extensions currently installed on Miraheze that work by executing external commands (wfShellExec, exec, or Shell::command) to provide media to the extensions (e.g. timelines, videos) or alter other databases. Most of these extensions require third-party libraries to be installed and executed. Unlike MediaWiki extensions, these libraries are harder to inspect and maintain for maximum security. A vulnerability in one of those libraries may be discovered anytime, which could lead to remote code execution.

To significantly reduce these potential security risks, we use [Firejail](https://firejail.wordpress.com/) (an SUID program) to execute those libraries inside sandboxes instead of executing them via the www-data user without further restrictions.

## ManageWiki Cache 

ManageWiki uses a caching backend for its settings, extensions, permissions, and namespaces. This caching system provides that each wiki has a JSON file located in `/srv/mediawiki/cache` with this information. In case that there is an issue with the ManageWiki cache for a specific wiki, the following can be used with `shell.php`: `$cw = new Miraheze\CreateWiki\CreateWikiJson( '<dbname>' ); $cw->resetWiki();`

## Composer 

Composer is a dependency manager for PHP libraries. MediaWiki itself, as well as quite a few extensions, make use of Composer. More information about Composer can be found on the [MediaWiki.org documentation page](https://meta.miraheze.org/wiki/mediawikiwiki:Composer). On Miraheze, the Composer dependency is managed with [mediawiki-repos](https://github.com/miraheze/mediawiki-repos), and any extensions that use Composer must be added with `composer: true` there in order for it to be installed properly. Please see the README in mediawiki-repos for further instructions.

## Profiling 

   ***Note**: If you don't know the X-WikiTide-Debug access key, please ask another member of the [Technology team](/tech-docs/techvolunteers).*

If you want to identify which parts of the code are taking a long time to execute, follow these steps:

**Profile the Web Request**

   ***Note**: Currently, `?forceprofile=1` is only available on [test151](/tech-docs/techtest151), ironically due to its own performance.*

Append `?forceprofile=1` to the URL of your MediaWiki page. This will trigger [profiling](https://www.mediawiki.org/wiki/Manual:Profiling) for that specific request.

**Set the X-WikiTide-Debug Headers**

Include the header `X-WikiTide-Debug: test151.wikitide.net`, replacing with the appropriate server.

If you are not on an internal server (i.e., from one of our own IP ranges), you must provide an access key via the `X-WikiTide-Debug-Access-Key` header. Save the key in a text file (e.g., access_key.txt) and reference it in your shell command using cat.

**Check Logs and Results**

After running the profiling request, examine the profiling output for bottlenecks. This data will indicate which parts of the code consume the most time.

---

**Examples **

**On an internal server (no access key required)**

```
curl -H "X-WikiTide-Debug: test151.wikitide.net" \
     "https://example.com/wiki/Main_Page?forceprofile=1" | grep '1 - main()' -A 450 | less
```

**On an external server (access key required)**

```
curl -H "X-WikiTide-Debug: test151.wikitide.net" \
     -H "X-WikiTide-Debug-Access-Key: $(cat access_key.txt)" \
     "https://example.com/wiki/Main_Page?forceprofile=1" | grep '1 - main()' -A 450 | less
```

---

*You can also use Chrome extensions for easier profiling and debugging:*

**[MediaWikiDebugJS](https://github.com/miraheze/MediaWikiDebugJS) Extension**

This extension helps you debug MediaWiki performance by showing response times and the backend MediaWiki or cache proxy servers to which your request connects.

Install the extension, then simply navigate to a page to start analyzing the performance in your browser.

**[WikiTideDebug](https://github.com/miraheze/WikiTideDebug) Extension**

This extension allows you to send HTTP requests directly to specific MediaWiki servers and check for errors cached in systems like [Varnish](/tech-docs/techvarnish) or [Cloudflare](/tech-docs/techcloudflare).

After installation, you can modify requests in the browser by specifying which backend server to hit (e.g., test151.wikitide.net) and inject the required `X-WikiTide-Debug` and `X-WikiTide-Debug-Access-Key` headers.

## MediaWiki-related Miraheze Guides 

* [Add a new extension](/tech-docs/techadding_a_new_extension)
* [Delete a wiki](/tech-docs/techdelete_a_wiki)
* [Move a wiki to another database server](/tech-docs/techmoving_a_wiki_to_another_database_server)
* [Remove a MediaWiki Extension](/tech-docs/techremoving_an_extension)
* [Update a MediaWiki Extension](https://meta.miraheze.org/wiki/Tech:Updating_an_extension)
* [How-To upgrade MediaWiki](/tech-docs/techupgrading_mediawiki)
* [Mwdeploy script](/tech-docs/techmwdeploy)

## Categories

* [Category:Services](https://meta.miraheze.org/wiki/Category:Services)



----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:MediaWiki_appserver)**