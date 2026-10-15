---
title: "Tech:Noticeboard/Request for feedback: changes to default MediaWiki settings (2)"
---

`{{ {{Mbox|text=This page is a draft. Please feel free to edit or give feedback, but do not start voting yet.}} }}`

This is a follow-up to [Tech:Noticeboard/Request for feedback: changes to default MediaWiki settings](/tech-docs/technoticeboard-request_for_feedback_changes_to_default_mediawiki_settings). I am proposing several more changes to Miraheze's default MediaWiki configuration, and members of the community are welcome to propose additional changes as well. This page will gather community feedback for the Technology Team's consideration. Proposals that are well-received by both the community and the Tech Team will be actioned. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 00:31, 14 October 2026 (UTC)
__NEWSECTIONLINK__
## Proposal 1: enable syntax highlighting by default 

**[CodeMirror](https://meta.miraheze.org/wiki/mw:Extension:CodeMirror)** is already a default extension, but its syntax highlighting feature is turned off until the user clicks the highlighter button in the editor toolbar. Syntax highlighting makes templates, links, and unclosed tags much easier to spot. It also comes with auto-completion which saves a lot of time looking up template titles and parser function names.

ManageWiki already has an option to make syntax highlighting the default (`$wmgCodeMirrorEnableDefault`). This proposal changes the default value of that option to `true`. Users who dislike syntax highlighting can still turn it off by clicking the toolbar button, and wikis can fully opt out in ManageWiki.

This change can either apply to all wikis that did not set this option explicitly or only to new wikis. I lean toward changing this for all wikis.

### Discussion 1a 

Please discuss enabling this option for all wikis that did not change this option. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 00:31, 14 October 2026 (UTC)

 `{{ {{Support}} }}` [Maitian MaiLin](https://meta.miraheze.org/wiki/User:Maitian_MaiLin) ([talk](https://meta.miraheze.org/wiki/User_talk:Maitian_MaiLin)) 11:18, 14 October 2026 (UTC)
      Just so you know, this RfF is still in drafting so votes don't count yet. - [<span style="color:#a25ac9">Sakurababochka</span>](https://meta.miraheze.org/wiki/User:Sakurababochka) ([<span style="color:#75c9af">talk</span>](https://meta.miraheze.org/wiki/Usertalk:Sakurababochka)) 11:23, 14 October 2026 (UTC)

### Discussion 1b 

Please discuss enabling this option only for new wikis. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 00:31, 14 October 2026 (UTC)

## Proposal 2: enable edit recovery by default 

**[Edit Recovery](https://meta.miraheze.org/wiki/mw:Help:Edit_Recovery)** saves unsaved changes in the source editor to the browser's local storage, so that work is not lost when the browser crashes, the tab is closed by accident, or the session expires. Next time the user opens the editor for that page, they are offered to restore their changes.

`$wgEnableEditRecovery` is enabled by default, but the feature stays hidden behind a user preference that is off by default. Most do not know it exists, so in practice it is barely used. This proposal sets `$wgDefaultUserOptions['editrecovery']` to `1` so that everyone gets this feature unless they turn it off in [Special:Preferences](https://meta.miraheze.org/wiki/Special:Preferences).

### Discussion 2 

Please discuss below. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 00:31, 14 October 2026 (UTC)

 `{{ {{Support}} }}` [Maitian MaiLin](https://meta.miraheze.org/wiki/User:Maitian_MaiLin) ([talk](https://meta.miraheze.org/wiki/User_talk:Maitian_MaiLin)) 11:19, 14 October 2026 (UTC)

This is a really imporatant and useful feature. I'm really sick of losing my edits for Internet lags and CAPTCHAs while contributing on Fandom. We can't count on everyone to pay enough attention to their [Special:Preferences](https://meta.miraheze.org/wiki/Special:Preferences), which is a really long page.--[AABb1221](https://meta.miraheze.org/wiki/User:AABb1221) ([talk](https://meta.miraheze.org/wiki/User_talk:AABb1221)) 04:19, 14 October 2026 (UTC)

## Proposal 3: do not enable MobileFrontend and MinervaNeue for new wikis 

**[MobileFrontend](https://meta.miraheze.org/wiki/mw:Extension:MobileFrontend)** (MF) and **[MinervaNeue](https://meta.miraheze.org/wiki/mw:Skin:MinervaNeue)** are enabled by default mostly because Vector 2010 does not work on small screens. We no longer use Vector 2010 as the default, and our default skin (Vector 2022) alongside the most popular ones (Timeless, Citizen, Cosmos, Monobook) are all responsive.

With MobileFrontend enabled, mobile visitors see Minerva instead of the wiki's default skin. Minerva is known is known to break and hide page content. For example, [Special:PermaLink/489799](https://meta.miraheze.org/wiki/Special:PermaLink/489799) looks fine on Vector 2022, but it is broken on mobile view ("Why Donate to Miraheze?" looks different), as reported on [Discord](https://discord.com/channels/407504499280707585/615786602454581249/1415156187074134109). MobileFrontend hiding navboxes is also a known quirk that requires ManageWiki tweaks to resolve.

This discrepancy is a major source of confusion. Disabling MF and Minerva for new wikis gives mobile visitors the similar experience as desktop visitors, and wikis that prefer Minerva can still opt in. Existing wikis are not affected and can continue to use Minerva if they so desire.

If a wiki changes its default skin to one that is not responsive, such as Vector legacy, MobileFrontend and MinervaNeue could be enabled automatically. I am not sure whether this is worth the added complexity, and some wikis might intentionally not use MobileFrontend alongside Vector legacy. This addition goes into proposal 3b.

### Discussion 3a 

Not enabling MobileFrontend and MinervaNeue for new wikis. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 00:31, 14 October 2026 (UTC)

   Minerva also ignores any custom sidebar the wiki has, which can potentially make mobile navigation much more fiddly. This isn't (as far as I know) made readily apparent anywhere, and I've seen it cause confusion more than once. - [<span style="color:#a25ac9">Sakurababochka</span>](https://meta.miraheze.org/wiki/User:Sakurababochka) ([<span style="color:#75c9af">talk</span>](https://meta.miraheze.org/wiki/Usertalk:Sakurababochka)) 09:25, 14 October 2026 (UTC)

### Discussion 3b 

Implement proposal 3a, and then automatically enabling MobileFrontend and MinervaNeue when a new wiki switches to a skin that is not responsive. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 00:31, 14 October 2026 (UTC)

   Sounds unnecessarily complicated, and this requires sorting out which skins are responsive and which are not. — [<span style="color:#DDAACC">Honoka55</span>](https://meta.miraheze.org/wiki/User:Honoka55)｜ [<span style="color:#CCAA88">talk</span>](https://meta.miraheze.org/wiki/User_talk:Honoka55) 11:31, 14 October 2026 (UTC)

## Proposal 4: add TemplateData to default extensions 

**[TemplateData](https://meta.miraheze.org/wiki/mw:Extension:TemplateData)** lets template editors describe a template's parameters, which is especially useful for VisualEditor.

TemplateData is also required by [TemplateWizard](https://meta.miraheze.org/wiki/mw:Extension:TemplateWizard), which could also be enabled, but I do not know enough about it. Maybe someone else can create a separate proposal for TemplateWizard.

### Discussion 4 

Please discuss below. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 00:31, 14 October 2026 (UTC)

   Surprised this isn't already the case. If VisualEditor is now enabled by default, editing templates would be really hard without TemplateData. [KockaAdmiralac](https://meta.miraheze.org/wiki/User:KockaAdmiralac) ([talk](https://meta.miraheze.org/wiki/User_talk:KockaAdmiralac)) 22:40, 14 October 2026 (UTC)

----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:Noticeboard/Request_for_feedback:_changes_to_default_MediaWiki_settings_(2))**