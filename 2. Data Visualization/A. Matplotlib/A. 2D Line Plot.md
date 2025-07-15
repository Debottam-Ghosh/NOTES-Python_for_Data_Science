#
# Chapter 1: 2D Line Plot in Matplotlib

<br>
<br>

## What is a Line Plot?
A 2D Line Plot in Matplotlib is used to **visualize data points connected by straight lines**. It is often used to show trends, time series, or relationships between variables.

<br>

## Basic Line Plot (`plt.plot(x,y)`) (without any style):
```bash
import matplotlib.pyplot as plt

x = [1, 2, 3, 4]
y = [2, 5, 7, 10]

plt.plot(x, y)
plt.show()
```
<img width="1463" height="518" alt="image" src="https://github.com/user-attachments/assets/acc150fd-9034-4d63-a21c-abb6665d46bd" />


<br>
<br>

## Title (`.title()`), Axis Labels (`.xlabel()`, `.ylabel()`):
```bash
x = [1, 2, 3, 4]
y = [2, 5, 7, 10]

plt.plot(x, y)

plt.title("Sample 2D Line Plot")
plt.xlabel("X-axis Label")
plt.ylabel("Y-axis Label")

plt.show()
```
<img width="1461" height="557" alt="image" src="https://github.com/user-attachments/assets/e0a20dff-9f1c-400b-92fe-7a00e4131b3a" />

<br>
<br>

## Multiple Line Plots and Legends:
```bash
x = [1, 2, 3, 4]
y1 = [1, 4, 9, 16]
y2 = [2, 3, 4, 5]

plt.plot(x, y1, label="Squared")
plt.plot(x, y2, label="Linear")

plt.title("Squared vs Linear Function")

plt.legend() 

plt.show()
```
**Remember:** If you don't give labels (`.label=`) on the lines ("Squared" or "Linear"), plt.legend will throw error.
<img width="1456" height="547" alt="image" src="https://github.com/user-attachments/assets/c02f0add-10ed-49ac-8ecb-29a3ddf0d8e3" />


