# Drop table

The *DROP TABLE* statement removes a table and its data permanently from the database.

In MySQL, you can also remove multiple tables using a single DROP TABLE statement, each table is separated by a comma.

```sql 
DROP TABLE [ IF EXISTS ] { database_name.table_name | table_name } [ ,...n ]; 
```

Example:

```sql
CREATE TABLE T1 (Col1 INT);  
DROP TABLE IF EXISTS T1;
```

Note: Try to use *CREATE OR REPLACE TABLE*. It shoul work in MariaDB, but not sure if it works in MySQL
