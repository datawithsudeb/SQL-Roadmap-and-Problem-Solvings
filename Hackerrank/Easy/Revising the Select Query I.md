# Problem Statement: Revising the Select Query I

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

Write a query to query all columns for all American cities in the **CITY** table with populations larger than 100,000. The **CountryCode** for America is `USA`.

### Example
**Input (CITY table subset):**
| ID | NAME | COUNTRYCODE | DISTRICT | POPULATION |
| :--- | :--- | :--- | :--- | :--- |
| 6 | Rotterdam | NLD | Zuid-Holland | 593321 |
| 3878 | Scottsdale | USA | Arizona | 202705 |
| 3965 | Corona | USA | California | 124966 |
| 3973 | Concord | USA | California | 121780 |
| 3977 | Cedar Rapids | USA | Iowa | 120758 |

**Output:**
| ID | NAME | COUNTRYCODE | DISTRICT | POPULATION |
| :--- | :--- | :--- | :--- | :--- |
| 3878 | Scottsdale | USA | Arizona | 202705 |
| 3965 | Corona | USA | California | 124966 |
| 3973 | Concord | USA | California | 121780 |
| 3977 | Cedar Rapids | USA | Iowa | 120758 |

### Explanation
- Cities like Scottsdale, Corona, Concord, and Cedar Rapids are returned because their `COUNTRYCODE` is `'USA'` and their `POPULATION` strictly exceeds `100000`.
- Rotterdam is excluded because its `COUNTRYCODE` is `'NLD'`, even though its population is over 100,000.

## HackerRank Problem Link
[Revising the Select Query I - HackerRank](https://www.hackerrank.com/challenges/revising-the-select-query/problem)

## Solution
```sql
SELECT *
FROM CITY
WHERE COUNTRYCODE = 'USA' 
  AND POPULATION > 100000;
