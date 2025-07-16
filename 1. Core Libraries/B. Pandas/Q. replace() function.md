#
# Chapter 17: replace() function

<br>
<br>

The `replace()` function in Pandas is used to replace values in a Series or DataFrame with other specified values.

<br>

## Examples:

<br>

### 1. Replace Specific Value:
```python
df.replace(0, None)  # Replaces all 0s with None
```
<br>

### 2. Replace Using Dictionary:
```python
df.replace({0: None, -1: 999}) # Replaces all 0s with None and all -1s with 999
```

<br>

### 3. Column-Specific Replacement:
```python
df.replace({'column1': {0: None}, 'column2': {-1: 999}})
```

<br>
<br>

## Append a New Row:
```python
df.loc[len(df)] = ['David', 40]
```


<br>

## To Delete the Last Row (or Any Row)
```python
df = df.drop(index=3)  # drops row with index = 3
df = df.drop(index=len(df)-1)  # drops the last row
```
