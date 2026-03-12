---
title: Tech:Server usage
---

 `{{ {{Tech navigation|servers|header=Servers|description=Miraheze has lots of servers in order to support its massive user base. Learn more about them here on Miraheze Meta.|keywords=miraheze servers}} }}`

Miraheze requires lots of **servers** in order to provide service. With over 400,000 unique visits and millions of page views per day, we require quite a bit of processing power.

Currently, servers at Miraheze are used for:

* [Cache proxy](/tech-docs/techvarnish): [cp161](/tech-docs/techcp161), [cp171](/tech-docs/techcp171), [cp191](/tech-docs/techcp191), [cp201](/tech-docs/techcp201),
* [Database](/tech-docs/techmariadb): [db151](/tech-docs/techdb151), [db161](/tech-docs/techdb161), [db171](/tech-docs/techdb171), [db172](/tech-docs/techdb172), [db181](/tech-docs/techdb181), [db182](/tech-docs/techdb182), [db192](/tech-docs/techdb192), [db201](/tech-docs/techdb201)
* [DNS](/tech-docs/techdns): [ns1](/tech-docs/techns1), [ns2](/tech-docs/techns2)
* [Mattermost](/tech-docs/techmattermost): [mattermost2](/tech-docs/techmattermost2)
* [MediaWiki](/tech-docs/techmediawiki_appserver): [mw151](/tech-docs/techmw151), [mw152](/tech-docs/techmw152), [mw153](/tech-docs/techmw153), [mw161](/tech-docs/techmw161), [mw162](/tech-docs/techmw162), [mw163](/tech-docs/techmw163), [mw171](/tech-docs/techmw171), [mw172](/tech-docs/techmw172), [mw173](/tech-docs/techmw173), [mw181](/tech-docs/techmw181), [mw182](/tech-docs/techmw182), [mw183](/tech-docs/techmw183), [mw191](/tech-docs/techmw191), [mw192](/tech-docs/techmw192), [mw193](/tech-docs/techmw193), [mw201](/tech-docs/techmw201), [mw202](/tech-docs/techmw202), [mw203](/tech-docs/techmw203), [mwtask151](/tech-docs/techmwtask151), [mwtask161](/tech-docs/techmwtask161), [mwtask171](/tech-docs/techmwtask171), [mwtask181](/tech-docs/techmwtask181)
* [Swift](/tech-docs/techswift): [swiftac171](/tech-docs/techswiftac171), [swiftobject151](/tech-docs/techswiftobject151), [swiftobject161](/tech-docs/techswiftobject161), [swiftobject171](/tech-docs/techswiftobject171), [swiftobject181](/tech-docs/techswiftobject181), [swiftobject191](/tech-docs/techswiftobject191), [swiftobject201](/tech-docs/techswiftobject201), [swiftproxy161](/tech-docs/techswiftproxy161), [swiftproxy171](/tech-docs/techswiftproxy171)
* Miscellaneous
   * [mon181](/tech-docs/techmon181): [Grafana](/tech-docs/techgrafana), [Icinga](/tech-docs/techicinga)
   * [phorge171](/tech-docs/techphorge171): [Phorge](/tech-docs/techphorge)
   * [mem151](/tech-docs/techmem151), [mem161](/tech-docs/techmem161), [mem191](/tech-docs/techmem191), [mem201](/tech-docs/techmem201): [Memcached](/tech-docs/techmemcached)
   * [graylog161](/tech-docs/techgraylog161): [Graylog](/tech-docs/techgraylog)
   * [ldap171](/tech-docs/techldap171): [Ldap](/tech-docs/techldap)
   * [matomo151](/tech-docs/techmatomo151): [Matomo](/tech-docs/techmatomo)
   * [prometheus151](/tech-docs/techprometheus151): Prometheus
* [Puppet](/tech-docs/techpuppet): [puppet181](/tech-docs/techpuppet181)
* Testing MediaWiki: [test151](/tech-docs/techtest151)

## Table of servers 

```
{{ {{#dpl:
|category = Running servers
|include  = {Server}:name:memory:cpu:nvme:location:os:usage:cloud
|table    = class="wikitable sortable",-,server name,Memory (RAM), CPU, Storage, Host/Location, Debian Version, Usage, Cloud
|tablerow = [[Tech:%%|%%]], %%, %%, %% U.2 NVMe, %%, %%, %%, %%, %%
|namespace = Tech
|ordermethod = title
}} }}
```

*Note*: Some information such as specs may be incorrect.

## Decommissioned servers 

```
{{ {{#dpl:
|category = Decommissioned servers
|include  = {Server}:name:memory:cpu:ssd:hdd:location:os:kernel:usage:cloud
|table    = class="wikitable sortable",-,server name,Memory (RAM), CPU, SSD, HDD, Host/Location, Debian Version, Kernel Version, Usage, Cloud
|tablerow = [[Tech:%%|%%]], %%, %%, %%, %%, %%, %%, %%, %%
|namespace = Tech
|ordermethod = title
}} }}
```

| server name | specs | date started | decommissioned date | former cost per month |
| --- | --- | --- | --- | --- |
| ~~cp26~~ *decommissioned* | 6 GB, 4 core @ 2.65 GHz, 100 GB SSD | 24 January 2024 | 2 September 2024 | $5.50 |
| ~~cp27~~ *decommissioned* | 6 GB, 4 core @ 2.65 GHz, 100 GB SSD | 28 January 2024 | 2 September 2024 | $5.50 |
| ~~cp36 (cloud16)~~ *[renamed](/tech-docs/techcp161)* | 10 GB, 6 cores @ 2.65 GHz, 100 GB U.2 NVMe | | 10 June 2025 |  |
| ~~cp37 (cloud17)~~ *[renamed](/tech-docs/techcp171)* | 32 GB, 8 cores @ 2.65 GHz, 500 GB U.2 NVMe | | 10 June 2025 |  |
| ~~cp38 (cloud19)~~ *[renamed](/tech-docs/techcp191)* | 32 GB, 8 cores @ 2.65 GHz, 500 GB U.2 NVMe | | 10 June 2025 |  |
| ~~cp41~~ *decommissioned* | 6 GB, 4 core @ 2.65 GHz, 100 GB SSD | 24 January 2024 | 2 September 2024 | $7.75 |
| ~~cp51~~ *decommissioned* | 6 GB, 4 core @ 2.65 GHz, 100 GB SSD | 24 January 2024 | 2 September 2024 | $7.40 |
| ~~lizardfs6~~ *decommissioned* | 32GB, 8 core @ 3.5GHz, 2 TB HDD | |  |  |
| changeprop151 | 12 GB, 8 cores (unknown speed), 20 GB U.2 NVMe | |  |  |
| graphite151 | 4 GB, 4 cores (unknown speed), 30 GB U.2 NVMe | |  |  |
| mw154 | 12 GB, 12 cores (unknown speed), 60 GB U.2 NVMe | |  |  |
| mw164 | 12 GB, 12 cores (unknown speed), 60 GB U.2 NVMe | |  |  |
| mw174 | 12 GB, 12 cores (unknown speed), 60 GB U.2 NVMe | |  |  |
| mw184 | 12 GB, 12 cores (unknown speed), 60 GB U.2 NVMe | |  |  |
| changeprop201 | 10 GB, 8 cores (unknown speed), 20 GB U.2 NVMe | |  |  |
| eventgate181 | 6 GB, 4 cores (unknown speed), 20 GB U.2 NVMe | |  |  |
| kafka181 | 20 GB, 8 cores (unknown speed), 30 GB U.2 NVMe | |  |  |
| mattermost1 | 2 GB, 2 cores (unknown speed), 40 GB SSD | |  |  |
| rdb151 | 4 GB, 2 cores (unknown speed), 10 GB U.2 NVMe | |  |  |

## Categories

* [Category:Servers](https://meta.miraheze.org/wiki/Category:Servers)

----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:Server_usage)**