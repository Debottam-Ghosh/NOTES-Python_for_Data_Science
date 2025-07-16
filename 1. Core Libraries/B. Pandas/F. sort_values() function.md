#
# Chapter 6: sort_values() function

<br>
<br>

`sort_values()` is used to sort a Series or DataFrame by values (not by index).

<br>

## For Series
```python
import pandas as pd

s = pd.Series([5, 2, 8, 3], index=['a', 'b', 'c', 'd'])

# Sort (by default in ascending order)
s.sort_values()
```
**Output:**
```python
b    2
d    3
a    5
c    8
dtype: int64
```
<br>

### Descending order:
```python
s.sort_values(ascending=False)
```

<br>
<br>




## For DataFrame
```python
df = pd.DataFrame({
    'name': ['Alice', 'Bob', 'Charlie'],
    'score': [85, 92, 78]
})

# Sort rows by 'score' column
df.sort_values(by='score')
```
**Output:**
```python
     name  score
2  Charlie     78
0    Alice     85
1      Bob     92
```
### Descending:
```bash
df.sort_values(by='score', ascending=False)
```

<br>
<br>

## Sort by Multiple Columns
```python
df = pd.DataFrame({
    'name': ['Alice', 'Bob', 'Charlie', 'Bob'],
    'score': [85, 92, 78, 75]
})

df.sort_values(by=['name', 'score'], ascending=[False, True])
```
###### First sorts by name in descending, then within the same name, by score in ascending order.

<br>
<br>

## In-place Sorting
By default, sort_values() returns a new object without changing the original one. But to sort in place:
```bash
df.sort_values(by='score', inplace=True)
```
###### This changes the original dataframe

<br>
<br>

## Most Used Parameters
| Parameter      | Description                                                         | Example                                           | Output / Effect                                                                 |
| -------------- | ------------------------------------------------------------------- | ------------------------------------------------- | ------------------------------------------------------------------------------- |
| `by`           | Column or list of columns to sort by                                | `df.sort_values(by='score')`                      | Sorts DataFrame rows by the `score` column                                      |
| `ascending`    | Sort order: `True` = ascending (default), `False` = descending      | `df.sort_values(by='score', ascending=False)`     | Sorts scores from high to low                                                   |
| `inplace`      | By default, `False`. If `True`, updates the DataFrame in place                           | `df.sort_values(by='score', inplace=True)`        | Modifies `df` directly, no need for reassignment                                |
| `na_position`  | Where to place NaN values: `'first'` or `'last'`(default)                    | `df.sort_values(by='score', na_position='first')` | NaN scores will appear at the top                                               |s
| `kind`         | Sorting algorithm: `'quicksort'`, `'mergesort'`, `'heapsort'`, etc. | `df.sort_values(by='score', kind='mergesort')`    | Needed when you want a **stable sort** (e.g., preserving order of equal values) |
| `axis`         | Sort rows (`0`, default) or columns (`1`)                           | `df.sort_values(by='score', axis=0)`              | Usually left as default for sorting rows                                        |




