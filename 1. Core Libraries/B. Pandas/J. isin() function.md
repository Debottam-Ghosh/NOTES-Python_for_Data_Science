#
# Chapter 10: isin() function

<br>
<br>

`insin()` checks whether each element in a Series or DataFrame is present in a list or another iterable.

<br>

## Basic Syntax:
```bash
df['column'].isin([value1, value2, ...])
```
##### Returns a boolean Series: True if the element is in the list, False otherwise.

<br>

## Example:
```bash
import pandas as pd

data = {'Player': ['Kohli', 'Rohit', 'Dhoni', 'Rahul'], 'Runs': [80, 65, 70, 50]}
df = pd.DataFrame(data)

# Filter players who are either 'Kohli' or 'Dhoni'
df[df['Player'].isin(['Kohli', 'Dhoni'])]
```
**Output:**
```bash
  Player  Runs
0  Kohli    80
2  Dhoni    70
```

### Works well with `~` for negation:

```bash
df[~df['Player'].isin(['Kohli', 'Dhoni'])]  # Not in
```
