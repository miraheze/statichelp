---
title: Tech:Translating Miraheze extensions/hi
---


Miraheze कुछ एक्सटेंशनों को विकसित कर और अनुरक्षित करता है, जैसे [CreateWiki](https://meta.miraheze.org/wiki/github:miraheze/CreateWiki) और [ManageWiki](https://meta.miraheze.org/wiki/github:miraheze/ManageWiki)। क्योंकि Miraheze पर अंग्रेज़ी थोड़ी-सी ही या फिर बिलकुल न जानने वाले सदस्य भी हैं, अंतर्राष्ट्रीयकरण ऐसे सदस्यों के लिए आवश्यक है।

वर्तमान में CreateWiki और ManageWiki के अनुवादों के लिए Miraheze [translatewiki.net](https://meta.miraheze.org/wiki/translatewiki:) का इस्तेमाल करता है।

## TranslateWiki की कार्यविधि 

* en.json में स्ट्रिंग्स जोड़ें।
* Translatewiki.net का बॉट, स्ट्रिंग्स को आयात करने पर कोड को पुल करेगा और वे अनुवादकों को अनुवाद के लिए दिखाए जाएँगे।
* Translatewiki.net पर अनुवादक टेक्स्ट को अनुवादित करते हैं।
* निर्यात बॉट को चलाने पर Translatewiki.net का बॉट $lang.json को पुश कर देगा।
* फिर उन्हें Miraheze क्लस्टर पर तैनात किया जाता है (सबमॉड्यूल को अद्यत होना चाहिए)।

## Categories

* [Category:Tech](https://meta.miraheze.org/wiki/Category:Tech)



----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:Translating_Miraheze_extensions/hi)**