# Problem Statement: Select By ID

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

Write a query to query all columns for a city in the **CITY** table with the ID `1661`.

### Example
**Input (CITY table subset):**
| ID | NAME | COUNTRYCODE | DISTRICT | POPULATION |
| :--- | :--- | :--- | :--- | :--- |
| 1660 | Serang | IDN | Banten | 618526 |
| 1661 | Sayreville | USA | New Jersey | 42777 |
| 1662 | South River | USA | New Jersey | 15322 |

**Output:**
| ID | NAME | COUNTRYCODE | DISTRICT | POPULATION |
| :--- | :--- | :--- | :--- | :--- |
| 1661 | Sayreville | USA | New Jersey | 42777 |

### Explanation
The query evaluates the dataset to match the precise identifier attribute value. Only the record belonging to Sayreville contains an `ID` equal to `1661`, so all its columns are returned in the output.

## HackerRank Problem Link
[Select By ID - HackerRank](https://www.hackerrank.com/challenges/select-by-id/problem)

## Solution
```sql
SELECT *
FROM CITY
WHERE ID = 1661;
