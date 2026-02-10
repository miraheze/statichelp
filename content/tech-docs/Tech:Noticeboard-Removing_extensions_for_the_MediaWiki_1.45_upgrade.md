---
title: Tech:Noticeboard/Removing extensions for the MediaWiki 1.45 upgrade
---


<!--Doesn't work on some edge cases: <templatestyles src="Discussion spacing/styles.css"/> -->

This page details extensions that the [Technology Team](/tech-docs/techhome) is planning to remove for the [MediaWiki 1.45 upgrade](https://meta.miraheze.org/wiki/MediaWiki/1.45).

Wiki administrators and bureaucrats: please check your wiki's `Special:Version` page and `Special:ManageWiki/extensions` to see whether your wiki has any of the extensions below installed. Note that some extensions will have spaces in their names, preventing a full name search from finding the extension.

If no objection with a convincing use case is raised, the technology team will proceed to remove the extensions listed below. Please reply in the discussion section with your feedback.

## Extension:Flow

### Rationale 1

The Wikimedia Foundation is on its way to [undeploy Flow](https://meta.miraheze.org/wiki/mediazilla:T332022) (StructuredDiscussions), after which the extension will be completely unmaintained. It has already caused issues with past MediaWiki upgrades on Miraheze, so we should remove it sooner than later.

The technology team plans to use an automated script to delete all Flow discussion pages and replace them with wikitext equivalents. There are two possible paths:
* The replaced page only has a single revision and the edit history would be lost. The sequence of events can only be inferred from the timestamps on signatures.
* The replaced page has the full page history reconstructed from past Flow discussions. This option presents more technical challenges but seems to be doable (albeit harder than the previous option).
The technology team is still evaluating the feasibility of the second option. If you'd like to preserve the full edit history, please say so in the discussion section below.

### Discussion 1

Please respond here. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 22:12, 8 February 2026 (UTC)

   Please use Option Two. PRGW still stands mainly as an archive, and deleting the extension's messages ruin the archival effort. I liked the Flow extension, but I understand the reasonings behind this. [jrStudios](https://meta.miraheze.org/wiki/User:JrStudios) ([talk](https://meta.miraheze.org/wiki/User_talk:JrStudios)) 14:44, 9 February 2026 (UTC)
   I concur. Flow is definitely in need of being put out to pasture. If preserving full edit histories is going to be that difficult, I'd prefer we pick the simplest solution to fixing this problem. [GethN7](https://meta.miraheze.org/wiki/User:GethN7) ([talk](https://meta.miraheze.org/wiki/User_talk:GethN7)) 15:58, 9 February 2026 (UTC)
   Likewise, option two is preferable, but getting rid of Flow is the more important goal. If that means losing the histories, we at All The Tropes will cope.  --[Looney Toons](https://meta.miraheze.org/wiki/User:Looney_Toons) ([talk](https://meta.miraheze.org/wiki/User_talk:Looney_Toons)) 18:46, 9 February 2026 (UTC)

## Extension:ImageRating

### Rationale 2

Per [T2934](https://meta.miraheze.org/wiki/phab:T2934), [Extension:ImageRating](https://meta.miraheze.org/wiki/mw:Extension:ImageRating) has been on Miraheze since 2018. Despite its long history, no wiki seems to be using it. For example, All The Tropes originally requested the extension, but nothing shows up on [Special:ImageRating](https://allthetropes.org/wiki/Special:ImageRating?type=best). Other wikis that enabled the extension also do not seem to be using it.

ImageRating is also incompatible in 1.45. Though the incompatibility can be fixed like any other extension, continued deployment consumes time fixing and testing the extension, and that time is better spent elsewhere.

### Discussion 2

__NEWSECTIONLINK__
Please respond here. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 10:21, 8 February 2026 (UTC)
 `{{ {{Support}} }}` As proposer. Support votes don't really matter here since we are mainly looking for serious use cases for this extension. This is merely an example comment. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 12:00, 6 February 2026 (UTC)
   Also think it's worthwhile to note the actual errors: [phorge:P562](https://meta.miraheze.org/wiki/phorge:P562), error 13 (available at [Special:Permalink/516330](https://meta.miraheze.org/wiki/Special:Permalink/516330) since Phorge's task editing leaves a lot to be desired) as well as [phorge:T14459#298025](https://meta.miraheze.org/wiki/phorge:T14459#298025) which is a completely different error. [TheWWRNerdGuy](https://meta.miraheze.org/wiki/User:TheWWRNerdGuy) ([talk](https://meta.miraheze.org/wiki/User_talk:TheWWRNerdGuy)) 12:26, 6 February 2026 (UTC)
       Those errors are essentially the same issue, even if it is manifesting through two different codepaths. [Pppery](https://meta.miraheze.org/wiki/User:Pppery) ([talk](https://meta.miraheze.org/wiki/User_talk:Pppery)) 03:11, 9 February 2026 (UTC)
   Also, what about MediaSpoiler? That also gave a database error and I'm not sure it has much use. [Crystalite13](https://meta.miraheze.org/wiki/User:Crystalite13) ([talk](https://meta.miraheze.org/wiki/User_talk:Crystalite13)) 16:21, 9 February 2026 (UTC)
      I fixed that extension a while ago. We already have a spoiler template on dev, so the extension doesn't add much to that. MediaSpoiler is however pretty widely used (enabled on 1200+ wikis), so forcing users to migrate could be a painful process unless we are sure that most wikis simply enable it without using its functionality.
      We thought this is the situation with 3d because the extension was broken for months with no bug reports coming to us, but turned out there are some serious use cases. With the popularity of MediaSpoiler I would assume quite a few wikis use it extensively. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 19:10, 9 February 2026 (UTC)

## Extension:3D

### Rationale 3

The extension has been non-functional since MediaWiki 1.44. No reports of its dysfunction were received, so the extension likely has little to no usage on the farm.

Features provided by this extension can be implemented with JavaScript, such as [the 3D model viewer on Strinova Wiki](https://meta.miraheze.org/wiki/mh:strinova:3D_Models).

### Discussion 3

Please respond here. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 10:27, 8 February 2026 (UTC)

I was planning to use 3D models in my wiki, but had not yet done so. Seeing 3D being removed is somewhat disappointing. As stated above, I know that it can be re-implemented in JavaScript, but that is quite a large amount of overhead. Are there any alternative extensions for displaying 3D models that could be used instead? [User:9021007xyz](https://meta.miraheze.org/wiki/User:9021007xyz) ([User talk:9021007xyz](https://meta.miraheze.org/wiki/User_talk:9021007xyz)) 03:07, 09 February 2026 (UTC)

   If there's enough interest in the extension someone might try to fix it or write a gadget to show 3D models. The extension only supports `stl` files, so its features shouldn't be too difficult to replicate. There won't be Multimedia Viewer integration or thumbnails, but it should be able to display 3d models fine. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 04:07, 9 February 2026 (UTC)

The 3D extension is used heavily on the [Polytope Wiki](https://polytope.miraheze.org/wiki/File:Great_icosidodecahedron.stl). --[Galoomba](https://meta.miraheze.org/wiki/User:Galoomba) ([talk](https://meta.miraheze.org/wiki/User_talk:Galoomba)) 14:27, 9 February 2026 (UTC)

   If I'm seeing this correctly, only the thumbnail, which is cached from a time when the extension is still functional, is showing. Other files such as [this one](https://polytope.miraheze.org/wiki/File:(10,2)-polysphericon.stl) is stuck on a "loading thumbnail" message. Neither shows the 3d model viewer when clicked unlike [when the extension is functioning properly](https://test.wikipedia.org/wiki/File:Programmatically_created_crystal.stl).
   Since the extension has some good use cases in a fairly active wiki, I think there is reason to keep and fix it. In the future, if an extension important to your wiki seems broken, feel free to report it on [Phorge](https://meta.miraheze.org/wiki/Phorge). Even if no volunteer ends up fixing the issue immediately, it'll at least let us know that there are still wikis that use and care about the extension. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 18:56, 9 February 2026 (UTC)

It's also used a lot on the [Forsaken Wiki](https://forsaken.wiki) [Crystalite13](https://meta.miraheze.org/wiki/User:Crystalite13) ([talk](https://meta.miraheze.org/wiki/User_talk:Crystalite13)) 16:09, 9 February 2026 (UTC)

   From a cursory search, I don't see any file on the wiki whose extension is `.stl`? [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 18:59, 9 February 2026 (UTC)
   Unless I’m mistaken, I believe Forsaken Wiki uses an in house JS based solution for its 3D viewer template. The extension is also not enabled on Forsaken Wiki. ***[<span style="color:#ff00ae">PixDeVl</span>](https://meta.miraheze.org/wiki/User:PixDeVl)* ([T](https://meta.miraheze.org/wiki/User_talk:PixDeVl)&#124;[C](https://meta.miraheze.org/wiki/Special:Contribs/PixDeVl)&#124;[G](https://meta.miraheze.org/wiki/Special:CA/PixDeVl))** 20:36, 9 February 2026 (UTC)

## Extension:ProtectSite

### Rationale 4

The extension does not prevent edits from occurring on the site (known since MediaWiki 1.44). No bug report was ever received.

Removing the `edit` permission from all user groups in `Special:ManageWiki/permissions` is equivalent to this extension in terms of functionality.

### Discussion 4

Please respond here. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 10:27, 8 February 2026 (UTC)
   Removing the `edit` permission from various usergroups sounds like a simple enough solution on paper. But in reality, that may cause problems. Namely the fact that it would require extensive knowledge of how ProtectSite works to be able to remove all the necessary permissions from various usergroups whilst adding them to the usergroups one wishes to be able to continue editing. That would require a lot of patience that the casual administrator simply wouldn't have. ProtectSite has other options besides simply preventing users from editing. Such as preventing users from uploading files. It's true that a user needs to be able to edit pages to upload files. But not everyone wants to jump straight to removing the edit permission from most usergroups. Reporting the bug to the maintainers of the extension and having them fix it would be preferable. ― [<font color="#800000">C.Syde</font>](https://meta.miraheze.org/wiki/User:C.Syde65) ([<font color="#000000">talk</font>](https://meta.miraheze.org/wiki/User_talk:C.Syde65) | [<font color="#000000">contribs</font>](https://meta.miraheze.org/wiki/Special:Contribs/C.Syde65)) 03:31, 9 February 2026 (UTC)
      I agree. It's much easier to just press "Protect" and configure the settings than it is to go through the Special:UserRights and configure all of the options for the group. Plus, what if you want *some* members of that group to access certain permissions, but not *others*. [BountyHunterX](https://meta.miraheze.org/wiki/User:BountyHunterX) ([talk](https://meta.miraheze.org/wiki/User_talk:BountyHunterX)) 21:08, 9 February 2026 (UTC)
   To piggyback on C.Syde65's response, ProtectSite offers more straightforward protection in terms of immediate functionality for new and inexperienced admins. If a wiki is experiencing harassment, it's not common knowledge (for some admins) that removing the Edit permission would also not permit users to upload files - under pressure, it's easier to nuke it all from a Special page that emulates Discord permission structure/menus, which may be familiar to newer admins. (ProtectSite can also prevent the creation of new accounts - not sure if that's affected by the Edit permission, or if it indeed still works.) I would agree with reporting the bug to the extension maintainers in the hopes that it could be fixed/made comaptible with 1.45. (I also see that [Extension:ProtectEntireWiki](https://meta.miraheze.org/wiki/mw:Extension:ProtectEntireWiki) exists, with more widespread functionality, but it seems to also be incompatible with 1.45.) - [JaneBuzJane](https://meta.miraheze.org/wiki/User:JaneBuzJane) ([talk](https://meta.miraheze.org/wiki/User_talk:JaneBuzJane)) 04:24, 9 February 2026 (UTC)
   @ [C.Syde65](https://meta.miraheze.org/wiki/User:C.Syde65) and [JaneBuzJane](https://meta.miraheze.org/wiki/User:JaneBuzJane): thanks for the response! I tested the extension locally, and it seems that the extension itself is functional. I suspect that it has some incompatibility with ManageWiki: perhaps site protection gets overridden by ManageWiki's permission system.
   There are 2 ways to keep a user-friendly protection interface that I can think of:
   * Figure out why ProtectSite fails to protect anything on Miraheze's setup (likely due to ManageWiki but could be something else).
   * Add a few shortcuts to the bottom of the [Special:ManageWiki/permissions](https://meta.miraheze.org/wiki/Special:ManageWiki/permissions) page for commonly-used operations (e.g. allow only admins to edit; allow all users but not IPs to edit; etc.). This may not be as user-friendly as ProtectSite but is a lot more intuitive.
   @ [Universal Omega](https://meta.miraheze.org/wiki/User:Universal_Omega) may have some ideas about the best way to proceed. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 05:09, 9 February 2026 (UTC)
      I will investigate this further, as we should be able to make it compatible with ManageWiki, since there is interest in the extension, I believe it is worth it to maintain and figure out a way to make it work. For now, we can consider ProtectSite will not be removed with 1.45 and we will try and figure it out more. [Universal Omega](https://meta.miraheze.org/wiki/User:Universal_Omega) ([talk](https://meta.miraheze.org/wiki/User_talk:Universal_Omega)) 05:15, 9 February 2026 (UTC)
         That sounds good! Thank you @ [Universal Omega](https://meta.miraheze.org/wiki/User:Universal_Omega) and @ [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) for the investigation. I do also like the idea of some intuitive shortcuts on the permissions page as well, and if ProtectSite ends up being incompatible with ManageWiki (either now or in the future), I think that would be a good solution. - [JaneBuzJane](https://meta.miraheze.org/wiki/User:JaneBuzJane) ([talk](https://meta.miraheze.org/wiki/User_talk:JaneBuzJane)) 17:49, 9 February 2026 (UTC)
         Yes, I too would appreciate this approach. Thank you for considering and investigating. [<span style="background:linear-gradient(90deg,#283cbd,#9030b0);-webkit-background-clip:text!important;-webkit-text-fill-color:transparent;">Soukupmi</span>](https://meta.miraheze.org/wiki/User:Soukupmi) ([talk](https://meta.miraheze.org/wiki/User_talk:Soukupmi)) ([✔](https://meta.miraheze.org/wiki/Special:Contributions/Soukupmi)) 19:42, 9 February 2026 (UTC)

## Extension:QuizGame

### Rationale 5

Just like ImageRating, testing revealed multiple issues with this extension. Its functionality sees little to no usage on the entire farm and would be a burden to keep deployed.

### Discussion 5

Please respond here. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 10:27, 8 February 2026 (UTC)

   I've experimented with both [QuizGame](https://meta.miraheze.org/wiki/mw:Extension:QuizGame) and [RandomGameUnit](https://meta.miraheze.org/wiki/mw:Extension:RandomGameUnit) on my home wiki from time to time, but got nowhere with it, so I disabled it. To prevent any headaches from forming in the near future on Miraheze, I think removing these two extensions would be a good idea. — [🧺 Wicker Basket](https://meta.miraheze.org/wiki/User:WickerBasket9) • [📝 Spam me!](https://meta.miraheze.org/wiki/User_talk:WickerBasket9) • [🗄️ Garbage can](https://meta.miraheze.org/wiki/Special:Contributions/WickerBasket9) • [🌎 Home wiki](https://meta.miraheze.org/wiki/mh:mlaatrabbot:My_Life_as_a_Teenage_Rabbot_Wiki) • [📑 Log book](https://meta.miraheze.org/wiki/Special:Log/User:WickerBasket9) 📆 03:53, 9 February 2026 (UTC)

## Extension:RandomGameUnit

### Rationale 6

Its functionality depends on QuizGame and has little use without it.

### Discussion 6

Please respond here. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 10:27, 8 February 2026 (UTC)

## Extension:NumberHeadings

### Rationale 7

Per [phorge:T14866](https://meta.miraheze.org/wiki/phorge:T14866), the extension is not compatible with 1.44's heading changes; the extension is maintained by Hallo Welt! GmbH who use a modified version of MediaWiki and are unlikely to fix it upstream. The extension itself is incredibly simple and could quite easily be replaced with a CSS Gadget.

### Discussion 7

Please respond here. [TheWWRNerdGuy](https://meta.miraheze.org/wiki/User:TheWWRNerdGuy) ([talk](https://meta.miraheze.org/wiki/User_talk:TheWWRNerdGuy)) 11:15, 8 February 2026 (UTC)

   I'm a bit conflicted about this one as the extension can be useful once fixed, but perhaps the best way forward is replacing with a Gadget if we can't get upstream to patch it. There were lots of delays with CommentStreams and it might happen again with NumberHeadings. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 08:23, 9 February 2026 (UTC)

## Extension:OrphanedTalkPages

### Rationale 8

Doesn't appear to work.

### Discussion 8

Please respond here. [TheWWRNerdGuy](https://meta.miraheze.org/wiki/User:TheWWRNerdGuy) ([talk](https://meta.miraheze.org/wiki/User_talk:TheWWRNerdGuy)) 11:24, 8 February 2026 (UTC)

   This one is a bit mysterious since [Special:OrphanedTalkPages](https://meta.miraheze.org/wiki/Special:OrphanedTalkPages) shows some recent talk pages such as [Help talk:Index](https://meta.miraheze.org/wiki/Help_talk:Index). I was unable to make it work on mirabeta either. I think I did an explicit maintenance script run and somehow orphaned talk pages still won't show up. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 22:18, 8 February 2026 (UTC)
      Hello, I suppose the issue would be that the orphaned pages predate the implementation of the extension, which could be causing it not to work? Because I remember using this extension to delete some orphaned pages after deleting the respective main page. --[Ucronista](https://meta.miraheze.org/wiki/User:Ucronista) ([talk](https://meta.miraheze.org/wiki/User_talk:Ucronista)) 00:08, 9 February 2026 (UTC)
         I redid a test on exttest.mirabeta.org, but nothing shows up on the special page. I'm not exactly sure why this is the case, but since the extension seems somewhat useful on Meta I skipped this extension in the notification. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 02:42, 9 February 2026 (UTC)
          Looking at the code that can't cause it; the query is computed based on the page table rather than the extension working with its own table. [Pppery](https://meta.miraheze.org/wiki/User:Pppery) ([talk](https://meta.miraheze.org/wiki/User_talk:Pppery)) 03:13, 9 February 2026 (UTC)

----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:Noticeboard/Removing_extensions_for_the_MediaWiki_1.45_upgrade)**