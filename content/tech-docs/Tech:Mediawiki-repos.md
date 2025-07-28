---
title: Tech:Mediawiki-repos
---

The [mediawiki-repos](https://github.com/miraheze/mediawiki-repos) repository manages the repositories for extensions and skins which are deployed on Miraheze.

## Changing the branch or URL of a repository 

Note that all steps in this process except for the first one require access to the beta and production [MediaWiki application servers](/tech-docs/techmediawiki_appserver).

* Open a PR in mediawiki-repos ([example](https://github.com/miraheze/mediawiki-repos/pull/78))
* Merge the PR
* Wait for puppet to run on puppet181 so mediawiki-repos is pulled (you can check [Icinga](https://monitoring.wikitide.net/monitoring/service/show?host=puppet181&service=puppet181%20Puppet) to see when puppet has last run), or run it manually if you have access
* On each of the canary servers (currently test151 and mwtask181), recreate the staging folders for the extension or skin.
   * Remove the folders. For the example PR linked above, this would be: 
```
sudo -u www-data rm /srv/mediawiki-staging/1.43/extensions/Preloader/ -rf
```
 and 
```
sudo -u www-data rm /srv/mediawiki-staging/1.44/extensions/Preloader/ -rf
```
 (check which MediaWiki versions are currently used before doing this)
   * Run puppet: 
```
sudo puppet agent -tv
```
* Upgrade the extension/skin if necessary

----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:Mediawiki-repos)**