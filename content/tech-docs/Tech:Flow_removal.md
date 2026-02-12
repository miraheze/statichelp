---
title: Tech:Flow removal
---

`{{ {{Mbox|type=content|text=This page is a work-in-progress. Its content is not yet finalized.}} }}`
This page documents the procedure for removing [Extension:StructuredDiscussions](https://meta.miraheze.org/wiki/mw:Extension:StructuredDiscussions) (Flow) on Miraheze. Wiki administrators: if you have any questions, please send them to the [talk page](https://meta.miraheze.org/wiki/{{TALKPAGENAME}}) and ping [User:PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna).

## Process

This is for the technology team's reference and for any third party interested in undeploying the extension.
* Use [pppery's script](https://gitlab.wikimedia.org/pppery/flow-export-with-history) to convert all Flow boards to wikitext and replace their history with wikitext revisions. Note that the script may require database access for certain edge cases.
* Do some [#Cleanup](#cleanup) if needed.
* Disable the Flow extension.
* Follow [https://wikitech.wikimedia.org/wiki/Flow](https://wikitech.wikimedia.org/wiki/Flow) to delete orphaned pages in the `Topic` namespace.
   * `sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php sql --wiki=testwiki --query="SELECT CONCAT('Topic:', page_title) AS page_title FROM page WHERE page_namespace=2600;" --json | jq -r '.[].page_title' > pages.txt`
   * `sudo -u www-data php /srv/mediawiki/1.45/maintenance/run.php deleteBatch --wiki=testwiki --u='Miraheze maintenance script' --r='Remove lingering Topic NS pages after uninstalling Flow' pages.txt`

## Cleanup

Links to pages in the `Topic` namespace will be invalidated. To fix them, [https://gitlab.wikimedia.org/pppery/flow-topic-links-fix](https://gitlab.wikimedia.org/pppery/flow-topic-links-fix) can be run. It does not require the flow board to be present but does require both Flow and CirrusSearch to be installed, which are not available on some wikis. This *could* be offered for wikis interested in keeping links but will involve more efforts.

----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:Flow_removal)**