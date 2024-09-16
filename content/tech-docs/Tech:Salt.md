---
title: Tech:Salt
---

Miraheze uses salt-ssh to do automated things like running puppet across all hosts almost instantly.

## Salt SSH 

Salt SSH is installed on [puppet181](https://meta.miraheze.org/wiki/Tech:Puppet181).

To run a salt command, ssh into [puppet181](https://meta.miraheze.org/wiki/Tech:Puppet181) and run:

salt-ssh -E '.*' cmd.run 'puppet agent -tv'

To limit the command to certain hosts like mw* do the following:

salt-ssh -E 'mw.*' cmd.run 'puppet agent -tv'

To run it against for example cp* and mw* (including mwtask*) do:

salt-ssh -E 'cp.*|mw.*' cmd.run 'puppet agent -tv'

To depool one of mw* from cp* do the following:

salt-ssh -E "cp.*" cmd.run "sudo varnishadm backend.set_health mw151 sick"

To repool do the following:

salt-ssh -E "cp.*" cmd.run "sudo varnishadm backend.set_health mw151 auto"

To list status of backends do the following:

salt-ssh -E "cp.*" cmd.run "sudo varnishadm backend.list"

## See also 

* [Salt Documentation](https://docs.saltstack.com/en/latest/topics/execution/remote_execution.html)
* [Salt Minion Targeting Documentation](https://docs.saltstack.com/en/latest/topics/targeting/globbing.html#globbing)

[Category:Services](https://meta.miraheze.org/wiki/Category:Services)

----
**Source**: https://meta.miraheze.org/wiki/Tech:Salt