---
title: Tech:Appointment and revocation policy/2025
---

`{{ {{Notice|Draft}} }}`

This policy concerns the procedure for granting shell access. Granting shell access (aka access to a server, or multiple servers) to someone needs to be done with extreme caution. With more people having shell access to (critical) servers, the chances of suffering from human mistakes and compromised shell accounts do increase.

## Appointment 

### MediaWiki Engineering 

The MediaWiki Engineering team runs a mentoring process that all prospective volunteers are expected to follow unless there are exceptional circumstances that show prior experience with MediaWiki at a high level and familiarity with Miraheze's setup. The mentoring is also not expected for users who have previously held access assuming they left less than 2 years ago.

All access requests should be sponsored by at least one member of Technology and a mentor identified. The mentor should be an existing member of the Technology with at least three months experience as a full member of Technology. A second assessor will be appointed by the Technology team.

The mentee should regularly assess themselves with their mentor for suitability to progress from beta access, which will be granted by standard to all new volunteers first, to production access.

It is not expected that new volunteers will be deemed suitable on their first discussion and they should ask their mentor for additional tasks to complete to demonstrate suitability and competency.

The Director of Technology (or as delegated) will sign off on all requests for beta access and if they are not the second assessor, they will provide sign off on production access as well.

For beta access, the prospective volunteer should request access in the normal manner. For promotion to production, the mentor will submit the request once the double marked assessment is complete and sign off has been provided by DTech.

### Infrastructure Engineering 

There is no current mentoring scheme for Infrastructure Engineering.

Prospective volunteers should discuss their suitability, competency and what areas they desire to work in.

The Director of Technology will consider whether full or limited root access is most appropriate and discuss with the remainder of the Technology Team who may elect to appoint a buddy with experience in a similar area.
### Discussion Policy 

While not necessary, it is encouraged that all SRE take part in the discussion and comment. Once an access request has elapsed an appropriate period of time (a few days to a week), the Engineering Managers will discuss the request together and make a joint decision considering all comments received, relevant experience, and community engagement. Depending on the request, either the Engineering Manager for MediaWiki (sysadmin global group, mw-admin access level) or the Engineering Manager for Infrastructure will close the Phorge task with the decision.

## Re-appointment after inactivity 

See: [Tech:Inactivity policy](/tech-docs/techinactivity_policy)

## Removal 

In the unfortunate circumstance that a user with access falls under the standards of a system administrator, violates policies deliberately, acts inappropriately, etc. the removal procedure may be initiated. It is to be noted that removal is the last resort, and that before considering removal, attempts to rectify the situation by communicating with the user in question should be made.

If a member of the SRE team believes that one of their colleagues falls under the aforementioned, they may contact their Engineering Manager and explain their situation and their thoughts on the matter. If the Engineering Manager in question declines to act or does not take appropriate measures, the SRE member may [complain to the Board](https://meta.miraheze.org/wiki/:File:Miraheze-Complaints-Procedure.pdf). Board complaints often can be resolved by mediation and informal discussions, so SRE members are encouraged to make use of this procedure if they are dissatisfied with the Engineering Manager's response, if they feel it would be more appropriate to contact the Board in the first place, or if the complaint concerns an Engineering Manager.

The Engineering Manager for the relevant team may propose that a system administrator is removed to the SRE Management Team, either after having received a report from a team member or of their own accord. Both Engineering Managers will weigh the arguments and may consult the whole Site Reliability Engineering team on whether they believe the user in question should be removed.

### For Inactivity 

See: [Tech:Inactivity policy](/tech-docs/techinactivity_policy)

## Suspension 

In exceptional circumstances, where waiting for the removal process to take place is impractical or not possible, a user may be temporarily suspended and have all their access removed by one of the Engineering Managers. This would be followed by the regular removal procedure, and access would be added back if it is ultimately decided against removal.

In ultimate emergencies, such as compromised accounts, any member with the relevant permissions may temporarily remove another sysadmin from the compromised account in question.

## How to Request Access 

### New Access 

This applies to people, who do not have shell access yet. After you have articulated a valid reason for requesting shell access, and followed the instructions below, your request will be dealt with as [described above](#appointment).
* Ensure you have an account on [GitHub](https://meta.miraheze.org/wiki/github:) and [Phorge](https://meta.miraheze.org/wiki/phorge:) (which requires a Miraheze account).
* Login into Phorge, and [fill in this form](https://meta.miraheze.org/wiki/phorge:maniphest/task/edit/form/17/) (do not forget to replace "[USERNAME]" with your username!). The form should contain the following information:
   * Miraheze Username
   * GitHub Username
   * Preferred shell username
   * A freshly generated 4096 bit RSA or ed25519 keypair, protected with a secure password.
      * Obviously you should only give us the public key, keep the private key <ins>private</ins>.
      * This key should not be used for non-Miraheze servers!
      * If using a FIDO2 key, see [Tech:FIDO2 SSH](/tech-docs/techfido2_ssh).
   * Description of the access you need. If you require sudo rights, please do not forget to include that as well.
   * The reason you need shell access.
   * A verification that your Miraheze, GitHub and Phorge accounts are owned by you. This can be accomplished by a) pasting the public key of your keypair on your **Miraheze Meta** user page (or another page in your user namespace) and b) creating a GitHub repository with a file containing the public key (or committing your public key to an already existing repository).

### Expanding Current Access 

If you already have a shell account and want to get extra privileges (or are requesting access to more servers) after this process has been completed, then you need to:
* Login to [Phorge](https://meta.miraheze.org/wiki/phorge:) and make a new request by using [this form](https://meta.miraheze.org/wiki/phorge:maniphest/task/edit/form/17/), including in the request:
   * Why you need extra access, and what benefit this would provide to either Miraheze or yourself (regarding productivity);
   * What access you specifically need (log viewing, service interaction, ability to deploy changes).

## Categories

* [Category:Tech](https://meta.miraheze.org/wiki/Category:Tech)

----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:Appointment_and_revocation_policy/2025)**