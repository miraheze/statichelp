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

## The state of the ReplaceText extension 

Since May 11, Miraheze has [disabled](https://meta.miraheze.org/wiki/github:miraheze/mw-config/commit/eb722ed3e703) `wgCompressRevisions` globally, thanks to our increase in storage in our database servers due to the move to our new data center. Thanks to this, we have also been able to bring back an extension that relied on this setting being disabled, [ReplaceText](https://meta.miraheze.org/wiki/mediawikiwiki:Extension:ReplaceText). Due to how this extension works, it **requires** that revisions not be compressed.

Now, disabling `wgCompressRevisions` doesn't retroactively decompress existing revisions, what it does is that it no longer compresses new revisions. Revisions of pages made before this setting was turned off are still compressed. ReplaceText doesn't work properly when the current revision of a page is a compressed revision. Therefore, wikis made on or before May 11 will very likely have issues with this extension still. Therefore, this extension is currently restricted and to enable it you must request it at [Steward requests/Restricted changes](https://meta.miraheze.org/wiki/Steward_requests/Restricted_changes)

[Stewards](https://meta.miraheze.org/wiki/Stewards) and [Wiki Mechanics](https://meta.miraheze.org/wiki/Wiki_Mechanics), this extension can be enabled on request at [SR/RC](https://meta.miraheze.org/wiki/SR/RC) for wikis created **after** May 11. If a wiki created prior to this date requests this extension, a member of the [Technology Team](/tech-docs/techvolunteers) has to manually verify that *all* of the pages' current revisions are not from before this date before being enabled. [Alex (Miraheze)](https://meta.miraheze.org/wiki/User:Alex_(Miraheze)) ([talk](https://meta.miraheze.org/wiki/User_talk:Alex_(Miraheze))) 18:34, 21 August 2024 (UTC)

## MediaWiki 1.43 upgrade 

Miraheze will be upgrading all wikis to MediaWiki 1.43 on Monday, January 27th at 18:00 UTC. This is expected to take approximately one hour and end at 19:00 UTC. During this window there may be intermittent downtime, but edits will be possible. Thank you for your understanding! [MacFan4000](https://meta.miraheze.org/wiki/User:MacFan4000) ([Talk](https://meta.miraheze.org/wiki/User_talk:MacFan4000) [Contribs](https://meta.miraheze.org/wiki/Special:Contributions/MacFan4000)) 22:01, 24 January 2025 (UTC)

## Server maintenance 

On February 22nd, 2025 from 18:45 until 23:30 UTC we will be performing maintenance on our servers. During this time we expect intermittent outages of all services. We will post updates as needed, and we thank you for your understanding. [MacFan4000](https://meta.miraheze.org/wiki/User:MacFan4000) ([Talk](https://meta.miraheze.org/wiki/User_talk:MacFan4000) [Contribs](https://meta.miraheze.org/wiki/Special:Contributions/MacFan4000)) 02:15, 12 February 2025 (UTC)

      This planned maintenance has been postponed due to late arriving parts. We will post again when a new date is known. [MacFan4000](https://meta.miraheze.org/wiki/User:MacFan4000) ([Talk](https://meta.miraheze.org/wiki/User_talk:MacFan4000) [Contribs](https://meta.miraheze.org/wiki/Special:Contributions/MacFan4000)) 20:42, 21 February 2025 (UTC)

         The maintenance will now take place on Wednesday February 26th from 18:45 until 23:30 UTC. Once again we expect intermittent outages of all services. [MacFan4000](https://meta.miraheze.org/wiki/User:MacFan4000) ([Talk](https://meta.miraheze.org/wiki/User_talk:MacFan4000) [Contribs](https://meta.miraheze.org/wiki/Special:Contributions/MacFan4000)) 17:58, 22 February 2025 (UTC)

## Server maintenance (again) 

We will be performing maintenance on our servers again on March 1st, 2025 from 18:45 until 20:45 UTC for hardware upgrades. We expect intermittent outages, so we highly recommend that you save your edits before then. We thank you for your understanding and appreciate your patience. [MacFan4000](https://meta.miraheze.org/wiki/User:MacFan4000) ([Talk](https://meta.miraheze.org/wiki/User_talk:MacFan4000) [Contribs](https://meta.miraheze.org/wiki/Special:Contributions/MacFan4000)) 14:28, 28 February 2025 (UTC)

   The maintenance has been postponed to Wednesday March 5th from 18:45 until 20:45 UTC. [MacFan4000](https://meta.miraheze.org/wiki/User:MacFan4000) ([Talk](https://meta.miraheze.org/wiki/User_talk:MacFan4000) [Contribs](https://meta.miraheze.org/wiki/Special:Contributions/MacFan4000)) 17:53, 1 March 2025 (UTC)

## Extension removals for the MediaWiki 1.45 update 

The technology team is planning to remove several extensions as a part of the upgrade to MediaWiki 1.45. See [the discussion page](https://meta.miraheze.org/wiki/Tech%3ANoticeboard/Removing_extensions_for_the_MediaWiki_1.45_upgrade) for details. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 02:46, 9 February 2026 (UTC)

----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:Noticeboard)**