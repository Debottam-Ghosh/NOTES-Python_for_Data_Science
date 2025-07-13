#
# Chapter 14: corr() function

<br>
<br>

The `corr()` function computes pairwise correlation of the numerical columns in a DataFrame, excluding missing values (NaNs).

## Syntax:
```bash
DataFrame.corr(method=__)
```

## Types of Correlation Methods:
| Method     | Measures Relationship | Type           | When to Use                    |
| ---------- | --------------------- | -------------- | ------------------------------ |
| `pearson` (Default) | Linear                | Parametric     | Data is normally distributed   |
| `kendall`  | Monotonic             | Non-parametric | Ordinal or small datasets      |
| `spearman` | Monotonic             | Non-parametric | When ranks are more meaningful |

<br>

## Example:
**Data:**
| Index | Math | Science | English |
| ----- | ---- | ------- | ------- |
| 0     | 90   | 88      | 70      |
| 1     | 80   | 85      | 60      |
| 2     | 70   | 70      | 80      |
| 3     | 60   | 65      | 75      |

<br>

**Code:**
```bash
print(df.corr())
```

<br>

**Output:**
|         | Math  | Science | English |
| ------- | ----- | ------- | ------- |
| Math    | 1.00  | 0.98    | -0.11   |
| Science | 0.98  | 1.00    | 0.07    |
| English | -0.11 | 0.07    | 1.00    |

<br>

## Interpretation:
- Values close to 1: Strong positive correlation
- Values close to -1: Strong negative correlation
- Values around 0: No correlation
<br>

## Limitations:
- Works only with numeric columns
- Sensitive to outliers (especially Pearson)
<br>

## Use Cases:
- EDA (Exploratory Data Analysis)
- Detecting multicollinearity in features
- Feature selection for machine learning
- Financial or time-series correlation analysis

