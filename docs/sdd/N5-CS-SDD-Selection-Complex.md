# Selection - Complex

Complex selection uses logical operators.

## Example 1 - AND

All comparisons must be `True`.

``` python
# Initialise variables
age = 16
time = "Night"

# Check values
if age <= 18 and time == "Day":

    # Both True: display message
    print("True!")

# Otherwise
else:

    # Either False: display message
    print("False!")
```


## Example 2 - OR

At least one comparison must be `True`.

``` python
# Initialise variables
age = 16
time = "Night"

# Check values
if age <= 18 or time == "Day":

    # Either True: display message
    print("True!")

# Otherwise
else:

    # Both False: display message
    print("False!")
```


## Example 3 - NOT

Reverses the Boolean.

``` python
# Initialise variable
age = 16

# Check value (brackets added for clarity)
if not (age <= 18):

    # True: display message
    print("True!")

# otherwise
else:

    # False: display message
    print("False!")
```


## Example 4 - Mixture

``` python
# Initialise variables
age = 21
banned = False

# Check values
if age >= 18 and not banned:

    # Both True: display message
    print("You can go to the pub.")
```
