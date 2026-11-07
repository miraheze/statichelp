---
title: Tech:Noticeboard/Notice about the SocialProfile extension
---

`{{ {{Mbox|text=This page is a draft}} }}`
The [SocialProfile](https://meta.miraheze.org/wiki/mw:Extension:SocialProfile) extension adds several features to a user's profile, such as avatars, adding friends/foes, and gifting. It was a popular extension, but also generated a disproportionate amount of burden for the Technology Team due to multiple issues:
* SocialProfile only supports LTS versions of MediaWiki (1.43 right now; 1.47 once it releases), while Miraheze upgrades to every stable version (we are on MediaWiki 1.46). Issues we encounter may not be fixed by maintainers of the extension because they do not support our MediaWiki version (see for example [T443385](https://meta.miraheze.org/wiki/mediazilla:T443385#12521989)).
* SocialProfile has some heavy technical debt that is still not resolved. For example, it does not use [extension registration](https://meta.miraheze.org/wiki/mw:Manual:Extension_registration), a feature available since MediaWiki 1.25 and adopted by almost all extensions (see [T152865](https://meta.miraheze.org/wiki/mediazilla:T152865)).
* SocialProfile only receives the minimal amount of maintenance, and non-critical bugs are often left unaddressed.
* Other problems which cannot be disclosed right now.

In light of the above, the Technology Team has already restricted the extension so that no new wiki can enable it. Due to its popularity, we will not remove SocialProfile outright. However, we will no longer offer the same level of support for this extension. Wikis are encouraged to disable SocialProfile and use [UserProfileV2](https://meta.miraheze.org/wiki/mw:Extension:UserProfileV2) instead.

Wikis that stay on SocialProfile are more likely to encounter bugs and other breaking changes when using the extension and are unlikely to receive help from the technology team. If members of the community still want to continue using the extension, they can report bugs upstream to [maintainers of SocialTools](https://phabricator.wikimedia.org/tag/social-tools/) and send fixes to [gerrit](https://gerrit.wikimedia.org/r/plugins/gitiles/mediawiki/extensions/SocialProfile/).

## Discussion 

__NEWSECTIONLINK__
Please reply here. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 11:15, 6 November 2026 (UTC)

   I've been thinking about a migration script from SocialProfile to UserProfileV2 which imports avatars and descriptions of oneself. However, with our current shortage in technology team members this is unlikely to happen. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 11:17, 6 November 2026 (UTC)

----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:Noticeboard/Notice_about_the_SocialProfile_extension)**