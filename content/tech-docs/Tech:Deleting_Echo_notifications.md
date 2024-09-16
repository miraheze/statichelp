---
title: Tech:Deleting Echo notifications
---

While quite a rare occurrence, it sometimes happens that a user is left with global Echo notifications from wikis that are either now private or have been deleted. There is currently no other method to get rid of them globally, so this method must be used in order to remove the notification for the user.

* Select the `mhglobal` database
* Run `SELECT gu_id FROM globaluser WHERE gu_name = '[USERNAME]';`
* Select the `metawiki` database
* Run `DELETE FROM echo_unread_wikis WHERE euw_user = '[RESULT FROM PREVIOUS QUERY]' AND euw_wiki = '[desired wiki]';`

## Categories

* [Category:Technology guidelines and guides](https://meta.miraheze.org/wiki/Category:Technology_guidelines_and_guides)

----
**Source**: [https://meta.miraheze.org/wiki/Tech:Deleting_Echo_notifications](https://meta.miraheze.org/wiki/Tech:Deleting_Echo_notifications)