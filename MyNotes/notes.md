- there is a operator type named `NOT BETWEEN 1 AND 10` which is used to choose datas lesser then 1 and greater than 10 just the opposite of `BETWEEN 1 AND 10`

- col_name `IN` (2,3,4,5) --> only take column names which are 2,3,4,5 an the opposite of it is col_name `NOT IN` (2,3,4,5)

- LIMIT num_limit OFFSET num_offset(exclusive);---> whereas limit tells us how amny rows to take , the `offset` tells us from which row number we should start taking the rows.

- inserting datas from one table to another table
```sql
INSERT INTO <dest_table> (col1,col2,col3,..) -- VALUES is not written in case of taking input from a diff table
SELECT
id,
first_name,
NULL, -- as if column does not exist
'unknown' -- again if the column doesn't exist in src table
FROM <src_table>

```
- there is a function named `UPPER()` to change it to uppercase.