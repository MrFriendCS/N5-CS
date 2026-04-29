# Modify Data

**Note:** It is possible to damage the data with an `UPDATE` statement.  It is advisable to practise with a `SELECT` statement first to see if the correct record, or records, will be changed.

## Single value changed

``` sql
UPDATE Pet
    SET dob = "2022-04-01"
    WHERE petID = 29;
```

## Multiple  values changed

``` sql
UPDATE Pet
    SET name = "Churchill", 
        species = "Cat"
    WHERE petID = 29;
```

__Caution__: without the `WHERE` clause all records would be updated!
