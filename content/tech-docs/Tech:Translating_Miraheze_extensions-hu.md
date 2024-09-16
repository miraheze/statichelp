---
title: Tech:Translating Miraheze extensions/hu
---


A Miraheze fejleszt és karbantart néhány bővítményt, például a [CreateWiki](https://meta.miraheze.org/wiki/github:miraheze/CreateWiki) és a [ManageWiki](https://meta.miraheze.org/wiki/github:miraheze/ManageWiki) nevű bővítményt. Mivel a Mirahezének vannak olyan felhasználói, akik nem vagy csak korlátozottan tudnak angolul, a nemzetköziesítés fontos a felhasználók számára.

Jelenleg a [translatewiki.netet](https://meta.miraheze.org/wiki/translatewiki:) használjuk a CreateWiki és a ManageWiki fordításaihoz.

## A TranslateWiki folyamat 

* Sztringek hozzáadása az en.json fájlhoz
* A translatewiki.net bot húzza a kódot, amikor importálják a karakterláncokat, és ez megjelenik a fordítóknak a fordításhoz.
* A Translatewiki.net fordítói lefordítják a szövegeket
* A Translatewiki.net bot a $lang.json-t küldi el, amikor az exportáló bot fut
* Ezután kerülnek telepítésre a Miraheze klaszterbe (az almodulokat frissíteni kell)

[Category:Tech](https://meta.miraheze.org/wiki/Category:Tech)

----
**Source**: [https://meta.miraheze.org/wiki/Tech:Translating_Miraheze_extensions/hu](https://meta.miraheze.org/wiki/Tech:Translating_Miraheze_extensions/hu)