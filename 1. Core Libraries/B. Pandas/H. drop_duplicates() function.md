#
# Chapter 8: drop_duplicates() funtion

<br>
<br>

`drop_duplicates()` in Pandas removes duplicate rows from a DataFrame or Series.

## Basic Syntax:
```bash
df.drop_duplicates(subset=None, keep='first', inplace=False)
````

<br>

## Key Parameters
| Parameter | Description                                                         |
| --------- | ------------------------------------------------------------------- |
| `subset`  | Column(s) to check for duplicates (default: all columns)            |
| `keep`    | Which duplicate to keep: `'first'`, `'last'`, or `False` (drop all) |
| `inplace` | If `True`, modifies the original DataFrame (no return). Default: 'False'|


###### In practice, we mostly use default parameters except 'subset'. So we will use: `df.drop_duplicates(subset=[['col1','col2',..]])`


<br>
<br>

## Example:
```bash
import pandas as pd

data = {
    'Name': ['Alice', 'Bob', 'Alice', 'David'],
    'Age': [25, 30, 25, 40]
}

df = pd.DataFrame(data)

print("Original DataFrame:")
print(df)

print("\n After drop_duplicates():")
print(df.drop_duplicates())
```

**Output**
```
Original DataFrame:
    Name  Age
0  Alice   25
1    Bob   30
2  Alice   25
3  David   40

After drop_duplicates():
    Name  Age
0  Alice   25
1    Bob   30
3  David   40
```

<br>

## More Examples:
```bash
# Drop duplicates based on 'Name' only
df.drop_duplicates(subset='Name')

# Keep the last occurrence instead of first
df.drop_duplicates(keep='last')

# Remove all duplicates (keep=False)
df.drop_duplicates(keep=False)

# Drop duplicates and update the original DataFrame
df.drop_duplicates(inplace=True)
```
