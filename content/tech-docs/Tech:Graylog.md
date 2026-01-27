---
title: Tech:Graylog
---

**Graylog** is a [centralized log management solution](https://www.graylog.org/) used to collect and analyze logs across WikiTide servers. The web interface is available at [https://logging.wikitide.net/](https://logging.wikitide.net/). Access is restricted to [Technology team members](/tech-docs/techvolunteers), who can authenticate using their LDAP credentials.

## Architecture 

Graylog currently runs on [graylog161.fsslc.wtnet](/tech-docs/techgraylog161). It includes the following services:

* **graylog-server** – the main log collection and processing service
* **opensearch** – handles indexing and searching of log messages
* **mongod** – stores Graylog's configuration data

```
                     +----------------------------------+                                        +------------------------------------------+
                     | test151.fsslc.wtnet             |                                        | graylog161.fsslc.wtnet                  |
                     | +------------+                   |                                        |                                          |
                     | |            |                   |                                        | +---------------+      +---------------+ |
+----------------+   | | MediaWiki  |-\                 |                                        | |               |      |               | |
|                |   | |            |  ---\             |                                    ------|graylog-server -------- opensearch    | |
| WikiTide User  |   | +------------+      --\          |             12210/tcp   ----------/    | |               |\     |               | |
|                |   |                   +------------+ |              ----------/               | +-------|-------+ \    +---------------+ |
+----------\-----+   | +-------------+   |            | |   ----------/                          |         |          |                     |
            ------\  | |             |   | syslog-ng  -----/          TLS encrypted              |          \         \                     |
                   ----|   NGINX     -----            | |                                        |  +-------|-------+  \  +---------------+ |
                     | |             |   +------------+ |                                        |  |               |   \ |               | |
                     | +-------------+    /             |                                        |  |     NGINX     |    ||    mongod     | |
                     |                   /              |                                        |  |               |     |               | |
                     | +-------------+  /               |                                        |  +------|--------+     +---------------+ |
                     | | /dev/log    | /                |                                        +---------|--------------------------------+
                     | | (kernel logs|/                 |                                                  |                                 
                     | | , etc.)     |                  |                                                  |                                 
                     | +-------------+                  |                                                  |                                 
                     |                                  |                                                  |                                 
                     +----------------------------------+                                        +---------|---------+                       
                                                                                                 |                   |                       
                                                                                                 |  Tech Team member |                       
                                                                                                 |                   |                       
                                                                                                 +-------------------+                       
```

In the above architecture, **syslog-ng** on **test151** receives logs locally and forwards them to **graylog-server**.
To enable this, set `base::syslog::syslog_daemon` to `syslog_ng` in Puppet. The [base::syslog](https://github.com/miraheze/puppet/blob/main/modules/base/manifests/syslog.pp) class will:

* Install **syslog-ng**
* Configure it to listen on **127.0.0.1:10514** for local logs
* Use the **system** source for kernel and system logs

## Streams 

Streams in Graylog define how log messages are routed and who can access them.
All messages go to the **All messages** stream by default.
Custom streams restrict access based on roles. For example, MediaWiki Specialists only see MediaWiki and NGINX streams.

## Querying the Data 

Graylog uses a [Lucene-like syntax](https://docs.graylog.org/en/4.0/pages/searching/query_language.html) for queries.
To view available fields, go to [Graylog Search](https://logging.wikitide.net/search) and click the **Fields** sidebar tab.

Examples:

* View NGINX logs for your IP:
* `nginx_remote_addr:"1.2.3.4"`
* View all SSH logs:
* `application_name:"sshd"`
* View all MediaWiki errors and warnings:
* `application_name:"mediawiki" AND (mediawiki_level:"ERROR" OR mediawiki_level:"WARNING")`
* View logs for a specific MediaWiki request (e.g. when retrieving the backtrace of a production error):
* `mediawiki_reqId:"642df1294318d7551fab367e"`

## Access 

The Graylog interface is not directly accessible without a [SOCKS5 proxy](https://meta.miraheze.org/wiki/w:SOCKS#SOCKS5), similar to [Proxmox](/tech-docs/techproxmox). To access Graylog, follow the setup instructions for SmartProxy on your browser, and then configure either OpenSSH or PuTTY to serve as the proxy.

### SmartProxy Setup 

Install SmartProxy:

* [Chrome](https://chrome.google.com/webstore/detail/smartproxy/jogcnplbkgkfdakgdenhlpcfhjioidoj)
* [Firefox](https://addons.mozilla.org/en-US/firefox/addon/smartproxy/)

Then configure:

* *Go to* **Proxy Server > Add server**
* **Name:** *WikiTide Proxy*
* **Address:** *127.0.0.1*
* **Port:** *8089*
* **Protocol:** *SOCKS5*
* **Save**

Next:

* *Go to* **Proxy Rules > Add rule**
* **Rule type:** *Search Domain and SubDomain*
* **Domain:** *logging.wikitide.net*
* **Apply Proxy:** *WikiTide Proxy*
* **Save** and click **Save** again at the bottom (make sure you click it in **both** places)

See this [video](https://imgur.com/a/yca7doi) for a quick walkthrough.

### OpenSSH 

If you're using OpenSSH, you can create a dynamic SOCKS5 proxy with:

```shell
ssh -D 8089 <server>.<dcname>.wtnet
```

Replace **<server>** with the server hostname (e.g., **test151**)
and **<dcname>** with the datacenter identifier (e.g., **fsslc**).

If using a bastion setup as described on [Tech:SSH#OpenSSH](/tech-docs/techssh#openssh), you can simply run:

```shell
ssh -D 8089 wikitidebast
```

This avoids making two SSH hops.

### PuTTY 

To configure PuTTY:

* Select a server to connect to
* Navigate to **Connection > SSH > Tunnels**
* Enter **8089** in the **Source port** field
* Choose the **Dynamic** and **Auto** radio buttons
* **Save** the session

If you plan to leave PuTTY open while idle, the session may time out.
To avoid this, see:
[How to prevent PuTTY timeout when idle](https://askubuntu.com/questions/254750/how-to-make-putty-ssh-connection-never-to-timeout-when-user-is-idle)

## Administration 

Graylog configuration is a mix of Puppet and web interface setup.
MongoDB on `graylog161.fsslc.wtnet` stores persistent configuration.

Relevant Puppet classes:

* [role::graylog](https://github.com/miraheze/puppet/blob/main/modules/role/manifests/graylog.pp) – configures the Graylog server
* [base::syslog](https://github.com/miraheze/puppet/blob/main/modules/base/manifests/syslog.pp) – configures syslog-ng forwarding on all clients

## Categories

* [Category:Services](https://meta.miraheze.org/wiki/Category:Services)

----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:Graylog)**