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

__FORCETOC__

## Migration to new servers 

Thanks to the support of our generous donors thus far through the [Fundraiser](https://meta.miraheze.org/wiki/Fundraiser) (we're currently at `{{ {{#expr:({{raw::Fundraiser 2024/amount}}/20000)*100round0}} }}`% of our goal), Miraheze has been to move to better servers. You may have noticed faster load times. This is because of our new servers! We thank our generous donors for their help in achieving this goal!

Image migration to our new servers are still ongoing though. During this period, you may notice images go missing for brief periods of time. This is a normal hiccup of file migration and we apologize for the inconvenience. Below is an FAQ with some commonly asked questions which we hope will help you understand what is going on. If you have any questions, please feel free to ask on the [Community portal](https://meta.miraheze.org/wiki/Community_portal), [Discord](https://meta.miraheze.org/wiki/Discord), or [IRC](https://meta.miraheze.org/wiki/IRC). [<span style="color: skyblue; font-weight: bold;">Agent</span> <span style="color: lime; font-weight: bold;">Isai</span>](https://meta.miraheze.org/wiki/User:Agent_Isai) [<span style="color: orange; font-weight: bold;">Talk to me!</span>](https://meta.miraheze.org/wiki/User_talk:Agent_Isai) 20:24, 27 January 2024 (UTC)

### FAQ 

#### What is happening? 

Miraheze has moved most of its services to bigger, better servers that are be able to handle more traffic with less load time and errors.

We have finished database migration but image migration is still in progress.

#### Why? 

Our old servers were *very* underequipped to handle our growing demands. In addition, they were very slow and are "on their last leg" due to RAID disk failure.

#### How long will the migration take? 

Databases have been migrated.

Swift (images) might take around a week or less to migrate.

#### What is the migration schedule? 

Most core services have already been migrated or set up (such as MediaWiki and Phorge). The last remaining thing is Swift (files).

Currently, images are being copied to our new servers. This may take around a week but likely less.

#### What can I expect during the migration? 

Database migration is complete. You should not notice any on-wiki hiccups.

For images, they may appear missing at random times while Swift copies over files and recalculates their hash. Rest assured, nothing is lost.

#### When will we begin to see speed improvements? 

You can see them already! Wikis load *much* faster than before!

## MediaWiki 1.42 upgrade

Miraheze will be upgrading to 1.42 this Wednesday, July 17.

We will let everyone know ~ 30 minutes before we start the upgrade via [Discord](https://meta.miraheze.org/wiki/Discord), [IRC](https://meta.miraheze.org/wiki/IRC) (on the #miraheze channel) and [Mastodon](https://mastodon.social/@miraheze). [Alex (Miraheze)](https://meta.miraheze.org/wiki/User:Alex_(Miraheze)) ([talk](https://meta.miraheze.org/wiki/User_talk:Alex_(Miraheze))) 09:42, 15 July 2024 (UTC)

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

----
**Source**: [https://meta.miraheze.org/wiki/Tech:Noticeboard](https://meta.miraheze.org/wiki/Tech:Noticeboard)