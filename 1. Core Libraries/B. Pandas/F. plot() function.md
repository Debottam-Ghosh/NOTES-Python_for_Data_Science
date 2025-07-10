#
# Chapter 6: plot() function

<br>
<br>

The `plot()` function is used to visualize data directly from a DataFrame or Series — without needing to manually call Matplotlib.

<br>

### Basic Syntax
```
df.plot(kind='line')  # Default is line plot
```

<br>

### Common Plot Types (kind=)
| Plot Type      | Keyword     | Description                      |
| -------------- | ----------- | -------------------------------- |
| Line           | `'line'`    | Default plot for numerical data  |
| Bar            | `'bar'`     | Vertical bar plot                |
| Horizontal Bar | `'barh'`    | Horizontal bar plot              |
| Histogram      | `'hist'`    | Frequency distribution           |
| Box            | `'box'`     | Box-and-whisker plot             |
| Area           | `'area'`    | Area under curve                 |
| Pie            | `'pie'`     | Pie chart (for Series only)      |
| Scatter        | `'scatter'` | Requires `x=` and `y=` arguments |


<br>

### Examples:
```bash
# Line plot (default)
df.plot()

# Bar plot
df.plot(kind='bar') # vertical bar chart
df.plot(kind='barh') # horizontal bar chart

# Histogram
df['age'].plot(kind='hist', bins=10)

# Pie
df['sex'].plot(kind='pie') 

# Box plot
df[['math', 'science']].plot(kind='box')

# Scatter plot (requires x and y)
df.plot(kind='scatter', x='height', y='weight')
```

<br>

#### Common Parameters:
| Parameter | Description                                              |
| --------- | -------------------------------------------------------- |
| `x`, `y`  | Columns to plot on x and y axes (for scatter/line plots) |
| `title`   | Set the title of the plot                                |
| `figsize` | Size of the plot, e.g., `(10, 6)`                        |
| `grid`    | Show grid lines (True/False)                             |
| `color`   | Set line/bar colors                                      |
| `legend`  | Show/hide legend (True/False)                            |

<br>

#### Customizing Example:
```bash
df.plot(kind='line', x='Year', y='Sales', title='Annual Sales', figsize=(8,5), grid=True)
```
<br>

### Remember:
- Add import matplotlib.pyplot as plt at the top.
- Use plt.show() to display plots if not using a notebook.
- unlike value_counts(), plot() can also be used on the full dataframe but it is used mostly on series in practice.



