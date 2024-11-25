# Average Population of Each Continent

Given the **CITY** and **COUNTRY** tables, query the names of all the continents (COUNTRY.Continent) and their respective average city populations (CITY.Population) rounded down to the nearest integer.

**Note:** CITY.CountryCode and COUNTRY.Code are matching key columns.

**Input Format**

The **CITY** and **COUNTRY** tables are described as follows:

![](../src/1449729804-f21d187d0f-CITY.jpg)

![](../src/1449769013-e54ce90480-Country.jpg)

## Submitted Code

```sql
SELECT COUNTRY.CONTINENT, ROUND(AVG(CITY.POPULATION), 0)
  FROM CITY, COUNTRY
 WHERE CITY.COUNTRYCODE = COUNTRY.CODE
 GROUP BY COUNTRY.CONTINENT;
```
