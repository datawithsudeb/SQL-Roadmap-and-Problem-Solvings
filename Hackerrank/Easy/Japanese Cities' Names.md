# Problem Statement: Japanese Cities' Names

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

Write a query to query the **NAME** of all Japanese cities in the **CITY** table. The **COUNTRYCODE** for Japan is `JPN`.

### Example
**Input (CITY table subset):**
| ID | NAME | COUNTRYCODE | DISTRICT | POPULATION |
| :--- | :--- | :--- | :--- | :--- |
| 1613 | Neyagawa | JPN | Osaka | 257315 |
| 1630 | Ageo | JPN | Saitama | 209400 |
| 3878 | Scottsdale | USA | Arizona | 202705 |

**Output:**
| NAME |
| :--- |
| Neyagawa |
| Ageo |

### Explanation
- The problem specifically requests only the names of the cities, meaning only the `NAME` column should be returned.
- Records for Neyagawa and Ageo are included because their `COUNTRYCODE` matches `'JPN'`.
- Scottsdale is filtered out because its `COUNTRYCODE` is `'USA'`.

## HackerRank Problem Link
[Japanese Cities' Names - HackerRank](https://www.hackerrank.com/challenges/japanese-cities-name/problem)

## Solution
```sql
SELECT NAME
FROM CITY
WHERE COUNTRYCODE = 'JPN';
