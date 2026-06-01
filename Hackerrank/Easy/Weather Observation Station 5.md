# Problem Statement: Weather Observation Station 5

## Problem Description
Table: **STATION**

| Column Name | Type |
| :--- | :--- |
| ID | NUMBER |
| CITY | VARCHAR2(21) |
| STATE | VARCHAR2(2) |
| LAT_N | NUMBER |
| LONG_W | NUMBER |

The **STATION** table contains geographic and location-based data for various weather observation stations[cite: 7].

Query the two cities in **STATION** with the shortest and longest **CITY** names, as well as their respective lengths (i.e.: number of characters in the name). If there is more than one smallest or largest city, choose the one that comes first alphabetically.

### Example
For example, if the **CITY** names are 'AMP', 'ABC', 'PQRS' and 'WXYZ':
- Shortest entries are 'AMP' and 'ABC' (length 3). Alphabetically, 'ABC' comes first.
- Longest entries are 'PQRS' and 'WXYZ' (length 4). Alphabetically, 'PQRS' comes first.

**Output:**
| CITY | LENGTH |
| :--- | :--- |
| ABC | 3 |
| PQRS | 4 |

## HackerRank Problem Link
[Weather Observation Station 5 - HackerRank](https://www.hackerrank.com/challenges/weather-observation-station-5/problem)

## Solution Explanation
Because standard SQL does not natively return multiple distinct rows with differing structural logic in a single simple clause without a union, this problem is best solved by running two separate queries (or combining them with a UNION operator depending on your environment preferences).

1. `LENGTH(CITY)`: This string function calculates the exact number of characters within each city string.

2. `ORDER BY LENGTH(CITY) ASC, CITY ASC`:

    - The primary sorting layer groups records by name length from shortest to longest (ASC).

    - The secondary tie-breaking sorting layer uses CITY ASC, which organizes rows alphabetically. This ensures that if multiple cities share the shortest length (e.g., 'ABC' and 'AMP'), the alphabetical index forces 'ABC' to the top.

3. `LIMIT 1`: Instructs the execution engine to slice the sorted dataset and isolate only the top row (the single shortest alphabetical city).

4. `ORDER BY LENGTH(CITY) DESC, CITY ASC`: Works identically for the second query, but reverses the primary sort criteria (DESC) to bring the longest city names to the peak of the result pipeline while keeping the tie-breaking alphabetical filter (CITY ASC) active.

## Solution
```sql
-- Query for the shortest city name
SELECT CITY, LENGTH(CITY)
FROM STATION
ORDER BY LENGTH(CITY) ASC, CITY ASC
LIMIT 1;

-- Query for the longest city name
SELECT CITY, LENGTH(CITY)
FROM STATION
ORDER BY LENGTH(CITY) DESC, CITY ASC
LIMIT 1;

