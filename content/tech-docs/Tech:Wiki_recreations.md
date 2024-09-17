---
title: Tech:Wiki recreations
---

`{{ {{SRE navigation|noticeboard|header=Wiki recreations following database outage|description=A recent database outage affected many wikis and now bureaucrat action is required to decide what course of action to take. Learn more on Miraheze Meta.|keywords=miraheze recreate wiki}} }}`

In November and December, 2022, the cloud server hosting a database, </code>db141</code>, went offline due to disk/corruption issues. We have been able to restore almost all wikis affected in the November crash and have recreated all wikis affected by the December crash. We have restored all content on public wikis (beginning with the letter A to O) affected by the December crash.

See [Tech:SRE noticeboard](https://meta.miraheze.org/wiki/Tech:SRE_noticeboard) for more information.

## FAQ 

### What happened? 

See [Tech:SRE noticeboard#What happened?](https://meta.miraheze.org/wiki/Tech:SRE_noticeboard#What_happened?) for details.

### My wiki (created after November 16) has been recreated but I don't see any edits, why? 

All public wikis created after November 16 which were on `db141` and between the letters A to O have had their content restored. If your wiki is in this category and your edits have not been reimported, please [contact us](https://meta.miraheze.org/wiki/Help_center).

### My wiki still displays a "Wiki temporarily unavailable" screen, why? 

It may be due to one of two reasons:
* **Your wiki was affected by database corruption** - A few wikis (initially 19, now down to 2) were affected by database corruption. If that's the case, [you will find your wiki listed here](https://meta.miraheze.org/wiki/phab:P475) (all 19 of the original wikis affected are listed here). We are working to bring back affected wikis and have brought most wikis back online.
* **This is a bug** - If your wiki is not on the list linked above, it is likely due to a bug as all wikis have been recreated. Please [contact us](https://meta.miraheze.org/wiki/Help_center) if that is the case.

### I am not bureaucrat on my wiki, why? 

This is likely due to a bug. Please file a request at [Stewards' noticeboard#Administrator/Bureaucrat access](https://meta.miraheze.org/wiki/Stewards'_noticeboard#Administrator/Bureaucrat_access) asking that you be repromoted. At this moment, we are only processing requests from the original wiki requester.

----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:Wiki_recreations)**