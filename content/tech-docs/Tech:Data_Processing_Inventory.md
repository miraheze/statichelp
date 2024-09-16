---
title: Tech:Data Processing Inventory
---

`{{ {{outdated}} }}`

At the [Board meeting of October 23, 2020](https://meta.miraheze.org/wiki/Board/Policies/20201023-Minutes) a data processing inventory was suggested. This page is a **draft**.

## Data processors 

| Processor | Website | Jurisdiction | Data processing agreement | Purpose | Data |
| --- | --- | --- | --- | --- | --- |
| DigitalOcean, LLC | [https://www.digitalocean.com/](https://www.digitalocean.com/) | United States | [https://www.digitalocean.com/legal/data-processing-agreement/](https://www.digitalocean.com/legal/data-processing-agreement/) | Hosting infrastructure | Usernames, real names, email addresses, IP addresses, (private) wiki content, passwords, optional user information, other usage information |
| OVH | [https://www.ovh.co.uk/](https://www.ovh.co.uk/) | France | | [https://www.ovh.co.uk/support/termsofservice/Data%20Processing%20Agreement_UK.pdf](https://www.ovh.co.uk/support/termsofservice/Data%20Processing%20Agreement_UK.pdf) | Hosting infrastructure | Usernames, real names, email addresses, IP addresses, (private) wiki content, passwords, optional user information, other usage information |
| RamNode LLC | [https://ramnode.com/](https://ramnode.com/) | United States | [https://www.ramnode.com/gdpr-dpa.pdf](https://www.ramnode.com/gdpr-dpa.pdf) | Hosting infrastructure | Usernames, real names, email addresses, IP addresses, (private) wiki content, passwords, optional user information, other usage information |

## Data processing 

| Data type | Subjects | Legal basis | Retention date | Processors |
| --- | --- | --- | --- | --- |
| IP address | Editors, readers | Anonymous editors: consent<br />CheckUser (registered editor): legitimate interests | Anonymous editing: indefinite (attribution mandatory by licensing)<br />CheckUser (registered editor): up to 90 days | DigitalOcean, OVH, RamNode |
| Usernames | Registered editors | Consent (account may not be required <sub>(*reference:* Communities may require registration prior to reading and editing, but Miraheze Limited commits to information access without prior registration.)</sub>) | Indefinite (until account has been renamed or deleted by user or per GDPR request <sub>(*reference:* Due to attribution requirements by licensing, user accounts will not be erased, but accounts will be renamed to apply [pseudonymisation](https://en.wikipedia.org/wiki/Pseudonymization).)</sub>) | DigitalOcean, OVH, RamNode |
| Password | Registered users | Legitimate interests (account security) | Indefinite (until changed or removed by user or per GDPR request) | DigitalOcean, OVH, RamNode |
| Email address | Registered users | Consent (not required upon registration), legitimate interests (account security / password reset) | Indefinite (until removed or changed by user or per GDPR request) | DigitalOcean, OVH, RamNode |
| Optional user information (e.g. a user page, real name) | Editors | Consent | Indefinite (until edited or removed by user or per GDPR request) | DigitalOcean, OVH, RamNode |
| colspan="4" | *Access logs / analytics* |
| IP address | Editors, readers | Legitimate interests | Up to 90 days | DigitalOcean, OVH, RamNode |
| Timestamp of request | Editors, readers | Legitimate interests | Up to 90 days | DigitalOcean, OVH, RamNode |
| User agent | Editors, readers | Legitimate interests | Up to 90 days | DigitalOcean, OVH, RamNode |
| URL | Editors, readers | Legitimate interests | Up to 90 days | DigitalOcean, OVH, RamNode |
| Referer | Editors, readers | Legitimate interests | Up to 90 days | DigitalOcean, OVH, RamNode |

**Legenda**

* Anonymous: user without an account
* Registered: user with an account
* Editors: anonymous or registered users, editing wiki content <sub>(*reference:* All editors are readers, but not all readers are editors.)</sub>
* Readers: anonymous or registered users, reading wiki content


----
**Source**: [https://meta.miraheze.org/wiki/Tech:Data_Processing_Inventory](https://meta.miraheze.org/wiki/Tech:Data_Processing_Inventory)