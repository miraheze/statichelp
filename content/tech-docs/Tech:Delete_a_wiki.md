---
title: Tech:Delete a wiki
---

Deleting a wiki is a fairly simple process if you have the required access and follow the process below.

A wiki must be marked as deleted through the ManageWiki interface before it can be deleted. This is simply going to `Special:ManageWiki/core/<dbname>`, where `<dbname>` represents the given wiki's database name, on `metawiki`.
* **Note:** This step should be completed by a [Steward](https://meta.miraheze.org/wiki/Stewards), usually following a request a [stewards' noticeboard](https://meta.miraheze.org/wiki/stewards'_noticeboard), notstanding wikis deleted pursuant to the [Terms of Use](https://meta.miraheze.org/wiki/Terms_of_Use)

Wikis are put on a timer - meaning they can only be deleted after a certain number of days (the current [Dormancy Policy](https://meta.miraheze.org/wiki/Dormancy_Policy) states that this is 14 days). Therefore, there are two methods to delete a wiki.

Performing the deletion if 14 days have passed:
* Run `mwscript extensions/CreateWiki/deleteWikis.php loginwiki <username>`
* You will then receive SQL DROP DATABASE syntax that you can use to run on the relevant database server.

Performing the deletion if 14 days have **not** passed:
* Run `mwscript extensions/CreateWiki/deleteWiki.php loginwiki --delete --deletewiki <wiki database>`
* Drop the database on the relevant database server.

[Category:Technology guidelines and guides](https://meta.miraheze.org/wiki/Category:Technology_guidelines_and_guides)

----
**Source**: [https://meta.miraheze.org/wiki/Tech:Delete_a_wiki](https://meta.miraheze.org/wiki/Tech:Delete_a_wiki)