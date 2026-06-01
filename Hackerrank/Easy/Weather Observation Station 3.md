# Problem Statement: Weather Observation Station 3

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

Write a query to print a list of **CITY** names from **STATION** for cities that have an **even ID number**. Print the results in any order, but exclude duplicates from the answer.

### Example
**Input (STATION table subset):**
| ID | CITY | STATE | LAT_N | LONG_W |
| :--- | :--- | :--- | :--- | :--- |
| 21 | Kissee Mills | MO | 139.65 | 118.90 |
| 22 | Loma Mar | CA | 48.74 | 134.12 |
| 24 | Loma Mar | CA | 48.74 | 134.12 |
| 26 | Sandy Hook | CT | 72.10 | 114.33 |

**Output:**
| CITY |
| :--- |
| Loma Mar |
| Sandy Hook |

### Explanation
- The city `Kissee Mills` is excluded because its `ID` (21) is odd.
- The city `Loma Mar` appears twice in the filtered dataset (with even IDs 22 and 24), but due to the duplicate exclusion constraint, it is listed only once in the final output.
- The city `Sandy Hook` is included because its `ID` (26) is even.

## HackerRank Problem Link
[Weather Observation Station 3 - HackerRank](https://www.hackerrank.com/challenges/weather-observation-station-3/problem)

## Solution
```sql
SELECT DISTINCT CITY
FROM STATION
WHERE MOD(ID, 2) = 0;
