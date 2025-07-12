#
# Chapter 11: merge() function

<br>
<br>

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
| `'inner'` | Only matching rows in both                | Common records only       |
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


