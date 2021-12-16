# Create table

* The `CREATE TABLE` instruction allows you to create a new table in the database.
* When creating a new table you need to provide the table name along with its column names, column definition and constraints.
* The column definition refers to the column data type and properties.

Simple syntax:

```sql
DROP TABLE IF EXISTS TableName;

CREATE TABLE TableName
(
    Id INT NOT NULL PRIMARY KEY, -- Primary Key column
    ColumnName2 VARCHAR(50) NOT NULL,
    ColumnName3 VARCHAR(50) NOT NULL
);
```

You can create table with default charset:

```sql
CREATE TABLE IF NOT EXISTS TableName (
    Id INT NOT NULL PRIMARY KEY,
    ColumnName2 VARCHAR(50) NOT NULL,
    ColumnName3 VARCHAR(50) NOT NULL
) DEFAULT CHARACTER SET utf8 COLLATE utf8_bin;
```