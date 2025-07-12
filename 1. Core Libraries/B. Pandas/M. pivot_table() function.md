#
# Chapter 13: pivot_table() function

<br>
<br>

## Basic Syntax:
```bash
df.pivot_table(index=__, columns=__, values=__, aggfunc='__')
```
<br>

## Key Parameters:

| Parameter      | Description                                         |
| -------------- | --------------------------------------------------- |
| `index`        | Column(s) to group by rows (becomes row index)      |
| `columns`      | Column(s) to turn into **new column headers**       |
| `values`       | Column to aggregate/summarize                       |
| `aggfunc`      | Aggregation function (`sum`, `mean`, `count`, etc.) |

<br>

## Example:
### Original Data:
| Region | Product | Sales |
| ------ | ------- | ----- |
| East   | Apple   | 100   |
| East   | Banana  | 150   |
| West   | Apple   | 200   |
| West   | Banana  | 250   |
| East   | Apple   | 300   |

<br>

### Code for Pivot Table:
```bash
df.pivot_table(index='Region', columns='Product', values='Sales', aggfunc='sum')
```

<br>

### Output: 
| Product | Apple | Banana |
| ------- | ----- | ------ |
| East    | 400   | 150    |
| West    | 200   | 250    |


<br>
<br>

## Supported Aggregation Functions:
| Function          | Meaning                |
| ----------------- | ---------------------- |
| `'sum'`           | Total                  |
| `'mean'`          | Average                |
| `'count'`         | Count of rows          |
| `'min'` / `'max'` | Minimum / Maximum      |
| `'median'`        | Middle value           |
| `'nunique'`       | Count of unique values |

<br>

You can also pass a **custom function:**

```bash
aggfunc=lambda x: x.max() - x.min()
```

<br>
<br>

## Multiple Index Example

<br>

### Code for Pivot Table:
```bash
df.pivot_table(index=['Region', 'Month'], columns='Product', values='Sales', aggfunc='sum')
```
<br>

### Output:
| Region | Month | Apple | Banana |
| ------ | ----- | ----- | ------ |
| East   | Jan   | 100   | 200    |
| East   | Feb   | 300   | NaN    |
| West   | Feb   | 150   | 250    |
| West   | Jan   | NaN   | 100    |

- `index=\['Region', 'Month']`: Grouped by both Region and Month
- `columns='Product'`: Spread Apple and Banana as columns

<br>
<br>

## Multiple values and aggfunc Example

<br>

### Code for Pivot Table:
```bash
df.pivot_table(
    index='Region',
    columns='Product',
    values=['Sales', 'Quantity'],
    aggfunc=['sum', 'mean']
)
```
<br>

### Output:
|        |      | Apple | Banana |       |      |
| ------ | ---- | ----- | ------ | ----- | ---- |
|        |      | **Sales** | **Qty**    | **Sales** | **Qty**  |
| **Region** |      |       |        |       |      |
| **East**   | mean | 200.0 | 20.0   | 200.0 | 20.0 |
|        | sum  | 400   | 40     | 200   | 20   |
| **West**   | mean | 150.0 | 15.0   | 250.0 | 25.0 |
|        | sum  | 150   | 15     | 250   | 25   |




