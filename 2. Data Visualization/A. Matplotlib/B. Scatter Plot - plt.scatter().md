#
# Chapter 2: Scatter Plot - Plotting Numerical vs Numerical

<br>
<br>

A scatter plot displays points based on two variables. It helps to visualize **correlation**, **distribution**, and **clusters** in data.

<br>

## Basic Scatter Plot:
```bash
import matplotlib.pyplot as plt

x = [1, 2, 3, 4, 5]
y = [5, 4, 4, 2, 3]

plt.scatter(x, y)

plt.show()
```
<img width="1455" height="516" alt="image" src="https://github.com/user-attachments/assets/05daddb8-df36-472f-a900-3e652d59ad6a" />


<br>
<br>

## Adding Title, Axis Labels, Grid:
```bash
import matplotlib.pyplot as plt

x = [1, 2, 3, 4, 5]
y = [5, 4, 4, 2, 3]

plt.scatter(x, y)

plt.title("Simple Scatter Plot")
plt.xlabel("X Axis")
plt.ylabel("Y Axis")

plt.grid(True)

plt.show()
```
<img width="1458" height="572" alt="image" src="https://github.com/user-attachments/assets/aece3892-0e0d-4f78-8be4-c99ecc3dfecd" />

<br>
<br>

## Changing Size, Colour, Marker:
```bash
import matplotlib.pyplot as plt

x = [1, 2, 3, 4, 5]
y = [5, 7, 4, 6, 5]

plt.scatter(x, y, s=200, c='Green', marker='+')

plt.show()
```
<img width="1457" height="504" alt="image" src="https://github.com/user-attachments/assets/11715db5-fe0a-4d55-b9c8-c9ef321d1f73" />

<br>
<br>

## Customizing points different colours and sizes:
```bash
import matplotlib.pyplot as plt

x = [1, 2, 3, 4, 5]
y = [5, 7, 4, 6, 5]
sizes = [30, 50, 80, 200, 500]
colors = ['red', 'green', 'blue', 'orange', 'purple']

plt.scatter(x, y, s=sizes, c=colors, alpha=0.6, marker='o')
plt.show()
```
<img width="1462" height="514" alt="image" src="https://github.com/user-attachments/assets/e399898a-9531-48a6-82c7-5df7ab6d4119" />


