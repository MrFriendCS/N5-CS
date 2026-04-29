# Logical Operators

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
