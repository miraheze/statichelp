---
title: Tech:GitHub
---

[GitHub](https://meta.miraheze.org/wiki/github:) is the service we use to host our open-source repositories. They can be found [here](https://meta.miraheze.org/wiki/github:miraheze).

Push access to the repositories is limited to [system administrators](https://meta.miraheze.org/wiki/Tech:SRE_Volunteers), but any user can make a pull request. [Puppet](/tech-docs/techpuppet.md) runs every 30 minutes (except MediaWiki extensions or skins) and can be run manually on each server by a [system administrator](https://meta.miraheze.org/wiki/Tech:SRE_Volunteers). It is recommended to read the "README.md" file for a repository before contributing to it.

## Production repositories 

### puppet 

Puppet is the repository that manages all services/servers.
* **Push Access**: [Site Reliability Engineers (Infrastructure)](https://meta.miraheze.org/wiki/Tech:Organisation#Team:_Infrastructure,_Site_Reliability_Engineering)
* **Servers**: [puppet181](https://meta.miraheze.org/wiki/Tech:puppet181)

### mw-config 

mw-config (MediaWiki configuration) is the repository that manages settings for MediaWiki.
* **Push Access**: [Site Reliability Engineers (Infrastructure)](https://meta.miraheze.org/wiki/Tech:Organisation#Team:_Infrastructure,_Site_Reliability_Engineering), [MediaWiki Engineers](https://meta.miraheze.org/wiki/Tech:Organisation#Team:_MediaWiki,_Site_Reliability_Engineering)
* **Servers**: [mw151](/tech-docs/techmw151.md), [mw152](/tech-docs/techmw152.md), [mw161](/tech-docs/techmw161.md), [mw162](/tech-docs/techmw162.md), [mw171](/tech-docs/techmw171.md), [mw172](/tech-docs/techmw172.md), [mw181](/tech-docs/techmw181.md), [mw182](/tech-docs/techmw182.md), [mwtask181](/tech-docs/techmwtask181.md), [test151](/tech-docs/techtest151.md)

### mediawiki 

mediawiki is the repository that manages the MediaWiki source code, skins, and extensions.
* **Push Access**: [Site Reliability Engineers (Infrastructure)](https://meta.miraheze.org/wiki/Tech:Organisation#Team:_Infrastructure,_Site_Reliability_Engineering), [MediaWiki Engineers](https://meta.miraheze.org/wiki/Tech:Organisation#Team:_MediaWiki,_Site_Reliability_Engineering)
* **Servers**: [mw151](/tech-docs/techmw151.md), [mw152](/tech-docs/techmw152.md), [mw161](/tech-docs/techmw161.md), [mw162](/tech-docs/techmw162.md), [mw171](/tech-docs/techmw171.md), [mw172](/tech-docs/techmw172.md), [mw181](/tech-docs/techmw181.md), [mw182](/tech-docs/techmw182.md), [mwtask181](/tech-docs/techmwtask181.md), [test151](/tech-docs/techtest151.md)

### dns 

[DNS](/tech-docs/techdns.md) (Domain Name System) is the repository that manages all DNS for Miraheze.
* **Push Access**: [Site Reliability Engineers (Infrastructure)](https://meta.miraheze.org/wiki/Tech:Organisation#Team:_Infrastructure,_Site_Reliability_Engineering)
* **Servers**: [ns1](/tech-docs/techns1.md), [ns2](/tech-docs/techns2.md)

### ssl 

[SSL](/tech-docs/techssl_certificates.md) (Secure Sockets Layer) is the repository that manages all SSL certificates for Miraheze.
* **Push Access**: [Site Reliability Engineers (Infrastructure)](https://meta.miraheze.org/wiki/Tech:Organisation#Team:_Infrastructure,_Site_Reliability_Engineering), ssl-admins
* **Servers**: [puppet181](/tech-docs/techpuppet181.md)

## MediaWiki extensions and skins 

### CreateWiki 

[CreateWiki](https://github.com/miraheze/CreateWiki) is a MediaWiki extension to request and create wikis on Miraheze.
* **Push Access**: Site Reliability Engineers (Infrastructure), MediaWiki Engineers, i18n<sub>(*reference:* Currently [@translatewiki](https://github.com/translatewiki) only)</sub>
* **Servers**: MediaWiki servers<sub>(*reference:* Only if the extension is updated using [mwdeploy](/tech-docs/techmwdeploy.md) or manually)</sub>

### ManageWiki 

[ManageWiki](https://github.com/miraheze/ManageWiki) is a MediaWiki extension to manage the state of the wikis on Miraheze.
* **Push Access**: Site Reliability Engineers (Infrastructure), MediaWiki Engineers, i18n
* **Servers**: MediaWiki servers

### WikiDiscover 

[WikiDiscover](https://github.com/miraheze/WikiDiscover) is a MediaWiki extension to create an [on-wiki list](https://meta.miraheze.org/wiki/Special:WikiDiscover) of Miraheze wikis.
* **Push Access**: Site Reliability Engineers (Infrastructure), MediaWiki Engineers, i18n
* **Servers**: MediaWiki servers

### IncidentReporting 

[IncidentReporting](https://github.com/miraheze/IncidentReporting) is a MediaWiki extension that provides MediaWiki-based incident reporting forms.
* **Push Access**: Site Reliability Engineers (Infrastructure), MediaWiki Engineers, i18n
* **Servers**: MediaWiki servers

### MatomoAnalytics 

[MatomoAnalytics](https://github.com/miraheze/MatomoAnalytics) is a MediaWiki extension for integration with Matomo for analytics.
* **Push Access**: Site Reliability Engineers (Infrastructure), MediaWiki Engineers, i18n
* **Servers**: MediaWiki servers

### RottenLinks 

[RottenLinks](https://github.com/miraheze/RottenLinks) is a MediaWiki extension for Rotten link detection.
* **Push Access**: Site Reliability Engineers (Infrastructure), MediaWiki Engineers, i18n
* **Servers**: MediaWiki servers

### GlobalNewFiles 

[GlobalNewFiles](https://github.com/miraheze/GlobalNewFiles) is a MediaWiki extension that provides a [special page](https://meta.miraheze.org/wiki/Special:GlobalNewFiles) to display all newly uploaded files globally.
* **Push Access**: Site Reliability Engineers (Infrastructure), MediaWiki Engineers, i18n
* **Servers**: MediaWiki servers

### RemovePII 

[RemovePII](https://github.com/miraheze/RemovePII) is a MediaWiki extension used by [trust and safety](https://meta.miraheze.org/wiki/Trust_and_Safety) to remove all personal identifiable information from a user.
* **Push Access**: Site Reliability Engineers (Infrastructure), MediaWiki Engineers, i18n
* **Servers**: MediaWiki servers

### ImportDump 

[ImportDump](https://github.com/miraheze/ImportDump) is a MediaWiki extension designed to automate user import requests.
* **Push Access**: Site Reliability Engineers (Infrastructure), MediaWiki Engineers, i18n
* **Servers**: MediaWiki servers

## References 

[Category:Tech](https://meta.miraheze.org/wiki/Category:Tech)

----
**Source**: [https://meta.miraheze.org/wiki/Tech:GitHub](https://meta.miraheze.org/wiki/Tech:GitHub)