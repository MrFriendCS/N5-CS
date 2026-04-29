# Comparison Operators

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


## Example 1 - if

Code is only run if the comparison is `True`.

``` python
# Initialise variable
age = 21

# Check value
if age >= 18:
    
    # True: display message
    print("You can go to the pub.")
```


## Example 2 - if, else

One section of code is always run.

``` python
# Initialise variable
age = 16

# check value
if age >= 18:
    
    # True: display message
    print("You can go to the pub.")

# Otherwise
else:

    # False: display message
    print("You can't go to the pub.")
```


## Example 3 - Nested if

Only the section of code for the first comparison that is `True` is run.  There can be multiple `if` statements, and the `else` is optional.

Numerical values are compared in order: largest to smallest (_see below_), or smallest to largest.

``` python
# Initialise variable
score = 53

# Check value
if score >= 80:

    # True: display message
    print("Excellent score!")

else:

  # Nested if

    # Check value
    if score >= 50:

        # True: display message
        print("Well done!")

    # Otherwise
    else:
        
        # All False: display message
        print("Oh dear!")
```


## Example 4 - if, elif, else

Only the section of code for the first comparison that is `True` is run.  There can be multiple `elif` statements, and the `else` is optional.  

Numerical values are compared in order: largest to smallest (_see below_), or smallest to largest.

``` python
# Initialise variable
score = 53

# Check value
if score < 50:

    # True: display message
    print("Oh dear!")

# Check value
elif score < 80:

    # True: display message
    print("Well done!")

# Otherwise
else:
    
    # All False: display message
    print("Excellent score!")
```
