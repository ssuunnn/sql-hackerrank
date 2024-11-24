# Weather Observation Station 12

Query the list of CITY names from **STATION** that do not start with vowels and do not end with vowels. Your result cannot contain duplicates.

**Input Format**

The **STATION** table is described as follows:

![](../src/1449345840-5f0a551030-Station.jpg)

where LAT_N is the northern latitude and LONG_W is the western longitude.

## Submitted Code

```sql
SELECT DISTINCT CITY
  FROM STATION
 WHERE LEFT(CITY, 1) NOT IN ('A', 'E', 'I', 'O', 'U')
   AND RIGHT(CITY, 1) NOT IN ('a', 'e', 'i', 'o', 'u');
```
