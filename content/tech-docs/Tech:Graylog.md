---
title: Tech:Graylog
---

**Graylog** is a [log management solution](https://www.graylog.org/) for logs stored on the servers. The web interface is available at [https://logging.wikitide.net/](https://logging.wikitide.net/). Access is restricted to [Technology team department personnel](/tech-docs/techvolunteers). Said people can use their LDAP credentials for authentication.

## Architecture 

Graylog runs on [graylog161.wikitide.net](/tech-docs/techgraylog161) as of now. There are three daemons running there: `graylog-server` for the actual log management, `opensearch` for storing the logs and `mongod` for storing Graylog's configuration.

```
                                                                                                                  
                     +----------------------------------+                                        +------------------------------------------+
                     | test151.wikitide.net             |                                        | graylog161.wikitide.net                  |
                     | +------------+                   |                                        |                                          |
                     | |            |                   |                                        | +---------------+      +---------------+ |
+----------------+   | | MediaWiki  |-\                 |                                        | |               |      |               | |
|                |   | |            |  ---\             |                                    ------|graylog-server -------- opensearch    | |
| Miraheze User  |   | +------------+      --\          |             12210/tcp   ----------/    | |               |\     |               | |
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

In the example above, test151 runs syslog-ng, which is responsible for receiving the logs locally and sending them to graylog-server. By setting `base::syslog::syslog_daemon` to 'syslog_ng' in puppet, [base::syslog](https://github.com/miraheze/puppet/blob/master/modules/base/manifests/syslog.pp) will install syslog-ng and configure it to listen on `127.0.0.1:10514` (for anything on the server sending its logs to that destination, such as MediaWiki and NGINX) and ['system'](https://www.syslog-ng.com/technical-documents/doc/syslog-ng-open-source-edition/3.22/administration-guide/26) for services such as ssh and kernel logs.

## Streams 

Streams are Graylog's categories of data. By default, the `All messages` stream is the stream for every message sent to Graylog. Streams are useful to limit access for certain members. For example, MediaWiki Administrators can only access the streams for MediaWiki and NGINX logs.

## Querying the data 

Graylog has a [search syntax](https://docs.graylog.org/en/4.0/pages/searching/query_language.html) that's close to Lucene's syntax. For MediaWiki and NGINX, custom fields have been defined: go to [https://logging.wikitide.net/search](https://logging.wikitide.net/search) and click on 'Fields' on your left. Using these fields, you can query the data. For example:

* View NGINX logs for your IP address: `nginx_remote_addr:"1.2.3.4"`
* View all SSH logs: `application_name:"sshd"`
* View all MediaWiki errors and warnings: `application_name:"mediawiki" AND (mediawiki_level:"ERROR" OR mediawiki_level:"WARNING")`

## Access 

For security reasons, the Graylog interface is inaccessible without a [SOCKS5 proxy](https://meta.miraheze.org/wiki/w:SOCKS#SOCKS5), just like [Proxmox' interface](/tech-docs/techproxmox). To make the process of using tunnels as easy as possible, please install SmartProxy: [Chrome](https://chrome.google.com/webstore/detail/smartproxy/jogcnplbkgkfdakgdenhlpcfhjioidoj?hl=nl) or [Firefox](https://addons.mozilla.org/en-US/firefox/addon/smartproxy/). We'll be using port 8089 (although other ports will work too) on your desktop or laptop, which will be used for a SOCKS5 proxy over SSH. If you have access to graylog161, you can use graylog161.wikitide.net. If you don't have access to graylog161, use either of the Bastion servers (bast*.wikitide.net).

In SmartProxy, create a proxy server: Proxy Server > Add server > Name = "WikiTide Proxy", Address = "127.0.0.1", Port = "8089", Protocol = "SOCKS5" > Save. Afterwards, create a proxy rule: Proxy Rules > Add rule > Rule type = "Search Domain and SubDomain", Domain = "logging.wikitide.net", then "Apply Proxy" to "WikiTide Proxy" > Save and then click "Save" on the bottom of the page as well.

You can also see this quick [video](https://imgur.com/a/yca7doi) on what the configuration looks like for SmartProxy

### OpenSSH 

If using OpenSSH, you can use `ssh -D 8089 <server>.wikitide.net`.

If using a bastion server and your configuration is based on [Tech:SSH#OpenSSH](https://meta.miraheze.org/wiki/Tech:SSH#OpenSSH), you should use `ssh -D 8089 wikitidebast`. This avoids making two SSH connections to the bastion.

### PuTTY 

It is recommended to save this config to a session. Choose a server you would like to connect to. Go to Connection > SSH > Tunnels, enter `8089` in `Source port` and select the radio buttons `Dynamic` and `Auto`. If you are planning to use Graylog for an extended period of time, without using PuTTY for executing commands on servers (idle state), you may hit a timeout: see [this](https://askubuntu.com/questions/254750/how-to-make-putty-ssh-connection-never-to-timeout-when-user-is-idle) for a fix.

## Administration 

Configuring Graylog is a combination of Puppet usage and using the web interface for configuration (where configuration will eventually be stored in MongoDB on graylog161.wikitide.net). [role::graylog](https://github.com/miraheze/puppet/blob/master/modules/role/manifests/graylog.pp) is used for graylog161's configuration. [base::syslog](https://github.com/miraheze/puppet/blob/master/modules/base/manifests/syslog.pp) contains the configuration for every server logging to Graylog.

[Category:Services](https://meta.miraheze.org/wiki/Category:Services)

----
**Source**: [https://meta.miraheze.org/wiki/Tech:Graylog](https://meta.miraheze.org/wiki/Tech:Graylog)