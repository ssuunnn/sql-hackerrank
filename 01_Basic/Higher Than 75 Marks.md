# Higher Than 75 Marks

Query the Name of any student in **STUDENTS** who scored higher than $75$ Marks. Order your output by the last three characters of each name. If two or more students both have names ending in the same last three characters (i.e.: Bobby, Robby, etc.), secondary sort them by ascending ID.

**Input Format**

The **STUDENTS** table is described as follows:

![](../src/1443815243-94b941f556-1.png)

The Name column only contains uppercase (`A`-`Z`) and lowercase (`a`-`z`) letters.

**Sample Input**

![](../src/1443815209-cf4b260993-2.png)

**Sample Output**

```
Ashley
Julia
Belvet
```

**Explanation**

Only Ashley, Julia, and Belvet have Marks > $75$. If you look at the last three characters of each of their names, there are no duplicates and 'ley' < 'lia' < 'vet'.

## Submitted Code

```sql
SELECT Name
  FROM STUDENTS
 WHERE Marks > 75
 ORDER BY SUBSTR(Name, -3), ID;
```
