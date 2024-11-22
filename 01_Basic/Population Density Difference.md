# Population Density Difference

Query the difference between the maximum and minimum populations in **CITY**.

**Input Format**

The **CITY** table is described as follows:

![](../src/1449729804-f21d187d0f-CITY.jpg)

## Submitted Code

```sql
SELECT MAX(POPULATION) - MIN(POPULATION)
  FROM CITY;
```
