#
#

<br>
<br>

###  1. Save DataFrame to a CSV file
```bash
df.to_csv('data.csv')
```
<br>

### 2. Save only selected columns
```bash
df.to_csv('data.csv', columns=['Name', 'Age'], index=False)  # index=False is used to exclude index column
```

<br>
<br>

## Most Used Pandas Export Options (Apart From CSV):

| Format        | Method                     | Description                                                 | File Extension  |
| ------------- | -------------------------- | ----------------------------------------------------------- | --------------- |
| **CSV**       | `to_csv()`                 | Exports to Comma-Separated Values file                      | `.csv`          |
| **Excel**     | `to_excel()`               | Exports to Excel format (XLSX, XLS)                         | `.xlsx`, `.xls` |
| **JSON**      | `to_json()`                | Exports to JSON format                                      | `.json`         |
| **HTML**      | `to_html()`                | Exports to an HTML table                                    | `.html`         |
| **SQL**       | `to_sql()`                 | Writes to a SQL database table                              | DB table        |
| **Pickle**    | `to_pickle()`              | Saves object in Python binary format                        | `.pkl`          |

<br>

### Notes:
- Some formats (like Excel, SQL, etc.) require optional dependencies like `openpyxl`, `sqlalchemy`, etc.
- Use index=False if you don’t want row indexes in output files (especially in CSV, Excel).
- Use `read_*()` equivalents to read them back (e.g., `read_csv()`, `read_json()`).


