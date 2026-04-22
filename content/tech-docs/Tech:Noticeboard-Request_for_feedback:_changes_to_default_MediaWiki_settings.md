---
title: Tech:Noticeboard/Request for feedback: changes to default MediaWiki settings
---

`{{ {{Mbox|text=This page is a draft. Please feel free to edit or give feedback, but do not start voting yet.}} }}`

I am proposing several changes to Miraheze's default MediaWiki configuration. This page will gather community feedback for the Technology Team's consideration. Proposals that are well-received by both the community and the Tech Team will be actioned.

[PetraMagna](https://meta.miraheze.org/wiki/User:PetraMagna) ([talk](https://meta.miraheze.org/wiki/User_talk:PetraMagna)) 07:15, 21 April 2026 (UTC)

## Proposal 1: add Gadgets to default extensions 

**[Gadgets](https://meta.miraheze.org/wiki/mw:Extension:Gadgets)** makes managing CSS and JavaScript tooling a lot easier. It is widely used on other hosts and doesn't add extraneous buttons for wikis that don't use it.

## Proposal 2: do not enable CologneBlue and Modern for new wikis 

Both **[CologneBlue](https://meta.miraheze.org/wiki/mw:Skin:CologneBlue)** and **[Modern](https://meta.miraheze.org/wiki/mw:Skin:Modern)** are old skins which rarely see usage. We demoted them from being globally enabled skins, but they are still enabled by default. The logical next step is to make these skins opt-in instead of opt-out on new wikis.

## Proposal 3: remove CiteThisPage from default extensions 

**[CiteThisPage](https://meta.miraheze.org/wiki/mw:Extension:CiteThisPage)** adds an additional link on the sidebar. The link is frequently abused by bots and crawlers, and they clutter the interface. The Purge extension also adds a sidebar button, but the button is useful enough to warrant exclusion from this proposal.

CiteThisPage is rarely used except for the few wikis that serve citable content in an academic context. As such, we should not let this extension take up valuable space on every page of each wiki and instead let wikis that need it opt in.

## Proposal 4: remove URL Shortener from default extensions 

**[UrlShortener](https://meta.miraheze.org/wiki/mw:Extension:UrlShortener)** has similar ratioanles as CiteThisPage. The extension might be more useful since getting a short URL is a common need. However, I have rarely (if ever) seen users post shortened URLs to their wiki, both on the official Miraheze Discord and on local wiki chats.

## Proposal 5: add PageImages to default extensions 

The popularity of **[PageImages](https://meta.miraheze.org/wiki/mw:Extension:PageImages)** can be seen from the long list of farms and distributions using it on [the mediawiki.org page](https://meta.miraheze.org/wiki/mw:Extension:PageImages#See_also), in addition to the WMF using it on their wikis. PageImages provides an automated mechanism for choosing an image preview, which is not perfect but works well enough for most common use cases and warrants its inclusion in every new wiki.

## Proposal 6: add Popups to default extensions 

**[Popups](https://meta.miraheze.org/wiki/mw:Extension:Popups)**, which depends on PageImages and requires proposal 5 to pass, provides a convenient preview of an article's text and image when the user hovers over a link. This is a standard feature on other hosts, so users would expect preview popups to be the default behavior.

This proposal could be more controversial than the rest because it modifies MediaWiki's default behavior. However, I believe this change is largely in the positive direction.

## Proposal 7: disable wgRestrictDisplayTitle for new wikis 

[$wgRestrictDisplayTitle](https://meta.miraheze.org/wiki/mw:Manual:$wgRestrictDisplayTitle) controls whether the `{{DISPLAYTITLE}}` magic word can make non-trivial changes to the page's displayed title. Setting it to `true` stems from the WMF's paranoid security model. This setting has caused lots of inconvenience in the form of support questions without much security benefits. For example, a malicious user can simply move a page to a bad title, which circumvents DisplayTitle restrictions entirely.

This change can either apply to all wikis that did not set this variable explicitly or only to new wikis. I lean toward changing this for all wikis because it's easier to implement.

## Proposal 8: enable wgNativeImageLazyLoading 

Enabling [$wgNativeImageLazyLoading](https://meta.miraheze.org/wiki/mw:Manual:$wgNativeImageLazyLoading) is mostly motivated by seeing wikis with hundreds of images per page complain about getting blocked by Cloudflare due to rate limiting. For example, [https://webkinzguide.com/wiki/Blue_Clothing_Collection](https://webkinzguide.com/wiki/Blue_Clothing_Collection) makes close to 1,000 requests to the server after I open the page. This short burst of requests is unnecessary because most of them are done for images that are not needed immediately.

Lazy loading is generally considered a net positive for user experience even for wikis with less images. I looked at wiki.gg and Weird Gloop, and both hosts use lazy loading.

I have found edge cases where this feature negatively impacts user experience. For example, on [https://strinova.org/wiki/Michele/gallery](https://strinova.org/wiki/Michele/gallery), the tabbing JavaScript does not handle lazy-loading well: clicking on a tab leads to a short delay in image loading. By enabling lazy loading we might hurt a small subset of wikis. However, mitigations for the tabbing problem exist, and I think lazy loading improves user experience overall.

This change can either apply to all wikis that did not set this variable explicitly or only to new wikis. I lean toward changing this for all wikis because it's easier to implement. Plus, many existing wikis are affected by the excessive number of images on a page but don't know about this option.

## Proposal 9: add InputBox to default extensions 

Many new users don't know how to create a wiki page. To address this, the default main page for new wikis recommend enabling CreatePage or CreatePageUw. This is not necessary if **[InputBox](https://meta.miraheze.org/wiki/mw:Extension:InputBox)** is enabled: we can simply add a page creation input box to the main page. The user enters a page title and is taken to the editing interface to create the corresponding page. This improves the new wiki experience, and if the wiki does not need the functionalities of this extension, InputBox stays out of the way.

Note that InputBox's benefits apply only to the main page of new wikis, though it has many other uses and is [deployed on many other wiki hosts](https://meta.miraheze.org/wiki/mw:Extension:InputBox#See_also).

## Proposal 10: add VisualEditor to default extensions 

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

## Proposal 11: add Linter and DiscussionTools to default extensions 

**[DiscussionTools](https://meta.miraheze.org/wiki/mw:Extension:DiscussionTools)** is one of my main motivations to enable VisualEditor by default. It makes on-wiki discussions much easier and handles signatures which new users find unintuitive.

**[Linter](https://meta.miraheze.org/wiki/mw:Extension:Linter)** is a required extension for DiscussionTools, so it will be enabled by default as well if this proposal passes.

----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:Noticeboard/Request_for_feedback:_changes_to_default_MediaWiki_settings)**