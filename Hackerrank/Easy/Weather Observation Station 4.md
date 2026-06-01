# Problem Statement: Weather Observation Station 4

## Problem Description
Table: **STATION**

| Column Name | Type |
| :--- | :--- |
| ID | NUMBER |
| CITY | VARCHAR2(21) |
| STATE | VARCHAR2(2) |
| LAT_N | NUMBER |
| LONG_W | NUMBER |

The **STATION** table contains geographic and location-based data for various weather observation stations.

Find the difference between the total number of **CITY** entries in the table and the number of distinct **CITY** entries in the table.

### Example
For example, if your **STATION** table has four records with **CITY** values 'New York', 'New York', 'White Plains', and 'McLean':
- Total number of city entries: 4
- Number of distinct city entries: 3
- Difference: 4 - 3 = 1

**Output:**
| DIFFERENCE |
| :--- |
| 1 |

## HackerRank Problem Link
[Weather Observation Station 4 - HackerRank](https://www.hackerrank.com/challenges/weather-observation-station-4/problem)

## Solution
```sql
SELECT COUNT(CITY) - COUNT(DISTINCT CITY) AS DIFFERENCE
FROM STATION;
