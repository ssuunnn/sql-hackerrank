# Japan Population

Query the sum of the populations for all Japanese cities in **CITY**. The COUNTRYCODE for Japan is **JPN**.

**Input Format**

The **CITY** table is described as follows:

![](../src/1449729804-f21d187d0f-CITY.jpg)

## Submitted Code

```sql
SELECT SUM(POPULATION)
  FROM CITY
 WHERE COUNTRYCODE = 'JPN';
```
