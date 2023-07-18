structured query language

flat file database 

relational database - store a lot of information
store data in rows and columns; tables 

C reating data (insert)
R eading data (select)
U pdating data (update)
D deleting data (delete and drop)

CREATE TABLE table (column type, ...)

sqlite3 to create a brand new database

```sql
sqlite3 favorites.db

.mode csv

.import favorites.csv favorites

.schema
```

SELECT columns FROM table;

SQL functions:
- AVG
- COUNT
- DISTINCT
- LOWER
- MAX
- MIN
- UPPER

- WHERE
- LIKE
- ORDER BY
- LIMIT
- GROUP BY

data types
- blob
- integer
- numeric
- real (aka float)
- text

cells in this column may/not be NULL