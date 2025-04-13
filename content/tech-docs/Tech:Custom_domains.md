---
title: Tech:Custom domains
---

Domain setup can be completed by anybody with access to the Cloudflare account (ops and ssl-admins). Initially the domain will show a Cloudflare error page if it hasn't been setup yet.

```
{{ {{MessageBox
|Flag color=firebrick
|Border color=firebrick
|Background color=#FEE
|Image=[[File:OOjs_UI_icon_notice-destructive.svg|40px|link=]]
|Message text=Always make sure that a domain is properly pointed before setting it up. If a domain is setup without it being pointed, the target wiki will become inaccessible. If you visit the domain, you should get a Cloudflare error page. Otherwise, if you add the custom hostnames in Cloudflare, you will see a big red error box when you check the domain status.
}} }}
```

1. Login to Cloudflare and select the WikiTide Foundation account on the dashboard.

2. Navigate to Websites -> miraheze.org -> SSL/TLS -> Custom Hostnames

3. Click the "Add Custom Hostname" button.

4. Enter in the following values

* Custom Hostname: This is the domain that you are setting up
* Minimum TLS version: 1.3
* Certificate type: Leave this on the default (Provided by Cloudflare)
* Certificate validation method: HTTP Validation

5. Once again, click "Add Custom Hostname"

6. Within a few minutes an SSL certificate will be issued. The domain will show the Miraheze landing page.

7. You need to add the domain to certs.yaml in the SSL repo. For formatting and values, go off of the previous entries in that file.

8. Once the SSL change is deployed, the domain will show the Wiki not Found page. At this point, you can set the domain in ManageWiki, and you are done.

## Categories

* [Category:Guides for sysadmins](https://meta.miraheze.org/wiki/Category:Guides_for_sysadmins)

----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:Custom_domains)**