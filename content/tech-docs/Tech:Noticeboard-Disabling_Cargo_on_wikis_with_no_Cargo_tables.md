---
title: Tech:Noticeboard/Disabling Cargo on wikis with no Cargo tables
---

`{{ {{Mbox|text=This page is a draft}} }}`
The **[Cargo](https://meta.miraheze.org/wiki/mw:Extension:Cargo)** extension has a history of performance problems and a large number of security vulnerabilities, with [cross-site scripting](https://meta.miraheze.org/wiki/w:Cross-site_scripting) (XSS) and [SQL injection](https://meta.miraheze.org/wiki/w:SQL_injection) (SQLi) being the most common (see [#Cargo vulnerabilities](#cargo-vulnerabilities) for more information). In light of the multitude of issues with Cargo and the availability of an alternative extension, [Bucket](https://meta.miraheze.org/wiki/mw:Extension:Bucket), the Technology Team is planning to reduce Cargo usage on Miraheze, with the ultimate goal of a full removal.

This page documents the first planned step, which is to disable Cargo on all wikis that enabled the extension in the past but are not actively using it.

## List of wikis 

If your wiki is on the list, the technology team will soon disable Cargo on the wiki. If your wiki is using Cargo but not on this list, we still recommend migrating away from Cargo. See [#Migrating away from Cargo](#migrating-away-from-cargo) for how to do so.

If you have any concerns, please respond in the [#Discussion](#discussion) section.

(list is TBD)

## Discussion 

__NEWSECTIONLINK__
Please reply here. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 23:24, 2 November 2026 (UTC)

## Appendix 

### Migrating away from Cargo 

We recommend using the [Bucket](https://meta.miraheze.org/wiki/mw:Extension:Bucket) extension, which offers features similar to those of Cargo. To make the transition easier for editors who do not want to write Lua, many pre-built modules are available on [Bucket Wiki](https://meta.miraheze.org/wiki/mh:bucket:), including [Module:Bucket](https://meta.miraheze.org/wiki/mh:bucket:) which offers a Cargo-like interface for storing and querying data.

### Cargo vulnerabilities 

XSS vulnerabilities allow the attacker to take over the wiki and gain access equivalent to an interface administrator/bureaucrat, and in 2026 alone the following XSS vulnerabilities are publicly disclosed: [https://phabricator.wikimedia.org/T416271](https://phabricator.wikimedia.org/T416271), [https://phabricator.wikimedia.org/T416368](https://phabricator.wikimedia.org/T416368), [https://phabricator.wikimedia.org/T416389](https://phabricator.wikimedia.org/T416389), [https://phabricator.wikimedia.org/T416402](https://phabricator.wikimedia.org/T416402), [https://phabricator.wikimedia.org/T424140](https://phabricator.wikimedia.org/T424140), [https://phabricator.wikimedia.org/T431567](https://phabricator.wikimedia.org/T431567), [https://phabricator.wikimedia.org/T435207](https://phabricator.wikimedia.org/T435207), [https://phabricator.wikimedia.org/T435206](https://phabricator.wikimedia.org/T435206), [https://phabricator.wikimedia.org/T435121](https://phabricator.wikimedia.org/T435121), [https://phabricator.wikimedia.org/T434977](https://phabricator.wikimedia.org/T434977), [https://phabricator.wikimedia.org/T434784](https://phabricator.wikimedia.org/T434784). SQLi is usually more severe but causes less harm on Miraheze's setup because we sandbox Cargo aggressively. Still, it allows the attacker to bring down a database. 2 of them have been discovered and publicized this year: [https://phabricator.wikimedia.org/T422774](https://phabricator.wikimedia.org/T422774) and [https://phabricator.wikimedia.org/T428274](https://phabricator.wikimedia.org/T428274).

Note that the lists above may be incomplete because newer vulnerabilities are not disclosed to the public.

----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:Noticeboard/Disabling_Cargo_on_wikis_with_no_Cargo_tables)**