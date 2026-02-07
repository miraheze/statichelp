---
title: Tech:Noticeboard/Removal of ImageRating extension
---

`{{ {{Mbox|type=content|text=This page is a draft. Its content is not yet finalized.}} }}`

This page will be linked in a Echo notification sent through [NotifyWikiUsers](https://github.com/miraheze/MirahezeMagic/blob/main/maintenance/NotifyWikiUsers.php) to all bureaucrats/admins whose wiki is using the ImageRating extension.

Undecided questions about this draft:
* Do we put this in the [Community portal](https://meta.miraheze.org/wiki/Community_portal), [Tech:Noticeboard](/tech-docs/technoticeboard), or this subpage? My preference is to use subpages because we need the link in the Echo notification to be persistent. Once the discussion is archived, its URL will change, invalidating the link for those who click on it late.
* Do we create 3 separate discussion pages (for ImageRating, QuizGame, and RandomGameUnit) or use a single page? If we use a single page, there'd be less pages to track, but some wiki admins may receive 3 notifications all pointing to the same page, which is kind of confusing. We can also send a single notification saying "some of the extensions your wiki is using may get removed".

## Rationale

Per [T2934](https://meta.miraheze.org/wiki/phab:T2934), [Extension:ImageRating](https://meta.miraheze.org/wiki/mw:Extension:ImageRating) has been on Miraheze since 2018. Despite its long history, no wiki seems to be using the extension. For example, All The Tropes originally requested it, but nothing shows up on [Special:ImageRating](https://allthetropes.org/wiki/Special:ImageRating?type=best). Other wikis that enabled the extension also do not seem to be using it.

The extension is compatible in 1.45. Though the incompatibility can be fixed like any other extension, continued deployment consumes time fixing and testing the extension that can be spent elsewhere.

## Discussion

__NEWSECTIONLINK__
If no objection with a convincing use case is raised, the technology will remove this extension. Please reply here with your comments. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 11:58, 6 February 2026 (UTC)

 `{{ {{Support}} }}` As proposer. Support votes don't really matter here since we are mainly looking for serious use cases for this extension. This is merely an example comment. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 12:00, 6 February 2026 (UTC)
   Also think it's worthwhile to note the actual errors: [phorge:P562](https://meta.miraheze.org/wiki/phorge:P562), error 13 (available at [Special:Permalink/516330](https://meta.miraheze.org/wiki/Special:Permalink/516330) since Phorge's task editing leaves a lot to be desired) as well as [phorge:T14459#298025](https://meta.miraheze.org/wiki/phorge:T14459#298025) which is a completely different error. [TheWWRNerdGuy](https://meta.miraheze.org/wiki/User:TheWWRNerdGuy) ([talk](https://meta.miraheze.org/wiki/User_talk:TheWWRNerdGuy)) 12:26, 6 February 2026 (UTC)

----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:Noticeboard/Removal_of_ImageRating_extension)**