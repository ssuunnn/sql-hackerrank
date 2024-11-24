# Weather Observation Station 15

Query the Western Longitude (LONG_W) for the largest Northern Latitude (LAT_N) in **STATION** that is less than $137.2345$. Round your answer to $4$ decimal places.

**Input Format**

The **STATION** table is described as follows:

![](../src/1449345840-5f0a551030-Station.jpg)

where LAT_N is the northern latitude and LONG_W is the western longitude.

## Submitted Code

```sql
SELECT ROUND(LONG_W, 4)
  FROM STATION
 WHERE LAT_N = (SELECT MAX(LAT_N)
                  FROM STATION
                 WHERE LAT_N < 137.2345);
```
