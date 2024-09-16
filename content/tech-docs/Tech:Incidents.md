---
title: Tech:Incidents
---

`{{ {{Tech policy}} }}`

All incidents that can be made public (i.e., those not involving security, privacy, or legal issues) will be made public with written reports detailing how the incident began, its social and technical factors, and how it can be prevented in future. User-facing impacts should always have a report filed, regardless of size, to record preventable actions.

## Incident Response 

### The Initial Response 

All issues should be treated equally regardless of their impact. Any outage will always be a critical one to someone – whether it is users, active volunteers, software, or system administrators.

The first person responding or acknowledging an incident has two key responsibilities:
* They are responsible for communication of the incident,
* They are responsible for diagnosing and restoring the service.

The immediate response, at any reported or suspected outage, is to diagnose the cause, the service stack, the impact on each type of user, and any fallout that may likely occur from the outage (missing data, rejected contributions etc.). However, communication needs to be given priority as well – if only one person is responding, they become the sole person responsible for the whole process. As soon as someone else acknowledges that they are present, the first responder needs to make an assessment of the situation and either hand off communication or primary diagnosis. The mains things to consider in making this decision are:
* Is the colleague more experienced with the service or a service owner? If so, hand off primary diagnosis to them!
* Is the colleague not a service owner or is a community engagement specialist? If so, hand off communication to allow you to focus more on diagnosis.

### Communication 

Once someone is assigned the role of community communicator, they are entirely responsible for responding to user queries on both platforms, and via social media/email/on-wiki as they occur. Do not interfere with the communicator or micromanage them, as this only redirects your attention from diagnosis to communicating unnecessarily.

If you are not the community communicator, focus your efforts on IRC in the #miraheze-tech-ops channel – this is the sole channel to be used for investigation – **except in the instance of a potential security issue, then use #wikitide-tech-internal!** Some tips for team communication are:
* `!log` everything – too much information is less of a problem than too little.
* Communicate everything that is relevant or is something you would like to know if you were reviewing the incident after it happened.
* Communicate as soon as possible when a state changes, this will be important for a post-mortem, especially if the community communicator is receiving changing reports that align with actions taken by the Technology team.

### Diagnosis / Investigation 

Use all tools available to you to observe the incident, these tools can include, but are not limited to:
* The wiki itself,
* User reports/Phorge,
* grafana,
* icinga,
* graylog,
* proxmox,
* Provider accounts.

The only outcome from an investigation should be that service is restored. How it is restored, is not relevant – a site that works but is brittle is better than a site that does not work at all because a long-term solution is being investigated. A long-term solution can be done with a brittle site – get the site up and running before pushing attention to experimenting with fixes.

### Post-Mortem 

Once everything is returned to its prior state of functioning, time should be taken to write an incident report. The incident report will then act as a guide, for the prevention of the incident repeating, work surrounding the incident, and a reference guide if a similar incident were to occur again.

An incident report must be filed for the following:
* A visible user-facing outage occurs of the wikis (this can be detected through monitoring alerts or user reports).
* Data loss occurs as the result of an incident or action.
* A security incident occurs, regardless of its impact.

For all other circumstances, an incident should be created if documenting it would be useful or provide learning opportunities. If in doubt, contact the Director of Technology to make the decision.

## Incident Reports 

To file a new incident report, fill out the form at [Special:IncidentReports/create](https://meta.miraheze.org/wiki/Special:IncidentReports/create).

## List of incidents 

All reports can be found at [Special:IncidentReports](https://meta.miraheze.org/wiki/Special:IncidentReports). Below are reports made before the new system implementation, and are kept for archival purposes only.
 `{{ {{Special:PrefixIndex/Tech:Incidents/|hideredirects=1}} }}`
[Category:Tech policy](https://meta.miraheze.org/wiki/Category:Tech_policy)

----
**Source**: https://meta.miraheze.org/wiki/Tech:Incidents