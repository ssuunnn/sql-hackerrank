# Top Earners

We define an employee's total earnings to be their monthly $salary \times months$ worked, and the maximum total earnings to be the maximum total earnings for any employee in the **Employee** table. Write a query to find the maximum total earnings for all employees as well as the total number of employees who have maximum total earnings. Then print these values as $2$ space-separated integers.

**Input Format**

The **Employee** table containing employee data for a company is described as follows:

![](../src/1458557872-4396838885-ScreenShot2016-03-21at4.27.13PM.png)

where employee_id is an employee's ID number, name is their name, months is the total number of months they've been working for the company, and salary is the their monthly salary.

**Sample Input**

![](../src/1458558202-9a8721e44b-ScreenShot2016-03-21at4.32.59PM.png)

**Sample Output**

```
69952 1
```

**Explanation**

The table and earnings data is depicted in the following diagram:

![](../src/1458559218-9f37585c7a-ScreenShot2016-03-21at4.49.23PM.png)

The maximum earnings value is $69952$. The only employee with earnings $=69952$ is Kimberly, so we print the maximum earnings value ($69952$) and a count of the number of employees who have earned $\$69952$ (which is $1$) as two space-separated values.

## Submitted Code

```sql
SELECT MAX(months * salary), COUNT(*)
  FROM Employee
 WHERE months * salary = (SELECT MAX(months * salary)
                            FROM Employee);
```
