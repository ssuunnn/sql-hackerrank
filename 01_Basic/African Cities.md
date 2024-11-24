# African Cities

Given the **CITY** and **COUNTRY** tables, query the names of all cities where the CONTINENT is 'Africa'.

**Note:** CITY.CountryCode and COUNTRY.Code are matching key columns.

**Input Format**

The **CITY** and **COUNTRY** tables are described as follows:

![](../src/1449729804-f21d187d0f-CITY.jpg)

![](../src/1449769013-e54ce90480-Country.jpg)

## Submitted Code

```sql
SELECT CITY.NAME
  FROM CITY, COUNTRY
 WHERE CITY.COUNTRYCODE = COUNTRY.CODE
   AND COUNTRY.CONTINENT = 'Africa';
```
