---
title: Tech:Parsoid
---

As of [MediaWiki/1.39](https://meta.miraheze.org/wiki/MediaWiki/1.39), Parsoid is used by Flow, DiscussionTools and VisualEditor to convert Wikitext->HTML and DOM5. It is a requirement for these extensions to be enabled on Miraheze (for performance reasons) and as such is a necessary piece of software. After 7 December 2020, Miraheze switched to the version bundled with MediaWiki Core. It is now a PHP service and the NodeJS version was removed.

Wikimedia began migrating to Parsoid as the default parser (replacing the legacy php parser simply known as parser.php) during MediaWiki 1.41. A plan for such a move on Miraheze is being developed on [Phorge](https://meta.miraheze.org/wiki/phorge:T10915) and is expected to be one of the largest changes to the MediaWiki backend since Miraheze began.

Since Late 2023, Parsoid has been enabled and cached for all Miraheze wikis in preparation for beta testing during 2024.

## Categories

* [Category:Services](https://meta.miraheze.org/wiki/Category:Services)

----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:Parsoid)**