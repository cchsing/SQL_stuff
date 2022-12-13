# Show the tables for databases in SQL

DESC mysql.user;

1. USE database_name;
2. SHOW tables;

# SELECT records from tables in databases SQL

SELECT column1,column2, ...
FROM database.table;

```
CREATE TABLE table_name (
    column1 datatype,
    column2 datatype,
    column3 datatype,
   ....
);
```

## creates a new table called "TestTables" (which is a copy of the "Customers" table)

```
CREATE TABLE TestTable AS
SELECT customername, contactname
FROM customers;
```
