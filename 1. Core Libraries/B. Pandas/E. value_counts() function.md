#
# Chapter 5: value_counts() function

<br>
<br>

`value_counts()` counts the number of occurrences of each unique value in a **Series** (i.e., a single column of a DataFrame). 
<br>
Remember value_counts() works on series and returns a series.

<br>

### Basic Syntax:
```
df['column'].value_counts()
```

<br>

### Example:
```bash
import pandas as pd

data = {'City': ['Delhi', 'Mumbai', 'Delhi', 'Chennai', 'Mumbai', 'Mumbai']}
df = pd.DataFrame(data)

print(df['City'].value_counts())
```
**Output:**
```
Mumbai     3
Delhi      2
Chennai    1
Name: City, dtype: int64
```

<br>
<br>

## Arithmetic Operations
you can perform arithmetic operations on value_counts() results in pandas, just like on any Series — because value_counts() returns a pandas Series.

<br>

### Example:
```bash
import pandas as pd

data = pd.Series(['apple', 'banana', 'apple', 'orange', 'banana', 'apple'])

# Get value counts
vc = data.value_counts()
print(vc)
```

**Output:**
```
apple     3
banana    2
orange    1
dtype: int64
```

<br>

### Example 1: Add a number to all counts
```
vc + 1
```
**Result:**
```
apple     4
banana    3
orange    2
dtype: int64
```
<br>
Similarly, you can do:
```
vc - 1
vc*3
vc/2
```
<br>

### Example 2: You can use these operations on two series too
```
s1 = pd.Series(['A', 'B', 'A', 'C'])
s2 = pd.Series(['A', 'B', 'B', 'D'])

vc1 = s1.value_counts() + vc2 = s2.value_counts()
```

**Result:**
```
A  3
B  3
C  1
D  1
```











