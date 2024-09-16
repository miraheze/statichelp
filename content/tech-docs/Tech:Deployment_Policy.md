---
title: Tech:Deployment Policy
---

Deployments happen regularly, and we deploy MediaWiki updates on a weekly cadence.

When reviewing a change to deploy, you must be sure of what it requires, this may include:
* Maintenance scripts
* Deployment parameters
* Resting

You can find this information by using what's available to you. You might want to consider the tags on PRs for updates.
* A build tag means it should not affect production.
* An i18n tag indicates you must add --l10n when deploying it.
* The schema change tag indicates SQL files have changed and should be applied.
* There is a ready to deploy tag to show someone is happy with it.

When merging updates, you should not rush. The following is a recommended order:
* Security updates
* build only changes
* i18n only or i18n with build
* Code changes without schema
* SQL changes

You should also consider how many you can safely test at once.

You must use the beta environment to deploy to first unless you are certain that the changes will not cause issues.

The final say with any deployment rests with the deployer. It is perfectly acceptable to say you are uncomfortable deploying a change.

## Gomerge 

[GoMerge](https://github.com/Cian911/gomerge) can be used to merge pull requests in batch. Please see it's readme for how to install.

`gomerge list --merge-method squash -r miraheze/mediawiki -t <token>` should be used to merge PRs.

Press space to (un)select and enter to run.

----
**Source**: https://meta.miraheze.org/wiki/Tech:Deployment_Policy