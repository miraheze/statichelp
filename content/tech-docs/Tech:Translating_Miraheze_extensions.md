---
title: Tech:Translating Miraheze extensions
---


<translate>

<!--T:1-->

Miraheze develops and maintains a few extensions, for example [[<tvar|cw>github:miraheze/CreateWiki</>|CreateWiki]] and [[<tvar|mw>github:miraheze/ManageWiki</>|ManageWiki]]. As Miraheze has users with no or limited knowledge of English, internationalization is important for such users.

<!--T:2-->

Currently, Miraheze uses [[<tvar|twn>translatewiki:</>|translatewiki.net]] for CreateWiki and ManageWiki translations.

## TranslateWiki process 

<!--T:3-->

</translate>
* 
<!--T:7-->

Add strings on en.json.
* 
<!--T:9-->

Translatewiki.net bot will pull the code when they import the strings, and it will be shown to translators to translate.
* 
<!--T:10-->

Translators in Translatewiki.net translate the texts.
* 
<!--T:11-->

Translatewiki.net bot will push the $lang.json when the export bot is run.
* 
<!--T:14-->

They are then deployed to the Miraheze cluster (the submodule must be updated).
[Category:Tech](https://meta.miraheze.org/wiki/Category:Tech)

----
**Source**: [https://meta.miraheze.org/wiki/Tech:Translating_Miraheze_extensions](https://meta.miraheze.org/wiki/Tech:Translating_Miraheze_extensions)