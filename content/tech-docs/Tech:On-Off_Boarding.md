---
title: Tech:On-Off Boarding
---

`{{ {{Tech policy}} }}`

This page groups together all documentation over on and off boarding volunteers with a level of escalated permissions (shell is the main one here right now). The page is written in the tense of on-boarding and any changes where necessary in the case of offboarding will be written below it.

For each onboarding or offboarding process, a Phorge task **[must](https://meta.miraheze.org/wiki/rfc:2119)** be created with a checklist to track the status of all actions. This is to ensure people have the proper rights during onboarding and minimal rights after offboarding.

## Shell 

This section is generic to all shell requests.

### Google Workspace 

* Add a Google Workspace account for the user.
   * *This service requires 2FA and accounts are automatically suspended if it is not enabled within 24 hours of creation.* A valid wikitide.org email must exist for access on file. Please make sure to add a backup email and list the users' manager. On off boarding, this access must be suspended. You should manually check search console for delegated access. This may need Owner rights. If a linked device is stolen, devices may be banned from the devices section of the admin portal rather than suspending an account.

### IRC 

* Elevation of rights in the following channels may be given:
   * #miraheze (IS: +ARVefiorstv, MWS: +AVeotv)
   * #miraheze-offtopic (IS: +ARVefiorstv, MWS: +AVeotv)
   * #miraheze-tech-ops (+ARVeiorstv)
      * Command: `/msg ChanServ FLAGS #miraheze-tech-ops [nick] tech`
   * #wikitide-tech-internal (+ARVeiorstv)
      * Command: `/msg ChanServ FLAGS #wikitide-tech-internal [nick] +ARVeiorstv`
      * /mode +I should also be given
         * Command: `/mode #wikitide-tech-internal +I $a:[nick]`
      * Access must be revoked on off-boarding, no exceptions (unless the user is a Board member, or has approval by the Director of Technology).
   * #miraheze-ops (+AVeotv)
      * Command: `/msg ChanServ FLAGS #miraheze-ops [nick] op`
   * #miraheze-feed (+ARSVefiorstv)
   * #miraheze-feed-login (+AORefiorstv)
* On off-boarding, +V should be taken away. Ops access can stay in non-confidential channels if the user is trustworthy.

### Discord 

* The user should be added to the appropriate roles on [Discord](https://meta.miraheze.org/wiki/Discord).
   * These roles must be removed on off-boarding.

### GitHub 

* The user should be added to the relevant team in the GitHub account (I.E. MediaWiki Specialists) which then provides sufficient access to push commits to the repositories they need to fulfil their role.
   * Access must be revoked on off-boarding, no exceptions.

### LDAP 

* An [LDAP](/tech-docs/techldap) account should be made for a new MediaWiki Specialist or Infrastructure Specialist.
   * On off-boarding, the LDAP account would not necessarily need to be deleted as long as the user doesn't have access to anything private or to execute anything. However, for extra security reasons, the password of the account should be changed to a random hash so that the account can no longer be accessed, but can still exist in the database.
* Add the user to the relevant LDAP groups (which also determine the emails they receive).

### Grafana 

* New MediaWiki Specialists or Infrastructure Specialists being on-boarded should be given adminship to Grafana.
   * Access must be revoked on off-boarding, no exceptions.

### Graylog 

* New MediaWiki Specialists or Infrastructure Specialists must receive access to Graylog. MediaWiki Specialists: grant Reader role only, you should share access to the MediaWiki related streams in Graylog. Infrastructure Specialist: grant Admin role.
   * Access must be revoked on off-boarding, no exceptions.

### Matomo 

* The user may be provided access to [Matomo](https://analytics.wikitide.net/index.php?module=UsersManager), our analytics platform. There are separate groups for MediaWiki Specialists or Infrastructure Specialists.
   * On off-boarding, this should be revoked by default, although there may be legitimate reasons to keep access.

### Monitoring 

* If the user wants monitoring alerts via email, [add them to icinga](https://meta.miraheze.org/wiki/github:miraheze/puppet/blob/master/modules/monitoring/files/users.conf) and then add them to a monitoring group.
   * On off-boarding, remove both contact and the addition to group definitions for the user.

### Status Page 

* System administrators may also be added to [https://mirahezestatus.net/](https://mirahezestatus.net/), which is done via hund.io.
   * Access should be revoked on off-boarding.

### Phorge 

* Add the user to the [acl*security](https://meta.miraheze.org/wiki/phorge:project/view/1) group, so they can function effectively in the worst-case scenario of a security issue.
   * On off-boarding, this group must be revoked. If the user thinks they have an important reason to keep access, please discuss with the Director of Technology.
* If the user wishes, and is eligible under the [access policy](https://meta.miraheze.org/wiki/Phorge#Access_Policy), grant Phorge administrator.
   * Must be revoked on off-boarding.

### Mattermost 

* The user should be invited to Mattermost and added to the channels as mentioned on [Tech:Mattermost](/tech-docs/techmattermost).
   * On off-boarding the user account should be disabled, unless they are (and are remaining) a member of the [Board of Directors](https://meta.miraheze.org/wiki/Board_of_Directors) or [Trust and Safety](https://meta.miraheze.org/wiki/Trust_and_Safety).

## Wikis 

* For MediaWiki Specialists, the global Technology team group may be useful - it is, however, not a strict requirement.
   * On off-boarding, any access to global groups or technical wikis must be revoked if it was for being a volunteer with shell or privileged access.
* Access to staffwiki can be granted to users holding shell access.
   * On off-boarding, this group must be revoked (both on-wiki and in LocalSettings.php), unless the user is also a member of the Board of Directors. In said case, please do not remove from staffwiki.

## Social Media 

### Twitter 

* If a new system administrator wishes, they may request access to the @miraheze and @MirahezeStatus Twitter accounts.
   * Access to the Twitter accounts should be revoked on off-boarding, unless the user intends to keep managing social media and is trustworthy enough. Use your judgement. `{{ {{note|TweetDeck situation:}} }}` As of writing, TweetDeck seems not to be available to volunteers in all regions due to new Twitter policies. The account for the Twitter password must only be shared with Technology team members or members of the Board of Directors who demonstrate a clear need for such access.

### Facebook 

* If a new system administrator wishes, they may request access to the @miraheze Facebook page.
   * Access to the Facebook page should be revoked on off-boarding, unless the user intends to keep managing social media and is trustworthy enough. Use your judgement.

## Infrastructure Specialists 

The above applies, this section covers things which are specific to Infrastructure Specialists only.

### OVH & FiberState 

* Basic access to the account for ticketing purposes and the 'operations back door' should be granted. This should be so any operations member can fulfil their duties on their own.
   * Access must be revoked on off-boarding, no exceptions.

### Proxmox 

* Infrastructure Specialists with Operations-level access should be given access to [Proxmox](/tech-docs/techproxmox) and ensure that they can properly login.
   * Access must be revoked on off-boarding, no exceptions.

### iDRAC 

* Infrastructure Specialists with Operations-level access should be given access to iDRAC on all the cloud servers and ensure that they can properly login.
   * Access must be revoked on off-boarding, no exceptions.

### Private Git 

* Infrastructure Specialists should be talked through how private git works and how to access and commit things to it. This is granted through root on puppet181 and no specific access is necessary besides puppet181 root.

## Categories

* [Category:Tech](https://meta.miraheze.org/wiki/Category:Tech)
* [Category:Tech policy](https://meta.miraheze.org/wiki/Category:Tech_policy)



----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:On-Off_Boarding)**