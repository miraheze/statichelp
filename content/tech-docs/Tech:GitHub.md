---
title: Tech:GitHub
---

**GitHub** is the service we use to host our open-source repositories. They can be found [here](https://github.com/miraheze).

Push access to the repositories is limited to [Technology team members](/tech-docs/techvolunteers), but any user can make a pull request. [Puppet](/tech-docs/techpuppet) runs every 30 minutes (except MediaWiki extensions or skins) and can be run manually on each server by a member of the Technology team with access. Some repositories can also be deployed with [mwdeploy](/tech-docs/techmwdeploy).

It is recommended to read the "README.md" file for a repository before contributing to it.

Some repositories may be given access to Technology team members without shell access, however, only those with shell access may be given push access to repositories that automatically deploy (puppet, mw-config, mediawiki-repos, ssl, dns, and MirahezeMagic)

## Production repositories 

### puppet 

[puppet](https://github.com/miraheze/puppet) is the repository that manages all services/servers.
* **Push Access**: [Infrastructure Specialists](/tech-docs/techorganization#infrastructure-specialist)
* **Servers**: [puppet181](/tech-docs/techpuppet181)

### mw-config 

[mw-config](https://github.com/miraheze/mw-config) (MediaWiki configuration) is the repository that manages settings for MediaWiki.
* **Push Access**: [Infrastructure Specialists](/tech-docs/techorganization#infrastructure-specialist), [MediaWiki Specialists](/tech-docs/techorganization#mediawiki-specialist)
* **Servers**: MediaWiki servers

### mediawiki-repos 

[mediawiki-repos](https://github.com/miraheze/mediawiki-repos) is the repository where we have a list of all installed extensions. Puppet uses this to clone the extension repos.
* **Push Access**: [Infrastructure Specialists](/tech-docs/techorganization#infrastructure-specialist), [MediaWiki Specialists](/tech-docs/techorganization#mediawiki-specialist)
* **Servers**: [mwtask171](/tech-docs/techmwtask171), [mwtask181](/tech-docs/techmwtask181), [test151](/tech-docs/techtest151)

### dns 

[dns](https://github.com/miraheze/dns) is the repository that manages all [DNS](/tech-docs/techdns) (Domain Name System) for Miraheze.
* **Push Access**: [Infrastructure Specialists](/tech-docs/techorganization#infrastructure-specialist)
* **Servers**: [ns1](/tech-docs/techns1), [ns2](/tech-docs/techns2)

### ssl 

[ssl](https://github.com/miraheze/ssl) is the repository that manages all [SSL certificates](/tech-docs/techssl_certificates) (Secure Sockets Layer) for Miraheze.
* **Push Access**: [Infrastructure Specialists](/tech-docs/techorganization#infrastructure-specialist), ssl-admins
* **Servers**: [puppet181](/tech-docs/techpuppet181)

## MediaWiki extensions and skins 

### CreateWiki 

[CreateWiki](https://github.com/miraheze/CreateWiki) is a MediaWiki extension to request and create wikis on Miraheze.
* **Push Access**: [Infrastructure Specialists](/tech-docs/techorganization#infrastructure-specialist), [MediaWiki Specialists](/tech-docs/techorganization#mediawiki-specialist), [Software Engineers](/tech-docs/techorganization#software-engineer), i18n [^1]
* **Servers**: MediaWiki servers [^2]

### GlobalNewFiles 

[GlobalNewFiles](https://github.com/miraheze/GlobalNewFiles) is a MediaWiki extension that provides a [special page](https://meta.miraheze.org/wiki/Special:GlobalNewFiles) to display all newly uploaded files globally.
* **Push Access**: [Infrastructure Specialists](/tech-docs/techorganization#infrastructure-specialist), [MediaWiki Specialists](/tech-docs/techorganization#mediawiki-specialist), [Software Engineers](/tech-docs/techorganization#software-engineer), i18n [^1]
* **Servers**: MediaWiki servers [^2]

### ImportDump 

[ImportDump](https://github.com/miraheze/ImportDump) is a MediaWiki extension designed to automate user import requests.
* **Push Access**: [Infrastructure Specialists](/tech-docs/techorganization#infrastructure-specialist), [MediaWiki Specialists](/tech-docs/techorganization#mediawiki-specialist), [Software Engineers](/tech-docs/techorganization#software-engineer), i18n [^1]
* **Servers**: MediaWiki servers [^2]

### IncidentReporting 

[IncidentReporting](https://github.com/miraheze/IncidentReporting) is a MediaWiki extension that provides MediaWiki-based incident reporting forms.
* **Push Access**: [Infrastructure Specialists](/tech-docs/techorganization#infrastructure-specialist), [MediaWiki Specialists](/tech-docs/techorganization#mediawiki-specialist), [Software Engineers](/tech-docs/techorganization#software-engineer), i18n [^1]
* **Servers**: MediaWiki servers [^2]

### ManageWiki 

[ManageWiki](https://github.com/miraheze/ManageWiki) is a MediaWiki extension to manage the state of the wikis on Miraheze.
* **Push Access**: [Infrastructure Specialists](/tech-docs/techorganization#infrastructure-specialist), [MediaWiki Specialists](/tech-docs/techorganization#mediawiki-specialist), [Software Engineers](/tech-docs/techorganization#software-engineer), i18n [^1]
* **Servers**: MediaWiki servers [^2]

### MatomoAnalytics 

[MatomoAnalytics](https://github.com/miraheze/MatomoAnalytics) is a MediaWiki extension for integration with Matomo for analytics.
* **Push Access**: [Infrastructure Specialists](/tech-docs/techorganization#infrastructure-specialist), [MediaWiki Specialists](/tech-docs/techorganization#mediawiki-specialist), [Software Engineers](/tech-docs/techorganization#software-engineer), i18n [^1]
* **Servers**: MediaWiki servers [^2]

### MirahezeMagic 

[MirahezeMagic](https://github.com/miraheze/MirahezeMagic) is a MediaWiki extension for Miraheze-specific i18n and hooks.
* **Push Access**: [Infrastructure Specialists](/tech-docs/techorganization#infrastructure-specialist), [MediaWiki Specialists](/tech-docs/techorganization#mediawiki-specialist), i18n [^1]
* **Servers**: MediaWiki servers [^3]

### RemovePII 

[RemovePII](https://github.com/miraheze/RemovePII) is a MediaWiki extension used by [trust and safety](https://meta.miraheze.org/wiki/Trust_and_Safety) to remove all personal identifiable information from a user.
* **Push Access**: [Infrastructure Specialists](/tech-docs/techorganization#infrastructure-specialist), [MediaWiki Specialists](/tech-docs/techorganization#mediawiki-specialist), [Software Engineers](/tech-docs/techorganization#software-engineer), i18n [^1]
* **Servers**: MediaWiki servers [^2]

### RequestSSL 

[RequestSSL](https://github.com/miraheze/RequestSSL) is a MediaWiki extension designed to facilitate user SSL requests for custom domains.
* **Push Access**: [Infrastructure Specialists](/tech-docs/techorganization#infrastructure-specialist), [MediaWiki Specialists](/tech-docs/techorganization#mediawiki-specialist), [Software Engineers](/tech-docs/techorganization#software-engineer), i18n [^1]
* **Servers**: MediaWiki servers [^2]

### RottenLinks 

[RottenLinks](https://github.com/miraheze/RottenLinks) is a MediaWiki extension for Rotten link detection.
* **Push Access**: [Infrastructure Specialists](/tech-docs/techorganization#infrastructure-specialist), [MediaWiki Specialists](/tech-docs/techorganization#mediawiki-specialist), [Software Engineers](/tech-docs/techorganization#software-engineer), i18n [^1]
* **Servers**: MediaWiki servers [^2]

### WikiDiscover 

[WikiDiscover](https://github.com/miraheze/WikiDiscover) is a MediaWiki extension to create an [on-wiki list](https://meta.miraheze.org/wiki/Special:WikiDiscover) of Miraheze wikis.
* **Push Access**: [Infrastructure Specialists](/tech-docs/techorganization#infrastructure-specialist), [MediaWiki Specialists](/tech-docs/techorganization#mediawiki-specialist), [Software Engineers](/tech-docs/techorganization#software-engineer), i18n [^1]
* **Servers**: MediaWiki servers [^2]

## References 

## Categories

* [Category:Tech](https://meta.miraheze.org/wiki/Category:Tech)

[^1]: Currently [@translatewiki](https://github.com/translatewiki) only
[^2]: Only if the extension is updated using [mwdeploy](/tech-docs/techmwdeploy).
[^3]: Extension is automatically updated by [mwdeploy](/tech-docs/techmwdeploy) whenever Puppet runs.


----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:GitHub)**