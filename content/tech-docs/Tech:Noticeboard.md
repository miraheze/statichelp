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
   I'd like to kindly ask if there's any news yet regarding this extension? Without maps (GeoJSON), my wiki isn't very useful, and almost every wiki page displays a map in an infobox. [Weltbibliographie](https://meta.miraheze.org/wiki/User:Weltbibliographie) ([talk](https://meta.miraheze.org/wiki/User_talk:Weltbibliographie)) 18:11, 31 July 2026 (UTC)
      Another vulnerability was found: [https://github.com/ProfessionalWiki/Maps/security/advisories/GHSA-rg4f-xvhj-mw22](https://github.com/ProfessionalWiki/Maps/security/advisories/GHSA-rg4f-xvhj-mw22)
      Considering this was found using Claude Code, the same tool that the maintainer uses, we have serious doubts that the maintainer has even considered security at all. [TheWWRNerdGuy](https://meta.miraheze.org/wiki/User:TheWWRNerdGuy) ([talk](https://meta.miraheze.org/wiki/User_talk:TheWWRNerdGuy)) 18:14, 31 July 2026 (UTC)

Hoping you can sort out the issue, maps are an important element for my wikis. [Bertie](https://meta.miraheze.org/wiki/User:Bertie) ([talk](https://meta.miraheze.org/wiki/User_talk:Bertie)) 06:18, 27 May 2026 (UTC)

I'm having trouble finding a CVE for this vulnerability (although I admit it's been nearly a decade since I was involved in IT security, so maybe I'm looking in the wrong place). What's the CVSS score for this vuln, and has the extension's maintainers provided a timeline on mitigation and resolution of the issue? In the meantime, what's available as a replacement? --[Robkelk](https://meta.miraheze.org/wiki/User:Robkelk) ([talk](https://meta.miraheze.org/wiki/User_talk:Robkelk)) 12:01, 27 May 2026 (UTC)

   Not all vulnerabilities end up getting a CVE, and even then it wouldn't be public yet. Unfortunately there is no direct drop-in replacement but you may have some success with [Kartographer](https://meta.miraheze.org/wiki/mw:Extension:Kartographer). We've also determined the need to perform a review of the extension for more issues. We don't have an exact timeline for this, but we aim to minimize its inavailability due to high usage and lack of replacement. [Skye](https://meta.miraheze.org/wiki/User:Skye) ([talk](https://meta.miraheze.org/wiki/User_talk:Skye)) 21:01, 27 May 2026 (UTC)
      Kartographer has its own share of bugs, as documented this month at [phab:T15384](https://meta.miraheze.org/wiki/phab:T15384). --[Routhwick](https://meta.miraheze.org/wiki/User:Routhwick) ([talk](https://meta.miraheze.org/wiki/User_talk:Routhwick)) 21:17, 27 May 2026 (UTC)
         Yeah, that makes sense. [DarkMatterMan4500](https://meta.miraheze.org/wiki/User:DarkMatterMan4500) ([talk](https://meta.miraheze.org/wiki/User_talk:DarkMatterMan4500)) ([contribs](https://meta.miraheze.org/wiki/Special:Contributions/DarkMatterMan4500)) 16:49, 21 June 2026 (UTC)

It's been a month and a half since the last update on this. Could we get a status update, please, even if it's "no change since the end of July"? -- [Robkelk](https://meta.miraheze.org/wiki/User:Robkelk) ([talk](https://meta.miraheze.org/wiki/User_talk:Robkelk)) 00:25, 20 September 2026 (UTC)

   After nearly half a year without maps in my map-based wiki, so I’d like to ask again if there’s any news and whether the extension might be available again soon. Now that it’s winter, I’d like to work on my wiki full steam ahead and get it online in a few months, but unfortunately that’s not possible with broken links instead of maps showing regional outlines. Thanks for any updates! [Weltbibliographie](https://meta.miraheze.org/wiki/User:Weltbibliographie) ([talk](https://meta.miraheze.org/wiki/User_talk:Weltbibliographie)) 10:32, 14 November 2026 (UTC)
      There are no updates [RhinosF1 (Miraheze)](https://meta.miraheze.org/wiki/User:RhinosF1_(Miraheze)) ([talk](https://meta.miraheze.org/wiki/User_talk:RhinosF1_(Miraheze))) 10:38, 14 November 2026 (UTC)
      the closest thing to an update is [phorge:T15794#330174](https://meta.miraheze.org/wiki/phorge:T15794#330174). [Jenny on Wiki](https://meta.miraheze.org/wiki/User:Jenny_on_Wiki) ([talk](https://meta.miraheze.org/wiki/User_talk:Jenny_on_Wiki)) 12:12, 15 November 2026 (UTC)
         After reading T15794 and then reading T15738 which was linked from that ticket, The comment "If we ever re-enable the extension" made by PetraMagna in T15738 in early August makes me worry. Are we *ever* going to get Maps back? If we're not going to get Maps back, please provide the migration strategy to a replacement extension. -- [Robkelk](https://meta.miraheze.org/wiki/User:Robkelk) ([talk](https://meta.miraheze.org/wiki/User_talk:Robkelk)) 14:10, 15 November 2026 (UTC)

## Extension removal for the MediaWiki 1.46 update 

As the [MediaWiki 1.46](https://meta.miraheze.org/wiki/MediaWiki/1.46) update draws near, the technology team is planning to remove several MediaWiki extensions due to both technical issues and perceived lack of usefulness/community interest.

The list of extensions is on [Tech:Noticeboard/Removing extensions for the MediaWiki 1.46 upgrade](/tech-docs/technoticeboard-removing_extensions_for_the_mediawiki_1.46_upgrade). If your wiki is affected and you want to keep a particular extension, please join the discussion and explain why the extension is important to your wiki. Administrators and bureaucrats on affected wikis will also receive a Echo notification shortly. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 01:22, 19 July 2026 (UTC)

## New Request for Feedback: RequestWiki redesign 

Please provide your comments on [Request for Feedback: RequestWiki redesign](https://meta.miraheze.org/wiki//Request_for_Feedback:_RequestWiki_redesign) if you have any opinions there.

Thank you,

[Universal Omega (Miraheze)](https://meta.miraheze.org/wiki/User:Universal_Omega_(Miraheze)) ([talk](https://meta.miraheze.org/wiki/User_talk:Universal_Omega_(Miraheze))) 20:09, 12 September 2026 (UTC)

## New Request for feedback on changes to default MediaWiki settings 

A discussion is on-going about several proposed changes to Miraheze's default MediaWiki settings at [Tech:Noticeboard/Request for feedback: changes to default MediaWiki settings (2)](/tech-docs/technoticeboard-request_for_feedback_changes_to_default_mediawiki_settings_(2)). Please cast your vote or express your thoughts about these changes. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 02:04, 18 October 2026 (UTC)

## Recent breaking change to ManageWiki extension 

It looks like the [ManageWiki](https://meta.miraheze.org/wiki/mw:Extension:ManageWiki) extension underwent some significant upgrades. While laudable, it seems the changes caused some unnecessary breaking effects, deleting non-standard user groups. On [<code>librarymakerswiki</code>](https://meta.miraheze.org/wiki/mh:librarymakers), I [created](https://meta.miraheze.org/wiki/mh:librarymakers:Special:Redirect/logid/1787) a `gatekeeper` user group, which now no longer exists. In another case, on [<code>hypotheticalweatherwiki</code>](https://meta.miraheze.org/wiki/mh:hypotheticalweather), [Drew Indigo (nee Hypercane)](https://meta.miraheze.org/wiki/User:Drew_Indigo) had to re-add `rollbacker` to me despite never removing it. I believe these are related and wanted to send a note that this change had breaking effects, so you can highlight this for the Technology Team in terms of potential training gaps (i.e., missed script run, etc.). [Doug](https://meta.miraheze.org/wiki/User:Doug) ([talk](https://meta.miraheze.org/wiki/User_talk:Doug)) 19:46, 22 November 2026 (UTC)

----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:Noticeboard)**