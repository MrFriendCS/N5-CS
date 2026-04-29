# Concatenation

Concatenate means to join together.


## Strings

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


## Non-strings

To concatenate something that is not a string, it must be cast (converted) to a string.

``` python
# Initialise variable
age = 18

# Cast to string and concatenate
phrase = "I am " + str(age)

# Display result
print(phrase)
```


## Arrays

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


## Non-arrays

To concatenate something that is not an array, it must be cast (converted) to an array.

``` python
# Initialise variables
myArray = [0, 1, 1, 2, 3, 5]
myInt = 8

# Cast to array and concatenate
combined = myArray + [myInt]

# Display result
print(combined)
```
