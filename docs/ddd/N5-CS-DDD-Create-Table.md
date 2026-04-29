# Create a Table

## Data types

| Type    | SQL             | Comment |
| ----    | ---             | ------- |
| Text    | VARCHAR(`size`) | Size = number of characters |
| Number  | INT or REAL     | |
| Date    | DATE            | YYYY-MM-DD |
| Time    | TIME            | HH:MM:SS |
| Boolean | BOOL            | |

## Validation

| Type              | SQL |
| ----              | --- |
| Presence check    | NOT NULL |
| Restricted choice | CHECK (`field` IN (`list of values`)) |
| Field length      | CHECK (LENGTH(`field`) = `value`) |
| Range             | CHECK (`field` >= `lower value` AND `field` <= `upper value`) |

## Example

### Data dictionaries

#### Entity: Vehicle

| Attribute | Key   | Type    | Size  | Req'd | Validation |
| --------- | :---: | ----    | :---: | :---: | ---------- |
| vehReg    | PK    | text    | 8     | Y     | length: >=4 |
| make      |       | text    | 20    | N     | |
| model     |       | text    | 20    | N     | |
| colour    |       | text    | 15    | Y     | |

#### Entity: Repair

| Attribute    | Key   | Type    | Size  | Req'd | Validation |
| ---------    | :---: | ----    | :---: | :---: | ---------- |
| repairNo     | PK    | number  |       | Y     | |
| vehReg       | FK    | text    | 8     | Y     | Exists in vehicle table |
| repairDate   |       | date    |       | N     | |
| costEstimate |       | number  |       | N     | range: >= 0.00 |
| costActual   |       | number  |       | N     | range: >= 0.00 |
| completed    |       | boolean |       | Y     | |
| paid         |       | text    | 7     | Y     | Restricted choice: Nothing, Part, All |

### SQL

``` sql
CREATE TABLE Vehicle (
    vehReg VARCHAR(8) NOT NULL 
        CHECK (LENGTH (vehReg >= 4)),
    make VARCHAR(20),
    model VARCHAR(20),
    colour VARCHAR(15) NOT NULL,
    PRIMARY KEY (vehReg)
);
```

``` sql
CREATE TABLE Repair (
    repairNo INT NOT NULL,
    vehReg VARCHAR(8) NOT NULL,
    repairDate DATE,
    costEstimate REAL 
        CHECK (costEstimate >= 0),
    costActual REAL 
        CHECK (costActual >= 0),
    completed BOOL NOT NULL,
    paid VARCHAR(7) NOT NULL
        CHECK (paid IN ("Nothing", "Part", "All")),
    PRIMARY KEY (repairNo),
    FOREIGN KEY (vehReg)
        REFERENCES Vehicle (vehReg)
);
```
