---
title: Tech:Adding a new extension
---

Any user can create a pull request to install and enable an extension, but it has to be merged by a [sysadmin](https://meta.miraheze.org/wiki/Special:MyLanguage/System_administrators). If you want to add a new extension, request it [here](https://meta.miraheze.org/wiki/Special:MyLanguage/Request_features).

All of this stuff needs to be done before the steps above:

* Open a ticket for a Security Review
* Wait. We will review the extension following [the MediaWiki extension developers' security checklist](https://meta.miraheze.org/wiki/mw:Security_for_developers), among other things. If we notice a bug or a security vulnerability, we'll try to fix it or wait for the extension developers to fix it.
* On passing review, the extension needs to be added to the [mediawiki-repos](https://github.com/miraheze/mediawiki-repos) repository on GitHub. There are detailed instructions for how to do this in the README on the repository itself.
The above steps are for the `mediawiki-repos` repository. The following are for the `mw-config` repository.
* ManageWikiExtensions.php gets a setting added as well. (Make sure to check if it requires another extension or if it should be restricted)
* If the extension has database tables, make sure to add them to the ManageWikiExtensions.php config!
* It is not required, but preferable that you also load it on test151 in order to make sure that everything works as intended
* Setup any other extension globals here.
* Then run the following script on mwtask181 and/or test151: `mwdeploy --world --config --l10n --extension-list --servers=all`

It should be noted that it is a good idea to add any configuration variable the extension adds to [ManageWiki](https://meta.miraheze.org/wiki/ManageWiki) to save the effort of doing that at a later date and be user-friendly.

## See also 

* [Updating an extension](https://meta.miraheze.org/wiki/Tech:Updating_an_extension)
* [Removing an extension](/tech-docs/techremoving_an_extension.md)

[Category:Guides](https://meta.miraheze.org/wiki/Category:Guides)
[Category:Technology guidelines and guides](https://meta.miraheze.org/wiki/Category:Technology_guidelines_and_guides)

----
**Source**: [https://meta.miraheze.org/wiki/Tech:Adding_a_new_extension](https://meta.miraheze.org/wiki/Tech:Adding_a_new_extension)