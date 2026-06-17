# Assignment

Variables are used to store values.  An assignment statement has 3 parts:

 1. **=** is the assignment operator (an equals sign in maths)
 2. The value to be assigned is to the right of the assignment operator
 3. The variable that the value will assigned to is to the left of the assignment operator

```
variableName = valueToAssign
```

The value *might* need to be calculated first before being assigned.


## Data types

``` python
# Assign an integer value
myInteger: int = 5
```

``` python
# Assign a real value
myReal: float = 3.14
```

``` python
# Assign a character
myCharacter: str = "&"
```

``` python
# Assign a string
myString: str = "Hello"
```

``` python
# Assign a Boolean value
myBoolean: bool = True
```


## Data structures


### All values

``` python
# Assign an array of integers
myArrayOfIntegers: list[int] = [56, 34, 2, 85, 51]
```

``` python
# Assign an array with many values - split over lines
myLongArray: list[str] = ["Monday", "Tuesday", "Wednesday", "Thursday", 
               "Friday", "Saturday", "Sunday"]
```

``` python
# Assign an array of strings - Shorthand
myArrayOfStrings: list[str]  = [""] * 4
```


### Individual value

Elements in an array are numbered, starting at zero.  They  are accessed using the subscript operator `[ ]` and the index position of the element.

``` python
# Assign a value to an element
myArrayOfIntegers[0] = 65
```


## Type Hinting

Type hinting is used to show what data type or data structure a variable will hold.


### Single Data Types

| SQA       | Python |
| ---       | ------ |
| Character | str |
| String    | str |
| Integer   | int |
| Real      | float |
| Boolean   | bool |


### Data Structures

| SQA                | Python |
| ---                | ------ |
| Array of Character | list[str] |
| Array of String    | list[str] |
| Array of Integer   | list[int] |
| Array of Real      | list[float] |
| Array of Boolean   | list[bool] |
