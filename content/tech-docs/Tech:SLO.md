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

<!-- <!-- Success: style="background-color:#90ee90;" Fail: style="background-color:#f08080;" --> -->

| Service | Type | Objective | Dec 22 | Jan 23 | Feb 23 | Mar 23 | Apr 23 | May 23 | Jun 23 | Jul 23 | Aug 23 | Sep 23 | Oct 23 | Nov 23 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| [Bastion](https://meta.miraheze.org/wiki/Tech:Bastion) | Availability | 99.5% | style="background-color:#90ee90;" | 100% | style="background-color:#90ee90;" | 100% | style="background-color:#90ee90;" | 100% |
| rowspan="2" | [Cache Proxy](https://meta.miraheze.org/wiki/Tech:Varnish) | Availability | 75%/99.5% | style="background-color:#90ee90;" | 75%/99.5% | style="background-color:#90ee90;" | 75%/99.5% | style="background-color:#90ee90;" | 75%/99.9% |
| Error | 7.5% | style="background-color:#90ee90;" | 6.87% | style="background-color:#90ee90;" | 3.81% | style="background-color:#90ee90;" | 4.16% |
| [Cloud](https://meta.miraheze.org/wiki/Tech:Proxmox) | Availability | 99.5% | style="background-color:#90ee90;" | 100% | style="background-color:#90ee90;" | 100% | style="background-color:#90ee90;" | 100% |
| rowspan="3" | [DNS](https://meta.miraheze.org/wiki/Tech:DNS) | Availability | 99.5% | style="background-color:#90ee90;" | 100% | style="background-color:#90ee90;" | 100% | style="background-color:#90ee90;" | 100% |
| Error | 0.5% | style="background-color:#90ee90;" | 0.2% | style="background-color:#90ee90;" | 0.15% | style="background-color:#90ee90;" | 0.16% |
| Latency | 5ms | style="background-color:#90ee90;" | 3.32ms | style="background-color:#90ee90;" | 3.23ms | style="background-color:#90ee90;" | 3.43ms |
| [ElasticSearch](https://meta.miraheze.org/wiki/Tech:ElasticSearch) | Availability | 99.5% | style="background-color:#90ee90;" | 100% | style="background-color:#90ee90;" | 100% | style="background-color:#90ee90;" | 100% |
| rowspan="3" | [Graylog](https://meta.miraheze.org/wiki/Tech:Graylog) | Availability | 99.5% | style="background-color:#90ee90;" | 100% | style="background-color:#90ee90;" | 100% | style="background-color:#90ee90;" | 100% |
| Error | 0.5% | style="background-color:#90ee90;" | 0% | style="background-color:#90ee90;" | 0% | style="background-color:#90ee90;" | 0% |
| Latency | 5ms | style="background-color:#90ee90;" | 0.65ms | style="background-color:#90ee90;" | 0.75ms | style="background-color:#90ee90;" | 1.01ms |
| [LDAP](https://meta.miraheze.org/wiki/Tech:Ldap) | Availability | 99.5% | style="background-color:#90ee90;" | 100% | style="background-color:#90ee90;" | 100% | style="background-color:#90ee90;" | 100% |
| Error | 1% | style="background-color:#f08080;" | [1.71%](https://meta.miraheze.org/wiki/phorge:T10216) | style="background-color:#90ee90;" | 0.34% | style="background-color:#90ee90;" | 0.83% |
| Latency | 30s | style="background-color:#90ee90;" | 9.61s | style="background-color:#90ee90;" | 10.80s | style="background-color:#90ee90;" | 28.08s |
| rowspan="2" | [MariaDB](https://meta.miraheze.org/wiki/Tech:MariaDB) | Availability | 99.5% | style="background-color:#f08080;" | [98.7%](https://meta.miraheze.org/wiki/phorge:T10217) | style="background-color:#90ee90;" | 100% | style="background-color:#90ee90;" | 100% |
| Error | 5% | style="background-color:#f08080;" | [7.95%](https://meta.miraheze.org/wiki/phorge:T10217) | style="background-color:#90ee90;" | 0.01% | style="background-color:#90ee90;" | 0.01% |
| rowspan="2" | [Phorge](https://meta.miraheze.org/wiki/Tech:Phorge) | Availability | 99.5% | style="background-color:#90ee90;" | 100% | style="background-color:#90ee90;" | 99.90% | style="background-color:#90ee90;" | 99.90% |
| Latency | 5s | style="background-color:#90ee90;" | 0.44s | style="background-color:#90ee90;" | 0.57s | style="background-color:#90ee90;" | 0.64s |
| rowspan="2" | [Puppet](https://meta.miraheze.org/wiki/Tech:Puppet) | Availability | 99.5% | style="background-color:#90ee90;" | 100% | style="background-color:#90ee90;" | 100% | style="background-color:#90ee90;" | 99.99% |
| Latency | 30ms | style="background-color:#90ee90;" | 17ms | style="background-color:#90ee90;" | 18.40ms | style="background-color:#90ee90;" | 20.90ms |
| rowspan="3" | [Swift](https://meta.miraheze.org/wiki/Tech:Swift) | Availability | 99.5% | style="background-color:#90ee90;" | 100% | style="background-color:#90ee90;" | 100% | style="background-color:#90ee90;" | 100% |
| Error | 1% | style="background-color:#90ee90;" | 0.07% | style="background-color:#f08080;" | [1.06%](https://meta.miraheze.org/wiki/phorge:T10434) | style="background-color:#90ee90;" | 0.75% |
| Latency | 1s | style="background-color:#90ee90;" | 0.50s | style="background-color:#90ee90;" | 0.54s | style="background-color:#90ee90;" | 0.52s |

## MediaWiki SLOs

<!-- <!-- Success: style="background-color:#90ee90;" Fail: style="background-color:#f08080;" --> -->

| Service | Type | Objective | Dec 22 | Jan 23 | Feb 23 | Mar 23 | Apr 23 | May 23 | Jun 23 | Jul 23 | Aug 23 | Sep 23 | Oct 23 | Nov 23 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| rowspan="2" | [JobQueue](https://meta.miraheze.org/wiki/Tech:MediaWiki_appserver#Jobrunner) | Availability | 99.5% | style="background-color:#f08080;" | [95.30%](https://meta.miraheze.org/wiki/phorge:T10218) | style="background-color:#90ee90;" | 99.90% | style="background-color:#90ee90;" | 100% |
| Errors | 1.5% | style="background-color:#f08080;" | [1.8%](https://meta.miraheze.org/wiki/phorge:T10218) | style="background-color:#f08080;" | [3.37%](https://meta.miraheze.org/wiki/phorge:T10218) | style="background-color:#90ee90;" | 0.02% |
| rowspan="3" | [MediaWiki](https://meta.miraheze.org/wiki/Tech:MediaWiki_appserver) | Availability | 99% | style="background-color:#f08080;" | [96.5%](https://meta.miraheze.org/wiki/phorge:T10219) | style="background-color:#90ee90;" | 99.30% | style="background-color:#90ee90;" | 99.50% |
| Error | 3% | style="background-color:#90ee90;" | 2.03% | style="background-color:#90ee90;" | 1.54% | style="background-color:#90ee90;" | 0.35% |
| Latency | 3s | style="background-color:#90ee90;" | 1.41s | style="background-color:#90ee90;" | 1.41s | style="background-color:#90ee90;" | 1.35s |
| [Memcached](https://meta.miraheze.org/wiki/Tech:Memcached) | Availability | 99.5% | style="background-color:#90ee90;" | 100% | style="background-color:#90ee90;" | 100% | style="background-color:#90ee90;" | 100% |

----
**Source**: https://meta.miraheze.org/wiki/Tech:SLO