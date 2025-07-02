#
# Chapter 8: Functions in NumPy

<br>
<br>

## 1. Array Creation
| Function                             | Description                            |
| ------------------------------------ | -------------------------------------- |
| `np.array()`                         | Create an array from list or tuple     |
| `np.zeros((r, c))`                   | Array of all 0s                        |
| `np.ones((r, c))`                    | Array of all 1s                        |
| `np.full((r, c), value)`             | constant matrix                        |
| `np.eye(n)`/`np.identity()       `   | Identity matrix (n×n)                  |
| `np.arange(start, stop, step)`       | Range of values like `range()`         |
| `np.linspace(start, stop, num)`      | Evenly spaced values between start and stop|
| `np.random.rand(m, n)`               | Uniform random values in \[0, 1)       |
| `np.random.randn(m, n)`              | Random values from normal distribution |
| `np.random.randint(low, high, size)` | Random integers                        |


<br>

## 2. Array Inspection
| Function               | Description              |
| ---------------------- | ------------------------ |
| `arr.shape`            | Shape (rows, cols)       |
| `arr.ndim`             | Number of dimensions     |
| `arr.size`             | Total number of elements |
| `arr.dtype`            | Data type                |
| `arr.itemsize`         | Bytes per element        |
| `np.info(np.function)` | Info on a NumPy function |

<br>


## 3. Reshaping & Flattening
| Function                       | Description                 |
| ------------------------------ | --------------------------- |
| `arr.reshape(r, c)`            | Change shape                |
| `arr.flatten()`                | 1D version                  |
| `arr.ravel()`                  | Flatten without copy        |
| `np.expand_dims(arr, axis)`    | Add dimension               |
| `np.squeeze(arr)`              | Remove singleton dimensions |
| `np.transpose(arr)` or `arr.T` | Swap axes                   |


<br>


## 4. Indexing & Slicing
| Function                 | Description        |
| ------------------------ | ------------------ |
| `arr[i]` or `arr[i, j]`  | Basic indexing     |
| `arr[:, i]`, `arr[i, :]` | Slice rows/columns |
| `arr[::2]`               | Step slicing       |
| `arr[arr > 5]`           | Boolean indexing   |
| `arr[[0, 2], [1, 2]]`    | Fancy indexing     |


<br>

## 5. Math & Aggregations
| Function                     | Description         |
| ---------------------------- | ------------------- |
| `np.sum(arr, axis=0)`        | Sum along axis      |
| `np.mean()`, `np.median()`   | Mean, median        |
| `np.std()`, `np.var()`       | Std. dev., variance |
| `np.min()`, `np.max()`       | Min/max value       |
| `np.argmin()`, `np.argmax()` | Index of min/max    |
| `np.cumsum()`                | Cumulative sum      |
| `np.cumprod()`               | Cumulative product  |


<br>

## 6. Element-wise Operations
| Function                            | Description                          |
| ----------------------------------- | ------------------------------------ |
| `np.add()`, `np.subtract()`         | Element-wise addition/subtraction    |
| `np.multiply()`, `np.divide()`      | Element-wise multiplication/division |
| `np.power(arr, n)`                  | Raise to power                       |
| `np.sqrt()`, `np.exp()`, `np.log()` | Square root, exponent, log           |


<br>

## 7. Linear Algebra
| Function            | Description           |
| ------------------- | --------------------- |
| `np.dot(a, b)`      | Dot product           |
| `np.matmul(a, b)`   | Matrix multiplication |
| `np.linalg.inv(a)`  | Inverse of a matrix   |
| `np.linalg.det(a)`  | Determinant           |
| `np.linalg.eig(a)`  | Eigenvalues/vectors   |
| `np.linalg.norm(a)` | Vector/matrix norm    |


<br>

## 8. Sorting & Searching
| Function                    | Description                            |
| --------------------------- | -------------------------------------- |
| `np.sort(arr)`              | Sort array                             |
| `np.argsort(arr)`           | Indices that would sort                |
| `np.where(condition)`       | Return indices where condition is True |
| `np.unique(arr)`            | Unique elements                        |



<br>

## 9. Random & Sampling
| Function                      | Description                            |
| ----------------------------- | -------------------------------------- |
| `np.random.seed(n)`           | Set random seed                        |
| `np.random.shuffle(arr)`      | Shuffle along the first axis           |
| `np.random.choice(arr, size)` | Random sample with/without replacement |

<br>

## 10. Other Handy Utilities
| Function                 | Description                       |
| ------------------------ | --------------------------------- |
| `np.clip(arr, min, max)` | Limit values in range             |
| `np.isnan(arr)`          | Detect NaNs                       |
| `np.isinf(arr)`          | Detect infinite values            |
| `np.allclose(a, b)`      | Compare arrays approximately      |
| `np.array_equal(a, b)`   | Check if arrays are exactly equal |

