---
title: Tech:Semantic MediaWiki
---

Semantic MediaWiki is a unique extension that requires additional steps to enable on wikis and to upgrade the extension.

## Enabling on Wikis 

Semantic MediaWiki requires running `setupStore.php` on installation.

The data generated by this script needs to be on all MediaWiki appservers. Due to this, it does not work running `setupStore.php` in `ManageWikiInstaller` directly. It has to be manually ran and deployed using the following steps.

### mwdeploy 

Login to [mwtask181](/tech-docs/techmwtask181), then run these commands.

```
mwscript extensions/SemanticMediaWiki/setupStore.php <wiki> -y
mwscript extensions/SemanticMediaWiki/setupStore.php <wiki> -y
mwdeploy --files=../mediawiki/<version>/extensions/SemanticMediaWiki/.smw.json --servers=all
```

* Replace `<wiki>` with the database name of the wiki you're enabling SMW on.
* Replace `<version>` with the correct MediaWiki version the wiki is using (IE 1.41).

The `setupStore.php` script should be run twice as it can fail on the first run.

## Upgrading Extension 

 `{{ {{Note}} }}` *These steps are not yet confirmed but are theoretically how it should work. It should first be tested on [test151](/tech-docs/techtest151) before attempted in production.*

Unlike most extensions, Semantic MediaWiki is not installed via git, but rather via composer. Therefore the usual method of upgrading it using `mwdeploy --upgrade-extensions=SemanticMediaWiki` will not work for SMW.

To upgrade SMW follow the following steps:
* Bump the version in the composer.local.json in the mediawiki-repos git repository
* Run puppet on [puppet181](/tech-docs/techpuppet181)
* Run puppet on [mwtask181](/tech-docs/techmwtask181) and [test151](/tech-docs/techtest151)
* Run `mwdeploy --world --versions=all --servers=all` on [mwtask181](/tech-docs/techmwtask181) and [test151](/tech-docs/techtest151)

## Categories

* [Category:Tech](https://meta.miraheze.org/wiki/Category:Tech)
* [Category:Technology guidelines and guides](https://meta.miraheze.org/wiki/Category:Technology_guidelines_and_guides)

----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:Semantic_MediaWiki)**