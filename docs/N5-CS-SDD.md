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
print("Hello world")

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

## Assign values

Variables are used to store values.  An assignment statement has 3 parts:

 1. **=** is the assignment operator (an equals sign in maths)
 2. The value to be assigned is to the right of the assignment operator
 3. The variable w the value will  is to the left of the assignment operator

The value is assigned to (stored in) the variable.  The value *might* need to be calculated first before being assigned.

``` python
myInteger = 5
```

``` python
myReal = 3.14
```

``` python
myCharacter = "&"
```

``` python
myString = "Hello"
```

``` python
myBoolean = True
```

``` python
myArrayOfIntegers = [56, 34, 2, 85, 51]
```

``` python
myArrayOfStrings = [""] * 4  # Shorthand
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
part1 = "Ho"
part2 = "use"

word = part1 + part2

print(word)
```

Be sure to include a space between words when concatenating.

``` python
word1 = "Hello"
word2 = "world"

phrase = word1 + " " + word2

print(phrase)
```

### Non-strings

To concatenate something that is not a string, it must be cast (converted) to a string.

``` python
age = 18

phrase = "I am " + str(age)

print(phrase)
```

### Arrays

An array can be concatenated with another array.

``` python
part1 = ["Ho", "Ho"]
part2 = ["Ho"]

combined = part1 + part2

print(combined)
```

### Non-arrays

To concatenate something that is not an array, it must be cast (converted) to an array.

``` python
myArray = []
myInt = 18

combined = myArray + [myInt]

print(combined)
```

## User input

### String input

**Note:** Anything from the keyboard is a *string*.

```python
word1 = input("Enter the first word: ")
word2 = input("Enter the second word: ")

phrase = word1 + " " + word2

print(phrase)
```

### Non-string input 

Values that have a different datatype must be cast from string to the correct datatype, using one of the following functions:

```python
myInt = int("42")
myReal = float("3.14")
```

#### Example

```python
value1 = int(input("Enter the first value: "))
value2 = int(input("Enter the second value: "))

addition = value1 + value2

print(addition)
```

## Comparison operators

Comparison operators are used to compare one value with another.   All of the following examples produce a Boolean answer of `True` or `False`.

Equality (the same as)
``` python
16 == 18
```

Inequality (not the same as)
``` python
16 != 18
```

Greater than
``` python
16 > 18
```

Greater than or equal to
``` python
16 >= 18
```

Less than
``` python
16 < 18
```

Less than or equal to
``` python
16 <= 18
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
value = int(input("Enter a value: "))

while value < 10:
    value = value + 1
    print(value)
```

## Predefined functions

### Random

The code to produce a random number needs to be imported before it can be used.

The code can be used to produce a random integer, with the lowest and highest possible values specified.

``` python
import random

myDice = random.randint(1, 6)

print(myDice)
```

### Round

#### Decimal Places

The round function works with floating point values (decimals).  It returns (produces) a value that is rounded to a specified number of decimal places

``` python
myReal = 3.14159265359

myRound = round(myReal, 2)

print(myRound)
```

#### Whole number

**Note:** Python does not always round up when a value has 5 tenths.  Instead it rounds to the nearest even number!

The round function can also be used to return a value without any decimal places (integer).

The following example will return a value of 4.

``` python
myReal= 3.5

myRound = round(myReal)

print(myRound)
```

The following example will ***also*** return a value of 4.

``` python
myReal= 4.5

myRound = round(myReal)

print(myRound)
```

### Length

The length function works with strings and arrays.  It returns a number of characters in a string or the number of elements in an array.

#### String

``` python
myString = "Computing"

myLength = len(myString)

print(myLength)
```

#### Array

``` python
myArrayOfIntegers = [56, 34, 2, 85, 51]

myLength = len(myArrayOfIntegers)

print(myLength)
```

## Standard algorithms

### Input validation

User input can be checked using a conditional loop.  If the value entered is not acceptable an error message is displayed and the value re-entered until it is.

It can be done two different ways, initial input before the loop or within the loop.

#### Input before loop

The conditional loop is only entered if the value entered is invalid.

``` python
# Input validation: Start
dice = int(input("Enter dice value: "))

while dice < 1 or dice > 6:
    print("Value must be from 1 to 6.")
    
    dice = int(input("Enter dice value: "))
# Input validation: End

# Display value - info only
print("You entered " + str(dice))
```

#### Input within loop

Variable is assigned a value that will cause the loop condition to be true.

``` python
# Input validation: Start
dice = 0

while dice < 1 or dice > 6:
    dice = int(input("Enter dice value: "))
    
    if dice < 1 or dice > 6:
        print("Value must be from 1 to 6.")
# Input validation: End

# Display value - info only
print("You entered " + str(dice))
```

### Running total

#### Fixed loop

``` python
# Initialise total
total = 0

for counter in range(4):
	# Get value
    age = int(input("Enter an age: "))

	# Add value to total
    total = total + age

print("The combined age is " + str(total))
```

#### Conditional loop

``` python
answer = ""
total = 0

while answer != "no":
    age = int(input("Enter an age: "))
    total = total + age

    answer = input("Enter another age? ")

print("The combined age is " + str(total))
```

### Traversing a 1-D array

Arrays store more than one value, called elements.  Each element has a position.  Python starts counting from zero.

Often, the loop variable is called __`index`__.

#### Putting values in

``` python
# Initialise array
heights = [0.0] * 5

# Display array
print(heights)

# Loop for each element
for index in range(len(heights)):

    # Get value to assign to array
    height = float(input("Enter a height: "))

	# Assign value to array
    heights[index] = height

# Display array
print(heights)
```

#### Getting values out

Method 1 - with a loop variable (`index`)

``` python
# Initialise array
scores = [56, 34, 2, 85, 51]

# Loop for each element in array
for index in range(len(scores)):

	# Get value from array
	score = scores[index]
	
    print(score)
```

Method 2 - without a loop variable

``` python
# Initialise array
scores = [56, 34, 2, 85, 51]

# Loop for each element in array
for score in scores:

    print(score)
```

### Multiple arrays

A program can use more than one array, in the same way that a program can use multiple variables.
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTU0MDU5NjQ0OSwxOTA5OTAzNDc2LC02MT
E4OTk2NjUsNDkzMDg4MzEwLC0yMDQzOTI3OTAyLC0yMTE5MjE1
NDgyLDEwMDI4NzQ3OTcsOTE4NTc0MTU2LDQ3NTY4MjI1OSwxMj
YzNTQ2MTEzLC0xNDg0MDczOTEwLDE2OTc4NDM2NjIsNzYyNDAx
OTgyLC0xNDk4NDYxMjQwLC03NDE5NDQ5MTcsLTIyOTM0ODIwMi
wxOTY4NTg1Mjg4LDgxNDM5NDkxOV19
-->