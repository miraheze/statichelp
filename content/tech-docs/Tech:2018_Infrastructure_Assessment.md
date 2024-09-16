---
title: Tech:2018 Infrastructure Assessment
---

This is a page designed to be a working ground for analysing the infrastructure Miraheze runs as of the 26th of July 2018.

## Current Infrastructure 

| Server | Primary Use | Services | CPU | Disk | Memory | Price (/mo) |
| --- | --- | --- | --- | --- | --- | --- |
| [bacula1](https://meta.miraheze.org/wiki/Tech:bacula1) | Backups | bacula, salt-minion | 1x2.40GHz | 500G | 512MB | $12 |
| [cp2](https://meta.miraheze.org/wiki/Tech:cp2) | Caching | varnish, salt-minion | 1x3.40GHz | 25G | 256MB | $2.67 |
| [cp4](https://meta.miraheze.org/wiki/Tech:cp4) | Caching | varnish, salt-minion | 1x2.40GHz | 40G | 1GB | $3.50 |
| [cp5](https://meta.miraheze.org/wiki/Tech:cp5) | Caching | varnish, salt-minion | 1x2.30GHz | 25G | 1GB | $5 |
| [db4](https://meta.miraheze.org/wiki/Tech:db4) | Database | MariaDB, postgres, salt-minion, bacula-client | 4x3.30GHz | 377G | 16GB | $80 |
| [misc1](https://meta.miraheze.org/wiki/Tech:misc1) | Miscellaneous | dns, icinga, grafana, irc bots, mail, salt-minion | 1x2.40GHz | 40G | 1GB | $3.15 |
| [misc2](https://meta.miraheze.org/wiki/Tech:misc2) | Miscellaneous | redis, piwik, salt-minion | 1x2.40GHz | 40G | 1GB | $3.15 |
| [misc3](https://meta.miraheze.org/wiki/Tech:misc3) | Miscellaneous | parsoid, electron, restbase, salt, salt-minion | 2x2.40GHz | 60G | 2GB | $7 |
| [misc4](https://meta.miraheze.org/wiki/Tech:misc4) | Miscellaneous | bacula-client, lizardfs-master, phabricator | 2x2.40GHz | 60G | 2GB | $7 |
| [mw1](https://meta.miraheze.org/wiki/Tech:mw1) | MediaWiki | mediawiki, salt-minion | 4x3.30GHz | 75G | 1GB | $10 |
| [mw2](https://meta.miraheze.org/wiki/Tech:mw2) | MediaWiki | mediawiki, salt-minion | 4x3.30GHz | 75G | 1GB | $10 |
| [mw3](https://meta.miraheze.org/wiki/Tech:mw3) | MediaWiki | mediawiki, salt-minion, jobrunner | 4x3.30GHz | 75G | 1GB | $10 |
| [ns1](https://meta.miraheze.org/wiki/Tech:ns1) | DNS | dns | 1x3.40GHz | 12G | 128MB | $1.13 |
| [puppet1](https://meta.miraheze.org/wiki/Tech:puppet1) | Puppet | puppet, salt-minion, bacula-client | 2x2.40GHz | 60G | 2GB | $7 |
| [lizardfs1](https://meta.miraheze.org/wiki/Tech:lizardfs1) | Static | lizardfs, salt-minion, bacula-client | 2x2.30GHz | 150G | 512MB | $4.85 |
| [lizardfs2](https://meta.miraheze.org/wiki/Tech:lizardfs2) | Static | lizardfs, salt-minion, bacula-client | 2x2.30GHz | 150G | 512MB | $4.85 |
| [test1](https://meta.miraheze.org/wiki/Tech:test1) | Testing | mediawiki, salt-minion | CPU: 1x2.40GHz | 40G | 1GB | $3.50 |

----
**Source**: [https://meta.miraheze.org/wiki/Tech:2018_Infrastructure_Assessment](https://meta.miraheze.org/wiki/Tech:2018_Infrastructure_Assessment)