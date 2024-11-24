# Average Population

Query the average population for all cities in **CITY**, rounded down to the nearest integer.

**Input Format**

The **CITY** table is described as follows:

![](../src/1449729804-f21d187d0f-CITY.jpg)

## Submitted Code

```sql
SELECT ROUND(AVG(POPULATION), 0)
  FROM CITY;
```
