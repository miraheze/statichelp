---
title: Tech:Projects/Automation of SSL requests
---

This is a project proposal for implementing a system where on request, users can generate a Lets Encrypt certificate which is then deployed to GitHub and to MediaWiki via $wgServer (after being approved by an SRE member).

## Background 

Currently, for users to have a domain apart from a Miraheze subdomain (i.e., example.miraheze.org) they must file a request on Phorge. Thereafter, an SRE member must generate an SSL certificate with a script on a server (puppet181), commit the SSL certificate and config on GitHub, and then complete $wgServer via Special:ManageWiki.

## Plan 

### Stage 1 

Updating certbot cli to check rDNS is correct and either CNAME or NS record is present. Add argument to skip this.

### Stage 2 

Creating a web form to automate creating SSL tasks + checking validity - refuse to create if invalid.

### Stage 3 

Creating a new wrapper for generating new SSL certs, pushing public keys to GitHub handling over private key additions via our private git repository on puppet181.

### Stage 4 

Implement an API into ManageWiki that allows updating of the $wgServer component.

## Requirements 

The current system will have to be completely redesigned and the server where private keys are generated should be the same place where they are ultimately stored, rather than two servers.

## Outcome Steps 

* A web form that allows users to create requests for custom domains (and by definition SSL certificates) which then can be approved or declined by SRE members. Approval would entail the automatic creation and deployment of the SSL certificate and configuration of the custom domain.

## Getting Started 

Anyone interested in starting this project should:
* Get familiar with how our SSL process currently operates (see [Tech:SSL certificates](Tech:SSL_certificates.md)) for more details.
* Get in touch with an [SRE](https://meta.miraheze.org/wiki/Tech:Organisation#Team:_MediaWiki,_Site_Reliability_Engineering) member to discuss how to proceed.

----
**Source**: [https://meta.miraheze.org/wiki/Tech:Projects/Automation_of_SSL_requests](https://meta.miraheze.org/wiki/Tech:Projects/Automation_of_SSL_requests)