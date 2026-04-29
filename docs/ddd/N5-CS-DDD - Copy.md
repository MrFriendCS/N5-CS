# Database Design and Development

## Notes

All the code examples use SQLite.  They will work with [DB Browser for SQLite](https://sqlitebrowser.org/).

These notes are focused on N5 Computing Science so some terms might be used differently.

SQLite, and SQL, keywords are not case sensitive.  The following are all equally valid:

``` sql
SELECT / SeLeCt / select
```

In the examples, the keywords will be in uppercase.

SQLite, and SQL, is not whitespace sensitive.  This means a statement can be all on a single line or split over multiple lines.  In general, the examples have one keyword per line.

The statements are terminated with a semicolon, __`;`__.  An individual statement will run without a semicolon but multiple statements will not.


## Attribute types (Data types)

SQLite has fewer data types than SQL.  However, SQL datatypes can be used and SQLite will match these to it's own datatypes.

| Data type     | Example data |
| ---------     | ------------ |
| Text          | "Cat", "01871 810100" |
| Number (INT)  | -99, 0, 99 |
| Number (REAL) | -99.0, 0.0, 99.0 |
| Date          | "2024-02-29" |
| Time          | "13:15:00" |
| Boolean       | TRUE, FALSE |


## Example Data

The example [database](N5-CS-Database.db) contains the tables and records that the SQL examples will work with. The file can be opened with [DB Browser for SQLite](https://sqlitebrowser.org/).

The first 4 records of the data used in the examples are shown in the following tables:

### Table: Pet

| petID | name     | species | dob |
| :---: | ----     | ------- | --- |
| 1     | Hans     | Cat     | 2015-09-22 |
| 2     | Minnnie  | Gerbil  | 2021-05-24 |
| 3        | Bo       | Rabbit  | 2011-10-13 |
| 4     | Joscelin | Gerbil  | 2022-02-19 |

### Table: Vaccination

| vaxID | petID | vaxDate    | name             | reaction | price |
| :---: | :---: | -------    | ----             | :------: | ----- |
| 1     | 13    | 2019-09-03 | Distemper        | TRUE     | 45.00 |
| 2     | 5     | 2020-06-23 | Canine hepatitis | FALSE    | 35.50 |
| 3     | 1     | 2015-12-17 | Cat Flu          | FALSE    | 12.99 |
| 4     | 17    | 2015-10-05 | Cat Flu          | FALSE    | 12.99 |


## ER Diagram

![N5 DDD Entity Relationship Diagram](N5-CS-DDD.png "ER Diagram")


### Views tables

To view all the tables in the database the `name` field of the `sqlite_schema` table is displayed.

``` sql
SELECT name
    FROM sqlite_schema
    WHERE type = "table";
```


## Information

### Comments

Single line comment.

``` sql
-- This comment is not displayed
```

Multiline comment.

``` sql
/*
This comment is not displayed
This comment is not displayed
*/
```

### Display information
It is possible to display simple messages (DB Browser for SQLite).

``` sql
SELECT "Hello World!";
```

## Display Data

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


## Filter results

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

### Simple search

A simple search compares a field in a record with a value.  If the comparison is `True` then the required fields of that record are displayed.

``` sql
SELECT *
    FROM Vaccination
    WHERE species = "Cat";
```

### Complex search

A complex search compares two fields.

#### AND

If both comparisons are `True` then the required fields of that record are displayed.

``` sql
SELECT *
    FROM Vaccination
    WHERE name = "Distemper"
      AND reaction = TRUE;
```

#### OR

If either comparison is `True` then the required fields of that record are displayed.

``` sql
SELECT *
    FROM Vaccination
    WHERE name = "Distemper"
       OR reaction = TRUE;
```


## Sort results

It is possible to sort the output of a search using `ORDER BY` and stating the field, or fields.  Fields are sorted ascending, smallest to largest, by default.

``` sql
SELECT *
    FROM Pet
    ORDER BY species ASC;
```

To change the sort order of a field to descending the keyword `DESC` used.  The keyword `ASC` is not needed but can be used to explicitly sort ascending.  More than one field can be sorted.

``` sql
SELECT *
    FROM Pet
    ORDER BY species DESC, 
             name ASC;
```


## Equi-join between tables

Tables are joined using the primary key of one table and the foreign key of the other table.

### Generic

``` sql
SELECT *
    FROM table1, table2
    WHERE table1.primaryKey = table2.foreignKey;
```

### Example

**Note:** In this example both tables have a field with the same name.  So that the database can distinguish between the fields they must be qualified with the table name.  Just using the field name would be _ambiguous_.

``` sql
SELECT *
    FROM Pet, Vaccination
    WHERE pet.petID = vaccination.petID;
```


## Add New Data

It is possible to insert a record, multiple records, or partial records into a table using `INSERT INTO` and `VALUES`.  All validation rules must be met for the new data to be added.

### Single record

``` sql
INSERT INTO Pet
    VALUES (26, "Tiger", "Cat", "2022-04-17");
```

### Multiple records

``` sql
INSERT INTO Pet
    VALUES (27, "Bill", "Ferret", "2022-05-01"),
           (28, "Ben", "Ferret", "2022-05-01");
```

### Partial record(s)

If a partial record is added then the field names must be stated.  The values must be in the same order as the fields.

``` sql
INSERT INTO Pet (species, name, petID)
    VALUES ("Dog", "Winston", 29);
```
