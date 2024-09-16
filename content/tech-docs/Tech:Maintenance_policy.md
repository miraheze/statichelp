---
title: Tech:Maintenance policy
---

`{{ {{Outdated}} }}`

## Planning for Maintenance 

* Scheduled maintenance must be discussed with at least one Engineering Manager (EM).
   * Actions requiring EM approval should be approved by the relevant EM for the service.
   * If maintenance affects both MediaWiki and Infrastructure services, both EMs should approve on the schedule and necessary actions.
   * If the relevant EM is unavailable, another EM may approve on their behalf.
* **At least** two members of Site Reliability Engineering (SRE) with root access **must** be available during the scheduled maintenance period, unless approved by an EM.
* If necessary, work with the Community Engagement Specialist (CES) to communicate this schedule to the community.
   * CES will own communications on the following channels:
      * Social Media (Facebook/Twitter)
      * Discord
      * On-wiki (Meta, Community/SRE Noticeboards, global site notice)

## Developing a Work Plan 

* A work plan **must** be established and agreed-upon with complete clarity among all involved members of SRE ahead of a maintenance window.
   * Work plan should provide a clear schedule of which SREs will be available at which points during maintenance.
      * Unless approved by EM, **at least** two qualifying SRE members **must** be available throughout maintenance.
   * Work plan **must** define a communications venue for documenting important actions taken and current work by each member of maintenance.
      * Maintenance team members are responsible for documenting their in-progress work to avoid conflicting changes.
      * Multiple operations should **not** be attempted simultaneously during the scheduled maintenance without prior EM approval.
      * Each member involved should be focused on a specified goal and completing it within the allotted time.
   * Involved SRE members should designate one member who will be leading the maintenance as part of the work plan.
      * If multiple simultaneous operations are approved by an EM, then one Maintenance Leader for each discrete service (MediaWiki/Infrastructure) should be designated. If operations are done on the same service, then only one Maintenance Leader for that service should be designated.
      * This individual will be responsible for coordinating/ensuring proper communication on work status.
      * If external support (IE ServerChoice) is required during the maintenance:
         * Maintenance leader should sign off on the urgency of the support **before** it is raised.
         * Maintenance leader **must** ensure that all members involved understand why it is necessary to raise external support.

## Initiating Maintenance 

* Maintenance **must** be announced at least **seven** days in advance, unless it is an emergency.
* To ensure data integrity, Wiki backups **must** be started at least **three** days before the scheduled maintenance.
* All backups **must** be 100% complete **before** maintenance may proceed. These backups should be stored on servers not targeted for maintenance if possible.
* Backups **must** also have external redundancy, such as uploading to archive.org or one member of SRE having saved them locally.
* If one member becomes unexpectedly unavailable **during** maintenance and their role in it is not urgent, it is up to the discretion of the remaining involved SRE member(s) whether to continue.
* If one member becomes unavailable for the planned maintenance **before** it begins, the maintenance should be postponed and rescheduled for a minimum of **three** additional days later.
* Changes to maintenance schedule (including extensions/delays) should be communicated with an EM and CES at the earliest opportunity.

**Remember**: Communication is key. All members involved should be apprised of what other members are doing, so it can be organised and focused on the relevant goal. The SRE member leading the maintenance should organise communication, and keep other members apprised of any issues when necessary. The CES should be kept informed when necessary for them to fulfill their role and communicate relevant information to the community.

## Exceptions - Emergency Maintenance 

* Emergency maintenance **must** be approved by an EM except when immediate intervention is required for service stability.
* If immediate intervention is required, the relevant EM should be notified as soon as possible and justification for immediate action should be conveyed.
* Maintenance Leader during an emergency maintenance event should engage a CES at earliest opportunity.

## Post-Mortem 

* If maintenance went over the scheduled window, an IncidentReport must be filed by an involved member.
   * At least one EM, as well as any other involved members, should be added as reviewers and approve the IncidentReport before publishing.
* Any Post-Mortem report (PMR) or After-action review (AAR) should be posted to staffwiki with key points made throughout the maintenance, any complications that arose, and root causes for those complications.
   * The report should then be reviewed by an EM and CES.
   * The CES should then make a public announcement, publishing the relevant information on the postmortem report to the community, on Miraheze Meta.
   * Publishing a public PMR/AAR is not a requirement if everything went perfectly.

## Policy Contributors 

This policy was initially created by [Universal Omega](https://meta.miraheze.org/wiki/User:Universal_Omega) with contributions from [NotAracham](https://meta.miraheze.org/wiki/User:NotAracham), [Reception123](https://meta.miraheze.org/wiki/User:Reception123), and [Void](https://meta.miraheze.org/wiki/User:Void).

[Category:Tech](https://meta.miraheze.org/wiki/Category:Tech)

----
**Source**: [https://meta.miraheze.org/wiki/Tech:Maintenance_policy](https://meta.miraheze.org/wiki/Tech:Maintenance_policy)