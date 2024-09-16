---
title: Tech:Translating Miraheze extensions
---


Miraheze develops and maintains a few extensions, for example [[github:miraheze/CreateWiki|CreateWiki]] and [[github:miraheze/ManageWiki|ManageWiki]]. As Miraheze has users with no or limited knowledge of English, internationalization is important for such users.

Currently, Miraheze uses [[translatewiki:|translatewiki.net]] for CreateWiki and ManageWiki translations.

## TranslateWiki process
* Add strings on en.json.
* Translatewiki.net bot will pull the code when they import the strings, and it will be shown to translators to translate.
* Translators in Translatewiki.net translate the texts.
* Translatewiki.net bot will push the $lang.json when the export bot is run.
* They are then deployed to the Miraheze cluster (the submodule must be updated).
[Category:Tech](https://meta.miraheze.org/wiki/Category:Tech)

----
**Source**: [https://meta.miraheze.org/wiki/Tech:Translating_Miraheze_extensions](https://meta.miraheze.org/wiki/Tech:Translating_Miraheze_extensions)