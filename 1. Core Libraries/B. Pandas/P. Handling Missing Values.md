# 
# Chapter 16: Handling Missing Values 

<br>
<br>


## Step 1: Detect Missing Values
#### ⭐ Column-wise count 
```bash
df.isnull().sum()          
```

<br>

##### You can use `.info()` to check non-null counts 

<br>

## Step 2: Decide on Strategy
| Situation                 | Suggested Action                             | Code                                                                                                 |
| ------------------------- | -------------------------------------------- | ----------------------------------------------------------------------------------------------------------- |
| **Few missing values**    | **Drop** rows/columns                        | `df.dropna()`<br>`df.dropna(axis=1)`                                                                        |
| **Numerical data**        | **Fill** with mean, median, or interpolation | `df['col'].fillna(df['col'].mean())`<br>`df['col'].fillna(df['col'].median())`<br>`df['col'].interpolate()` |
| **Categorical data**      | **Fill** with mode or "Unknown"              | `df['col'].fillna(df['col'].mode()[0])`<br>`df['col'].fillna('Unknown')`                                    |
| **Time series**           | Use **forward fill** or **backward fill**    | `df.fillna(method='ffill')`<br>`df.fillna(method='bfill')`                                                  |
| **Critical missing data** | Consider **domain-specific logic** or drop   | `df = df[df['income'].notnull()]`<br>`df['col'].fillna(custom_logic(df))`                                   |

<br>

## Step 3: Handle Missing Values

### Situation 1 - Drop Missing:
```bash
df.dropna()                  # Drop rows with any NaN
df.dropna(axis=1)            # Drop columns with any NaN
df.dropna(subset=['col'])    # Drop rows with NaN only in 'col'. You can pass multiple columns
df.dropna(thresh=2)          # Keep rows with at least 2 non-NaNs
```

<br>

### Situation 2 - Fill Missing:
```bash
df.fillna(0)                            # Fill all NaNs with 0
df['col'].fillna(df['col'].mean())     # Fill with mean
df['col'].fillna(df['col'].mode()[0])  # Fill with mode
df.fillna(method='ffill')              # Forward fill
df.fillna(method='bfill')              # Backward fill
```

<br>

## Step 4: Verify
After filling or dropping:
```bash
df.isnull().sum()  # Should be 0 or as expected
```
