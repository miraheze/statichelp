---
title: Tech:Mwdeploy/2026 draft
---

**mwdeploy** is our MediaWiki deployment tool available on all MediaWiki servers.

The current canary server is mwtask181; test151 is managed separately by the same tool.

The `--servers` argument must currently be included. You should just append every command with `--servers=all` to deploy to all servers. Doing that on test151 will only deploy it locally on test151. You can include a comma separated list if you wish to deploy to specific servers.

## Logging 

All errors and warnings will log failure messages to [SAL](/tech-docs/techserver_admin_log). A deployment will abort if the commands to copy data from staging to the canary server.

You can add `--no-log`, which will direct output to your terminal rather than `logsalmsg`. It's recommended to use this when deploying security patches/upgrades.

## Upgrading extensions and skins 

 `{{ {{main|Tech:Updating an extension}} }}`

For skins, use `--upgrade-skins` instead of `--upgrade-extensions`.

To upgrade an extension on all MediaWiki versions:
```bash
mwdeploy --upgrade-extensions=ExtensionName --servers=all --versions=all
```

To upgrade an extension on a specific MediaWiki version:
```bash
mwdeploy --upgrade-extensions=ExtensionName --servers=all --versions=1.45
```

Multiple extensions can also be upgraded at the same time by separating the names with commas:
```bash
mwdeploy --upgrade-extensions=Extension1,Extension2,Extension3 --servers=all --versions=all
```

To deploy local changes (or a local patch/PR) (equivalent to using `--folders=<version>/extensions/ExtensionName`):
```bash
mwdeploy --upgrade-extensions=ExtensionName --servers=all --force-upgrade
```

### Deploying a GitHub PR 

Use the following shell commands to check out and deploy a pull request made to an extension. Replace [PR NUMBER] with the number of the PR you want to check out and [BRANCH] with the branch the PR commits are on.
```bash
cd /srv/mediawiki-staging/1.45/extensions/ExtensionName
sudo -u www-data git fetch origin pull/[PR NUMBER]/head:[BRANCH]
sudo -u www-data git checkout [BRANCH]
cd ~
mwdeploy --upgrade-extensions=ExtensionName --servers=all --force-upgrade
```

### Deploying a Gerrit patch 

For extensions with patches in Gerrit, you can fetch and deploy a specific patch:
```bash
cd /srv/mediawiki-staging/1.45/extensions/ExtensionName
sudo -u www-data git fetch https://gerrit.wikimedia.org/r/p/mediawiki/extensions/ExtensionName refs/changes/[XX]/[PATCH_NUMBER]/[REVISION]
sudo -u www-data git checkout FETCH_HEAD
cd ~
mwdeploy --upgrade-extensions=ExtensionName --servers=all --force-upgrade
```

## Deploying config changes 

To pull and deploy the changes:
```bash
mwdeploy --config --pull=config --servers=all
```

To deploy local changes (equivalent to using `--folders=config`):
```bash
mwdeploy --config --servers=all
```

### Deploying an mw-config PR on beta 

Use the following shell commands to check out and deploy a pull request made to mw-config (e.g. for testing a change on beta).
Replace [PR NUMBER] with the number of the PR you want to check out and [BRANCH] with the branch the PR commits are on (not the target branch!).
```bash
cd /srv/mediawiki-staging/config
sudo -u www-data git fetch origin pull/[PR NUMBER]/head:[BRANCH]
sudo -u www-data git checkout [BRANCH]
cd ~
mwdeploy --config --servers=all
```

A `--pr` parameter that simplifies this process was suggested in [T13932](https://meta.miraheze.org/wiki/phorge:T13932).

## Deploying MediaWiki 

You can use any mix of the 3 `--world --config --l10n` parameters.

To deploy MediaWiki with no i18n/l10n changes:
```bash
mwdeploy --world --servers=all
```

To deploy MediaWiki with i18n/l10n changes (equivalent to running MergeMessageLists and RebuildLC):
```bash
mwdeploy --world --l10n --servers=all
```

To actually upgrade MediaWiki from the current upstream git branch:
```bash
mwdeploy --world --pull=world --l10n --servers=all
```

## Syncing files and folders 

To deploy a change to only specific files:
```bash
mwdeploy --files=w/index.php,w/api.php --servers=all
```

To sync a folder, or multiple folders:
```bash
mwdeploy --folders=1.45/extensions/Echo,1.45/skins/Vector --servers=all
```

## Resetting MediaWiki 

The `--reset-world` option resets the MediaWiki installation for the specified version. It removes the staging folder and reapplies Puppet configuration, effectively starting from a clean slate. This is useful when a deployment has gone wrong or when a full reset and removal of any local changes is required.

Example usage:
```bash
mwdeploy --versions=1.45 --servers=all --reset-world
```

## Upgrading the Entire MediaWiki Installation 

 `{{ {{main|Tech:Upgrading MediaWiki}} }}`

The `--upgrade-world` option upgrades MediaWiki, vendor, all extensions, and all skins for the specified versions. It automatically sets `--world`, `--l10n`, `--upgrade-extensions=all`, `--upgrade-skins=all`, `--upgrade-vendor`, and `--ignore-time`. This is the most comprehensive upgrade option.

Example usage:
```bash
mwdeploy --versions=1.45 --servers=all --upgrade-world
```

## Upgrading Vendor 

The `--upgrade-vendor` option updates the `vendor/` folder via Composer for the specified MediaWiki versions. It applies patches if needed and ensures all dependencies are up-to-date. This is typically used when libraries or PHP dependencies have changed or when a new local patch needs to be applied.

Example usage:
```bash
mwdeploy --versions=1.45 --servers=all --upgrade-vendor
```

## TODO 

* errorpages and landing
* ignore-time explanation
* --extension-list

## If a canary check fails 

If you see 'DEPLOY ABORTED' in SAL, this means that one of the servers in the list failed checks to ensure MediaWiki was not down.

The ABORTED message will show which server failed. If it shows 'localhost', that means the error occured on the server you're deploying from.

If the affected server is not fully down, you can SSH into it and run:
```bash
sudo journalctl -e
```
to see what exactly is causing the error.

In some cases, for example if you're depooling a crashed database cluster during an outage, you may need to bypass the check. Use `--force`.

## Failover a canary server 

<!-- Wasn't able to confirm whether this section is still up to date after updating the rest of the page, so I've moved the notice here -->

 `{{ {{Outdated||section}} }}`
While it won't cause issues to have a short loss of service on the active canary server, you just won't be able to deploy new stuff. Eventually, you might need to fail over to a replacement. Follow these steps if you do.
* Ensure the replacement is fully up to date.
* Enable use_staging and is_canary on the new server, disable remote_sync and switch default_sync to 'all' in puppet.
* Run puppet on the new server - this should add the staging clones, remove the ssh access from the current canary to the new and set the config to sync everywhere.
If the old server is being moved to a normal setup:
* Disable is_canary and use_staging in puppet.
* run puppet. This will enable remote access from the new canary. It will not wipe the old staging folder.
If the server is being decommissioned:
* Follow the normal server lifecycle procedure
* Wipe `/srv/mediawiki-staging/`

----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:Mwdeploy/2026_draft)**