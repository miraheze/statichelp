---
title: Tech:Deleting and moving batches of pages on a wiki
---

`{{ {{shortcut|Tech:DELETEBATCH|Tech:MOVEBATCH}} }}`

To delete or move large batches of pages on a wiki, use the following steps with the `deleteBatch.php` or `moveBatch.php` MediaWiki maintenance scripts:

* **Login** to [mwtask181](/tech-docs/techmwtask181) (the active maintenance server).
* **Upload a text file** (e.g. `subdomain.txt`) to your shell account. This file should list the pages to be deleted or moved — **including namespaces**, if applicable.
* **Run the appropriate maintenance script** using `mwscript`. Replace the placeholders with actual values:
 `{{ {{Note}} }}` You may want to use [nukeNS.php](https://meta.miraheze.org/wiki/mw:Manual:nukeNS.php) rather than deleteBatch.

```bash
mwscript deleteBatch wikidbname --u="'<your username> (Miraheze)'" --r="'[[phorge:T###|Requested]]'" deleteBatch.txt
```

Or, if moving pages instead of deleting:

```bash
mwscript moveBatch wikidbname --u="'<your username> (Miraheze)'" --r="'[[phorge:T###|Requested]]'" moveBatch.txt
```

*Note:* Use `moveBatch.php` or `deleteBatch.php` as appropriate. You may need to use additional arguments then what is mentioned here.

* **Logout** once your task is complete on [mwtask181](/tech-docs/techmwtask181).

## Categories

* [Category:Technology guidelines and guides](https://meta.miraheze.org/wiki/Category:Technology_guidelines_and_guides)

----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:Deleting_and_moving_batches_of_pages_on_a_wiki)**