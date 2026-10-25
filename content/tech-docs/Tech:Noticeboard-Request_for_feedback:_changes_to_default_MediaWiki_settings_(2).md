---
title: "Tech:Noticeboard/Request for feedback: changes to default MediaWiki settings (2)"
---

This is a follow-up to [Tech:Noticeboard/Request for feedback: changes to default MediaWiki settings](/tech-docs/technoticeboard-request_for_feedback_changes_to_default_mediawiki_settings). I am proposing several more changes to Miraheze's default MediaWiki configuration, and members of the community are welcome to propose additional changes as well. This page will gather community feedback for the Technology Team's consideration. Proposals that are well-received by both the community and the Tech Team will be actioned. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 00:31, 14 October 2026 (UTC)
    The draft is finalized and voting can start. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 06:24, 16 October 2026 (UTC)
__NEWSECTIONLINK__
## Proposal 1: enable syntax highlighting by default 

**[CodeMirror](https://meta.miraheze.org/wiki/mw:Extension:CodeMirror)** is already a default extension, but its syntax highlighting feature is turned off until the user clicks the highlighter button in the editor toolbar. Syntax highlighting makes templates, links, and unclosed tags much easier to spot. It also comes with auto-completion which saves a lot of time looking up template titles and parser function names.

ManageWiki already has an option to make syntax highlighting the default (`$wmgCodeMirrorEnableDefault`). This proposal changes the default value of that option to `true`. Users who dislike syntax highlighting can still turn it off by clicking the toolbar button, and wikis can fully opt out in ManageWiki.

This change can either apply to all wikis that did not set this option explicitly or only to new wikis. I lean toward changing this for all wikis.

### Discussion 1a 

Please discuss enabling this option for all wikis that did not change this option. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 00:31, 14 October 2026 (UTC)

 `{{ {{Support}} }}` [Maitian MaiLin](https://meta.miraheze.org/wiki/User:Maitian_MaiLin) ([talk](https://meta.miraheze.org/wiki/User_talk:Maitian_MaiLin)) 11:18, 14 October 2026 (UTC)
      Just so you know, this RfF is still in drafting so votes don't count yet. - [<span style="color:#a25ac9">Sakurababochka</span>](https://meta.miraheze.org/wiki/User:Sakurababochka) ([<span style="color:#75c9af">talk</span>](https://meta.miraheze.org/wiki/Usertalk:Sakurababochka)) 11:23, 14 October 2026 (UTC)
         Since the proposal has not changed since this vote is cast, I suppose we can keep it as is. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 06:25, 16 October 2026 (UTC)
 `{{ {{support}} }}` as proposer. CM6 still has some minor issues such as [mediazilla:T441381](https://meta.miraheze.org/wiki/mediazilla:T441381) but I think the experience has gotten good enough that we can enable it for new users. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 06:26, 16 October 2026 (UTC)
 `{{ {{oppose}} }}` per JaneBuzJane's comments on 1b and my general opposition to making farm-wide settings changes which aren't necessary security/tech/T&S changes. As the default is disabled, plenty of wikis which are happy with it disabled would be included in the list of wikis which have not changed this setting. - [<span style="color:#a25ac9">Sakurababochka</span>](https://meta.miraheze.org/wiki/User:Sakurababochka) ([<span style="color:#75c9af">talk</span>](https://meta.miraheze.org/wiki/Usertalk:Sakurababochka)) 08:18, 16 October 2026 (UTC)
      I think most wikis keep the status quo because they are not aware of the existence of this setting. I sampled a few wikis on other hosts (wiki.gg, Fandom, and WeirdGloop), and all of them present the syntax highlighter to logged-out users in the wikitext editor. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 08:49, 17 October 2026 (UTC)
 `{{ {{support}} }}` - syntax highlighting makes it *so* much easier to read wikitext, and I believe newer users would see quite a benefit from it. [Rexogamer](https://meta.miraheze.org/wiki/User:Rexogamer) ([talk](https://meta.miraheze.org/wiki/User_talk:Rexogamer)) 16:56, 16 October 2026 (UTC)
 `{{ {{Abstain}} }}` - Even though it is useful, particularly for newbies, I have been accustomed to editing wikitext without using syntax. So I would leave it as abstain. [Unfunktion](https://meta.miraheze.org/wiki/User:Unfunktion) ([talk](https://meta.miraheze.org/wiki/User_talk:Unfunktion)) 16:11, 18 October 2026 (UTC)
 `{{ {{s}} }}` This is useful.--[AABb1221](https://meta.miraheze.org/wiki/User:AABb1221) ([talk](https://meta.miraheze.org/wiki/User_talk:AABb1221)) 11:30, 24 October 2026 (UTC)
 `{{ {{support}} }}` makes sense as a default [Jenny on Wiki](https://meta.miraheze.org/wiki/User:Jenny_on_Wiki) ([talk](https://meta.miraheze.org/wiki/User_talk:Jenny_on_Wiki)) 15:15, 24 October 2026 (UTC)

### Discussion 1b 

Please discuss enabling this option only for new wikis. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 00:31, 14 October 2026 (UTC)

   One thing that might perhaps be of note for the proposal of "enable for all wikis" is that syntax highlighting isn't always good. I have made some accessibility changes in my common.css to make the colors have more contrast. If other editors have made tweaks like this, it could be jarring to suddenly see a big change like this (even if the fix is just clicking the button, they may not know HOW to do that, or they could get lost down the Editing Preferences toolbar rabbit hole). I know we're not voting yet but I feel like this is a strong point for enabling it only for new wikis. [JaneBuzJane](https://meta.miraheze.org/wiki/User:JaneBuzJane) ([talk](https://meta.miraheze.org/wiki/User_talk:JaneBuzJane)) 02:14, 15 October 2026 (UTC)
      Yeah custom CSS would indeed cause issues. Another source of problems is wikis that have customized the colors based on CodeMirror 5 but not 6. The old styling will be broken on the new CodeMirror. But since we are a few weeks past the MW 1.46 upgrade I assume most wikis have done the minimal CSS fix. This will be less of an issue with time. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 06:31, 16 October 2026 (UTC)
 `{{ {{abstain}} }}` per above comments on this proposal. - [<span style="color:#a25ac9">Sakurababochka</span>](https://meta.miraheze.org/wiki/User:Sakurababochka) ([<span style="color:#75c9af">talk</span>](https://meta.miraheze.org/wiki/Usertalk:Sakurababochka)) 08:18, 16 October 2026 (UTC)
 `{{ {{Support}} }}` only for new wikis. I am of the opinion that it would be needlessly disruptive otherwise. - [JaneBuzJane](https://meta.miraheze.org/wiki/User:JaneBuzJane) ([talk](https://meta.miraheze.org/wiki/User_talk:JaneBuzJane)) 13:48, 18 October 2026 (UTC)

## Proposal 2: enable edit recovery by default 

**[Edit Recovery](https://meta.miraheze.org/wiki/mw:Help:Edit_Recovery)** saves unsaved changes in the source editor to the browser's local storage, so that work is not lost when the browser crashes, the tab is closed by accident, or the session expires. Next time the user opens the editor for that page, they are offered to restore their changes.

`$wgEnableEditRecovery` is enabled by default, but the feature stays hidden behind a user preference that is off by default. Most do not know it exists, so in practice it is barely used. This proposal sets `$wgDefaultUserOptions['editrecovery']` to `1` so that everyone gets this feature unless they turn it off in [Special:Preferences](https://meta.miraheze.org/wiki/Special:Preferences).

### Discussion 2 

Please discuss below. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 00:31, 14 October 2026 (UTC)

 `{{ {{Support}} }}` [Maitian MaiLin](https://meta.miraheze.org/wiki/User:Maitian_MaiLin) ([talk](https://meta.miraheze.org/wiki/User_talk:Maitian_MaiLin)) 11:19, 14 October 2026 (UTC)
   Kind of a random question, but does this work for anon editors? I'm assuming not, since the toggle is in Special:Preferences. I'm just curious. [JaneBuzJane](https://meta.miraheze.org/wiki/User:JaneBuzJane) ([talk](https://meta.miraheze.org/wiki/User_talk:JaneBuzJane)) 02:09, 15 October 2026 (UTC)
      Per documentation on mw.org [wgDefaultUserOptions](https://meta.miraheze.org/wiki/mw:Manual:$wgDefaultUserOptions) "will override the default user preferences for anonymous visitors and users who have not customized their preferences". So my guess would be it does work for anons. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 06:35, 16 October 2026 (UTC)
   This is a really imporatant and useful feature. I'm really sick of losing my edits for Internet lags and CAPTCHAs while contributing on Fandom. We can't count on everyone to pay enough attention to their [Special:Preferences](https://meta.miraheze.org/wiki/Special:Preferences), which is a really long page.--[AABb1221](https://meta.miraheze.org/wiki/User:AABb1221) ([talk](https://meta.miraheze.org/wiki/User_talk:AABb1221)) 04:19, 14 October 2026 (UTC)
 `{{ {{Support}} }}` as proposer. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 06:35, 16 October 2026 (UTC)
 `{{ {{support}} }}` on the grounds of having lost more edits than I can count to page reloads. - [<span style="color:#a25ac9">Sakurababochka</span>](https://meta.miraheze.org/wiki/User:Sakurababochka) ([<span style="color:#75c9af">talk</span>](https://meta.miraheze.org/wiki/Usertalk:Sakurababochka)) 08:18, 16 October 2026 (UTC)
 `{{ {{support|strongest}} }}` [Jenny on Wiki](https://meta.miraheze.org/wiki/User:Jenny_on_Wiki) ([talk](https://meta.miraheze.org/wiki/User_talk:Jenny_on_Wiki)) 14:16, 16 October 2026 (UTC)
 `{{ {{support}} }}` per proposal. - [JaneBuzJane](https://meta.miraheze.org/wiki/User:JaneBuzJane) ([talk](https://meta.miraheze.org/wiki/User_talk:JaneBuzJane)) 13:49, 18 October 2026 (UTC)
 `{{ {{Support|partial}} }}` - ‎ I hardly use edit recovery, only once. But maybe, just in case. It would be helpful. [Unfunktion](https://meta.miraheze.org/wiki/User:Unfunktion) ([talk](https://meta.miraheze.org/wiki/User_talk:Unfunktion)) 16:12, 18 October 2026 (UTC)
 `{{ {{Support}} }}`.--[<span style="color:#00C0FF;">铁桶</span>](https://meta.miraheze.org/wiki/User:铁桶) ([Talk](https://meta.miraheze.org/wiki/User_Talk:铁桶)) 15:04, 19 October 2026 (UTC)
 `{{ {{s}} }}` per rationale above.--[AABb1221](https://meta.miraheze.org/wiki/User:AABb1221) ([talk](https://meta.miraheze.org/wiki/User_talk:AABb1221)) 11:31, 24 October 2026 (UTC)

## Proposal 3: do not enable MobileFrontend and MinervaNeue for new wikis 

**[MobileFrontend](https://meta.miraheze.org/wiki/mw:Extension:MobileFrontend)** (MF) and **[MinervaNeue](https://meta.miraheze.org/wiki/mw:Skin:MinervaNeue)** are enabled by default mostly because Vector 2010 does not work on small screens. We no longer use Vector 2010 as the default, and our default skin (Vector 2022) alongside the most popular ones (Timeless, Citizen, Cosmos, Monobook) are all responsive.

With MobileFrontend enabled, mobile visitors see Minerva instead of the wiki's default skin. Minerva is known is known to break and hide page content. For example, [Special:PermaLink/489799](https://meta.miraheze.org/wiki/Special:PermaLink/489799) looks fine on Vector 2022, but it is broken on mobile view ("Why Donate to Miraheze?" looks different), as reported on [Discord](https://discord.com/channels/407504499280707585/615786602454581249/1415156187074134109). MobileFrontend hiding navboxes is also a known quirk that requires ManageWiki tweaks to resolve.

This discrepancy is a major source of confusion. Disabling MF and Minerva for new wikis gives mobile visitors the similar experience as desktop visitors, and wikis that prefer Minerva can still opt in. Existing wikis are not affected and can continue to use Minerva if they so desire.

~~If a wiki changes its default skin to one that is not responsive, such as Vector legacy, MobileFrontend and MinervaNeue could be enabled automatically. I am not sure whether this is worth the added complexity, and some wikis might intentionally not use MobileFrontend alongside Vector legacy. This addition goes into proposal 3b.~~ This proposal was drafted as 3b but has been withdrawn due to multiple concerns.

### Discussion 3a 

Not enabling MobileFrontend and MinervaNeue for new wikis. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 00:31, 14 October 2026 (UTC)

   Minerva also ignores any custom sidebar the wiki has, which can potentially make mobile navigation much more fiddly. This isn't (as far as I know) made readily apparent anywhere, and I've seen it cause confusion more than once. - [<span style="color:#a25ac9">Sakurababochka</span>](https://meta.miraheze.org/wiki/User:Sakurababochka) ([<span style="color:#75c9af">talk</span>](https://meta.miraheze.org/wiki/Usertalk:Sakurababochka)) 09:25, 14 October 2026 (UTC)
 `{{ {{support}} }}` as proposer. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 06:35, 16 October 2026 (UTC)
      I should note that we plan to add a help message in ManageWiki for $wgDefaultSkin telling users of Vector legacy to enable MobileFrontend and Minerna if this proposal passes. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 06:36, 16 October 2026 (UTC)
 `{{ {{support}} }}` per my comments on this proposal from the drafting period. - [<span style="color:#a25ac9">Sakurababochka</span>](https://meta.miraheze.org/wiki/User:Sakurababochka) ([<span style="color:#75c9af">talk</span>](https://meta.miraheze.org/wiki/Usertalk:Sakurababochka)) 08:18, 16 October 2026 (UTC)
 `{{ {{support}} }}` - assuming `{{ {{code|$wgVectorResponsive}} }}` is(/will be) on by default. [Rexogamer](https://meta.miraheze.org/wiki/User:Rexogamer) ([talk](https://meta.miraheze.org/wiki/User_talk:Rexogamer)) 17:24, 16 October 2026 (UTC)
      Yep. It is the default on new wikis created on Miraheze. Older wikis retain the old default (disabled) per our [previous RfF](/tech-docs/technoticeboard-request_for_feedback_changes_to_default_mediawiki_settings). [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 08:51, 17 October 2026 (UTC)
 `{{ {{support|strongest}} }}` Support per proposal. In my experience they cause more problems than they solve. - [JaneBuzJane](https://meta.miraheze.org/wiki/User:JaneBuzJane) ([talk](https://meta.miraheze.org/wiki/User_talk:JaneBuzJane)) 13:51, 18 October 2026 (UTC)
 `{{ {{Support|strong}} }}` - I feel these kinda make navigating wikis difficult, especially for navboxes. [Unfunktion](https://meta.miraheze.org/wiki/User:Unfunktion) ([talk](https://meta.miraheze.org/wiki/User_talk:Unfunktion)) 16:17, 18 October 2026 (UTC)
 `{{ {{Note}} }}` MobileFrontend is compatible with other skins (Vector, Timeless, Monobook, Citizen), so that could potentially be an option. [MacFan4000](https://meta.miraheze.org/wiki/User:MacFan4000) ([Talk](https://meta.miraheze.org/wiki/User_talk:MacFan4000) [Contribs](https://meta.miraheze.org/wiki/Special:Contributions/MacFan4000)) 16:32, 19 October 2026 (UTC)
 `{{ {{support}} }}` [Jenny on Wiki](https://meta.miraheze.org/wiki/User:Jenny_on_Wiki) ([talk](https://meta.miraheze.org/wiki/User_talk:Jenny_on_Wiki)) 15:16, 24 October 2026 (UTC) `{{ {{Collapse top|title=Withdrawn proposal}} }}`

### Discussion 3b 

Implement proposal 3a, and then automatically enabling MobileFrontend and MinervaNeue when a new wiki switches to a skin that is not responsive. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 00:31, 14 October 2026 (UTC)

   Sounds unnecessarily complicated, and this requires sorting out which skins are responsive and which are not. — [<span style="color:#DDAACC">Honoka55</span>](https://meta.miraheze.org/wiki/User:Honoka55)｜ [<span style="color:#CCAA88">talk</span>](https://meta.miraheze.org/wiki/User_talk:Honoka55) 11:31, 14 October 2026 (UTC)
   I would propose removing 3b as an option - it would be difficult to keep track of which skins are responsive and which are not, but moreover, it could cause a lot of confusion for editors who enable a skin and then see a different one on mobile than they selected. - [JaneBuzJane](https://meta.miraheze.org/wiki/User:JaneBuzJane) ([talk](https://meta.miraheze.org/wiki/User_talk:JaneBuzJane)) 02:07, 15 October 2026 (UTC)
   Thanks for the feedback. I will withdraw this proposal. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 06:20, 16 October 2026 (UTC) `{{ {{Collapse bottom}} }}`

## Proposal 4: add TemplateData to default extensions 

**[TemplateData](https://meta.miraheze.org/wiki/mw:Extension:TemplateData)** lets template editors describe a template's parameters, which is especially useful for VisualEditor.

TemplateData is also required by [TemplateWizard](https://meta.miraheze.org/wiki/mw:Extension:TemplateWizard), which could also be enabled, but I do not know enough about it. Maybe someone else can create a separate proposal for TemplateWizard.

### Discussion 4 

Please discuss below. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 00:31, 14 October 2026 (UTC)

   Surprised this isn't already the case. If VisualEditor is now enabled by default, editing templates would be really hard without TemplateData. [KockaAdmiralac](https://meta.miraheze.org/wiki/User:KockaAdmiralac) ([talk](https://meta.miraheze.org/wiki/User_talk:KockaAdmiralac)) 22:40, 14 October 2026 (UTC)
      I believe you were the person who mentioned TemplateData last time, but it was too late for new proposals, so TemplateData waited until this RfF. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 06:37, 16 October 2026 (UTC)
 `{{ {{support}} }}` as proposer. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 06:37, 16 October 2026 (UTC)
 `{{ {{Abstain}} }}`, since I am not familiar with the extension and it would be remiss of me to vote as though I was. - [<span style="color:#a25ac9">Sakurababochka</span>](https://meta.miraheze.org/wiki/User:Sakurababochka) ([<span style="color:#75c9af">talk</span>](https://meta.miraheze.org/wiki/Usertalk:Sakurababochka)) 08:18, 16 October 2026 (UTC)
 `{{ {{support}} }}` - ...it isn't already? [Rexogamer](https://meta.miraheze.org/wiki/User:Rexogamer) ([talk](https://meta.miraheze.org/wiki/User_talk:Rexogamer)) 17:15, 16 October 2026 (UTC)
 `{{ {{support}} }}` per proposal. - [JaneBuzJane](https://meta.miraheze.org/wiki/User:JaneBuzJane) ([talk](https://meta.miraheze.org/wiki/User_talk:JaneBuzJane)) 13:51, 18 October 2026 (UTC)
 `{{ {{Support}} }}` - I believe it can be helpful. [Unfunktion](https://meta.miraheze.org/wiki/User:Unfunktion) ([talk](https://meta.miraheze.org/wiki/User_talk:Unfunktion)) 16:21, 18 October 2026 (UTC)
 `{{ {{Support}} }}`.--[<span style="color:#00C0FF;">铁桶</span>](https://meta.miraheze.org/wiki/User:铁桶) ([Talk](https://meta.miraheze.org/wiki/User_Talk:铁桶)) 15:04, 19 October 2026 (UTC)
 `{{ {{support}} }}` [Jenny on Wiki](https://meta.miraheze.org/wiki/User:Jenny_on_Wiki) ([talk](https://meta.miraheze.org/wiki/User_talk:Jenny_on_Wiki)) 15:16, 24 October 2026 (UTC)

----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:Noticeboard/Request_for_feedback:_changes_to_default_MediaWiki_settings_(2))**