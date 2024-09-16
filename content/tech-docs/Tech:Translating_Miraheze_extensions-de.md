---
title: Tech:Translating Miraheze extensions/de
---


Miraheze entwickelt und pflegt ein paar Erweiterungen, zum Beispiel [CreateWiki](https://meta.miraheze.org/wiki/github:miraheze/CreateWiki) und [ManageWiki](https://meta.miraheze.org/wiki/github:miraheze/ManageWiki). Da Miraheze Nutzer hat, die kein oder nur wenig Englisch können, ist die Internationalisierung für die Nutzer wichtig.

Derzeit verwenden wir [translatewiki.net](https://meta.miraheze.org/wiki/translatewiki:) für CreateWiki und ManageWiki Übersetzungen.

## TranslateWiki Prozess 

* Strings in en.json hinzufügen
* Der Translatewiki.net-Bot zieht den Code, wenn er die Strings importiert, und er wird den Übersetzern zum Übersetzen angezeigt
* Die Übersetzer von Translatewiki.net übersetzen die Texte
* Der Translatewiki.net-Bot wird die $lang.json pushen, wenn der Export-Bot ausgeführt wird.
* Sie werden dann auf dem Miraheze-Cluster bereitgestellt (das Submodul muss aktualisiert werden)

[Category:Tech](https://meta.miraheze.org/wiki/Category:Tech)

----
**Source**: https://meta.miraheze.org/wiki/Tech:Translating_Miraheze_extensions/de