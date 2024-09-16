---
title: Tech:SRE Import guideline
---

Imports are a vital process as they allow users to migrate their wikis from other platforms to Miraheze, to easily use content from other wikis without having to copy/paste, and they provide easier copyright attribution.

While imports are very important to Miraheze, the import process must not be abused. Excessive requests for imports (especially those simply copying articles from Wikipedia or a single user trying to 'fork' wikis, are to be scrutinized before being authorized).

This policy is an SRE policy and due to its complexity, it is not necessary to have regular users read it before making a request. Instead, it is to be used by SRE members when determining whether an import will be approved.

## Types of import 

The key metric in all the cases below is how many *active users* there are on the Miraheze wiki and how many are expected to join; the rationale behind this policy is to prevent wikis with few users from occupying significant amounts of server space without *actually using the content* they imported, so Miraheze does not end up hosting content from other wikis.

### Type I: Migrating from another platform 

When a wiki is migrating from another platform (and all or most users are coming to Miraheze), it is usually fine to import large XML and image dumps to Miraheze with no further questions needing to be asked.
 `{{ {{note|Exception:}} }}` If the XML and image dumps requested are very large (~>10GB for XMLs, >15GB for images) some further questions should be asked (regarding active users).

### Type II: Forking from another wiki 

When a wiki is 'forking' another wiki (and most users from that wiki are not coming to Miraheze), we should enquire how many active users there are (or are expected), if the import is larger than 2GB for XMLs, and 5GB for images.

### Type III: Importing from Wikipedia or other large projects 

When importing from Wikipedia (or other encyclopedia-like wikis), we will ask how the import requested is actually necessary, especially if articles from the Main space are being imported.
 `{{ {{note|Exceptions:}} }}` Templates, JS/CSS scripts, Gadgets, etc., are to be given more leeway, as long as they are not excessive and will actually be used on the wiki.

## Questions to be asked (if necessary) 

* How many active users are there on your wiki, and how many do you expect there to be in the near future (realistically)? (All Types (for Type I only if large))
* Why is this content necessary for your wiki? Will you actually use the content after importing it, how? (Type III)

## Indicative table 

This table indicates the approximate sizes of XMLs/images to be considered for forked wikis and Wikipedia imports. This table is only indicative, and requests can be refused or approved even if they do not fit into these categories. This table **DOES NOT** apply to Type I imports.

All suggestions below can be exceeded if approved by a MWE that is satisfied a reasonable use case exists, after asking questions. The numbers are not fixed and should not be taken literally (i.e., if there's a 1.1 XML, that won't necessarily require additional questions). If the limit is not exceeded, no additional questions need to be asked and the import can be approved.

| + |
| Active users | Max XML size (suggestion) | Max images size (suggestion) | Additional comments |
| --- | --- | --- | --- |
| 1 | 500 MB | 2.5 GB | If from Wikipedia and not Templates, Gadgets, etc max 100 MB |
| 2-5 | 1 GB | 5 GB | |
| 5-15 | 5 GB | 10 GB | |
| 15-25 | 10 GB | 20 GB | |
| > 25 | 15 GB | 30 GB | |

----
**Source**: [https://meta.miraheze.org/wiki/Tech:SRE_Import_guideline](https://meta.miraheze.org/wiki/Tech:SRE_Import_guideline)