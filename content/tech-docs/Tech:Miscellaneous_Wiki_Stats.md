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
| July 2025 | 1321 | 384 | 1705 | 77% |
| June 2025 | 1168 | 257 | 1446 | 82% |
| May 2025 | 1245 | 313 | 1622 | 80% |
| April 2025 | 1129 | 353 | 1482 | 76% |
| March 2025 | 1061 | 452 | 1513 | 70% |
| February 2025 | 965 | 334 | 1299 | 73% |
| January 2025 | 871 | 299 | 1170 | 74% |
| December 2024 | 950 | 245 | 1195 | 79% |
| November 2024 | 809 | 256 | 1065 | 75% |
| October 2024 | 857 | 301 | 1158 | 74% |
| September 2024 | 664 | 432 | 1096 | 60% |
NOTE: The number of approved and declined requests don't match up to the total due to the fact that not all requests made in the relevant month are handled within the same month (i.e. requests made on the 30th and 31st might be handled next month).

## Raw wiki creation data 

First, let's see how many wiki requests there were at the time I collected the data.
**Date collected: 14 August 2025** (Reception123)
```
MariaDB [metawiki]> SELECT COUNT(*) FROM cw_requests;
+----------+
| COUNT(*) |
+----------+
|    64241 |
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
| CreateWiki AI                                 |  6262 |
| Tali64Â³                                      |  6014 |
| Reception123                                  |  3848 |
| Jph2                                          |  3291 |
| DarkMatterMan4500                             |  2577 |
| Agent Isai                                    |  2050 |
| Doug                                          |  1887 |
| NotAracham                                    |  1883 |
| Subwayfares                                   |  1777 |
| Void                                          |  1737 |
| Rodejong                                      |  1594 |
| é–‹æ‹“è€…                                     |  1411 |
| Redmin                                        |  1159 |
| Waki285                                       |  1075 |
| Chrs                                          |   847 |
| MirahezeGDPR                                  |   726 |
| Zppix                                         |   622 |
| Raidarr                                       |   598 |
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
| Sau226                                        |    63 |
| Pisces                                        |    63 |
| Centrist16                                    |    52 |
| Megacane                                      |    51 |
| Zeus                                          |    47 |
| Bongo Cat                                     |    44 |
| Cy                                            |    44 |
| 1108-Kiju                                     |    40 |
| Universal Omega                               |    39 |
| PixDeVl                                       |    37 |
| Sario528                                      |    34 |
| Lawrence-Prairies                             |    27 |
| CircleyDoesExtracter                          |    26 |
| LegoMaster                                    |    26 |
| GDPRAccount                                   |    25 |
| SleepyMode                                    |    24 |
| Gustave London                                |    22 |
| OrangeStar                                    |    21 |
| Furricane                                     |    20 |
| Fungster                                      |    17 |
| Samuel                                        |    17 |
| ã‚·ãƒ¥ãƒ´ã‚¡ãƒ«ãƒ„                            |    16 |
| Pkbwcgs                                       |    14 |
| Corey                                         |    14 |
| XOF                                           |    12 |
| CoolieCoolster                                |    11 |
| Sammy                                         |    11 |
| Wolf                                          |    11 |
| OlegCinema                                    |    10 |
| Bunnypranav                                   |     8 |
| Eduaddad                                      |     7 |
| TheresNoTime                                  |     6 |
| Alex (Miraheze)                               |     5 |
| ãã‚‰ãŸã“                                  |     5 |
| Avengium                                      |     4 |
| CreateWiki Extension                          |     3 |
| Integer                                       |     3 |
| Aeywoo                                        |     2 |
| Example4                                      |     1 |
| Labster                                       |     1 |
+-----------------------------------------------+-------+
84 rows in set (0.564 sec)
```

#### For wikis created between 2024-2026

Proposed alternate script:
```
select actor_name, count(*) as count from logging join actor on actor_id = log_actor where log_type = 'farmer' and log_action = 'createwiki' and LEFT(log_timestamp,4) BETWEEN '2024' AND '2026' group by log_actor order by count desc;

+----------------------+-------+
| actor_name           | count |
+----------------------+-------+
| CreateWiki AI        |  6262 |
| Jph2                 |  1962 |
| Subwayfares          |  1777 |
| Rodejong             |  1594 |
| Reception123         |  1530 |
| Waki285              |  1043 |
| NotAracham           |   814 |
| Tali64Â³             |   619 |
| BrandonWM            |   466 |
| Redmin               |   247 |
| Raidarr              |   100 |
| Agent Isai           |    81 |
| Pisces               |    63 |
| Zeus                 |    47 |
| 1108-Kiju            |    40 |
| Universal Omega      |    39 |
| PixDeVl              |    37 |
| OrangeStar           |    21 |
| Bunnypranav          |     8 |
| Zppix                |     7 |
| Alex (Miraheze)      |     5 |
| CreateWiki Extension |     3 |
| Aeywoo               |     2 |
+----------------------+-------+
23 rows in set (0.108 sec)
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
| en            | 16697 |
| ru            |   484 |
| ja            |   466 |
| es            |   438 |
| fr            |   432 |
| pt-br         |   310 |
| de            |   278 |
| pl            |   199 |
| it            |   169 |
| zh-cn         |   140 |
| zh            |   137 |
| ko            |   123 |
| en-gb         |   118 |
| zh-hans       |    93 |
| es-419        |    77 |
| nl            |    62 |
| tr            |    57 |
| id            |    54 |
| he            |    53 |
| vi            |    52 |
| uk            |    50 |
| cs            |    40 |
| pt            |    39 |
| zh-tw         |    32 |
| fi            |    31 |
| sv            |    25 |
| hu            |    24 |
| zh-hant       |    23 |
| bn            |    21 |
| ar            |    19 |
| en-ca         |    18 |
| ro            |    18 |
| es-formal     |    16 |
| th            |    15 |
| no            |    13 |
| ca            |    12 |
| de-at         |    11 |
| el            |    11 |
| da            |    11 |
| de-formal     |    10 |
| fa            |    10 |
| de-ch         |     8 |
| sk            |     7 |
| bg            |     7 |
| zh-hk         |     7 |
| ms            |     7 |
| nb            |     6 |
| tl            |     6 |
| lt            |     5 |
| eo            |     4 |
| sr            |     4 |
| hr            |     4 |
| rsk           |     3 |
| ka            |     3 |
| frc           |     3 |
| gl            |     3 |
| sl            |     3 |
| hi            |     2 |
| lzh           |     2 |
| hu-formal     |     2 |
| et            |     2 |
| la            |     2 |
| ia            |     2 |
| grc           |     2 |
| hy            |     2 |
| fur           |     2 |
| gan-hans      |     2 |
| lv            |     2 |
| az            |     2 |
| qbg           |     1 |
| dtp           |     1 |
| lfn           |     1 |
| isv           |     1 |
| sq            |     1 |
| ab            |     1 |
| br            |     1 |
| af            |     1 |
| cpx-hans      |     1 |
| zh-mo         |     1 |
| zgh           |     1 |
| krl           |     1 |
| bar           |     1 |
| mrh           |     1 |
| gor           |     1 |
| zh-classical  |     1 |
| kw            |     1 |
| szl           |     1 |
| ang           |     1 |
| lad           |     1 |
| mwl           |     1 |
| yi            |     1 |
| be            |     1 |
| nn            |     1 |
| ta            |     1 |
| ml            |     1 |
| gu            |     1 |
| cy            |     1 |
| syl           |     1 |
| arz           |     1 |
| isv-latn      |     1 |
| wa            |     1 |
| sr-el         |     1 |
+---------------+-------+
102 rows in set (0.030 sec)
```

#### Wikis by categories

```
MariaDB [mhglobal]> SELECT wiki_category, COUNT(*) as COUNT FROM cw_wikis GROUP BY wiki_category ORDER BY COUNT DESC;
+-----------------+-------+
| wiki_category   | COUNT |
+-----------------+-------+
| gaming          |  5210 |
| uncategorised   |  2572 |
| fantasy         |  2365 |
| fandom          |  1778 |
| literature      |  1182 |
| private         |  1137 |
| entertainment   |  1034 |
| community       |   868 |
| education       |   609 |
| history         |   548 |
| software        |   519 |
| music           |   436 |
| politics        |   428 |
| science         |   281 |
| humour          |   260 |
| sport           |   252 |
| langling        |   225 |
| songcontest     |   199 |
| geography       |   172 |
| military        |   154 |
| leisure         |   128 |
| religion        |   116 |
| artarc          |   114 |
| electronics     |    97 |
| media           |    88 |
| medical         |    82 |
| businessfinance |    63 |
| podcast         |    57 |
| automotive      |    51 |
+-----------------+-------+
29 rows in set (0.042 sec)
```

----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:Miscellaneous_Wiki_Stats)**