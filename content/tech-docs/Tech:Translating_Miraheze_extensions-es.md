---
title: Tech:Translating Miraheze extensions/es
---


Miraheze desarrolla y mantiene ciertas extensiones, por ejemplo [CreateWiki](https://meta.miraheze.org/wiki/github:miraheze/CreateWiki) y [ManageWiki](https://meta.miraheze.org/wiki/github:miraheze/ManageWiki). Miraheze al poseer usuarios con o sin ningún conocimiento en inglés, es importante la internacionalización de las extensiones para los usuarios.

Actualmente, usamos [translatewiki.net](https://meta.miraheze.org/wiki/translatewiki:) para las traducciones de CreateWiki y ManageWiki.

## Proceso de TranslateWiki 

* Añadir cadenas en en.json
* El bot de Translatewiki.net extraerá el código cuando importen las cadenas, y se mostrará a los traductores para traducir.
* Los traductores en Translatewiki.net traducen los textos
* El bot de Translatewiki.net presionará $lang.json cuando se ejecuta el bot exportador
* Luego se implementará en el clúster de Miraheze (el submódulo debe de actualizarse)

[Category:Tech](https://meta.miraheze.org/wiki/Category:Tech)

----
**Source**: https://meta.miraheze.org/wiki/Tech:Translating_Miraheze_extensions/es