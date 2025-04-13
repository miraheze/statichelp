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

## GlobalBlocking affecting account autocreation 

On MediaWiki 1.42, the GlobalBlocking extension, used by Miraheze [Stewards](https://meta.miraheze.org/wiki/Stewards) and [Global Administrators](https://meta.miraheze.org/wiki/Global_Administrators) to block IP addresses on all wikis, is now capable to stopping account autocreation if your IP is affected by a global block.

"Account autocreation" is a process your account goes through if you don't have a local account in a wiki but are logged in to Miraheze. An account is created for you automatically in this case by the CentralAuth extension in said wiki.

Previously, global blocks issues by Stewards and Global Administrators did not interfere with your ability to go through this process, however, in 1.42 this is no longer the case. Much like how you can't use Special:CreateAccount if your IP is under the effects of a block that prevents account creation, account autocreation is now stopped by global blocks.

Users that browse using VPNs and similar proxy services, which are a common target of global blocks, will be affected by this. You'll be unable to login to wikis you haven't logged in to before (wikis that don't show up on your [Special:CentralAuth](https://meta.miraheze.org/wiki/Special:CentralAuth) page).

If you're affected by this, you may be able to contact Stewards and Global Administrators for help. You can reach them on Meta via [Steward requests/Miscellaneous](https://meta.miraheze.org/wiki/Steward_requests/Miscellaneous) or via email at cvt `{{ {{@}} }}`miraheze.org. [Alex (Miraheze)](https://meta.miraheze.org/wiki/User:Alex_(Miraheze)) ([talk](https://meta.miraheze.org/wiki/User_talk:Alex_(Miraheze))) 15:43, 17 July 2024 (UTC)

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

----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:Noticeboard)**