# Logical operators

Compare more than one set of values to produce a Boolean answer of `True` or `False`.


## AND

Both comparisons must be `True` to produce a final answer of `True`.

| Comparison 1 | Comparison 2 | Result |
| ------------ | ------------ | ------ |
| False        | False        | False  |
| False        | True         | False  |
| True         | False        | False  |
| True         | True         | True   |

``` python
16 <= 18 and "Night" == "Day"  # True and False => False
```


## OR

One or both comparisons must be `True` to produce a final answer of `True`.

| Comparison 1 | Comparison 2 | Result |
| ------------ | ------------ | ------ |
| False        | False        | False  |
| False        | True         | True   |
| True         | False        | True   |
| True         | True         | True   |

``` python
16 <= 18 or "Night" == "Day"  # True or False => True
```


## NOT

Reverses the result of the comparison.

| Comparison | Result |
| ---------- | ------ |
| False      | True   |
| True       | False  |

``` python
not (16 <= 18))  # not (True) => False
```

## Selection - Complex

Complex selection uses logical operators.

### Example 1 - AND

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


### Example 2 - OR

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


### Example 3 - NOT

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


### Example 4 - Mixture

``` python
# Initialise variables
age = 21
banned = False

# Check values
if age >= 18 and not banned:

    # Both True: display message
    print("You can go to the pub.")
```
