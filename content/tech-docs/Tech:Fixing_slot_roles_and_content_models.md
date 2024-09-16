---
title: Tech:Fixing slot roles and content models
---

After a wiki is recreated it will often give a `NameTableAccessException` or `RevisionAccessException`, sometimes hours after the recreation. To fix this, you may need to manually run some SQL or PHP commands to insert the data. The following commands may need ran (in order):

```sql
INSERT INTO slot_roles (role_id, role_name) VALUES (1, 'main');
INSERT INTO content_models (model_id, model_name) VALUES (1, 'wikitext');
INSERT INTO content_models (model_id, model_name) VALUES (2, 'css');
INSERT INTO content_models (model_id, model_name) VALUES (3, 'javascript');
INSERT INTO content_models (model_id, model_name) VALUES (4, 'Scribunto');
INSERT INTO content_models (model_id, model_name) VALUES (5, 'json');
```

You can also use shell.php and run (in order):
```php
MediaWiki\MediaWikiServices::getInstance()->getSlotRoleStore()->acquireId( 'main' );
MediaWiki\MediaWikiServices::getInstance()->getContentModelStore()->acquireId( 'wikitext' );
MediaWiki\MediaWikiServices::getInstance()->getContentModelStore()->acquireId( 'css' );
MediaWiki\MediaWikiServices::getInstance()->getContentModelStore()->acquireId( 'javascript' );
MediaWiki\MediaWikiServices::getInstance()->getContentModelStore()->acquireId( 'Scribunto' );
MediaWiki\MediaWikiServices::getInstance()->getContentModelStore()->acquireId( 'json' );
```

Repeat for any others needed such as potentially sanitized-css.

If the order somehow goes wrong from what matches in the content table you can try different orders/ids by running:
```sql
DELETE FROM content_models;
ALTER TABLE content_models AUTO_INCREMENT = 1;
```
After running that make sure you exit shell.php or sql.php (if using) and rerun or it won't know of the AUTO_INCREMENT being reset and IDs will still be wrong.

[Category:Tech](https://meta.miraheze.org/wiki/Category:Tech)
[Category:Technology guidelines and guides](https://meta.miraheze.org/wiki/Category:Technology_guidelines_and_guides)

----
**Source**: https://meta.miraheze.org/wiki/Tech:Fixing_slot_roles_and_content_models