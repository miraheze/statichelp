---
title: Tech:Noticeboard/Removing extensions for the MediaWiki 1.46 upgrade
---

`{{ {{Mbox|type=content|text=This page is a draft. Its content is not yet finalized.}} }}`
This page details extensions that the [Technology Team](/tech-docs/techhome) is planning to remove before or during the [MediaWiki 1.46 upgrade](https://meta.miraheze.org/wiki/MediaWiki/1.46).

Wiki administrators and bureaucrats: please check your wiki's `Special:Version` page and `Special:ManageWiki/extensions` to see whether your wiki has any of the extensions below installed. Note that some extensions will have spaces in their names, preventing a full name search from finding the extension.

Each extension is in a different situation. Some are going to be removed for technical reasons and the decision is unlikely to be changed by community input. Others are proposed for removal due to a perceived lack of usefulness combined with other technical considerations. If there is enough community interest in preserving the extension in question, the technology team could attempt to fix the extension instead of removing it.__NEWSECTIONLINK__

--[PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 11:17, 13 July 2026 (UTC)

## Extension:DataTransfer

### Rationale 1

Testing revealed multiple issues with the extension that prevent it from properly functioning.

The technology team also believes that it has limited use since most functionalities are covered by MediaWiki's native import/export features.

### Discussion 1

Please respond here. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 11:17, 13 July 2026 (UTC)

## Extension:LanguageSelector

### Rationale 2

This is tracked on [T14657](https://meta.miraheze.org/wiki/phab:T14657).

The extension is no longer maintained, uses hooks removed more than 5 years ago, and can "lead people to seeing the page in a random language".

Its functionalities also overlap with [Extension:UniversalLanguageSelector](https://meta.miraheze.org/wiki/mw:Extension:UniversalLanguageSelector).

LanguageSelector's removal is unlikely to be changed, though if there is need for changing the interface language without logging in, the technology team can consider adding additional configurations to UniversalLanguageSelector.

### Discussion 2

Please respond here. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 11:17, 13 July 2026 (UTC)

## Extension:AutoCreatePage

### Rationale 3

This is tracked on [T15017](https://meta.miraheze.org/wiki/phab:T15017). The extension has unfixable security issues, which I will not detail here.

It doesn't have a full replacement, though the page creation process can be made much easier by using [Extension:InputBox](https://meta.miraheze.org/wiki/mw:Extension:InputBox) with a preload template.

### Discussion 3

Please respond here. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 11:17, 13 July 2026 (UTC)

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

----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:Noticeboard/Removing_extensions_for_the_MediaWiki_1.46_upgrade)**