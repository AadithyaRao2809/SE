# DML Commands


`SELECT {<attribures>} FROM <table_name>` creates a table from the given table with the attributes.
`INSERT INTO <table_name> VALUES(<attributes>, ...)` Creates a new row in the table and adds the attributes listed in the row.
`UPDATE <table_name> SET <condition>` changes the value in the column to the new value specified.
`DELETE FROM <table_name>` removes the entries from the table. Does not change the structure or the memory used by the table.
`WHERE <condition>` is used to specify only some entries of a given table.  Not used standalone, but used along with select, insert, delete, and update commands.

`DISTINCT` is used to select only one distinct value from the table. 
`GROUP BY <attribute>` clause is used along with aggregate functions to create a table of a single group, on which the aggregate function will be applied individually.
`HAVING <condition>` Whenever a condition marked with HAVING clause is true, then only the query will return the result
`ORDER BY` used to sort the results in order. accompanied by `ASC` or `DESC` to denote ascending or descending.
`LIKE` used to query with string matching. `%<str>%` is used to denote ant substring. and the `_` matches any character.

### Set Operations
`UNION` used to combine the result of two SQL statements.
`INTERSECT` gets the data common to the input tables.
`EXCEPT` gets all the rows in the first query bu not in the second query. Set difference operation.
`ALL` can be used along with any set operation. It retains the duplicate entries in the result.


### Aggregate Functions
- `COUNT` counts how many rows are in a particular column.
- `SUM` adds together all the values in a particular column.
- `MIN` and `MAX` return the lowest and highest values in a particular column, respectively.
- `AVG` calculates the average of a group of selected values.

Most commonly used with the `GROUP BY` command to get the aggregation of categories, and not the entire table.

`HAVING` is used to select a group based on a condition. Works the way `WHERE` works on individual records.


 [Join Expressions](join-expressions.md)