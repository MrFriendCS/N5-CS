# User input


## String input

**Note:** Anything from the keyboard is a *string*.

```python
# Get values from user
word1 = input("Enter the first word: ")
word2 = input("Enter the second word: ")

# Concatenate strings
phrase = word1 + " " + word2

# Display result
print(phrase)
```


## Non-string input 

Values that have a different datatype must be cast from string to the correct datatype, using one of the following functions:

```python
# Cast string to integer
myInt = int("42")

# Cast string to real
myReal = float("3.14")
```


### Example

```python
# Get values from user and cast to integers
value1 = int(input("Enter the first value: "))
value2 = int(input("Enter the second value: "))

# Add integers
addition = value1 + value2

# Display result
print(addition)
```
