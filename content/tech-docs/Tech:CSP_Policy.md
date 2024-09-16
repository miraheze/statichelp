---
title: Tech:CSP Policy
---

`{{ {{Tech policy}} }}`

This policy lays out the process by which the [Technology team](/tech-docs/techvolunteers) may approve new additions to the Content Security Policy (CSP). Sites added to the CSP may have content on that domain loaded by all Miraheze wikis. CSP approvals are generally the responsibility of MediaWiki Specialists, as a function of MediaWiki security. Though, any step in the approvals process may be handled by an Infrastructure Specialist.

## Questions 

* Is the site equipped with a privacy policy?
   * Does the site attempt to comply with the GDPR? Can European Union inhabitants invoke their individual rights?
   * Does the site provide a list of personal data being collected by using the service?
   * Is the website owner known to have a bad reputation regarding privacy?
   * Can wikis use the external service, even if the visitor wants to deny any cookies or other form of tracking?
   * Will wikis stay usable, even if the visitor blocks the external resource by using an ad blocker?
   * Is there a Data Protection Officer and/or Privacy Team that can be contacted by Miraheze?
* Is the site equipped with a security policy?
   * Does the site clarify their security measures to protect collected user data? Can the site assure measures are being taken to protect code injection into the loaded external resources?
   * Is the website owner known to have a bad reputation regarding information security?
   * Is there a Chief Information Security Officer and/or Security Team that can be contacted by Miraheze?

## Principles 

* All above questions must be answered with honesty. Answers must be backed up by references, be it public or private ones. If a question cannot be answered, the answer must be explicitly answered as 'unknown'.
* The Content Security Policy rule must be scoped to allow minimal content inclusion: only mandatory (sub)domains and resource types (e.g. script-src, img-src, font-src) can be added to the Content Security Policy.
* The Technology team explores the option of resolving the problem using existing, trustworthy and contracted services, servers and service providers. This could include proxying any resource loading and data transfers through Miraheze servers or by using vetted, contracted service providers. If this is not possible due to workload, financial or technical constraints,
* The Director of Technology will be consulted for determining consensus. If consensus is reached to allow the external resource, the resource can be added to the Content Security Policy.
* In the event of an imminent threat to service stability, privacy or security, the Technology team (as the ultimately responsible party) may remove any external resource from the Content Security Policy, without announcement beforehand, and may require a new review before the resource can be readded to the Content Security Policy.
* This policy applies to all services governed by Miraheze's Privacy Policy. Two resource types are exempted from this policy and can be added by the Technology team: any resource fully controlled by the Technology team (hosted on-premise or outsourced, via contracted vendor) and any resource hosted via a domain name fully owned by Miraheze.
In the event of a dispute or situation not covered by this policy, the Director of Technology decides.

## Categories

* [Category:Tech policy](https://meta.miraheze.org/wiki/Category:Tech_policy)

----
**Source**: [https://meta.miraheze.org/wiki/Tech:CSP_Policy](https://meta.miraheze.org/wiki/Tech:CSP_Policy)