---
title: Tech:Icinga/Base Monitoring
---

This page is used to provide generic basic monitoring guidance if an alert goes off for core base monitoring. If there is any specific guidance for certain services (e.g., cloud infrastructure, cache proxies, MediaWiki) a link should be added from this page to the relevant guidance provided in the service documentation.

## APT 

If critical packages are listed for upgrade, go to the alerting server and check to see which packages require upgrading. If you can make the upgrades, feel free to. If not or if packages need further review, please open a task and assign it to the relevant service owner.

## Conntrack Table 

A critical alert with the conntrack table requires further investigation. A one or two high utilisation of the conntrack table is not something to be concerned about; however, if this regularly is full, or gets saturated, we can start to have incoming TCP packets dropped due to not being able to track the connection packets. We might need to either increase the limit, or exclude a protocol/port relationship from the conntrack table.

## Current Load 

Please review the demand on the server! If a server is constantly under high load, it might be time to review the demand being placed under the server.

Utilise services like *top to determine what might be causing the high loads and whether any services running on the service could be unfairly consuming CPU time. Disk IO might also be causing abnormally high wait times for the CPU.

## Disk Space 

Firstly, please try to clear some space if possible by clearing out cache files or log files. If you are not the service owner, feel free to create a Phorge task to make the service owner aware, so they can look further.

If additional disk space is required, please file a [server resource request](https://meta.miraheze.org/wiki/phorge:maniphest/task/edit/form/16/) and seek the relevant approval to increase disk space.

If this is not a VM on cloud infrastructure, please notify Infrastructure using a generic Phorge task, so decisions can be made regarding how to resolve the alert.

## Nftables 

Nftables is our firewall, responsible for all packet filtering on the server. If the service fails to reload, the ruleset already loaded in the kernel stays active, meaning a failed reload does not remove existing rules, it just means no further firewall changes will take effect until the service is fixed.

Check the service status and the reason for the failure first:
```bash
sudo service nftables status
sudo journalctl -u nftables -n 50
```

Most failures are a syntax error in one of the rule fragments under /etc/nftables/. The journal output will point at the specific file and line number. Before reloading again, it's worth confirming the full ruleset actually compiles:
```bash
sudo nft -c -f /etc/nftables/main.nft
```

Once the underlying fragment is fixed (usually by the next Puppet run), restart the service and confirm the ruleset loaded correctly:
```bash
sudo service nftables restart
sudo nft list ruleset
```

## Chrony 

Chrony is our NTP daemon and keeps the server's clock synchronized. The check compares chronyd's offset against thresholds of 50ms (warning) and 100ms (critical), and its stratum against 5 (warning) and 10 (critical); it also fails critical if chronyd cannot reach a working time source at all.

A time offset or stratum alert which clears itself on the next check is not a major concern, as chrony is continuously correcting small drift on its own and stratum can shift briefly as chrony reselects sources. If it fires repeatedly, or the offset keeps growing, first check that chronyd is running and can reach its configured servers:

```bash
systemctl status chronyd
chronyc tracking
chronyc sources -v
```

*Reference ID: 00000000* in *chronyc tracking* means chrony has no working source at all; check network access to the configured NTP servers and any firewall rules in front of them. A high stratum usually means the upstream sources are themselves further from a reference clock than expected; check *chronyc sources -v* to see which source chrony picked and how many hops away it is. Otherwise, a large or growing offset usually resolves itself once chrony has had time to slew the clock; if it doesn't, chrony can step the clock back in line with a manual restart of chronyd.

## PowerDNS Recursor 

PowerDNS is our server side DNS cache - this is responsible for giving us amazing quick load times for repeated DNS lookups by caching them for up to 5 minutes at a time. If this service is providing any non-OK status codes for DNS responses to wikitide.net, it is critical to debug this as a priority. The service might just require a restart – but even if a restart resolves the problems – please flag this immediately to anyone who handles DNS to investigate whether a more thorough debugging is required.

## Puppet 

If the alert has been fired because of an administrative disablement, there is no need to do anything if this is a warning only. If critical, it may be a good idea to ask the person who disabled it if they still require it to be disabled.

If there is a puppet failure, debug the failure and attempt to make a fix if possible. If you are unable to debug the issue, raise a task with Infrastructure who will assist as general service owners of Puppet.

## SSH 

If you are the service owner and can restart the SSH service – please do so, this should resolve the alert. If you cannot, or are not the service owner, contact Infrastructure who will resolve the alert.

----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:Icinga/Base_Monitoring)**