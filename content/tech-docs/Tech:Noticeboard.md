---
title: Tech:Noticeboard
---

`{{ {{/header}} }}`

<!-- DO NOT MODIFY THIS AUTOARCHIVE VALUE UNLESS YOU KNOW WHAT YOU ARE DOING -->

```
{{ {{Autoarchive/config
|archive = Tech:Noticeboard/Archive %(counter)d
|algo = old(31d)
|counter = 1
|maxarchivesize = 150K
|archiveheader = {{Archive}} |minthreadstoarchive = 1
}} }}
```
 `{{ {{Navigation Miraheze}} }}`

## Server maintenance (again) 

We will be performing maintenance on our servers again on March 1st, 2025 from 18:45 until 20:45 UTC for hardware upgrades. We expect intermittent outages, so we highly recommend that you save your edits before then. We thank you for your understanding and appreciate your patience. [MacFan4000](https://meta.miraheze.org/wiki/User:MacFan4000) ([Talk](https://meta.miraheze.org/wiki/User_talk:MacFan4000) [Contribs](https://meta.miraheze.org/wiki/Special:Contributions/MacFan4000)) 14:28, 28 February 2025 (UTC)

   The maintenance has been postponed to Wednesday March 5th from 18:45 until 20:45 UTC. [MacFan4000](https://meta.miraheze.org/wiki/User:MacFan4000) ([Talk](https://meta.miraheze.org/wiki/User_talk:MacFan4000) [Contribs](https://meta.miraheze.org/wiki/Special:Contributions/MacFan4000)) 17:53, 1 March 2025 (UTC)

## Extension removals for the MediaWiki 1.45 update 

The technology team is planning to remove several extensions as a part of the upgrade to MediaWiki 1.45. See [the discussion page](https://meta.miraheze.org/wiki/Tech%3ANoticeboard/Removing_extensions_for_the_MediaWiki_1.45_upgrade) for details. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 02:46, 9 February 2026 (UTC)

## New request for feedback on changes to Miraheze's default MediaWiki configuration 

Please go to [Tech:Noticeboard/Request for feedback: changes to default MediaWiki settings](/tech-docs/technoticeboard-request_for_feedback_changes_to_default_mediawiki_settings) to view the proposals and voice your opinions. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 00:47, 24 April 2026 (UTC)

   You got it. [DarkMatterMan4500](https://meta.miraheze.org/wiki/User:DarkMatterMan4500) ([talk](https://meta.miraheze.org/wiki/User_talk:DarkMatterMan4500)) ([contribs](https://meta.miraheze.org/wiki/Special:Contributions/DarkMatterMan4500)) 17:02, 16 May 2026 (UTC)

## Maps has been globally disabled 

Hello,

Following credible reports of a security vulnerability in the [Maps extension](https://meta.miraheze.org/wiki/mw:Extension:Maps), we have decided to disable the extension on all wikis until the security of it can be ensured. There are no signs of the vulnerability being used on Miraheze and we remain uncompromised.

We will be notifying you again once the extension is re-enabled. We apologize for the inconvenience and are happy to answer any questions regarding the matter.

[Skye (Miraheze)](https://meta.miraheze.org/wiki/User:Skye_(Miraheze)) ([talk](https://meta.miraheze.org/wiki/User_talk:Skye_(Miraheze)))<br />
MediaWiki Specialist<br />
02:33, 27 May 2026 (UTC)

   Cargo extension’s default map feature is unfortunately not very user-friendly for our use case.
   We previously relied on the Maps extension to use Leaflet-based interactive maps together with Cargo queries.
   Is there any recommended alternative for interactive mapping after the removal of Maps? [Kijo Sora](https://meta.miraheze.org/wiki/User:Kijo_Sora) ([talk](https://meta.miraheze.org/wiki/User_talk:Kijo_Sora)) 05:06, 27 May 2026 (UTC)
   I think this might be (related to) [issue #898 on ProfessionalWiki/Maps@Github](https://meta.miraheze.org/wiki/github:ProfessionalWiki/Maps/issues/898) (Maps 12.1.2 vs. SMW 7.0.0); correct me otherwise. --[Routhwick](https://meta.miraheze.org/wiki/User:Routhwick) ([talk](https://meta.miraheze.org/wiki/User_talk:Routhwick)) 08:21, 27 May 2026 (UTC)
      [On the other hand](https://meta.miraheze.org/wiki/github:ProfessionalWiki/Maps/security/advisories/GHSA-4h7g-5542-v3fc)... --[Routhwick](https://meta.miraheze.org/wiki/User:Routhwick) ([talk](https://meta.miraheze.org/wiki/User_talk:Routhwick)) 08:12, 29 May 2026 (UTC)
         CVSS 8.6. Yes, the extension has to remain offline until that's fixed. --[Robkelk](https://meta.miraheze.org/wiki/User:Robkelk) ([talk](https://meta.miraheze.org/wiki/User_talk:Robkelk)) 12:54, 29 May 2026 (UTC)
   Furthermore, it wasn't functioning fully anymore. [Wazzimagiygg](https://meta.miraheze.org/wiki/User:Wazzimagiygg) ([talk](https://meta.miraheze.org/wiki/User_talk:Wazzimagiygg)) 18:45, 27 May 2026 (UTC)
      If you're talking about the issue where some map tiles don't load, perhaps [phab:T15102](https://meta.miraheze.org/wiki/phab:T15102) might address the matter. --[Robkelk](https://meta.miraheze.org/wiki/User:Robkelk) ([talk](https://meta.miraheze.org/wiki/User_talk:Robkelk)) 18:58, 27 May 2026 (UTC)

Hoping you can sort out the issue, maps are an important element for my wikis. [Bertie](https://meta.miraheze.org/wiki/User:Bertie) ([talk](https://meta.miraheze.org/wiki/User_talk:Bertie)) 06:18, 27 May 2026 (UTC)

I'm having trouble finding a CVE for this vulnerability (although I admit it's been nearly a decade since I was involved in IT security, so maybe I'm looking in the wrong place). What's the CVSS score for this vuln, and has the extension's maintainers provided a timeline on mitigation and resolution of the issue? In the meantime, what's available as a replacement? --[Robkelk](https://meta.miraheze.org/wiki/User:Robkelk) ([talk](https://meta.miraheze.org/wiki/User_talk:Robkelk)) 12:01, 27 May 2026 (UTC)

   Not all vulnerabilities end up getting a CVE, and even then it wouldn't be public yet. Unfortunately there is no direct drop-in replacement but you may have some success with [Kartographer](https://meta.miraheze.org/wiki/mw:Extension:Kartographer). We've also determined the need to perform a review of the extension for more issues. We don't have an exact timeline for this, but we aim to minimize its inavailability due to high usage and lack of replacement. [Skye](https://meta.miraheze.org/wiki/User:Skye) ([talk](https://meta.miraheze.org/wiki/User_talk:Skye)) 21:01, 27 May 2026 (UTC)
      Kartographer has its own share of bugs, as documented this month at [phab:T15384](https://meta.miraheze.org/wiki/phab:T15384). --[Routhwick](https://meta.miraheze.org/wiki/User:Routhwick) ([talk](https://meta.miraheze.org/wiki/User_talk:Routhwick)) 21:17, 27 May 2026 (UTC)
         Yeah, that makes sense. [DarkMatterMan4500](https://meta.miraheze.org/wiki/User:DarkMatterMan4500) ([talk](https://meta.miraheze.org/wiki/User_talk:DarkMatterMan4500)) ([contribs](https://meta.miraheze.org/wiki/Special:Contributions/DarkMatterMan4500)) 16:49, 21 June 2026 (UTC)

## Changes to Miraheze's default MediaWiki configuration 

Following a successful [Request for Feedback](/tech-docs/technoticeboard-request_for_feedback_changes_to_default_mediawiki_settings), the Technology Team is making several changes to Miraheze's default MediaWiki configurations. We believe they are a net positive for most wikis. If they do not work well for your wiki, you can change the setting back on ManageWiki. The configuration changes are as follows:
* `wgNativeImageLazyLoading` is enabled.
* `wgRestrictDisplayTitle` is disabled.
* `wgArticleCountMethod` is changed from `link` to `any`.
* `wgTabberNeueEnableAnimation` is disabled.
* `wgVectorResponsive` is set to `true` for all new wikis. Existing wikis are unaffected.
Please note that if you have changed the setting manually on ManageWiki before, it will not be changed by us. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 11:58, 15 June 2026 (UTC)

----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:Noticeboard)**