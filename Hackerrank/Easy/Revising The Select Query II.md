# Problem Statement: Revising the Select Query II

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

Write a query to query the **NAME** field for all American cities in the **CITY** table with populations larger than 120,000. The **CountryCode** for America is `USA`.

### Example
**Input (CITY table subset):**
| ID | NAME | COUNTRYCODE | DISTRICT | POPULATION |
| :--- | :--- | :--- | :--- | :--- |
| 3878 | Scottsdale | USA | Arizona | 202705 |
| 3965 | Corona | USA | California | 124966 |
| 3973 | Concord | USA | California | 121780 |
| 3977 | Cedar Rapids | USA | Iowa | 120758 |

**Output:**
| NAME |
| :--- |
| Scottsdale |
| Corona |
| Concord |

### Explanation
- Scottsdale (202,705), Corona (124,966), and Concord (121,780) are all located in the USA and have populations strictly greater than 120,000. Their names are returned.
- Cedar Rapids (120,758) is excluded because its population does not exceed the 120,000 threshold.
- Unlike the previous challenge, only the `NAME` column is requested in the output, rather than all columns.

## HackerRank Problem Link
[Revising the Select Query II - HackerRank](https://www.hackerrank.com/challenges/revising-the-select-query-2/problem)

## Solution
```sql
SELECT NAME
FROM CITY
WHERE COUNTRYCODE = 'USA' 
  AND POPULATION > 120000;
