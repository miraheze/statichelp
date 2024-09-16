---
title: Tech:Compromised Handling
---

`{{ {{Tech policy}} }}`

If you're on this page just to learn things, that's good. If you're on this page because something has been compromised - that's less good but let's make the matter go away quickly and securely.

## What private data is stored that can be compromised? 

We store a fair amount of private things, not so much user-facing all the time but service-level things like passwords, certificate keys, actual servers, and so on. Here is a list of things we store which if compromised, should be dealt with as a serious incident:

* Servers
* Bacula (passwords)
* Grafana (passwords)
* GlusterFS (SSL Certificates)
* Icinga2 (It contains passwords to connect to the db)
* Icingaweb2 (Includes user passwords in the db and contains passwords to connect to the db)
* IRC (mirahezebots password)
* MariaDB (account passwords and databases)
* MediaWiki (private settings, on-wiki accounts)
* PostgreSQL (account passwords, databases, private keys)
* PuppetDB (passwords for postgresql)
* Redis (password)
* Salt master (private keys)
* SSL (private keys)

If you add something to private git which is not covered above, please ensure you update this page with the necessary information. If you don't and a security incident occurs relating to what you've added, you will be liable for the outcome even if you were not the cause of the incident in the first place.

## Who to notify if something is compromised? 

In general, an email to sre `{{ {{@}} }}`miraheze.org should always be sent if any data (or suspicion of data) is compromised. Specific services will have specific additional people to contact or people who should be notified to assess the situation (the person who is most knowledgeable about the component - see list of [Site Reliability Engineering](https://meta.miraheze.org/wiki/Tech:SRE_Volunteers) team members).

We operate as an open project, therefore any security incident (no matter how small) will result in a community notification through an incident report. An incident report should always be submitted for security incidents as they're far more damaging in the long run than a 10-minute service outage, and is our way of showing progress and work towards providing a more secure platform. Reports should be drafted and approved by an Engineering Manager first as the consequences of a poor or unsatisfactorily complete report can be unpredictable.

## Handling Compromises 

### Servers 

The servers should be the most secure parts of the Miraheze operation. Firewalls exist to keep port access limited, failed SSH attempts eventually result in port bans for specific IPs, secure ciphers are used, and the root user cannot be logged into. Security updates are also run regularly - this prospect should be very unlikely but things happen.

Once someone is aware that a server has been compromised, their ability to handle the situation will be limited by their access. Site Reliability Engineering should be notified immediately. In extreme cases, if the user discovering the possible compromise has root access on the server but is not a Site Reliability Engineer, they may be able to handle parts of the plan below; however, if they're unsure, crowd control is the best method by means of either shutting the server down, disallowing port 22, or shutting down SSH - Site Reliability Engineering have back doors in, others do not.

* Ensure no one can gain access to the system after the issue has been discovered. Be it stopping the ssh server, shutting it down (or a reboot to close connections), blocking all ports etc. just ensure no one can get into the system.
* Begin to get a handle on how access may have been gained - through software? an SSH account? Compromised SSH key? If it can be tied to a certain and definitive SSH account - remove said account from all servers and check the rest for safety.
* Evaluate how the hole can be closed, if a key was compromised - ensure it is gone and force a regeneration, if a service/software allowed access - was it a security issue upstream? Were we running old software? Could it be how we're using it? Thoroughly investigate this question and follow solutions up.
* Discuss findings with others or send findings to sre `{{ {{@}} }}`miraheze.org to get more eyes on it.

The above is a basic plan to follow. Certain situations require more in-depth investigations, they can take minutes to hours to days to even weeks.

### Bacula 

Bacula passwords are used for authenticating communication between Bacula clients and directors. If the password becomes compromised, it is a possibility that a user can run their own backups using Bacula and thusly compromise data. The password should be reset in private git and puppet can then be run to update the passwords globally on the cluster. You should try to conclude how the password was compromised as it may make the solution ineffective here.

### Grafana 

Grafana passwords are used so that users can edit the dashboards. If a user forgets their password, they can have grafana reset their password by sending them an email. If their account became compromised, the hacker could make a malicious dashboard that could possibly gain additional metrics we don't want them to know about the system.

### IRC 

The IRC account (mirahezebots) is just a cloaked account for bots to share to avoid disclosing which server they're stored on. Nothing is stored on the account, and it has no access to private channels or extended privileges. The password should be reset in private git and puppet can then be run to update the passwords globally on the cluster (then bot services restarted). You should try to conclude how the password was compromised as it may make the solution ineffective here.

### MariaDB - database(s) 

MariaDB databases include wiki databases and other misc. services. If a database itself is compromised, there is not much collateral from it in the long run. The integrity of the database must be checked, investigate how access could have been gained and patch the vulnerability and monitor. If the database contained passwords, a precautionary reset of all passwords stored in the database should happen. A standard acknowledgement of the compromise should be noted and if possible, all people notified if any data of theirs could have been in the database.

### MariaDB - passwords 

The level of severity depends on which password is assumed to have been compromised. An evaluation of all databases that may have been compromised should be done after immediately resetting the password that was compromised and all below (if root). The process [for databases above](#mariadb---databases) applies mostly as a compromised password compromises databases.

The key should be updated both in puppet and manually on the server (Puppet does not automatically change SQL passwords).

### MediaWiki 

No data can be compromised by this method. The Upgrade/Secret keys should be randomly regenerated and deployed. The ReCaptcha keys aren't important, they're just a confirmation stage for Google.

### Redis 

Redis stores jobqueues and session data. Running the jobqueue and then restarting Redis (standard with the password reset) will clear up session data stored. The password should be reset in private git and puppet can then be run to update the passwords globally on the cluster. You should try to conclude how the password was compromised as it may make the solution ineffective here.

### SSL Private Keys 

All traffic should be viewed as compromised (as traffic may be decrypted though man-in-the-middle attacks and other methods) and the relevant domain(s) should be pulled if they have the certs regenerated immediately. An investigation should be launched into how the key was obtained and wiki owners/users should be notified.

### Salt (Private Keys) 

All servers should be viewed as compromised. All private keys should be regenerated. You should remove all hosts immediately (by following [Salt](https://meta.miraheze.org/wiki/Tech:Salt) (Section salt master).

## Notification of Users 

Under EU law, we're required to notify all European users in the event of a breach of their personal data within 72 hours of discovery of the breach. Since we never bother to geolocate people, assume that all users are European and do the right thing. Notification steps should depend on the extent of the breach, and what we discover in our investigation.
* If we determine that no PII has been compromised, writing up an incident report on Meta is enough.
* If we determine that a decent section of users have had their information compromised, run a sitenotice.  If it happened to be restricted to a few wikis, we can run it there, otherwise, do a global sitenotice.  Link to the incident report.
* If we can identify individual users who have had their PII compromised, go ahead and email them if they ever gave us their address.  If we have a lot of emails to write (hopefully not), prepare a mass email.  Use the bcc field as to not make things worse.
* External notification methods should be considered too, like Twitter.
[Category:Tech](https://meta.miraheze.org/wiki/Category:Tech)

----
**Source**: https://meta.miraheze.org/wiki/Tech:Compromised_Handling