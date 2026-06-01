# Problem Statement: Japanese Cities' Attributes

## Problem Description
Table: **CITY**

| Column Name | Type |
| :--- | :--- |
| ID | NUMBER |
| NAME | VARCHAR2(17) |
| COUNTRYCODE | VARCHAR2(3) |
| DISTRICT | VARCHAR2(20) |
| POPULATION | NUMBER |

The **CITY** table contains information about various cities across the world. 

Write a query to query all attributes of every Japanese city in the **CITY** table. The **COUNTRYCODE** for Japan is `JPN`.

### Example
**Input (CITY table subset):**
| ID | NAME | COUNTRYCODE | DISTRICT | POPULATION |
| :--- | :--- | :--- | :--- | :--- |
| 1613 | Neyagawa | JPN | Osaka | 257315 |
| 1630 | Ageo | JPN | Saitama | 209400 |
| 3878 | Scottsdale | USA | Arizona | 202705 |

**Output:**
| ID | NAME | COUNTRYCODE | DISTRICT | POPULATION |
| :--- | :--- | :--- | :--- | :--- |
| 1613 | Neyagawa | JPN | Osaka | 257315 |
| 1630 | Ageo | JPN | Saitama | 209400 |

### Explanation
- The problem requests "all attributes," which implies selecting every column from the table.
- Records for Neyagawa and Ageo are returned because their `COUNTRYCODE` matches `'JPN'`. 
- Scottsdale is filtered out because its `COUNTRYCODE` is `'USA'`.

## HackerRank Problem Link
[Japanese Cities' Attributes - HackerRank](https://www.hackerrank.com/challenges/japanese-cities-attributes/problem)

## Solution
```sql
SELECT *
FROM CITY
WHERE COUNTRYCODE = 'JPN';
