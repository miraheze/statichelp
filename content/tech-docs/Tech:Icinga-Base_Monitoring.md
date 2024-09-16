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

## Ferm 

Ferm is a frontend for iptables. If this service fails, it should not mean there are no more firewall rules but no changes can be applied until it is fixed. We firstly need to check all firewall rules are present in iptables, restart the service and debug why it failed. This could be either sometimes DNS records will fail or a configuration file created might have incorrect syntax.

## NTP 

An NTP time offset which immediately corrects itself is not a major concern as long as it does not repeat consistently. If this is the case, or the deviation grows more and more, the clock should be manually reset (or automatically through NTP) to the correct time, UTC.

## PowerDNS Recursor 

PowerDNS is our server side DNS cache - this is responsible for giving us amazing quick load times for repeated DNS lookups by caching them for up to 5 minutes at a time. If this service is providing any non-OK status codes for DNS responses to wikitide.net, it is critical to debug this as a priority. The service might just require a restart – but even if a restart resolves the problems – please flag this immediately to anyone who handles DNS to investigate whether a more thorough debugging is required.

## Puppet 

If the alert has been fired because of an administrative disablement, there is no need to do anything if this is a warning only. If critical, it may be a good idea to ask the person who disabled it if they still require it to be disabled.

If there is a puppet failure, debug the failure and attempt to make a fix if possible. If you are unable to debug the issue, raise a task with Infrastructure who will assist as general service owners of Puppet.

## SSH 

If you are the service owner and can restart the SSH service – please do so, this should resolve the alert. If you cannot, or are not the service owner, contact Infrastructure who will resolve the alert.

----
**Source**: [https://meta.miraheze.org/wiki/Tech:Icinga/Base_Monitoring](https://meta.miraheze.org/wiki/Tech:Icinga/Base_Monitoring)