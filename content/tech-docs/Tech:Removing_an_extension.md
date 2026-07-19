---
title: Tech:Removing an extension
---

If a decision has been made to remove an extension from Miraheze—for example, because it is unmaintained, incompatible with the current MediaWiki version, or any other valid reason—the following procedure should be followed. Any user may submit a pull request to remove an extension, but only a [Technology team member](/tech-docs/techvolunteers) with appropriate access can merge and deploy the change.

## Gathering community feedback 

If an extension is about to be removed, though the tech team could consider keeping it with enough community support, consider asking for feedback on a subpage of [Tech:Noticeboard](/tech-docs/technoticeboard). Affected wikis should be made aware via the [NotifyWikiUsers](https://meta.miraheze.org/wiki/github:miraheze/MirahezeMagic/blob/main/maintenance/NotifyWikiUsers.php) script in MirahezeMagic. This will also give them some time to migrate to other solutions before the extension is removed.

The detailed steps of sending notifications is as follows:
* `sudo -u www-data mkdir /tmp/exts`
* For each extension, run `sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:GenerateExtensionDatabaseList --wiki=metawiki --extension=embedvideo --directory=/tmp/exts` with the necessary modifications.
* Save the following PHP script somewhere. 
```php
<?php
/**
 * Merge multiple PHP array files into a single file
 * Usage: php dblist_merge.php output.php input1.php input2.php [input3.php ...]
 */

if ($argc < 3) {
    echo "Usage: php {$argv[0]} output.php input1.php input2.php [input3.php ...]\n";
    exit(1);
}

$outputFile = $argv[1];
$inputFiles = array_slice($argv, 2);

$mergedData = [];

foreach ($inputFiles as $file) {
    if (!file_exists($file)) {
        echo "Warning: File '$file' does not exist, skipping...\n";
        continue;
    }

    $data = include $file;

    if (!is_array($data)) {
        echo "Warning: File '$file' does not return an array, skipping...\n";
        continue;
    }

    $mergedData = array_merge_recursive($mergedData, $data);
}

// Generate output file
$output = "<?php\n// Automatically generated\nreturn " . var_export($mergedData, true) . ";\n";

file_put_contents($outputFile, $output);

echo "Successfully merged " . count($inputFiles) . " files into '$outputFile'\n";
```
* Run the PHP script in the previous step: `php dblist_merge.php output.php /tmp/exts/*.php`
* Manually remove testwiki from output.php if it exists. PTW doesn't need to be notified.
* Run the following script:
```bash
foreachwikiindblist output.php /srv/mediawiki/1.45/maintenance/run.php MirahezeMagic:NotifyWikiUsers \
 --header='Extension removal notice' \
 --message='The technology team plans to remove one or more extensions currently used by your wiki. Please check the tech noticeboard on Meta to discuss.' \
 --link='m:Tech:Noticeboard/Removing_extensions_for_the_MediaWiki_1.46_upgrade' \
 --link-label='Discussion page' \
 --group=bureaucrat \
 --group=sysop
```

## Removing an extension 

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

If a full removal is not appropriate (e.g., in cases of temporary security concerns), an extension can be *globally disabled* without deleting user configuration by adding it to the `$wi::$disabledExtensions` array at the end of `LocalSettings.php`.

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