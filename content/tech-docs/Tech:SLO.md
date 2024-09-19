---
title: Tech:SLO
---

Miraheze's Site Reliability Engineering team have crafted a set of Service Level Objectives (SLOs) to measure the performance of critical services that we operate. Miraheze does not offer any formal Service Level Agreements (SLAs) so failure to meet the objectives below do not offer any financial or legal penalties - however there is an agreed internal escalation process for SLOs being breached.

**SLO Monitoring Process**

* SLOs are monitored on a monthly average basis - either at the end of the month or the beginning, we will publish the results below in the relevant table to signify our performances alongside whether the objective was met or not this month.
* Once SLOs are published below - if any SLO is failed, it will be highlighted for review internally.
* Following a first failure, a Phorge task will be created to review the performance data to evaluate whether the failure can be attributed to factors beyond control - or whether something needs to be done or implemented to ensure a success the following month.
* SLOs will be re-evaluated and if a second failure in a row occurs, a new Phorge task is created and assigned to the other SRE team for an external-team review. The other team will conduct a review to understand the failings that led to the performance indicator not being achieved.
* In the rare circumstance an SLO is failed three months in a row - the matter will be escalated to the Board of Directors for a review as there is a series of consecutive failures that need to be considered.

## Infrastructure SLOs 

<!-- Success: style="background-color:#90ee90;" Fail: style="background-color:#f08080;" -->

| Service | Type | Objective | Dec 22 | Jan 23 | Feb 23 | Mar 23 | Apr 23 | May 23 | Jun 23 | Jul 23 | Aug 23 | Sep 23 | Oct 23 | Nov 23 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| [Bastion](https://meta.miraheze.org/wiki/Tech:Bastion) | Availability | 99.5% | 100% | 100% | 100% | |  |  |  |  |  |  |  |
| rowspan="2" | [Cache Proxy](/tech-docs/techvarnish) | Availability | 75%/99.5% | 75%/99.5% | 75%/99.5% | 75%/99.9% | |  |  |  |  |  |  |  |
| Error | 7.5% | 6.87% | 3.81% | 4.16% | |  |  |  |  |  |  |  |
| [Cloud](/tech-docs/techproxmox) | Availability | 99.5% | 100% | 100% | 100% | |  |  |  |  |  |  |  |
| rowspan="3" | [DNS](/tech-docs/techdns) | Availability | 99.5% | 100% | 100% | 100% | |  |  |  |  |  |  |  |
| Error | 0.5% | 0.2% | 0.15% | 0.16% | |  |  |  |  |  |  |  |
| Latency | 5ms | 3.32ms | 3.23ms | 3.43ms | |  |  |  |  |  |  |  |
| [ElasticSearch](https://meta.miraheze.org/wiki/Tech:ElasticSearch) | Availability | 99.5% | 100% | 100% | 100% | |  |  |  |  |  |  |  |
| rowspan="3" | [Graylog](/tech-docs/techgraylog) | Availability | 99.5% | 100% | 100% | 100% | |  |  |  |  |  |  |  |
| Error | 0.5% | 0% | 0% | 0% | |  |  |  |  |  |  |  |
| Latency | 5ms | 0.65ms | 0.75ms | 1.01ms | |  |  |  |  |  |  |  |
| [LDAP](/tech-docs/techldap) | Availability | 99.5% | 100% | 100% | 100% | |  |  |  |  |  |  |  |
| Error | 1% | [1.71%](https://meta.miraheze.org/wiki/phorge:T10216) | 0.34% | 0.83% | |  |  |  |  |  |  |  |
| Latency | 30s | 9.61s | 10.80s | 28.08s | |  |  |  |  |  |  |  |
| rowspan="2" | [MariaDB](/tech-docs/techmariadb) | Availability | 99.5% | [98.7%](https://meta.miraheze.org/wiki/phorge:T10217) | 100% | 100% | |  |  |  |  |  |  |  |
| Error | 5% | [7.95%](https://meta.miraheze.org/wiki/phorge:T10217) | 0.01% | 0.01% | |  |  |  |  |  |  |  |
| rowspan="2" | [Phorge](/tech-docs/techphorge) | Availability | 99.5% | 100% | 99.90% | 99.90% | |  |  |  |  |  |  |  |
| Latency | 5s | 0.44s | 0.57s | 0.64s | |  |  |  |  |  |  |  |
| rowspan="2" | [Puppet](/tech-docs/techpuppet) | Availability | 99.5% | 100% | 100% | 99.99% | |  |  |  |  |  |  |  |
| Latency | 30ms | 17ms | 18.40ms | 20.90ms | |  |  |  |  |  |  |  |
| rowspan="3" | [Swift](/tech-docs/techswift) | Availability | 99.5% | 100% | 100% | 100% | |  |  |  |  |  |  |  |
| Error | 1% | 0.07% | [1.06%](https://meta.miraheze.org/wiki/phorge:T10434) | 0.75% | |  |  |  |  |  |  |  |
| Latency | 1s | 0.50s | 0.54s | 0.52s | |  |  |  |  |  |  |  |

## MediaWiki SLOs

<!-- Success: style="background-color:#90ee90;" Fail: style="background-color:#f08080;" -->

| Service | Type | Objective | Dec 22 | Jan 23 | Feb 23 | Mar 23 | Apr 23 | May 23 | Jun 23 | Jul 23 | Aug 23 | Sep 23 | Oct 23 | Nov 23 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| rowspan="2" | [JobQueue](/tech-docs/techmediawiki_appserver#jobrunner) | Availability | 99.5% | [95.30%](https://meta.miraheze.org/wiki/phorge:T10218) | 99.90% | 100% | |  |  |  |  |  |  |  |
| Errors | 1.5% | [1.8%](https://meta.miraheze.org/wiki/phorge:T10218) | [3.37%](https://meta.miraheze.org/wiki/phorge:T10218) | 0.02% | |  |  |  |  |  |  |  |
| rowspan="3" | [MediaWiki](/tech-docs/techmediawiki_appserver) | Availability | 99% | [96.5%](https://meta.miraheze.org/wiki/phorge:T10219) | 99.30% | 99.50% | |  |  |  |  |  |  |  |
| Error | 3% | 2.03% | 1.54% | 0.35% | |  |  |  |  |  |  |  |
| Latency | 3s | 1.41s | 1.41s | 1.35s | |  |  |  |  |  |  |  |
| [Memcached](/tech-docs/techmemcached) | Availability | 99.5% | 100% | 100% | 100% | |  |  |  |  |  |  |  |



----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:SLO)**