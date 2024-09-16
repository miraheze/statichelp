---
title: Tech:Translating Miraheze extensions/bn
---


Miraheze কয়েকটি এক্সটেনশন বিকাশ ও পরিচালনা করে, উদাহরণস্বরূপ [CreateWiki](https://meta.miraheze.org/wiki/github:miraheze/CreateWiki) এবং [ManageWiki](https://meta.miraheze.org/wiki/github:miraheze/ManageWiki)। Miraheze-এ যেহেতু ইংরেজির অল্প জ্ঞান আছে বা কোন জ্ঞানই নেই এমন ব্যবহারকারীরা রয়েছেন, তাই ব্যবহারকারীদের জন্য আন্তর্জাতিকীকরণ খুব গুরুত্বপূর্ণ।

বর্তমানে আমরা CreateWiki এবং ManageWiki অনুবাদ করার জন্য [transtewiki.net](https://meta.miraheze.org/wiki/translatewiki:) ব্যবহার করি।

## TranslateWiki প্রক্রিয়া 

* en.json-এ স্ট্রিং যোগ করুন
* Translatewiki.net বট কোডগুলি টানবে যখন তারা স্ট্রিংগুলি আমদানি করবে এবং অনুবাদের জন্য এটি অনুবাদকদের কাছে প্রদর্শিত হবে
* Translatewiki.net অনুবাদকগণ পাঠ্য অনুবাদ করেন
* যখন রফতানি বট চালানো হয়, Translatewiki.net বটটি $lang.json পাঠিয়ে দিবে
* তারপরে এগুলি Miraheze ক্লাস্টারে স্থাপন করা হয় (সাবমডিউলটি অবশ্যই আগে আপডেট করতে হবে)

## Categories

* [Category:Tech](https://meta.miraheze.org/wiki/Category:Tech)

----
**Source**: [https://meta.miraheze.org/wiki/Tech:Translating_Miraheze_extensions/bn](https://meta.miraheze.org/wiki/Tech:Translating_Miraheze_extensions/bn)