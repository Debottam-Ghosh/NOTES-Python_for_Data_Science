#
# Chapter 7: Broadcasting in NumPy

<br>
<br>

**Broadcasting** in NumPy allows us to perform **arithmetic operations on arrays of different shapes** without reshaping them. It automatically adjusts the **smaller array to match the larger array's shape** by replicating its values along the necessary dimensions.

<br>

### Basic Idea:
When performing operations on two arrays:
- NumPy compares their shapes.
- It "stretches" the smaller array across the larger one, without copying data, if compatible.

<br>

### Broadcasting Rules:
If the arrays have different dimensions, prepend 1s to the shape of the smaller array.
Two dimensions are compatible when:
- They are equal, or
- One of them is 1

![image](https://github.com/user-attachments/assets/9f74303a-41de-4b66-8b43-dc6cca9b9126)

### Example 1: Scalar and Array
```python
import numpy as np
a = np.array([1, 2, 3])
b = 10

print(a + b)  # Output: [11 12 13]
```
###### The scalar 10 is broadcast to [10, 10, 10].

<br>

### Example 2: 2D and 1D
```python
a = np.array([[1, 2, 3],
              [4, 5, 6]])

b = np.array([10, 20, 30])

print(a + b)
```
##### Output
```
[[11 22 33]
 [14 25 36]]
```
Here, `b` is broadcast to both rows of `a`

<br>

### Summary Table:
| Shape A   | Shape B   | Result Shape   |
| --------- | --------- | -------------- |
| (3, 1)    | (1, 4)    | (3, 4)         |
| (5, 1, 6) | (1, 4, 1) | (5, 4, 6)      |
| (3, 2)    | (3,)      | ❌ Incompatible |
| (4, 3, 2) | (3, 2)    | (4, 3, 2)      |






