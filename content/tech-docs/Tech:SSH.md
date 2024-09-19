---
title: Tech:SSH
---

SSH is used to administer servers remotely here on Miraheze.

## SSH fingerprints

SSH fingerprints of every host are available at [Tech:SSH fingerprints](/tech-docs/techssh_fingerprints).

## Architecture

Connections go first through a bastion host, then to the server you want to connect to. For bastions you can choose either [bast161](/tech-docs/techbast161) or [bast181](/tech-docs/techbast181).

## OpenSSH

Copy paste the following into your `~/.ssh/config` file, modify as appropriate.

```
Host wikitidebast
        HostName bast181.wikitide.net
        IdentityFile <path to private key here>
        ServerAliveInterval 60
        User <shell username here>

Host *.wikitide.net
        IdentityFile <path to private key here>
        User <shell username here>
        ProxyJump wikitidebast
```

`ServerAliveInterval` is there to help those stuck behind CGNAT, to prevent it from closing the connection if you stay idle too long. You can remove it if not needed.

## PuTTY

 `{{ {{hatnote|Copied from [[User:Reception123/bastion]], credits to Universal Omega}} }}`

* Open PuTTY
* Connection -> SSH -> Auth: enable "Allow agent forwarding"
* Connection -> Data: enter your shell username in "Auto-login username"
* Connection -> Proxy:
   * Proxy type: "Local"
   * Proxy hostname: "bast161.wikitide.net"
   * Port: "0"
   * Exclude Hosts/IPs: "bast161.wikitide.net,bast181.wikitide.net"
   * Do DNS name lookup at proxy end: "Auto"
   * Username: shell username
   * Password: private key password
   * Telnet command, or local proxy command: "plink %user@%proxyhost -nc %host:%port -pw %pass"
* Session -> Default Settings -> Save

**Note:**
* Your private key password is not actually visible within PuTTY, and is still required to access any other terminal session.
   * However OpenSSH is probably more secure due to this so probably that would be a better option.
* This configuration will also apply (in the most part) to some SCP clients, such as WinSCP.
   * With the exception that for "Local proxy command", you must use the full path to plink. For example, '"C:\\Program Files\\PuTTY\\plink.exe" %user@%proxyhost -nc %host:%port -pw %pass'.

----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:SSH)**