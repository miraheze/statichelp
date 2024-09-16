---
title: Tech:Translating Miraheze extensions/sv
---


Miraheze utvecklar och underhåller några egna tillägg, till exempel [CreateWiki](https://meta.miraheze.org/wiki/github:miraheze/CreateWiki) och [ManageWiki](https://meta.miraheze.org/wiki/github:miraheze/ManageWiki). Då Miraheze har användare med lite eller inga kunskaper i engelska, är internationalisering viktigt.

Vi använder för närvarande [translatewiki.net](https://meta.miraheze.org/wiki/translatewiki:) för översättning av CreateWiki och ManageWiki.

## TranslateWiki-processen 

* Lägg till strängar på en.json
* Translatewiki.net-botten hämtar koden när den importerar strängarna, och så visas den för översättare så de kan översätta.
* Översättare på Translatewiki.net översätter texterna
* Translatewiki.net-botten ger $lang.json när exportbotten har körts
* De rullas sen ut på Miraheze-nätet (undermodulen måste vara uppdaterad)

[Category:Tech](https://meta.miraheze.org/wiki/Category:Tech)

----
**Source**: https://meta.miraheze.org/wiki/Tech:Translating_Miraheze_extensions/sv