#
# Chapter 1: Creating NumPy Array
<br>
<br>

## 1. Importing NumPy
```python
import numpy as np
```

<br>

## 2. Creating Arrays from Lists or Tuples
### From list (1 dimensional array i.e., vector):
```python
arr = np.array([1, 2, 3])
```


### From list of lists (n dimensional array):
```python
arr = np.array([[1,2,3],[2,5,6],[8,1,7],[8,9,23]])
```
<br>

## 3. Creating Arrays with Initial Values
### Zeros:
```python
arr1 = np.zeros(5)   # [0. 0. 0. 0. 0.]
arr2 = np.zeros((2,3))  # 2x3 array of zeros
```

### Ones:
```python
arr1 = np.ones(4)     # [1. 1. 1. 1.]
arr2 = np.ones((3,4))  # 3x4 array of ones
```
### Identity matrix
```python
np.identity(3)  # 3x3 identity matrix
```
### Diagonal from list
```python
np.diag([1, 2, 3])  # 3x3 diagonal matrix
````


<br>

## 4. Creating Sequences
### arange(start, stop, step)
```python
np.arange(0, 10, 2)  # [0 2 4 6 8]
```

### linspace(start, stop, num)
```python
np.linspace(0, 1, 5)  # [0.  0.25 0.5  0.75 1.]
```

<br>

## 5. Creating Random Arrays
### Uniform (0 to 1)
```python
np.random.rand(3)        # 3x1 matrix 
np.random.rand(3, 2)     # 3x2 matrix
```

### Normal Distribution (mean=0, sd=1, no fixed range)
```python
np.random.randn(3, 4)
```

### Integers
```python
np.random.randint(1, 10, size=(2, 3))  # Random integers from 1 to 9
```
