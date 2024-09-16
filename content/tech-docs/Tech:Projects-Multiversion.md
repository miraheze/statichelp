---
title: Tech:Projects/Multiversion
---

```
{{ {{MessageBox
| type = notice
| Image = [[File:Yes check.svg|30px|link=]]
| Message text = This project has been completed by [[User:Universal Omega|Universal Omega]]!
| Background color = #D3D3D3
| Border color = black
| Flag color = black
}} }}
```

This is a project proposal to introduce the ability to deploy multiple MediaWiki versions to one server.

## Background 

Currently, only one version of MediaWiki can be deployed to one server. By allowing for multiple versions to exist on a server, the impact of minor upgrades can be reduced. In addition, wikis may opt in to be 'experimental wikis' and get updates beforehand so that we can assure there are no issues.

## Plan 

* Introduce puppet variables to change where MediaWiki is installed and where the repository is called from
* Introduce a new repository for storing the mediawiki versions in submodules
* Develop a prep script that sysadmins can run every wiki to update the modules
* Develop the multiversion logic to map wiki to version
* Develop maintenance script wrapper for sysadmins
* Upgrade the deploy tool so it can handle each version

## Requirements 

There are no external requirements and no blockers requiring additional help.

## Outcome Steps 

* Allowing multiple MediaWiki versions to be deployed on a single server

## Getting Started 

Anyone interested in starting this project should:
* get familiar with how we currently do MediaWiki updates
* get in touch with an [SRE](https://meta.miraheze.org/wiki/Tech:Organisation#Team:_MediaWiki,_Site_Reliability_Engineering) member to discuss how to proceed

----
**Source**: [https://meta.miraheze.org/wiki/Tech:Projects/Multiversion](https://meta.miraheze.org/wiki/Tech:Projects/Multiversion)