---
title: Tech:Redis
---

Redis is used for object caching as well as storing the job queue, which is run by MediaWiki. Redis is currently installed on [jobchron171](https://meta.miraheze.org/wiki/Tech:Jobchron171).

## Commands 

**AUTH**

The redis installation is protected by a password to increase security more than firewalling can do (e.g. protection from co-inhabiting services). The password is stored in the private git repo. The first command ran for anyone wanting to do anything is usually `AUTH <password>`.

**FLUSHALL**

This will flush all keys from the database storage and can be helpful for in-house debugging or resolving issues. The command should be run sparingly, like its child `FLUSHDB`.

**INFO**

INFO provides information about the running installation and run-time-specific information like databases, keys, CPU usages, replication states, memory, clients, and versions.

**KEYS**

KEYS can be used to list all keys matching a regex, or just all keys stored by doing `KEYS *`.

**MONITOR**

MONITOR listens for requests received by redis from the point the request was issued, and outputs it all into the shell view. This can be extremely helpful in debugging issues as it directly shows what is being queried, where, how, and the output over the selective query by the client (typically MediaWiki).
[Category:Services](https://meta.miraheze.org/wiki/Category:Services)

----
**Source**: [https://meta.miraheze.org/wiki/Tech:Redis](https://meta.miraheze.org/wiki/Tech:Redis)