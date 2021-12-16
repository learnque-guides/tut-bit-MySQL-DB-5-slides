# Create, drop database

Syntax for database creation:

```sql
CREATE {DATABASE | SCHEMA} [IF NOT EXISTS] db_name
    [create_option] ...

create_option: [DEFAULT] {
    CHARACTER SET [=] charset_name
  | COLLATE [=] collation_name
  | ENCRYPTION [=] {'Y' | 'N'}
}
```

Example:

```sql
CREATE DATABASE IF NOT EXISTS `test`
    DEFAULT CHARACTER SET utf8 COLLATE utf8_bin;
USE `test`;
```

You can modify database with ALTER DATABASE:

```sql
ALTER {DATABASE | SCHEMA} [db_name]
    alter_option ...

alter_option: {
    [DEFAULT] CHARACTER SET [=] charset_name
  | [DEFAULT] COLLATE [=] collation_name
  | [DEFAULT] ENCRYPTION [=] {'Y' | 'N'}
  | READ ONLY [=] {DEFAULT | 0 | 1}
}
```

You can remove database with:

```sql
DROP DATABASE IF EXISTS `test`;
```