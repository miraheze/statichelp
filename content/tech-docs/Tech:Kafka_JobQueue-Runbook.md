---
title: Tech:Kafka JobQueue/Runbook
---

The MediaWiki Kafka JobQueue is responsible for many background actions carried out by MediaWiki and can often cause alerts.

This runbook should help you understand quickly if an incident requires intervention.

## Alerts 

* High JobQueue Backlog - this is self explanatory and alerts when the backlog of the JobQueue is high. This alone isn't necessarily an incident but a high backlog over an extended period of time could be an indicator something is wrong.
* JobQueue is rapidly increasing - this tells you that the JobQueue backlog has been going up at a fast rate over an extended period of time. This is indicative of a problem but could be caused by something as simple as multiple edits in quick succession.
* JobQueue backlog has been estimated at over 8 hours for a long time - this tells you that we aren't processing jobs fast enough. You should investigate why.
## Dashboards 

* [Total Jobs ](https://grafana.wikitide.net/d/GtxbP1Xnk/mediawiki?orgId=1&from=now-3h&to=now&timezone=browser&var-node=$__all&var-job=$__all&viewPanel=panel-54)
* [Count by Job ](https://grafana.wikitide.net/d/GtxbP1Xnk/mediawiki?orgId=1&from=now-3h&to=now&timezone=browser&var-node=$__all&var-job=$__all&viewPanel=panel-48)
These 2 dashboards allow you to see the current count of jobs and how it's changing over time. This will allow you to see what is causing the backlog and whether it's going up or down.

* [Delta](https://grafana.wikitide.net/d/GtxbP1Xnk/mediawiki?orgId=1&from=now-3h&to=now&timezone=browser&var-node=$__all&var-job=$__all&viewPanel=panel-68)
This allow you to see whether the queue is going up or down. The average for this should be zero or negative. A positive number means it's going up

* [Time to clear ](https://grafana.wikitide.net/d/GtxbP1Xnk/mediawiki?orgId=1&from=now-3h&to=now&timezone=browser&var-node=$__all&var-job=$__all&viewPanel=panel-69)
This graph only works if the queue is going down. It will tell you at the current rate how long it takes to clear the Queue

## Debugging 

Use this command to current offset of the JobQueue.

`/usr/local/bin/kafka consumer-groups.sh --all-groups --describe --bootstrap-server=localhost:9092 | grep "smw.update"`

The output will look like the below. 80795 is the relevant number here.

`cpjobqueue-semantic_mediawiki_jobs default.mediawiki.job.smw.update
 
                               0 80795           153256          72461           329268-73a5310f-8184-4dd5-b5e5-6fe596e9d59c /2602:294:0:b33:0:0:0:106 329268 `

The below can then be used to inspect a job

`/usr/local/bin/kafka console-consumer.sh --bootstrap-server localhost:9092 --topic=default.mediawiki.job.smw.update  --partition 0 --offset 80795 --max-messages 1 --consumer-property enable.auto.commit=false`

## Running Jobs 

< TO DO >
## Clearing a topic 

`/usr/local/bin/kafka topics.sh --bootstrap-server localhost:9092 --delete --topic <topic>`

**Note:** <topic> can either be a plain text string or a regex. E.g `mediawiki.test` or `mediawiki.test.*`.

**Note:** The topic will be auto-created again by Changeprop.

**Do not delete** on-disk. It may lead to some kind of messing up kafka. We also use burrow which it may mess up.

## Resources 

* [Kafka Topics CLI Tutorial](https://learn.conduktor.io/kafka/kafka-topics-cli-tutorial/)

----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:Kafka_JobQueue/Runbook)**