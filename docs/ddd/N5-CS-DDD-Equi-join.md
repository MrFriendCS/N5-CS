# Equi-join

Tables are joined using the primary key of one table and the foreign key of the other table.

## Generic

``` sql
SELECT *
    FROM table1, table2
    WHERE table1.primaryKey = table2.foreignKey;
```

## Example

**Note:** In this example both tables have a field with the same name.  So that the database can distinguish between the fields they must be qualified with the table name.  Just using the field name would be _ambiguous_.

``` sql
SELECT *
    FROM Pet, Vaccination
    WHERE pet.petID = vaccination.petID;
```
