---
title: Tech:Upgrading MediaWiki
---

## Pulling the new MediaWiki version

* Update [hieradata/common.yaml](https://meta.miraheze.org/wiki/github:miraheze/puppet/blob/master/hieradata/common.yaml) on [Puppet](/tech-docs/techpuppet) to pull the new version ([example](https://meta.miraheze.org/wiki/github:miraheze/puppet/blob/706206b92cb428ac4223f829b45289066d4e4b05/hieradata/common.yaml#L11C1-L12C22)). Add separately to test151's hieradata ([example](https://meta.miraheze.org/wiki/github:miraheze/puppet/commit/3034cf5fb05ac1bff0dbe216ee36d24d815ca945)). It will be pulled on the next Puppet run.
* Make the new release the default version on Mirabeta at test151's hieradata ([example](https://meta.miraheze.org/wiki/github:miraheze/puppet/commit/c5b3003c42b156b320db55356d6bc656ad097640)).
* Update `MirahezeFunctions`' `MEDIAWIKI_VERSIONS` constant and mark the new version as the "beta" version ([example](https://meta.miraheze.org/wiki/github:miraheze/mw-config/commit/498f935e7f9b679146f48ecdebd5b684f159899b)).
* Change all wikis on Mirabeta to the new release using the [changeMediaWikiVersion.php](https://meta.miraheze.org/wiki/github:miraheze/MirahezeMagic/blob/master/maintenance/changeMediaWikiVersion.php) maintenance script from MirahezeMagic if this didn't happen automatically.
* Locate any possible new SQL patches and maintenance scripts that may need to be applied/run on the new version using MirahezeMagic's [findSQLPatches.php](https://meta.miraheze.org/wiki/github:miraheze/MirahezeMagic/blob/master/maintenance/findSQLPatches.php) and [findPossibleUpgradeScripts.php](https://meta.miraheze.org/wiki/github:miraheze/MirahezeMagic/blob/master/maintenance/findPossibleUpgradeScripts.php). Apply/run them on wikis at Mirabeta/on the global database as needed.

## Preparing for the MediaWiki upgrade in production

Two tasks should be created on [Phorge](https://meta.miraheze.org/wiki/Phorge), one to upgrade MediaWiki (example: [phorge:T12041](https://meta.miraheze.org/wiki/phorge:T12041)) and another to test extensions (example: [phorge:T12042](https://meta.miraheze.org/wiki/phorge:T12042)).

Now there's nothing to do but test stuff until the new version is officially released by upstream.

## Upgrading production

 `{{ {{Note|An upgrade should not be done on your own, and should be planned in advance with the team}} }}`

Once the new version has been officially released, it's time for prod to be upgraded.

* Run `mwdeploy --upgrade-world --versions=<new version> --servers=all` on mwtask.
* Use [findSQLPatches.php](https://meta.miraheze.org/wiki/github:miraheze/MirahezeMagic/blob/master/maintenance/findSQLPatches.php) and [findPossibleUpgradeScripts.php](https://meta.miraheze.org/wiki/github:miraheze/MirahezeMagic/blob/master/maintenance/findPossibleUpgradeScripts.php) to locate any possible needed SQL patches and maintenance scripts. Note them on the upgrade task.
* The MediaWiki team should now decide on an upgrade date, where at least 2 people (and someone with root access, just in case) will be available during the upgrade and a bit of time after it. This date should be announced on [Discord](https://meta.miraheze.org/wiki/Discord), social media, [on-wiki](/tech-docs/technoticeboard), etc...
* Upgrade all wikis to the new version using [changeMediaWikiVersion.php](https://meta.miraheze.org/wiki/github:miraheze/MirahezeMagic/blob/master/maintenance/changeMediaWikiVersion.php).
* Set the new version as the default release in [hieradata/common.yaml](https://meta.miraheze.org/wiki/github:miraheze/puppet/blob/master/hieradata/common.yaml).
* Make the new version the "stable" version on `MirahezeFunctions`' `MEDIAWIKI_VERSIONS` constant.
* Run maintenance scripts and apply SQL patches as needed.



----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:Upgrading_MediaWiki)**