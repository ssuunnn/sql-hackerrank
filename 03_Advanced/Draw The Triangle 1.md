# Draw The Triangle 1

P(R) represents a pattern drawn by Julia in R rows. The following pattern represents P(5):

```
* * * * * 
* * * * 
* * * 
* * 
*
```

Write a query to print the pattern P(20).

## Submitted Code

```sql
 SELECT RPAD('*', (2 * LEVEL) - 1, ' *')
   FROM DUAL
CONNECT BY LEVEL <= 20
  ORDER BY LEVEL DESC;
```
