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

| index | Name    | Score |
| ----- | ------- | ----- |
| 0     | Alice   | 90    |
| 1     | Bob     | 85    |
| 2     | Charlie | 95    |








