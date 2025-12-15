---
title: Tech:Removing an extension
---

If a decision has been made to remove an extension from Miraheze—for example, because it is unmaintained, incompatible with the current MediaWiki version, or any other valid reason—the following procedure should be followed. Any user may submit a pull request to remove an extension, but only a [Technology team member](/tech-docs/techvolunteers) with appropriate access can merge and deploy the change.

*The steps below must be followed in order:*

* First, make sure the extension is temporarily restricted so that no new installs can occur during the removal process. To do this, follow the instructions at the [Globally Disabling Extensions](#globally-disabling-extensions) section.
* Run:
* 
```bash
mwscript ManageWiki:ToggleExtension loginwiki --name=<extension> --disable --all-wikis --execute
```
* Remove any associated settings using:
* 
```bash
mwscript ManageWiki:PopulateWikiSettings loginwiki --setting=<setting> --remove --all-wikis --execute
```
* Delete any related configuration from the following files:
  * `ManageWikiExtensions.php`
  * `LocalWiki.php`
  * `LocalSettings.php`
  * `GlobalSettings.php`
* *Note: If the extension also has entries in `ManageWikiSettings.php` or `ManageWikiNamespaces.php`, remove those as well.*
* Once configuration has been cleaned up, remove the extension from the `mediawiki-repos` GitHub repository.

*On `mwtask181` and `test151`, also perform the following:*

* Run:
* 
```bash
sudo -u www-data rm -rf /srv/mediawiki-staging/*/{repo_path}
```
* Deploy updates with:
* 
```bash
mwdeploy --world --config --pull=config --l10n --extension-list --servers=all --versions=all
```

## Globally Disabling Extensions 

If a full removal is not appropriate (e.g., in cases of temporary security concerns), an extension can be *globally disabled* without deleting user configuration by adding it to the 
```php
$wi::$disabledExtensions
```
 array at the end of `LocalSettings.php`.

This should follow the format:

      
```php
'key from ManageWikiExtensions' => 'reason',
```

* The *reason* may be plain text or a wikitext link to a Phorge task (e.g., `[[phorge:T12345]]`).
* This disables the extension in `Special:ManageWiki/extensions`, requires the `managewiki-restricted` permission to modify it, and prevents the extension from being loaded.

## See also 

* [Adding a new extension](/tech-docs/techadding_a_new_extension)

## Categories

* [Category:Technology guidelines and guides](https://meta.miraheze.org/wiki/Category:Technology_guidelines_and_guides)

----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:Removing_an_extension)**