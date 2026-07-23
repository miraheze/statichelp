---
title: Tech:Noticeboard/Removing extensions for the MediaWiki 1.46 upgrade
---

This page details extensions that the [Technology Team](/tech-docs/techhome) is planning to remove before or during the [MediaWiki 1.46 upgrade](https://meta.miraheze.org/wiki/MediaWiki/1.46).

Wiki administrators and bureaucrats: please check your wiki's `Special:Version` page and `Special:ManageWiki/extensions` to see whether your wiki has any of the extensions below installed. Note that some extensions will have spaces in their names, preventing a full name search from finding the extension.

Each extension is in a different situation. Some are going to be removed for technical reasons and the decision is unlikely to be changed by community input. Others are proposed for removal due to a perceived lack of usefulness combined with other technical considerations. If there is enough community interest in preserving the extension in question, the technology team could attempt to fix the extension instead of removing it. Please not that the result of the discussions below is non-binding: extension additions and removals are at the discretion of the technology team.__NEWSECTIONLINK__

--[PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 11:17, 13 July 2026 (UTC)

## Extension:DataTransfer

### Rationale 1

Testing revealed multiple issues with the extension that prevent it from properly functioning.

The technology team also believes that it has limited use since most functionalities are covered by MediaWiki's native import/export features.

### Discussion 1

Please respond here. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 11:17, 13 July 2026 (UTC)

   No concerns this, as there are acceptable alternatives. I'm wondering, though, can you share some stats on the number of wikis on which each extension is enabled (active wikis only; no need for locked, closed, or deleted wikis, I think). [Doug](https://meta.miraheze.org/wiki/User:Doug) ([talk](https://meta.miraheze.org/wiki/User_talk:Doug)) 01:53, 19 July 2026 (UTC)
      Added in the appendix. The parser function doesn't provide a way to filter by wiki state unfortunately. The [list on the communities wiki](https://meta.miraheze.org/wiki/mh:communities:List_of_extensions_by_popularity) only includes public, non-deleted wikis with the number of active users in mind, which could also be useful. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 14:33, 19 July 2026 (UTC)
         Ah, okay. Thanks. I'll check out [that page on Communities wiki](https://meta.miraheze.org/wiki/mh:communities:List_of_extensions_by_popularity). To clarify, I was wondering if there was an SQL query that could be run to generate that information. In any case, the information in the Appendix you've provided is helpful enough (number of wikis using it). [Doug](https://meta.miraheze.org/wiki/User:Doug) ([talk](https://meta.miraheze.org/wiki/User_talk:Doug)) 14:54, 19 July 2026 (UTC)
   Enabled it little more than a couple of years ago on my [creative-venture wiki](https://meta.miraheze.org/wiki/mh:ConstantNoble), just for the sake of the track listings on my forthcoming anthro novel's [side project](https://meta.miraheze.org/wiki/mh:ConstantNoble:Portal:VIMU_Vault); about the only extension I know of that supports CSV imports (via Special:ImportCSV). --[Routhwick](https://meta.miraheze.org/wiki/User:Routhwick) ([talk](https://meta.miraheze.org/wiki/User_talk:Routhwick)) 14:12, 22 July 2026 (UTC)
      Thanks for the feedback. I didn't expect wikis to be in need of this use case. Since we do have a wiki that need a DataTransfer feature not available in other extensions, tech can decide in the end whether the effort to fix this extension is worth it.
      Alternatively, you can convert the CSV file into an XML dump and use Special:Import. The XML dump does require a bit more effort to produce, though. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 17:30, 22 July 2026 (UTC)

## Extension:LanguageSelector

### Rationale 2

This is tracked on [T14657](https://meta.miraheze.org/wiki/phab:T14657).

The extension is no longer maintained, uses hooks removed more than 5 years ago, and can "lead people to seeing the page in a random language".

Its functionalities also overlap with [Extension:UniversalLanguageSelector](https://meta.miraheze.org/wiki/mw:Extension:UniversalLanguageSelector).

LanguageSelector's removal is unlikely to be changed, though if there is need for changing the interface language without logging in, the technology team can consider adding additional configurations to UniversalLanguageSelector.

### Discussion 2

Please respond here. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 11:17, 13 July 2026 (UTC)

   Note: the technology team will disable Language Selector and enable Universal Language Selector for all wikis that still uses Language Selector before removal. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 16:44, 20 July 2026 (UTC)

## Extension:AutoCreatePage

### Rationale 3

This is tracked on [T15017](https://meta.miraheze.org/wiki/phab:T15017). The extension has unfixable security issues, which I will not detail here.

It doesn't have a full replacement, though the page creation process can be made much easier by using [Extension:InputBox](https://meta.miraheze.org/wiki/mw:Extension:InputBox) with a preload template.

### Discussion 3

Please respond here. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 11:17, 13 July 2026 (UTC)

   No concerns. [Doug](https://meta.miraheze.org/wiki/User:Doug) ([talk](https://meta.miraheze.org/wiki/User_talk:Doug)) 01:55, 19 July 2026 (UTC)
   What alternative we have? This is BASIC for creating new categories on the fly. [Jakeukalane](https://meta.miraheze.org/wiki/User:Jakeukalane) ([talk](https://meta.miraheze.org/wiki/User_talk:Jakeukalane)) 16:48, 20 July 2026 (UTC)
      [Auto Create Category Pages](https://meta.miraheze.org/wiki/mw:Extension:Auto_Create_Category_Pages). [TheWWRNerdGuy](https://meta.miraheze.org/wiki/User:TheWWRNerdGuy) ([talk](https://meta.miraheze.org/wiki/User_talk:TheWWRNerdGuy)) 17:16, 20 July 2026 (UTC)

## Extension:FeaturedFeeds

### Rationale 4

The extension requires changes to mw-config, and a total of 0 wikis is using it this way despite many wikis enabling it in ManageWiki.

### Discussion 4

Please respond here. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 11:17, 13 July 2026 (UTC)

## Extension:MagicNoCache

### Rationale 5

Disabling the parser cache is almost never a good idea and has caused multiple outages on the entire farm in the past. If there is a need for frequent parser cache purges, we can consider restricting this extension or installing the [UpdateDaily extension](https://github.com/wiki-gg-oss/mediawiki-extensions-UpdateDaily).

### Discussion 5

Please respond here. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 11:17, 13 July 2026 (UTC)

## Extension:GeoGebra

### Rationale 6

This extension is not functional and does not show anything in our tests. It has been broken since MediaWiki 1.44, and no wiki reported this breakage to us. The original wiki that requested it is already deleted. We take this to mean a lack of interest in the extension.

### Discussion 6

Please respond here. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 12:17, 15 July 2026 (UTC)

## Extension:CleanChanges

### Rationale 7

See [T14270](https://meta.miraheze.org/wiki/phab:T14270) and [T379896](https://meta.miraheze.org/wiki/mediazilla:T379896).

The only useful feature left is the user filter, which doesn't make much sense since one can go to the Special:Contributions page for per-user recent changes.

### Discussion 7

Please respond here. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 00:34, 19 July 2026 (UTC)

   No issues here. Should be superseded by [Extension:SimpleChanges](https://meta.miraheze.org/wiki/mw:Extension:SimpleChanges). [CostinTea](https://meta.miraheze.org/wiki/User:CostinTea) ([talk](https://meta.miraheze.org/wiki/User_talk:CostinTea)) 23:33, 19 July 2026 (UTC)

## Extension:InterwikiSorting

### Rationale 8

See [T15015](https://meta.miraheze.org/wiki/phab:T15015). The Wikimedia Foundation, which maintains this extension, has undeployed it in [T253764](https://meta.miraheze.org/wiki/mediazilla:T253764).

The extension will likely become unmaintained as its largest user abandon it.

### Discussion 8

Please respond here. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 00:42, 19 July 2026 (UTC)
   Personally I think we can keep InterwikiSorting for a few MediaWiki versions, but as MediaWiki evolves, the extension will inevitably break. It is also poorly documented on mediawiki.org and has no instructions on how to use it. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 00:42, 19 July 2026 (UTC)

## Appendix: number of wikis using each extension

Data sourced from ManageWiki/WikiDiscover. All wikis (including inactive and deleted wikis) are included.
| pattern=<nowiki> | arg1=EXT | datatransfer | languageselector | autocreatepages | featuredfeeds | magicnocache | geogebra | cleanchanges | interwikisorting |

----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:Noticeboard/Removing_extensions_for_the_MediaWiki_1.46_upgrade)**