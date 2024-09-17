---
title: Tech:Server usage
---

 `{{ {{Tech navigation|servers|header=Servers|description=Miraheze has lots of servers in order to support its massive user base. Learn more about them here on Miraheze Meta.|keywords=miraheze servers}} }}`

Miraheze requires lots of **servers** in order to provide service. With over 400,000 unique visits and millions of page views per day, we require quite a bit of processing power.

Currently, servers at Miraheze are used for:

* Cache proxy: [cp26](https://meta.miraheze.org/wiki/Tech:Cp26), [cp27](https://meta.miraheze.org/wiki/Tech:Cp27), [cp36](https://meta.miraheze.org/wiki/Tech:Cp36), [cp37](https://meta.miraheze.org/wiki/Tech:Cp37), [cp41](https://meta.miraheze.org/wiki/Tech:Cp41), [cp51](https://meta.miraheze.org/wiki/Tech:Cp51)
* Database: [db151](/tech-docs/techdb151), [db161](/tech-docs/techdb161), [db171](/tech-docs/techdb171), [db181](/tech-docs/techdb181), [db182](/tech-docs/techdb182)
* DNS: [ns1](/tech-docs/techns1), [ns2](/tech-docs/techns2)
* MediaWiki: [mw151](/tech-docs/techmw151), [mw152](/tech-docs/techmw152), [mw153](https://meta.miraheze.org/wiki/Tech:Mw153), [mw154](https://meta.miraheze.org/wiki/Tech:Mw154), [mw161](/tech-docs/techmw161), [mw162](/tech-docs/techmw162), [mw163](https://meta.miraheze.org/wiki/Tech:Mw163), [mw164](https://meta.miraheze.org/wiki/Tech:Mw164), [mw171](/tech-docs/techmw171), [mw172](/tech-docs/techmw172), [mw173](https://meta.miraheze.org/wiki/Tech:Mw173), [mw174](https://meta.miraheze.org/wiki/Tech:Mw174), [mw181](/tech-docs/techmw181), [mw182](/tech-docs/techmw182), [mw183](https://meta.miraheze.org/wiki/Tech:Mw183), [mw184](https://meta.miraheze.org/wiki/Tech:Mw184), [mwtask151](https://meta.miraheze.org/wiki/Tech:Mwtask151), [mwtask161](https://meta.miraheze.org/wiki/Tech:Mwtask161), [mwtask171](/tech-docs/techmwtask171), [mwtask181](/tech-docs/techmwtask181), [jobchron171](/tech-docs/techjobchron171)
* Swift: [swiftac171](/tech-docs/techswiftac171), [swiftobject151](/tech-docs/techswiftobject151), [swiftobject161](/tech-docs/techswiftobject161), [swiftobject171](/tech-docs/techswiftobject171), [swiftobject181](/tech-docs/techswiftobject181), [swiftproxy161](/tech-docs/techswiftproxy161), [swiftproxy171](/tech-docs/techswiftproxy171)
* Miscellaneous
   * [mon181](/tech-docs/techmon181): [Grafana](/tech-docs/techgrafana), [Icinga](/tech-docs/techicinga)
   * [phorge171](/tech-docs/techphorge171): [Phorge](/tech-docs/techphorge)
   * [mem151](/tech-docs/techmem151), [mem161](/tech-docs/techmem161): [Memcached](/tech-docs/techmemcached)
   * [graylog161](/tech-docs/techgraylog161): [Graylog](/tech-docs/techgraylog)
   * [ldap171](/tech-docs/techldap171): [Ldap](/tech-docs/techldap)
   * [matomo151](/tech-docs/techmatomo151): [Matomo](/tech-docs/techmatomo)
   * [prometheus151](/tech-docs/techprometheus151): Prometheus
* [Puppet](/tech-docs/techpuppet): [puppet181](/tech-docs/techpuppet181)
* Testing MediaWiki: [test151](/tech-docs/techtest151)

## Table of servers 

| server name | Memory (RAM) | CPU | Storage | Host | Location | Debian version | Kernel version |
| --- | --- | --- | --- | --- | --- | --- | --- |
| [cp26](https://meta.miraheze.org/wiki/Tech:cp26) | 6 GB | 4 core @ 2.65 GHz | 100 GB SSD | Contabo | Nuremburg, Germany | Bookworm | |
| [cp27](https://meta.miraheze.org/wiki/Tech:Cp27) | 6 GB | 4 core @ 2.65 GHz | 100 GB SSD | Contabo | Nuremburg, Germany | Bookworm | |
| [cp36](https://meta.miraheze.org/wiki/Tech:Cp36) (cloud16) | 4 GB | 4 core @ 2.65 GHz | 100 GB U.2 NVMe | Fiberstate | Salt Lake City, UT | Bookworm | |
| [cp37](https://meta.miraheze.org/wiki/Tech:Cp37) (cloud17) | 4 GB | 4 core @ 2.65 GHz | 100 GB U.2 NVMe | Fiberstate | Salt Lake City, UT | Bookworm | |
| [cp41](https://meta.miraheze.org/wiki/Tech:cp41) | 6 GB | 4 core @ 2.65 GHz | 100 GB SSD | Contabo | Hong Kong | Bookworm | |
| [cp51](https://meta.miraheze.org/wiki/Tech:Cp51) | 6 GB | 4 core @ 2.65 GHz | 100 GB SSD | Contabo | London, England | Bookworm | |
| [ns1](/tech-docs/techns1) (cloud17) | 1 GB | 1 core @ 2 GHz | 10 GB U.2 NVMe | Fiberstate | Salt Lake City, UT | Bookworm | |
| [ns2](/tech-docs/techns2) | 1 GB | 1 core (unknown speed) | 10 GB SSD | OVH | London, England | Bookworm | |
| [bast161](/tech-docs/techbast161) | 1 GB | 1 core (unknown speed) | 10 GB U.2 NVMe | Fiberstate | Salt Lake City, UT | Bookworm | |
| [bast181](/tech-docs/techbast181) | 1 GB | 1 core (unknown speed) | 10 GB U.2 NVMe | Fiberstate | Salt Lake City, UT | Bookworm | |
| [cloud15](/tech-docs/techcloud15) | 256 GB | 40 cores @ 3.2 GHz | 4 TB U.2 NVMe | Fiberstate | Salt Lake City, UT | Bookworm | |
| [cloud16](/tech-docs/techcloud16) | 256 GB | 40 cores @ 3.2 GHz | 4 TB U.2 NVMe | Fiberstate | Salt Lake City, UT | Bookworm | |
| [cloud17](/tech-docs/techcloud17) | 256 GB | 40 cores @ 3.2 GHz | 4 TB U.2 NVMe | Fiberstate | Salt Lake City, UT | Bookworm | |
| [cloud18](/tech-docs/techcloud18) | 256 GB | 40 cores @ 3.2 GHz | 4 TB U.2 NVMe | Fiberstate | Salt Lake City, UT | Bookworm | |
| [db151](/tech-docs/techdb151) | 50 GB | 6 cores (unknown speed) | 1 TB U.2 NVMe | Fiberstate | Salt Lake City, UT | Bookworm | |
| [db161](/tech-docs/techdb161) | 50 GB | 6 cores (unknown speed) | 1 TB U.2 NVMe | Fiberstate | Salt Lake City, UT | Bookworm | |
| [db171](/tech-docs/techdb171) | 50 GB | 6 cores (unknown speed) | 1 TB U.2 NVMe | Fiberstate | Salt Lake City, UT | Bookworm | |
| [db181](/tech-docs/techdb181) | 50 GB | 6 cores (unknown speed) | 1 TB U.2 NVMe | Fiberstate | Salt Lake City, UT | Bookworm | |
| [db182](/tech-docs/techdb182) | 14 GB | 6 cores (unknown speed) | 512 GB U.2 NVMe | Fiberstate | Salt Lake City, UT | Bookworm | |
| [os151](/tech-docs/techos151) | 8 GB | 2 cores (unknown speed) | 250 GB U.2 NVMe | Fiberstate | Salt Lake City, UT | Bookworm | |
| [os161](/tech-docs/techos161) | 8 GB | 2 cores (unknown speed) | 250 GB U.2 NVMe | Fiberstate | Salt Lake City, UT | Bookworm | |
| [graylog161](/tech-docs/techgraylog161) | 6 GB | 4 core (unknown speed) | 20 GB U.2 NVMe | Fiberstate | Salt Lake City, UT | Bookworm | |
| [jobchron171](/tech-docs/techjobchron171) | 2 GB | 2 core (unknown speed) | 9 GB U.2 NVMe | Fiberstate | Salt Lake City, UT | Bookworm | |
| [ldap171](/tech-docs/techldap171) | 1 GB | 1 core (unknown speed) | 10 GB U.2 NVMe | Fiberstate | Salt Lake City, UT | Bookworm | |
| [matomo151](/tech-docs/techmatomo151) | 4 GB | 4 cores (unknown speed) | 20 GB U.2 NVMe | Fiberstate | Salt Lake City, UT | Bookworm | |
| [mem151](/tech-docs/techmem151) | 64 GB | 2 core (unknown speed) | 10 GB U.2 NVMe | Fiberstate | Salt Lake City, UT | Bookworm | |
| [mem161](/tech-docs/techmem161) | 64 GB | 2 core (unknown speed) | 10 GB U.2 NVMe | Fiberstate | Salt Lake City, UT | Bookworm | |
| [mon181](/tech-docs/techmon181) | 4 GB | 4 cores (unknown speed) | 20 GB U.2 NVMe | Fiberstate | Salt Lake City, UT | Bookworm | |
| [mw151](/tech-docs/techmw151) | 12 GB | 12 cores (unknown speed) | 60 GB U.2 NVMe | Fiberstate | Salt Lake City, UT | Bookworm | |
| [mw152](/tech-docs/techmw152) | 12 GB | 12 cores (unknown speed) | 60 GB U.2 NVMe | Fiberstate | Salt Lake City, UT | Bookworm | |
| [mw161](/tech-docs/techmw161) | 12 GB | 12 cores (unknown speed) | 60 GB U.2 NVMe | Fiberstate | Salt Lake City, UT | Bookworm | |
| [mw162](/tech-docs/techmw162) | 12 GB | 12 cores (unknown speed) | 60 GB U.2 NVMe | Fiberstate | Salt Lake City, UT | Bookworm | |
| [mw171](/tech-docs/techmw171) | 12 GB | 12 cores (unknown speed) | 60 GB U.2 NVMe | Fiberstate | Salt Lake City, UT | Bookworm | |
| [mw172](/tech-docs/techmw172) | 12 GB | 12 cores (unknown speed) | 60 GB U.2 NVMe | Fiberstate | Salt Lake City, UT | Bookworm | |
| [mw181](/tech-docs/techmw181) | 12 GB | 12 cores (unknown speed) | 60 GB U.2 NVMe | Fiberstate | Salt Lake City, UT | Bookworm | |
| [mw182](/tech-docs/techmw182) | 12 GB | 12 cores (unknown speed) | 60 GB U.2 NVMe | Fiberstate | Salt Lake City, UT | Bookworm | |
| [mwtask181](/tech-docs/techmwtask181) | 12 GB | 12 cores (unknown speed) | 250 GB U.2 NVMe | Fiberstate | Salt Lake City, UT | Bookworm | |
| [phorge171](/tech-docs/techphorge171) | 2 GB | 1 core (unknown speed) | 50 GB U.2 NVMe | Fiberstate | Salt Lake City, UT | Bookworm | |
| [prometheus151](/tech-docs/techprometheus151) | 2 GB | 2 cores (unknown speed) | 150 GB U.2 NVMe | Fiberstate | Salt Lake City, UT | Bookworm | |
| [puppet181](/tech-docs/techpuppet181) | 8 GB | 6 cores (unknown speed) | 35 GB U.2 NVMe | Fiberstate | Salt Lake City, UT | Bookworm | |
| [reports171](/tech-docs/techreports171) | 1 GB | 2 cores (unknown speed) | 20 GB U.2 NVMe | Fiberstate | Salt Lake City, UT | Bookworm | |
| [swiftac171](/tech-docs/techswiftac171) | 6 GB | 6 cores (unknown speed) | 100 GB U.2 NVMe | Fiberstate | Salt Lake City, UT | Bookworm | |
| [swiftobject151](/tech-docs/techswiftobject151) | 6 GB | 6 cores (unknown speed) | 1.5 TB U.2 NVMe | Fiberstate | Salt Lake City, UT | Bookworm | |
| [swiftobject161](/tech-docs/techswiftobject161) | 6 GB | 6 cores (unknown speed) | 1.5 TB U.2 NVMe | Fiberstate | Salt Lake City, UT | Bookworm | |
| [swiftobject171](/tech-docs/techswiftobject171) | 6 GB | 6 cores (unknown speed) | 1.5 TB U.2 NVMe | Fiberstate | Salt Lake City, UT | Bookworm | |
| [swiftobject181](/tech-docs/techswiftobject181) | 6 GB | 6 cores (unknown speed) | 1.5 TB U.2 NVMe | Fiberstate | Salt Lake City, UT | Bookworm | |
| [swiftproxy161](/tech-docs/techswiftproxy161) | 4 GB | 4 cores (unknown speed) | 30 GB U.2 NVMe | Fiberstate | Salt Lake City, UT | Bookworm | |
| [swiftproxy171](/tech-docs/techswiftproxy171) | 4 GB | 4 cores (unknown speed) | 30 GB U.2 NVMe | Fiberstate | Salt Lake City, UT | Bookworm | |
| [test151](/tech-docs/techtest151) | 12 GB | 12 cores (unknown speed) | 100 GB U.2 NVMe | Fiberstate | Salt Lake City, UT | Bookworm | |

*Note*: Some information such as specs may be incorrect.

## Decommissioned servers 

| server name | specs | date started | decommissioned date | former cost per month |
| --- | --- | --- | --- | --- |
| ~~[cp1](https://meta.miraheze.org/wiki/Tech:cp1)~~ *decommissioned* | |  | 5 October 2017 | N/A |
| [<s>cp2</s>](https://meta.miraheze.org/wiki/Tech:cp2) *decommissioned* | 256MB SVZ, 1 core @ 3.40 GHz, 25 GB SSD | | 14 February 2020 | $8/qtr |
| [<s>cp3</s>](https://meta.miraheze.org/wiki/Tech:Cp3) *decommissioned* | 1GB, 1 core @ 3.40 GHz, | 13 March 2019 | | $10 (not paid by Miraheze) |
| [<s>cp4</s>](https://meta.miraheze.org/wiki/Tech:cp4) *decommissioned* | 256MB SVZ, 1 core @ 3.40 GHz, 25 GB SSD | 5 October 2017 | 19 March 2020 | $8/qtr |
| [<s>cp5</s>](https://meta.miraheze.org/wiki/Tech:Cp5) *decommissioned* | 1GB, 1 core, 25 GB SSD | 1 April 2018‎ | 5 April 2019‎ | |
| [<s>cp6</s>](https://meta.miraheze.org/wiki/Tech:Cp6) *decommissioned* | 2GB, 2 cores, 20 GB SSD | 7 February 2020 | 1 February 2021 | |
| [<s>cp7</s>](https://meta.miraheze.org/wiki/Tech:Cp7) *decommissioned* | 2GB, 2 cores, 20 GB SSD | 12 February 2020 | 1 February 2021 | |
| ~~[cp8](https://meta.miraheze.org/wiki/Tech:Cp8)~~ *decommissioned* | 2GB, 2 cores, 20 GB SSD | 11 February 2020 | 1 February 2021 | |
| [<s>cp9</s>](https://meta.miraheze.org/wiki/Tech:Cp9) *decommissioned* | |  |  |  |
| [<s>cp10</s>](https://meta.miraheze.org/wiki/Tech:Cp10) *decommissioned* | 2GB, 2 cores, 30 GB SSD | 1 February 2021 | |  |
| [<s>cp11</s>](https://meta.miraheze.org/wiki/Tech:Cp11) *decommissioned* | 2GB, 2 cores, 30 GB SSD | 1 February 2021 | |  |
| [<s>cp12</s>](https://meta.miraheze.org/wiki/Tech:Cp12) *decommissioned* | 2GB, 2 cores, 30 GB SSD | 1 February 2021 | |  |
| ~~[db1](https://meta.miraheze.org/wiki/Tech:db1)~~ *decommissioned* | |  | 5 October 2015 | N/A |
| ~~[db2](https://meta.miraheze.org/wiki/Tech:db2)~~ *decommissioned* | 8GB, 4 cores @ 2.30 GHz, 120G GB SSD | |  | N/A |
| ~~[db3](https://meta.miraheze.org/wiki/Tech:Db3)~~ *decommissioned* | 6GB, 2 cores @ 2.30 GHz, 100G GB SSD | |  | N/A |
| [<s>db4</s>](https://meta.miraheze.org/wiki/Tech:Db4) *decommissioned* | 16GB, 4 cores @ 3.3 GHz, 400GB GB SSD | | 29 March 2020 | $80 |
| [<s>db5</s>](https://meta.miraheze.org/wiki/Tech:Db5) *decommissioned* | 8GB, 2 cores @ 3.3 GHz, 200GB GB SSD | |  | $40 |
| [<s>db6</s>](https://meta.miraheze.org/wiki/Tech:Db6) *decommissioned* | |  |  |  |
| [<s>db7</s>](https://meta.miraheze.org/wiki/Tech:Db7) *decommissioned* | 16GB, 4 cores, 350 GB SSD | | 13 January 2021 |  |
| [<s>dbt1</s>](https://meta.miraheze.org/wiki/Tech:Dbt1) *decommissioned* | |  |  |  |
| ~~[Elasticsearch1](https://meta.miraheze.org/wiki/Tech:Elasticsearch1)~~ *decommissioned* | 1GB, 4 cores @ 3.3 GHz, 75 GB SSD | |  | $10 |
| [<s>gluster1</s>](https://meta.miraheze.org/wiki/Tech:Gluster1) *decommissioned* | 4GB, 4 cores, 708 GB SSD | 9 February 2020 | 1 February 2021 | |
| [<s>gluster2</s>](https://meta.miraheze.org/wiki/Tech:Gluster2) *decommissioned* | 4GB, 4 cores, 350 GB SSD | 06 May 2020 | 1 February 2021 | |
| [<s>graylog1</s>](https://meta.miraheze.org/wiki/Tech:Graylog1) *decommissioned* | 8GB, 2 cores, 550 GB SSD | | 1 February 2021 |  |
| [<s>jobrunner1</s>](https://meta.miraheze.org/wiki/Tech:Jobrunner1) *decommissioned* | 2GB, 3 cores, 30 GB SSD | 12 February 2020 | 1 February 2021 | |
| [<s>jobrunner2</s>](https://meta.miraheze.org/wiki/Tech:Jobrunner2) *decommissioned* | 2GB, 3 cores, 30 GB SSD | 26 September 2020‎ | 1 February 2021 | |
| [<s>jobrunner3</s>](https://meta.miraheze.org/wiki/Tech:Jobrunner3) *decommissioned* | 3GB, 3 cores, 30 GB SSD | 1 February 2021 | 11 August 2021 | |
| [<s>jobrunner4</s>](https://meta.miraheze.org/wiki/Tech:Jobrunner4) *decommissioned* | 3GB, 3 cores, 30 GB SSD | 1 February 2021 | 11 August 2021 | |
| [<s>ldap1</s>](https://meta.miraheze.org/wiki/Tech:Ldap1) *decommissioned* | 1GB, 1 core, 25 GB SSD | | 1 February 2021 |  |
| [<s>lizardfs1</s>](https://meta.miraheze.org/wiki/Tech:lizardfs1) *decommissioned* | 512MB, 2 core @ 2.30 GHz, 150 GB HDD | |  | $5 |
| [<s>lizardfs2</s>](https://meta.miraheze.org/wiki/Tech:_lizardfs2) *decommissioned* | 512MB, 2 core @ 2.30 GHz, 150 GB HDD | |  | $5 |
| [<s>lizardfs3</s>](https://meta.miraheze.org/wiki/Tech:_lizardfs3) *decommissioned* | 512MB, 2 core @ 2.30 GHz, 150 GB HDD | |  | $5 |
| [<s>lizardfs4</s>](https://meta.miraheze.org/wiki/Tech:lizardfs4) *decommissioned* | 1GB, 2 core @ 2.30 GHz, 325 GB HDD | |  | $5 |
| [<s>lizardfs5</s>](https://meta.miraheze.org/wiki/Tech:lizardfs5) *decommissioned* | 1GB, 2 core @ 2.30 GHz, 325 GB HDD | |  | $5 |
| [<s>lizardfs6</s>](https://meta.miraheze.org/wiki/Tech:lizardfs6) *decommissioned* | 32GB, 8 core @ 3.5GHz, 2 TB HDD | |  |  |
| [<s>mail1</s>](https://meta.miraheze.org/wiki/Tech:Mail1) *decommissioned* | 1GB, 1 core, 10 GB SSD | 12 February 2020 | 1 February 2021 | |
| [<s>misc1</s>](https://meta.miraheze.org/wiki/Tech:Misc1) *decommissioned* | 1GB, 1 core @ 2.40 GHz, 40 GB SSD | |  |  |
| [<s>misc2</s>](https://meta.miraheze.org/wiki/Tech:Misc2) *decommissioned* | 1GB, 1 core @ 2.40 GHz, 40 GB SSD | | 19 March 2020 | $3.15 |
| [<s>misc3</s>](https://meta.miraheze.org/wiki/Tech:Misc3) *decommissioned* | 1GB, 1 core @ 3.30 GHz, 40 GB SSD | | 19 March 2020 | $3.15 |
| [<s>misc4</s>](https://meta.miraheze.org/wiki/Tech:Misc4) *decommissioned* | 2GB, 1 core @ 2.30 GHz, 60 GB SSD | | 19 March 2020 | $7 |
| [<s>mw1</s>](https://meta.miraheze.org/wiki/Tech:Mw1) *decommissioned* | 1GB, 4 cores @ 3.40 GHz, 50 GB SSD | | 29 March 2020 | $10 |
| [<s>mw2</s>](https://meta.miraheze.org/wiki/Tech:Mw2) *decommissioned* | 1GB, 4 cores @ 3.40 GHz, 50 GB SSD | | 29 March 2020 | $10 |
| [<s>mw3</s>](https://meta.miraheze.org/wiki/Tech:Mw3) *decommissioned* | 1GB, 4 cores @ 3.40 GHz, 50 GB SSD | | 29 March 2020 | $10 |
| [<s>mw4</s>](https://meta.miraheze.org/wiki/Tech:Mw4) *decommissioned* | 3GB, 4 cores, 20 GB SSD | 8 February 2020 | 1 February 2021 | |
| [<s>mw5</s>](https://meta.miraheze.org/wiki/Tech:Mw5) *decommissioned* | 3GB, 4 cores, 20 GB SSD | 11 February 2020 | 1 February 2021 | |
| [<s>mw6</s>](https://meta.miraheze.org/wiki/Tech:Mw6) *decommissioned* | 3GB, 4 cores, 20 GB SSD | 11 February 2020 | 1 February 2021 | |
| [<s>mw7</s>](https://meta.miraheze.org/wiki/Tech:Mw7) *decommissioned* | 3GB, 4 cores, 20 GB SSD | 11 February 2020 | 1 February 2021 | |
| [<s>nfs1</s>](https://meta.miraheze.org/wiki/Tech:nfs1) *decommissioned* | 512 MB, 1 core @ 2.30 GHz, 15 GB HDD | |  | N/A |
| [<s>ns3</s>](https://meta.miraheze.org/wiki/Tech:Ns3) *decommissioned* | |  |  | N/A |
| [<s>parsoid1</s>](https://meta.miraheze.org/wiki/Tech:Parsoid1) *decommissioned* | |  |  | N/A |
| [<s>phab1</s>](https://meta.miraheze.org/wiki/Tech:Phab1) *decommissioned* | 1GB, 2 cores, 25 GB SSD | 12 February 2020 | 1 February 2021 | |
| [<s>puppet1</s>](https://meta.miraheze.org/wiki/Tech:Puppet1) *decommissioned* | 2GB, 2 core @ 2.30 GHz, 60 GB SSD | | 19 March 2020 | $7.00 |
| [<s>puppet2</s>](https://meta.miraheze.org/wiki/Tech:Puppet2) *decommissioned* | 5GB, 4 cores, 23 GB SSD | 8 February 2020 | 1 February 2021 | |
| [<s>rdb1</s>](https://meta.miraheze.org/wiki/Tech:Rdb1) *decommissioned* | 3GB, 2 cores, 10 GB SSD | 10 February 2020 | 1 February 2021 | |
| [<s>rdb2</s>](https://meta.miraheze.org/wiki/Tech:Rdb2) *decommissioned* | 3GB, 2 cores, 10 GB SSD | 12 February 2020 | 1 February 2021 | |
| [<s>services1</s>](https://meta.miraheze.org/wiki/Tech:Services1) *decommissioned* | 3GB, 2 cores, 10 GB SSD | 10 February 2020 | 1 February 2021 | |
| [<s>services2</s>](https://meta.miraheze.org/wiki/Tech:Services2) *decommissioned* | 3GB, 2 cores, 10 GB SSD | 12 February 2020 | 1 February 2021 | |
| [<s>services3</s>](https://meta.miraheze.org/wiki/Tech:Services3) *decommissioned* | 3GB, 2 cores, 10 GB SSD | 1 February 2021 | 31 October 2021 | |
| [<s>services4</s>](https://meta.miraheze.org/wiki/Tech:Services4) *decommissioned* | 3GB, 2 cores, 10 GB SSD | 1 February 2021 | 31 October 2021 | |
| [<s>swift1</s>](https://meta.miraheze.org/wiki/Tech:swift1) *decommissioned* | 512MB, 2 core @ 2.30 GHz, 150 GB HDD | |  | N/A |
| [<s>swift2</s>](https://meta.miraheze.org/wiki/Tech:swift2) *decommissioned* | 512MB, 2 core @ 2.30 GHz, 150 GB HDD | |  | N/A |
| [<s>test1</s>](https://meta.miraheze.org/wiki/Tech:Test1) *decommissioned* | 1GB, 4 cores @ 3.40 GHz, 50 GB SSD | | 19 March 2020 | $3.15 |
| [<s>test2</s>](https://meta.miraheze.org/wiki/Tech:Test2) *decommissioned* | 1.5GB, 1 core, 20 GB SSD | 10 February 2020 | 1 February 2021 | |
| [db11](https://meta.miraheze.org/wiki/Tech:Db11) | 8GB, 4 cores, 400GB GB NVMe | | 14 January 2022 |  |
| [db12](https://meta.miraheze.org/wiki/Tech:Db12) | 8GB, 4 cores, 400GB GB NVMe | | 14 January 2022 |  |
| [db13](https://meta.miraheze.org/wiki/Tech:Db13) | 8GB, 4 cores, 400GB GB NVMe | | 14 January 2022 |  |
| [gluster3](https://meta.miraheze.org/wiki/Tech:Gluster3) | 4GB, 3 cores, 708 GB SSD | 9 February 2020 | 14 January 2022 | |
| [gluster4](https://meta.miraheze.org/wiki/Tech:Gluster4) | 4GB, 3 cores, 350 GB SSD | 06 May 2020 | 14 January 2022 | |
| [graylog2](https://meta.miraheze.org/wiki/Tech:Gluster2) | 8GB, 2 cores, 550 GB SSD | 1 February 2021 | 14 January 2022 | |
| [mwtask1](https://meta.miraheze.org/wiki/Tech:Mwtask1) | 2GB, 2 cores, 50GB SSD | 11 August 2021 | 14 January 2022 | |
| [jobchron1](https://meta.miraheze.org/wiki/Tech:Jobchron1) | 2GB, 1 core, 10GB SSD | 11 August 2021 | 14 January 2022 | |
| [ldap2](https://meta.miraheze.org/wiki/Tech:Ldap2) | 1GB, 1 core, 25 GB SSD | 1 February 2021 | 14 January 2022 | |
| [mail2](https://meta.miraheze.org/wiki/Tech:Mail2) | 1GB, 1 core, 10 GB SSD | 1 February 2021 | 14 January 2022 | |
| [mem1](https://meta.miraheze.org/wiki/Tech:Mem1) | 8GB, 2 cores, 10 GB SSD | 1 February 2021 | 14 January 2022 | |
| [mem2](https://meta.miraheze.org/wiki/Tech:Mem2) | 8GB, 2 cores, 10 GB SSD | 1 February 2021 | 14 January 2022 | |
| [Mon1](https://meta.miraheze.org/wiki/Tech:Mon1) | 4GB, 2 cores, 30 GB | 12 February 2020 | 14 January 2022 | |
| [mw8](https://meta.miraheze.org/wiki/Tech:Mw8) | 3GB, 4 cores, 20 GB SSD | 1 February 2021 | 14 January 2022 | |
| [mw9](https://meta.miraheze.org/wiki/Tech:Mw9) | 3GB, 4 cores, 20 GB SSD | 1 February 2021 | 14 January 2022 | |
| [mw10](https://meta.miraheze.org/wiki/Tech:Mw10) | 3GB, 4 cores, 20 GB SSD | 1 February 2021 | 14 January 2022 | |
| [mw11](https://meta.miraheze.org/wiki/Tech:Mw11) | 3GB, 4 cores, 20 GB SSD | 1 February 2021 | 14 January 2022 | |
| [mw12](https://meta.miraheze.org/wiki/Tech:Mw12) | 4GB, 4 cores, 20 GB SSD | 11 August 2021 | 14 January 2022 | |
| [mw13](https://meta.miraheze.org/wiki/Tech:Mw13) | 4GB, 4 cores, 20 GB SSD | 11 August 2021 | 14 January 2022 | |
| [phab2](https://meta.miraheze.org/wiki/Tech:Phab2) | 1GB, 2 cores, 25 GB SSD | 1 February 2021 | 14 January 2022 | |
| [puppet3](https://meta.miraheze.org/wiki/Tech:Puppet3) | 5GB, 4 cores, 23 GB SSD | 1 February 2021 | 14 January 2022 | |
| [test3](https://meta.miraheze.org/wiki/Tech:Test3) | 1.5GB, 1 core, 20 GB SSD | 1 February 2021 | 14 January 2022 | |
| [bacula2](https://meta.miraheze.org/wiki/Tech:Bacula2) | 3GB, 2 cores, 1TB HDD | |  | $12 |
| [mw101](https://meta.miraheze.org/wiki/Tech:Mw101) | 5GB, 3 cores, 23GB SSD | |  |  |
| [mw102](https://meta.miraheze.org/wiki/Tech:Mw102) | 5GB, 3 cores, 23GB SSD | |  |  |
| [mw111](https://meta.miraheze.org/wiki/Tech:Mw111) | 5GB, 3 cores, 23GB SSD | |  |  |
| [mw112](https://meta.miraheze.org/wiki/Tech:Mw112) | 5GB, 3 cores, 23GB SSD | |  |  |
| [test101](https://meta.miraheze.org/wiki/Tech:test101) | 2GB, 1 core, 18GB SSD | |  |  |
| [mwtask111](https://meta.miraheze.org/wiki/Tech:Mwtask111) | 2GB, 2 cores, 68GB HDD | |  |  |
| [matomo101](https://meta.miraheze.org/wiki/Tech:matomo101) | 2GB, 1 core, 20GB SSD | |  |  |
| [ldap111](https://meta.miraheze.org/wiki/Tech:ldap111) | 1GB, 1 core, 9GB HDD | |  |  |
| [prometheus101](https://meta.miraheze.org/wiki/Tech:prometheus101) | 1GB, 1 core, 150GB HDD | |  |  |
| [mon111](https://meta.miraheze.org/wiki/Tech:mon111) | 4GB, 2 cores, 182GB HDD | |  |  |
| [puppet111](https://meta.miraheze.org/wiki/Tech:puppet111) | 6GB, 3 cores, 27GB SSD | |  |  |
| [es101](https://meta.miraheze.org/wiki/Tech:es101) | 4GB, 2 cores, 274GB HDD | |  |  |
| [es111](https://meta.miraheze.org/wiki/Tech:es111) | 4GB, 2 cores, 274GB HDD | |  |  |
| [es121](https://meta.miraheze.org/wiki/Tech:es121) | 4GB, 2 cores, 274GB HDD | |  |  |
| [mem121](https://meta.miraheze.org/wiki/Tech:mem121) | 7GB, 1 core, 9GB SSD | |  |  |
| [db111](https://meta.miraheze.org/wiki/Tech:Db111) | 10GB, 3 cores, 644GB SSD | |  |  |
| [gluster101](https://meta.miraheze.org/wiki/Tech:gluster101) | 3GB, 2 cores, 824GB HDD | |  |  |
| [gluster111](https://meta.miraheze.org/wiki/Tech:gluster111) | 3GB, 2 cores, 824GB HDD | |  |  |
| [gluster121](https://meta.miraheze.org/wiki/Tech:gluster121) | 3GB, 2 cores, 824GB HDD | |  |  |
| [bast101](https://meta.miraheze.org/wiki/Tech:bast101) | 1GB, 1 core, 18GB SSD | |  |  |
| [mem101](https://meta.miraheze.org/wiki/Tech:mem101) | 7GB, 1 core, 9GB SSD | |  |  |
| [cp20](https://meta.miraheze.org/wiki/Tech:cp20) | 2 GB, 1 core @ 2.40 GHz, 40 GB SSD | |  |  |
| [cp21](https://meta.miraheze.org/wiki/Tech:Cp21) | 2 GB, 1 core @ 2.40 GHz,40 GB SSD | |  |  |
| [cp30](https://meta.miraheze.org/wiki/Tech:Cp30) | 2 GB, 1 core @ 2.40 GHz,40 GB SSD | |  |  |
| [cp31](https://meta.miraheze.org/wiki/Tech:Cp31) | 2 GB, 1 core @ 2.40 GHz,40 GB SSD | |  |  |
| [bast121](https://meta.miraheze.org/wiki/Tech:bast121) | 1 GB, 1 core (unknown speed), 20 GB SSD | |  |  |
| [bast141](https://meta.miraheze.org/wiki/Tech:bast141) | 1 GB, 1 core (unknown speed), 10 GB SSD | |  |  |
| [cloud10](https://meta.miraheze.org/wiki/Tech:cloud10) | 64 GB, 24 cores @ 2.67 GHz, 960 GB SSD, 1.8 TB HDD | |  |  |
| [cloud11](https://meta.miraheze.org/wiki/Tech:cloud11) | 64 GB, 24 cores @ 2.67 GHz, 960 GB SSD, 1.8 TB HDD | |  |  |
| [cloud12](https://meta.miraheze.org/wiki/Tech:cloud12) | 64 GB, 24 cores @ 2.67 GHz, 960 GB SSD, 1.8 TB HDD | |  |  |
| [cloud13](https://meta.miraheze.org/wiki/Tech:cloud13) | 128 GB, 40 cores @ 2.80 GHz, 900 GB SSD | |  |  |
| [cloud14](https://meta.miraheze.org/wiki/Tech:cloud14) | 128 GB, 40 cores @ 2.80 GHz, 900 GB SSD | |  |  |
| [db101](https://meta.miraheze.org/wiki/Tech:Db101) | 10 GB, 3 cores (unknown speed), 644 GB SSD | |  |  |
| [db112](https://meta.miraheze.org/wiki/Tech:Db112) | 7 GB, 3 cores (unknown speed), 147 GB SSD | |  |  |
| [db121](https://meta.miraheze.org/wiki/Tech:Db121) | 10 GB, 3 cores (unknown speed), 641 GB SSD | |  |  |
| [db131](https://meta.miraheze.org/wiki/Tech:Db131) | 18 GB, 4 cores (unknown speed), 263 GB SSD | |  |  |
| [db111](https://meta.miraheze.org/wiki/Tech:Db111) | 18 GB, 4 cores (unknown speed), 263 GB SSD | |  |  |
| [es131](https://meta.miraheze.org/wiki/Tech:es131) | 4 GB, 2 cores (unknown speed), 221 GB SSD | |  |  |
| [es141](https://meta.miraheze.org/wiki/Tech:es141) | 4 GB, 2 cores (unknown speed), 221 GB SSD | |  |  |
| [graylog121](https://meta.miraheze.org/wiki/Tech:graylog121) | 2 GB, 1 core (unknown speed), 10 GB SSD | |  |  |
| [jonchron121](https://meta.miraheze.org/wiki/Tech:jobchron121) | 2 GB, 1 core (unknown speed), 9 GB HDD | |  |  |
| [ldap141](https://meta.miraheze.org/wiki/Tech:ldap141) | 1 GB, 1 core (unknown speed), 10 GB SSD | |  |  |
| [mail121](https://meta.miraheze.org/wiki/Tech:mail121) | 1 GB, 1 core (unknown speed), 9 GB HDD | |  |  |
| [matomo131](https://meta.miraheze.org/wiki/Tech:matomo131) | 2 GB, 2 cores (unknown speed), 20 GB SSD | |  |  |
| [mem131](https://meta.miraheze.org/wiki/Tech:mem131) | 12 GB, 1 core (unknown speed), 10 GB SSD | |  |  |
| [mem141](https://meta.miraheze.org/wiki/Tech:mem141) | 12 GB, 1 core (unknown speed), 10 GB SSD | |  |  |
| [mon141](https://meta.miraheze.org/wiki/Tech:mon141) | 2 GB, 3 cores (unknown speed), 20 GB SSD | |  |  |
| [mw131](https://meta.miraheze.org/wiki/Tech:Mw131) | 5 GB, 6 cores (unknown speed), 25 GB SSD | |  |  |
| [mw132](https://meta.miraheze.org/wiki/Tech:Mw132) | 5 GB, 6 cores (unknown speed), 25 GB SSD | |  |  |
| [mw141](https://meta.miraheze.org/wiki/Tech:Mw141) | 5 GB, 6 cores (unknown speed), 25 GB SSD | |  |  |
| [mw142](https://meta.miraheze.org/wiki/Tech:Mw142) | 5 GB, 6 cores (unknown speed), 25 GB SSD | |  |  |
| [mw121](https://meta.miraheze.org/wiki/Tech:Mw121) | 5 GB, 6 cores (unknown speed), 23 GB SSD | |  |  |
| [mw122](https://meta.miraheze.org/wiki/Tech:Mw122) | 5 GB, 6 cores (unknown speed), 23 GB SSD | |  |  |
| [mwtask141](https://meta.miraheze.org/wiki/Tech:Mwtask141) | 2 GB, 2 cores (unknown speed), 75 GB SSD | |  |  |
| [phab121](https://meta.miraheze.org/wiki/Tech:phab121) | 1 GB, 1 core (unknown speed), 27 GB SSD | |  |  |
| [prometheus131](https://meta.miraheze.org/wiki/Tech:prometheus131) | 1 GB, 2 cores (unknown speed), 147 GB SSD | |  |  |
| [puppet141](https://meta.miraheze.org/wiki/Tech:puppet141) | 6 GB, 3 cores (unknown speed), 31 GB SSD | |  |  |
| [swiftac111](https://meta.miraheze.org/wiki/Tech:swiftac111) | 4 GB, 4 cores (unknown speed), 130 GB SSD | |  |  |
| [swiftobject111](https://meta.miraheze.org/wiki/Tech:swiftobject111) | 4 GB, 2 cores (unknown speed), 558 GB HDD | |  |  |
| [swiftobject112](https://meta.miraheze.org/wiki/Tech:swiftobject112) | 4 GB, 2 cores (unknown speed), 558 GB HDD | |  |  |
| [swiftobject113](https://meta.miraheze.org/wiki/Tech:swiftobject113) | 4 GB, 2 cores (unknown speed), 558 GB HDD | |  |  |
| [swiftobject121](https://meta.miraheze.org/wiki/Tech:swiftobject121) | 4 GB, 2 cores (unknown speed), 498 GB HDD | |  |  |
| [swiftobject122](https://meta.miraheze.org/wiki/Tech:swiftobject122) | 4 GB, 2 cores (unknown speed), 931 GB HDD | |  |  |
| [swiftproxy111](https://meta.miraheze.org/wiki/Tech:swiftproxy111) | 4 GB, 4 cores (unknown speed), 30 GB SSD | |  |  |
| [swiftproxy131](https://meta.miraheze.org/wiki/Tech:swiftproxy131) | 4 GB, 4 cores (unknown speed), 30 GB SSD | |  |  |
| [test131](https://meta.miraheze.org/wiki/Tech:test131) | 2 GB, 2 cores (unknown speed), 30 GB SSD | |  |  |

## Categories

* [Category:Servers](https://meta.miraheze.org/wiki/Category:Servers)

----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:Server_usage)**