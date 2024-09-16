---
title: Tech:Grafana
---

Grafana is used to receive metric information from servers in production such as load, memory usage, networking and more. It is an essential tool used for graphing the data, and then to evaluate outages or performance issues by narrowing the cause to either be on or off the server (as well as insight into how the server reacts under high usage).

## Central Server 

All data is collected on a central server which also serves the [web interface](https://grafana.wikitide.net/). Currently, this server is [mon181](https://meta.miraheze.org/wiki/Tech:Mon181). All servers have firewall rules opening the relevant ports that are needed, so the central server can communicate with all the clients and clients can send metric information to the central server.

## Adding New Servers 

This is done automatically on the first puppet run as Grafana configuration is handled in the base module. The central server can be replaced by adding `role::grafana` to the server in site.pp.

[Category:Monitoring services](https://meta.miraheze.org/wiki/Category:Monitoring_services)

----
**Source**: https://meta.miraheze.org/wiki/Tech:Grafana