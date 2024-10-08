---
title: Tech:Phorge
---

Phorge is an issue tracking software running on [phorge171](/tech-docs/techphorge171).

Phorge documentation can be found [here](https://we.phorge.it/book/phorge/).

For non-technical details about the functioning of Phorge, please see [this page](https://meta.miraheze.org/wiki/Phorge).

## Upgrading 

Upgrading Phorge is a process which is mostly automated by the software itself and just requires a few manual steps from a Technology Team member.
* Stop phd daemons. (./bin/phd stop)
* git pull the stable branch for libphutil, arcanist and phorge.
* Run ./bin/storage upgrade and process through the prompts.
* Start the phd daemons. (./bin/phd start)
* Restart the php8.2-fpm service.

## Categories

* [Category:Services](https://meta.miraheze.org/wiki/Category:Services)

----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:Phorge)**