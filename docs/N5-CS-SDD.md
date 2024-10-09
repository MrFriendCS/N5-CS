# Software Design and Development

## Notes

All the code examples use Python.

Python uses indentation (spaces at the beginning of a line) to show where code blocks are.

These notes are focused on N5 Computing Science so some terms are used differently.  Any reference to an `array` will actually use a `list`.

## Information

### Comments

Single line comment.

``` python
## This comment is not displayed
```

Multiline comment.

``` python
"""
This comment is not displayed
This comment is not displayed
"""
```

### Display information

``` python
# Display text
print("Hello world")

# Dispplay a number
print(3.14)
```

## Data

### Data types

#### Character

A single character: letter, number, or symbol.  Contained in quote marks.

``` python
"a"
"1"
"@"
```

#### String

A string of characters.  Contained in quote marks.

``` python
"Hello world"
"00.1200"
",./#';"
"Pa55w0rd|"
```

#### Integer

A whole number, positive and negative.  _Not_ contained in quotes.

``` python
1234
0
-4321
```

#### Real

A decimal number, positive and negative.  _Not_ contained in quotes.

``` python
3.14
0.0
-3.14
```

#### Boolean

A binary choice.  _Not_ contained in quotes.

``` python
True
False
```

### Data structure

An array can hold multiple values of the same data type, all within square brackets (`[ ]`).

#### Array of characters

``` python
["a", "g", "z", "d"]
```

#### Array of strings

``` python
["hat", "mat", "sat"]
```

#### Array of integers

``` python
[47, -6, 99, 1001]
```

#### Array of real

``` python
[3.14, -89.65, 0.0]
```

#### Array of Boolean

``` python
[True, True, False]
```

## Assignment

Variables are used to store values.  An assignment statement has 3 parts:

 1. **=** is the assignment operator (an equals sign in maths)
 2. The value to be assigned is to the right of the assignment operator
 3. The variable that the value will assigned to is to the left of the assignment operator

```
variableName = valueToAssign
```

The value *might* need to be calculated first before being assigned.

### Data types

``` python
# Assign an integer value
myInteger = 5
```

``` python
# Assign a real value
myReal = 3.14
```

``` python
# Assign a character
myCharacter = "&"
```

``` python
# Assign a string
myString = "Hello"
```

``` python
# Assign a Boolean value
myBoolean = True
```


### Data structures

#### All values

``` python
# Assign an array of integers
myArrayOfIntegers = [56, 34, 2, 85, 51]
```

``` python
# Assign an array of strings - Shorthand
myArrayOfStrings = [""] * 4
```

#### Individual value

Elements in an array are numbered, starting at zero.  They  are accessed using the subscript operator `[ ]` and the index position of the element.

``` python
# Assig
myArrayOfIntegers[0] = 65
```


## Arithmetic operations

Addition
``` python
4 + 2
```

Subtraction
``` python
4 - 2
```

Multiplication
``` python
4 * 2
```

Division
``` python
4 / 2
```

Exponentiation (to the power of)
``` python
4 ** 2
```

### Examples

``` python
myMultiplication = 3 * 2
print(myMultiplication)
```

``` python
mySquare = 3 ** 2
print(mySquare)
```

``` python
myAge = 21
myAge = myAge + 1
print(myAge)
```

## Concatenation

Concatenate means to join together.

### Strings

A string can be concatenated with another string.

``` python
# Initialise variables
part1 = "Ho"
part2 = "use"

# Concatenate strings
word = part1 + part2

# Display result
print(word)
```

Be sure to include a space between words when concatenating.

``` python
# Initialise variables
word1 = "Hello"
word2 = "world"

# Concatenate strings
phrase = word1 + " " + word2

# Display result
print(phrase)
```

### Non-strings

To concatenate something that is not a string, it must be cast (converted) to a string.

``` python
# Initialise variable
age = 18

# Cast to string and concatenate
phrase = "I am " + str(age)

# Display result
print(phrase)
```

### Arrays

An array can be concatenated with another array.

``` python
# Initialise variables
part1 = ["Ho", "Ho"]
part2 = ["Ho"]

# Concatenate arrays
combined = part1 + part2

# Display result
print(combined)
```

### Non-arrays

To concatenate something that is not an array, it must be cast (converted) to an array.

``` python
# Initialise variables
myArray = [7, 11, 15]
myInt = 18

# Cast to array and concatenate
combined = myArray + [myInt]

# Display result
print(combined)
```

## User input

### String input

**Note:** Anything from the keyboard is a *string*.

```python
# Get values from user
word1 = input("Enter the first word: ")
word2 = input("Enter the second word: ")

# Concatenate values
phrase = word1 + " " + word2

# Display result
print(phrase)
```

### Non-string input 

Values that have a different datatype must be cast from string to the correct datatype, using one of the following functions:

```python
# Cast string to integer
myInt = int("42")

# Cast string to real
myReal = float("3.14")
```

#### Example

```python
# Get values from user and cast to integers
value1 = int(input("Enter the first value: "))
value2 = int(input("Enter the second value: "))

# Add values
addition = value1 + value2

# Display result
print(addition)
```

## Comparison operators

Comparison operators are used to compare one value with another.   All of the following examples produce a Boolean answer of `True` or `False`.

Equality (the same as)
``` python
16 == 18  # False
```

Inequality (not the same as)
``` python
16 != 18  # True
```

Greater than
``` python
16 > 18  # False
```

Greater than or equal to
``` python
16 >= 18  # False
```

Less than
``` python
16 < 18  # True
```

Less than or equal to
``` python
16 <= 18  # True
```

## Selection - Simple

Selection makes use of a comparison operator to decide what to do.

### Example 1 - if

Code is only run if the comparison is `True`.

``` python
age = 21

if age >= 18:
    # True
    print("You can go to the pub.")
```

### Example 2 - if, else

One section of code is always run.

``` python
age = 16

if age >= 18:
    # True
    print("You can go to the pub.")
else:
    # False
    print("You can't go to the pub.")
```

### Example 3 - if, elif, else

Only the section of code for the first comparison that is `True` is run.  There can be multiple `elif` statements.

There can be multiple `elif` statements, and the `else` is optional.  Numerical values are compared in order: largest to smallest (_see below_), or smallest to largest.

``` python
score = 53

if score >= 80:
    # True
    print("Excellent score!")
elif score >= 50:
    # True
    print("Well done!")
else:
    #  False
    print("Oh dear!")
```

## Logical operators

Compare more than one set of values to produce a Boolean answer of `True` or `False`.

### AND

Both comparisons must be `True` to produce a final answer of `True`.

| Comparison 1 | Comparison 2 | Result |
| ------------ | ------------ | ------ |
| False        | False        | False  |
| False        | True         | False  |
| True         | False        | False  |
| True         | True         | True   |

``` python
16 <= 18 and "Night" == "Day"
```

### OR

One or both comparisons must be `True` to produce a final answer of `True`.

| Comparison 1 | Comparison 2 | Result |
| ------------ | ------------ | ------ |
| False        | False        | False  |
| False        | True         | True   |
| True         | False        | True   |
| True         | True         | True   |

``` python
16 <= 18 or "Night" == "Day"
```

### NOT

Reverses the result of the comparison.

| Comparison | Result |
| ---------- | ------ |
| False      | True   |
| True       | False  |

``` python
not (16 <= 18))
```

## Selection - Complex

Complex selection uses logical operators.

### Example 1 - AND

All comparisons must be `True`.

``` python
age = 16
time = "Night"

if age <= 18 and time == "Day":
	print("True!")
else:
	print("False!")
```

### Example 2 - OR

At least one comparison must be `True`.

``` python
age = 16
time = "Night"

if age <= 18 or time == "Day":
	print("True!")
else:
	print("False!")
```

### Example 3 - NOT

Reverses the Boolean.

``` python
age = 16

if not(age <= 18):
	print("True!")
else:
	print("False!")
```

### Example 4 - Mixture

``` python
age = 21
banned = False

if age >= 18 and not(banned):
    print("You can go to the pub.")
```

##  Loops

### Fixed loop (for)

Before a fixed loop starts, the number of times it will run ***is*** stated.

The range function produces a sequence of values.  The last value in the sequence is always one less than the `stop` value:

``` python
range(stop)  ## Starts from 0

range(start, stop)

range(start, stop, step)
```

#### Example 1 - Stop value

Display the numbers 0 to 9, ten numbers in total.  The __loop variable__ is `counter` and it holds the current value from the range function.

``` python
for counter in range(10):
    print(counter)
```

#### Example 2 - Start and stop values

Display the numbers 1 to 9.

``` python
for counter in range(1, 10):
    print(counter)
```

#### Example 3 - Start, stop, and stop values

Display the odd numbers from 1 to 9.

``` python
for counter in range(1, 10, 2):
    print(counter)
```

### Conditional loop (while)

Before a conditional loop starts, the number of times it will run ***is not*** stated.

It only runs if the comparison is `True`.  Each time the code is completed the comparison is checked again.  If it is still `True` the code is run again.

### Example

``` python
# Get value from user
value = int(input("Enter a value: "))

# Check value
while value < 10:

    # Increment value
    value = value + 1

    # Display value
    print(value)
```

## Predefined functions

### Random

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

### Round

#### Decimal Places

The round function works with floating point values (decimals).  It returns (produces) a value that is rounded to a specified number of decimal places

``` python
# Initialise variable
myReal = 3.14159265359

# Round to 2 decimal places
myRound = round(myReal, 2)

print(myRound)
```

#### Whole number

**Note:** Python does not always round up when a value has 5 tenths.  Instead it rounds to the nearest even number!

The round function can also be used to return a value without any decimal places (integer).

The following example will return a value of 4.

``` python
myReal= 3.5

# Round to zero decimal places
myRound = round(myReal)

print(myRound)
```

The following example will ***also*** return a value of 4.

``` python
myReal= 4.5

# Round to zero decimal places
myRound = round(myReal)

print(myRound)
```

### Length

The length function works with strings and arrays.  It returns a number of characters in a string or the number of elements in an array.

#### String

``` python
# Initialise variable
myString = "Computing"

# Get number of characters in string
myLength = len(myString)

# Display result
print(myLength)
```

#### Array

``` python
# Initialise variable
myArrayOfIntegers = [56, 34, 2, 85, 51]

# Get number of elements in array
myLength = len(myArrayOfIntegers)

# Display result
print(myLength)
```

## Standard algorithms

### Input validation

User input can be checked using a conditional loop.  If the value entered is not acceptable an error message is displayed and the value re-entered until it is.

It can be done two different ways, initial input before the loop or within the loop.

#### Input before loop

This approach can be easier to use when the input validation is within another loop.

The conditional loop is only entered if the value entered is invalid.

``` python
# Get value from user and cast
dice = int(input("Enter dice value: "))

# Check value
while dice < 1 or dice > 6:

    # Display meaningful error message
    print("Value must be from 1 to 6.")
    
    # Get value from user and cast
    dice = int(input("Enter dice value: "))

# Display value - info only
print("You entered " + str(dice))
```

#### Input within loop

Variable is assigned a value that will cause the loop condition to be true.

``` python
# Initialise variable - not valid
dice = 0

# Check value
while dice < 1 or dice > 6:

    # Get value from user and cast
    dice = int(input("Enter dice value: "))
    
    # Check value
    if dice < 1 or dice > 6:

        # Display meaningful error message
        print("Value must be from 1 to 6.")

# Display value - info only
print("You entered " + str(dice))
```

### Running total

#### Fixed loop

``` python
# Initialise variable
total = 0

# Loop required number of times
for counter in range(4):

	# Get value from user and cast
    age = int(input("Enter an age: "))

	# Add value to total
    total = total + age

# Display result
print("The combined age is " + str(total))
```

#### Conditional loop

``` python
# Initialise variables
answer = ""
total = 0

# Chack answer - loop until False
while answer != "no":

    # Get value from user and cast
    age = int(input("Enter an age: "))
    
    # Add value to total
    total = total + age
    
    # Get answer from user
    answer = input("Enter another age? ")

# Display result
print("The combined age is " + str(total))
```

### Traversing a 1-D array

Arrays store more than one value, called elements.  Each element has a position.  Python starts counting from zero.

Often, the loop variable is called __`index`__.

#### Putting values in

``` python
# Initialise variable
heights = [0.0] * 5

# Display array
print(heights)

# Loop for each element in array
for index in range(len(heights)):

    # Get value to assign to array
    height = float(input("Enter a height: "))

	# Assign value to array
    heights[index] = height

# Display array
print(heights)
```

#### Getting values out

##### Method 1

The loop variable `index` is assigned each value in turn from the `range()` function.

``` python
# Initialise variable
scores = [56, 34, 2, 85, 51]

# Loop for each element in array
for index in range(len(scores)):

	# Get value from array
	score = scores[index]
	
	# Display current value
    print(score)
```

##### Method 2

The loop variable `score` is assigned each value in turn from the `scores` array.

``` python
# Initialise array
scores = [56, 34, 2, 85, 51]

# Loop for each element in array
for score in scores:

    # Display current value
    print(score)
```

### Multiple arrays

A program can use more than one array, in the same way that a program can use multiple variables.
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTExOTUxODQwNzAsLTIwNjA4MjQ1NjYsMT
U3MTUxNTQ2MiwxMzY1MjAwNjkyLDQwOTE5MDkwMywxNjA5MTIx
MTUzLDIxMDA3ODIzMjUsMjAxNDQ1MzIwNCwtMTU5NzM4NzUxMC
wtMzQzMTk2NzE4LDE3MDUwMjY0MDEsLTEwODM0MjY3ODUsMTAx
NDMwMTE4Myw3Nzc0NzYwNTYsMTkwOTkwMzQ3NiwtNjExODk5Nj
Y1LDQ5MzA4ODMxMCwtMjA0MzkyNzkwMiwtMjExOTIxNTQ4Miwx
MDAyODc0Nzk3XX0=
-->