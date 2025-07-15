#
# Chapter 3: Bar Chart 
## - Plotting Categorical variable vs Numerical Variable

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

## Changing Colour, Edge-Colour, Width and Transparency (`alpha=`) of the Bar:
```bash
import matplotlib.pyplot as plt

categories = ['Apple', 'Banana', 'Mango', 'Orange']
sales = [40, 70, 30, 85]

plt.bar(categories, sales, color='orange', edgecolor='black', width=0.6, alpha=0.8)

plt.title("Fruit Sales")
plt.xlabel("Fruit")
plt.ylabel("Units Sold")

plt.grid(axis='y')   # you can use like this to show one axis grid 

plt.show()
```
<img width="1459" height="568" alt="image" src="https://github.com/user-attachments/assets/7a0713fd-fb3b-4dde-b0bd-8706775d9663" />

<br>
<br>

## plt.xticks()
<br>

### 1. Set custom tick positions and labels:
```bash
plt.xticks([0, 1, 2], ['Low', 'Medium', 'High'])
```
###### Note: [0,1,2] are indices. So you don't need to write the old labels
<img width="1452" height="564" alt="image" src="https://github.com/user-attachments/assets/d259561b-efab-4b7d-8b83-5f4055144331" />

<br>

### 2. Set vertical or angled labels:
```bash
plt.xticks(rotation=50)
```
###### - Here `50` is the angle. Clerly `rotation=90` will make the labels vertical
###### - Use this when there are many categories on x axis or their names are long to avoid overlapping
###### - You can use `yticks` in the same way
<img width="1458" height="606" alt="image" src="https://github.com/user-attachments/assets/9b14f281-247a-4ce8-93ae-72bdf567e951" />

<br>
<br>

## Stacked Column Chart:
```bash
import pandas as pd
import matplotlib.pyplot as plt

df = pd.DataFrame(data=
                  {'Fruit':['Apple','Mango','Banana'], 
                   '2021':[50,75,60], 
                   '2022':[80,70,55], 
                   '2023':[40,80,60]})

x = df['Fruit']
y1 = df['2021']
y2 = df['2022']
y3 = df['2023']

# Plotting stacked bar chart
plt.bar(x, y1, label='2021')
plt.bar(x, y2, bottom=y1, label='2022')
plt.bar(x, y3, bottom=y1 + y2, label='2023')

plt.xlabel("Fruit")
plt.ylabel("Sales")
plt.title("Fruit Sales Over 3 Years")

plt.legend()
plt.show()
```
###### You can't use a list as `Fruit` directly, you need to convert that into np.array()
<img width="1459" height="573" alt="image" src="https://github.com/user-attachments/assets/bb90e4a1-d130-49c3-b238-bfb8e6942432" />


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



