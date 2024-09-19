---
title: Tech:Deleting and moving batches of pages on a wiki
---

`{{ {{shortcut|[[Tech:DELETEBATCH]]|[[Tech:MOVEBATCH]]}} }}`

To delete or move large batches of pages on a wiki, execute the following commands for the `deleteBatch.php` and `moveBatch.php` [MediaWiki](https://meta.miraheze.org/wiki/MediaWiki) maintenance scripts in the following sequence:

* Login to `mwtask181` (active maintenance server).
* Upload a text file, named as *subdomain.txt*, ideally, to your shell folder, which contains the list of pages for deletion or moving (include the namespace, where applicable!), replacing the *italicized* portions as applicable.
* Run `sudo -u www-data php /srv/mediawiki/w/maintenance/deleteBatch.php --wiki=wikidbname -u "Miraheze maintenance script" -r "[[phab:T###|Requested]]" /home/yourshellusername/wikisubdomain.txt`, replacing the ***bolded and italicized*** portions as applicable. **Note:** *`deleteBatch.php`* is interchangeable with *`moveBatch.php`* as applicable.
* sudo `sudo -u www-data php /srv/mediawiki/w/maintenance/deleteBatch.php --wiki=wikidbname -u "Miraheze maintenance script" -r "[[phab:T###|Requested]]" /home/yourshellusername/wikisubdomain.txt`, replacing the ***bolded italicized*** portions as applicable. **Note:** *`deleteBatch.php`* is interchangeable with *`moveBatch.php`* as applicable.
* Logout (if you are done with your business on `mwtask181`).

## Categories

* [Category:Technology guidelines and guides](https://meta.miraheze.org/wiki/Category:Technology_guidelines_and_guides)



----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:Deleting_and_moving_batches_of_pages_on_a_wiki)**