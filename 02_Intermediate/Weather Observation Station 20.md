# Weather Observation Station 20

A [median](https://en.wikipedia.org/wiki/Median) is defined as a number separating the higher half of a data set from the lower half. Query the median of the Northern Latitudes (LAT_N) from **STATION** and round your answer to $4$ decimal places.

**Input Format**

The **STATION** table is described as follows:

![](../src/1449345840-5f0a551030-Station.jpg)

where LAT_N is the northern latitude and LONG_W is the western longitude.

## Submitted Code

```sql
SELECT ROUND(AVG(LAT_N), 4)
  FROM (SELECT LAT_N,
               ROW_NUMBER() OVER(ORDER BY LAT_N) AS ROW_NUM,
               COUNT(LAT_N) OVER() AS N
          FROM STATION) T
 WHERE CASE WHEN MOD(N, 2) = 1
                 THEN ROW_NUM = (N+1)/2
                 ELSE ROW_NUM IN (N/2, (N/2)+1)
        END;
```
