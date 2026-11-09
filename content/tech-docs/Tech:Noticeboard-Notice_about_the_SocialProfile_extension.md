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
      I would appreciate this as a prominent user of the extension, though I would understand why it's not possible. Would the data for the extension still exist if I disable it? --*[<span style="font-weight: bold; background:linear-gradient(#0a689e,#1d91c0,#81d3e1,#1d91c0,#0a689e);; -webkit-background-clip:text !important; -webkit-text-fill-color:transparent; font-family:monospace">zeus</span>](https://meta.miraheze.org/wiki/User:Zeus), [f](https://meta.miraheze.org/wiki/User_talk:Zeus)• [k](https://meta.miraheze.org/wiki/Special:Contributions/Zeus)• [a](https://meta.miraheze.org/wiki/mh:meta:Special:CentralAuth/Zeus) blad* 13:24, 6 November 2026 (UTC)
         It will still exist. So the workflow would be as follows: disable SocialProfile, enable UPV2, and then migrate data from SocialProfile (no longer accessible by users but are still in the database) into UPV2. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 00:32, 7 November 2026 (UTC)
       I like this idea and would be curious on how it could be done; could profile images on swift be reused or do we need to handle moving files to a new container and changing names and such? I imagine other pieces of data would be a lot easier to transfer by yoinking data from SP's database into UPV2 (I would check the schemas now but GitLab decided to hit me with a cinder block rate limit so I can't see UPV2's source).<br /> If we don't have a task on Phorge for this idea yet, may be a good idea to make one so the idea doesn't evaporate, and for visibility for new and prospective techers to take. — ***[<span style="color:#ff00ae">PixDeVl</span>](https://meta.miraheze.org/wiki/User:PixDeVl)* ([T](https://meta.miraheze.org/wiki/User_talk:PixDeVl)&#124;[C](https://meta.miraheze.org/wiki/Special:Contribs/PixDeVl)&#124;[G](https://meta.miraheze.org/wiki/Special:CA/PixDeVl))** 05:15, 7 November 2026 (UTC)
         Forgot to link it here: [https://issue-tracker.miraheze.org/T16465](https://issue-tracker.miraheze.org/T16465). [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 08:44, 8 November 2026 (UTC)

----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:Noticeboard/Notice_about_the_SocialProfile_extension)**