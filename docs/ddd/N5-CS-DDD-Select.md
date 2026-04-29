# Display Data

To search a database, a basic statement with two keywords `SELECT` and `FROM` is used.

The `SELECT` keyword lists the required field(s).  The `FROM` keyword states the table(s) that the fields are in.

To display all the fields the __`*`__ symbol is used.

``` sql
SELECT *
    FROM Pet;
```

To select one, or more fields, their names are used.

``` sql
SELECT name, species
    FROM Pet;
```
