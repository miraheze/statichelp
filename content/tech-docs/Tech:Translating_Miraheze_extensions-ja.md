---
title: Tech:Translating Miraheze extensions/ja
---


Mirahezeは、 [CreateWiki](https://meta.miraheze.org/wiki/github:miraheze/CreateWiki)や [ManageWiki](https://meta.miraheze.org/wiki/github:miraheze/ManageWiki)のように、いくつかの拡張機能を開発・維持しています。Miraheze には英語の知識がない、もしくはわずかな知識しか持たないユーザーがいるため、国際化は利用者にとって大切です。

現在、私達は [translatewiki.net](https://meta.miraheze.org/wiki/translatewiki:)を、CreateWikiやManageWikiの翻訳に使っております。

## TranslateWikiでのプロセス 

* en.jsonに文字列を追加する。
* Translatewiki.netのボットは文字列をインポートした時にコードをpullし、その内容は翻訳のために翻訳者に示されます。
* Translatewiki.netの翻訳者は文章を翻訳する。
* Translatewiki.netのボットは、エクスポートボットが実行された時に、 $lang.json に内容をプッシュする。
* そうなると、Mirahezeクラスターに実装される（サブモジュールもアップデートされなければならない）。

## Categories

* [Category:Tech](https://meta.miraheze.org/wiki/Category:Tech)

----
**Source**: [https://meta.miraheze.org/wiki/Tech:Translating_Miraheze_extensions/ja](https://meta.miraheze.org/wiki/Tech:Translating_Miraheze_extensions/ja)