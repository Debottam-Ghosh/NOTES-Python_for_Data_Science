#
# Chapter 3: What NumPy is a better choice over list for data science

<br>
<br>

## 1. Speed (Execution Time)
**NumPy is written in C under the hood**. Operations like addition, multiplication, and matrix operations are executed using highly optimized native code.

```bash
# NumPy
a = np.array([1, 2, 3])
b = np.array([4, 5, 6])
a + b  # Fast, vectorized

# List
a = [1, 2, 3]
b = [4, 5, 6]
[i + j for i, j in zip(a, b)]  # Slower, loop-based
```
<br>

## 2. Memory Efficiency
NumPy arrays use contiguous memory blocks and store data compactly. **Lists store references to objects**, which takes more memory.
```bash
import numpy as np
import sys

arr = np.array([1, 2, 3, 4])
lst = [1, 2, 3, 4]

sys.getsizeof(arr)  # Smaller
sys.getsizeof(lst)  # Larger
```
<br>

## 3. Multidimensional Support
NumPy makes working with 2D and 3D arrays easy. Lists require manual nesting and custom logic.
```bash
# NumPy
mat = np.array([[1, 2], [3, 4]])
mat.T  # Transpose directly

# List
mat = [[1, 2], [3, 4]]
list(zip(*mat))  # More work
```
<br>

## 4. Vectorized Operations & Broadcasting
```bash
a = np.array([1, 2, 3])
a * 2  # Output: [2 4 6] → Element-wise

# With lists
a = [1, 2, 3]
a * 2  # Output: [1, 2, 3, 1, 2, 3] → Repetition, not multiplication
```
<br>

## 5. Rich Functionality
NumPy has tons of mathematical, statistical, and linear algebra functions:
```bash
np.mean(arr), np.std(arr), np.dot(A, B), np.linalg.inv(A), ...
```
<br>

## When Lists Might Be Better
- When you need to store different types in one container
- For non-numerical or general-purpose data
- Simpler tasks that don't involve heavy computation




