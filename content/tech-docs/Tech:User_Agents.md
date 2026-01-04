---
title: Tech:User Agents
---

If you are operating a bot, you must follow the rules below when setting a user agent. Failure to do so will likely result in you being rate-limited or blocked. This may affect your entire network without warning. The technology team deploys many methods to target abuse and utilise automated and manual actions.

Please note that additional restrictions may also apply. You should not make requests at an excessive rate.

## Rules 

* Your user agent must not mimic a browser UA
* You must include contact details (either a clearly marked User name or email)

## Examples 

Directly sending a request with python's `requests` library will result in the request getting rejected.
```python
requests.get("https://meta.miraheze.org/w/api.php")
```

Requests that explicitly define the contact information will succeed:
```python
requests.get(
    "https://meta.miraheze.org/w/api.php?action=query&meta=siteinfo&format=json", 
	headers={"user-agent": "Test bot by User:<username>"}
)
```

----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:User_Agents)**