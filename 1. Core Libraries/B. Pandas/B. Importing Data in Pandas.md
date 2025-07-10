#
# Chapter 2: Importing Data in Pandas

<br>
<br>

We can import data from excel, csv files etc very easily using pandas.
<br>

#### Example
```bash
import pandas as pd
df = pd.read_csv("filename.csv")
```

<br>
<br>

#### Basic Functions for Importing Data
| Function           | File Type          | Example                      |
| ------------------ | ------------------ | ---------------------------- |
| `pd.read_csv()`    | CSV                | `pd.read_csv('data.csv')`    |
| `pd.read_excel()`  | Excel (.xls/.xlsx) | `pd.read_excel('data.xlsx')` |
| `pd.read_json()`   | JSON               | `pd.read_json('data.json')`  |
| `pd.read_html()`   | HTML tables        | `pd.read_html('page.html')`  |
| `pd.read_sql()`    | SQL queries        | `pd.read_sql(query, conn)`   |
| `pd.read_table()`  | Delimited text     | `pd.read_table('data.txt')`  |
| `pd.read_pickle()` | Pickle format      | `pd.read_pickle('data.pkl')` |

<br>

#### Reading from URLs or Web
```bash
pd.read_csv('https://example.com/data.csv')
```
No need to download manually — Pandas can read directly from web sources.


