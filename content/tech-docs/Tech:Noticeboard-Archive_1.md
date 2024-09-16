---
title: Tech:Noticeboard/Archive 1
---

`{{ {{Archive}} }}` 
## Cloud14 issues 

We are very pleased to inform users that **we have been able to restore almost all wikis affected by the November crash of db141**. Most wikis affected by the initial crash should be online once again. A very small subset of wikis (initially 19 wikis, now only 2) were affected by varying levels of database corruption and additional intervention by our system administrators is required. You may view the original list [here](https://meta.miraheze.org/wiki/phab:P475). We are working to get these back up and running again and will contact their wiki's bureaucrats were possible to inform them if any additional steps are required from their part.

Wikis created after November 16th which are on `db141` have now been reopened. We have backups of all public wikis on db141 from the letter A-O and part of P and will reimport these backups automatically for any post-November 16 wiki. Pre-November wikis will need to opt-in to restoration as several users have expressed a desire to not restore these backups.

Please read the following FAQ for more information.

### FAQ 

#### What happened? 

On 16 November 2022, one of our cloud servers, `cloud14`, suffered disk failures which led to all services on it, including `db141`, to be brought offline. We were able to successfully restore the data on those servers and have brought most of the initially affected wikis back online. On the day that we were able to restore the data, we were conducting scheduled maintenance and requested our hosting provider reseat some disks. While we cancelled that request, the on-site personnel did not see the cancellation on time and proceeded to reseat the disks but reseated the wrong disks. Instead of reseating the disks for `cloud13` (as we requested), they reseated the disks for `cloud14` which was on and this action ultimately caused data corruption. Cloud14 hosted a new database server (also called `db141` but unrelated to the one involved in the November crash, also called `db141.1` colloquially) which was affected by the December crash.

#### What does this mean? 

While wikis initially affected by the `db141` outage in November are back online, wikis created on the 'new' `db141` (db141.1) after that were still inaccessible. All post-November crash wikis on `db141` have been recreated.

#### What wikis on db141.1 were backed up? 

All public wikis from A-O (inclusive) had a database dump done for them when the disk issue occurred in December. Some wikis in P were captured but not all. Wikis after that and private wikis did not have a database dump done for them just yet.

#### I created a wiki after the November crash, why am I affected? 

~~Due to a blunder by our hosting provider, the disks containing the 'new' `db141` were corrupted which is why your wiki is offline.~~

All wikis created after the November crash are back online. If you are experiencing any issues, please [contact us](https://meta.miraheze.org/wiki/Help_center).

#### I created a wiki after the November crash, when will my wiki return? 

Reopening of impacted wikis was completed on 03:49, 30 December 2022 (UTC)

#### My wiki was affected by the November crash and recreated by request, how can I restore the edits made on the 'recreated' version? 

If we have a backup of your wiki, we have an opportunity to merge in edits if requested. This will be done by default for all wikis created after the November outage with no action required

The newest edit on a page will prevail as the version shown. If you restored your wiki previously but had not edited a page since before the wiki went down then the page should remain the same. If you have edited the page since it went down then the newest edit will be the one shown. All other edits will appear as normal in the edit history.

#### How do I request an import for my December 18 backup? 

To request a backup, you must meet two requirements:
* You must be a Bureaucrat on the wiki for which you are filing the request
* The wiki must meet requirements for backup listed above in the section detailing which wikis were backed up.

We are providing two avenues for making this request:
* Requests can be filed by authenticated users in **[this discord thread](https://discord.com/channels/407504499280707585/1058256313055989800)**
* Requests can also be filed by making a post on the **[Community noticeboard](https://meta.miraheze.org/wiki/Community_noticeboard)**, please include the URL of the wiki for which you are requesting import of backups.

#### I don't want edits merged in! 

No action is needed on your part if your wiki existed prior to the November crash. Per overwhelming feedback, we will NOT be automatically importing for this set of wikis.

#### My wiki was affected by database corruption, what can I expect? 

System administrators are trying to do everything possible to restore these wikis. Most wikis have been fixed and will be coming back online shortly. We will notify wiki bureaucrats if anything is needed from their part.

#### I don't want my wiki restored from it's pre-November crash state, I like it better as it was prior to the December crash, what can I do? 

We can delete the restored wiki and restore any backup we have on hand. Please first file a request to reset your wiki on **[Phabricator](https://meta.miraheze.org/wiki/Phabricator)**, once this is done, follow the above instructions to request an import of the Dec 18 backup.

#### What is Miraheze doing to prevent this from happening ever again? 

We have introduced robust backups to prevent a widescale issue like this from affecting us as it did and to help us come back online faster than this time. During this incident, as some vital services such as Puppet were affected, we were unable to do much for the first 2-3 days while we restored that and other services such as Mail, Monitoring, and others. Initially, our backups were also outdated which caused an issue with restoring wikis. We have now introduced reliable backups and we are fully committed to publishing monthly public backups on archive.org that our users can download and see that they're there to provide more ease and comfort. You may see our backup schedule at [Backups](https://meta.miraheze.org/wiki/Backups).
 `{{ {{Collapse top|Older announcement archive}} }}`
The below are archived announcements relating to this.

---

* 20:00 (UTC), Monday, 26 December 2022 - We have uploaded the databases to our new database server. We are now working to get the wiki back online. Due to the holidays, this may take a bit longer than usual. Thank you for your understanding.

---

Originally posted on 19 December, 2022:

We have very important news regarding db141.

Yesterday, we were able to access and recover the data on the corrupted drives, including the drives which contained the original `db141`. We intend to begin restoring affected wikis as soon as possible and we will be releasing more information about it once we get details finalised.

Now, during our scheduled maintenance yesterday, we encountered an issue attempting to get new storage drives detected by our `cloud13` server. We asked our hosting provider to reseat the disks but we then deemed it unnecessary and cancelled the request. Unfortunately, the request was still being processed and our hosting provider mistakenly reseated `cloud14`'s drives while the server was on. Due to this, the server locked up and we had to run some file system repair tools (fsck specifically) to get it back online.

Once `cloud14` and all its virtual servers came back up, we discovered that because the new `db141` was running and writing data when that happened, the database had become corrupted. Thankfully, we ran backups for most wikis yesterday so they should be safe. This has made the task of restoring wikis affected by the original `db141` outage a bit easier. What we plan to do is restore all original `db141` wikis from the recovered disks and then, using our backups, merge new edits made on the recreated wikis back into these original wikis. We do not have an ETA for when we will do this but we are thrilled to have recovered the data.

We apologise for yet another downtime on these wikis but this incident has helped foment stronger backup procedures to prevent catastrophic disasters from occurring. We are now working to restore these wikis and we will provide more information once we have it. Thank you for your understanding.

TL;DR: We recovered the data from the broken, original db141 disks but the new db141 was corrupted due to a hosting provider error. We have backups from yesterday so we will now restore the original db141 and merge the edits from recreated wikis back into the old wikis. [Miraheze Site Reliability Engineering](https://meta.miraheze.org/wiki/User:Miraheze_Operations) 00:00, 19 December 2022 (UTC)

---

The cloud server (cloud14) which hosts one of our database, db141, experienced a disk issue. As a result, a small number of wikis hosted on db141 are unavailable. We have reinstalled the affected server on new disks and are working to recover the data from the affected disks. Earliest ETA of these wikis being back online is early next week. We deeply apologise for the inconvenience but rest assured we're working diligently to have this issue fixed ASAP.

**~~LATEST UPDATE~~ Outdated, see above.**

* 4AM (UTC), Tuesday, Nov. 29 - The affected disks have been shipped to Owen as of November 24th. We are still in the process of determining how to recover the data and if it is even feasible by our means. The previous update has been amended to reflect the fact that **we have not yet involved a professional data recovery service** as it may be prohibitively expensive to do so.

* 2AM (UTC), Monday, Nov. 21 - We have reinstalled cloud14 and have began re-provisioning servers affected by the disk issue. Mail and IRC bots are now functional. We are working on re-provisioning servers for MediaWiki which should improve loading speeds. We are in the process of sending the disks containing db141 to Owen to review the physical disks and determine how to proceed with professional data recovery and the earliest ETA we can provide for when wikis may be back online is early next week.

**FAQ**

**What happened?**

A cloud server (cloud14) hosting one of our database, db141, ran into disk issues. As a result, the database cannot be accessed and some services hosted by the cloud server have been knocked offline. We have reinstalled the affected cloud server on new disks and are working to restore affected services.

**Who is affected?**

Only wikis on db141. Affected wikis display an error saying "Wiki temporarily unavailable." Most wikis on Miraheze are fine.

**When will this be fixed?**

While cloud14 has been reinstalled, we will have to send the affected disks to professional data recovery. The earliest ETA for having wikis restored is potentially early next week.

**Is data loss involved?**

We are unsure. It may be possible that the disks are not actually faulty but rather that the RAID controller is which would mean your data is safe, or it's possible the actual disks have gone bad. If it is the latter, that would indicate we received a bad batch of SSDs from the manufacturer.

**What other services are affected?**

At this moment, the only user-facing affected server is MediaWiki due to some servers being knocked offline. We are working to provision new MediaWiki servers which should fix loading.

**What is the plan for now?**

We have reinstalled the affected cloud server on new disks. Most affected services (excluding wikis) are fully functional once again. We are going to send the affected disks to a professional data recovery service to see what can be done. While costly, we thank each one of our [donors](https://meta.miraheze.org/wiki/Donate) who has supported us along the way. If all goes well, the earliest estimate for affected wikis coming back online is early next week.

Our number one priority at this moment is restoring wikis. About 500 open public wikis are affected by this so we understand this has certainly caused an impact for many of Miraheze's users. Rest assured we have not forgotten about those wikis. Every one of our 5,500+ wikis is important so we are working very hard to restore these wiki's data and bring them back online. We are so grateful that for the patience our users have had before this unprecedented issue. We will be posting updates ***here*** so please stay tuned. If you have any questions, please join us on our [Discord](https://meta.miraheze.org/wiki/Discord). Thank you. `{{ {{Collapse bottom}} }}`

## SRE Vacancy: Software Engineer (Developer) (MediaWiki) 

Miraheze is looking for Software Engineers to join our MediaWiki Team to develop code to improve the user experience of Miraheze users, build tools that allow communities to grow, and tools that support our valuable volunteers in managing a dynamic and active global community. If you think this could be you, please do have a look at [the Vacancies page](https://meta.miraheze.org/wiki/Miraheze_Vacancies#Software_Engineer_(Developer)_(MediaWiki)) which includes further information. [Reception123](https://meta.miraheze.org/wiki/User:Reception123) [(talk)](https://meta.miraheze.org/wiki/User_talk:Reception123) ([<span style="color:#33FFE3; font-weight: bold;">C</span>](https://meta.miraheze.org/wiki/Special:Contributions/Reception123)) 07:09, 31 January 2023 (UTC)

## Cargo disabled 

Due to a severe security vulnerability with [Cargo](https://meta.miraheze.org/wiki/mw:Extension:Cargo) which has been acknowledged upstream (Wikimedia Phabricator ticket currently private), the extension has been disabled on all wikis. We deeply apologize for the inconvenience but we hope this issue is resolved soon.

While there is absolutely no indication that the security vulnerabilities discovered in Cargo were exploited on Miraheze, out of a great abundance of caution, all user sessions have been reset. This means all users were logged out and must log back in again. As a general internet safety reminder, please do not reuse passwords between services and make sure to regularly change your password to a strong, unique one. [<span style="color: skyblue; font-weight: bold;">Agent</span> <span style="color: lime; font-weight: bold;">Isai</span>](https://meta.miraheze.org/wiki/User:Agent_Isai) [<span style="color: orange; font-weight: bold;">Talk to me!</span>](https://meta.miraheze.org/wiki/User_talk:Agent_Isai) 03:52, 5 April 2023 (UTC)

We plan on isolating Cargo to its own database going forward. Wikis that opt-in to Cargo will have their own database for Cargo data separate from the wiki database. Void has done a lot of work on this ([https://github.com/miraheze/mw-config/pull/5182](https://github.com/miraheze/mw-config/pull/5182), [https://github.com/miraheze/MirahezeMagic/pull/413](https://github.com/miraheze/MirahezeMagic/pull/413), [https://github.com/miraheze/puppet/commit/241009f1d77c4935621aae016ae0757bac246b83](https://github.com/miraheze/puppet/commit/241009f1d77c4935621aae016ae0757bac246b83)), though there are still some details left to flesh out. This will be useful if similar vulnerabilities are ever discovered again on Cargo. Unfortunately, we still do not have an ETA on when Cargo will be re-enabled. [OrangeStar](https://meta.miraheze.org/wiki/User:OrangeStar) ([talk](https://meta.miraheze.org/wiki/User_talk:OrangeStar)) 11:06, 14 April 2023 (UTC)

   Cargo has been re-enabled following some steps to make it more secure in our setup. If you experience any problems with cargo, please open a bug report on [Phabricator](https://meta.miraheze.org/wiki/Phabricator). If you become aware of any security concern regarding the extension (or any of our other extensions for that matter) please email security `{{ {{at}} }}`miraheze.org with as many details as possible, or file a security task on Phabricator **using [this form](https://phabricator.miraheze.org/maniphest/task/edit/form/2/)**. -- [<span style="color:#123524">Void</span>](https://meta.miraheze.org/wiki/User:Void) [<span style="color:#353839">''Whispers''</span>](https://meta.miraheze.org/wiki/User_talk:Void) 23:16, 16 April 2023 (UTC)

## Cloud11 and Swift issues 

Due to a disk issue on cloud11 (where Swift servers are located), files are currently not displaying properly and uploads are not possible. More information will be provided when available. [Reception123](https://meta.miraheze.org/wiki/User:Reception123) [(talk)](https://meta.miraheze.org/wiki/User_talk:Reception123) ([<span style="color:#33FFE3; font-weight: bold;">C</span>](https://meta.miraheze.org/wiki/Special:Contributions/Reception123)) 13:15, 11 April 2023 (UTC)
   Adding to the above, while the servers which actually hold image files are unaffected, the server that verifies that users have the proper permissions to view files and which directs traffic is down. This means that requests for images might return errors such as "Unauthorized. You do not have permission to view this file." and such. We are working to correct the issue but have no ETA at the moment for when this will be fixed. [<span style="color: skyblue; font-weight: bold;">Agent</span> <span style="color: lime; font-weight: bold;">Isai</span>](https://meta.miraheze.org/wiki/User:Agent_Isai) [<span style="color: orange; font-weight: bold;">Talk to me!</span>](https://meta.miraheze.org/wiki/User_talk:Agent_Isai) 00:36, 12 April 2023 (UTC)
   An update to the above. We're still working on recovering the data from the affected cloud server. We have been able to successfully access some data but we must now reinstall the cloud server to continue working on recovery. We hope to do the reinstall either today or tomorrow. [<span style="color: skyblue; font-weight: bold;">Agent</span> <span style="color: lime; font-weight: bold;">Isai</span>](https://meta.miraheze.org/wiki/User:Agent_Isai) [<span style="color: orange; font-weight: bold;">Talk to me!</span>](https://meta.miraheze.org/wiki/User_talk:Agent_Isai) 17:36, 15 April 2023 (UTC)

**This is now `{{ {{Done|solved}} }}`**. SRE's infrastructure team reinstalled the faulty servers today, and images have come back online for almost all wikis. **If you are experiencing problems related to images/files still**, please create a ticket on [Phabricator](https://meta.miraheze.org/wiki/Phabricator). [OrangeStar](https://meta.miraheze.org/wiki/User:OrangeStar) ([talk](https://meta.miraheze.org/wiki/User_talk:OrangeStar)) 19:51, 16 April 2023 (UTC)

## Graph disabled 

Graph has been disabled on all wikis due to a very severe security bug which caused it to be disabled on all Wikimedia wikis earlier today. Please see [Wikimedia Phabricator task T334940](https://meta.miraheze.org/wiki/w:phab:T334940) for more information. We hope that this issue is fixed soon. [<span style="color: skyblue; font-weight: bold;">Agent</span> <span style="color: lime; font-weight: bold;">Isai</span>](https://meta.miraheze.org/wiki/User:Agent_Isai) [<span style="color: orange; font-weight: bold;">Talk to me!</span>](https://meta.miraheze.org/wiki/User_talk:Agent_Isai) 01:13, 19 April 2023 (UTC)

    Local issue is [https://phabricator.miraheze.org/T10756](https://phabricator.miraheze.org/T10756). In the meantime you can take the code between the <graph> tags and paste it into [https://vega.github.io/vega-editor/?mode=vega](https://vega.github.io/vega-editor/?mode=vega) to generate PNG or SVG replacements. [Psephomancy](https://meta.miraheze.org/wiki/User:Psephomancy) ([talk](https://meta.miraheze.org/wiki/User_talk:Psephomancy)) 20:35, 11 November 2023 (UTC)

## Swift outage 

Image uploads and deletions, and [import requests](https://meta.miraheze.org/wiki/Special:RequestImportDump) are temporarily unavailable due to our file servers running out of space. We hope to fix this soon. [<span style="color: skyblue; font-weight: bold;">Agent</span> <span style="color: lime; font-weight: bold;">Isai</span>](https://meta.miraheze.org/wiki/User:Agent_Isai) [<span style="color: orange; font-weight: bold;">Talk to me!</span>](https://meta.miraheze.org/wiki/User_talk:Agent_Isai) 02:21, 22 June 2023 (UTC)

    We have resolved the issue. File uploads, deletions, and import requests have been reenabled. Thank you for bearing with us and apologize for the inconvenience caused. [Paladox](https://meta.miraheze.org/wiki/User:Paladox) ([talk](https://meta.miraheze.org/wiki/User_talk:Paladox)) 15:11, 22 June 2023 (UTC)

## An update on the criminal investigation into recent DDoS attacks 

*Posted by [RhinosF1](https://meta.miraheze.org/wiki/User:RhinosF1) following discussions with [Void](https://meta.miraheze.org/wiki/User:Void) and local police*

I'd like to provide an update to the community on the denial of service attacks we experienced last month.

Following an investigation by Nottinghamshire Police, they have identified a person of interest in the USA and the matter has been passed to authorities there to investigate.

We'd like to thank Nottinghamshire Police for their support and those within the community who provided evidence to us or the National Fraud Intelligence Bureau.

Miraheze will not tolerate abuse of its services and those who are involved face having their access terminated or limited as well as prosecution where enough evidence exists.

We'd also like to take this opportunity to remind those in the UK that they can and should report cyber crime and fraud via [https://actionfraud.police.uk](https://actionfraud.police.uk)

Any users who wish to find out more information about the laws and consequences surrounding cyber crime can visit [https://www.nationalcrimeagency.gov.uk/cyber-choices](https://www.nationalcrimeagency.gov.uk/cyber-choices)
    ~ [RhinosF1](https://meta.miraheze.org/wiki/User:RhinosF1) - [(chat)](https://meta.miraheze.org/wiki/User_talk:_RhinosF1) [· acc](https://meta.miraheze.org/wiki/Special:CentralAuth/RhinosF1) [· c](https://meta.miraheze.org/wiki/Special:Contributions/RhinosF1) - ( `{{ {{User:RhinosF1/sigcol|1=RhinosF1}} }}`) 18:51, 11 October 2023 (UTC)

## Categories

* [Category:Archives of Technology noticeboard](https://meta.miraheze.org/wiki/Category:Archives_of_Technology_noticeboard)

----
**Source**: [https://meta.miraheze.org/wiki/Tech:Noticeboard/Archive_1](https://meta.miraheze.org/wiki/Tech:Noticeboard/Archive_1)