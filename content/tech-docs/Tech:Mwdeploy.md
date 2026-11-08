---
title: Tech:Mwdeploy
---

**mwdeploy** is our MediaWiki deployment tool available on all MediaWiki servers.

The current canary server is mwtask181; test151 is managed separately by the same tool.

The `--servers` argument must currently be included. You should just append every command with `--servers=all` to deploy to all servers. Doing that on test151 will only deploy it locally on test151. You can include a comma separated list if you wish to deploy to specific servers.

## How it works 

On test151, mwdeploy copies files in `/srv/mediawiki-staging` into `/srv/mediawiki`. This way, you can make the changes to extensions/skins/config as you need in the staging directory without affecting the server. Once you are ready, run mwdeploy to copy your changes to the corresponding directory in `/srv/mediawiki`, where the new files are served to incoming web traffic. Note that staging gets reset by puppet once every 30 minutes, so the following sequence of events is possible: you change the content in staging -> deploy -> staging gets reset by puppet -> staging has old content while the server is running your updated version. Someone else might come in and deploy their own changes upon the old content, which means your changes will be reset.

On mwtask181, mwdeploy copies the specified files in `/srv/mediawiki-staging` into all mw* and mwtask* servers. This is convenient because otherwise you will need to update the skin/extension/config on every single server, whereas with mwdeploy you only need a single command.

## Logging 

All errors and warnings will log failure messages to [SAL](/tech-docs/techserver_admin_log). A deployment will abort if the commands to copy data from staging to the canary server.

The `--task` argument will also log the `mwdeploy` run in the referenced Phorge task. For example, `--task=T15578` created [phorge:T15578#327783](https://meta.miraheze.org/wiki/phorge:T15578#327783).

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

To pull the latest changes from GitHub and deploy the changes:
* `mwdeploy --config --pull=config --servers=all`

To deploy local changes (equivalent to using **--folders=config**):
* `mwdeploy --config --servers=all`

## Deploying extension or config PRs on beta 

### For mw-config 

Use the following shell commands to check out and deploy a pull request made to mw-config (e.g. for testing a change on beta).
Replace *[PR NUMBER]* with the number of the PR you want to check out and *[BRANCH]* with the branch the PR commits are on (not the target branch!).
```
cd /srv/mediawiki-staging/config
sugit fetch origin pull/[PR NUMBER]/head:[BRANCH]
sugit checkout [BRANCH]
cd ~
mwdeploy --config --servers=all
```

A `--pr` parameter that simplifies this process was suggested in [T13932](https://meta.miraheze.org/wiki/phorge:T13932).

If you frequently deploy PRs from your own fork, you can add your fork as a remote. For example, to add a remote named petra pointing toward [User:PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna)'s fork of mw-config, use the following:
```
sugit remote add petra https://github.com/lihaohong6/mw-config
sugit fetch petra [remote-branch-name]:[local-branch-name]
```

### For extensions and skins 

The procedure is similar with mw-config, except that:
* You need to go to `/srv/mediawiki-staging/[VERSION]/extensions/[EXTENSION NAME]`
* Run the same `sugit fetch origin pull/[PR NUMBER]/head:[BRANCH]` and `sugit checkout [BRANCH]` lines
* Run `mwdeploy --folders=[VERSION]/extensions/[EXTENSION NAME]`

For example,
```shell
cd /srv/mediawiki-staging/1.46/extensions/MirahezeMagic
sugit fetch origin pull/678/head:pr678
sugit switch pr678
mwdeploy --folders=1.46/extensions/MirahezeMagic --servers=test151
```

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

The ABORTED message will show which server failed. If it shows 'localhost', that means the error occured on the server you're deploying from. If the affected server is not fully down, you can SSH into it and run `sudo journalctl -e` to see what exactly is causing the error.

If icinga alerts do not show the failed server as depooled, you should probably get someone to consider it or very quickly rollback. You may want to deploy to only the broken server first before deploying the rollback everywhere.

In some cases, for example if you're depooling a crashed database cluster during an outage, you may need to bypass the check. To do this, use `--force`. The check will still happen, but failures will be shown in your terminal output instead and will be ignored.

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