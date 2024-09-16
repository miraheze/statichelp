---
title: Tech:Memcached
---

Memcached is used for object and session caching. Memcached is currently installed on [mem151](Tech:Mem151.md) and [mem161](Tech:Mem161.md).

## Commands 

**flush_all**

This will flush all keys from the database storage and can be helpful for in-house debugging or resolving issues. The command should be run sparingly, like its child `flush_all`. You can also specify how long it can take (in seconds) to run, for example `flush_all 900`.

**get**

This can be used to fetch the listed key. This does not support regex. It must be the exact key. Example: `get saldanwiki:matomo:id`.

**set**

This can be used to set a key with a value. Example `set saldanwiki:matomo:id 0 4 12`.

**delete**

This can be used to delete a key. Example `delete saldanwiki:matomo:id`.

**stats**

Used to display general stats about the memcached instance.

Note: You can get all keys via PHP there's currently no easy way to do it just with TCP.

## Running 

There are multiple ways to connect to memcached and run commands. PHP or via TCP.

To use TCP, run the following:

`telnet 127.0.0.1 11211`

Then follow [#Commands](#Commands).

You can do it via PHP by [following](https://meta.miraheze.org/wiki/github:miraheze/MirahezeMagic/blob/e4e20be/includes/MirahezeMagicHooks.php#L263) and the [docs](https://www.php.net/manual/en/class.memcached.php).

## See Also 

* [Memcached commands cheat sheet](https://lzone.de/cheat-sheet/memcached)

[Category:Services](https://meta.miraheze.org/wiki/Category:Services)

----
**Source**: [https://meta.miraheze.org/wiki/Tech:Memcached](https://meta.miraheze.org/wiki/Tech:Memcached)