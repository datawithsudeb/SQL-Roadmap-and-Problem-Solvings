# Problem Statement: Select All

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

Write a query to query all columns for every row in the **CITY** table.

### Example
**Input (CITY table subset):**
| ID | NAME | COUNTRYCODE | DISTRICT | POPULATION |
| :--- | :--- | :--- | :--- | :--- |
| 6 | Rotterdam | NLD | Zuid-Holland | 593321 |
| 3878 | Scottsdale | USA | Arizona | 202705 |

**Output:**
| ID | NAME | COUNTRYCODE | DISTRICT | POPULATION |
| :--- | :--- | :--- | :--- | :--- |
| 6 | Rotterdam | NLD | Zuid-Holland | 593321 |
| 3878 | Scottsdale | USA | Arizona | 202705 |

### Explanation
The requirement specifies that all columns (`ID`, `NAME`, `COUNTRYCODE`, `DISTRICT`, and `POPULATION`) must be pulled for every single row present in the table without applying any structural or value-based criteria constraints.

## HackerRank Problem Link
[Select All - HackerRank](https://www.hackerrank.com/challenges/select-all-by-id/problem)

## Solution
```sql
SELECT *
FROM CITY;
