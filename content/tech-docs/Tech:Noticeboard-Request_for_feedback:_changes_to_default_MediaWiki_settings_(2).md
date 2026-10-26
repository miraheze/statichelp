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

```
{{ {{Discussion
|comment=Closed as successful. [[User:PetraMagna|PetraMagna]] ([[User talk:PetraMagna|talk]]) 00:17, 25 October 2026 (UTC)
|1=
'''[[mw:Help:Edit Recovery|Edit Recovery]]''' saves unsaved changes in the source editor to the browser's local storage, so that work is not lost when the browser crashes, the tab is closed by accident, or the session expires. Next time the user opens the editor for that page, they are offered to restore their changes.

<code>$wgEnableEditRecovery</code> is enabled by default, but the feature stays hidden behind a user preference that is off by default. Most do not know it exists, so in practice it is barely used. This proposal sets <code>$wgDefaultUserOptions['editrecovery']</code> to <code>1</code> so that everyone gets this feature unless they turn it off in [[Special:Preferences]].

=== Discussion 2 ===
Please discuss below. [[User:PetraMagna|PetraMagna]] ([[User talk:PetraMagna|talk]]) 00:31, 14 October 2026 (UTC)

:{{Support}} [[User:Maitian MaiLin|Maitian MaiLin]] ([[User talk:Maitian MaiLin|talk]]) 11:19, 14 October 2026 (UTC)
:Kind of a random question, but does this work for anon editors? I'm assuming not, since the toggle is in Special:Preferences. I'm just curious. [[User:JaneBuzJane|JaneBuzJane]] ([[User talk:JaneBuzJane|talk]]) 02:09, 15 October 2026 (UTC)
::Per documentation on mw.org [[mw:Manual:$wgDefaultUserOptions|wgDefaultUserOptions]] "will override the default user preferences for anonymous visitors and users who have not customized their preferences". So my guess would be it does work for anons. [[User:PetraMagna|PetraMagna]] ([[User talk:PetraMagna|talk]]) 06:35, 16 October 2026 (UTC)
:This is a really imporatant and useful feature. I'm really sick of losing my edits for Internet lags and CAPTCHAs while contributing on Fandom. We can't count on everyone to pay enough attention to their [[Special:Preferences]], which is a really long page.--[[User:AABb1221|AABb1221]] ([[User talk:AABb1221|talk]]) 04:19, 14 October 2026 (UTC)
:{{Support}} as proposer. [[User:PetraMagna|PetraMagna]] ([[User talk:PetraMagna|talk]]) 06:35, 16 October 2026 (UTC)
:{{support}} on the grounds of having lost more edits than I can count to page reloads. - [[User:Sakurababochka|<span style="color:#a25ac9">Sakurababochka</span>]] <small> ([[Usertalk:Sakurababochka|<span style="color:#75c9af">talk</span>]]) </small> 08:18, 16 October 2026 (UTC)
:{{support|strongest}} [[User:Jenny on Wiki|Jenny on Wiki]] ([[User talk:Jenny on Wiki|talk]]) 14:16, 16 October 2026 (UTC)
:{{support}} per proposal. - [[User:JaneBuzJane|JaneBuzJane]] ([[User talk:JaneBuzJane|talk]]) 13:49, 18 October 2026 (UTC)
:{{Support|partial}} - ‎ I hardly use edit recovery, only once. But maybe, just in case. It would be helpful. [[User:Unfunktion|Unfunktion]] ([[User talk:Unfunktion|talk]]) 16:12, 18 October 2026 (UTC)
:{{Support}}.--[[User:铁桶|<span style="color:#00C0FF;">铁桶</span>]] ([[User Talk:铁桶|Talk]]) 15:04, 19 October 2026 (UTC)
:{{s}} per rationale above.--[[User:AABb1221|AABb1221]] ([[User talk:AABb1221|talk]]) 11:31, 24 October 2026 (UTC)
}} }}
```

## Proposal 3: do not enable MobileFrontend and MinervaNeue for new wikis 

```
{{ {{Discussion
|comment=Closed as successful. [[User:PetraMagna|PetraMagna]] ([[User talk:PetraMagna|talk]]) 00:17, 25 October 2026 (UTC)
|1=
'''[[mw:Extension:MobileFrontend|MobileFrontend]]''' (MF) and '''[[mw:Skin:MinervaNeue|MinervaNeue]]''' are enabled by default mostly because Vector 2010 does not work on small screens. We no longer use Vector 2010 as the default, and our default skin (Vector 2022) alongside the most popular ones (Timeless, Citizen, Cosmos, Monobook) are all responsive.

With MobileFrontend enabled, mobile visitors see Minerva instead of the wiki's default skin. Minerva is known is known to break and hide page content. For example, [[Special:PermaLink/489799]] looks fine on Vector 2022, but it is broken on mobile view ("Why Donate to Miraheze?" looks different), as reported on [https://discord.com/channels/407504499280707585/615786602454581249/1415156187074134109 Discord]. MobileFrontend hiding navboxes is also a known quirk that requires ManageWiki tweaks to resolve.

This discrepancy is a major source of confusion. Disabling MF and Minerva for new wikis gives mobile visitors the similar experience as desktop visitors, and wikis that prefer Minerva can still opt in. Existing wikis are not affected and can continue to use Minerva if they so desire.

<s>If a wiki changes its default skin to one that is not responsive, such as Vector legacy, MobileFrontend and MinervaNeue could be enabled automatically. I am not sure whether this is worth the added complexity, and some wikis might intentionally not use MobileFrontend alongside Vector legacy. This addition goes into proposal 3b.</s> This proposal was drafted as 3b but has been withdrawn due to multiple concerns.

=== Discussion 3a ===
Not enabling MobileFrontend and MinervaNeue for new wikis. [[User:PetraMagna|PetraMagna]] ([[User talk:PetraMagna|talk]]) 00:31, 14 October 2026 (UTC)

:Minerva also ignores any custom sidebar the wiki has, which can potentially make mobile navigation much more fiddly. This isn't (as far as I know) made readily apparent anywhere, and I've seen it cause confusion more than once. - [[User:Sakurababochka|<span style="color:#a25ac9">Sakurababochka</span>]] <small> ([[Usertalk:Sakurababochka|<span style="color:#75c9af">talk</span>]]) </small> 09:25, 14 October 2026 (UTC)
:{{support}} as proposer. [[User:PetraMagna|PetraMagna]] ([[User talk:PetraMagna|talk]]) 06:35, 16 October 2026 (UTC)
::I should note that we plan to add a help message in ManageWiki for $wgDefaultSkin telling users of Vector legacy to enable MobileFrontend and Minerna if this proposal passes. [[User:PetraMagna|PetraMagna]] ([[User talk:PetraMagna|talk]]) 06:36, 16 October 2026 (UTC)
:{{support}} per my comments on this proposal from the drafting period. - [[User:Sakurababochka|<span style="color:#a25ac9">Sakurababochka</span>]] <small> ([[Usertalk:Sakurababochka|<span style="color:#75c9af">talk</span>]]) </small> 08:18, 16 October 2026 (UTC)
:{{support}} - assuming {{code|$wgVectorResponsive}} is(/will be) on by default. [[User:Rexogamer|Rexogamer]] ([[User talk:Rexogamer|talk]]) 17:24, 16 October 2026 (UTC)
::Yep. It is the default on new wikis created on Miraheze. Older wikis retain the old default (disabled) per our [[Tech:Noticeboard/Request_for_feedback:_changes_to_default_MediaWiki_settings|previous RfF]]. [[User:PetraMagna|PetraMagna]] ([[User talk:PetraMagna|talk]]) 08:51, 17 October 2026 (UTC)
:{{support|strongest}} Support per proposal. In my experience they cause more problems than they solve. - [[User:JaneBuzJane|JaneBuzJane]] ([[User talk:JaneBuzJane|talk]]) 13:51, 18 October 2026 (UTC)
:{{Support|strong}} - I feel these kinda make navigating wikis difficult, especially for navboxes. [[User:Unfunktion|Unfunktion]] ([[User talk:Unfunktion|talk]]) 16:17, 18 October 2026 (UTC)
:{{Note}} MobileFrontend is compatible with other skins (Vector, Timeless, Monobook, Citizen), so that could potentially be an option. [[User:MacFan4000|MacFan4000]] <sup>([[User talk:MacFan4000|Talk]] [[Special:Contributions/MacFan4000|Contribs]])</sup> 16:32, 19 October 2026 (UTC)
:{{support}} [[User:Jenny on Wiki|Jenny on Wiki]] ([[User talk:Jenny on Wiki|talk]]) 15:16, 24 October 2026 (UTC)
{{Collapse top|title=Withdrawn proposal}}

=== Discussion 3b ===
Implement proposal 3a, and then automatically enabling MobileFrontend and MinervaNeue when a new wiki switches to a skin that is not responsive. [[User:PetraMagna|PetraMagna]] ([[User talk:PetraMagna|talk]]) 00:31, 14 October 2026 (UTC)

:Sounds unnecessarily complicated, and this requires sorting out which skins are responsive and which are not. —[[User:Honoka55|<span style="color:#DDAACC">Honoka55</span>]]｜[[User talk:Honoka55|<span style="color:#CCAA88">talk</span>]] 11:31, 14 October 2026 (UTC)
:I would propose removing 3b as an option - it would be difficult to keep track of which skins are responsive and which are not, but moreover, it could cause a lot of confusion for editors who enable a skin and then see a different one on mobile than they selected. - [[User:JaneBuzJane|JaneBuzJane]] ([[User talk:JaneBuzJane|talk]]) 02:07, 15 October 2026 (UTC)
:Thanks for the feedback. I will withdraw this proposal. [[User:PetraMagna|PetraMagna]] ([[User talk:PetraMagna|talk]]) 06:20, 16 October 2026 (UTC)
{{Collapse bottom}}
}} }}
```

## Proposal 4: add TemplateData to default extensions 

```
{{ {{Discussion
|comment=Closed as successful. [[User:PetraMagna|PetraMagna]] ([[User talk:PetraMagna|talk]]) 00:17, 25 October 2026 (UTC)
|1=
'''[[mw:Extension:TemplateData|TemplateData]]''' lets template editors describe a template's parameters, which is especially useful for VisualEditor.

TemplateData is also required by [[mw:Extension:TemplateWizard|TemplateWizard]], which could also be enabled, but I do not know enough about it. Maybe someone else can create a separate proposal for TemplateWizard.

=== Discussion 4 ===
Please discuss below. [[User:PetraMagna|PetraMagna]] ([[User talk:PetraMagna|talk]]) 00:31, 14 October 2026 (UTC)

:Surprised this isn't already the case. If VisualEditor is now enabled by default, editing templates would be really hard without TemplateData. [[User:KockaAdmiralac|KockaAdmiralac]] ([[User talk:KockaAdmiralac|talk]]) 22:40, 14 October 2026 (UTC)
::I believe you were the person who mentioned TemplateData last time, but it was too late for new proposals, so TemplateData waited until this RfF. [[User:PetraMagna|PetraMagna]] ([[User talk:PetraMagna|talk]]) 06:37, 16 October 2026 (UTC)
:{{support}} as proposer. [[User:PetraMagna|PetraMagna]] ([[User talk:PetraMagna|talk]]) 06:37, 16 October 2026 (UTC)
:{{Abstain}}, since I am not familiar with the extension and it would be remiss of me to vote as though I was. - [[User:Sakurababochka|<span style="color:#a25ac9">Sakurababochka</span>]] <small> ([[Usertalk:Sakurababochka|<span style="color:#75c9af">talk</span>]]) </small> 08:18, 16 October 2026 (UTC)
:{{support}} - ...it isn't already? [[User:Rexogamer|Rexogamer]] ([[User talk:Rexogamer|talk]]) 17:15, 16 October 2026 (UTC)
:{{support}} per proposal. - [[User:JaneBuzJane|JaneBuzJane]] ([[User talk:JaneBuzJane|talk]]) 13:51, 18 October 2026 (UTC)
:{{Support}} - I believe it can be helpful. [[User:Unfunktion|Unfunktion]] ([[User talk:Unfunktion|talk]]) 16:21, 18 October 2026 (UTC)
:{{Support}}.--[[User:铁桶|<span style="color:#00C0FF;">铁桶</span>]] ([[User Talk:铁桶|Talk]]) 15:04, 19 October 2026 (UTC)
:{{support}} [[User:Jenny on Wiki|Jenny on Wiki]] ([[User talk:Jenny on Wiki|talk]]) 15:16, 24 October 2026 (UTC)
}} }}
```

----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:Noticeboard/Request_for_feedback:_changes_to_default_MediaWiki_settings_(2))**