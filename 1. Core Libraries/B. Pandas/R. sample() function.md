#
# Chapter 18: sample() function

<br>
<br>

The `sample()` function in Pandas is used to randomly select **rows** or **columns** from a DataFrame or Series.

<br>

## Examples

<br>

### 1. Sample 3 random rows
```
df.sample(n=3)
```

### 2. Sample 20% of the data
```
df.sample(frac=0.2)
```
###### `n` and `frac` are mutually exclusive — use one at a time.
<br>

### 3. Sample with replacement (allows duplicates)
```
df.sample(n=5, replace=True)
```
<br>

### 4. Sample with a fixed random seed
```
df.sample(n=3, random_state=42)
```
##### Use random_state for reproducible results (especially in ML tasks).

<br>

### 5. Sample columns instead of rows
```bash
df.sample(n=2, axis=1)  # Select 2 random columns
```
