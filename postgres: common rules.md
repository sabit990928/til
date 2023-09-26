GROUP BY

Each column in the `SELECT` statement should either be called in an aggregate function or be in the `GROUP BY` clause.

[Nice and simple explanation](https://learnsql.com/blog/not-a-group-by-expression-error/).

Remember that in the database, an SQL SELECT statement always executes in this order:

```psql
    FROM
    WHERE
    GROUP BY
    HAVING
    SELECT
    ORDER BY
```
