#
# Chapter 15: rename() function

<br>
<br>

The `rename()` function is used to change the names of columns or index labels in a DataFrame.

<br>

## Syntax:
```bash
DataFrame.rename(columns=__)
# OR
DataFrame.rename(index=___)
```


## Examples:
**Original Data:**
| Index | Math | Sci     | Eng     |
| ----- | ---- | ------- | ------- |
| 0     | 90   | 88      | 70      |
| 1     | 80   | 85      | 60      |
<br>

**Renaming Columns Using Dictionary**
```bash
df.rename(columns={'Math': 'Mathematics', 'Sci':'Science', 'Eng': 'English'})
```
**Output:**
| Index | Mathematics | Science | English |
| ----- | ----------- | ------- | --- |
| 0     | 90          | 88      | 70  |
| 1     | 80          | 85      | 60  |

<br>


**Renaming Columns Using Function**
```bash
df.rename(columns=str.upper)  # All columns to uppercase
```

**Output:**
| Index | MATH | SCI     | ENG     |
| ----- | ---- | ------- | ------- |
| 0     | 90   | 88      | 70      |
| 1     | 80   | 85      | 60      |
###### Name of the 'Index' column will not changed

