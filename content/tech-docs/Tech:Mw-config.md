---
title: Tech:Mw-config
---

**mw-config** is where Miraheze's MediaWiki configuration (and more!) is stored. [It is publicly available on GitHub](https://meta.miraheze.org/wiki/github:miraheze/mw-config), and anyone can submit a PR to change things around, install custom hook handlers for their wiki, and more.

## Where everything is

mw-config is split up into multiple files, in sharp contrast with the all-encompasing LocalSettings.php you would normally have in typical MediaWiki installations. You should know the following terminology:

* **Global** means either affecting all wikis in Miraheze or affecting Miraheze in general, nor specifically targeting wikis.
* **Local** means affecting one or more wikis in Miraheze, but not all of them.

| + Files and their purpose |
| File | | Purpose |
| --- | --- | --- |
| Database.php | | Database-related configuration, for all the farm |
| FileBackend.php | | File storage-related configuration, for all the farm |
| GlobalCache.php | | Cache related-configuration, for all the farm |
| GlobalExtensions.php | | Extensions loaded on all of Miraheze's wikis. These ones cannot be disabled via ManageWiki |
| GlobalLogging.php | | Miraheze's logging configuration |
| GlobalSettings.php | | A bit of a mess. Contains all of our globally-installed hooks, handles loading some wiki-specific extensions, as well as loading dependencies of some extensions (unused?) *some* globally-applied configs, and much more |
| GlobalSkins.php | | Skins loaded in all of our wikis. These ones cannot be disabled via ManageWiki |
| InterwikiSortOrders.php | | Configuration for $wgInterwikiSortingInterwikiSortOrders, from the InterwikiSorting extension |
| LocalSettings.php | | The entry point. Loads the rest of the files, has some configs, but is mostly used for configurating variables the same way you'd do in standard MediaWiki, but through wgConf instead. |
| LocalWiki.php | | Wiki-specific settings that cannot be done through ManageWiki or LocalSettings.php's wgConf, as well as custom hook handlers for the wikis |
| ManageWikiExtensions.php | | Entries for all the extensions that can be configured through ManageWiki |
| ManageWikiNamespaces.php | | Configuration related to namespaces |
| ManageWikiSettings.php | | Configuration for all the variables that can be configured via ManageWiki |
| SemanticMediaWiki.php | | Configuration specific to the Semantic MediaWiki extension |
| Wikibase.php | | Configuration specific to the Wikibase extensions |

## How to do some typical changes

A lot of the changes done to this repo are just the same thing but for different wikis each time.

### Extended confirmed protection or other custom protection levels

Example PR: [T11506: Setup extendedconfirmed protection for mypediawiki](https://meta.miraheze.org/wiki/github:miraheze/mw-config/pull/5437)

TODO

### Removing ManageWiki extensions or configurations

TODO

### Installing new extensions and their configuration

See also: [User:PixDeVl/TC 101#mediawiki-repos.yaml & ManageWikiExtensions.php](https://meta.miraheze.org/wiki/User:PixDeVl/TC_101#mediawiki-repos.yaml_&_ManageWikiExtensions.php)

TODO

### Writing a custom hook handler for a wiki

Example PR: [T9101: Redirect USER_WIKI_TALK to USER_TALK for polandballruwiki](https://meta.miraheze.org/wiki/github:miraheze/mw-config/pull/4662)

Assuming you know how to write hook handlers on regular MediaWiki LocalSettings.php, here it is very similar but you do them on `LocalWiki.php` instead.

* Go to `LocalWiki.php`.
* Write a case statement for your wiki's database name (you can see this on ManageWiki if you don't know it).
* Attach your hook via `$wgHooks`.

----
**Source**: [https://meta.miraheze.org/wiki/Tech:Mw-config](https://meta.miraheze.org/wiki/Tech:Mw-config)