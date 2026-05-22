---
title: Tech:Noticeboard/Request for feedback: changes to default MediaWiki settings
---

__NEWSECTIONLINK__I am proposing several changes to Miraheze's default MediaWiki configuration. This page will gather community feedback for the Technology Team's consideration. Proposals that are well-received by both the community and the Tech Team will be actioned.

[PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 07:15, 21 April 2026 (UTC)
   We also got a proposal headed by [KockaAdmiralac](https://meta.miraheze.org/wiki/User:KockaAdmiralac) which is great: all of the other proposals in the list are ones I find agreeable, while 16 is something that I won't include normally. Next time we do an RfF, we should encourage members of the community to add their own proposals at the end so that we don't just enact changes that I like. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 23:12, 23 April 2026 (UTC)
   I have closed 7 out of the 16 proposals because they either have near-unanimous support or lots of oppose. The rest can wait for a bit longer for more opinions. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 23:08, 6 May 2026 (UTC)

## Proposal 1: add Gadgets to default extensions 

```
{{ {{Discussion
|comment=Closing as {{done|successful}} per near-unanimous support. [[User:PetraMagna|PetraMagna]] ([[User talk:PetraMagna|talk]]) 22:51, 6 May 2026 (UTC)
|1=
'''[[mw:Extension:Gadgets|Gadgets]]''' makes managing CSS and JavaScript tooling a lot easier. It is widely used on other hosts and doesn't add extraneous buttons for wikis that don't use it.

=== Discussion 1 ===
Please discuss below. [[User:PetraMagna|PetraMagna]] ([[User talk:PetraMagna|talk]]) 05:07, 23 April 2026 (UTC)

:{{support}} As proposer. Not much is said about this extension because it is generally considered very useful. [[User:PetraMagna|PetraMagna]] ([[User talk:PetraMagna|talk]]) 05:11, 23 April 2026 (UTC)
:{{support}} [[User:KockaAdmiralac|KockaAdmiralac]] ([[User talk:KockaAdmiralac|talk]]) 17:09, 23 April 2026 (UTC)
:{{support}} per above....[[User:Crystalite13|'''💎Crystalite13💎''']] 17:10, 23 April 2026 (UTC)
:{{support}} per above. - [[User:JaneBuzJane|JaneBuzJane]] ([[User talk:JaneBuzJane|talk]]) 19:12, 23 April 2026 (UTC)
:{{support}} per above. [[User:TheWWRNerdGuy|TheWWRNerdGuy]] ([[User talk:TheWWRNerdGuy|talk]]) 19:51, 23 April 2026 (UTC)
:{{support}} as gadgets are an incredibly, incredibly useful feature and this reduces the friction necessary for a new wiki to install their first gadgets. — <span style="font-variant: small-caps">[[User:Chrs|chrs]] ([[User talk:Chrs|talk]])</span> 23:21, 23 April 2026 (UTC)
:{{support}} per above [[User:SomeRandomDeveloper|SomeRandomDeveloper]] ([[User talk:SomeRandomDeveloper|talk]]) 12:32, 24 April 2026 (UTC)
:{{support|strongest}} Honestly, this will make things a lot easier, rather than making things more complicated, so.... --[[User:DarkMatterMan4500|DarkMatterMan4500]] ([[User talk:DarkMatterMan4500|talk]]) ([[Special:Contributions/DarkMatterMan4500|contribs]]) 15:29, 24 April 2026 (UTC)
:{{support}} per above. ~ [[User:Elisapoly|Elisapoly]] ([[User talk:Elisapoly|talk]]) 18:37, 24 April 2026 (UTC)
:{{Abstain}} (( I kind of keep away from extensions ... Also I have not used Gadgets before ... )) --- [[User:Imamy|Imamy]] ([[User talk:Imamy|talk]]) 23:56, 24 April 2026 (UTC)
:{{Question}} (( Can Gadgets be enabled by the Bureaucrat? ... ... ... or must this extension be enabled by Phorge? ... )) --- [[User:Imamy|Imamy]] ([[User talk:Imamy|talk]]) 23:56, 24 April 2026 (UTC)
::They are available in ManageWiki to enable. [[User:KockaAdmiralac|KockaAdmiralac]] ([[User talk:KockaAdmiralac|talk]]) 23:58, 24 April 2026 (UTC)
:::Thank you for answering ...  That saved me a lot of research time ... --- [[User:Imamy|Imamy]] ([[User talk:Imamy|talk]]) 00:16, 25 April 2026 (UTC)
:{{support}} Per above…… [[User:Himvat (GNF)|Himvat (GNF)]] ([[User talk:Himvat (GNF)|talk]]) 08:17, 30 April 2026 (UTC)
:{{support}} They are a superior alternative to common.js pages etc. that people would probably use by default. [[User:Harej|Harej]] ([[User talk:Harej|talk]]) 02:09, 1 May 2026 (UTC)
:{{Support}} Per above. [[User:Emiliers|Emiliers]] ([[User talk:Emiliers|talk]]) 18:38, 1 May 2026 (UTC)
}} }}
```

## Proposal 2: do not enable CologneBlue and Modern for new wikis 

Both **[CologneBlue](https://meta.miraheze.org/wiki/mw:Skin:CologneBlue)** and **[Modern](https://meta.miraheze.org/wiki/mw:Skin:Modern)** are old skins which rarely see usage. We demoted them from being globally enabled skins, but they are still enabled by default. The logical next step is to make these skins opt-in instead of opt-out on new wikis.

### Discussion 2 

Please discuss below. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 05:07, 23 April 2026 (UTC)

 `{{ {{support}} }}` As proposer. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 05:11, 23 April 2026 (UTC)
 `{{ {{support}} }}` [KockaAdmiralac](https://meta.miraheze.org/wiki/User:KockaAdmiralac) ([talk](https://meta.miraheze.org/wiki/User_talk:KockaAdmiralac)) 17:11, 23 April 2026 (UTC)
 `{{ {{support}} }}`, Most questions about them in the Discord are about disabling them. - [JaneBuzJane](https://meta.miraheze.org/wiki/User:JaneBuzJane) ([talk](https://meta.miraheze.org/wiki/User_talk:JaneBuzJane)) 19:16, 23 April 2026 (UTC)
 `{{ {{support}} }}` per above. [TheWWRNerdGuy](https://meta.miraheze.org/wiki/User:TheWWRNerdGuy) ([talk](https://meta.miraheze.org/wiki/User_talk:TheWWRNerdGuy)) 19:51, 23 April 2026 (UTC)
 `{{ {{oppose}} }}` on the basis that a skin being enabled causes no change in behavior unless a user explicitly decides to select it. As someone who has set a non-default skin (legacy vector) as a global preference, I'll remind everyone that a user can only use a skin which has been enabled on the wiki, meaning that disabling a skin restricts user agency, which we should seek to maximize. — [chrs](https://meta.miraheze.org/wiki/User:Chrs) ([talk](https://meta.miraheze.org/wiki/User_talk:Chrs)) 23:31, 23 April 2026 (UTC)
      Legacy Vector is globally enabled. If we're gonna talk about having skins enabled by default, why would those skins be cologne blue and modern over skins like cosmos and citizen? [TheWWRNerdGuy](https://meta.miraheze.org/wiki/User:TheWWRNerdGuy) ([talk](https://meta.miraheze.org/wiki/User_talk:TheWWRNerdGuy)) 23:58, 23 April 2026 (UTC)
         I'd concur with you there, and would be willing to go so far as to say that almost every skin should be enabled globally or by default. — [chrs](https://meta.miraheze.org/wiki/User:Chrs) ([talk](https://meta.miraheze.org/wiki/User_talk:Chrs)) 00:16, 24 April 2026 (UTC)
 `{{ {{support}} }}` [SomeRandomDeveloper](https://meta.miraheze.org/wiki/User:SomeRandomDeveloper) ([talk](https://meta.miraheze.org/wiki/User_talk:SomeRandomDeveloper)) 12:33, 24 April 2026 (UTC)
 `{{ {{abstain}} }}` Meh, never cared much for either of those two skins, so you can do what you want with them. --[DarkMatterMan4500](https://meta.miraheze.org/wiki/User:DarkMatterMan4500) ([talk](https://meta.miraheze.org/wiki/User_talk:DarkMatterMan4500)) ([contribs](https://meta.miraheze.org/wiki/Special:Contributions/DarkMatterMan4500)) 15:29, 24 April 2026 (UTC)
 `{{ {{Oppose}} }}` (( As someone who may someday want to use a skin ... any skin, I would find it very helpful if it were to remain available ... The idea of opting in is a lot of work especially for the novice ... and the more we cut or reduce options, the harder it is to know what changed ... kind of makes it difficult for me as a user to know how things tied together ... It's extremely hard to open a discussion about something that is removed because I'd have to look elsewhere for words and examples ... <br /> ... I'll be more than happy to revisit my stance if a more interesting point is brought up ... ... ... because I still find things useful even when they stop working ... so that reason won't convince me to remove ... )) --- [Imamy](https://meta.miraheze.org/wiki/User:Imamy) ([talk](https://meta.miraheze.org/wiki/User_talk:Imamy)) 00:12, 25 April 2026 (UTC)
 `{{ {{Oppose}} }}` Per above…… [Himvat (GNF)](https://meta.miraheze.org/wiki/User:Himvat_(GNF)) ([talk](https://meta.miraheze.org/wiki/User_talk:Himvat_(GNF))) 08:18, 30 April 2026 (UTC)
 `{{ {{support}} }}` The default available skins should be sensible defaults, and I do not know that CologneBlue and Modern have kept up. I imagine they would clash with a lot of customized wikis as they exist. The skins should still be available but I don't think they should be default options. [Harej](https://meta.miraheze.org/wiki/User:Harej) ([talk](https://meta.miraheze.org/wiki/User_talk:Harej)) 02:09, 1 May 2026 (UTC)
 `{{ {{Support}} }}` These skins aren't used terribly often (we disabled them ourselves after a vote), and leaving unstyled/untouched skins open to be selected simply adds more burden on the admins (in case something is broken on them) without any tangible benefits. If folks want to actually use these skins, they're easy to enable after the fact. [Emiliers](https://meta.miraheze.org/wiki/User:Emiliers) ([talk](https://meta.miraheze.org/wiki/User_talk:Emiliers)) 18:44, 1 May 2026 (UTC)
 `{{ {{support}} }}` [ark](https://meta.miraheze.org/wiki/User:ark) ([talk](https://meta.miraheze.org/wiki/User_talk:ark)) 07:23, 3 May 2026 (UTC)
 `{{ {{Support}} }}` If it means reducing our servers workload (in a way). As Emiliers said, if the folk wants to use the skin, they can just easily er-enable it ~ [Elisapoly](https://meta.miraheze.org/wiki/User:Elisapoly) ([talk](https://meta.miraheze.org/wiki/User_talk:Elisapoly)) 04:08, 10 May 2026 (UTC)

## Proposal 3: remove CiteThisPage from default extensions 

```
{{ {{Discussion
|comment=Closing as {{done|successful}}. [[User:PetraMagna|PetraMagna]] ([[User talk:PetraMagna|talk]]) 07:44, 15 May 2026 (UTC)
|1=

'''[[mw:Extension:CiteThisPage|CiteThisPage]]''' adds an additional link on the sidebar. The link is frequently abused by bots and crawlers, and they clutter the interface. The Purge extension also adds a sidebar button, but the button is useful enough to warrant exclusion from this proposal.

CiteThisPage is rarely used except for the few wikis that serve citable content in an academic context. As such, we should not let this extension take up valuable space on every page of each wiki and instead let wikis that need it opt in.

=== Discussion 3 ===
Please discuss below. [[User:PetraMagna|PetraMagna]] ([[User talk:PetraMagna|talk]]) 05:07, 23 April 2026 (UTC)

:{{support}} As proposer. [[User:PetraMagna|PetraMagna]] ([[User talk:PetraMagna|talk]]) 05:11, 23 April 2026 (UTC)
:{{support}} [[User:KockaAdmiralac|KockaAdmiralac]] ([[User talk:KockaAdmiralac|talk]]) 17:11, 23 April 2026 (UTC)
:{{support}} per proposal. - [[User:JaneBuzJane|JaneBuzJane]] ([[User talk:JaneBuzJane|talk]]) 19:17, 23 April 2026 (UTC)
:{{support}} per above. [[User:TheWWRNerdGuy|TheWWRNerdGuy]] ([[User talk:TheWWRNerdGuy|talk]]) 19:51, 23 April 2026 (UTC)
:{{support|weak}} as while the usefulness of the feature outweighs interface clutter in my opinion, if it's enough of a performance problem that bots crawling it causes issues, then it would make sense to limit to wikis with actually citable content. — <span style="font-variant: small-caps">[[User:Chrs|chrs]] ([[User talk:Chrs|talk]])</span> 23:40, 23 April 2026 (UTC)
:{{support}} I don't think anybody is using this. [[User:SomeRandomDeveloper|SomeRandomDeveloper]] ([[User talk:SomeRandomDeveloper|talk]]) 12:34, 24 April 2026 (UTC)
:{{support|weak}} I just find it quite bothersome in some aspects. --[[User:DarkMatterMan4500|DarkMatterMan4500]] ([[User talk:DarkMatterMan4500|talk]]) ([[Special:Contributions/DarkMatterMan4500|contribs]]) 15:29, 24 April 2026 (UTC)
:{{Oppose}} (( ... I kind of feel educating the users on building a better looking site would be a better approach than removing the extension ... because it does sound like a useful extension ... I vote to keep the extension ... )) --- [[User:Imamy|Imamy]] ([[User talk:Imamy|talk]]) 00:33, 25 April 2026 (UTC)
::This is about not automatically enabling it for new wikis, not removing the extension from Miraheze entirely. Anyone can always enable it from ManageWiki. [[User:TheWWRNerdGuy|TheWWRNerdGuy]] ([[User talk:TheWWRNerdGuy|talk]]) 12:13, 25 April 2026 (UTC)
::::: The proposal sounded much like the change is towards improving appearance of a wiki ... It does not matter whether the User can find the extension in ManageWiki ... if creative control begins from the tech end, then a tutorial should accompany the wiki so that users know how to request help ... 
:::--- [[User:Imamy|Imamy]] ([[User talk:Imamy|talk]]) 20:49, 25 April 2026 (UTC)
:{{support}} as this seems to be very academic related, which 99% of wikis here probably don't use it ~ [[User:Elisapoly|Elisapoly]] ([[User talk:Elisapoly|talk]]) 17:40, 25 April 2026 (UTC)
:{{support}} It's a very Wikipedia-centric feature that I don't think makes sense for most wikis. Most people in my experience just copy the wiki link without building out a full academic citation. It should remain available for the wikis that want it but it doesn't make sense to me to have it on by default. [[User:Harej|Harej]] ([[User talk:Harej|talk]]) 02:09, 1 May 2026 (UTC)
:{{Neutral}} I've never used it on our wiki, but I don't want to preclude the possibility of it being really useful for other people, even just passerbys accessing our wiki for the first time. [[User:Emiliers|Emiliers]] ([[User talk:Emiliers|talk]]) 21:36, 1 May 2026 (UTC)

}} }}
```

## Proposal 4: remove URL Shortener from default extensions 

```
{{ {{Discussion
|comment=Closing as {{not done|unsuccessful}}. There is an [https://gerrit.wikimedia.org/r/c/mediawiki/extensions/UrlShortener/+/1277246 unreviewed gerrit patch] to only show the button to those who have permission to create short URLs. Further adjustments to the default MediaWiki config will allow more users to create short URLs.<br> There is also some discussions about whether the extension should use a central database on Meta or not. We changed it in the last MW upgrade which broke a lot of wikis' short URLs. We need to decide whether we want to revert this change. [[User:PetraMagna|PetraMagna]] ([[User talk:PetraMagna|talk]]) 23:02, 6 May 2026 (UTC)
|1=

'''[[mw:Extension:UrlShortener|UrlShortener]]''' has similar rationales as CiteThisPage. The extension might be more useful since getting a short URL is a common need. However, I have rarely (if ever) seen users post shortened URLs to their wiki, both on the official Miraheze Discord and on local wiki chats.

=== Discussion 4 ===
Please discuss below. [[User:PetraMagna|PetraMagna]] ([[User talk:PetraMagna|talk]]) 05:07, 23 April 2026 (UTC)

:{{support}} As proposer. [[User:PetraMagna|PetraMagna]] ([[User talk:PetraMagna|talk]]) 05:12, 23 April 2026 (UTC)
:{{support}} I've seen this extension randomly misconfigured on a wiki I was helping set up recently, and wondered why it was enabled at all. [[User:KockaAdmiralac|KockaAdmiralac]] ([[User talk:KockaAdmiralac|talk]]) 17:12, 23 April 2026 (UTC)
:{{support}} per proposal. I realized that although I'd configured this on a wiki for which I admin, I never used it. - [[User:JaneBuzJane|JaneBuzJane]] ([[User talk:JaneBuzJane|talk]]) 19:17, 23 April 2026 (UTC)
:{{support}} per above. [[User:TheWWRNerdGuy|TheWWRNerdGuy]] ([[User talk:TheWWRNerdGuy|talk]]) 19:51, 23 April 2026 (UTC)
:{{oppose}} on the basis that a short URL can be quite useful to readers. — <span style="font-variant: small-caps">[[User:Chrs|chrs]] ([[User talk:Chrs|talk]])</span> 23:41, 23 April 2026 (UTC)
:{{comment}} If we do keep this extension we should make some changes so that:
:1. Autoconfirmed/registered users can create short URLs (current default is admins, which is too restrictive). We don't want to open this to anons to avoid scraper bots creating URLs from clicking a button.
:2. The creation button is shown only for users who can create short URLs. Otherwise users would see and click the button but get a permission error.
:I don't observe much uses of this extension on a few wikis that I surveyed, but if we can implement 2 at least it will won't be abused by bots. [[User:PetraMagna|PetraMagna]] ([[User talk:PetraMagna|talk]]) 00:36, 24 April 2026 (UTC)
::Those both sound like excellent defaults. — <span style="font-variant: small-caps">[[User:Chrs|chrs]] ([[User talk:Chrs|talk]])</span> 00:39, 24 April 2026 (UTC)
: {{Oppose}} I think better approach is making it configured better by default. It is useful on wikis because it allows creating shorter URLs for very long pages, especially some non-english ones that URL encode a lot of characters, among other things, short URLs can be very helpful. It being default helps anyone being able to use it unless the wikis explicitly dont want it to be usable. While the current default setup is to restrictive, I do believe adjusting that to make users be able to create short URLs for example would be a much better experience and make the extension very useful. [[User:Universal Omega|Universal Omega]] ([[User talk:Universal Omega|talk]]) 08:52, 24 April 2026 (UTC)
:{{oppose}} per above, we should just fix the permissions [[User:SomeRandomDeveloper|SomeRandomDeveloper]] ([[User talk:SomeRandomDeveloper|talk]]) 12:35, 24 April 2026 (UTC)
: {{abstain}} Meh. --[[User:DarkMatterMan4500|DarkMatterMan4500]] ([[User talk:DarkMatterMan4500|talk]]) ([[Special:Contributions/DarkMatterMan4500|contribs]]) 15:29, 24 April 2026 (UTC)
:{{Oppose}} ((I don't use this extension but the idea of shutting down those who may using the short urls kind of bothers me ... I assume that removing the extension will remove the functionality ... ... ... I also like the points made to justify the usefulness ... ... ... There are lots of features and lots of extensions that I don't use but I'm sure that is due to circumstances and I feel this extension falls into such a category ... I vote to keep this extension ...)) --- [[User:Imamy|Imamy]] ([[User talk:Imamy|talk]]) 00:42, 25 April 2026 (UTC)
::Just FYI. All extension/skin removals here refer to removing it from ''new'' wikis, not all wikis. [[User:PetraMagna|PetraMagna]] ([[User talk:PetraMagna|talk]]) 04:11, 25 April 2026 (UTC)
::::: Thank you for clarifying ...
:::: This is not the same as if MediaWiki chose to discontinue a feature ... I feel this would still affect the ones who are accustomed to having this extension ... 
::::: I've come across this scenario enough where 2 products only on the surface look the same ... Unless there is a need for change ... it would be better to keep it uniform ...
:::--- [[User:Imamy|Imamy]] ([[User talk:Imamy|talk]]) 04:38, 25 April 2026 (UTC)
:{{Oppose}} URL shorteners can be useful for long pages. This is especially the case in languages where page titles are not written in the Latin alphabet and are often percent-encoded in URLs. These URLs get really long and unwieldy, and the URL shortener helps mitigate that. It's useful enough to be a default feature. [[User:Harej|Harej]] ([[User talk:Harej|talk]]) 02:09, 1 May 2026 (UTC)
:{{Oppose|weak}} As mentioned on Discord, we liked and used this option on our wiki until the MediaWiki update somehow moved url shorteners to farm-wide instead of individual wikis, which resulted in breaking all previous short links. While I still think the extension is useful (hence my weak oppose), I do think some settings should be changed to make it more usable, including actually allowing access to logs so we can more easily grab old shortlinks we made. [[User:Emiliers|Emiliers]] ([[User talk:Emiliers|talk]]) 21:34, 1 May 2026 (UTC)
}} }}
```

## Proposal 5: add PageImages to default extensions 

```
{{ {{Discussion
|comment=Closing as {{done|successful}} per near-unanimous support. [[User:PetraMagna|PetraMagna]] ([[User talk:PetraMagna|talk]]) 22:53, 6 May 2026 (UTC)
|1=
The popularity of '''[[mw:Extension:PageImages|PageImages]]''' can be seen from the long list of farms and distributions using it on [[mw:Extension:PageImages#See_also|the mediawiki.org page]], in addition to the WMF using it on their wikis. PageImages provides an automated mechanism for choosing an image preview, which is not perfect but works well enough for most common use cases and warrants its inclusion in every new wiki.

=== Discussion 5 ===
Please discuss below. [[User:PetraMagna|PetraMagna]] ([[User talk:PetraMagna|talk]]) 05:07, 23 April 2026 (UTC)

:{{support}} As proposer. [[User:PetraMagna|PetraMagna]] ([[User talk:PetraMagna|talk]]) 05:12, 23 April 2026 (UTC)
:{{support}} [[User:KockaAdmiralac|KockaAdmiralac]] ([[User talk:KockaAdmiralac|talk]]) 17:13, 23 April 2026 (UTC)
:{{support}} per above. [[User:TheWWRNerdGuy|TheWWRNerdGuy]] ([[User talk:TheWWRNerdGuy|talk]]) 19:52, 23 April 2026 (UTC)
:{{support}} per the reasoning given in the proposal. — <span style="font-variant: small-caps">[[User:Chrs|chrs]] ([[User talk:Chrs|talk]])</span> 23:42, 23 April 2026 (UTC)
:{{Support}} for new wikis only. - [[User:JaneBuzJane|JaneBuzJane]] ([[User talk:JaneBuzJane|talk]]) 03:49, 24 April 2026 (UTC)
:{{support}} makes a lot of sense [[User:SomeRandomDeveloper|SomeRandomDeveloper]] ([[User talk:SomeRandomDeveloper|talk]]) 12:36, 24 April 2026 (UTC)
:{{support}} This would make a lot more sense to me. --[[User:DarkMatterMan4500|DarkMatterMan4500]] ([[User talk:DarkMatterMan4500|talk]]) ([[Special:Contributions/DarkMatterMan4500|contribs]]) 15:29, 24 April 2026 (UTC)
:{{support}} per above as it helps in searching for specific articles ~ [[User:Elisapoly|Elisapoly]] ([[User talk:Elisapoly|talk]]) 18:42, 24 April 2026 (UTC)
:{{Support}} ((I don't use it but I think that a site I'm currently part of does use it ... so I am going to support for that reason  ... Also I don't know how the extension works but as long as it's available I will take the time to learn how this extension works ... and hopefully this will help me grow ... )) --- [[User:Imamy|Imamy]] ([[User talk:Imamy|talk]]) 00:50, 25 April 2026 (UTC)
:{{Support}} It's a basic infrastructural feature that enables other useful feature, including search as I understand. [[User:Harej|Harej]] ([[User talk:Harej|talk]]) 02:09, 1 May 2026 (UTC)
}} }}
```

## Proposal 6: add Popups to default extensions 

**[Popups](https://meta.miraheze.org/wiki/mw:Extension:Popups)**, which depends on PageImages and requires proposal 5 to pass, provides a convenient preview of an article's text and image when the user hovers over a link. This is a standard feature on other hosts, so users would expect preview popups to be the default behavior.

This proposal could be more controversial than the rest because it modifies MediaWiki's default behavior. However, I believe this change is largely in the positive direction.

### Discussion 6 

Please discuss below. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 05:07, 23 April 2026 (UTC)

 `{{ {{support|weak}} }}` As proposer. There are many ways TextExtracts will fail to extract anything from a wiki page, leading to an empty preview. This is my main reservation about this extension as it may degrade user experience, hence this weak support. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 05:14, 23 April 2026 (UTC)
 `{{ {{support}} }}` for similar reasons to why I supported [https://meta.miraheze.org/wiki/Community_portal/Archive_54#RfF:_Extension:MultimediaViewer_should_be_enabled_by_default](https://meta.miraheze.org/wiki/Community_portal/Archive_54#RfF:_Extension:MultimediaViewer_should_be_enabled_by_default). [TheWWRNerdGuy](https://meta.miraheze.org/wiki/User:TheWWRNerdGuy) ([talk](https://meta.miraheze.org/wiki/User_talk:TheWWRNerdGuy)) 19:54, 23 April 2026 (UTC)
 `{{ {{support}} }}` as this is a massively valuable enhancement to the reader experience. There's a reason Wikipedia uses this. — [chrs](https://meta.miraheze.org/wiki/User:Chrs) ([talk](https://meta.miraheze.org/wiki/User_talk:Chrs)) 23:45, 23 April 2026 (UTC)
 `{{ {{Support}} }}` for new wikis only. - [JaneBuzJane](https://meta.miraheze.org/wiki/User:JaneBuzJane) ([talk](https://meta.miraheze.org/wiki/User_talk:JaneBuzJane)) 03:50, 24 April 2026 (UTC)
 `{{ {{weak support}} }}` not useful in all cases, but I suppose bureaucrats can disable it again if necessary [SomeRandomDeveloper](https://meta.miraheze.org/wiki/User:SomeRandomDeveloper) ([talk](https://meta.miraheze.org/wiki/User_talk:SomeRandomDeveloper)) 12:37, 24 April 2026 (UTC)
 `{{ {{support|weak}} }}` This should've been done right from the start. --[DarkMatterMan4500](https://meta.miraheze.org/wiki/User:DarkMatterMan4500) ([talk](https://meta.miraheze.org/wiki/User_talk:DarkMatterMan4500)) ([contribs](https://meta.miraheze.org/wiki/Special:Contributions/DarkMatterMan4500)) 15:20, 24 April 2026 (UTC)
 `{{ {{support}} }}` per above. ~ [Elisapoly](https://meta.miraheze.org/wiki/User:Elisapoly) ([talk](https://meta.miraheze.org/wiki/User_talk:Elisapoly)) 18:42, 24 April 2026 (UTC)
 `{{ {{oppose|weak}} }}` as this is a somewhat intrusive piece of UX relative to other extensions, especially factoring the concern that sometimes it may simply not work, and may prove mixed as a default behavior. It's the kind of thing I would want to be optional to request right in the request form to be enabled outright, but not necessarily make the choice on the spot. But I do not feel very strongly about this. --**[raidarr](https://meta.miraheze.org/wiki/User:Raidarr)** **(** [💬](https://meta.miraheze.org/wiki/User_talk:Raidarr) **)** 00:49, 25 April 2026 (UTC)
 `{{ {{Support}} }}` Hm ... I thought Popups was already available as a default ... I may be confusing Popups with a similar extension ... but I like the idea of making Popups available ... It sounds useful ... --- [Imamy](https://meta.miraheze.org/wiki/User:Imamy) ([talk](https://meta.miraheze.org/wiki/User_talk:Imamy)) 00:56, 25 April 2026 (UTC)
 `{{ {{oppose|weak}} }}` Given the variety in how wikis are set up, popups *as a default* may clash with different customization settings. However the extension is coded well enough in my experience that this usually doesn't happen. I think the cautious thing would be to not make it default. I do not think the potential usefulness justifies the potential issues in making it default. [Harej](https://meta.miraheze.org/wiki/User:Harej) ([talk](https://meta.miraheze.org/wiki/User_talk:Harej)) 02:09, 1 May 2026 (UTC)
 `{{ {{Weak oppose}} }}` As mentioned on Discord, we found that popups just simply didn't work on our wiki, so making it default might introduce more issues than not. [Emiliers](https://meta.miraheze.org/wiki/User:Emiliers) ([talk](https://meta.miraheze.org/wiki/User_talk:Emiliers)) 18:49, 1 May 2026 (UTC)

## Proposal 7: disable wgRestrictDisplayTitle 

```
{{ {{Discussion
|comment=Closing as {{done|successful}} per near-unanimous support. wgRestrictDisplayTitle will be disabled for all wikis except those that explicitly set it to true at some point. [[User:PetraMagna|PetraMagna]] ([[User talk:PetraMagna|talk]]) 22:54, 6 May 2026 (UTC)
|1=
[[mw:Manual:$wgRestrictDisplayTitle|$wgRestrictDisplayTitle]] controls whether the <code><nowiki>{{DISPLAYTITLE}}</nowiki></code> magic word can make non-trivial changes to the page's displayed title. Setting it to <code>true</code> stems from the WMF's paranoid security model. This setting has caused lots of inconvenience in the form of support questions without much security benefits. For example, a malicious user can simply move a page to a bad title, which circumvents DisplayTitle restrictions entirely.

This change can either apply to all wikis that did not set this variable explicitly or only to new wikis. I lean toward changing this for all wikis because it's easier to implement.

=== Discussion 7a ===
Please discuss disabling this option for all wikis that did not change this option. [[User:PetraMagna|PetraMagna]] ([[User talk:PetraMagna|talk]]) 05:07, 23 April 2026 (UTC)

:{{support}} As proposer. We get lots of support questions on this and users would enable [[mw:Extension:DisplayTitle|Extension:DisplayTitle]] thinking it will fix the problem for them. [[User:PetraMagna|PetraMagna]] ([[User talk:PetraMagna|talk]]) 05:15, 23 April 2026 (UTC)
:{{support}} Other wiki farms I've seen have this disabled by default, and the restrictions seem a bit arbitrary to me. [[User:KockaAdmiralac|KockaAdmiralac]] ([[User talk:KockaAdmiralac|talk]]) 17:15, 23 April 2026 (UTC)
:{{Support}} per above. - [[User:JaneBuzJane|JaneBuzJane]] ([[User talk:JaneBuzJane|talk]]) 19:27, 23 April 2026 (UTC)
:{{support}} per above. [[User:TheWWRNerdGuy|TheWWRNerdGuy]] ([[User talk:TheWWRNerdGuy|talk]]) 19:58, 23 April 2026 (UTC)
:{{neutral}} because while this setting doesn't accomplish much in terms of actual security, it does still serve the purpose of ensuring that you can copy a page's title to use as a link. — <span style="font-variant: small-caps">[[User:Chrs|chrs]] ([[User talk:Chrs|talk]])</span> 23:53, 23 April 2026 (UTC)
::Personally I use [[mh:battlecats:MediaWiki:Gadget-CopyTitle.js|this script]] which means I don't need to worry about the page's displayed title being linkable, I can just copy the page name directly. [[User:TheWWRNerdGuy|TheWWRNerdGuy]] ([[User talk:TheWWRNerdGuy|talk]]) 00:01, 24 April 2026 (UTC)
:::This is more of a "don't confuse newer users" thing than a "don't annoy experienced users things". I can see the benefit in turning this off by default however, so while I don't oppose this I do still feel the need to point out that it's a thing for a reason (rather than just a "security feature" which [[w:WP:KABOOM|doesn't actually work]]). — <span style="font-variant: small-caps">[[User:Chrs|chrs]] ([[User talk:Chrs|talk]])</span> 00:07, 24 April 2026 (UTC)
:{{support}} per above [[User:SomeRandomDeveloper|SomeRandomDeveloper]] ([[User talk:SomeRandomDeveloper|talk]]) 12:37, 24 April 2026 (UTC)
:{{Abstain}} (( Skipping ... I don't think that I understand what this proposal is saying ... )) --- [[User:Imamy|Imamy]] ([[User talk:Imamy|talk]]) 01:05, 25 April 2026 (UTC)
:{{Support}} A tech team member can tell me if I am wrong, but if there is no true security concern with enabling it (that wouldn't exist otherwise), I think it's better to let wikis overwrite the (presented) title directly, rather than come up with some awful hack that probably won't work as well. [[User:Harej|Harej]] ([[User talk:Harej|talk]]) 02:09, 1 May 2026 (UTC)
:{{Support}} I remember this being a point of confusion for us initially before we found the setting to disable it. [[User:Emiliers|Emiliers]] ([[User talk:Emiliers|talk]]) 21:40, 1 May 2026 (UTC)

=== Discussion 7b ===
Please discuss disabling this option only for new wikis. [[User:PetraMagna|PetraMagna]] ([[User talk:PetraMagna|talk]]) 05:07, 23 April 2026 (UTC)

:{{support|weak}} I don't mind this either, except that to change the defaults only for new wikis is a lot more work for the tech team compared with switching all wikis over to a different default. [[User:PetraMagna|PetraMagna]] ([[User talk:PetraMagna|talk]]) 05:17, 23 April 2026 (UTC)
:{{Abstain}} (( Skipping ... I don't think that I understand what this proposal is saying ... )) --- [[User:Imamy|Imamy]] ([[User talk:Imamy|talk]]) 01:06, 25 April 2026 (UTC)
:{{Support}} I think my argument for this is the same as the one above. [[User:Harej|Harej]] ([[User talk:Harej|talk]]) 02:09, 1 May 2026 (UTC)
}} }}
```

## Proposal 8: enable wgNativeImageLazyLoading 

```
{{ {{Discussion
|comment=Closing as {{done|successful}} per near-unanimous support. wgNativeImageLazyLoading will be enabled for all wikis except those that explicitly disabled it at some point. [[User:PetraMagna|PetraMagna]] ([[User talk:PetraMagna|talk]]) 22:55, 6 May 2026 (UTC)
|1=
Enabling [[mw:Manual:$wgNativeImageLazyLoading|$wgNativeImageLazyLoading]] is mostly motivated by seeing wikis with hundreds of images per page complain about getting blocked by Cloudflare due to rate limiting. For example, [https://webkinzguide.com/wiki/Blue_Clothing_Collection] makes close to 1,000 requests to the server after I open the page. This short burst of requests is unnecessary because most of them are done for images that are not needed immediately.

Lazy loading is generally considered a net positive for user experience even for wikis with less images. I looked at wiki.gg and Weird Gloop, and both hosts use lazy loading.

I have found edge cases where this feature negatively impacts user experience. For example, on [https://strinova.org/wiki/Michele/gallery], the tabbing JavaScript does not handle lazy-loading well: clicking on a tab leads to a short delay in image loading. By enabling lazy loading we might hurt a small subset of wikis. However, mitigations for the tabbing problem exist, and I think lazy loading improves user experience overall.

This change can either apply to all wikis that did not set this variable explicitly or only to new wikis. I lean toward changing this for all wikis because it's easier to implement. Plus, many existing wikis are affected by the excessive number of images on a page but don't know about this option.

=== Discussion 8a ===
Please discuss enabling this option for all wikis that did not change this option. [[User:PetraMagna|PetraMagna]] ([[User talk:PetraMagna|talk]]) 05:07, 23 April 2026 (UTC)

:{{support}} As proposer. [[User:PetraMagna|PetraMagna]] ([[User talk:PetraMagna|talk]]) 05:17, 23 April 2026 (UTC)
:{{support}} [[User:KockaAdmiralac|KockaAdmiralac]] ([[User talk:KockaAdmiralac|talk]]) 17:16, 23 April 2026 (UTC)
:{{Support}} per proposal. - [[User:JaneBuzJane|JaneBuzJane]] ([[User talk:JaneBuzJane|talk]]) 19:29, 23 April 2026 (UTC)
:{{support}} per above. [[User:TheWWRNerdGuy|TheWWRNerdGuy]] ([[User talk:TheWWRNerdGuy|talk]]) 19:58, 23 April 2026 (UTC)
:{{support|weak}} as while on net this is an improvement, this will cause a regression with respect to tabs. — <span style="font-variant: small-caps">[[User:Chrs|chrs]] ([[User talk:Chrs|talk]])</span> 00:00, 24 April 2026 (UTC)
:{{support}} per proposal [[User:SomeRandomDeveloper|SomeRandomDeveloper]] ([[User talk:SomeRandomDeveloper|talk]]) 12:38, 24 April 2026 (UTC)
:{{Abstain}} (( Skipping ... Not sure that I really want this or understand the implications ... I kind of feel that it would be better served to educate instead of changing the setting ... It's kind of difficult to express or describe the exact nature of issues such as loading issues unless one is very lucky to say it right the first time and to be understood the first time ... I feel it may be better to just wait for requests for assistance and then offer this as a solution ... rather than to try and reverse explain that all the new behavior is due to a default setting has changed sometime a few years ago when they were not paying attention to that specific page when the change took place ... )) --- [[User:Imamy|Imamy]] ([[User talk:Imamy|talk]]) 01:19, 25 April 2026 (UTC)
:{{support}} Good measure to cut down on bandwidth use. Not everyone has unlimited data. [[User:Harej|Harej]] ([[User talk:Harej|talk]]) 02:09, 1 May 2026 (UTC)
:{{Support}} I'd have to see this in action first to see whether or not it'll affect the performance of some of our tabber-heavy pages, but I wouldn't mind this being the default. If needed, it can always be disabled. [[User:Emiliers|Emiliers]] ([[User talk:Emiliers|talk]]) 21:45, 1 May 2026 (UTC)
:{{support}} [[User:ark|ark]] ([[User talk:ark|talk]]) 07:35, 3 May 2026 (UTC)

=== Discussion 8b ===
Please discuss enabling this option only for new wikis. [[User:PetraMagna|PetraMagna]] ([[User talk:PetraMagna|talk]]) 05:07, 23 April 2026 (UTC)

:{{support|weak}} Same rationale as 7b. This is more work for the tech team compared with 8a. [[User:PetraMagna|PetraMagna]] ([[User talk:PetraMagna|talk]]) 05:18, 23 April 2026 (UTC)
:{{Oppose}} (( I think that most people can't differentiate between the age of a wiki ... They'll just be confused to know why their wiki behaves differently from some other wiki ... I prefer changing settings to all wikis or no wikis ...)) --- [[User:Imamy|Imamy]] ([[User talk:Imamy|talk]]) 01:22, 25 April 2026 (UTC)
:{{support}} I think I support it either way. [[User:Harej|Harej]] ([[User talk:Harej|talk]]) 02:09, 1 May 2026 (UTC)
}} }}
```

## Proposal 9: add InputBox to default extensions 

```
{{ {{Discussion
|comment=Closing as {{done|successful}}. [[User:PetraMagna|PetraMagna]] ([[User talk:PetraMagna|talk]]) 07:46, 15 May 2026 (UTC)
|1=

Many new users don't know how to create a wiki page. To address this, the default main page for new wikis recommend enabling CreatePage or CreatePageUw. This is not necessary if '''[[mw:Extension:InputBox|InputBox]]''' is enabled: we can simply add a page creation input box to the main page. The user enters a page title and is taken to the editing interface to create the corresponding page. This improves the new wiki experience, and if the wiki does not need the functionalities of this extension, InputBox stays out of the way.

Note that InputBox's benefits apply only to the main page of new wikis, though it has many other uses and is [[mw:Extension:InputBox#See_also|deployed on many other wiki hosts]].

=== Discussion 9 ===
Please discuss below. [[User:PetraMagna|PetraMagna]] ([[User talk:PetraMagna|talk]]) 05:07, 23 April 2026 (UTC)

:{{support}} As proposer. [[User:PetraMagna|PetraMagna]] ([[User talk:PetraMagna|talk]]) 05:18, 23 April 2026 (UTC)
:{{Weak support}} I personally believe that users need to figure a few things out on their own ("teach a man to fish" etc.) but I know that MH as a farm does try to enable editors of all types, especially new wikians, and this proposal would support that initiative. I also don't like that this extension explicitly calls out that the [[mw:Extension:InputBox#General_syntax|buttons aren't accessible]], yet has made no move to fix it—but that is mostly a personal quibble. - [[User:JaneBuzJane|JaneBuzJane]] ([[User talk:JaneBuzJane|talk]]) 19:38, 23 April 2026 (UTC)
:{{support}} looks like a good way to reduce the "how to make an article" questions we get. [[User:TheWWRNerdGuy|TheWWRNerdGuy]] ([[User talk:TheWWRNerdGuy|talk]]) 20:17, 23 April 2026 (UTC)
:{{support}} as this is a useful extension in general and one without downsides to enabling. — <span style="font-variant: small-caps">[[User:Chrs|chrs]] ([[User talk:Chrs|talk]])</span> 23:58, 23 April 2026 (UTC)
:{{support}} per above as this is generally good for brand new users ~ [[User:Elisapoly|Elisapoly]] ([[User talk:Elisapoly|talk]]) 18:42, 24 April 2026 (UTC)
:{{Oppose}} (( It feels intrusive ... Even though it may be easy to disable but I think it's much the same as when it was proposed to add a community portal to every wiki by default ... I am okay with it if it is an option that can be selected from within the wiki request to be implemented if the wiki is approved ... but I do not want it as a default ... )) --- [[User:Imamy|Imamy]] ([[User talk:Imamy|talk]]) 01:29, 25 April 2026 (UTC)
:{{support}} I've always found it to be useful as an entry point for page creation. [[User:Harej|Harej]] ([[User talk:Harej|talk]]) 02:09, 1 May 2026 (UTC)
:{{Abstain}} Personal preference, but I prefer the Create Page link over an input box, and looking at the docs, the buttons having nonaccessible labels don't inspire much confidence either. But I also don't want to reject an extension I've never even tried out before, especially when it's clear that others find it a useful entry point. [[User:Emiliers|Emiliers]] ([[User talk:Emiliers|talk]]) 21:50, 1 May 2026 (UTC)
: {{support|partial}} I wouldn't mind this very much. --[[User:DarkMatterMan4500|DarkMatterMan4500]] ([[User talk:DarkMatterMan4500|talk]]) ([[Special:Contributions/DarkMatterMan4500|contribs]]) 18:32, 9 May 2026 (UTC)

}} }}
```

## Proposal 10: add VisualEditor to default extensions 

 `{{ {{Discussion top|Closed as {{done|successful}}. [[User:PetraMagna|PetraMagna]] ([[User talk:PetraMagna|talk]]) 12:07, 20 May 2026 (UTC)}} }}`
**[VisualEditor](https://meta.miraheze.org/wiki/mw:Extension:VisualEditor)** is a controversial extension. I did not expect it to receive support knowing that most experienced editors only use the source editor. However, River changed my mind on this topic. A paraphrase of her argument is below:

| + How different defaults affect users |
| Want VE? | Know how ManageWiki works | VE is default | VE is not default |
| --- | --- | --- | --- |
| Yes | Yes | No action needed | They can toggle it in ManageWiki |
| Yes | No | No action needed | They will be inconvenienced. |
| No | Yes | They can toggle it in ManageWiki | No action needed |
| No | No | They will be inconvenienced. | No action needed |

If someone knows how ManageWiki works, they can simply toggle VisualEditor. If they don't, we arrive at 2 groups of editors:
* They want VE. If VE is not the default, they need to figure out how ManageWiki works.
* They do not want VE. If VE is the default, they need to figure out how ManageWiki/Preferences works.
Those who prefer the source editor over VE are likely to be more familiar with the MediaWiki ecosystem and know their way around reading documentation. They are much more likely to figure ManageWiki out by themselves than those who only know VE. As such, when faced with a choice between either group, we should inconvenience the veterans in group 2 instead of the newbies in group 1.

I still have my reservations about VE due to its many quirks, but I think this proposal is worth considering.

### Discussion 10 

Please discuss below. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 05:07, 23 April 2026 (UTC)

 `{{ {{support|weak}} }}` I still have some doubts about VE itself, but since this is a popular extension I think River's argument makes a lot of sense. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 05:19, 23 April 2026 (UTC)
 `{{ {{support}} }}` I've mostly had a positive experience with VisualEditor on wikis where I've enabled it by default, and with properly set up TemplateData it can be a really powerful tool for new editors. [KockaAdmiralac](https://meta.miraheze.org/wiki/User:KockaAdmiralac) ([talk](https://meta.miraheze.org/wiki/User_talk:KockaAdmiralac)) 18:14, 23 April 2026 (UTC)
 `{{ {{Weak support}} }}` I hate VE but I agree with the proposal that we should inconvenience the experienced admins/editors over the new ones. - [JaneBuzJane](https://meta.miraheze.org/wiki/User:JaneBuzJane) ([talk](https://meta.miraheze.org/wiki/User_talk:JaneBuzJane)) 19:39, 23 April 2026 (UTC)
 `{{ {{support}} }}` I've seen numerous [SR/D](https://meta.miraheze.org/wiki/SR/D) requests from people who want to go back to Fandom's simplicity, often citing the visual editor despite the fact that it's right here and available on Miraheze. VE can be disabled in [Special:GlobalPreferences](https://meta.miraheze.org/wiki/Special:GlobalPreferences) so enabling it by default really shouldn't be an inconvenience to whoever doesn't like it. [TheWWRNerdGuy](https://meta.miraheze.org/wiki/User:TheWWRNerdGuy) ([talk](https://meta.miraheze.org/wiki/User_talk:TheWWRNerdGuy)) 20:20, 23 April 2026 (UTC)
 `{{ {{support|weak}} }}` as while I certainly don't use it, making more tools available by default is generally better. — [chrs](https://meta.miraheze.org/wiki/User:Chrs) ([talk](https://meta.miraheze.org/wiki/User_talk:Chrs)) 00:20, 24 April 2026 (UTC)
 `{{ {{oppose}} }}` a lot of our extensions are not really compatible with VE (e.g. most of the ones that provide parser functions), and I think that enabling VE by default would degrade the UX for new users / wiki admins. The vast majority of documentation regarding extensions provides examples for the source editor. [SomeRandomDeveloper](https://meta.miraheze.org/wiki/User:SomeRandomDeveloper) ([talk](https://meta.miraheze.org/wiki/User_talk:SomeRandomDeveloper)) 12:44, 24 April 2026 (UTC)
 `{{ {{support|strongest}} }}` As I myself coming from Fandom after editing for a few years, I have used Visual Editor for almost a year (as Fandom strongly support using VE back then) before my admins on my wiki encourages me to use Source Editor for more complex coding as well as having more granularity when it comes to wiki editing. Now, while I'm already used to Source Editor, many more who are migrating from Fandom will soon find it a rude awakening that VE here is not a default extension and have to maneuver through ManageWiki. Experience in using VE here is also not the same as Fandom but that's another topic for another day. Is it inconvenience though for veterans? I think not as we just simply click 'Edit Source'. ~ [Elisapoly](https://meta.miraheze.org/wiki/User:Elisapoly) ([talk](https://meta.miraheze.org/wiki/User_talk:Elisapoly)) 18:33, 24 April 2026 (UTC)
 `{{ {{support}} }}` as someone who personally loathes the editor, but notices it is commonly popular, expected, and a minor hurdle to deal with for operators when they want it. Conversely, anyone committed to not having it or notices some conflict or ill behavior with it can pretty easily have their cake too. I'm open to changing if there are similarly popular extensions that people commonly enable on new wikis otherwise that really don't play nicely. --**[raidarr](https://meta.miraheze.org/wiki/User:Raidarr)** **(** [💬](https://meta.miraheze.org/wiki/User_talk:Raidarr) **)** 00:55, 25 April 2026 (UTC)
 `{{ {{Support}} }}` ((I was never able to figure out how to use VE but I'm certain that some will say the same with source editing ... It's really comes down to customization ... A wiki is for most their home away from home ... so I think conflicts and set backs where ManageWiki is concerned is not very important ... If they really want VE and if they have to learn ManageWiki, then they will figure it out as they go along ... but to keep someone from developing their wiki by restricting VE makes no sense since managing and maintaining wikis is hard enough as it is ... I don't feel that ManageWiki is necessary until after there is actual content on the site ... but odds of creating content is slim if the editor has to spend all their time figuring out how to use editing tools ...)) --- [Imamy](https://meta.miraheze.org/wiki/User:Imamy) ([talk](https://meta.miraheze.org/wiki/User_talk:Imamy)) 01:43, 25 April 2026 (UTC)
 `{{ {{support}} }}` If you are a new editor, VisualEditor does *so much* to mitigate the inessential weirdness that comes with editing MediaWiki pages. As best as I can tell, you can only find MediaWiki markup in MediaWiki—not in Google Docs, Microsoft Word, Markdown, LaTeX, anything. It's unique to this particular software. Aside from helping those with less experience, it helps me (as someone who's been editing wikis for over 20 years) be more efficient. I think the concern about extension compatibility is valid – the experience is shallow beyond support for built-in MediaWiki syntax – and wikis have the option to disable it. I think, for most wikis, the usefulness outweighs the drawbacks. [Harej](https://meta.miraheze.org/wiki/User:Harej) ([talk](https://meta.miraheze.org/wiki/User_talk:Harej)) 02:09, 1 May 2026 (UTC)
 `{{ {{Weak support}} }}` I hate visual editor and never use it unless I have to write guidelines/docs for the wiki, but I know experienced editors who swear by it. Also, VE is needed for DiscussionTools to work, and that extension has drastically reduced the amount of unsigned comments and made it much easier for new editors to participate in discussions, so overall I think VE is a net positive. And anyone who prefers Source will most likely find it fairly easy to disable Visual in their preferences, as I did. [Emiliers](https://meta.miraheze.org/wiki/User:Emiliers) ([talk](https://meta.miraheze.org/wiki/User_talk:Emiliers)) 18:55, 1 May 2026 (UTC)
 `{{ {{support|weak}} }}` [ark](https://meta.miraheze.org/wiki/User:ark) ([talk](https://meta.miraheze.org/wiki/User_talk:ark)) 07:38, 3 May 2026 (UTC)
    I lean towards a `{{ {{support|weak}} }}` as well on the original argument raised by Petra and River. I share SRD's concerns on the matter, but think that the user interesting in using such parser functions also fall into the group of more experienced users who can figure out how to turn off VE without much trouble. I would like to possibly see a note on the default wiki main page addressing this slightly though, to minimize confusion for new users. As for the existing docs... yeah that's just not gonna be fun for us but I think overall a net positive, if we do it right. --***[<span style="color:#ff00ae">PixDeVl</span>](https://meta.miraheze.org/wiki/User:PixDeVl)* ([T](https://meta.miraheze.org/wiki/User_talk:PixDeVl)&#124;[C](https://meta.miraheze.org/wiki/Special:Contribs/PixDeVl)&#124;[G](https://meta.miraheze.org/wiki/Special:CA/PixDeVl))** 02:15, 10 May 2026 (UTC)
 `{{ {{support}} }}` This should've been done right from the start, honestly. --[DarkMatterMan4500](https://meta.miraheze.org/wiki/User:DarkMatterMan4500) ([talk](https://meta.miraheze.org/wiki/User_talk:DarkMatterMan4500)) ([contribs](https://meta.miraheze.org/wiki/Special:Contributions/DarkMatterMan4500)) 17:04, 16 May 2026 (UTC)
 `{{ {{Discussion bottom}} }}`

## Proposal 11: add Linter and DiscussionTools to default extensions 

```
{{ {{Discussion
|comment=Closing as {{done|successful}} per unanimous support. This will need to wait on the VisualEditor proposal. [[User:PetraMagna|PetraMagna]] ([[User talk:PetraMagna|talk]]) 22:56, 6 May 2026 (UTC)
|1=
'''[[mw:Extension:DiscussionTools|DiscussionTools]]''' is one of my main motivations to enable VisualEditor by default. It makes on-wiki discussions much easier and handles signatures which new users find unintuitive.

'''[[mw:Extension:Linter|Linter]]''' is a required extension for DiscussionTools, so it will be enabled by default as well if this proposal passes.

=== Discussion 11 ===
Please discuss below. [[User:PetraMagna|PetraMagna]] ([[User talk:PetraMagna|talk]]) 05:07, 23 April 2026 (UTC)

:{{support|strongest}} DiscussionTools makes talk pages so much easier to use. In fact, I structured this page in a way that makes it easier for other editors to respond using DiscussionTools. If VisualEditor does get enabled by default, I am strongly in favor of enabling DiscussionTools as well. [[User:PetraMagna|PetraMagna]] ([[User talk:PetraMagna|talk]]) 05:22, 23 April 2026 (UTC)
:{{support|strongest}} Super useful extension, wholeheartedly support. [[User:Crystalite13|'''💎Crystalite13💎''']] 17:14, 23 April 2026 (UTC)
:{{support}} In addition, Linter lets you find some silly formatting mishaps that you wouldn't have found otherwise. [[User:KockaAdmiralac|KockaAdmiralac]] ([[User talk:KockaAdmiralac|talk]]) 18:15, 23 April 2026 (UTC)
:{{support}} per above. - [[User:JaneBuzJane|JaneBuzJane]] ([[User talk:JaneBuzJane|talk]]) 19:41, 23 April 2026 (UTC)
:{{support}} per above. [[User:TheWWRNerdGuy|TheWWRNerdGuy]] ([[User talk:TheWWRNerdGuy|talk]]) 20:23, 23 April 2026 (UTC)
:{{support}} as DiscussionTools is an incredibly useful extension. — <span style="font-variant: small-caps">[[User:Chrs|chrs]] ([[User talk:Chrs|talk]])</span> 00:20, 24 April 2026 (UTC)
:{{support|strong}} per above [[User:SomeRandomDeveloper|SomeRandomDeveloper]] ([[User talk:SomeRandomDeveloper|talk]]) 12:45, 24 April 2026 (UTC)
:{{support|strongest}} super useful extensions ~ [[User:Elisapoly|Elisapoly]] ([[User talk:Elisapoly|talk]]) 18:42, 24 April 2026 (UTC)
:{{Support}} ((It would make a more consistent experience across wikis ... It may also reduce experimentation with other discussion / comment extensions ...)) --- [[User:Imamy|Imamy]] ([[User talk:Imamy|talk]]) 01:48, 25 April 2026 (UTC)
:{{support}} DiscussionTools is lovely and helps addresses the issue that discussions on MediaWiki don't work like they do anywhere else. [[User:Harej|Harej]] ([[User talk:Harej|talk]]) 02:09, 1 May 2026 (UTC)
:{{support|strongest}} Justifies the annoyance of VE and then some. [[User:Emiliers|Emiliers]] ([[User talk:Emiliers|talk]]) 18:58, 1 May 2026 (UTC)
:{{support}} per above. [[User:ark|ark]] ([[User talk:ark|talk]]) 07:38, 3 May 2026 (UTC)

}} }}
```

## Proposal 12: disable $wgTabberNeueEnableAnimation by default 

This was a suggestion of [User:TheWWRNerdGuy](https://meta.miraheze.org/wiki/User:TheWWRNerdGuy).

An update to the extension close to 2 years ago enabled animations by default for all wikis ([T12350](https://meta.miraheze.org/wiki/phorge:T12350)). The animation is slow and results in prolonged waiting for content to show up. An example of the scrolling animation can be seen on [Public Test Wiki](https://publictestwiki.com/wiki/User:PetraMagna/TabberNeue). In comparison, on [a page with scrolling disabled](https://strinova.org/wiki/User:PetraMagna/TabberNeue), the user experience is much smoother.

I believe following the upstream default was a mistake. Animations consuming an excessive amount of time should be disabled by default.

### Discussion 12a 

Please discuss disabling this option for all wikis that did not change this option. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 05:07, 23 April 2026 (UTC)

 `{{ {{Support}} }}` As proposer. I've been a hater of `$wgTabberNeueEnableAnimation` ever since [T12350](https://meta.miraheze.org/wiki/phorge:T12350). [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 05:24, 23 April 2026 (UTC)
 `{{ {{weak support}} }}` I'm alright with the animation. However, it feels like it might screw with some lazyloading: if you have an image tabber, click on tab 1 and then tab 3, it might either load the images in tab 2, or display a blank tab. I haven't properly tested this scenario, though. [KockaAdmiralac](https://meta.miraheze.org/wiki/User:KockaAdmiralac) ([talk](https://meta.miraheze.org/wiki/User_talk:KockaAdmiralac)) 18:18, 23 April 2026 (UTC)
 `{{ {{support}} }}` per proposal. - [JaneBuzJane](https://meta.miraheze.org/wiki/User:JaneBuzJane) ([talk](https://meta.miraheze.org/wiki/User_talk:JaneBuzJane)) 19:41, 23 April 2026 (UTC)
 `{{ {{support|strongest}} }}` shouldn't be surprising since I was the one who suggested it but I hate the animation and the motion sickness it gives me. [TheWWRNerdGuy](https://meta.miraheze.org/wiki/User:TheWWRNerdGuy) ([talk](https://meta.miraheze.org/wiki/User_talk:TheWWRNerdGuy)) 20:24, 23 April 2026 (UTC)
 `{{ {{support}} }}` per above, bad upstream default. — [chrs](https://meta.miraheze.org/wiki/User:Chrs) ([talk](https://meta.miraheze.org/wiki/User_talk:Chrs)) 00:22, 24 April 2026 (UTC)
 `{{ {{Abstain}} }}` (( ... Skipping ... don't know how this works ... )) --- [Imamy](https://meta.miraheze.org/wiki/User:Imamy) ([talk](https://meta.miraheze.org/wiki/User_talk:Imamy)) 01:50, 25 April 2026 (UTC)
 `{{ {{support}} }}` The animation slows things down and isn't necessary. [Harej](https://meta.miraheze.org/wiki/User:Harej) ([talk](https://meta.miraheze.org/wiki/User_talk:Harej)) 02:09, 1 May 2026 (UTC)
 `{{ {{Abstain}} }}` I personally hate the animation, but I've seen a few editors who find it neat, so I don't want to yuck their yum. If there's a tech reason for wanting to disable this (e.g. performance improvements), then consider this a weak support instead. [Emiliers](https://meta.miraheze.org/wiki/User:Emiliers) ([talk](https://meta.miraheze.org/wiki/User_talk:Emiliers)) 21:53, 1 May 2026 (UTC)
 `{{ {{support}} }}` [ark](https://meta.miraheze.org/wiki/User:ark) ([talk](https://meta.miraheze.org/wiki/User_talk:ark)) 07:40, 3 May 2026 (UTC)
 `{{ {{support|weak}} }}` This might entirely be dependent on the users' preferences. Some don't like animation while some find it neat to see animation. I, for one, would support disabling it, albeit weak as I worry that disabling it might prompt questions from users in discord. ~ [Elisapoly](https://meta.miraheze.org/wiki/User:Elisapoly) ([talk](https://meta.miraheze.org/wiki/User_talk:Elisapoly)) 04:20, 10 May 2026 (UTC)
 `{{ {{support|weak}} }}` It does get irritating, especially when you don't even know which ones you want to use, and end up screwing something up by mistake. --[DarkMatterMan4500](https://meta.miraheze.org/wiki/User:DarkMatterMan4500) ([talk](https://meta.miraheze.org/wiki/User_talk:DarkMatterMan4500)) ([contribs](https://meta.miraheze.org/wiki/Special:Contributions/DarkMatterMan4500)) 17:08, 16 May 2026 (UTC)
### Discussion 12b 

Please discuss disabling this option only for new wikis. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 05:07, 23 April 2026 (UTC)

 `{{ {{support|weak}} }}` Same rationale as 7b. This is more work for the tech team compared with 12a. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 05:25, 23 April 2026 (UTC)
 `{{ {{oppose|weka}} }}` in favor of 12a per `{{ {{no ping|PetraMagna}} }}` and the fact that this discussion originated from a bad change to defaults by upstream. — [chrs](https://meta.miraheze.org/wiki/User:Chrs) ([talk](https://meta.miraheze.org/wiki/User_talk:Chrs)) 00:25, 24 April 2026 (UTC)
 `{{ {{Oppose}} }}` (( ... I really don't like the idea of troubleshooting issues that require knowledge of which wiki generation that a wiki came from ... I prefer apply to all or apply to none ... )) --- [Imamy](https://meta.miraheze.org/wiki/User:Imamy) ([talk](https://meta.miraheze.org/wiki/User_talk:Imamy)) 01:53, 25 April 2026 (UTC)
 `{{ {{support}} }}` The animation slows things down and isn't necessary. [Harej](https://meta.miraheze.org/wiki/User:Harej) ([talk](https://meta.miraheze.org/wiki/User_talk:Harej)) 02:09, 1 May 2026 (UTC)
 `{{ {{Support}} }}` Honestly, thinking about it a bit more, this might be a better option if disabling the animation is preferred, so it doesn't mess with a setting that existing wikis have probably gotten used to (if they haven't taken the opportunity to disable it already). [Emiliers](https://meta.miraheze.org/wiki/User:Emiliers) ([talk](https://meta.miraheze.org/wiki/User_talk:Emiliers)) 04:36, 2 May 2026 (UTC)
 `{{ {{Support}} }}` For new wiki, I support. If they want the animation, they could just easily enable it. ~ [Elisapoly](https://meta.miraheze.org/wiki/User:Elisapoly) ([talk](https://meta.miraheze.org/wiki/User_talk:Elisapoly)) 04:20, 10 May 2026 (UTC)
 `{{ {{support|weak}} }}` Per other people's opinions, in addition to the fact that this would probably be for the best in the long-term. --[DarkMatterMan4500](https://meta.miraheze.org/wiki/User:DarkMatterMan4500) ([talk](https://meta.miraheze.org/wiki/User_talk:DarkMatterMan4500)) ([contribs](https://meta.miraheze.org/wiki/Special:Contributions/DarkMatterMan4500)) 17:08, 16 May 2026 (UTC)

## Proposal 13: disable $wgPortableInfoboxUseHeadings by default 

This was a suggestion of [User:TheWWRNerdGuy](https://meta.miraheze.org/wiki/User:TheWWRNerdGuy).

This setting causes compatibility issues with other extensions such as TextExtracts (see [GitHub issue](https://github.com/lkucharczyk/mediawiki-PortableInfobox/issues/17)). It will soon be set to false by default ([PR](https://github.com/Universal-Omega/PortableInfobox/pull/185)) due to other reasons such as incompatibility with Parsoid.

I am in favor of applying this change only to new wikis. Old wikis should keep the old setting because it is a breaking change and could mess up their CSS (`h3` becomes `div`). If we want to apply a breaking HTML change, we should do so when we upgrade MediaWiki when users are expecting breaking changes.

### Discussion 13a 

Please discuss disabling this option for all wikis that did not change this option. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 05:07, 23 April 2026 (UTC)

 `{{ {{support|weak}} }}` For reasons said above. If we want to take this route, we should delay the implementation until the next MediaWiki upgrade where breaking changes are expected. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 05:28, 23 April 2026 (UTC)
 `{{ {{support}} }}` if it's going to break with parsoid anyway and disabling it for all wikis is the easier option, I don't see why we don't just kill two birds with one stone. [TheWWRNerdGuy](https://meta.miraheze.org/wiki/User:TheWWRNerdGuy) ([talk](https://meta.miraheze.org/wiki/User_talk:TheWWRNerdGuy)) 20:28, 23 April 2026 (UTC)
      This issue was raised in [mediazilla:T363025](https://meta.miraheze.org/wiki/mediazilla:T363025): Parsoid messes with section headings and there was no way to disable that behavior. I don't think the WMF responded to or fixed the issue, but it is not impossible that they somehow address it before MW 1.47. One can dream. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 23:18, 23 April 2026 (UTC)
         VisualEditor actually [strips section tags](https://meta.miraheze.org/wiki/github:wikimedia/mediawiki/blob/REL1_45/includes/Rest/Handler/Helper/HtmlOutputRendererHelper.php#L786-L811) already, and given [wmfphab:T385317](https://meta.miraheze.org/wiki/wmfphab:T385317) I feel like there's some hope for section stripping to become configurable, lest we resort to [forbidden magic](https://meta.miraheze.org/wiki/github:utdrwiki/PortableInfobox/commit/04f868d). [KockaAdmiralac](https://meta.miraheze.org/wiki/User:KockaAdmiralac) ([talk](https://meta.miraheze.org/wiki/User_talk:KockaAdmiralac)) 23:39, 23 April 2026 (UTC)
 `{{ {{comment}} }}` I was just informed by [User:Universal Omega](https://meta.miraheze.org/wiki/User:Universal_Omega) that PortableInfobox plans to remove this option soon and will default to using `div` instead of headings. Depending on our update cadence of the extension, this change will reach Miraheze no later than MediaWiki 1.46, which will happen in about 2 to 3 months. Thus, the outcome of this proposal will be less consequential than the others. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 09:06, 24 April 2026 (UTC)
 `{{ {{Abstain}} }}` (( ... Skipping ... going way over my head ... )) --- [Imamy](https://meta.miraheze.org/wiki/User:Imamy) ([talk](https://meta.miraheze.org/wiki/User_talk:Imamy)) 01:56, 25 April 2026 (UTC)
 `{{ {{support|strongest}} }}` There is another problem is that TextExtracts treats the `{{ {{code|<h2>}} }}` tag within PortableInfoboxes as “real heading within body text.” Consequently, if an extension calling TextExtracts utilizes the parameters `{{ {{code|&exintro{{=}}true}} }}` or `{{ {{code|&explaintext{{=}}true&exintro{{=}}true}} }}`, the extract will be empty. (such as Popups when `{{ {{code|$wgPopupsTextExtractsIntroOnly {{=}} True}} }}`, WikiSEO when `{{ {{code|$wgWikiSeoEnableAutoDescription {{=}} True}} }}`).<br />Furthermore, broken CSS is relatively easy to spot and fix, while these issues with TextExtracts are much more difficult to find and fix. --[Maitian MaiLin](https://meta.miraheze.org/wiki/User:Maitian_MaiLin) ([talk](https://meta.miraheze.org/wiki/User_talk:Maitian_MaiLin)) 08:00, 30 April 2026 (UTC)
 `{{ {{Abstain}} }}` [Harej](https://meta.miraheze.org/wiki/User:Harej) ([talk](https://meta.miraheze.org/wiki/User_talk:Harej)) 02:09, 1 May 2026 (UTC)
 `{{ {{support}} }}` given the incompatibility with both TextExtracts and Parsoid. It appears that we will need to bite this bullet, and I would strongly concur with the general principle espoused by PetraMagna that the best time to do this sort of thing would be alongside a MediaWiki update. — [chrs](https://meta.miraheze.org/wiki/User:Chrs) ([talk](https://meta.miraheze.org/wiki/User_talk:Chrs)) 03:22, 1 May 2026 (UTC)
 `{{ {{support|weak}} }}` I mean, I wouldn't mind these types of changes for shit that I rarely (or barely) even use, so yeah. --[DarkMatterMan4500](https://meta.miraheze.org/wiki/User:DarkMatterMan4500) ([talk](https://meta.miraheze.org/wiki/User_talk:DarkMatterMan4500)) ([contribs](https://meta.miraheze.org/wiki/Special:Contributions/DarkMatterMan4500)) 11:33, 4 May 2026 (UTC)

### Discussion 13b 

Please discuss disabling this option only for new wikis. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 05:07, 23 April 2026 (UTC)

 `{{ {{support}} }}` Although `$wgPortableInfoboxUseHeadings` will likely be removed eventually (due to incompatibilities with Parsoid), it may not happen in the near future, especially since we are uncertain whether Parsoid read view will actually happen on MW 1.47. We should try to not break our wikis if possible, even if it means more work for tech. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 05:34, 23 April 2026 (UTC)
 `{{ {{support}} }}` per proposal - while 13a would make sense, I support the less disruptive way overall. - [JaneBuzJane](https://meta.miraheze.org/wiki/User:JaneBuzJane) ([talk](https://meta.miraheze.org/wiki/User_talk:JaneBuzJane)) 19:44, 23 April 2026 (UTC)
 `{{ {{Oppose}} }}` (( ... I prefer that wiki behavior is consistent regardless of creation date ... )) --- [Imamy](https://meta.miraheze.org/wiki/User:Imamy) ([talk](https://meta.miraheze.org/wiki/User_talk:Imamy)) 02:00, 25 April 2026 (UTC)
 `{{ {{Abstain}} }}` [Harej](https://meta.miraheze.org/wiki/User:Harej) ([talk](https://meta.miraheze.org/wiki/User_talk:Harej)) 02:09, 1 May 2026 (UTC)
 `{{ {{Comment}} }}` We don't use portable infoboxes on our wiki, so this doesn't affect us, which is why I initially abstained, but I figure I might offer my two cents. Since headings are being depreciated in the next MediaWiki upgrade, it makes sense to me to hold off 13a until then, rather than doing it now, but even if it's more work for the tech team *now*, it might be helpful to disable this option for new wikis, just so you don't get even more people having issues with this once the entire option gets depreciated and you're even more busy fixing all the other bugs that came with the new MediaWiki upgrade. So more work now for less work later. Of course, this is just a suggestion by someone outside looking in, so you don't have to listen to it, especially if the work now would be more taxing than bug-fixing later. [Emiliers](https://meta.miraheze.org/wiki/User:Emiliers) ([talk](https://meta.miraheze.org/wiki/User_talk:Emiliers)) 01:37, 7 May 2026 (UTC)
 `{{ {{Abstain}} }}` Meh. --[DarkMatterMan4500](https://meta.miraheze.org/wiki/User:DarkMatterMan4500) ([talk](https://meta.miraheze.org/wiki/User_talk:DarkMatterMan4500)) ([contribs](https://meta.miraheze.org/wiki/Special:Contributions/DarkMatterMan4500)) 17:10, 16 May 2026 (UTC)

## Proposal 14: enable $wgVectorResponsive by default 

This was a suggestion of [User:KockaAdmiralac](https://meta.miraheze.org/wiki/User:KockaAdmiralac).

When visiting a wiki without [MobileFrontend](https://meta.miraheze.org/wiki/mw:Extension:MobileFrontend) on mobile, Vector 2022 will default to the desktop view instead of using its responsive version. Although [the documentation](https://meta.miraheze.org/wiki/mw:Manual:$wgVectorResponsive) says it doesn't do anything, this setting still makes a difference by [marking a skin as responsive](https://github.com/wikimedia/mediawiki-skins-Vector/blob/6debcfe8aa68d2ba01e8a3a127a5bcc79bc4aab3/includes/SkinVector22.php#L81), which allows mobile users to see the responsive view instead of the desktop view.

### Discussion 14a 

Please discuss enabling this option for all wikis that did not change this option. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 05:07, 23 April 2026 (UTC)
 `{{ {{support}} }}` As proposer. Too many support questions were on this config. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 05:35, 23 April 2026 (UTC)
 `{{ {{support}} }}` [KockaAdmiralac](https://meta.miraheze.org/wiki/User:KockaAdmiralac) ([talk](https://meta.miraheze.org/wiki/User_talk:KockaAdmiralac)) 18:20, 23 April 2026 (UTC)
 `{{ {{neutral}} }}` I haven't really done much work with Vector 2022 so I can't tell how out of the way the setting is, but I feel like most of the above settings are for people who don't know what a managewiki is or people who aren't aware a certain thing can be customised. As far as I'm aware, this setting would only be necessary for people who've already configured stuff on ManageWiki since MobileFrontend is a default extension. [TheWWRNerdGuy](https://meta.miraheze.org/wiki/User:TheWWRNerdGuy) ([talk](https://meta.miraheze.org/wiki/User_talk:TheWWRNerdGuy)) 20:35, 23 April 2026 (UTC)
 `{{ {{Abstain}} }}` (( ... Skipping ... I feel there's a lot of potential here that can benefit a lot of users but this is out of my territory ...)) --- [Imamy](https://meta.miraheze.org/wiki/User:Imamy) ([talk](https://meta.miraheze.org/wiki/User_talk:Imamy)) 02:11, 25 April 2026 (UTC)
 `{{ {{support}} }}` In general skins should be responsive. [Harej](https://meta.miraheze.org/wiki/User:Harej) ([talk](https://meta.miraheze.org/wiki/User_talk:Harej)) 02:09, 1 May 2026 (UTC)
 `{{ {{Support}} }}` I wasn't even aware this wasn't default behavior. [Emiliers](https://meta.miraheze.org/wiki/User:Emiliers) ([talk](https://meta.miraheze.org/wiki/User_talk:Emiliers)) 19:03, 1 May 2026 (UTC)
 `{{ {{support}} }}` This should've been made an option by default anyways. --[DarkMatterMan4500](https://meta.miraheze.org/wiki/User:DarkMatterMan4500) ([talk](https://meta.miraheze.org/wiki/User_talk:DarkMatterMan4500)) ([contribs](https://meta.miraheze.org/wiki/Special:Contributions/DarkMatterMan4500)) 11:28, 4 May 2026 (UTC)
 `{{ {{support}} }}` as skins should be responsive per modern design ~ [Elisapoly](https://meta.miraheze.org/wiki/User:Elisapoly) ([talk](https://meta.miraheze.org/wiki/User_talk:Elisapoly)) 04:19, 10 May 2026 (UTC)
 `{{ {{Support}} }}` per PetraMagna. **[<span style="color:black;">O<small>BSIDIAN</small>G<small>UY</small></span>](https://meta.miraheze.org/wiki/User:ObsidianGuy) ([T](https://meta.miraheze.org/wiki/User_talk:ObsidianGuy)| [C](https://meta.miraheze.org/wiki/Special:Contributions/ObsidianGuy)| [G](https://meta.miraheze.org/wiki/Special:CentralAuth/ObsidianGuy))** 23:52, 21 May 2026 (UTC)

### Discussion 14b 

Please discuss enabling this option only for new wikis. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 05:07, 23 April 2026 (UTC)

 `{{ {{support|weak}} }}` Same rationale as 7b. This is more work for the tech team compared with 14a. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 05:37, 23 April 2026 (UTC)
 `{{ {{support|strongest}} }}` Responsive mode was a game changer when considering which skin to support, and why we initially went with Vector-2022, but it could drastically interfere with the CSS of wikis that didn't develop their CSS with it in mind, leading to unexpected breaking changes. - [JaneBuzJane](https://meta.miraheze.org/wiki/User:JaneBuzJane) ([talk](https://meta.miraheze.org/wiki/User_talk:JaneBuzJane)) 19:47, 23 April 2026 (UTC)
      I compared some wikis and it does seem like CSS is injected beyond the viewport change. The `skin--responsive` class changes the behavior of, for example, images with high width. These are in my opinion pretty light changes and I find them to be less intrusive than, for example, MobileFrontend making all images have `width: 100% !important` on mobile. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 00:10, 24 April 2026 (UTC)
         But if b gets similar levels of support than a I think to be safe we should implement b only. I would interpret supporter of 14a to support 14b as well, but the converse is not true since 14b supporters specifically don't want a change to apply to all wikis. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 00:16, 24 April 2026 (UTC)
 `{{ {{support}} }}` in particular with sway from Jane's input as moderately less intrusive, but feel free to interpret a weak support for 14a if it helps, as a change that leans for the net better. --**[raidarr](https://meta.miraheze.org/wiki/User:Raidarr)** **(** [💬](https://meta.miraheze.org/wiki/User_talk:Raidarr) **)** 00:58, 25 April 2026 (UTC)
 `{{ {{Oppose}} }}` (( I vote to apply to all or no wikis ... )) --- [Imamy](https://meta.miraheze.org/wiki/User:Imamy) ([talk](https://meta.miraheze.org/wiki/User_talk:Imamy)) 02:12, 25 April 2026 (UTC)
 `{{ {{support}} }}` In general skins should be responsive. [Harej](https://meta.miraheze.org/wiki/User:Harej) ([talk](https://meta.miraheze.org/wiki/User_talk:Harej)) 02:09, 1 May 2026 (UTC)
 `{{ {{support}} }}` per my comment above ~ [Elisapoly](https://meta.miraheze.org/wiki/User:Elisapoly) ([talk](https://meta.miraheze.org/wiki/User_talk:Elisapoly)) 04:19, 10 May 2026 (UTC)
 `{{ {{support|strongest}} }}` Per comments made by Elisapoly above, along with my additional support of having this enabled by default. --[DarkMatterMan4500](https://meta.miraheze.org/wiki/User:DarkMatterMan4500) ([talk](https://meta.miraheze.org/wiki/User_talk:DarkMatterMan4500)) ([contribs](https://meta.miraheze.org/wiki/Special:Contributions/DarkMatterMan4500)) 17:11, 16 May 2026 (UTC)

## Proposal 15: set $wgArticleCountMethod to 'any' 

```
{{ {{Discussion
|comment=Closing as {{done|successful}} per near-unanimous support. wgArticleCountMethod will be set to 'any' for all wikis except those that explicitly changed it at some point. [[User:PetraMagna|PetraMagna]] ([[User talk:PetraMagna|talk]]) 22:57, 6 May 2026 (UTC)
|1=
This was a suggestion of [[User:KockaAdmiralac]].

By default, whether a wiki page counts as an article depends on the presence of a link on that page. This has caused confusion in the past. Defaulting [[mw:Manual:$wgArticleCountMethod|$wgArticleCountMethod]] to <code>'any'</code>, which simply counts all pages in content namespaces, is a lot more intuitive.

=== Discussion 15a ===
Please discuss enabling this option for all wikis that did not change this option. [[User:PetraMagna|PetraMagna]] ([[User talk:PetraMagna|talk]]) 05:07, 23 April 2026 (UTC)

:{{support}} As proposer. Lots of support questions were asked on this setting. [[User:PetraMagna|PetraMagna]] ([[User talk:PetraMagna|talk]]) 05:38, 23 April 2026 (UTC)
:{{support}} [[User:KockaAdmiralac|KockaAdmiralac]] ([[User talk:KockaAdmiralac|talk]]) 18:21, 23 April 2026 (UTC)
:{{support}} per proposal. - [[User:JaneBuzJane|JaneBuzJane]] ([[User talk:JaneBuzJane|talk]]) 19:47, 23 April 2026 (UTC)
:{{support|weak}} I don't want to go too crazy with changing default settings, especially when it's something minor like article count, but this default is kinda insane. [[User:TheWWRNerdGuy|TheWWRNerdGuy]] ([[User talk:TheWWRNerdGuy|talk]]) 20:38, 23 April 2026 (UTC)
:{{support|weak}} To be [[mh:allthetropes:Brutal Honesty|brutally honest]], there's just so much work that needs to be done with this type of thing, so is it really a surprise to anyone at this point? --[[User:DarkMatterMan4500|DarkMatterMan4500]] ([[User talk:DarkMatterMan4500|talk]]) ([[Special:Contributions/DarkMatterMan4500|contribs]]) 15:38, 24 April 2026 (UTC)
:{{support}}, I would project that this change at worst would incur a few 'huhs' trickling in for the short term, while curing a large category of 'huh' across the long term. --'''[[User:Raidarr|raidarr]]''' '''('''[[User_talk:Raidarr|💬]]''')''' 01:00, 25 April 2026 (UTC)
:{{Support}} (( If it is more intuitive, I'll go for it ... )) --- [[User:Imamy|Imamy]] ([[User talk:Imamy|talk]]) 02:16, 25 April 2026 (UTC)
:{{Support}} More intuitive to people. [[User:Harej|Harej]] ([[User talk:Harej|talk]]) 02:09, 1 May 2026 (UTC)
:{{Support}} Sounds reasonable. [[User:Emiliers|Emiliers]] ([[User talk:Emiliers|talk]]) 21:29, 1 May 2026 (UTC)

=== Discussion 15b ===
Please discuss enabling this option only for new wikis. [[User:PetraMagna|PetraMagna]] ([[User talk:PetraMagna|talk]]) 05:07, 23 April 2026 (UTC)

:{{support}} There might be an interest in avoiding confusion caused by sudden jumps in article counts, which justifies more work for the tech team. [[User:PetraMagna|PetraMagna]] ([[User talk:PetraMagna|talk]]) 05:40, 23 April 2026 (UTC)
:{{support}} If it fits anyway. --[[User:DarkMatterMan4500|DarkMatterMan4500]] ([[User talk:DarkMatterMan4500|talk]]) ([[Special:Contributions/DarkMatterMan4500|contribs]]) 15:38, 24 April 2026 (UTC)
:{{oppose}} (( ... Change must apply to all or no wikis ... )) --- [[User:Imamy|Imamy]] ([[User talk:Imamy|talk]]) 02:17, 25 April 2026 (UTC)
:{{Support}} More intuitive to people. [[User:Harej|Harej]] ([[User talk:Harej|talk]]) 02:09, 1 May 2026 (UTC)

}} }}
```

## Proposal 16: set $wgDefaultUserOptions['showrollbackconfirmation'] to 1 

This was a suggestion of [User:KockaAdmiralac](https://meta.miraheze.org/wiki/User:KockaAdmiralac).

Accidental rollbacks have been a common occurrence. A preference to show a confirmation before rollbacking was added [7 years ago](https://meta.miraheze.org/wiki/wikimediaphab:T199537), but given a discussion earlier this month about accidental rollbacks in the Miraheze Discord server, it seems that there's relatively low awareness of this feature. Some Wikimedia wikis, such as the [German Wikipedia,](https://noc.wikimedia.org/wiki.php?wiki=dewiki#wmgShowRollbackConfirmationDefaultUserOptions) already enabled this option by default.

### Discussion 16a 

Discuss enabling this option for all users that did not change this option. [KockaAdmiralac](https://meta.miraheze.org/wiki/User:KockaAdmiralac) ([talk](https://meta.miraheze.org/wiki/User_talk:KockaAdmiralac)) 17:08, 23 April 2026 (UTC)
 `{{ {{support}} }}` As proposer. [KockaAdmiralac](https://meta.miraheze.org/wiki/User:KockaAdmiralac) ([talk](https://meta.miraheze.org/wiki/User_talk:KockaAdmiralac)) 17:08, 23 April 2026 (UTC)
 `{{ {{support}} }}` per proposal. - [JaneBuzJane](https://meta.miraheze.org/wiki/User:JaneBuzJane) ([talk](https://meta.miraheze.org/wiki/User_talk:JaneBuzJane)) 19:48, 23 April 2026 (UTC)
 `{{ {{support}} }}` as a user preference it can be globally disabled anyway so I have no issue with this. [TheWWRNerdGuy](https://meta.miraheze.org/wiki/User:TheWWRNerdGuy) ([talk](https://meta.miraheze.org/wiki/User_talk:TheWWRNerdGuy)) 20:48, 23 April 2026 (UTC)
 `{{ {{abstain}} }}` I personally don't find accidentally clicking the rollback button a problem, but I understand this may not be the case for other users, especially on mobile. [PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 23:43, 23 April 2026 (UTC)
 `{{ {{oppose}} }}` as the whole intent of rollback is to be as expeditious as possible, and we should maintain that default. I know that many people like having a confirmation (enough for MediaWiki to support this as an option), but that doesn't mean that `{{ {{tq|low awareness of this feature}} }}` justifies degrading what rollback is intended to accomplish. — [chrs](https://meta.miraheze.org/wiki/User:Chrs) ([talk](https://meta.miraheze.org/wiki/User_talk:Chrs)) 00:38, 24 April 2026 (UTC)
 `{{ {{support|strong}} }}` This honestly should've been a thing a long time ago, so I'll support this. --[DarkMatterMan4500](https://meta.miraheze.org/wiki/User:DarkMatterMan4500) ([talk](https://meta.miraheze.org/wiki/User_talk:DarkMatterMan4500)) ([contribs](https://meta.miraheze.org/wiki/Special:Contributions/DarkMatterMan4500)) 15:38, 24 April 2026 (UTC)
 `{{ {{support|weak}} }}`, if there is interface text pointing out this can be changed in user preference. If not I would recommend injecting some for clarity, and to account for the concern raised by Chrs. --**[raidarr](https://meta.miraheze.org/wiki/User:Raidarr)** **(** [💬](https://meta.miraheze.org/wiki/User_talk:Raidarr) **)** 01:02, 25 April 2026 (UTC)
 `{{ {{Oppose}} }}` ((I think fiddling with this feature at this point is going to create havoc or at least some form of discomfort ... ... ... There should be a way to help enable the confirmation without making it a default ... some people will prefer speed and some may not know how to change back the setting ... )) --- [Imamy](https://meta.miraheze.org/wiki/User:Imamy) ([talk](https://meta.miraheze.org/wiki/User_talk:Imamy)) 02:26, 25 April 2026 (UTC)
 `{{ {{Abstain}} }}` [Harej](https://meta.miraheze.org/wiki/User:Harej) ([talk](https://meta.miraheze.org/wiki/User_talk:Harej)) 02:09, 1 May 2026 (UTC)
 `{{ {{Support}} }}` I'll self-report -- I was one of those people who kept accidentally rollbacking and had to be told an option was available to add a confirmation. While I understand the desire for expedience, the time difference between clicking once vs clicking twice is negligible, while saving the rollbacker from massive amounts of potential embarrassment. A worthwhile trade, in my opinion. [Emiliers](https://meta.miraheze.org/wiki/User:Emiliers) ([talk](https://meta.miraheze.org/wiki/User_talk:Emiliers)) 19:09, 1 May 2026 (UTC)
 `{{ {{support}} }}` [ark](https://meta.miraheze.org/wiki/User:ark) ([talk](https://meta.miraheze.org/wiki/User_talk:ark)) 07:44, 3 May 2026 (UTC)


<!--No template, thanks in advance.-->

Hell no. Defeats the purpose of the rollback. &mdash;[<span style="color:green"><kbd>revi</kbd></span>](https://meta.miraheze.org/wiki/User:Revi) 10:13, 9 May 2026 (UTC)
 `{{ {{Support}} }}`. **[<span style="color:black;">O<small>BSIDIAN</small>G<small>UY</small></span>](https://meta.miraheze.org/wiki/User:ObsidianGuy) ([T](https://meta.miraheze.org/wiki/User_talk:ObsidianGuy)| [C](https://meta.miraheze.org/wiki/Special:Contributions/ObsidianGuy)| [G](https://meta.miraheze.org/wiki/Special:CentralAuth/ObsidianGuy))** 23:50, 21 May 2026 (UTC)

### Discussion 16b 

Discuss enabling this option only for new users. [KockaAdmiralac](https://meta.miraheze.org/wiki/User:KockaAdmiralac) ([talk](https://meta.miraheze.org/wiki/User_talk:KockaAdmiralac)) 17:08, 23 April 2026 (UTC)
 `{{ {{weak support}} }}` This is a bit more work and I feel like it would be useful for existing users who did not know about the feature as well. [KockaAdmiralac](https://meta.miraheze.org/wiki/User:KockaAdmiralac) ([talk](https://meta.miraheze.org/wiki/User_talk:KockaAdmiralac)) 17:08, 23 April 2026 (UTC)
 `{{ {{support|partial}} }}` As long as it benefits in the long-run? Well, you have my support. --[DarkMatterMan4500](https://meta.miraheze.org/wiki/User:DarkMatterMan4500) ([talk](https://meta.miraheze.org/wiki/User_talk:DarkMatterMan4500)) ([contribs](https://meta.miraheze.org/wiki/Special:Contributions/DarkMatterMan4500)) 15:38, 24 April 2026 (UTC)
 `{{ {{Oppose}} }}` ((I'm not really sure why this is necessary ... I'm of the opinion that it takes time to get good at using tools ... The confirmation option may be perfect for certain situations but if everyone has a different experience, it will make communication more difficult ... I always assume that what I experience is more or less shared by others but the way these proposals are going, it's like going out of our way to create potential for confusion and misunderstandings ... I would prefer to give the user the option to toggle between the states rather than deciding for the user ...)) --- [Imamy](https://meta.miraheze.org/wiki/User:Imamy) ([talk](https://meta.miraheze.org/wiki/User_talk:Imamy)) 02:32, 25 April 2026 (UTC)
 `{{ {{Abstain}} }}` [Harej](https://meta.miraheze.org/wiki/User:Harej) ([talk](https://meta.miraheze.org/wiki/User_talk:Harej)) 02:09, 1 May 2026 (UTC)

----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:Noticeboard/Request_for_feedback:_changes_to_default_MediaWiki_settings)**