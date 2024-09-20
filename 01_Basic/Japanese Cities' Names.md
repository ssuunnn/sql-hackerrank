# Japanese Cities' Names

Query the names of all the Japanese cities in the **CITY** table. The **COUNTRYCODE** for Japan is `JPN`.

The **CITY** table is described as follows:

![](../src/1449729804-f21d187d0f-CITY.jpg)

## Submitted Code

```sql
SELECT NAME FROM CITY WHERE COUNTRYCODE = 'JPN';
```
