# Examples

## Display data

Select various fields from two tables, with two search conditions and ordered on two fields.

``` sql
SELECT Pet.name, species, Vaccination.name, vaxDate
    FROM Pet, Vaccination
    WHERE Pet.petID = Vaccination.petID
      AND species = "Rabbit"
    ORDER BY Pet.name ASC,
             vaxDate DESC;
```

## Change data

Update vaccination records so that **Feline Leukaemia Virus** is replaced with **FLV**.

* Create a `SELECT` statement to test that the `WHERE` clause selects the correct records.

``` sql
SELECT *
    FROM Vaccination
    WHERE name = "Feline Leukaemia Virus";
```

* Create an `UPDATE` statement to update the correct records.

``` sql
UPDATE Vaccination
    SET name = "FLV"
    WHERE name = "Feline Leukaemia Virus";
```

* Check that the changes have been made.

``` sql
SELECT *
    FROM Vaccination
    WHERE name = "FLV"
       OR name = "Feline Leukaemia Virus";
```
