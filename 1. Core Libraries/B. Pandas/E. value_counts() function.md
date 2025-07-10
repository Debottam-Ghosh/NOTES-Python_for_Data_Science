#
# Chapter 5: value_counts() function

<br>
<br>

`value_counts()` counts the number of occurrences of each unique value in a **Series** (i.e., a single column of a DataFrame). 
<br>
Remember value_counts() only works on series.

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



