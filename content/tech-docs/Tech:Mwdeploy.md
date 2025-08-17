---
title: Tech:Mwdeploy
---

**mwdeploy** is our MediaWiki deployment tool available on all MediaWiki servers.

The current canary server is mwtask181; test151 is managed separately by the same tool.

The `--servers` argument must currently be included. You should just append every command with `--servers=all` to deploy to all servers. Doing that on test151 will only deploy it locally on test151. You can include a comma separated list if you wish to deploy to specific servers.

## Logging 

All errors and warnings will log failure messages to [SAL](/tech-docs/techserver_admin_log). A deployment will abort if the commands to copy data from staging to the canary server.

You can add `--no-log`, which will direct output to your terminal rather than `logsalmsg`. It's recommended to use this when deploying security patches/upgrades.

## Upgrading extensions and skins 

For skins, use `--upgrade-skins` instead of `--upgrade-extensions`.

To upgrade an extension on all MediaWiki versions:
* `mwdeploy --upgrade-extensions=ExtensionName --servers=all --versions=all`

To upgrade an extension on a specific MediaWiki version:
* `mwdeploy --upgrade-extensions=ExtensionName --servers=all --versions=1.44`

Multiple extensions can also be upgraded at the same time by separating the names with commas:
* `mwdeploy --upgrade-extensions=Extension1,Extension2,Extension3 --servers=all --versions=all`

## Deploying config changes 

To pull and deploy the changes:
* `mwdeploy --config --pull=config --servers=all`

To deploy local changes (equivalent to using **--folders=config**):
* `mwdeploy --config --servers=all`

### Deploying an mw-config PR on beta 

Use the following shell commands to check out and deploy a pull request made to mw-config (e.g. for testing a change on beta).
Replace *[PR NUMBER]* with the number of the PR you want to check out and *[BRANCH]* with the branch the PR commits are on (not the target branch!).
```
cd /srv/mediawiki-staging/config
sudo -u www-data git fetch origin pull/[PR NUMBER]/head:[BRANCH]
sudo -u www-data git checkout [BRANCH]
cd ~
mwdeploy --config --servers=all
```

A `--pr` parameter that simplifies this process was suggested in [T13932](https://meta.miraheze.org/wiki/phorge:T13932).

## Deploying MediaWiki 

You can use any mix of the 3 `--world --config and --l10n` parameters.

To deploy MediaWiki with no i18n/l10n changes:
* `mwdeploy --world --servers=all`

To deploy MediaWiki with i18n/l10n changes (equivalent to running MergeMessageLists and RebuildLC):
* `mwdeploy --world --l10n --servers=all`

## Syncing files and folders 

If you wanted to deploy a change to only a single file (or multiple specific files) without syncing all files:
* `mwdeploy --files=w/index.php,w/api.php --servers=all`

To sync a folder, or multiple folders:
* `mwdeploy --folders=1.43/extensions/Echo,1.43/skins/Vector --servers=all`

## If a canary check fails 

If you see 'DEPLOY ABORTED' in SAL, this means that one of the servers in the list failed checks to ensure mediawiki was not down. This is a fairly basic check, so it probably means the server is completely fataling.

If you need to bypass the check, use `--force`. The check will still happen, but failures will be shown in your terminal output instead and will be ignored.

The ABORTED message will show which server failed, hopefully it will be 'localhost' which means the server you are deploying from.

If icinga alerts do not show the failed server as depooled, you should probably get someone to consider it or very quickly rollback. You may want to deploy to only the broken server first before deploying the rollback everywhere.

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
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:Mwdeploy)**