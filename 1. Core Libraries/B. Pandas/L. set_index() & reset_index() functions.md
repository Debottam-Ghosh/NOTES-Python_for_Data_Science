#
# Chapter 12: set_index() & reset_index() 

<br>
<br>

## `set_index()` in pandas
<br>

### What it does:
- Moves one or more columns into the index (row labels).
- Helps in organizing, grouping, and faster row lookup.

<br>

### Syntax:
```bash
df.set_index('column_name')
```
<br>

### Example:
```bash
df = pd.DataFrame({
    'ID': [1, 2, 3],
    'Name': ['Alice', 'Bob', 'Charlie'],
    'Score': [90, 85, 95]
})

df.set_index('ID')
```
**Result:**
| ID | Name    | Score |
| -- | ------- | ----- |
| 1  | Alice   | 90    |
| 2  | Bob     | 85    |
| 3  | Charlie | 95    |
##### Now ID is no longer a column — it’s the index.
<br>

---

<br>


## `reset_index()` in pandas
### What it does:
- Converts the index back into a column.
- Resets index to default [0, 1, 2, …].
<br>

### Syntax:
```bash
df.reset_index()
```
<br>

### Example (continued from above):
```bash
df.reset_index()
```
**Result:**
| index | ID | Name    | Score |
| ----- | -- | ------- | ----- |
| 0     | 1  | Alice   | 90    |
| 1     | 2  | Bob     | 85    |
| 2     | 3  | Charlie | 95    |
##### The custom index (ID) is now a column again, and index is back to default.
<br>

### `drop=True` parameter in reset_index()
```bash
df.reset_index(drop=True)
```
- This removes the current index without adding it as a column.
- Keeps the data clean and avoids unnecessary columns.

**Result:**

| Name    | Score |
| ------- | ----- |
| Alice   | 90    |
| Bob     | 85    |
| Charlie | 95    |


<br>
<br>

### TRICK that I follow:
You can use reset_index() for converting a series to a dataframe!
```bash
s = pd.Series([85, 90, 78], name='Score')
print(s)
```
#### Output is a series here:
```
0    85
1    90
2    78
Name: Score, dtype: int64
```
<br>

### But we can convert it to a dataframe using:
```bash
df=s.reset_index()
```
**Output:**
| index | Score |
| ----- | ----- |
| 0     | 85    |
| 1     | 90    |
| 2     | 78    |









