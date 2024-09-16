---
title: Tech:Translating Miraheze extensions/zh-tw
---


Miraheze develops and maintains a few extensions, for example [CreateWiki](https://meta.miraheze.org/wiki/github:miraheze/CreateWiki) and [ManageWiki](https://meta.miraheze.org/wiki/github:miraheze/ManageWiki). As Miraheze has users with no or limited knowledge of English, internationalization is important for such users.

現在我們使用 [translatewiki.net](https://meta.miraheze.org/wiki/translatewiki:)來處理 [新增維基](https://meta.miraheze.org/wiki/$cw)和 [維基管理](https://meta.miraheze.org/wiki/$mw)的翻譯。

## TranslateWiki process

* Add strings on en.json.
* Translatewiki.net bot will pull the code when they import the strings, and it will be shown to translators to translate.
* Translators in Translatewiki.net translate the texts.
* Translatewiki.net bot will push the $lang.json when the export bot is run.
* They are then deployed to the Miraheze cluster (the submodule must be updated).

## Categories

* [Category:Tech](https://meta.miraheze.org/wiki/Category:Tech)

----
**Source**: [https://meta.miraheze.org/wiki/Tech:Translating_Miraheze_extensions/zh-tw](https://meta.miraheze.org/wiki/Tech:Translating_Miraheze_extensions/zh-tw)