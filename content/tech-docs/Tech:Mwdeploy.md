---
title: Tech:Mwdeploy
---

`{{ {{Outdated}} }}`

**mwdeploy** is our MediaWiki deployment tool available on all MediaWiki servers.

The current canary server is mwtask181; test151 is managed separately by the same tool.

The --servers argument must currently be included. You should just append every command with `--servers=all` to deploy to all servers. Doing that on test151 will only deploy it locally on test151. You can include a comma separated list if you wish to deploy to specific servers.

## Logging 

All errors and warnings will log failure messages to [SAL](Tech:Server_admin_log.md). A deployment will abort if the commands to copy data from staging to the canary server.

You can add `--no-log`. This will direct output to your terminal rather than `logsalmsg`.

## The main parameters 

To deploy config changes (should happen automatically once puppet runs, is logged):
* `mwdeploy --config --servers=all`

To deploy MediaWiki with no i18n/l10n changes
* `mwdeploy --world --servers=all`

To deploy MediaWiki with i18n/l10n changes (equivalent to running MergeMessageLists and RebuildLC):
* `mwdeploy --world --l10n --servers=all`

You can use any mix of the 3 `--world --config and --l10n` parameters.

If you wanted to deploy a change to only a single file (or multiple specific files) without syncing all files:
* `mwdeploy --files=w/index.php,w/api.php --servers=all`

To sync a folder, or multiple folders:
* `mwdeploy --folders=1.40/extensions/Echo,1.40/skins/Vector --servers=all`

## If a canary check fails 

If you see 'DEPLOY ABORTED' in SAL, this means that one of the servers in the list failed checks to ensure mediawiki was not down. This is a fairly basic check, so it probably means the server is completely fataling.

If you need to bypass the check, use `--force`. The check will still happen, but failures will be shown in your terminal output instead and will be ignored.

The ABORTED message will show which server failed, hopefully it will be 'localhost' which means the server you are deploying from.

If icinga alerts do not show the failed server as depooled, you should probably get someone to consider it or very quickly rollback. You may want to deploy to only the broken server first before deploying the rollback everywhere.

## Failover a canary server 

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
**Source**: [https://meta.miraheze.org/wiki/Tech:Mwdeploy](https://meta.miraheze.org/wiki/Tech:Mwdeploy)