---
title: Tech:Icinga
---

Icinga is used to monitor the status of the infrastructure and service-level information. It is running on [mon181](/tech-docs/techmon181). All servers are automatically set up with checks for SSH, load, users on the server and disk space. Additional services are also monitored though such as mail, MariaDB statistics, NGINX and so on.

Icinga access is currently only available to the [Technology team](/tech-docs/techvolunteers).

## Configuration 

Icinga is configured as standard out of the box for Debian Bullseye with little changes to the configuration. Configuration is managed through puppet.

## Adding users 

Users can refer to either "Contacts" (those who get emails and alerts) or "Interface users" (those who can use the Icinga interface). Contacts are added through the configuration file [users.conf](https://github.com/miraheze/puppet/blob/master/modules/monitoring/files/users.conf). Interface users can be added by an admin in [https://monitoring.wikitide.net/user/list](https://monitoring.wikitide.net/user/list), then adding their username to the relevant permissions needed in [roles.ini](https://github.com/miraheze/puppet/blob/master/modules/icingaweb2/templates/roles.ini.erb).

## Categories

* [Category:Monitoring services](https://meta.miraheze.org/wiki/Category:Monitoring_services)



----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:Icinga)**