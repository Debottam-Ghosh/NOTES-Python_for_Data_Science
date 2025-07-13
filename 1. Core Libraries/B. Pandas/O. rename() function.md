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
###### NOTE: Name of the 'Index' column will not changed.

<br>
<br>

### You can also change the indexes' names (Not the column name) also:
```bash
df.rename(index={'0': 'Student1', '1': 'Student2'})
```
**Output:**
| Index | Math  | Sci | Eng |
| ----- | ----------- | ------- | --- |
| Student 1     | 90          | 88      | 70  |
| Student 2     | 80          | 85      | 60  |


<br>

<br>

You can change indexes and columns simultaneously like:
```bash
df.rename(columns={'Math': 'Mathematics', 'Sci':'Science', 'Eng': 'English'}, index={'0': 'Student1', '1': 'Student2'})
```
**Output:**
| Index | Mathematocs  | Science | English |
| ----- | ----------- | ------- | --- |
| Student 1     | 90          | 88      | 70  |
| Student 2     | 80          | 85      | 60  |

