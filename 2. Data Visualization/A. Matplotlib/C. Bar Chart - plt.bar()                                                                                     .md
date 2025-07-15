#
# Chapter 3: Bar Chart - Plotting Categorical variable vs Aggregate (Numerical) Variable

<br>
<br>

A bar chart represents data with rectangular bars. Each bar’s **height (or width)** shows the value of a variable for a particular category.

<br>
<br>

## Basic Bar Chart:
```bash
import matplotlib.pyplot as plt

categories = ['A', 'B', 'C', 'D']
values = [10, 24, 36, 18]

plt.bar(categories, values)

plt.show()
```
<img width="1453" height="521" alt="image" src="https://github.com/user-attachments/assets/b34dd335-92e3-4ad1-a5bb-86c90de39f29" />

<br>
<br>

## Adding Title, Axis Labels:
```bash
import matplotlib.pyplot as plt

categories = ['A', 'B', 'C', 'D']
values = [10, 24, 36, 18]

plt.bar(categories, values)

plt.title("Basic Bar Chart")
plt.xlabel("Category")
plt.ylabel("Value")

plt.show()
```
<img width="1457" height="560" alt="image" src="https://github.com/user-attachments/assets/6335ebe8-605b-4f64-b570-6e3cbf602b21" />

<br>
<br>

## Changing Colour, Edge-Colour, Width of the Bar:
```bash
import matplotlib.pyplot as plt

categories = ['Apple', 'Banana', 'Mango', 'Orange']
sales = [40, 70, 30, 85]

plt.bar(categories, sales, color='orange', edgecolor='black', width=0.6)

plt.title("Fruit Sales")
plt.xlabel("Fruit")
plt.ylabel("Units Sold")

plt.grid(axis='y')   # you can use like this to show one axis grid 

plt.show()
```
<img width="1459" height="568" alt="image" src="https://github.com/user-attachments/assets/7a0713fd-fb3b-4dde-b0bd-8706775d9663" />

<br>
<br>

## Horizontal Bar Chart (`plt.barh()`):
```bash
plt.barh(categories, sales, color='green')

plt.title("Horizontal Bar Chart")
plt.xlabel("Units Sold")
plt.ylabel("Fruit")

plt.show()
```
###### Everything you learned in `plt.bar()` is equally applicable to `plt.barh()`
<img width="1460" height="572" alt="image" src="https://github.com/user-attachments/assets/0c7d6ccc-8278-4991-8fae-ca55b940f644" />

## 

