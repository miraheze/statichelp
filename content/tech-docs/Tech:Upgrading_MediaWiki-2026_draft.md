---
title: Tech:Upgrading MediaWiki/2026 draft
---

## Preperations 

 `{{ {{note|For production use loginwiki instead of loginwikibeta.}} }}`
* Check if there are any migrations that can be done **before** the upgrade (they must have support for `WRITE_BOTH` migration variables at the minimum).
* `{{ {{note|No SQL patches can be done before at least new wikis are upgraded (see [[#Upgrading new wikis]] for that), otherwise new wikis will be missing the patches that were already ran on existing wikis.}} }}`
* Find new SQL patches that are needed:
* `mwscript MirahezeMagic:FindSQLPatches loginwikibeta --no-log --from-version=<old_version> --to-version=<new_version>`
* Find new maintenance scripts that may be needed (typically only those with LoggedUpdateMaintenance are actually needed):
* `mwscript MirahezeMagic:FindPossibleUpgradeScripts loginwikibeta --no-log --from-version=<old_version> --to-version=<new_version>`

### JSON Schema for UpgradeWiki 

This JSON file defines the upgrade steps for a wiki, including SQL patches and maintenance scripts. All paths are relative to the server root unless absolute paths are given.
 `{{ {{note|Pay attention to what scripts and patches do. If you have a patch that drops something in pre_patches, and a maintenance script that does the migration, that will lead to data loss. In that case the patch should be in post_patches.}} }}`

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
        "class": "Miraheze\\MirahezeMagic\\Maintenance\\ChangeMediaWikiVersion",
        "options": { "mwversion": "1.45" }
    },
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

#### Notes 

* Those that are only needed on the global database (testglobal/mhglobal), or a specific wiki should be omitted from the JSON and ran manually in that case.
* Due to performance issues, **ChangeMediaWikiVersion** should **never** be added here. See [#ChangeMediaWikiVersion](#changemediawikiversion) instead.
* The runner automatically injects wiki context:
   * `wikidb` is set for SQL files.
   * `wiki` is set for maintenance scripts unless overridden.
* Validation rules:
   * `pre_patches` and `post_patches` must be arrays.
   * `maintenance` must be an array of objects with a non-empty `class`.
   * `options` must be key/value object; `args` must be an array of strings or integers.
   * `if_extension_enabled`, if present, must be a string corresponding to a valid enabled extension.

## ChangeMediaWikiVersion 

## Upgrading beta 

## Upgrading new wikis 


----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:Upgrading_MediaWiki/2026_draft)**