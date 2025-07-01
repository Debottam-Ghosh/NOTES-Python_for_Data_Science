#
# Chapter 4: Indexing, Slicing, iteration

<br>
<br>

# Indexing
**1 Dimensional Array**
```bash
arr = np.array([10, 20, 30, 40])

arr[0]       # 10
arr[-1]      # 40
```
<br> 

**2 Dimendional Array**
```bash
a = np.array([[1, 2, 3],
              [4, 5, 6]])

a[1]         # [4,5,6] (row 1)
a[0, 1]      # 2 (row 0, column 1)
a[1][2]      # 6 (row 1, column 2)
```
<br>
<br>

---

<br>

# Slicing

Slicing in NumPy allows you to extract sub-arrays using a concise syntax.

## 1 Dimensional Slicing
```bash
import numpy as np
a = np.array([10, 20, 30, 40, 50])
```
<br>

**General Form:** `arr[start:stop:step]`
<br>

| Slice     | Output             | Meaning               |
| --------- | ------------------ | --------------------- |
| `a[1:4]`  | `[20 30 40]`       | From index 1 to 3     |
| `a[:3]`   | `[10 20 30]`       | From start to index 2 |
| `a[2:]`   | `[30 40 50]`       | From index 2 to end   |
| `a[::2]`  | `[10 30 50]`       | Every 2nd element     |
| `a[::-1]` | `[50 40 30 20 10]` | Reversed array        |


<br>

## Slicing in 2D Arrays
```bash
b = np.array([[1, 2, 3],
              [4, 5, 6],
              [7, 8, 9]])
```

<br>

**Genaral Form:** `arr[row_start:row_stop, col_start:col_stop]`

<br>

| Slice           | Output                        | Meaning                   |
| --------------- | ----------------------------- | ------------------------- |
| `b[0:2, 1:3]`   | `[[2 3], [5 6]]`              | Rows 0–1, Columns 1–2     |
| `b[:, 1]`       | `[2 5 8]`                     | All rows, column 1        |
| `b[1, :]`       | `[4 5 6]`                     | Row 1, all columns        |
| `b[:2, :2]`     | `[[1 2], [4 5]]`              | Top-left 2x2 subarray     |
| `b[::-1, ::-1]` | `[[9 8 7], [6 5 4], [3 2 1]]` | Reversed rows and columns |

<br>
<br>

---

<br>

# Iteration on NumPy Arrays
Unlike Python lists, NumPy is optimized to **avoid loops using vectorized operations**. But when you need to iterate, here are the key methods:
<br>

## 1. Iterating Over 1D Arrays
```bash
import numpy as np

a = np.array([10, 20, 30])
for item in a:
    print(item)
```

**Output:**
```bash
10
20
30
```

<br>

## 2. Iterating Over 2D Arrays (Row-wise)
```bash
a = np.array([[1, 2], [3, 4]])

for row in a:
    print(row)
```
**Output:**
```
[1 2]
[3 4]
```
###### Each row is a 1D NumPy array.

<br>

##  3. Iterating Over Each Element (Element-wise)
**Use `np.nditer()`:**
```bash
for val in np.nditer(a):
    print(val)
```
**Output:**
```
1
2
3
4
```







