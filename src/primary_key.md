# Primary key

* The *PRIMARY KEY* constraint allows you to define a primary key of a table when you create or alter table.
* Typically, you define the primary key for a table in the *CREATE TABLE* statement.
* If a table, for some reasons, does not have a primary key, you can use the *ALTER TABLE* statement to add a primary key.

```sql
CREATE TABLE table_name (
    primary_key_column INT AUTO_INCREMENT PRIMARY KEY NOT NULL,
    col2 col2_definition,
    col3 col3_definition
);
```

```sql
ALTER TABLE table_name
   ADD CONSTRAINT PK_table_name_Id PRIMARY KEY(primary_key_column);
```

Limitations and Restrictions:
* A table can contain only one *PRIMARY KEY* constraint.
* All columns defined within a *PRIMARY KEY* constraint must be defined as *NOT NULL*.
