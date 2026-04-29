#  Loops


## Fixed loop (for)

Before a fixed loop starts, the number of times it will run ***is*** stated.

The range function produces a sequence of values.  The last value in the sequence is always one less than the `stop` value:

``` python
range(stop)  ## Starts from 0

range(start, stop)

range(start, stop, step)
```


### Example 1 - Stop value

Display the numbers 0 to 9, ten numbers in total.  The __loop variable__ is `counter` and it holds the current value from the range function.

``` python
# Fixed loop: Stop value
for counter in range(10):

    # Display loop variable
    print(counter)
```


### Example 2 - Start and stop values

Display the numbers 1 to 9.

``` python
# Fixed loop: Start, Stop values
for counter in range(1, 10):

    # Display loop variable
    print(counter)
```


### Example 3 - Start, stop, and stop values

Display the odd numbers from 1 to 9.

``` python
# Fixed loop: Start, Stop, Step values
for counter in range(1, 10, 2):

    # Display loop variable
    print(counter)
```


## Conditional loop (while)

Before a conditional loop starts, the number of times it will run ***is not*** stated.

It only runs if the comparison is `True`.  Each time the code is completed the comparison is checked again.  If it is still `True` the code is run again.


## Example

``` python
# Get value from user and cast to integer
value = int(input("Enter a value: "))

# Check value
while value < 10:

    # True: do the following

    # Increment value
    value = value + 1

    # True: Display value
    print(value)
```
