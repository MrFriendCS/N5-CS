# Standard Algorithms


## Input validation

User input can be checked using a conditional loop.  If the value entered is not acceptable an error message is displayed and the value re-entered until it is.

It can be done two different ways, initial input before the loop or within the loop.


### Input before loop

This approach can be easier to use when the input validation is within another loop.

The conditional loop is only entered if the value entered is invalid.

``` python
# Get value from user and cast
dice = int(input("Enter dice value: "))

# Check values
while dice < 1 or dice > 6:

    # Display meaningful error message
    print("Value must be from 1 to 6.")
    
    # Get value from user and cast
    dice = int(input("Enter dice value: "))

# Display value - info only
print("You entered " + str(dice))
```


### Input within loop

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


## Running total


### Fixed loop

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


### Conditional loop

``` python
# Initialise variables
answer = ""
total = 0

# Check answer - loop until False
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


## Traversing a 1-D array

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


### Getting values out


#### Method 1

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


#### Method 2

The loop variable `score` is assigned each value in turn from the `scores` array.

``` python
# Initialise variable
scores = [56, 34, 2, 85, 51]

# Loop for each element in array
for score in scores:

    # Display current value
    print(score)
```


## Multiple arrays

A program can use more than one array, in the same way that a program can use multiple variables.
