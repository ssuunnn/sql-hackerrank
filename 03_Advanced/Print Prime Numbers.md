# Print Prime Numbers

Write a query to print all prime numbers less than or equal to $1000$. Print your result on a single line, and use the ampersand ($\&$) character as your separator (instead of a space).

For example, the output for all prime numbers $\leq 10$ would be:

```
2&3&5&7
```

## Submitted Code

```sql
  WITH NUM_LIST AS ( SELECT LEVEL AS NUM
                       FROM DUAL
                    CONNECT BY LEVEL <= 1000)
SELECT LISTAGG(T.NUM, '&') WITHIN GROUP(ORDER BY T.NUM)
  FROM (SELECT N1.NUM
          FROM NUM_LIST N1, NUM_LIST N2
         WHERE MOD(N1.NUM, N2.NUM) = 0
         GROUP BY N1.NUM
        HAVING COUNT(N1.NUM) = 2) T;
```
