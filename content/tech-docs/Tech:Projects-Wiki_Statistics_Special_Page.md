---
title: Tech:Projects/Wiki Statistics Special Page
---

This is a project proposal for adding a statistics page on all Miraheze wikis which allow users to view restricted analytical information for the wiki.

## Background 

Currently, Miraheze provides no analytical information to users about how many times a wiki is viewed, how many unique visitors there are to the wiki or what pages are considered popular based on viewing statistics. However, Miraheze does track (to a degree, inline with the [Privacy Policy](https://meta.miraheze.org/wiki/Privacy_Policy) and respecting DNT headers) which pages are read by users, how long for, which wiki, how they got there, and browsing/OS information. This is all collected by using [Piwik](https://meta.miraheze.org/wiki/Tech:Piwik) ([link](https://piwik.miraheze.org)) which is restricted to system administrators only.

It has been a [common theme among the community](https://meta.miraheze.org/wiki/phabricator:T680) that there needs to be some form of analytical information available on wikis and there is a shared opinion among system administrators that the information should be derived from Piwik.

## Plan 

### Special Page 

The visual aspect of the project should be delivered in the form of a special page that will be available on every wiki. The special page can be tabular and just a list of views per month for a set period of months, unique visitors per month and a list of the top 3 views pages on the wiki.

The access to the special page could be granular as well, with the assignment of a "view-analytics" user right that can be assigned to * by default, but wikis could revoke and assign the user right and therefore access to the page on their personal needs.

### Integration with Piwik 

Piwik provides an API that can be used to gather and collect the information by default. While the API requires a view-enabled account, API requests for wikis could be passed through an operations managed account with the access information passed to the extension through configuration variables.

There is currently a generalised site ID set up in Piwik where all wikis except allthetropeswiki have a shared site ID (1) and allthetropeswiki has site ID 2. If this becomes an issue with collating information from the API, it could be possible to have each wiki assigned a permanent and unique ID which can then be used to collect information from Piwik. The RemoteWiki class in MirahezeMagic could be adapted to provide this functionality.

## Requirements 

There may be changes that need to be made in Piwik to allow granulated collection of data for this project—pre-existing modules could be adapted and then locally installed by Miraheze to achieve this, and avoid upstream blocking of progress.

As Piwik is currently a restricted service, access, and testing requires someone from Miraheze Operations to be able to make progress on the project.

## Outcome Steps 

* A special page available on Miraheze wikis that shows the total number of views on a wiki either in recorded history or on a per monthly break down.
* A special page available on Miraheze wikis that shows the total number of unique visitors to the wiki on a per monthly break down.
* A special page that lists the most popular/viewed pages on the wiki by unique visitors - this would be an additional step and not a requirement to complete the project originally.

## Getting Started 

Anyone interested in starting this project should:
* Get familiar with how Piwik works and how its API can be used to collect views per page / views across a whole site.
* Get in touch with an [operations](https://meta.miraheze.org/wiki/Tech:Organisation#Team:_MediaWiki,_Site_Reliability_Engineering) member to discuss next steps for integrating with the current Piwik install.

----
**Source**: https://meta.miraheze.org/wiki/Tech:Projects/Wiki_Statistics_Special_Page