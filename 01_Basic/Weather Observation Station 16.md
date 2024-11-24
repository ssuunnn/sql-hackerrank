# Weather Observation Station 16

Query the smallest Northern Latitude (LAT_N) from **STATION** that is greater than $38.7780$. Round your answer to $4$ decimal places.

**Input Format**

The **STATION** table is described as follows:

![](../src/1449345840-5f0a551030-Station.jpg)

where LAT_N is the northern latitude and LONG_W is the western longitude.

## Submitted Code

```sql
SELECT ROUND(MIN(LAT_N), 4)
  FROM STATION
 WHERE LAT_N > 38.7780;
```
