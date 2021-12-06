# Check constraint

*CHECK* constraints reject values that evaluate to FALSE.

It only check for TRUE and FALSE. NULL will be ignored.

```sql
-- Create the table in the specified schema
CREATE TABLE Drinks
(
    Id INT NOT NULL PRIMARY KEY,
    Name INT,
    CHECK (Name IN (1, 2, 3))
);
```

Check constraint can be altered later as well:

```sql
ALTER TABLE Drinks
ADD CONSTRAINT checkName CHECK (NAME IN (1, 2, 3));
```