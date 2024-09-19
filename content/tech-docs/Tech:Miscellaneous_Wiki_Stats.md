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
First, let's see how many wiki requests there were at the time I collected the data.
**Date collected: 27 April 2024** (Reception123)
```
MariaDB [metawiki]> SELECT COUNT(*) FROM cw_requests;
+----------+
| COUNT(*) |
+----------+
|    43747 |
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
| DarkMatterMan4500                             |  2577 |
| Reception123                                  |  2374 |
| MirahezeGDPR                                  |  2034 |
| Jph2                                          |  1994 |
| Doug                                          |  1887 |
| Void                                          |  1737 |
| é–‹æ‹“è€…                                     |  1411 |
| NotAracham                                    |  1255 |
| Redmin                                        |  1035 |
| Chrs                                          |   847 |
| MirahezeGDPR                                  |   726 |
| Zppix                                         |   620 |
| Raidarr                                       |   567 |
| Examknow                                      |   517 |
| AlvaroMolina                                  |   478 |
| BrandonWM                                     |   448 |
| Amanda Catherine                              |   447 |
| RhinosF1                                      |   444 |
| MirahezeGDPR                                  |   440 |
| MacFan4000                                    |   424 |
| MrJaroslavik                                  |   392 |
| TriX                                          |   389 |
| Rodejong                                      |   360 |
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
| Startus                                       |    97 |
| HeartsDo                                      |    94 |
| HispanoBOT                                    |    93 |
| NDKilla                                       |    84 |
| Bonnedav                                      |    76 |
| Cmg                                           |    75 |
| Sau226                                        |    63 |
| Pisces                                        |    57 |
| Centrist16                                    |    52 |
| Megacane                                      |    51 |
| Cy                                            |    44 |
| Bongo Cat                                     |    44 |
| Zeus                                          |    39 |
| Sario528                                      |    34 |
| Waki285                                       |    32 |
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
| 1108-Kiju                                     |    16 |
| Corey                                         |    14 |
| Pkbwcgs                                       |    14 |
| XOF                                           |    12 |
| CoolieCoolster                                |    11 |
| Universal Omega                               |    11 |
| Sammy                                         |    11 |
| Wolf                                          |    11 |
| OlegCinema                                    |    10 |
| PixDeVl                                       |     8 |
| Eduaddad                                      |     7 |
| TheresNoTime                                  |     6 |
| ãã‚‰ãŸã“                                  |     5 |
| Avengium                                      |     4 |
| Integer                                       |     3 |
| Labster                                       |     1 |
| Alex (Miraheze)                               |     1 |
| Example4                                      |     1 |
+-----------------------------------------------+-------+
79 rows in set (0.283 sec)
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
| Jph2                                          |  1994 |
| NotAracham                                    |  1255 |
| DarkMatterMan4500                             |  1255 |
| MirahezeGDPR                                  |  1239 |
| Chrs                                          |   631 |
| Redmin                                        |   501 |
| Raidarr                                       |   482 |
| MirahezeGDPR                                  |   450 |
| BrandonWM                                     |   448 |
| Rodejong                                      |   360 |
| MirahezeGDPR                                  |   292 |
| Zppix                                         |   261 |
| Reception123                                  |   247 |
| Void                                          |   135 |
| Doug                                          |    73 |
| Hispano76                                     |    66 |
| Pisces                                        |    57 |
| Bongo Cat                                     |    44 |
| Startus                                       |    43 |
| Zeus                                          |    39 |
| OrangeStar                                    |    21 |
| Msnhinet8                                     |    20 |
| 1108-Kiju                                     |    16 |
| Universal Omega                               |    11 |
| PixDeVl                                       |     8 |
| Sario528                                      |     6 |
| RhinosF1                                      |     5 |
| Avengium                                      |     2 |
| ã‚·ãƒ¥ãƒ´ã‚¡ãƒ«ãƒ„                            |     2 |
| Alex (Miraheze)                               |     1 |
| John                                          |     1 |
+-----------------------------------------------+-------+
32 rows in set (0.101 sec)
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

```
MariaDB [metawiki]> select actor_name, count(*) as count from logging join actor on actor_id = log_actor where log_type = 'farmer' and log_action = 'requestdecline' and (log_timestamp like '2022%' or log_timestamp like '2023%') group by log_actor order by count desc;
+-----------------------------------------------+-------+
| actor_name                                    | count |
+-----------------------------------------------+-------+
| Tali64Â³                                      |  1910 |
| MirahezeGDPR                                  |  1543 |
| DarkMatterMan4500                             |   866 |
| Jph2                                          |   803 |
| NotAracham                                    |   583 |
| Chrs                                          |   290 |
| Redmin                                        |   205 |
| Zppix                                         |   154 |
| Raidarr                                       |   115 |
| Reception123                                  |    75 |
| Startus                                       |    69 |
| Doug                                          |    62 |
| MirahezeGDPR                                  |    57 |
| MirahezeGDPR                                  |    50 |
| Void                                          |    35 |
| Bongo Cat                                     |    16 |
| Hispano76                                     |     7 |
| RhinosF1                                      |     4 |
| Msnhinet8                                     |     2 |
| HeartsDo                                      |     2 |
| Amanda Catherine                              |     1 |
| Avengium                                      |     1 |
+-----------------------------------------------+-------+
22 rows in set (0.061 sec)
```

#### Wikis by languages

```
MariaDB [mhglobal]> SELECT wiki_language, COUNT(*) as COUNT FROM cw_wikis GROUP BY wiki_language ORDER BY COUNT DESC;
+---------------+-------+
| wiki_language | COUNT |
+---------------+-------+
| en            |  8778 |
| ru            |   280 |
| ja            |   260 |
| fr            |   254 |
| es            |   222 |
| pl            |   147 |
| de            |   147 |
| pt-br         |   139 |
| it            |   119 |
| zh            |    98 |
| ko            |    90 |
| zh-cn         |    75 |
| en-gb         |    74 |
| zh-hans       |    46 |
| nl            |    42 |
| es-419        |    33 |
| zh-tw         |    33 |
| tr            |    30 |
| uk            |    27 |
| cs            |    27 |
| pt            |    26 |
| he            |    23 |
| zh-hant       |    21 |
| bn            |    20 |
| fi            |    18 |
| id            |    17 |
| hu            |    17 |
| vi            |    15 |
| sv            |    15 |
| ar            |    11 |
| es-formal     |    11 |
| th            |    10 |
| ro            |    10 |
| no            |     8 |
| en-ca         |     8 |
| de-formal     |     8 |
| ca            |     8 |
| sk            |     7 |
| el            |     5 |
| zh-hk         |     4 |
| bg            |     4 |
| nb            |     4 |
| de-at         |     4 |
| gl            |     3 |
| da            |     3 |
| de-ch         |     3 |
| hy            |     2 |
| eo            |     2 |
| et            |     2 |
| fur           |     2 |
| als           |     2 |
| tl            |     2 |
| frc           |     2 |
| lt            |     2 |
| kk            |     2 |
| sr-el         |     2 |
| ms            |     2 |
| fa            |     2 |
| zh-mo         |     1 |
| cy            |     1 |
| sl            |     1 |
| hr            |     1 |
| ryu           |     1 |
| zh-min-nan    |     1 |
| az            |     1 |
| rsk           |     1 |
| zh-my         |     1 |
| bar           |     1 |
| mk            |     1 |
| sq            |     1 |
| my            |     1 |
| hi            |     1 |
| qbg           |     1 |
| arz           |     1 |
| br            |     1 |
| zh-classical  |     1 |
| ab            |     1 |
| tok           |     1 |
| lfn           |     1 |
| isv           |     1 |
| hu-formal     |     1 |
| ka            |     1 |
| ike-cans      |     1 |
| kk-kz         |     1 |
| simple        |     1 |
+---------------+-------+
85 rows in set (0.017 sec)
```

#### Wikis by categories

```
MariaDB [mhglobal]> SELECT wiki_category, COUNT(*) as COUNT FROM cw_wikis GROUP BY wiki_category ORDER BY COUNT DESC;
+-----------------+-------+
| wiki_category   | COUNT |
+-----------------+-------+
| gaming          |  2587 |
| fantasy         |  1522 |
| uncategorised   |  1218 |
| fandom          |  1078 |
| private         |   772 |
| literature      |   733 |
| entertainment   |   616 |
| community       |   566 |
| education       |   386 |
| software        |   338 |
| music           |   294 |
| history         |   259 |
| politics        |   257 |
| humour          |   196 |
| science         |   156 |
| sport           |   143 |
| langling        |   139 |
| songcontest     |   123 |
| geography       |   104 |
| leisure         |    85 |
| military        |    71 |
| religion        |    70 |
| artarc          |    69 |
| electronics     |    62 |
| media           |    59 |
| medical         |    40 |
| businessfinance |    34 |
| podcast         |    34 |
| automotive      |    30 |
+-----------------+-------+
29 rows in set (0.025 sec)
```



----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:Miscellaneous_Wiki_Stats)**