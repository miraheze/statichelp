---
title: Tech:Noticeboard/Removing extensions for the MediaWiki 1.45 upgrade
---

`{{ {{Mbox|type=content|text=This page is a draft. Its content is not yet finalized.}} }}`

This page details extensions that the [Technology Team](/tech-docs/techhome) is planning to remove for the [MediaWiki 1.45 upgrade](https://meta.miraheze.org/wiki/MediaWiki/1.45).

Wiki administrators and bureaucrats: please check your wiki's `Special:Version` page and `Special:ManageWiki/extensions` to see whether your wiki has any of the extensions below installed. Note that some extensions will have spaces in their names, preventing a full name search from finding the extension.

If no objection with a convincing use case is raised, the technology team will proceed to remove the extensions listed below. Please reply in the discussion section with your feedback.

## Extension:Flow

### Rationale 1

The Wikimedia Foundation is on its way to [undeploy Flow](https://meta.miraheze.org/wiki/mediazilla:T332022) (StructuredDiscussions), after which the extension will be completely unmaintained. It has already caused issues with past MediaWiki upgrades on Miraheze, so we should remove it sooner than later.

The technology team plans to use an automated script to delete all Flow discussion pages and replace them with wikitext equivalents. There are two possible paths:
* The replaced page only has a single revision and the edit history would be lost. The sequence of events can only be inferred from the timestamps on signatures.
* The replaced page has the full page history reconstructed from past Flow discussions. This option presents more technical challenges but seems to be doable (albeit harder than the previous option).
The technology team is still evaluating the feasibility of the second option. If you'd like to preserve the full edit history, please say so in the discussion section below.

### Discussion 1

Please respond here. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 22:12, 8 February 2026 (UTC)

## Extension:ImageRating

### Rationale 2

Per [T2934](https://meta.miraheze.org/wiki/phab:T2934), [Extension:ImageRating](https://meta.miraheze.org/wiki/mw:Extension:ImageRating) has been on Miraheze since 2018. Despite its long history, no wiki seems to be using it. For example, All The Tropes originally requested the extension, but nothing shows up on [Special:ImageRating](https://allthetropes.org/wiki/Special:ImageRating?type=best). Other wikis that enabled the extension also do not seem to be using it.

ImageRating is also incompatible in 1.45. Though the incompatibility can be fixed like any other extension, continued deployment consumes time fixing and testing the extension, and that time is better spent elsewhere.

### Discussion 2

__NEWSECTIONLINK__
Please respond here. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 10:21, 8 February 2026 (UTC)
 `{{ {{Support}} }}` As proposer. Support votes don't really matter here since we are mainly looking for serious use cases for this extension. This is merely an example comment. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 12:00, 6 February 2026 (UTC)
   Also think it's worthwhile to note the actual errors: [phorge:P562](https://meta.miraheze.org/wiki/phorge:P562), error 13 (available at [Special:Permalink/516330](https://meta.miraheze.org/wiki/Special:Permalink/516330) since Phorge's task editing leaves a lot to be desired) as well as [phorge:T14459#298025](https://meta.miraheze.org/wiki/phorge:T14459#298025) which is a completely different error. [TheWWRNerdGuy](https://meta.miraheze.org/wiki/User:TheWWRNerdGuy) ([talk](https://meta.miraheze.org/wiki/User_talk:TheWWRNerdGuy)) 12:26, 6 February 2026 (UTC)

## Extension:3D

### Rationale 3

The extension has been non-functional since MediaWiki 1.44. No reports of its dysfunction were received, so the extension likely has little to no usage on the farm.

Features provided by this extension can be implemented with JavaScript, such as [the 3D model viewer on Strinova Wiki](https://meta.miraheze.org/wiki/mh:strinova:3D_Models).

### Discussion 3

Please respond here. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 10:27, 8 February 2026 (UTC)

## Extension:ProtectSite

### Rationale 4

The extension does not prevent edits from occurring on the site (known since MediaWiki 1.44). No bug report was ever received.

Removing the `edit` permission from all user groups in `Special:ManageWiki/permissions` is equivalent to this extension in terms of functionality.

### Discussion 4

Please respond here. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 10:27, 8 February 2026 (UTC)

## Extension:QuizGame

### Rationale 5

Just like ImageRating, testing revealed multiple issues with this extension. Its functionality sees little to no usage on the entire farm and would be a burden to keep deployed.

### Discussion 5

Please respond here. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 10:27, 8 February 2026 (UTC)

## Extension:RandomGameUnit

### Rationale 6

Its functionality depends on QuizGame and has little use without it.

### Discussion 6

Please respond here. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 10:27, 8 February 2026 (UTC)

## Extension:NumberHeadings

### Rationale 7

Per [phorge:T14866](https://meta.miraheze.org/wiki/phorge:T14866), the extension is not compatible with 1.44's heading changes; the extension is maintained by Hallo Welt! GmbH who use a modified version of MediaWiki and are unlikely to fix it upstream. The extension itself is incredibly simple and could quite easily be replaced with a CSS Gadget.

### Discussion 7

Please respond here. [TheWWRNerdGuy](https://meta.miraheze.org/wiki/User:TheWWRNerdGuy) ([talk](https://meta.miraheze.org/wiki/User_talk:TheWWRNerdGuy)) 11:15, 8 February 2026 (UTC)

## Extension:OrphanedTalkPages

### Rationale 8

Doesn't appear to work.

### Discussion 8

Please respond here. [TheWWRNerdGuy](https://meta.miraheze.org/wiki/User:TheWWRNerdGuy) ([talk](https://meta.miraheze.org/wiki/User_talk:TheWWRNerdGuy)) 11:24, 8 February 2026 (UTC)

   This one is a bit mysterious since [Special:OrphanedTalkPages](https://meta.miraheze.org/wiki/Special:OrphanedTalkPages) shows some recent talk pages such as [Help talk:Index](https://meta.miraheze.org/wiki/Help_talk:Index). I was unable to make it work on mirabeta either. I think I did an explicit maintenance script run and somehow orphaned talk pages still won't show up. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 22:18, 8 February 2026 (UTC)

----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:Noticeboard/Removing_extensions_for_the_MediaWiki_1.45_upgrade)**