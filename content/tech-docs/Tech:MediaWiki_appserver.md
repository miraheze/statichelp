---
title: Tech:MediaWiki appserver
---

**MediaWiki application servers** (MediaWiki appserver) is a name given to the stack of software which runs Miraheze wikis. It is made up of several components.

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
   * You should always verify what will be run first, by using `--no-run`, and verifying the output first.

* **sql.php** – Self explanatory, to run SQL commands.

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

[mwtask181](Tech:Mwtask181.md) is responsible for running jobs on MediaWiki. As mentioned above, maintenance scripts should be run on this server.

* To see how many jobs are currently waiting to be run on a wiki, you can use the **showJobs.php** maintenance script (`sudo -u www-data php /srv/mediawiki/<version>/maintenance/showJobs.php --wiki=examplewiki`

* If a large backlog of jobs is created on a wiki, they can be manually run by a sysadmin with the **runJobs.php** maintenance script (`sudo -u www-data php /srv/mediawiki/<version>/maintenance/runJobs.php --wiki=examplewiki`
   * It is possible to specify the types of jobs that you want to run with `--type`. A list of available types can be found [here](https://meta.miraheze.org/wiki/mediawikiwiki:Manual:$wgJobClasses).
   * It is possible to specify the memory limit as well with `--memory-limit`

Jobrunner is a service, so if it is necessary, it may be restarted with `sudo service jobrunner restart`

Metrics regarding the jobqueue and types of jobs can be viewed [via Grafana](https://grafana.wikitide.net/d/3L3WYylMz/mediawiki-job-queue).

## Nginx 

*See more about Nginx on the main documentation page: [Tech:Nginx](Tech:Nginx.md)*

NGINX is a high-performance web server which Miraheze uses for all of our services that use HTTP.

## Firejail 

There are many extensions currently installed on Miraheze that work by executing external commands (wfShellExec, exec, or Shell::command) to provide media to the extensions (e.g. timelines, videos) or alter other databases. Most of these extensions require third-party libraries to be installed and executed. Unlike MediaWiki extensions, these libraries are harder to inspect and maintain for maximum security. A vulnerability in one of those libraries may be discovered anytime, which could lead to remote code execution.

To significantly reduce these potential security risks, we use [Firejail](https://firejail.wordpress.com/) (an SUID program) to execute those libraries inside sandboxes instead of executing them via the www-data user without further restrictions.

## ManageWiki Cache 

ManageWiki uses a caching backend for its settings, extensions, permissions, and namespaces. This caching system provides that each wiki has a JSON file located in `/srv/mediawiki/cache` with this information. In case that there is an issue with the ManageWiki cache for a specific wiki, the following can be used with `shell.php`: `$cw = new Miraheze\CreateWiki\CreateWikiJson( '<dbname>' ); $cw->resetWiki();`

## Composer 

Composer is a dependency manager for PHP libraries. MediaWiki itself as well as quite a few extensions make use of Composer. More information about Composer can be found on the [MediaWiki.org documentation page](https://meta.miraheze.org/wiki/mediawikiwiki:Composer). On Miraheze, the Composer dependency is managed with Puppet, and any extensions that use Composer must be added [to the Puppet file](https://github.com/miraheze/puppet/blob/master/modules/mediawiki/manifests/extensionsetup.pp) in order for it to be installed properly.

## Profiling 

If you want to find out what parts of the code take such a long time to execute, you can [profile](https://www.mediawiki.org/wiki/Manual:Profiling) your web requests. This can be done by appending `?forceprofile=1` to the URL and setting the `X-Miraheze-Debug: test151.wikitide.net` header.

Example:
```
$ curl -H 'X-Miraheze-Debug: test151.wikitide.net' 'https://allthetropes.org/wiki/Main_Page?forceprofile=1' | grep '1 - main()' -A 450 | less
```

## MediaWiki-related Miraheze Guides 

* [Add a new extension](Tech:Adding_a_new_extension.md)
* [Delete a wiki](Tech:Delete_a_wiki.md)
* [Move a wiki to another database server](Tech:Moving_a_wiki_to_another_database_server.md)
* [Remove a MediaWiki Extension](Tech:Removing_an_extension.md)
* [Update a MediaWiki Extension](https://meta.miraheze.org/wiki/Tech:Updating_an_extension)
* [How-To upgrade MediaWiki](Tech:Upgrading_MediaWiki.md)
* [Deploy mediawiki script](https://meta.miraheze.org/wiki/Tech:Deploy-mediawiki)

[Category:Services](https://meta.miraheze.org/wiki/Category:Services)

----
**Source**: [https://meta.miraheze.org/wiki/Tech:MediaWiki_appserver](https://meta.miraheze.org/wiki/Tech:MediaWiki_appserver)