---
title: Tech:CirrusSearch
---

## Troubleshooting 

### illegal_argument_exception: no mapping found for field [suggest] 

This was seen in [T13277](https://meta.miraheze.org/wiki/phorge:T13277) and [T13334](https://meta.miraheze.org/wiki/phorge:T13334) when checking Greylog for a failed search request. This error is related to [#Primary index was expected to be an alias](#primary-index-was-expected-to-be-an-alias), and it can be fixed by fixing that as well.

### Primary index was expected to be an alias 

This was first seen in [T13334](https://meta.miraheze.org/wiki/phorge:T13334) when running CirrusSearch:UpdateSearchIndexConfig on a wiki exhibiting "illegal_argument_exception: no mapping found for field [suggest]". Unfortunately, it is not yet known what causes this. For now, this can be worked around by manually deleting the wiki's indices:
```shell
$ curl -X DELETE https://opensearch-mw.wikitide.net/testwiki_{content,general}
```

The output should be 
```json
{"acknowledged":true}{"acknowledged":true}
```
.

Afterwards, rebuild the search index from scratch. This would normally incur downtime for searching, but considering that searching is already broken, this doesn't really matter. Instructions ([copied from CirrusSearch README](https://gerrit.wikimedia.org/r/plugins/gitiles/mediawiki/extensions/CirrusSearch/+/1f4719b6b1445888014c03527028f5497a269406/README#162)):
```shell
$ mwscript CirrusSearch:UpdateSearchIndexConfig testwiki --startOver
$ mwscript CirrusSearch:ForceSearchIndex testwiki
```

This problem was once recorded to have happened ever since CirrusSearch was enabled on the wiki ([T13277#266442](https://meta.miraheze.org/wiki/phorge:T13277#266442)).

----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:CirrusSearch)**