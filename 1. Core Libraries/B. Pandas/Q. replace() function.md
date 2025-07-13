#
# Chapter 17: replace() function

<br>
<br>

The `replace()` function in Pandas is used to replace values in a Series or DataFrame with other specified values.

<br>

## Examples:

<br>

### 1. Replace Specific Value:
```bash
df.replace(0, None)  # Replaces all 0s with None
```
<br>

### 2. Replace Using Dictionary:
```bash
df.replace({0: None, -1: 999}) # Replaces all 0s with None and all -1s with 999
```

<br>

### 3. Column-Specific Replacement:
```bash
df.replace({'column1': {0: None}, 'column2': {-1: 999}})
```
