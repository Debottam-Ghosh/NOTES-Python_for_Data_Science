#
# Chapter 6: Reshaping NumPy Arrays

<br>
<br>

**Reshaping** means changing the shape (dimensions) of a NumPy array without changing the data.

<br>

## `reshape()` Method
```bash
arr.reshape(rows, columns)
```

###### The total number of elements must remain the same

**Example:**
```bash
a = np.arange(12)       # [0, 1, ..., 11]
a.reshape(3, 4)         # shape (3, 4)
```

<br>

## Using `-1` (Auto-calculate dimension)
Let NumPy automatically infer one dimension:

```bash
a = np.arange(8)
a.reshape(2, -1)   # → shape (2, 4)
a.reshape(-1, 4)   # → shape (2, 4)
```
###### **Note:** Only one dimension can be -1

<br>

## Flattening (1D Conversion)
### `flatten()` → Returns a copy:
```bash
a = np.array([[1, 2], [3, 4]])
a.flatten()         # [1 2 3 4]
```
<br>
  
### `ravel()` → Returns a view (if possible):
```bash
a.ravel()           # [1 2 3 4]
```

<br>

## Reshape in Higher Dimensions
```bash
a = np.arange(24)
a.reshape(2, 3, 4)  # 3D array with shape (2, 3, 4)
```



