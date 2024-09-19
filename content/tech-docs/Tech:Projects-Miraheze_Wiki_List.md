---
title: Tech:Projects/Miraheze Wiki List
---

```
{{ {{MessageBox
| type = notice
| Image = [[File:Yes check.svg|30px|link=]]
| Message text = This project has been completed! A new extension has been developed by [[User:John]]. You can use it at [[Special:WikiDiscover]].
| Background color =#D3D3D3
| Border color =black
| Flag color =black
}} }}
```

This is a proposal for a replacement of [SiteMatrix](https://meta.miraheze.org/wiki/Special:SiteMatrix) with a new page that serves the same purpose and extends scope and abilities for Miraheze.

## Background 

The current SiteMatrix page is built for Wikimedia - it separates all listed wikis into projects and languages of which Miraheze doesn't do. All wikis Miraheze has displays in a single list at the bottom of the page which makes it extremely unfriendly.

## Plan 

### Special Page 

The extension will mostly be an additional special page (could be at the currently used Special:SiteMatrix) that should:
* split projects up between our two categories (public and private),
* clearly display closed wikis (strike through, closed tag, grey out? presentation is up for debate).

In addition the page could:
* display a random open and public wiki to suggest to someone to look at,
* rank wikis by most pages, most recent edits, most active users, most page views (links into [another proposal](/tech-docs/techprojects-wiki_statistics_special_page)).

### API 

Like the current extension, there should be an accessible [API](https://meta.miraheze.org/w/api.php?action=sitematrix). The API should match the current useful information available (wiki name, database name, open/closed, private/public, language) but should then further extend by include the full URL of the wiki (useful for custom domains), date of creation, any statistics implemented above and/or ranking information implemented above.

As soon as the current SiteMatrix abilities are implemented into our own extension, it should be initially deployed. Experimental changes can be deployed to extloadwiki prior to full deployment.

## Requirements 

There are no external requirements and no blockers requiring additional help.

## Outcome Steps 

* A special page on all wikis that lists every wiki split up by their status (open, closed) and availability (public, private).
* A special page should be on all wikis that ranks wikis by statistics IF those capabilities exist at the time. If not, this becomes a wishlist and not an outcome.
* A special page that can list all wikis of a particular language.
* An API that meets or supersedes the current SiteMatrix API.

## Getting Started 

Anyone interested in this project should:
* register their interest at the [phorge ticket](https://meta.miraheze.org/wiki/phorge:T218),
* discuss a possible timeline/integration plan with a [mw-admin](/tech-docs/techorganization#mediawiki-specialist) or [operations](/tech-docs/techorganization#infrastructure-specialist) member.



----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:Projects/Miraheze_Wiki_List)**