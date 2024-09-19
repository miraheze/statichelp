---
title: Tech:Translating Miraheze extensions/it
---


Miraheze develops and maintains a few extensions, for example [CreateWiki](https://meta.miraheze.org/wiki/github:miraheze/CreateWiki) and [ManageWiki](https://meta.miraheze.org/wiki/github:miraheze/ManageWiki). As Miraheze has users with no or limited knowledge of English, internationalization is important for such users.

Currently, Miraheze uses [translatewiki.net](https://meta.miraheze.org/wiki/translatewiki:) for CreateWiki and ManageWiki translations.

## TranslateWiki process

* Add strings on en.json.
* Translatewiki.net bot will pull the code when they import the strings, and it will be shown to translators to translate.
* Translators in Translatewiki.net translate the texts.
* Translatewiki.net bot will push the $lang.json when the export bot is run.
* They are then deployed to the Miraheze cluster (the submodule must be updated).

## Categories

* [Category:Tech](https://meta.miraheze.org/wiki/Category:Tech)



----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:Translating_Miraheze_extensions/it)**