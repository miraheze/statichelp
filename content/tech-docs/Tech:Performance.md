---
title: Tech:Performance
---

This page briefly documents some procedures that members of the [Technology Team](https://meta.miraheze.org/wiki/Technology_Team) can follow to improve performance on the farm.

## Cloudflare

Go to Security -> Analytics. Filter requests that are "Served by origin" and ignore ones that are already cached or blocked by Cloudflare. Look for problematic access patterns. For example, if a wiki is seeing too many web requests relative to its popularity, it might be under a web scraper or running inefficient JS which sends lots of requests to the server.

For web scrapers, figure out their access pattern and challenge them.

For wikis with inefficient JS, reach out to them about it.

For popular wikis, examine uncached requests and see if they can be cached by Cloudflare or optimized on-wiki. Caching -> Overview can give a sense of which wikis are sending the most uncached requests and how much data these are transferring.

## Nginx logs

Cook from Weird Gloop made the initial suggestion for this approach.

Go to [Graylog](/tech-docs/techgraylog). Search for `application_name:nginx` in the past hour. Click on the "..." menu and click export. Export fields `timestamp`, `nginx_request_host`, `nginx_request_time`, and optionally `nginx_request_path`.

After the data is exported, it can be analyzed locally. For example, DuckDB provides a direct interface with CSV files. If you name the exported file `data.csv`, you can run `duckdb data.csv` and the exported table will be available as if it is a SQL table.

You can, for example, find out which wikis take up the most server resources. Note that while Cloudflare only shows many requests are made, `nginx_request_time` tells you the time the server spent processing a request.
```sql
select 
  nginx_request_host as host,
  round(sum(nginx_request_time)) as time,
  round(avg(nginx_request_time), 2) as average
from data
group by host
order by time desc
limit 50;
```

If a wiki's average time is too high, it is possibly under scraping activity, where expensive requests such as `oldid` and `action=diff` are consuming too much resources.

Another useful technique is graphing the minute-by-minute changes in server resource usage to see if there are any spikes.
```sql
COPY (
    SELECT
        date_trunc('minute', timestamp) AS minute,
        nginx_request_host AS host,
        sum(nginx_request_time) AS t
    FROM data
    WHERE nginx_request_host IS NOT NULL
    GROUP BY minute, host
    ORDER BY minute DESC, t DESC
) TO 'request_times.csv' (HEADER, DELIMITER ',');
```
This exports the per-minute request time data to a CSV file, which can then be used in a plot.

## Speedscope

This is waiting on [T15183](https://meta.miraheze.org/wiki/phorge:T15183).

----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:Performance)**