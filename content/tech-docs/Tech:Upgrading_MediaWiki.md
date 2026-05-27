---
title: Tech:Upgrading MediaWiki
---

## Preparations 

<!-- I've not pasted the link to the mm thread but you can see it on the Planning channel -->

### Create Phorge Tasks 

Two tasks should be created on [Phorge](https://meta.miraheze.org/wiki/Phorge), one to upgrade MediaWiki (example: [T14458](https://meta.miraheze.org/wiki/phorge:T14458)) and another to test extensions (example: [T14459](https://meta.miraheze.org/wiki/phorge:T14459)). Additionally, a paste should be created for exception backtraces found during testing (example: [P562](https://meta.miraheze.org/wiki/phorge:P562)), and sub tasks of the main upgrade task should be created for extensions that should be totally undeployed before the upgrade (example: [T14866](https://meta.miraheze.org/wiki/phorge:T14866)).

### Deploy the New Version 

* Clone the new version by adding to `mediawiki::multiversion::versions` in [mediawiki_beta.yaml](https://meta.miraheze.org/wiki/github:miraheze/puppet/blob/main/hieradata/role/common/mediawiki_beta.yaml), and later, a few days to a week before the planned launch of the [NextTide](https://meta.miraheze.org/wiki/NextTide) program, to [common.yaml](https://meta.miraheze.org/wiki/github:miraheze/puppet/blob/main/hieradata/common.yaml) for it to be deployed on production.
* Once Puppet pulls the changes to [puppet181](/tech-docs/techpuppet181), run `sudo puppet agent -tv` on [test151](/tech-docs/techtest151) for beta or [mwtask181](/tech-docs/techmwtask181) for production.
* Deploy the new version with: `mwdeploy --world --l10n --ignore-time --extension-list --servers=all --versions=<new_version>`.

### Prepare for the Upgrade 

 `{{ {{Note}} }}` Before upgrading production this should be double checked again as well, as some things may have changed since first checking.

* Check if there are any migrations that can be done **before** the upgrade (they must have support for `WRITE_BOTH` migration variables at the minimum).
* `{{ {{Note}} }}` No SQL patches can be done before at least new wikis are upgraded (see [#Upgrading New Wikis](#upgrading-new-wikis) for that), otherwise new wikis will be missing the patches that were already ran on existing wikis. `{{ {{Note|For production use loginwiki instead of loginwikibeta.}} }}`
* Find new SQL patches that are needed:
* `mwscript MirahezeMagic:FindSQLPatches loginwikibeta --no-log --from-version=<old_version> --to-version=<new_version>`
* Find new maintenance scripts that may be needed (typically (but not always) only those with **LoggedUpdateMaintenance** are actually needed):
* `mwscript MirahezeMagic:FindPossibleUpgradeScripts loginwikibeta --no-log --from-version=<old_version> --to-version=<new_version>`

#### Necessary Config Changes 

* Look for any new or renamed SQL files for new tables for global extensions and add to `wgCreateWikiSQLFiles` in [LocalSettings.php](https://meta.miraheze.org/wiki/github:miraheze/mw-config/blob/main/LocalSettings.php). You can add a new array, keyed by the new version to set for only the new version ([example](https://meta.miraheze.org/wiki/github:miraheze/mw-config/commit/366474e) – if one is being renamed rather than adding a new one, remove the **+** and copy the entire current default but with the changes).
* If a global extension can be removed (e.g. when Interwiki was merged into core in MediaWiki 1.44), update [GlobalExtensions.php](https://meta.miraheze.org/wiki/github:miraheze/mw-config/blob/main/GlobalExtensions.php), and wrap the extension in a `$wi->version` if block ([example](https://meta.miraheze.org/wiki/github:miraheze/mw-config/commit/025e63a)). Also add **versions** in [mediawiki-repos.yaml](https://meta.miraheze.org/wiki/github:miraheze/mediawiki-repos/blob/main/mediawiki-repos.yaml) ([example](https://meta.miraheze.org/wiki/github:miraheze/mediawiki-repos/commit/4244212)).
* If any settings need changed only for the new version, if in LocalSettings.php, you can use the new version just like any wiki (e.g. **1.45**) in `$wgConf`. If outside `$wgConf`, you can use `$wi->version` in if blocks.
* Audit any new permissions and determine if they need to be added to `$wgManageWikiPermissionsDisallowedRights`.
* Some extensions may have moved from old configuration variables to virtual domains. This should be checked and added to `$wgVirtualDomainsMapping` where appropriate.

<!-- NOTE: this can be removed in a few releases when all extensions have migrated to virtual domains but as of now this is still ongoing so is mentioned here. -->

## Create JSON Schema for UpgradeWiki 

This JSON file defines the upgrade steps for a wiki, including SQL patches and maintenance scripts. All paths are relative to the server root unless absolute paths are given.
 `{{ {{Note|Pay attention to what scripts and patches do. If you have a patch that drops something in pre_patches, and a maintenance script that does the migration, that will lead to data loss. In that case the patch should be in post_patches.}} }}`

### Format 

#### mwversion 

* Required string of the **new** MediaWiki version.
* Only used as the upgrade key so that the same upgrade isn't attempted twice on the same wiki.
* Example: `{ "mwversion": "1.45" }`

#### pre_patches 

* Array of SQL files to run **before** maintenance scripts.
* Each entry can be:
   * A string containing the path to the SQL file.
   * An object: `{ "file": "/path/to/file.sql" }`
   * Optional: `if_extension_enabled` (string) — name of an extension; this patch only runs if the extension is enabled.
* Example:
```json
"pre_patches": [
	"/patches/001_initial.sql",
	{ "file": "/patches/002_add_columns.sql" },
	{ "file": "/patches/conditional.sql", "if_extension_enabled": "CentralAuth" }
]
```

#### maintenance 

* Array of maintenance scripts to run **after pre_patches**.
* Each entry is an object with the following properties:
   * `class` (string, required) — fully qualified class name of the maintenance script.
   * `options` (object, optional) — key/value pairs passed to the script as options.
   * `args` (array, optional) — positional arguments passed to the script.
   * `if_extension_enabled` (string, optional) — only run this maintenance script if the given extension is enabled.
* Example:
```json
"maintenance": [
	{
		"class": "MediaWiki\\Extension\\CentralAuth\\Maintenance\\FixRenameUserLocalLogs",
		"options": { "logwiki": "metawiki", "fix": true },
		"if_extension_enabled": "CentralAuth"
	}
]
```

#### post_patches 

* Array of SQL files to run **after maintenance scripts**.
* Format is identical to `pre_patches`, including support for `if_extension_enabled`.
* Example:
```json
"post_patches": [
	"/patches/999_finalize.sql",
	{ "file": "/patches/conditional_post.sql", "if_extension_enabled": "FlaggedRevs" }
]
```

#### Full Example 

<!-- [[phorge:T15364|]] contains a full list -->

```
{{ {{collapse|
<syntaxhighlight lang="json">
{
	"mwversion": "1.45",
	"pre_patches": [
		"/srv/mediawiki/1.45/sql/mysql/patch-existencelinks.sql",
		"/srv/mediawiki/1.45/sql/mysql/patch-imagelinks-add-il_target_id.sql",
		{
			"file": "/srv/mediawiki/1.45/extensions/PageTriage/sql/mysql/patch_ptrp_tags_updated_nullable.sql",
			"if_extension_enabled": "PageTriage"
		}
	],
	"maintenance": [
		{
			"class": "FixWrongPasswordPrefixes"
		},
		{
			"class": "MediaWiki\\Extension\\CentralAuth\\Maintenance\\FixRenameUserLocalLogs",
			"options": { "logwiki": "metawiki", "fix": true },
			"if_extension_enabled": "CentralAuth"
		},
		{
			"class": "UpdateCollation",
			"options": { "only-migrate-normalization": true }
		},
		{
			"class": "MediaWiki\\Extension\\ExampleExtension\\Maintenance\\ExampleScript",
			"args": [
				"firstPositionalArg",
				"secondPositionalArg"
			]
		},
	],
	"post_patches": [
		"/srv/mediawiki/1.45/extensions/AbuseFilter/db_patches/mysql/patch-drop-afl_ip.sql",
		"/srv/mediawiki/1.45/sql/mysql/patch-categorylinks-drop-cl_to-cl_collation.sql",
		{
			"file": "/srv/mediawiki/1.45/extensions/FlaggedRevs/sql/add_review_timestamp.sql",
			"if_extension_enabled": "FlaggedRevs"
		}
	]
}
</syntaxhighlight>
|Click to expand a complete example JSON schema.}} }}
```

#### Notes 

* Those that are only needed on the global database (testglobal/mhglobal), or a specific wiki should be omitted from the JSON and ran manually in that case.
* Due to performance issues, **ChangeMediaWikiVersion** should **never** be added here. See [#ChangeMediaWikiVersion](#changemediawikiversion) instead.
* The runner automatically injects wiki context:
   * `wikidb` is set for SQL files.
   * `wiki` is set for maintenance scripts unless overridden.
* Validation rules:
   * `mwversion` must be a string of the new version.
   * `pre_patches` and `post_patches` must be arrays.
   * `maintenance` must be an array of objects with a non-empty `class`.
   * `options` must be key/value object; `args` must be an array of strings or integers.
   * `if_extension_enabled`, if present, must be a string corresponding to a valid enabled extension.
   * `{{ {{Note}} }}` Should be provided even if it's a global extension since some wikis, such as `ldapwikiwiki`, may not have certain extensions such as CentralAuth enabled.

### Creating the schema 

See [T15364](https://meta.miraheze.org/wiki/phorge:T15364) for an example schema as well as global scripts/patches. See Mattermost for the threads relating to the 1.46 update.

#### SQL patches 

All patches should be carefully read through and compared to the tables that currently exist on both local wikis and the global database (mhglobal/testglobal). Some general points collected through previous upgrades are:

* If a patch is modifying a global table, it should be ran manually. The rest of these points still apply to global scripts, just without being in the schema.
* If a global extension is adding a new table, you'll need to read the docs and/or code of the extension to determine if it's meant to be a local or global table.
* If a patch is adding a new field to the table then it should be in pre_patches.
   * The order of these patches matters. If patch A adds a field and patch B does something that uses the field from patch A, then patch B must be ran after patch A. Always check the fields from the current table.
   * If patch B creates an index that uses a field from patch A, then patch B must go after patch A.
* If a patch is altering a field in a way that could possibly be incompatible with the current field (e.g. changing type, or making the field not null), then it is likely there is a maintenance script that makes the current field compatible. In this case, the field altering patch should be in post_patches.
* If a patch is dropping a field then it should go in post_patches. Generally fields will be dropped when they're superseded, in which case a field will be added in pre_patches, then a maintenance script will populate that field, then the superseded field will be dropped. Sometimes a field might just be removed with no substitute but there's no harm in putting these drops in post_patches.

#### Maintenance scripts 

FindSQLPatches is unlikely to have any false positives or false negatives. This is not the case with FindPossibleUpgradeScripts.

Read through all the maintenance scripts that FindPossibleUpgradeScripts returned. *Typically* the ones you're looking for will extend LoggedUpdateMaintenance and the rest will just be regular maintenance scripts, but use your own judgement.

UpgradeWiki will rely on PHP class names being accurate, so make sure that you double check all the classes in the schema exist. For example, with 1.46's `"class": "\\MigrateTranscodeStates",` in the schema, go to a wiki (in this case one that's enabled TimedMediaHandler) and run `class_exists( \MigrateTranscodeStates::class )`.

As with SQL patches, maintenance scripts affecting global tables should be run manually rather than being in the UpgradeWiki schema.

#### Finding false negatives 

As stated earlier, while SQL patches are unlikely to come up with false negatives by design, there will likely be some necessary maintenance scripts that are not caught by FindPossibleUpgradeScripts. Typically these will be affecting tables that had SQL patches anyway.

For example, in 1.46, every single one of the pre_patches also had a corresponding maintenance script, except for the patch to the imagelinks table. The imagelinks patch created a new field with `DEFAULT NULL`, and one of the later patches would alter this field to become `NOT NULL`. Therefore, it would be impossible for there to not be a maintenance script. That maintenance script turned out to be `MigrateLinksTable`.

<!-- this probably needs some expansion -->

### Sanity check 

 `{{ {{Note}} }}` **update.php loses data! This check is only to find things you missed; finding nothing in this check does not mean that you found everything.**

A method of checking your work is to check what update.php does.

For core patches, check `getCoreUpdateList` from [MysqlUpdater.php](https://gerrit.wikimedia.org/r/plugins/gitiles/mediawiki/core/+/refs/heads/master/includes/Installer/MysqlUpdater.php). This will give you a sense of both the orders of patches and the maintenance scripts that need to be run. Using the earlier imagelinks example, the field is added, the inherited [migrateImagelinks](https://gerrit.wikimedia.org/r/plugins/gitiles/mediawiki/core/+/6b7c81780425f91d7d79b8c7bdb1d8d9d3c74343/includes/Installer/DatabaseUpdater.php#1553) function is executed, the column altering patch is run, then finally the old field is dropped.

For extension patches, check what implements `LoadExtensionSchemaUpdatesHook`. Typically these will have comments explaining what version each part of `onLoadExtensionSchemaUpdates` exists for.

## ChangeMediaWikiVersion 

 `{{ {{Note}} }}` Due to performance issues this script should **never** be ran in **foreachwikiindblist** with a lot of wikis. For that reason, this script provides numerous options to run on a batched set of wikis.

* `--mwversion=<new_version>` is the version to change selected wikis to.
* `--dry-run` can be used to preview what it would do without actually committing any changes.
* `--all-wikis` can be used to change the version for all wikis, including deleted wikis.
* `{{ {{Note}} }}` This typically should not be used on production, as we don't upgrade all wikis at once.

**State options**:
* `--active` – change the version for only active wikis, which are those not marked as closed, deleted, or inactive.
* `--closed` – change the version for only closed wikis.
* `--deleted` – change the version for only deleted wikis.
* `--inactive` – change the version for only inactive wikis.

**Special options**:
 `{{ {{Note}} }}` These should rarely be necessary to use.

* <code>--file=</path/to/file></code> – can provide a file with dbnames, one per line, to upgrade.
* `--regex=<selection regex>` – can provide regex based on dbname to upgrade those wikis. May be helpful if batching in alphabetical order.

## Upgrading Beta 

* Change **beta** in `MEDIAWIKI_VERSIONS` in [MirahezeFunctions](https://meta.miraheze.org/wiki/github:miraheze/mw-config/blob/main/initialise/MirahezeFunctions.php) to the new version.
* Switch the default version in `mediawiki::multiversion::versions` in [mediawiki_beta.yaml](https://meta.miraheze.org/wiki/github:miraheze/puppet/blob/main/hieradata/role/common/mediawiki_beta.yaml) to the new version. This key only makes systemd timers run using the new version.
* Ensure that the JSON schema for UpgradeWiki is available at some `/path/to/json/file.json`.

**On [test151](/tech-docs/techtest151)**:
* Run `mwdeploy --config --pull=config --servers=all` to deploy the changes.
* Run `mwscript MirahezeMagic:ChangeMediaWikiVersion loginwikibeta --mwversion=<new_version> --all-wikis --no-log`.
* Run `mwscript MirahezeMagic:UpgradeWiki all --json=/path/to/json/file.json --version=<new_version>`.
* Run `mwscript MirahezeMagic:UpgradeWiki deleted --json=/path/to/json/file.json --version=<new_version>` (to also upgrade any deleted wikis).

## Upgrading Individual Wikis (NextTide) 

 `{{ {{Note}} }}` NextTide may not always be possible if there are some backwards incompatible schema changes between global and local tables.

First, create a paste on Phorge to track wikis that have opt-in to NextTide (example: [P556](https://meta.miraheze.org/wiki/phorge:P556)). Wikis that have opted into previous NextTide programs are **not** automatically opt-in everytime, with the exception of **testwiki** which is always opt-in.

**To upgrade an individual wiki**:
* Run `mwscript MirahezeMagic:ChangeMediaWikiVersion <wiki> --mwversion=<new_version> --no-log`.
* Run `mwscript MirahezeMagic:UpgradeWiki <wiki> --json=/path/to/json/file.json --version=<new_version>`.
* Add the wiki to the NextTide paste.

## Upgrading New Wikis 

 `{{ {{Note}} }}` Once **metawiki** is upgraded, you can switch `wgCreateWikiSQLFiles` in [LocalSettings.php](https://meta.miraheze.org/wiki/github:miraheze/mw-config/blob/main/LocalSettings.php) back to using `$IP` again.

* Disable new wiki requests, wiki creations, and the AI auto approvals temporarily (this should be communicated to Wiki Reviewers first) ([example commit](https://meta.miraheze.org/wiki/github:miraheze/mw-config/commit/009ea7d)).
* Run `mwscript MirahezeMagic:PopulateMediaWikiVersion loginwiki --old-version=<old_version> --new-version=<new_version>` and **wait for it to finish**. This script populates the old version in the **mediawiki-version** field for all existing wikis so that they are explicitly on the old version so that new wikis can use the new version (which will now be the default version).
* `{{ {{Note|PopulateMediaWikiVersion also supports a <code>--dry-run</code> option you could run first.}} }}`
* Update `wgCreateWikiSQLFiles` in [LocalSettings.php](https://meta.miraheze.org/wiki/github:miraheze/mw-config/blob/main/LocalSettings.php) to use the full absolute path rather than `$IP` and merge the version key with default. Also, add a new **legacy** option and change **stable** to the new version in `MEDIAWIKI_VERSIONS` in [MirahezeFunctions](https://meta.miraheze.org/wiki/github:miraheze/mw-config/blob/main/initialise/MirahezeFunctions.php). – [Example commit](https://meta.miraheze.org/wiki/github:miraheze/mw-config/commit/46c7fa2)
* Run `mwdeploy --config --pull=config --servers=all` on [mwtask181](/tech-docs/techmwtask181) to deploy the changes.
* Once existing wikis look fine and are still on the old version properly, reenable wiki requests and wiki creations by reverting the commit in the first step of this section.
* Run `mwdeploy --config --pull=config --servers=all` on [mwtask181](/tech-docs/techmwtask181) to deploy the changes once again.
* Communicate to Wiki Reviewers that they may resume and to let the Technology team know of any issues.

## Upgrading in Batches 

 `{{ {{Note}} }}` We upgrade wikis in batches over the course of a few days to a week.

* The first batch is always considered to be [NextTide](https://meta.miraheze.org/wiki/NextTide).
* If the NextTide program is skipped due to some sort of incompatibility, then this still includes any opt-in wiki and **testwiki**.
* The second batch would be new wikis (see [#Upgrading New Wikis](#upgrading-new-wikis)).
* The third batch would be all wikis in [Miraheze projects](https://meta.miraheze.org/wiki/Miraheze_projects) (for upgrading see and follow the same steps in [Upgrading Individual Wikis](#upgrading-individual-wikis-nexttide)).
* `{{ {{Note}} }}` Some wikis like metawiki may have wiki specific patches such as for global AbuseFilter filter and should be applied at this time. Additionally, once **metawiki** is completed, you can switch `wgCreateWikiSQLFiles` in [LocalSettings.php](https://meta.miraheze.org/wiki/github:miraheze/mw-config/blob/main/LocalSettings.php) back to using `$IP` again.
* The fourth, fifth, and sixth batches would be deleted, closed, and inactive wikis respectively.
* `{{ {{Note}} }}` These should be at least 24 hours after the third batch has been completed, and could all be done around the same time by running them on separate **mwtask** servers simultaneously.
* The seventh batch would be active wikis.
* `{{ {{Note}} }}` These should be done at least 24 hours after the sixth batch has been completed.
* See [#Finalizing Upgrade](#finalizing-upgrade) for the eighth and final batch.

For each batched state you can follow the instructions in [#ChangeMediaWikiVersion](#changemediawikiversion) to change the version for each state and wait for those scripts to finish.

Once that is done, you can use `mwscript MirahezeMagic:UpgradeWiki <active/closed/deleted/inactive> --json=/path/to/json/file.json --version=<new_version>` to begin the upgrades on wikis per state.

Once all wikis are on the new version (or at least **loginwiki**), switch the default version in `mediawiki::multiversion::versions` in [common.yaml](https://meta.miraheze.org/wiki/github:miraheze/puppet/blob/main/hieradata/common.yaml) to the new version. This key only makes systemd timers run using the new version.

## Finalizing Upgrade 

Some wikis may have been missed during the upgrade. You can check `/srv/mediawiki/cache/legacy-wikis.php` to see if any wikis remain.

**If wikis still remain**:
* `sudo -u www-data cp /srv/mediawiki/cache/legacy-wikis.php /srv/mediawiki/cache/upgrade-wikis.php` (to ensure you are not using a list file that may change while the upgrade is still ongoing)
* `sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/upgrade-wikis.php /srv/mediawiki/<old_version>/maintenance/run.php MirahezeMagic:ChangeMediaWikiVersion --mwversion=<new_version>`
* `{{ {{Note}} }}` Due to performance issues mentioned above this may cause temporary farm instability and should be monitored very closely.
* `sudo -u www-data /usr/local/bin/foreachwikiindblist /srv/mediawiki/cache/upgrade-wikis.php /srv/mediawiki/<new_version>/maintenance/run.php MirahezeMagic:UpgradeWiki --json=/path/to/json/file.json`

Once those are done, once again, confirm if any wikis remain in `/srv/mediawiki/cache/legacy-wikis.php`. If not, delete the **upgrade-wikis.php** file now as well.

## Monitoring for Errors 

 `{{ {{Note}} }}` UpgradeWiki logs errors in two places for redundancy.

**You can either**:
* Search for `mediawiki_channel:UpgradeWiki` on [Graylog](/tech-docs/techgraylog).
* Check `/var/log/mediawiki/debuglogs/UpgradeWiki-exceptions.log` on **the server that UpgradeWiki is running on**.

If wikis are found in either of those places it is very likely that the upgrade failed, and some, or all, schema and/or maintenance scripts were not ran on the wikis there and should be investigated as soon as possible.

Also during the upgrade process when some wikis begin to be upgraded, you can monitor for certain errors for wikis on the new version by searching for `mediawiki_version:<new_version>` on [Graylog](/tech-docs/techgraylog).

## Cleaning Up Old Version 

* Remove **legacy** from `MEDIAWIKI_VERSIONS` in [MirahezeFunctions](https://meta.miraheze.org/wiki/github:miraheze/mw-config/blob/main/initialise/MirahezeFunctions.php).
* Remove the old version from `mediawiki::multiversion::versions` in [mediawiki_beta.yaml](https://meta.miraheze.org/wiki/github:miraheze/puppet/blob/main/hieradata/role/common/mediawiki_beta.yaml) and [common.yaml](https://meta.miraheze.org/wiki/github:miraheze/puppet/blob/main/hieradata/common.yaml) and wait for Puppet to pull it to [puppet181](/tech-docs/techpuppet181).
* Run `cleanup-old-mediawiki <old_version>` on all mw, mwtask, and test servers. This can also be done with [salt-ssh](/tech-docs/techsalt) from [puppet181](/tech-docs/techpuppet181).

## Post-Upgrade 

* Create a parent task on Phorge that all upgrade-related, user-reported issues will be added as subtasks (example: [T14979](https://meta.miraheze.org/wiki/phorge:T14979)).
* Check for configuration variables and permissions that no longer exist and remove them in [mw-config](https://meta.miraheze.org/wiki/github:miraheze/mw-config).
* Cleanup upgrade-related code in [mw-config](https://meta.miraheze.org/wiki/github:miraheze/mw-config).
* Remove any entries in [mediawiki-repos.yaml](https://meta.miraheze.org/wiki/github:miraheze/mediawiki-repos/blob/main/mediawiki-repos.yaml) that are now excluded by the **versions** key.

## Categories

* [Category:Tech](https://meta.miraheze.org/wiki/Category:Tech)
* [Category:Technology guidelines and guides](https://meta.miraheze.org/wiki/Category:Technology_guidelines_and_guides)

----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:Upgrading_MediaWiki)**