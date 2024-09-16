---
title: Tech:Server lifecycle
---

This page describes the stages a Miraheze server goes through. Following this guide ensures transitions between stages are done according to existing policies, using best practices, with keeping data protection in mind and while keeping monitoring noise and potential for downtime at a minimum.

## Requesting 

Anyone from Site Reliability Engineering managing services offered by the Technical Team, such as MediaWiki Engineers and Site Reliability Engineers, can request a server. The request should be tracked in Phorge, assigned to the Director of Site Reliability Engineering. In *emergencies*, the Deputy Director of Site Engineering Reliability may approve a request without talking to the Director of Site Reliability Engineering beforehand, but the Director of Site Reliability Engineering should be made aware afterwards.

## Installing 

These steps must be performed in order. This list is not exhaustive, but applies to all servers. Certain servers, such as Proxmox hosts, may need an adjusted procedure from your side: [Tech:Proxmox#VPS](https://meta.miraheze.org/wiki/Tech:Proxmox#VPS)
* Add an entry for the server to the wikitide.net DNS zone. If possible, also setup reverse DNS for the IPs.
* Change the hostname of the server. This must be in the format <server name>.wikitide.net. If you cannot do this via the Service Provider, run the command `hostnamectl set-hostname <server name>.wikitide.net` via the console.
* Log in via the console, KVM, or whatever it is called by the Service Provider. In most case, you have received the password via mail. Never share root passwords with other people.
* Most servers are accessible via SSH by default. In that case, you may find it easier to work via PuTTY or similar. To do that, dump the fingerprint of the SSH host key. For PuTTY, `ssh-keygen -E md5 -l -f /etc/ssh/ssh_host_ed25519_key.pub` seems to be appropriate.
* When connecting, verify the fingerprint matches. If so, you can proceed with the rest of the steps.
* Add the fingerprint to [Tech:SSH fingerprints](https://meta.miraheze.org/wiki/Tech:SSH_fingerprints). Do this early, so you don't forget this.
* Configure the server via Puppet: [Adding a new puppet agent (server) to the Puppetserver](https://meta.miraheze.org/wiki/Tech:Puppet#Adding_a_new_puppet_agent_.28server.29_to_the_Puppetserver).

## Decommissioning 

Decommissioning a server means the server will be fully removed from the Miraheze infrastructure. The server must be cancelled (via OVH/RamNode control panel) or deleted from Proxmox (in the case of a VM). Its hostname may not be reused.

* Depool the server from the services it's in use for. If the server is a master, failover to a replica or secondary server.
* Set downtime in Icinga for the server and all of its services, to avoid unnecessary Icinga alerts for the server.
* Ensure [the server is removed from the Puppet CA and database](https://meta.miraheze.org/wiki/Tech:Puppet#Removing_puppet_agent_.28server.29_on_the_Puppetserver).
* Remove all references to the server from manifests/site.pp. If the hostname and/or IP address is defined in other code (Hiera variables, mw-config/Database.php, etc.), remove those references as well.
* Manually remove any traces of PII or other confidential information. On most systems, `rm -rf /root /etc/ssl/private /var/log` does most of the job. If the server was used for database hosting (e.g., MariaDB) or file hosting, please remove such information as well.
* Cancel the service via the OVH or RamNode control panel. If the server is a Proxmox VM, fully remove the server from the Proxmox inventory.

## Reimage 

Reimaging a server means the server will be kept in use, but a new OS will be installed. While this is not usual (except for Proxmox hosts), there may be use cases where decommissioning a server is not needed. The hostname may be reused, as long the server will serve the same role. If the server is converted to serve another role, the hostname may not ever be used again.

* Depool the server from the services it's in use for. If the server is a master, failover to a replica or secondary server.
* Set downtime in Icinga for the server and all of its services, to avoid unnecessary Icinga alerts for the server.
* Ensure [the server is removed from the Puppet CA and database](https://meta.miraheze.org/wiki/Tech:Puppet#Removing_puppet_agent_.28server.29_on_the_Puppetserver).
* **If the server will not serve the same role**: remove all references to the server from manifests/site.pp. If the hostname and/or IP address is defined in other code (Hiera variables, mw-config/Database.php, etc.), remove those references as well.
* Manually remove any traces of PII or other confidential information. On most systems, `rm -rf /root /etc/ssl/private /var/log` does most of the job. If the server was used for database hosting (e.g., MariaDB) or file hosting, please remove such information as well.
* Reimage the server with a fresh copy of Debian.
* **If the server will not serve the same role**: readd the server to manifests/site.pp and other files, with a new fresh hostname.
* Repool the server where necessary.

## Upgrade 

An upgrade may be necessary in cases where horizontal scaling (having three smaller servers, instead of one big one) is not possible or needed. Upgrades must follow the [requesting](#Requesting) section above. An upgrade is considered to require a reboot, but without the need for a reimage. If a reimage is needed, please follow both these steps and the steps for [reimaging](#Reimage). The guide expects you have gotten an OK from the service experts, and that they are aware of the upgrades. If a server must be depooled before an upgrade is performed, the guide expects you know how to do that.

* Depool the server from the services it's in use for. If the server is a master, failover to a replica or secondary server.
* Set downtime in Icinga for the server and all of its services, to avoid unnecessary Icinga alerts for the server.
* Perform the upgrades.
* Confirm the upgrade went well, and ensure all production services are restarted and working properly.
* Remove downtime in Icinga for the server and all of its servers, this ensures we have proper monitoring back.
* Repool the server where necessary.

[Category:Tech](https://meta.miraheze.org/wiki/Category:Tech)
[Category:Technology guidelines and guides](https://meta.miraheze.org/wiki/Category:Technology_guidelines_and_guides)

----
**Source**: [https://meta.miraheze.org/wiki/Tech:Server_lifecycle](https://meta.miraheze.org/wiki/Tech:Server_lifecycle)