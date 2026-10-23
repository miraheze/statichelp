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
* Upload the patch file to your home directory on test151 for testing.
* Go to the staging folder of the extension/skin.
* Run `sugit am ~/PatchName.patch`
* If the previous step gave you an error like "Committer identity unknown", run `sugit config --local user.name "www-data"` and try the previous step again
* Deploy it using mwdeploy (e.g. `mwdeploy --servers=all --folders=1.45/extensions/ExtensionName`). Security patches should use the `--no-log` option to avoid publicly disclosing the existence of a patch.
* Once the patch is confirmed to be working on test151, add the patch to [https://github.com/miraheze/mediawiki-repos](https://github.com/miraheze/mediawiki-repos). Security patches should go into the private patch repository. Once added, puppet will automatically sync the patch on both test151 and mwtask181.
* Once the patch is on mwtask181, run the usual mwdeploy upgrade extension workflow.

## Removing a local patch

If a local patch is no longer needed, it should be removed so that mwdeploy can handle updates automatically. Assuming that the local patch is the last commit in the extension's repository, patch removal can be done with `sugit reset --hard HEAD^`.

----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:Local_patches)**