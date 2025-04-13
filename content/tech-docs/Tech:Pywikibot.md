---
title: Tech:Pywikibot
---

[Pywikibot](https://meta.miraheze.org/wiki/mediawikiwiki:Manual:Pywikibot) is a library and collection of scripts for MediaWiki sites, like the one you're reading this on.

Pywikibot is installed and managed on [bots171](https://meta.miraheze.org/wiki/Tech:Bots171) via [Puppet](/tech-docs/techpuppet) and is configured to use the [User:BeeBot](https://meta.miraheze.org/wiki/User:BeeBot) account. Access to it is therefore currently restricted to Infrastructure Specialists, although this can be reviewed if access to this Pywikibot install is requested by someone who does not currently have it, since it may come in handy to be able to use some of these scripts.

Its crontab and family config can be viewed and edited via the [pywikibot-config Git repository](https://meta.miraheze.org/wiki/github:miraheze/pywikibot-config).

It runs the [stable branch](https://meta.miraheze.org/wiki/github:wikimedia/pywikibot/tree/stable), with the latest commits automatically pulled in on every puppet run.

Config

## Usage

To run scripts, instead of invoking pwb.py directly, you have to use the wrapper script [pywikibot](https://meta.miraheze.org/wiki/github:miraheze/puppet/blob/main/modules/irc/templates/pywikibot/pywikibot.sh) as the pywikibot user (`sudo -u pywikibot pywikibot <script> <parameters>`). This script itself doesn't interpret any of the parameters, all parameters to it are passed as-is to pwb.py

## Custom scripts

We don't currently have any custom Pywikibot scripts installed. If the need arises to write one, please add it to a GitHub repo, have that GitHub repo be cloned to `/var/local/pwb/wikitide-scripts/` (for example) by Puppet, then change [user_script_paths](https://doc.wikimedia.org/pywikibot/stable/api_ref/pywikibot.config.html#external-script-path-settings) on [user-config.py](https://meta.miraheze.org/wiki/github:miraheze/puppet/blob/main/modules/irc/templates/pywikibot/user-config.py) so that pywikibot finds the custom script repo. Do not use `/srv/pywikibot/scripts/userscripts/`.

## Installation details

### Directories

The following directories are used for pywikibot:

* /srv/pywikibot/: Where pywikibot itself is installed.
* /var/local/pwb/: The directory pointed to by the PYWIKIBOT_DIR environment variable ([github:miraheze/puppet/blob/main/modules/irc/manifests/pywikibot.pp#L5](https://meta.miraheze.org/wiki/github:miraheze/puppet/blob/main/modules/irc/manifests/pywikibot.pp#L5)). This is set automatically by the `/usr/local/bin/pywikibot` wrapper script.
* /var/log/pwb/: Where the contents of STDOUT on scripts run in a cron are logged to. For example, the logs of the archivebot run automatically on Meta are on `/var/log/pwb/metawiki-archivebot-job-cron.log`

----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:Pywikibot)**