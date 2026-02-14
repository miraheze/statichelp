---
title: Tech:Flow removal
---

`{{ {{Mbox|type=content|text=This page is a work-in-progress. Its content is not yet finalized.}} }}`
This page documents the procedure for removing [Extension:StructuredDiscussions](https://meta.miraheze.org/wiki/mw:Extension:StructuredDiscussions) (Flow) on Miraheze. Wiki administrators: if you have any questions, please send them to the [talk page](https://meta.miraheze.org/wiki/{{TALKPAGENAME}}) and ping [User:PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna).

## Process

This is for the technology team's reference and for any third party interested in undeploying the extension.
* Ensure that no namespace defaults to content model `flow-board`. 
```
sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php ./ConvertFlowToWikitext.php --wiki=wiki
```
* Use [pppery's script](https://gitlab.wikimedia.org/pppery/flow-export-with-history) to convert all Flow boards to wikitext and replace their history with wikitext revisions. Note that the script may require database access for certain edge cases. 
```
python prep.py wikiname
python fullConvert.py
```
* Do some [#Cleanup](#cleanup) if needed.
* Disable the Flow extension.
* Follow [https://wikitech.wikimedia.org/wiki/Flow](https://wikitech.wikimedia.org/wiki/Flow) to delete orphaned pages in the `Topic` namespace. 
```
sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php sql --wiki=testwiki --query="SELECT CONCAT('Topic:', page_title) AS page_title FROM page WHERE page_namespace=2600;" --json | jq -r '.[].page_title' > pages.txt
```
 
```
sudo -u www-data php /srv/mediawiki/1.44/maintenance/run.php deleteBatch --wiki=testwiki --u='Miraheze maintenance script' --r='Remove lingering Topic NS pages after uninstalling Flow' pages.txt
```

## Cleanup

Links to pages in the `Topic` namespace will be invalidated. To fix them, [https://gitlab.wikimedia.org/pppery/flow-topic-links-fix](https://gitlab.wikimedia.org/pppery/flow-topic-links-fix) can be run. It does not require the flow board to be present but does require both Flow and CirrusSearch to be installed, which are not available on some wikis. This *could* be offered for wikis interested in keeping links but will involve more efforts.

## Timeline

There are more than 200 wikis that use Flow. The majority of them have never created any Flow boards, so the extension can be disabled for them without any cleanup required. That leaves 79 wikis with Flow boards that need to be converted to wikitext for archival purposes before removing Flow.

In the table below, "undeploy Flow" means: convert all Flow boards to wikitext, disable Flow, and then remove all pages in Topic NS.
| Event | Date (UTC) |
| --- | --- |
| Disable Flow for all wikis that have not created any Flow boards | 2026-02-10 |
| Undeploy Flow on [Public Test Wiki](https://meta.miraheze.org/wiki/testwiki:) | 2026-02-11 |
| Undeploy Flow on most wikis. As of writing 19 wikis remain unconverted either due to their size, their visibility (private), or some technical issue with a few pages that prevent them from being exported to wikitext. | 2026-02-13 |

## Aftermath

Due to a mistaken update to the XML export script, all edits in the page history are identified as being made by "Unknown user" on some wikis.

----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:Flow_removal)**