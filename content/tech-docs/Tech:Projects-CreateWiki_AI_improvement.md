---
title: Tech:Projects/CreateWiki AI improvement
---

This is a project proposal for the current AI system for CreateWiki to allow for different factors to be considered when assessing how 'good' a request is.

## Background 

Currently, all wiki requests are manually approved by wiki creators, but a score is given by the CreateWiki AI system. The current system only considers the description provided by users, but does not consider other factors (such as the reasons for the request being declined).

## Plan 

* Move the CreateWiki AI away from using PHP since it's not very suitable for PHP.
* Create a (private) blacklist that will cause the AI not to automatically approve any wikis that include certain words (regex) in their description.
* Not consider requests that are declined for duplicate or because the database already exists.
* Figure out a sensible way to integrate other approval/decline reasons in the AI's assessment.

(Any further steps necessary to perfect the AI system are welcome.)

## Requirements 

There are no external requirements and no blockers requiring additional help.

## Outcome Steps 

* Allowing for the blacklisting of words/regex where the AI will never fulfil a request if they match.
* Allowing the AI to take into account decline/approve reasons.

## Getting Started 

Anyone interested in starting this project should:
* get familiar with how the current CreateWiki AI works (see [the CreateWiki repo](https://github.com/miraheze/CreateWiki) for more details.
* get in touch with an [SRE](https://meta.miraheze.org/wiki/Tech:Organisation#Team:_MediaWiki,_Site_Reliability_Engineering) member to discuss how to proceed.

----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:Projects/CreateWiki_AI_improvement)**