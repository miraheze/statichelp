---
title: Tech:Local patches
---

Though most extension/skin upgrades can be handled by [mwdeploy](/tech-docs/techmwdeploy) with ease, sometimes it is necessary to apply a **local patch** not available upstream.

## Considerations

Local patches should be avoided whenever possible in favor of submitting them upstream and updating the extension when the patch is merged and backported. However, in some situations local patches may be necessary:
* A security vulnerability requires a patch that cannot be publicized upstream.
* A fatal extension bug is affecting many wikis, but the patch's review upstream is stalled (e.g. the Math extension, see [T13808](https://meta.miraheze.org/wiki/phorge:T13808) on Phorge).

## Procedure

* Create a patch file. An example workflow is shown below, though other methods exist as well.
   * Make sure the last commit in your local repo is what you want to deploy
   * Run `git format-patch HEAD^ --stdout > <Patch name>.patch`
* Upload the patch file to your home directory on test151 for testing or the current canary server of mwdeploy (e.g. mwtask181) for global deployment.
* Go to the staging folder of the extension/skin.
* Run `sudo -u www-data git am ~/PatchName.patch`
* If the previous step gave you an error like "Committer identity unknown", run `sudo -u www-data git config --local user.name "www-data"` and try the previous step again
* Deploy it using mwdeploy (e.g. `mwdeploy --servers=all --folders=1.45/extensions/ExtensionName`). Security patches should use the `--no-log` option to avoid publicly disclosing the existence of a patch.
* Add the patch to [T14242](https://meta.miraheze.org/wiki/Phorge:T14242), a tracking task for local patches. This is not necessary for patches applied only to Mirabeta.

----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:Local_patches)**