---
title: Tech:Removing an extension
---

If a decision has been made to remove an extension from Miraheze for whatever reason (i.e., it's unmaintained, it isn't compatible with the current version of MediaWiki, etc.) the following procedure should be followed when removing an extension. Any user can create a pull request to remove an extension, but it has to be merged and deployed by a [system administrator](https://meta.miraheze.org/wiki/Tech:SRE_Volunteers).

The steps below must be done in this order:

* Generate a list of all wikis using the extension with `/srv/mediawiki/<VERSION>/extensions/MirahezeMagic/maintenance/generateExtensionDatabaseList.php --wiki=loginwiki --extension=extension --directory=/srv/mediawiki`. This will create a JSON list in `/srv/mediawiki` called `<EXTENSION>.json`
* Run `sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/<EXTENSION>.json /srv/mediawiki/<VERSION>/extensions/ManageWiki/maintenance/toggleExtension.php --disable extension`
* Remove any settings configured using `sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/databases.json /srv/mediawiki/<VERSION>/extensions/ManageWiki/maintenance/populateWikiSettings.php --wgsetting=wgSettingName --sourcelist=false --remove`
* Remove any existing configuration from ManageWikiExtensions.php, LocalSettings.php, and GlobalSettings.php. (Note: If the extension has extra settings in ManageWikiSettings.php, make sure to remove that too)
* Remove the extension from the mediawiki-repos on GitHub after the settings above have been successfully removed.

On mwtask181 and test151:
* run `sudo -u www-data rm -rf /srv/mediawiki-staging/w/{submodule_path}`
* run `mwdeploy --world --config --l10n --extension-list --servers=all`

## Globally disabling extensions 

If it is not appropriate to fully remove an extension, but the extension should not be active on any wikis (e.g., in the event of a security vulnerability with a particular extension), it can be globally disabled without disrupting any related configuration that users have set in ManageWiki by adding the extension to the `$disabledExtensions` array found at the bottom of LocalSettings.php.

## See also 

* [Adding a new extension](Tech:Adding_a_new_extension.md)
* [Updating an extension](https://meta.miraheze.org/wiki/Tech:Updating_an_extension)

[Category:Technology guidelines and guides](https://meta.miraheze.org/wiki/Category:Technology_guidelines_and_guides)

----
**Source**: [https://meta.miraheze.org/wiki/Tech:Removing_an_extension](https://meta.miraheze.org/wiki/Tech:Removing_an_extension)