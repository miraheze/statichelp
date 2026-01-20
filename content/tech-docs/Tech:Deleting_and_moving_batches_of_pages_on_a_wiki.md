---
title: Tech:Deleting and moving batches of pages on a wiki
---

`{{ {{shortcut|Tech:DELETEBATCH|Tech:MOVEBATCH}} }}`

To delete or move large batches of pages on a wiki, use the following steps with the `deleteBatch.php` or `moveBatch.php` MediaWiki maintenance scripts:

* **Login** to [mwtask181](/tech-docs/techmwtask181) (the active maintenance server).
* **Upload a text file** (e.g. `subdomain.txt`) to your shell account. This file should list the pages to be deleted or moved — **including namespaces**, if applicable.
* **Run the appropriate maintenance script** using `mwscript`. Replace the placeholders with actual values:

```bash
mwscript deleteBatch wikidbname --u="Miraheze maintenance script" --r="[[phorge:T###|Requested]]" /home/yourshellusername/subdomain.txt
```

Or, if moving pages instead of deleting:

```bash
mwscript moveBatch wikidbname --u="Miraheze maintenance script" --r="[[phorge:T###|Requested]]" /home/yourshellusername/subdomain.txt
```

*Note:* Use `moveBatch.php` or `deleteBatch.php` as appropriate. You may need to use additional arguments then what is mentioned here.

* **Logout** once your task is complete on [mwtask181](/tech-docs/techmwtask181).

## Categories

* [Category:Technology guidelines and guides](https://meta.miraheze.org/wiki/Category:Technology_guidelines_and_guides)

----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:Deleting_and_moving_batches_of_pages_on_a_wiki)**