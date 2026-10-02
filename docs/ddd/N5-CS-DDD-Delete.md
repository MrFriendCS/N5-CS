# Remove Data

**Note:** It is possible to damage the data with a `DELETE FROM` statement.  It is advisable to practise with a `SELECT` statement first to see if the correct record, or records, will be deleted.

``` sql
DELETE FROM Pet
    WHERE petID = 29;
```

**Caution**: without the `WHERE` clause all records would be deleted!
