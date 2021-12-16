# Alter table

The *ALTER TABLE ADD* statement allows you to add one or more columns to a table.

```sql
ALTER TABLE TableName
    ADD NewColumnName /*new_column_name*/ int /*new_column_datatype*/ NULL /*new_column_nullability*/;
```

The *ALTER TABLE DROP* statement allows you to remove one or more columns from a table.

```sql
ALTER TABLE TableName
    DROP COLUMN ColumnName;
```

The *ALTER TABLE MODIFY COLUMN* statement allows you to update one or more columns.

```sql
ALTER TABLE HelloWorld 
    ADD Email varchar(255);

ALTER TABLE HelloWorld 
    MODIFY COLUMN Email varchar(300);
```

It is possible to put column before or after existing column:

```sql
ALTER TABLE table_name
  MODIFY column_name column_definition
    [ FIRST | AFTER column_name ],
  MODIFY column_name column_definition
    [ FIRST | AFTER column_name ],
  ...
;
```

It is possible to rename column as well, e.g.:

```sql
ALTER TABLE tablename CHANGE col1 newcol1 VARCHAR(50);
```

or 

```sql
ALTER TABLE tablename RENAME COLUMN id TO new_id;
```

You can rename table name as well:

```sql
RENAME TABLE
    tbl_name TO new_tbl_name
    [, tbl_name2 TO new_tbl_name2] ...
```