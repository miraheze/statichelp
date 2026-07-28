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
| Month | Approved | Declined | Abandoned | Total requests | % approved |
| --- | --- | --- | --- | --- | --- |
| June 2026 | 1570 | 296 | 387 | 2253 | 73% |
| May 2026 | 1623 | 274 | 311 | 2208 | 74% |
| April 2026 | 1522 | 541 | - | 2064 | 74% |
| March 2026 | 1566 | 585 | - | 2151 | 73% |
| February 2026 | 1422 | 447 | - | 1903 | 75% |
| January 2026 | 1516 | 492 | - | 2009 | 75% |
| December 2025 | 1330 | 457 | - | 1787 | 74% |
| November 2025 | 1259 | 438 | - | 1697 | 74% |
| October 2025 | 1207 | 553 | - | 1760 | 69% |
| September 2025 | 1132 | 527 | - | 1659 | 68% |
| August 2025 | 1274 | 482 | - | 1756 | 73% |
| July 2025 | 1321 | 384 | - | 1705 | 77% |
| June 2025 | 1168 | 257 | - | 1446 | 82% |
| May 2025 | 1245 | 313 | - | 1622 | 80% |
| April 2025 | 1129 | 353 | - | 1482 | 76% |
| March 2025 | 1061 | 452 | - | 1513 | 70% |
| February 2025 | 965 | 334 | - | 1299 | 73% |
| January 2025 | 871 | 299 | - | 1170 | 74% |
| December 2024 | 950 | 245 | - | 1195 | 79% |
| November 2024 | 809 | 256 | - | 1065 | 75% |
| October 2024 | 857 | 301 | - | 1158 | 74% |
| September 2024 | 664 | 432 | - | 1096 | 60% |
NOTE: The number of approved and declined requests don't match up to the total due to the fact that not all requests made in the relevant month are handled within the same month (i.e. requests made on the 30th and 31st might be handled next month).

NOTE: Starting with **22 May 2026**, a new abandoned status was introduced for users who wish to abandon their request or for requests where there has been no response within 5 days to a wiki reviewer's question.

## Raw wiki creation data 

First, let's see how many wiki requests there were at the time I collected the data.
**Date collected: 27 July 2026** (Reception123)
```
MariaDB [metawiki]> SELECT COUNT(*) FROM cw_requests;
+----------+
| COUNT(*) |
+----------+
|    86796 |
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
| CreateWiki AI                                 | 17327 |
| MirahezeGDPR 2a5b022c87c3a6a1efb338a29bca2ba2 |  6014 |
| Jph2                                          |  3902 |
| Reception123                                  |  3862 |
| NotAracham                                    |  3707 |
| DarkMatterMan4500                             |  2577 |
| Agent Isai                                    |  2087 |
| Rodejong                                      |  2076 |
| Doug                                          |  1887 |
| Subwayfares                                   |  1877 |
| Arawynn                                       |  1752 |
| Void                                          |  1737 |
| é–‹æ‹“è€…                                     |  1411 |
| Chrs                                          |  1310 |
| Redmin                                        |  1161 |
| Waki285                                       |  1076 |
| MirahezeGDPR ed559456ed959f58dfc14364b317b1b8 |   726 |
| Zppix                                         |   623 |
| Raidarr                                       |   598 |
| BrandonWM                                     |   523 |
| Examknow                                      |   517 |
| AlvaroMolina                                  |   478 |
| Amanda Catherine                              |   447 |
| RhinosF1                                      |   444 |
| MirahezeGDPR a51581232c7cc84ec1a32c40d8489548 |   440 |
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
| Universal Omega                               |    43 |
| PixDeVl                                       |    43 |
| 1108-Kiju                                     |    41 |
| Sario528                                      |    34 |
| Lawrence-Prairies                             |    27 |
| CircleyDoesExtracter                          |    26 |
| LegoMaster                                    |    26 |
| Aeywoo                                        |    25 |
| GDPRAccount                                   |    25 |
| SleepyMode                                    |    24 |
| Gustave London                                |    22 |
| OrangeStar                                    |    21 |
| Furricane                                     |    20 |
| Samuel                                        |    17 |
| Fungster                                      |    17 |
| ã‚·ãƒ¥ãƒ´ã‚¡ãƒ«ãƒ„                            |    16 |
| Bunnypranav                                   |    14 |
| Corey                                         |    14 |
| Pkbwcgs                                       |    14 |
| XOF                                           |    12 |
| CoolieCoolster                                |    11 |
| Sammy                                         |    11 |
| Wolf                                          |    11 |
| OlegCinema                                    |    10 |
| Eduaddad                                      |     7 |
| TheresNoTime                                  |     6 |
| PetraMagna (Miraheze)                         |     5 |
| ãã‚‰ãŸã“                                  |     5 |
| Alex (Miraheze)                               |     5 |
| Avengium                                      |     4 |
| Integer                                       |     3 |
| CreateWiki Extension                          |     3 |
| SomeRandomDeveloper (Miraheze)                |     1 |
| Labster                                       |     1 |
| TheWWRNerdGuy (Miraheze)                      |     1 |
| Example4                                      |     1 |
+-----------------------------------------------+-------+
88 rows in set (0.464 sec)
```

#### For wikis created between 2024-2026

Proposed alternate script:
```
select actor_name, count(*) as count from logging join actor on actor_id = log_actor where log_type = 'farmer' and log_action = 'createwiki' and LEFT(log_timestamp,4) BETWEEN '2024' AND '2026' group by log_actor order by count desc;

+-----------------------------------------------+-------+
| actor_name                                    | count |
+-----------------------------------------------+-------+
| CreateWiki AI                                 | 17327 |
| NotAracham                                    |  2638 |
| Jph2                                          |  2573 |
| Rodejong                                      |  2076 |
| Subwayfares                                   |  1877 |
| Arawynn                                       |  1752 |
| Reception123                                  |  1544 |
| Waki285                                       |  1044 |
| MirahezeGDPR 2a5b022c87c3a6a1efb338a29bca2ba2 |   619 |
| BrandonWM                                     |   523 |
| Chrs                                          |   463 |
| Redmin                                        |   249 |
| Agent Isai                                    |   118 |
| Raidarr                                       |   100 |
| Pisces                                        |    63 |
| Zeus                                          |    47 |
| Universal Omega                               |    43 |
| PixDeVl                                       |    43 |
| 1108-Kiju                                     |    41 |
| Aeywoo                                        |    25 |
| OrangeStar                                    |    21 |
| Bunnypranav                                   |    14 |
| Zppix                                         |     8 |
| PetraMagna (Miraheze)                         |     5 |
| Alex (Miraheze)                               |     5 |
| CreateWiki Extension                          |     3 |
| SomeRandomDeveloper (Miraheze)                |     1 |
| TheWWRNerdGuy (Miraheze)                      |     1 |
+-----------------------------------------------+-------+
28 rows in set (0.208 sec)
```

#### For wikis declined between 2024-2026

NOTE: **Prior to 2 April 2024, decline was generally used instead of 'needs more details'**
```
MariaDB [metawiki]> select actor_name, count(*) as count from logging join actor on actor_id = log_actor where log_type = 'farmer' and log_action = 'requestdecline' and LEFT(log_timestamp,4) BETWEEN '2024' AND '2026' group by log_actor order by count desc;

+-----------------------------------------------+-------+
| actor_name                                    | count |
+-----------------------------------------------+-------+
| Jph2                                          |  7388 |
| Rodejong                                      |  3561 |
| CreateWiki AI                                 |  1622 |
| NotAracham                                    |  1107 |
| Arawynn                                       |   554 |
| Waki285                                       |   357 |
| BrandonWM                                     |   338 |
| Redmin                                        |   230 |
| Reception123                                  |   185 |
| MirahezeGDPR 2a5b022c87c3a6a1efb338a29bca2ba2 |   181 |
| Zeus                                          |   114 |
| Chrs                                          |    89 |
| Subwayfares                                   |    83 |
| Agent Isai                                    |    55 |
| 1108-Kiju                                     |    38 |
| Pisces                                        |    38 |
| Raidarr                                       |    32 |
| Zppix                                         |    30 |
| PixDeVl                                       |    22 |
| Aeywoo                                        |    21 |
| Bunnypranav                                   |     7 |
| OrangeStar                                    |     6 |
| Skye                                          |     1 |
| Universal Omega                               |     1 |
+-----------------------------------------------+-------+
24 rows in set (0.126 sec)
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
| en            | 21651 |
| es            |   667 |
| ja            |   660 |
| ru            |   646 |
| fr            |   565 |
| pt-br         |   462 |
| de            |   386 |
| zh-cn         |   245 |
| pl            |   240 |
| it            |   224 |
| zh            |   211 |
| zh-hans       |   202 |
| ko            |   196 |
| es-419        |   158 |
| en-gb         |   142 |
| id            |   111 |
| tr            |    99 |
| vi            |    87 |
| uk            |    68 |
| zh-tw         |    58 |
| nl            |    51 |
| pt            |    50 |
| cs            |    49 |
| he            |    48 |
| ar            |    38 |
| zh-hant       |    34 |
| es-formal     |    30 |
| fi            |    29 |
| th            |    28 |
| bn            |    28 |
| hu            |    27 |
| en-ca         |    26 |
| sv            |    22 |
| fa            |    16 |
| ca            |    16 |
| de-at         |    15 |
| no            |    14 |
| da            |    14 |
| el            |    13 |
| ro            |    13 |
| de-formal     |    11 |
| lt            |     9 |
| de-ch         |     9 |
| sk            |     8 |
| bg            |     7 |
| zh-hk         |     6 |
| et            |     6 |
| nb            |     5 |
| ms            |     4 |
| hr            |     4 |
| hy            |     4 |
| hi            |     4 |
| ang           |     3 |
| arz           |     3 |
| sr-el         |     3 |
| be            |     3 |
| frc           |     3 |
| eo            |     3 |
| ml            |     3 |
| ie            |     3 |
| hu-formal     |     3 |
| tl            |     3 |
| gl            |     2 |
| isv-latn      |     2 |
| sr            |     2 |
| rue           |     2 |
| az            |     2 |
| ka            |     2 |
| my            |     2 |
| la            |     2 |
| si            |     2 |
| gan-hans      |     2 |
| sr-ec         |     2 |
| is            |     2 |
| lv            |     2 |
| sl            |     2 |
| grc           |     1 |
| crh-cyrl      |     1 |
| am            |     1 |
| bar           |     1 |
| bbc           |     1 |
| oc            |     1 |
| sq            |     1 |
| ia            |     1 |
| szl           |     1 |
| tg            |     1 |
| as            |     1 |
| rsk           |     1 |
| nan-hant      |     1 |
| bpy           |     1 |
| lad           |     1 |
| mrh           |     1 |
| vmf           |     1 |
| sah           |     1 |
| so            |     1 |
| ta            |     1 |
| zgh           |     1 |
| acm           |     1 |
| frp           |     1 |
| fur           |     1 |
| zh-my         |     1 |
| chn           |     1 |
| syl           |     1 |
| tok           |     1 |
| hak-hans      |     1 |
| ab            |     1 |
| br            |     1 |
| wa            |     1 |
| kk            |     1 |
| zh-mo         |     1 |
| gu            |     1 |
| dtp           |     1 |
| lfn           |     1 |
| bs            |     1 |
| isv           |     1 |
| ht            |     1 |
| fy            |     1 |
| zh-classical  |     1 |
| kw            |     1 |
| lzh           |     1 |
| nl-informal   |     1 |
+---------------+-------+
121 rows in set (0.053 sec)
```

#### Wikis by categories

```
MariaDB [mhglobal]> SELECT wiki_category, COUNT(*) as COUNT FROM cw_wikis GROUP BY wiki_category ORDER BY COUNT DESC;
+-----------------+-------+
| wiki_category   | COUNT |
+-----------------+-------+
| gaming          |  7937 |
| fantasy         |  3171 |
| fandom          |  2720 |
| uncategorised   |  2425 |
| entertainment   |  1487 |
| literature      |  1439 |
| community       |  1133 |
| private         |  1123 |
| history         |   800 |
| education       |   793 |
| music           |   586 |
| software        |   560 |
| politics        |   535 |
| sport           |   374 |
| humour          |   371 |
| langling        |   292 |
| science         |   285 |
| military        |   241 |
| geography       |   240 |
| songcontest     |   232 |
| artarc          |   217 |
| religion        |   137 |
| electronics     |   135 |
| leisure         |   128 |
| media           |   124 |
| businessfinance |    95 |
| medical         |    93 |
| automotive      |    81 |
| podcast         |    61 |
|                 |     4 |
+-----------------+-------+
30 rows in set (0.062 sec)
```

----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:Miscellaneous_Wiki_Stats)**