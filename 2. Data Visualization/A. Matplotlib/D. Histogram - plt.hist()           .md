#
# Chapter 4: Histogram - Plotting intervals vs numerical data

<br>
<br>

A **histogram** is a graphical representation that organizes a group of **continuous numerical data** into **bins (intervals)**. It shows the **frequency distribution** — i.e., how often each range of values occurs.

<br>
<br>

## Basic Histogram
```bash
import matplotlib.pyplot as plt

data = [10, 20, 20, 30, 30, 30, 40, 50, 50, 60]

plt.hist(data, bins=10)

plt.show()
```
<img width="1457" height="515" alt="image" src="https://github.com/user-attachments/assets/7d9a64b1-fa72-4763-8402-efa3628682aa" />

<br>
<br>

## Example with Customization:
```bash
import matplotlib.pyplot as plt
import numpy as np

data = np.random.normal(50, 15, 200)  # Mean=50, Std=15, n=200

plt.hist(data, bins=10, color='orange', edgecolor='black', alpha=0.75)
plt.title("Distribution of Scores")
plt.xlabel("Score")
plt.ylabel("Frequency")

plt.grid(True)

plt.show()
```
<img width="1457" height="568" alt="image" src="https://github.com/user-attachments/assets/253e5df1-e242-4e73-a4b9-54d98b469e87" />


<br>
<br>

## Multiple Histograms:
```bash
data1 = np.random.normal(60, 10, 200)
data2 = np.random.normal(40, 15, 200)

plt.hist([data1, data2], bins=15, label=['Group A', 'Group B'], alpha=0.6)
plt.legend()
plt.title("Comparison Histogram")

plt.show()
```
<img width="1448" height="537" alt="image" src="https://github.com/user-attachments/assets/183e75f8-1d21-4bae-bb11-48b455a9b40d" />


