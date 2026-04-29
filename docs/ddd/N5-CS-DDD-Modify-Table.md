# Modify a Table

Modifying a table involves a number of steps:

 1. Get the details of the table
 2. Create a new table using the modified details of the old table
 3. Copy the data from the old table to the new table
 4. Check the data has been copied
 5. Turn off referential integrity - _if needed_
 6. Delete the old table
 7. Rename the new table as the old table
 8. Turn on referential integrity - _if needed_

## 1. Get details

To view the field names, keys, data types, and validation of a table the `sqlite_schema.sql` field for the required table is displayed:

``` sql
SELECT sql
    FROM sqlite_schema
    WHERE tbl_name = "vaccination";
```

The output will look similar to:

``` sql
CREATE TABLE Vaccination (
    vaxID INT NOT NULL,
    petID INT NOT NULL,
    vaxDate DATE NOT NULL,
    name VARCHAR(30) NOT NULL,
    reaction BOOL NOT NULL,
    price REAL NOT NULL,
    PRIMARY KEY (vaxID),
    FOREIGN KEY (petID) 
        REFERENCES pet (petID)
)
```

## 2. Create new table

Create a new table by copying and pasting the output of Step 1, with the required changes made.

``` sql
CREATE TABLE NewVaccination (
    vaxID INT NOT NULL,
    petID INT NOT NULL,
    vaxDate DATE NOT NULL,
    name VARCHAR(30) NOT NULL 
        CHECK (LENGTH (name) >= 2),
    reaction BOOL NOT NULL,
    price REAL NOT NULL 
        CHECK (price >= 10 
           AND price <= 100),
    PRIMARY KEY (vaxID),
    FOREIGN KEY (petID) 
        REFERENCES Pet (petID)
);
```

## 3. Copy data

Copy the data from the old table into the new table.

``` sql
INSERT INTO NewVaccianation
    SELECT *
    FROM Vaccination;
```

## 4. Check data

Check that the data has been copied into the new table.

``` sql
SELECT *
    FROM NewVaccianation;
```

## 5. Turn off referential integrity

If the primary key of the old table is used as a foreign key  in another table then referential integrity will need to be turned off.

``` sql
PRAGMA foreign_keys = off;
```

## 6. Delete old table

Delete the old table.

``` sql
DROP TABLE Vaccination;
```

## 7. Rename new table

Rename the new table.

``` sql
ALTER TABLE NewVaccination
    RENAME TO Vaccination;
```

## 8. Turn on referential integrity

If referential integrity was turned off, it will needed to be turned on.

``` sql
PRAGMA foreign_keys = on;
```
