---
title: Tech:Unattached local account
---

Local accounts not attached to any global accounts are pretty obvious. Users will be unable to sign in to wikis where their local account is not attached to their global account, and will get messages like "The supplied credentials cannot be changed, as nothing would use them". Additionally, this local account will not appear on the user's CentralAuth page, and if you go to said local account's Special:Contributions page, you will not see the global account link.

## Confirming for sure

Connect to the mhglobal database, and run `SELECT * FROM localnames WHERE ln_name="Example";`, replacing Example for the username of the user. You will get a list of wikis where that user has a global account, like this one:

```
MariaDB [mhglobal]> SELECT * FROM localnames WHERE ln_name="Alex (Miraheze)";
+-----------------------+-----------------+
| ln_wiki               | ln_name         |
+-----------------------+-----------------+
| characterclashwiki    | Alex (Miraheze) |
| hebwiki               | Alex (Miraheze) |
| indomitawiki          | Alex (Miraheze) |
| kylariswiki           | Alex (Miraheze) |
| lemmingmediawikiwiki  | Alex (Miraheze) |
| loginwiki             | Alex (Miraheze) |
| maksiorudziawiki      | Alex (Miraheze) |
| metawiki              | Alex (Miraheze) |
| onsecwiki             | Alex (Miraheze) |
| rainversewiki         | Alex (Miraheze) |
| staffwiki             | Alex (Miraheze) |
| sublimelibrarywiki    | Alex (Miraheze) |
| themagnusarchiveswiki | Alex (Miraheze) |
+-----------------------+-----------------+
```

Now enter the database for the wiki where there's a suspected unattached local account. Run a query like `SELECT user_name, user_id FROM user WHERE user_name="Example";`. If you get a result and the wiki is not listed on the previous query we made on the mhglobal database's localnames table, then there's a confirmed unattached local account.

## Fixing it

### Less hackily 

Execute the following line of code (works on the wiki with the unattached account, though it works elsewhere as well):
```php
MediaWiki\Extension\CentralAuth\User\CentralAuthUser::getInstance( User::newFromName( 'Username' ) )->attach( 'databasenamewiki', 'admin' );
```

(`admin` here means that the account was attached by an admin, see [CentralAuthUser#attach()](https://gerrit.wikimedia.org/r/plugins/gitiles/mediawiki/extensions/CentralAuth/+/2500cb0a91eb7cf0ec70de8adbeda7832105c812/includes/User/CentralAuthUser.php#2269) for details)

### Hackily 

* Insert the wiki-username pair on the localnames table in mhglobal, with a query like `INSERT INTO localnames(ln_wiki, ln_name) VALUES ("metawiki", "Example");`, with the correct database name and username. At this point, if you go to that user's Special:CentralAuth page, you will see CentralAuth recognizes there's an unattached local account.
* Run the `attachAccount.php` maintenance script from CentralAuth on an mwtask server. You'll have to create a text file with just the username of that user in a single line. Run it like `mwscript extensions/CentralAuth/attachAccount.php earferanawiki --userlist=/home/alex/InternetArchiveBot.txt`. You should see the following output:

```
CentralAuth account attach for: InternetArchiveBot
ATTACHING: InternetArchiveBot@scruffwiki
[2024-10-13 13:34:14] processed: 1 (2.4/sec); ok: 0 (0.0%); attached: 1 (100.0%); partial: 0 (0.0%); failed: 0 (0.0%); missing: 0 (0.0%);
done.
```

Once that's done, the user will be able to login as normal, and you should see this account listed on Special:CentralAuth.

## Categories

* [Category:Guides for sysadmins](https://meta.miraheze.org/wiki/Category:Guides_for_sysadmins)

----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:Unattached_local_account)**