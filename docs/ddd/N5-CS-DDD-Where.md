# Filter Results

To limit the number of records returned, the `WHERE` keyword is used with a comparison operator.

**Note:** Whilst SQL keywords are not case sensitive, search terms are.  Searching for `Hello` will not find `hello`, `HELLO`, or any other variation.

### Comparison operators

Comparison operators are used to compare one value with another.

| Symbol | Meaning |
| :----: | :------ |
| =      | Equality (the same as) |
| <>     | Inequality (not the same as) |
| >      | Greater than |
| >=     | Greater than or equal to |
| <      | Less than |
| <=     | Less than or equal to |

## Simple search

A simple search compares a field in a record with a value.  If the comparison is `True` then the required fields of that record are displayed.

``` sql
SELECT *
    FROM Vaccination
    WHERE species = "Cat";
```

## Complex search

A complex search compares two fields.

#### AND

If both comparisons are `True` then the required fields of that record are displayed.

``` sql
SELECT *
    FROM Vaccination
    WHERE name = "Distemper"
      AND reaction = TRUE;
```

### OR

If either comparison is `True` then the required fields of that record are displayed.

``` sql
SELECT *
    FROM Vaccination
    WHERE name = "Distemper"
       OR reaction = TRUE;
```
