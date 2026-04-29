# Add Data

It is possible to insert a record, multiple records, or partial records into a table using `INSERT INTO` and `VALUES`.  All validation rules must be met for the new data to be added.

## Single record

``` sql
INSERT INTO Pet
    VALUES (26, "Tiger", "Cat", "2022-04-17");
```

## Multiple records

``` sql
INSERT INTO Pet
    VALUES (27, "Bill", "Ferret", "2022-05-01"),
           (28, "Ben", "Ferret", "2022-05-01");
```

## Partial record(s)

If a partial record is added then the field names must be stated.  The values must be in the same order as the fields.

``` sql
INSERT INTO Pet (species, name, petID)
    VALUES ("Dog", "Winston", 29);
```
