# Revising Aggregations - The Sum Function

Query the total population of all cities in **CITY** where District is **California**.

**Input Format**

The **CITY** table is described as follows:

![](../src/1449729804-f21d187d0f-CITY.jpg)

## Submitted Code

```sql
SELECT SUM(POPULATION)
  FROM CITY
 WHERE DISTRICT = 'California';
```
