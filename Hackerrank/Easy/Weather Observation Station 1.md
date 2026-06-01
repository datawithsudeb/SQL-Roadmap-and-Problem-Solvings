# Problem Statement: Weather Observation Station 1

## Problem Description
Table: **STATION**

| Column Name | Type |
| :--- | :--- |
| ID | NUMBER |
| CITY | VARCHAR2(21) |
| STATE | VARCHAR2(2) |
| LAT_N | NUMBER |
| LONG_W | NUMBER |

The **STATION** table contains geographic and location-based data for various weather observation stations. Where **LAT_N** is the northern latitude and **LONG_W** is the western longitude.

Write a query to print a list of **CITY** and **STATE** from the **STATION** table.

### Example
**Input (STATION table subset):**
| ID | CITY | STATE | LAT_N | LONG_W |
| :--- | :--- | :--- | :--- | :--- |
| 794 | Kissee Mills | MO | 139.65 | 118.90 |
| 824 | Loma Mar | CA | 48.74 | 134.12 |
| 603 | Sandy Hook | CT | 72.10 | 114.33 |

**Output:**
| CITY | STATE |
| :--- | :--- |
| Kissee Mills | MO |
| Loma Mar | CA |
| Sandy Hook | CT |

### Explanation
The problem requires returning a structured directory containing only two specific attributes from the dataset: the name of the municipality (`CITY`) and its corresponding regional subdivision (`STATE`). Other metrics like geographic identifiers (`ID`) and coordinate boundaries (`LAT_N`, `LONG_W`) are omitted from the projection.

## HackerRank Problem Link
[Weather Observation Station 1 - HackerRank](https://www.hackerrank.com/challenges/weather-observation-station-1/problem)

## Solution
```sql
SELECT CITY, STATE
FROM STATION;
