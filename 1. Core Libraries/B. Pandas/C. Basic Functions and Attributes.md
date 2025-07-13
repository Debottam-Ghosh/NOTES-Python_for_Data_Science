#
# Chapter 3: Basic Functions and Attributes

<br>
<br>

| **Function / Attribute** | **Short Description**                                                                                    |
| ------------------------ | -------------------------------------------------------------------------------------------------------- |
| `df.head(n)`             | Returns the **first `n` rows** of the DataFrame (default is 5). Useful for a quick preview.              |
| `df.tail(n)`             | Returns the **last `n` rows** of the DataFrame (default is 5). Helpful for checking end of data.         |
| `df.shape`               | Returns a **tuple** showing the number of **rows and columns** in the form `(rows, columns)`.            |
| `df.columns`             | Lists the **column labels** (names) of the DataFrame.                                                    |
| `df.dtypes`              | Shows the **data type** (`int64`, `object`, etc.) of each column.                                        |
| `df.info()`              | Gives a **summary**: number of non-null entries, column types, and memory usage.                         |
| `df.describe()`          | Provides **statistical summary** (count, mean, std, min, max, quartiles) for **numerical columns** only. |
| `df.index`               | Inspect or manipulate row labels                                                                         |
| `df.values`              | Access data without labels                                                                               |
| `df.astype()`            | Convert the data type of a Series or DataFrame column(s) to a specified type. <br> `df['Age'] = df['Age'].astype(int)`  # Convert a Single Column <br> `df = df.astype({'Age': 'float', 'Name': 'string'})`  # Convert Multiple Columns  |








