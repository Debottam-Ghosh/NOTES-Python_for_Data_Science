#
# Chapter 9: Groupby() function

<br>
<br>

`groupby()` used to group rows of a DataFrame based on the values in one or more columns, and then apply aggregation or transformation functions like sum(), mean(), count(), etc.

<br>

## Basic Syntax:
```bash
df.groupby('column_name')
```
You usually combine it with an aggregation function:

```bash
df.groupby('column_name')['other_column'].sum()
```

<br>
<br>

## Example:
```python
import pandas as pd

data = {
    'Department': ['Sales', 'Sales', 'HR', 'HR', 'IT'],
    'Salary': [50000, 55000, 60000, 62000, 70000]
}

df = pd.DataFrame(data)

# Group by Department and calculate average salary
grouped = df.groupby('Department')['Salary'].mean()
print(grouped)
```
**Output**
```bash
Department
HR       61000.0
IT       70000.0
Sales    52500.0
Name: Salary, dtype: float64
```

<br>
<br>

## Common Aggregation Functions:
| Function    | Description            |
| ----------- | ---------------------- |
| `.sum()`    | Sum of values          |
| `.mean()`   | Average                |
| `.count()`  | Count of non-NA values |
| `.min()`    | Minimum                |
| `.max()`    | Maximum                |
| `.median()` | Median value           |
| `.std()`    | Standard deviation     |

<br>
<br>

## Multiple Aggregations:
```bash
df.groupby('Department')['Salary'].agg(['mean', 'max', 'count'])
```

<br>
<br>

## Group by Multiple Columns:
```bash
df.groupby(['Department', 'JobRole'])['Salary'].mean()
```
