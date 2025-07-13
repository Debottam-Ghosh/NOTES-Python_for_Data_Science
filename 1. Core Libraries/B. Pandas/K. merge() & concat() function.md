#
# Chapter 11: merge() & concat() function

<br>
<br>

# `merge()` function
`merge()` is used to combine two DataFrames based on common columns or indices, similar to SQL JOIN operations.

<br>

## Basic Syntax:
```bash
df1.merge(df2, how='inner', on=None)
# OR 
df1.merge(df2, how='inner', left_on=None, right_on=None)
```

<br>

## Key Parameters
| Parameter                    | Description                                             |
| ---------------------------- | ------------------------------------------------------- |
| `left`, `right`              | The two DataFrames you want to merge                    |
| `how`                        | Type of join: `'inner'`, `'outer'`, `'left'`, `'right'` |
| `on`                         | Column name(s) to join on (must be in both DataFrames)  |
| `left_on`                    | Column(s) from left DataFrame to join on                |
| `right_on`                   | Column(s) from right DataFrame to join on               |

<br>

## Types of Joins
| Join Type | Description                               | Keeps                     |
| --------- | ----------------------------------------- | ------------------------- |
| `'inner'` | Only matching rows in both (DEFAULT)      | Common records only       |
| `'outer'` | All rows from both, fill missing with NaN | Union of all rows         |
| `'left'`  | All rows from left + matches from right   | Left DataFrame dominates  |
| `'right'` | All rows from right + matches from left   | Right DataFrame dominates |

<br>

## Examples:
### 1. Inner Join on a column
```bash
df1.merge(df2, on='id', how='inner')
```
<br>

### 2. Left Join with different column names
```bash
df1.merge(df2, left_on='emp_id', right_on='staff_id', how='left')
```

<br>
<br>

---

<br>
<br>

# concat() function
`concat()` is a Pandas function used to combine multiple Series or DataFrames along rows (axis=0) or columns (axis=1)

<br>

## Row-wise Concatenation (axis=0, default)
```bash
import pandas as pd

df1 = pd.DataFrame({'Name': ['Alice', 'Bob'], 'Age': [25, 30]})
df2 = pd.DataFrame({'Name': ['Charlie', 'David'], 'Age': [35, 40]})

pd.concat([df1, df2])
```
**Output:**
```
      Name  Age
0    Alice   25
1      Bob   30
0  Charlie   35
1    David   40
```
##### Note: Index is duplicated unless you use `ignore_index=True`

<br>

## Column-wise Concatenation (axis=1)
```bash
df3 = pd.DataFrame({'City': ['Delhi', 'Mumbai']})
pd.concat([df1, df3], axis=1)
```
**Output**
```
    Name  Age   City
0  Alice   25  Delhi
1    Bob   30  Mumbai
```
