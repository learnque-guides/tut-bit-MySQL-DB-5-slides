# Foreign key

* A foreign key is a column or group of columns in a table that links to a column or group of columns in another table. The foreign key places constraints in the related tables, so database can maintain referential integrity.
* The table containing the foreign key is called the child table, and the referenced table is the parent table.
* Typically, the foreign key columns of the child table often refer to the primary key columns of the parent table.

```sql
CREATE TABLE Trailers (
    Id INT IDENTITY(1,1) NOT NULL AUTO_INCREMENT PRIMARY KEY,
    Number VARCHAR(50) NOT NULL,
    CarId INT, 
    FOREIGN KEY(CarId) REFERENCES Cars(Id)
);
```

```sql
ALTER TABLE tbl_name
    ADD [CONSTRAINT [symbol]] FOREIGN KEY
    [index_name] (col_name, ...)
    REFERENCES tbl_name (col_name,...)
    [ON DELETE reference_option]
    [ON UPDATE reference_option]
```

* A table can have more than one foreign key where each foreign key references to a primary key of the different parent tables.
* Once a foreign key constraint is in place, the foreign key columns from the child table must have the corresponding row in the parent key columns of the parent table or values in these foreign key columns must be *NULL*.
