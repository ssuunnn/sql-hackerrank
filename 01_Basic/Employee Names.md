# Employee Names

Write a query that prints a list of employee names (i.e.: the name attribute) from the **Employee** table in alphabetical order.

**Input Format**

The **Employee** table containing employee data for a company is described as follows:

![](../src/1458557872-4396838885-ScreenShot2016-03-21at4.27.13PM.png)

where employee_id is an employee's ID number, name is their name, months is the total number of months they've been working for the company, and salary is their monthly salary.

**Sample Input**

![](../src/1458558202-9a8721e44b-ScreenShot2016-03-21at4.32.59PM.png)

**Sample Output**

```
Angela
Bonnie
Frank
Joe
Kimberly
Lisa
Michael
Patrick
Rose
Todd
```

## Submitted Code

```sql
SELECT name
  FROM Employee
 ORDER BY name;
```
