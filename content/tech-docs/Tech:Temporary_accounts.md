---
title: Tech:Temporary accounts
---

`{{ {{Mbox|text=This page is a draft and does '''not''' reflect Miraheze's current technical setup.}} }}`

[Temporary account](https://meta.miraheze.org/wiki/mw:Help:Temporary_accounts) is a new feature in MediaWiki that improves upon IP editing. After enabling temporary accounts, new anonymous edits will automatically result in the creation of a temporary account without revealing the editor's IP. It preserves the privacy of anons without requiring account creation to edit.

See [the help page on mediawiki.org](https://meta.miraheze.org/wiki/mw:Help:Temporary_accounts) for more information.

## Enabling temporary accounts 

### Prerequisites 

The request must be made by a bureaucrat of the local wiki, with the understanding that many extensions may be incompatible with temporary accounts and might cause problems on the wiki in question. See [T15186](https://meta.miraheze.org/wiki/phab:T15186) for the current progress of extension testing on temporary accounts.

The wiki should ideally:
* Have a decent amount of editing activity from new users so that there will be attempts at creating temporary accounts. For example, if IP editing is enabled, the wiki should have at least a few IP edits per month.
* Have at least 2 users who are actively patrolling changes on the wiki. The [Counter Vandalism Team](https://meta.miraheze.org/wiki/Counter_Vandalism_Team) is interested in knowing whether temporary accounts present difficulties when combating vandalism.

### Request enabling temporary accounts

Please send a request on [SR/RC](https://meta.miraheze.org/wiki/SR/RC) with the following text attached:
```
I am aware that temporary accounts may be incompatible with extensions on my wiki and may cause the wiki to malfunction. I accept the risk and am still willing to enable temporary accounts.
```

## Testing extensions 

An extension that was written before temporary accounts existed may break, or it may treat temporary users the wrong way. If an extension your wiki is using is not checked on [T15186](https://meta.miraheze.org/wiki/phab:T15186), you are recommended to test this extension on your wiki after temporary accounts are enabled to ensure that new users will not encounter any issues.

### Before you start 

* Use a private or incognito window so you are fully logged out. To start again as a new visitor, close the private window and open a new one.
* Make sure logged-out users are actually allowed to use the feature you are testing. Many extensions by default only let logged-in users perform an action in question, such as commenting or voting.
* You will know you have a temporary account when your username starts with `~` followed by some numbers.
* If the wiki refuses to create a temporary account because too many were created recently, wait for a while or try from a different network.

### What to test 

* **Account creation**. Perform an action supported by the extension (comment, vote, etc.) while logged-out and see if it leads to successful account creation. For example, in a commenting extension, try to create a comment as an anon. The extension should create a temporary account for this user. It should not throw an error.
* **No IP addresses shown anywhere**. After performing the action in question, check whether the IP address is shown anywhere (e.g. as the author of a comment). Only the temporary user name should be shown. Displaying user IPs after temporary accounts are enabled is considered a privacy leak.
* **Temporary accounts are not treated like full accounts**. While using a temporary account, extensions should not try to persist user preferences on the server. Temporary accounts are meant to be transient, so preferences are stored on the local browser. A broken extension will try to send user preferences to the server and fail, resulting in its inability to remember user choices and generating error logs in the browser console.
* **Temporary account linked correctly**. Temporary accounts should not have user pages. Links to the account should lead straight to the `Special:Contributions` page just like IPs. They should not lead to `User:` pages.
* **None of the above**. Some extensions such as [ParserFunctions](https://meta.miraheze.org/wiki/mw:Extension:ParserFunctions) are unrelated to temporary accounts in any way and do not need to be tested. However, please be aware that extensions may have poorly-documented niche features that interact with temporary accounts in unforeseen ways.

If you do find a bug, please report on [Phorge](https://meta.miraheze.org/wiki/Phorge) by creating a new task. If an extension is compatible with temporary accounts after testing, please report your success by commenting on [T15186](https://meta.miraheze.org/wiki/phab:T15186).

----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:Temporary_accounts)**