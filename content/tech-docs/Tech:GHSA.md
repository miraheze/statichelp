---
title: Tech:GHSA
---

GHSA or GitHub Security Advisories is a tool used to create public advisories for Security issues, Request CVEs and create private code changes without public release.

Advisories should only be created for software we build for external parties - this includes MediaWiki extensions and shared resources such as Puppet modules. Anything internally built or internal to Miraheze only should be followed using a 'Security Disclosure' published on Phorge's blog feature and/or on Meta wiki as has been done in the past. Please see [this page](https://meta.miraheze.org/wiki//Written_Security_Disclosure_Template) for an example template to use for written security disclosures.

## How to Create a GitHub Security Advisory 

If you need to create an advisory, follow the steps below:
* Go to the repository that is relevant for the code you wish to create an advisory for.
* Select the 'Security' tab and then on the side menu, select 'Security Advisories' and then press the green button 'New Draft Security Advisory'.
* Fill out the information to the best of your knowledge currently. If unsure, leave it blank or insert 'N/K'. See an explanation of the [CVSS](#Making an Assessment Using CVSS) matrix.
* Once created, on the right-hand side there is an option to invite 'Collaborators' to see the advisory. This can include anyone who may require access to the advisory prior to publishing, such as 'Security' project members who are not in Site Reliability Engineering, the reporter, or any trusted volunteer developer who has or is working on a patch.

**If a fix is possible:**
* Click the create private fork button. This must be done by a member of that repository.
* Start creating your patch privately.
* Ask someone to review the patch.
* Ask a member of the SRE Management Team to review the advisory prior to publication. This is to ensure all lines of enquiry, and steps taken to prevent and minimise technical risk, have been taken. It is recommended to also inform [Trust and Safety](https://meta.miraheze.org/wiki/Trust_and_Safety) of the advisory prior to publication as well.
* Click 'Request CVE'.
* Publish it, you may for some repositories want to inform Wikimedia Security to add to the next supplementary announcement.
* Check the information on Mitre/NVD is correct and communicate with them.

**If a fix is not possible:**
* Ask a member of the SRE Management Team to review the advisory prior to publication. This is to ensure all lines of enquiry and steps taken to prevent and minimise technical risk have been taken. It is recommended to also inform [Trust and Safety](https://meta.miraheze.org/wiki/Trust_and_Safety) of the advisory prior to publication as well.
* Click 'Request CVE'.
* Publish it, you may for some repositories want to inform Wikimedia Security to add to the next supplementary announcement.
* Check the information on Mitre/NVD is correct and communicate with them.

## Making an Assessment Using CVSS 

**Attack Vector**

* Network – Any attack that can be carried out using a network connection. This will be the main one used by Miraheze as a web service provider and software developers, most attacks will require network access to Miraheze's server.
* Adjacent – Similar to above except there is an intermediary step required in the network access.
* Local – Any attack that can be carried out locally, such as on a user's device by opening another type of software programme. This is unlikely to be used on Miraheze except in the case of intentionally deploying code or software that has an unintended consequence on Miraheze's servers.
* Physical – Any attack that requires physical, in person, access to a device. This could be a server's hard driver or a 2FA authentication device. This is unlikely to be used for Miraheze.

**Attack Complexity**

* Low – A low complexity attack is one which can be executed easily, at will, without any difficulties and will always succeed.
* High – A high complexity attack is one which can be executed, but depends heavily on factors that can't be controlled. This can include time of day, processing running, race conditions, etc.

**Privileges Requires**

* None – No privileges are required to execute the attack. Any account, of any access level, accessing from any location, on any device can execute this attack.
* Low – Privileges are required, but these are not complex or rare. Examples would include being logged into any account or having a level of permissions widely accessible.
* High – Privileges are required and these are not easy to achieve nor common place. An example would include server access.

**User Interaction**

* None – an attack to be successful does not require another person to complete an action.
* Required – an attack to be successful requires another person to complete an action.

**Scope**

* Unchanged – An attack on a component or software is localised only to the relevant component. For example, accessing information only will always be unchanged.
* Changed – An attack on a component or software is not localised and can impact another component. For example, changing information held or bypassing another layer of authentication inadvertently.

**Confidentiality**

* None – The attack cannot possibly expose any information considered confidential to the attacker.
* Low – The attack discloses information. However, this information is not critical to the operation of the software, does not increase the risk to other components or is only partially revealed.
* High – The attack discloses critical information or discloses information that is wholly reflective of the component.

**Integrity**

* None – The attack does not allow any information to be modified.
* Low – The attack allows information to be modified, but this is a small amount of information that the attacker cannot control what is modified.
* High – The attack allows information to be modified and this is either critical information or complete control is given.

**Availability**

* None – The attack has no impact on availability of service, information, or resources.
* Low – The attack has some impact on availability, but this is degradation only.
* High – The attack has some impact on availability, but this is a critical service, or there is a total unavailability of the service.

[Category:Guides for sysadmins](https://meta.miraheze.org/wiki/Category:Guides_for_sysadmins)

----
**Source**: [https://meta.miraheze.org/wiki/Tech:GHSA](https://meta.miraheze.org/wiki/Tech:GHSA)