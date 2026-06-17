# User input


## String input

**Note:** Anything from the keyboard is a *string*.

```python
# Initialise variables
word1: str = ""
word2: str = ""
phrase: str = ""

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
# Initialise variables
myStr1: str = "42"
myStr2: str = "3.14"
myInt: int = 0
myReal: float = 0.0

# Cast string to integer
myInt = int(myStr1)

# Cast string to real
myReal = float(myStr2)
```


### Example

```python
# Initialise variables
value1: int = 0
value2: int = 0
addition: int = 0

# Get values from user and cast to integers
value1 = int(input("Enter the first value: "))
value2 = int(input("Enter the second value: "))

# Add integers
addition = value1 + value2

# Display result
print(addition)
```
