---
title: Tech:Security
---

Unfortunately, most of our third-party repos don't have specific mail lists for security, and therefore the main checks will have to be done by a [Technology team member](/tech-docs/techvolunteers). However, security-announcements is subscribed to the following:
* `icinga-announce-request@lists.icinga.org`
* `announce-request@mariadb.org`
* `https://community.grafana.com/c/security-announcements/38` and ` https://community.grafana.com/c/releases/9`

## Handling a Security incident guidelines (Relationship with Trust and Safety) 

Since the creation of the Trust and Safety team in early 2021, the T&S team is primarily responsible for dealing with security threats, such as DoS/DDoS attacks or any other exploits that can be used that would cause harm to Miraheze or the [WikiTide Foundation](https://meta.miraheze.org/wiki/WikiTide_Foundation). That being said, in this area, Technology team cooperation is essential for T&S to be able to effectively operate, and in some cases the Technology team will have to take urgent measures to stop or prevent an active threat from doing damage to the farm. There are two main types of threat that will generally arise:
 `{{ {{note}} }}` This guideline only applies to threats where actions for resolution aren’t around software deploys created externally (or internally for our software).

### Active threat (Emergency) 

There is an '**active' threat** when there is evidence that there have recently been attempts (whether successful or not) from a third party to exploit a vulnerability or to attack Miraheze otherwise (DDoS/DoS, etc.).

Due to their urgent nature, active threats may be dealt with by any Technology team member without having to first consult T&S or the Director of Technology (attempts to contact T&S should always be made first, but if there is no response action may be taken). Any action done by a Technology team member should be *temporary* and after it is done the Director of Technology and the T&S team should be informed.

**Examples of active threats**: Someone posting code that can be used to exploit something, an active DDoS/DoS attack taking place.

### Passive threat 

There is a '**passive' threat** when there is evidence of an existing vulnerability, but there is no evidence of any proof of concept or actual attempt (whether successful or not) to exploit that vulnerability recently. While these are still serious security issues, they are not as urgent as active threats, given the low probability that they will be exploited immediately.

Due to their less urgent nature than active threats, Technology team members should only deal with them after the Director of Technology or a T&S member (or both) have been consulted (attempts to contact T&S should always be made first, if there is no response the Director of Technology should be contacted). Any action done by the Technology team member should be *temporary* (unless T&S agrees to a permanent solution) and after it is done the T&S team should be informed (if done on Director of Technology approval only).

**Examples of passive threats**: Someone reporting a vulnerability but no evidence that it has been exploited (or attempts have been made) or is widely known.

If in doubt about whether a threat is active or passive and the Director of Technology or any T&S member is around, use your judgment and consult members of the team who are around. Remember that T&S and the Technology team must collaborate on security issues.



----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:Security)**