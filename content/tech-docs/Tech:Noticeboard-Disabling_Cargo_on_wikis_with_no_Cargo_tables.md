---
title: Tech:Noticeboard/Disabling Cargo on wikis with no Cargo tables
---

`{{ {{Mbox|text=This page is a draft}} }}`
The **[Cargo](https://meta.miraheze.org/wiki/mw:Extension:Cargo)** extension has a history of performance problems and a large number of security vulnerabilities, with [cross-site scripting](https://meta.miraheze.org/wiki/w:Cross-site_scripting) (XSS) and [SQL injection](https://meta.miraheze.org/wiki/w:SQL_injection) (SQLi) being the most common (see [#Cargo vulnerabilities](#cargo-vulnerabilities) for more information). In light of the multitude of issues with Cargo and the availability of an alternative extension, [Bucket](https://meta.miraheze.org/wiki/mw:Extension:Bucket), the Technology Team is planning to reduce Cargo usage on Miraheze, with the ultimate goal of a full removal.

This page documents the first planned step, which is to disable Cargo on all wikis that enabled the extension in the past but are not actively using it.

## List of wikis 

If your wiki is on the list, the technology team will soon disable Cargo on the wiki. If your wiki is using Cargo but not on this list, we still recommend migrating away from Cargo. See [#Migrating away from Cargo](#migrating-away-from-cargo) for how to do so.

If you have any concerns, please respond in the [#Discussion](#discussion) section.

Only public wikis are included. Private wikis are excluded from the list to not reveal any information about them.

| Wiki | State | Visibility |
| --- | --- | --- |
| [Wiki Dddddddddddd](https://meta.miraheze.org/wiki/mh:1134819) | active | Public |
| [Appalling TikToks Wiki](https://meta.miraheze.org/wiki/mh:abysmaltiktokvideos) | closed | Public |
| [City of Smoke and Ash](https://meta.miraheze.org/wiki/mh:acosaa) | active | Public |
| [Aether Gazer Wiki](https://meta.miraheze.org/wiki/mh:aethergazer) | active | Public |
| [antiX Linux fan](https://meta.miraheze.org/wiki/mh:antixlinuxfan) | active | Public |
| [The Backrooms Wiki](https://meta.miraheze.org/wiki/mh:backrooms) | active | Public |
| [Blockland - Wiki](https://meta.miraheze.org/wiki/mh:blockland) | inactive | Public |
| [Borost](https://meta.miraheze.org/wiki/mh:borost) | active | Public |
| [Custom Gameshows Wiki](https://meta.miraheze.org/wiki/mh:cg) | active | Public |
| [Comfy Camp Archives](https://meta.miraheze.org/wiki/mh:comfycamp) | active | Public |
| [CSLE](https://meta.miraheze.org/wiki/mh:csle) | inactive | Public |
| [C.Syde&#39;s Wiki](https://meta.miraheze.org/wiki/mh:csydes) | active | Public |
| [ct777-wiki](https://meta.miraheze.org/wiki/mh:ct777) | active | Public |
| [Deep Adaptation - Adaption radicale](https://meta.miraheze.org/wiki/mh:deepadaptation) | closed | Public |
| [Degrees of Lewdity Wiki](https://meta.miraheze.org/wiki/mh:degreesoflewdity) | active | Public |
| [DOORS中文创意维基](https://meta.miraheze.org/wiki/mh:doorscnfansfanonhub) | active | Public |
| [Echoes of Vision](https://meta.miraheze.org/wiki/mh:echoesofvision) | active | Public |
| [Empire d&#39;Arsois](https://meta.miraheze.org/wiki/mh:empiredarsois) | active | Public |
| [Guia Galáctico](https://meta.miraheze.org/wiki/mh:esporo) | active | Public |
| [Evosystem Wiki](https://meta.miraheze.org/wiki/mh:evosystem) | active | Public |
| [Fiction and Fictional Settings Wiki](https://meta.miraheze.org/wiki/mh:fictionandfictionalsettingswiki) | active | Public |
| [GHGWIKI](https://meta.miraheze.org/wiki/mh:gamebaikeshuwiki) | active | Public |
| [Gapia Wiki](https://meta.miraheze.org/wiki/mh:gapia) | active | Public |
| [HammerBro101 Wiki](https://meta.miraheze.org/wiki/mh:hammerbro101) | active | Public |
| [Heart of Crown](https://meta.miraheze.org/wiki/mh:heartofcrown) | closed | Public |
| [Nyüjapapedia](https://meta.miraheze.org/wiki/mh:hismajestytheemperor) | active | Public |
| [The Hively Beeble](https://meta.miraheze.org/wiki/mh:hivesociety) | inactive | Public |
| [موسوعة فهرس القرآن الكريم](https://meta.miraheze.org/wiki/mh:islamiclibrary) | inactive | Public |
| [ポーランドボールwiki](https://meta.miraheze.org/wiki/mh:japolandball) | active | Public |
| [The Lands Of Liberos Project ](https://meta.miraheze.org/wiki/mh:landofliberos) | closed | Public |
| [Wiki Lớp Học Mật Ngữ](https://meta.miraheze.org/wiki/mh:lhmn) | active | Public |
| [LifeWiki](https://meta.miraheze.org/wiki/mh:life) | active | Public |
| [Lim Zhi Hao](https://meta.miraheze.org/wiki/mh:limzhihaowinston) | active | Public |
| [LUPW Wiki](https://meta.miraheze.org/wiki/mh:lupw) | active | Public |
| [Lust Doll Plus Wiki](https://meta.miraheze.org/wiki/mh:lustdollplus) | active | Public |
| [Mandaepedia](https://meta.miraheze.org/wiki/mh:mandaepedia) | active | Public |
| [Marathon Wiki](https://meta.miraheze.org/wiki/mh:marathon) | closed | Public |
| [Red&#39;s Worlds](https://meta.miraheze.org/wiki/mh:maraxia) | active | Public |
| [Minecraft Parkour Wiki](https://meta.miraheze.org/wiki/mh:mcpk) | active | Public |
| [Melayu Archipelago Wiki](https://meta.miraheze.org/wiki/mh:melayu) | active | Public |
| [Merc Storia English Wiki](https://meta.miraheze.org/wiki/mh:mercstoria) | active | Public |
| [Migdal ConLang Wiki](https://meta.miraheze.org/wiki/mh:migdal) | active | Public |
| [Neon Jungle Living Community Wiki](https://meta.miraheze.org/wiki/mh:neonjunglelc) | active | Public |
| [OC堆放间](https://meta.miraheze.org/wiki/mh:nknkoc) | active | Public |
| [Noctilucent: Before Dawn Wiki](https://meta.miraheze.org/wiki/mh:noctilucent) | active | Public |
| [Nontortion](https://meta.miraheze.org/wiki/mh:nontortion) | active | Public |
| [NU: carnival Wiki](https://meta.miraheze.org/wiki/mh:nucarnival) | active | Public |
| [ParentRatings](https://meta.miraheze.org/wiki/mh:parentratings) | inactive | Public |
| [Партопедия](https://meta.miraheze.org/wiki/mh:partopedia) | inactive | Public |
| [Philosophy Model](https://meta.miraheze.org/wiki/mh:philosophymodel) | active | Public |
| [Physikexperimente](https://meta.miraheze.org/wiki/mh:physikexperimente) | inactive | Public |
| [Project JoJo 2 Wiki](https://meta.miraheze.org/wiki/mh:pjj2) | active | Public |
| [Psychopragmatics](https://meta.miraheze.org/wiki/mh:pmatic) | inactive | Public |
| [The Stardust Archives](https://meta.miraheze.org/wiki/mh:projectstardustwiki) | active | Public |
| [ZWB Wiki](https://meta.miraheze.org/wiki/mh:pvzz2) | inactive | Public |
| [QueerSport](https://meta.miraheze.org/wiki/mh:queersport) | active | Public |
| [Rift Fishing](https://meta.miraheze.org/wiki/mh:riftfishing) | closed | Public |
| [Saimoe Wiki](https://meta.miraheze.org/wiki/mh:saimoe) | active | Public |
| [SkySaga Wiki](https://meta.miraheze.org/wiki/mh:skysaga) | active | Public |
| [Wiki_Some-Ideas_Quel Avenir](https://meta.miraheze.org/wiki/mh:somesideaswikiquelavenir) | inactive | Public |
| [Encyclopedia SpongeBobia](https://meta.miraheze.org/wiki/mh:spongebob) | active | Public |
| [Stella Sora Wiki](https://meta.miraheze.org/wiki/mh:stellasora) | active | Public |
| [Tampvan Wiki ](https://meta.miraheze.org/wiki/mh:tampvan) | active | Public |
| [Template Wiki](https://meta.miraheze.org/wiki/mh:templatewikiarchive) | active | Public |
| [Империя Скотта](https://meta.miraheze.org/wiki/mh:testopedia) | closed | Public |
| [DoveArchives](https://meta.miraheze.org/wiki/mh:thesohnlandwiki) | active | Public |
| [塔诺王国wiki站](https://meta.miraheze.org/wiki/mh:tnwgwiki) | active | Public |
| [东宁要览·东宁wiki](https://meta.miraheze.org/wiki/mh:tounae) | active | Public |
| [Трансформеры вики](https://meta.miraheze.org/wiki/mh:transformers) | active | Public |
| [Ucronías](https://meta.miraheze.org/wiki/mh:ucronias) | active | Public |
| [UpInTheSky Wiki](https://meta.miraheze.org/wiki/mh:upinthesky) | active | Public |
| [UtaMacross Wiki](https://meta.miraheze.org/wiki/mh:utamacross) | active | Public |
| [Vietnamese EnderBot](https://meta.miraheze.org/wiki/mh:vnenderbot) | active | Public |
| [Waste Of Space Wiki](https://meta.miraheze.org/wiki/mh:wasteofspace) | active | Public |
| [Союз вики](https://meta.miraheze.org/wiki/mh:wikiball) | active | Public |
| [WikiTacticalVoting](https://meta.miraheze.org/wiki/mh:wikitacticalvoting) | active | Public |
| [NSMBU Modding Wiki](https://meta.miraheze.org/wiki/mh:zenith) | active | Public |

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