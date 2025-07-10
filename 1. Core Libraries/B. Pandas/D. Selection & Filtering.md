#
# Chapter 4: Data Selection & Filtering

<br>
<br>

| Function / Syntax       | Description                           |
| ----------------------- | ------------------------------------- |
| `df['col']`             | Select a column                       |
| `df[['col1', 'col2']]`  | Select multiple columns               |
| `df[df['col'] > 10]`    | Boolean filtering or Masking          |
| `df.iloc[rows, cols]`   | Select by position (index-based)      |
| `df.loc[rows, cols]`    | Select by labels (index/column names) |
<br>

#### Example of `.iloc` Variations
```bash
import pandas as pd
# Sample DataFrame
data = {
    'Name': ['Alice', 'Bob', 'Charlie', 'David', 'Eva'],
    'Age': [25, 30, 35, 40, 45],
    'City': ['New York', 'Los Angeles', 'Chicago', 'Houston', 'Phoenix']
}

df = pd.DataFrame(data) #Converting the dict to pandas dataframe

print("Original DataFrame:")
print(df)

print("\n 1. Selecting ONLY rows (first 3 rows):")
print(df.iloc[0:3])  # Rows 0 to 2, all columns

print("\n 2. Selecting ONLY columns (column 1 and 2):")
print(df.iloc[:, 1:3])  # All rows, columns 1 and 2 (Age and City)

print("\n 3. Selecting specific rows and columns (row 0, column 1):")
print(df.iloc[0, 1])  # Age of first person (25)

print("\n 4. Selecting multiple rows & columns (rows 0 & 2, columns 0 & 2):")
print(df.iloc[[0, 2], [0, 2]])  # Name and City of Alice and Charlie

print("\n5. Slicing rows and columns (rows 1:4, columns 0:2):")
print(df.iloc[1:4, 0:2])  # Rows 1 to 3, columns 0 to 1

print("\n 6. Fancy indexing rows and all columns (rows 0, 3, 4):")
print(df.iloc[[0, 3, 4], :])  # Alice, David, Eva with all columns

print("\n 7. Fancy indexing columns and all rows (columns 2, 0):")
print(df.iloc[:, [2, 0]])  # City and Name columns
```

<br>
<br>

#### Example of Masking (or Boolean Filtering)
```bash
df[df['age']>25]  # all rows with age>25

df[(df[age]>25) & (df[sex]==male)] # all male with age>25

# or you can also do this:
mask1 = df[age]>25
mask2 = df[sex]==male
df[mask1 & mask2] 
```
<br>

**Rule of Thumb:**
- **Basic Syntax:** `df[(condition 1) Bitwise Logical Operator (condition 2) ...]`
- Use `&`, `|`, `~` for AND, OR, NOT in Pandas.
- **Always** wrap each condition in parentheses when combining them.

<br>
<br>
