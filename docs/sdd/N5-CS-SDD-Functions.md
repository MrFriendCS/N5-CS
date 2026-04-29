# Predefined Functions


## Random

The code to produce a random number needs to be imported before it can be used.

The code can be used to produce a random integer, with the lowest and highest possible values specified.

``` python
# Get extra code
import random

# Pick a random integer
myDice = random.randint(1, 6)

# Display value
print(myDice)
```


## Round


### Decimal Places

The round function works with floating point values (decimals).  It returns (produces) a value that is rounded to a specified number of decimal places

``` python
# Initialise variable
myReal = 3.14159265359

# Round to 2 decimal places
myRound = round(myReal, 2)

print(myRound)
```


### Whole number

**Note:** Python does not always round up when a value has 5 tenths.  Instead it rounds to the nearest even number!

The round function can also be used to return a value without any decimal places (integer).

The following example will return a value of 4.

``` python
# Initialise variable
myReal= 3.5

# Round to zero decimal places
myRound = round(myReal)

# Display result
print(myRound)
```

The following example will ***also*** return a value of 4.

``` python
# Initialise variable
myReal= 4.5

# Round to zero decimal places
myRound = round(myReal)

# Display result
print(myRound)
```


## Length

The length function works with strings and arrays.  It returns a number of characters in a string or the number of elements in an array.


### String

``` python
# Initialise variable
myString = "Computing"

# Get number of characters in string
myLength = len(myString)

# Display result
print(myLength)
```


### Array

``` python
# Initialise variable
myArrayOfIntegers = [56, 34, 2, 85, 51]

# Get number of elements in array
myLength = len(myArrayOfIntegers)

# Display result
print(myLength)
```
