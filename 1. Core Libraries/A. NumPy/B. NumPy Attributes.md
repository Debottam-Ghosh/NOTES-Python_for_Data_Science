# 
# Chapter 2: NumPy Attributes

<br>


<br>



## 1. `.ndim` — Number of Dimensions
```bash
arr.ndim
```
Returns the number of axes (dimensions).

#### Example:
```bash
np.array([1, 2, 3]).ndim  # 1
np.array([[1, 2], [3, 4]]).ndim  # 2
```
<br>


## 2. .shape — Shape of the Array
```bash
arr.shape
```
Returns a tuple showing the size in each dimension.

#### Example:
```bash
np.array([[1, 2], [3, 4]]).shape  # (2, 2)
```
<br>



## 3. `.size` — Total Number of Elements
```bash
arr.size
```
Returns the total number of elements in the array.

#### Example:
```bash
np.array([[1, 2], [3, 4]]).size  # 4
```

<br>



## 4. `.dtype` — Data Type of Elements
```bash
arr.dtype
```
Shows the data type (int32, float64, etc.).

#### Example:
```bash
np.array([1, 2, 3]).dtype  # dtype('int64') (depends on system)
```
<br>



## 5. `.itemsize` — Size (in bytes) of One Element
```bash
arr.itemsize
```
Shows how many bytes each element occupies.

#### Example:

```bash
np.array([1, 2, 3], dtype=np.int32).itemsize  # 4
```
<br>



## 6. `.T` — Transpose of the Array
```bash
arr.T
```
Transposes the array (useful for matrices).

#### Example:
```bash
np.array([[1, 2], [3, 4]]).T  # [[1, 3], [2, 4]]
```
<br>



## 7. ndarray.real and ndarray.imag
Used for complex number arrays:
```bash
arr.real   # Real part
arr.imag   # Imaginary part
```

## Example Summary:
```bash
import numpy as np

a = np.array([[1, 2, 3], [4, 5, 6]])

print("Shape:", a.shape)        # (2, 3)
print("Dimensions:", a.ndim)    # 2
print("Size:", a.size)          # 6
print("Data type:", a.dtype)    # int64
print("Item size:", a.itemsize) # 8 (bytes per int)
```
