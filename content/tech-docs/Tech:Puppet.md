---
title: Tech:Puppet
---

Miraheze uses a puppet master-slave configuration for deploying and managing configuration across all of the [servers](https://meta.miraheze.org/wiki/:category:servers).

## Puppet Agents 

Puppet agents are all servers in the cluster and are able to access the puppet master in order to collect resources and manifests that have been pre-compiled on the master. Puppet agents aren't really overly special except that they have puppet installed on them and have a signed upstream cert on the master.

The manifest is run every 30 minutes on all agents (which differs from the previous masterless set up where it was every hour unless a change was made). To manually run puppet on an agent, you need to run the following as root:
puppet agent -tv

To disable puppet runs, then you need to run the following as root:
puppet agent --disable="<reason>"
To then re-enable puppet runs:
puppet agent --enable

## Puppet Master 

The puppetmaster is the central server that hosts the private git repo and the public git repo (from GitHub) and compiles the manifests for agents to run.

**Certificates**

When reinstalling a server, you need to clean all certificate information about the particular server. This can be done by running:
puppetserver ca clean --certname <node>
When installing a new server, it may be necessary to check what hostname it is using to make a new request for a certificate or maybe just to generally check if any new certificate requests exist. This can be done by running:
puppetserver ca list
When decommissioning a server, it is necessary to revoke the certificate of the server to prevent it from being used to access the contents of the puppetmaster; this should also be done in the event any server is compromised:
puppetserver ca revoke --certname <node>
When adding a server to the puppetmaster, it is necessary to sign the certificate request. The following command will verify the certificate is legitimate and then authorise it to use the puppetmaster's contents:
puppetserver ca sign --certname <node>

**master**

If in the process of debugging you are unsure what the puppermaster is telling an agent to run or is passing on to an agent, it is possible to get a full JSON output of what is being to the server by running:
puppet master --compile <node>

**node**

When reinstalling or decommissioning a host, it is necessary to tell the puppetmaster to forget everything it currently knows about the host. This can be done by running:
puppet node clean <node>
When working with facts, you can get a JSON output of all facts the puppetmaster is aware of that each node knows. This can be done by running:
puppet node find <node>

## Adding a new puppet agent (server) to the Puppetserver 

*This section is only a part of the installation process, see [Tech:Server lifecycle](/tech-docs/techserver_lifecycle) for all steps.*

Here are the steps you should follow when adding a new puppet agent (server) to the Puppetserver:

<!-- TODO: Make this a script rather than a paste -->

* Step 1: Run [https://issue-tracker.miraheze.org/P220](https://issue-tracker.miraheze.org/P220) (you will have to do it a few times as at the apt-install step, it forgets the commands to run after). If you cannot just copy-paste, use a URL to download the script:
* `wget -O puppet.sh https://phorge-static.wikitide.net/file/data/wmmm75y6r7nls47h6rtf/PHID-FILE-viitpgh7mzarscwsnszy/puppet_install_script`
* Step 2: (On the **puppetserver**) `cd /etc/puppetlabs/puppet/git && git pull`
* Step 3: (On the **agent**) execute `puppet agent -tv --server puppet181.wikitide.net --waitforcert 60 `
* Step 4: (On the **puppetserver**) Check `puppetserver ca list`, and make sure that the fingerprints match
* Step 5: (On the **puppetserver**) After you have made sure that the fingerprints match, execute:
* `puppetserver ca sign --certname [servername].wikitide.net`
* Step 6: (On the **agent**) execute `puppet agent -tv --server puppet181.wikitide.net`
    `{{ {{note}} }}` The agent will automatically detect the signed certificate and proceed from there.
* Step 7: (On the **agent**) verify that `puppet agent -tv` works without `--server puppet181.wikitide.net`.

## Removing puppet agent (server) on the Puppetserver 

*This section is only a part of the decommission and reimage processes, see [Tech:Server lifecycle](/tech-docs/techserver_lifecycle) for all steps.*

Here are the steps you should follow when removing a puppet agent (server) from the Puppetserver:

* Step 1: (On the **puppetserver**) execute `sudo puppet node deactivate <host>`
* Step 2: (On the **puppetserver**) execute `puppetserver ca clean --certname <host>`
* Step 3: (On **mon181**) execute `puppet agent -tv`

## Categories

* [Category:Services](https://meta.miraheze.org/wiki/Category:Services)
* [Category:Technology guidelines and guides](https://meta.miraheze.org/wiki/Category:Technology_guidelines_and_guides)



----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:Puppet)**