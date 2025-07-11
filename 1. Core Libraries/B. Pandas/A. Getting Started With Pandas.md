#
# Chapter 1: Getting Started With Pandas
<br>
<br>

**Pandas** is an open-source Python library used primarily for **data manipulation and analysis**. It's built on top of NumPy and provides flexible and powerful data structures designed to make working with **structured data (like tables and time series)** fast and easy.
<br>

### What Pandas Does:
- Reads and writes data from various file formats: CSV, Excel, SQL databases, JSON, etc.
- Handles missing data gracefully and provides tools to clean it.
- Filters, sorts, and reshapes data efficiently.
- Aggregates and summarizes data using group operations.
- Performs time series analysis, such as date range generation and resampling.
- Supports label-based indexing, which makes working with rows and columns intuitive.
<br>

Pandas is widely used in data science, finance, machine learning, and any area where structured data is analyzed. It essentially turns raw data into a format that's much easier to analyze and visualize.

<br>

## DataFrame and Series:
Pandas treats a dataset(csv, excel etc.) as a **DataFrame** and when you fetch one row or one column, it is treated as a **Series**
In DataFrame, there are rows and columns and in series, there are index and values


<br>

### Creating a Pandas Series
A Series is a one-dimensional labeled array — like a single column of data.
```bash
# Creating a Series from a list
scores = pd.Series([85, 90, 78, 92])
print(scores)
```
**Output**
```bash
0    85
1    90
2    78
3    92
dtype: int64
```

<br>

You can also give custom index:
```bash
scores = pd.Series([85, 90, 78, 92], index=["Alice", "Bob", "Charlie", "David"])
print(scores)
```
**Output**
```bash
Alice      85
Bob        90
Charlie    78
David      92
dtype: int64
```

<br>
<br>

### Creating a Pandas DataFrame
A DataFrame is a two-dimensional table with rows and columns.

```bash
data = {
    'Name': ['Alice', 'Bob', 'Charlie', 'David'],
    'Math': [85, 90, 78, 92],
    'Science': [88, 85, 82, 95]
}

df = pd.DataFrame(data)
print(df)
```

**Output:**
```bash
      Name  Math  Science
0    Alice    85       88
1      Bob    90       85
2  Charlie    78       82
3    David    92       95
```














