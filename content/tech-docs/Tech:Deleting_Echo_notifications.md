---
title: Tech:Deleting Echo notifications
---

While quite a rare occurrence, it sometimes happens that a user is left with global Echo notifications from wikis that are either now private or have been deleted. There is currently no other method to get rid of them globally, so this method must be used in order to remove the notification for the user.

* Select the `mhglobal` database
* Run `SELECT gu_id FROM globaluser WHERE gu_name = '[USERNAME]';`
* Select the `metawiki` database
* Run `DELETE FROM echo_unread_wikis WHERE euw_user = '[RESULT FROM PREVIOUS QUERY]' AND euw_wiki = '[desired wiki]';`
* Select the local wiki database
* Run `SELECT user_id FROM user WHERE user_name = '[USERNAME]';`
* Run <code>UPDATE echo_notification SET notification_read_timestamp="[SOME TIMESTAMP PRIOR TO NOW]" WHERE notification_read_timestamp IS NULL AND notification_user=[RESULT FROM PREVIOUS QUERY];

## Categories

* [Category:Technology guidelines and guides](https://meta.miraheze.org/wiki/Category:Technology_guidelines_and_guides)

----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:Deleting_Echo_notifications)**