---
title: Tech:Miscellaneous Wiki Stats
---

This page contains miscellaneous wiki statistics that can be queried via SQL query. The page was originally created by John and the queries were tuned with the help of Southparkfan.

## Historical 

Data originally collected by [NDKilla](https://meta.miraheze.org/wiki/User:NDKilla) and [Reception123](https://meta.miraheze.org/wiki/User:Reception123). As of approximately 2020, updated information (including new information on approved requests) collected by [Reception123](https://meta.miraheze.org/wiki/User:Reception123).

This data is collected in the capacity of a system administrator and no data being revealed is considered private or sensitive. Therefore reusing anything on this page is fair game with or without credit to myself.

Please note that the number of requests is nowhere near the actual number of wikis due to deletion, denied requests and spam. (Reception123)

Other statistics can be found on [this page](https://meta.miraheze.org/wiki/User:Reception123/temp_stats) temporarily.

---

## Wiki request status per month 

| + |
| Month | Approved | Declined | Total requests | % approved |
| --- | --- | --- | --- | --- |
| March 2025 | 1013 | 392 | 1458 | 72% |
| February 2025 | 959 | 308 | 1299 | 76% |
| January 2025 | 837 | 290 | 1127 | 74% |
| December 2024 | 918 | 234 | 1152 | 79% |
| November 2024 | 768 | 251 | 1019 | 75% |
| October 2024 | 857 | 301 | 1158 | 74% |
| September 2024 | 664 | 432 | 1096 | 60% |
NOTE: The number of approved and declined requests don't match up to the total due to the fact that not all requests made in the relevant month are handled within the same month (i.e. requests made on the 30th and 31st might be handled next month).

## Raw wiki creation data 

First, let's see how many wiki requests there were at the time I collected the data.
**Date collected: 18 February 2025** (Reception123)
```
MariaDB [metawiki]> SELECT COUNT(*) FROM cw_requests;
+----------+
| COUNT(*) |
+----------+
|    55287 |
+----------+
```

Now let's associated user_ids with the last person who commented. This in general gives a fair estimate and is the best we have. Therefore the value can be expected to be plus or minus a few.

~~**For all wiki requests**~~
```
MariaDB [metawiki]> SELECT user.user_name, COUNT(*) as COUNT FROM cw_requests JOIN user ON cw_requests.cw_status_comment_user = user.user_id GROUP BY cw_requests.cw_status_comment_user ORDER BY COUNT DESC;
'''Last updated: 24 August 2018''' (''OUTDATED!'')

+-------------------+-------+
| user_name         | COUNT |
+-------------------+-------+
| Reception123      |  1773 |
| Void              |   656 |
| AlvaroMolina      |   533 |
| MacFan4000        |   487 |
| TriX              |   431 |
| John              |   224 |
| Southparkfan      |   120 |
| CnocBride         |   102 |
| Revi              |    93 |
| NDKilla           |    79 |
| Wiki1776          |    70 |
| SleepyMode        |    60 |
| Videojeux4        |    54 |
| Sau226            |    42 |
| Zppix             |    38 |
| ItsPugle          |    35 |
| Lawrence-Prairies |    33 |
| GOTILON           |    29 |
| Samuel            |    17 |
| XOF               |    12 |
| Corey             |    11 |
| Sammy             |     9 |
| Paladox           |     6 |
| There'sNoTime     |     6 |
| Labster           |     2 |
| Guy vandegrift    |     1 |
+-------------------+-------+
```

~~**For approved wiki requests**~~
```
MariaDB [metawiki]> SELECT user.user_name, COUNT(*) as COUNT FROM cw_requests JOIN user ON cw_requests.cw_status_comment_user = user.user_id WHERE cw_requests.cw_status="approved"  GROUP BY cw_requests.cw_status_comment_user ORDER BY COUNT DESC;
'''Last updated: 24 August 2018''' (''OUTDATED!'')

+-------------------+-------+
| user_name         | COUNT |
+-------------------+-------+
| Reception123      |  1548 |
| AlvaroMolina      |   443 |
| Void              |   425 |
| TriX              |   412 |
| MacFan4000        |   409 |
| John              |   177 |
| Southparkfan      |   105 |
| Revi              |    80 |
| CnocBride         |    74 |
| NDKilla           |    70 |
| Wiki1776          |    60 |
| Videojeux4        |    40 |
| Sau226            |    35 |
| Zppix             |    28 |
| SleepyMode        |    26 |
| Lawrence-Prairies |    25 |
| ItsPugle          |    25 |
| GOTILON           |    24 |
| Samuel            |    17 |
| XOF               |    12 |
| Corey             |    11 |
| Sammy             |     9 |
| There'sNoTime     |     6 |
| Paladox           |     3 |
| Labster           |     1 |
+-------------------+-------+
```

#### For wikis created

```
MariaDB [metawiki]> select actor_name, count(*) as count from logging join actor on actor_id = log_actor where log_type = 'farmer' and log_action = 'createwiki' group by log_actor order by count desc;
+-----------------------------------------------+-------+
| actor_name                                    | count |
+-----------------------------------------------+-------+
| Tali64Â³                                      |  6014 |
| Reception123                                  |  3616 |
| Jph2                                          |  2959 |
| DarkMatterMan4500                             |  2577 |
| Agent Isai                                    |  2046 |
| Doug                                          |  1887 |
| Subwayfares                                   |  1747 |
| Void                                          |  1737 |
| NotAracham                                    |  1494 |
| é–‹æ‹“è€…                                     |  1411 |
| Rodejong                                      |  1388 |
| Redmin                                        |  1144 |
| Waki285                                       |  1074 |
| Chrs                                          |   847 |
| CreateWiki AI                                 |   753 |
| MirahezeGDPR                                  |   726 |
| Zppix                                         |   621 |
| Raidarr                                       |   593 |
| Examknow                                      |   517 |
| AlvaroMolina                                  |   478 |
| BrandonWM                                     |   466 |
| Amanda Catherine                              |   447 |
| RhinosF1                                      |   444 |
| MirahezeGDPR                                  |   440 |
| MacFan4000                                    |   424 |
| MrJaroslavik                                  |   392 |
| TriX                                          |   389 |
| Hispano76                                     |   354 |
| SA 13 Bro                                     |   234 |
| John                                          |   230 |
| Paladox                                       |   214 |
| CnocBride                                     |   193 |
| Southparkfan                                  |   158 |
| Msnhinet8                                     |   128 |
| TBCtableEX                                    |   114 |
| GOTILON                                       |   109 |
| Guy vandegrift                                |   104 |
| Revi                                          |   103 |
| Ratekreel                                     |    97 |
| HeartsDo                                      |    94 |
| HispanoBOT                                    |    93 |
| NDKilla                                       |    84 |
| Bonnedav                                      |    76 |
| Cmg                                           |    75 |
| Pisces                                        |    63 |
| Sau226                                        |    63 |
| Centrist16                                    |    52 |
| Megacane                                      |    51 |
| Zeus                                          |    47 |
| Cy                                            |    44 |
| Bongo Cat                                     |    44 |
| 1108-Kiju                                     |    38 |
| Sario528                                      |    34 |
| Lawrence-Prairies                             |    27 |
| CircleyDoesExtracter                          |    26 |
| LegoMaster                                    |    26 |
| GDPRAccount                                   |    25 |
| SleepyMode                                    |    24 |
| Universal Omega                               |    23 |
| Gustave London                                |    22 |
| OrangeStar                                    |    21 |
| Furricane                                     |    20 |
| PixDeVl                                       |    20 |
| Fungster                                      |    17 |
| Samuel                                        |    17 |
| ã‚·ãƒ¥ãƒ´ã‚¡ãƒ«ãƒ„                            |    16 |
| Corey                                         |    14 |
| Pkbwcgs                                       |    14 |
| XOF                                           |    12 |
| Wolf                                          |    11 |
| CoolieCoolster                                |    11 |
| Sammy                                         |    11 |
| OlegCinema                                    |    10 |
| Eduaddad                                      |     7 |
| TheresNoTime                                  |     6 |
| ãã‚‰ãŸã“                                  |     5 |
| Alex (Miraheze)                               |     5 |
| Avengium                                      |     4 |
| CreateWiki Extension                          |     3 |
| Integer                                       |     3 |
| Labster                                       |     1 |
| Example4                                      |     1 |
+-----------------------------------------------+-------+
82 rows in set (0.758 sec)
```

#### For wikis created between 2024-2026

Proposed alternate script:
```
select actor_name, count(*) as count from logging join actor on actor_id = log_actor where log_type = 'farmer' and log_action = 'createwiki' and LEFT(log_timestamp,4) BETWEEN '2024' AND '2026' group by log_actor order by count desc;

+----------------------+-------+
| actor_name           | count |
+----------------------+-------+
| Subwayfares          |  1747 |
| Jph2                 |  1630 |
| Rodejong             |  1388 |
| Reception123         |  1298 |
| Waki285              |  1042 |
| CreateWiki AI        |   753 |
| Tali64Â³             |   619 |
| BrandonWM            |   466 |
| NotAracham           |   425 |
| Redmin               |   232 |
| Raidarr              |    95 |
| Agent Isai           |    77 |
| Pisces               |    63 |
| Zeus                 |    47 |
| 1108-Kiju            |    38 |
| Universal Omega      |    23 |
| OrangeStar           |    21 |
| PixDeVl              |    20 |
| Zppix                |     6 |
| Alex (Miraheze)      |     5 |
| CreateWiki Extension |     3 |
+----------------------+-------+
21 rows in set (0.117 sec)
```

#### For wikis created between 2022-2024

Proposed alternate script:
```
select actor_name, count(*) as count from logging join actor on actor_id = log_actor where log_type = 'farmer' and log_action = 'createwiki' and LEFT(log_timestamp,4) BETWEEN '2022' AND '2024' group by log_actor order by count desc;
```
 --[NotAracham](https://meta.miraheze.org/wiki/m:User:NotAracham) ([talk](https://meta.miraheze.org/wiki/m:User_talk:NotAracham) • [contribs](https://meta.miraheze.org/wiki/m:Special:Contributions/NotAracham) • [global](https://meta.miraheze.org/wiki/m:Special:CentralAuth/NotAracham)) 17:08, 16 March 2023 (UTC)

```
select actor_name, count(*) as count from logging join actor on actor_id = log_actor where log_type = 'farmer' and log_action = 'createwiki' and (log_timestamp like '2022%') group by log_actor order by count desc;
+-----------------------------------------------+-------+
| actor_name                                    | count |
+-----------------------------------------------+-------+
| Tali64Â³                                      |  6014 |
| Jph2                                          |  2834 |
| NotAracham                                    |  1459 |
| Reception123                                  |  1455 |
| DarkMatterMan4500                             |  1255 |
| Agent Isai                                    |  1251 |
| Rodejong                                      |  1251 |
| Subwayfares                                   |  1222 |
| Waki285                                       |  1041 |
| Chrs                                          |   631 |
| Redmin                                        |   594 |
| Raidarr                                       |   489 |
| BrandonWM                                     |   465 |
| MirahezeGDPR                                  |   450 |
| MirahezeGDPR                                  |   292 |
| Zppix                                         |   262 |
| Void                                          |   135 |
| Doug                                          |    73 |
| Hispano76                                     |    66 |
| Pisces                                        |    63 |
| Zeus                                          |    47 |
| Bongo Cat                                     |    44 |
| Ratekreel                                     |    43 |
| 1108-Kiju                                     |    38 |
| Universal Omega                               |    22 |
| OrangeStar                                    |    21 |
| PixDeVl                                       |    20 |
| Msnhinet8                                     |    20 |
| Sario528                                      |     6 |
| Alex (Miraheze)                               |     5 |
| RhinosF1                                      |     5 |
| CreateWiki Extension                          |     3 |
| Avengium                                      |     2 |
| ã‚·ãƒ¥ãƒ´ã‚¡ãƒ«ãƒ„                            |     2 |
| John                                          |     1 |
+-----------------------------------------------+-------+
35 rows in set (0.122 sec)
```

#### For wikis created between 2019-2021

```
MariaDB [metawiki]> select actor_name, count(*) as count from logging join actor on actor_id = log_actor where log_type = 'farmer' and log_action = 'createwiki' and (log_timestamp like '2021%' or log_timestamp like '2020%' or log_timestamp like '2019%' or log_timestamp like '2019%') group by log_actor order by count desc;
+-----------------------------------------+-------+
| actor_name                              | count |
+-----------------------------------------+-------+
| Dmehus                                  |  1814 |
| DarkMatterMan4500                       |  1322 |
| é–‹æ‹“è€…                               |  1144 |
| Agent Isai                              |   795 |
| Void                                    |   772 |
| Redmin                                  |   534 |
| Examknow                                |   517 |
| Reception123                            |   477 |
| Amanda Catherine                        |   447 |
| RhinosF1                                |   439 |
| MrJaroslavik                            |   392 |
| Zppix                                   |   309 |
| Universal Omega                         |   276 |
| Hispano76                               |   258 |
| SA 13 Bro                               |   234 |
| Chrs                                    |   216 |
| Naleksuh                                |   148 |
| TBCtableEX                              |   114 |
| Paladox                                 |    96 |
| Raidarr                                 |    85 |
| Msnhinet8                               |    77 |
| Bonnedav                                |    76 |
| Cmg                                     |    75 |
| Startus                                 |    54 |
| Hypercane                               |    51 |
| John                                    |    35 |
| Waki285                                 |    32 |
| Sario528                                |    28 |
| HeartsDo                                |    26 |
| CircleyDoesExtracter                    |    26 |
| LegoMaster                              |    26 |
| Gustave London                          |    22 |
| Furricane                               |    20 |
| Fungster                                |    17 |
| CnocBride                               |    16 |
| ã‚·ãƒ¥ãƒ´ã‚¡ãƒ«ãƒ„                      |    14 |
| Southparkfan                            |    12 |
| Wolf                                    |    11 |
| Eduaddad                                |     7 |
| Revi                                    |     6 |
| AlvaroMolina                            |     5 |
| ãã‚‰ãŸã“                            |     5 |
| MacFan4000                              |     4 |
| Cy                                      |     3 |
| Integer                                 |     3 |
| Avengium                                |     2 |
| NDKilla                                 |     1 |
| Pkbwcgs                                 |     1 |
+-----------------------------------------+-------+
48 rows in set (0.288 sec)
```

#### For wikis declined between 2022-2024

NOTE: **Prior to 2 April 2024, decline was generally used instead of 'needs more details'**
```
MariaDB [metawiki]> select actor_name, count(*) as count from logging join actor on actor_id = log_actor where log_type = 'farmer' and log_action = 'requestdecline' and LEFT(log_timestamp,4) BETWEEN '2022' AND '2024' group by log_actor order by count desc;

+-----------------------------------------------+-------+
| actor_name                                    | count |
+-----------------------------------------------+-------+
| Jph2                                          |  4776 |
| Tali64Â³                                      |  2091 |
| Agent Isai                                    |  1597 |
| Rodejong                                      |  1164 |
| DarkMatterMan4500                             |   866 |
| NotAracham                                    |   790 |
| Redmin                                        |   419 |
| Waki285                                       |   351 |
| BrandonWM                                     |   317 |
| Chrs                                          |   290 |
| Reception123                                  |   221 |
| Zppix                                         |   163 |
| Raidarr                                       |   138 |
| Zeus                                          |   114 |
| Ratekreel                                     |    69 |
| Doug                                          |    62 |
| MirahezeGDPR                                  |    57 |
| MirahezeGDPR                                  |    50 |
| Subwayfares                                   |    44 |
| Pisces                                        |    38 |
| Void                                          |    35 |
| 1108-Kiju                                     |    35 |
| Bongo Cat                                     |    16 |
| PixDeVl                                       |    14 |
| Hispano76                                     |     7 |
| OrangeStar                                    |     6 |
| RhinosF1                                      |     4 |
| Msnhinet8                                     |     2 |
| HeartsDo                                      |     2 |
| Amanda Catherine                              |     1 |
| Avengium                                      |     1 |
+-----------------------------------------------+-------+
31 rows in set (2.430 sec)
```

#### For wikis where more details were requested between 2022-2024

NOTE: **Only applies starting 2 April 2024. Overlaps with later approvals/declines!**
```
MariaDB [metawiki]> select actor_name, count(*) as count from logging join actor on actor_id = log_actor where log_type = 'farmer' and log_action = 'requestmoredetails' and LEFT(log_timestamp,4) BETWEEN '2022' AND '2024' group by log_actor order by count desc;
+--------------+-------+
| actor_name   | count |
+--------------+-------+
| Rodejong     |  2095 |
| Waki285      |  1511 |
| Jph2         |  1155 |
| Reception123 |   324 |
| Redmin       |    80 |
| NotAracham   |    57 |
| BrandonWM    |    34 |
| Zeus         |    11 |
| PixDeVl      |    11 |
| Agent Isai   |     9 |
| 1108-Kiju    |     9 |
| Pisces       |     8 |
| Raidarr      |     5 |
| Zppix        |     3 |
+--------------+-------+
```

#### Wikis by languages

```
MariaDB [mhglobal]> SELECT wiki_language, COUNT(*) as COUNT FROM cw_wikis GROUP BY wiki_language ORDER BY COUNT DESC;
+---------------+-------+
| wiki_language | COUNT |
+---------------+-------+
| en            | 11385 |
| ru            |   327 |
| ja            |   322 |
| fr            |   285 |
| es            |   266 |
| de            |   198 |
| pt-br         |   178 |
| pl            |   151 |
| it            |   106 |
| zh            |   106 |
| en-gb         |    97 |
| zh-cn         |    89 |
| ko            |    83 |
| zh-hans       |    67 |
| nl            |    48 |
| es-419        |    39 |
| he            |    39 |
| tr            |    34 |
| cs            |    34 |
| uk            |    32 |
| pt            |    28 |
| zh-tw         |    28 |
| vi            |    26 |
| id            |    26 |
| fi            |    20 |
| zh-hant       |    17 |
| hu            |    17 |
| sv            |    17 |
| bn            |    12 |
| ro            |    11 |
| es-formal     |    11 |
| no            |    11 |
| ca            |    10 |
| th            |     9 |
| en-ca         |     9 |
| ar            |     9 |
| de-at         |     8 |
| de-formal     |     8 |
| el            |     6 |
| sk            |     6 |
| ms            |     6 |
| da            |     5 |
| de-ch         |     5 |
| nb            |     4 |
| lt            |     4 |
| ka            |     3 |
| fa            |     3 |
| gl            |     3 |
| zh-hk         |     3 |
| eo            |     2 |
| sr            |     2 |
| tl            |     2 |
| bg            |     2 |
| fur           |     2 |
| hr            |     2 |
| rsk           |     2 |
| frc           |     2 |
| lzh           |     2 |
| hu-formal     |     2 |
| et            |     2 |
| grc           |     2 |
| zgh           |     1 |
| dtp           |     1 |
| isv           |     1 |
| la            |     1 |
| arz           |     1 |
| ia            |     1 |
| azb           |     1 |
| zh-mo         |     1 |
| cy            |     1 |
| krl           |     1 |
| sq            |     1 |
| ab            |     1 |
| br            |     1 |
| cpx-hans      |     1 |
| gu            |     1 |
| lv            |     1 |
| kw            |     1 |
| ryu           |     1 |
| hi            |     1 |
| qbg           |     1 |
| lfn           |     1 |
| gan-hans      |     1 |
| bar           |     1 |
| sl            |     1 |
| zh-classical  |     1 |
| nn            |     1 |
| szl           |     1 |
+---------------+-------+
88 rows in set (0.021 sec)
```

#### Wikis by categories

```
MariaDB [mhglobal]> SELECT wiki_category, COUNT(*) as COUNT FROM cw_wikis GROUP BY wiki_category ORDER BY COUNT DESC;
+-----------------+-------+
| wiki_category   | COUNT |
+-----------------+-------+
| gaming          |  3438 |
| fantasy         |  1720 |
| uncategorised   |  1516 |
| fandom          |  1229 |
| private         |   838 |
| literature      |   835 |
| entertainment   |   701 |
| community       |   649 |
| education       |   403 |
| software        |   369 |
| history         |   362 |
| politics        |   303 |
| music           |   279 |
| science         |   195 |
| humour          |   182 |
| langling        |   172 |
| sport           |   168 |
| songcontest     |   151 |
| geography       |   108 |
| leisure         |   104 |
| religion        |    91 |
| military        |    86 |
| artarc          |    68 |
| electronics     |    65 |
| media           |    61 |
| medical         |    53 |
| businessfinance |    40 |
| podcast         |    39 |
| automotive      |    37 |
+-----------------+-------+
29 rows in set (0.029 sec)
```

----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:Miscellaneous_Wiki_Stats)**