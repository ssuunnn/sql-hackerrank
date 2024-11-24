# Revising Aggregations - The Count Function

Query a count of the number of cities in **CITY** having a Population larger than $100,000$.

**Input Format**

The **CITY** table is described as follows:

![](../src/1449729804-f21d187d0f-CITY.jpg)

## Submitted Code

```sql
SELECT COUNT(*)
  FROM CITY
 WHERE POPULATION > 100000;
```
