#
# Chapter 1: Line Chart - Plotting Categorical vs Numerical 

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

## Multiple Line Plots and Legends(`plt.legend()`):
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
<br>

<img width="1456" height="547" alt="image" src="https://github.com/user-attachments/assets/c02f0add-10ed-49ac-8ecb-29a3ddf0d8e3" />


<br>
<br>

## Customizing with Colour (`color=`), Line Style (`linestyle=`), Line Width (`linewidth=`), Marker (`marker=`)
```bash
x = [1, 2, 3, 4]
y = [1, 4, 9, 16]

plt.plot(x, y, color='green', linestyle='--', linewidth=2, marker='o', label='Data Line')

plt.show()
```
<img width="1461" height="524" alt="image" src="https://github.com/user-attachments/assets/77d237e8-9a5f-4198-adcb-6b956e360e5c" />

<br>
<br>

## Adding Grid (`plt.grid(True)`)
```bash
x = [1, 2, 3, 4]
y = [1, 4, 9, 16]

plt.plot(x, y)
plt.grid(True)

plt.show()
```
<img width="1452" height="511" alt="image" src="https://github.com/user-attachments/assets/13dc2424-13b0-455b-87a0-937103ede4cf" />

<br>
<br>

## Controling Figure Size (`plt.figure(figsize=(w, h))`):
```
x = [1, 2, 3, 4, 5]
y = [1, 4, 9, 16, 25]

# Create a figure with custom size (width=8 inches, height=5 inches)
plt.figure(figsize=(8, 5))

plt.plot(x, y)

plt.show()
```
###### Use `plt.figure(figsize=(w, h))`to control plot size and use it **before** `plt.plot()`. Otherwise it won't work.

<br>
<br>

## Saving the Figure (`plt.savefig('filename.png')`):
```bash
x = [1, 2, 3, 4, 5]
y = [1, 4, 9, 16, 25]

plt.plot(x, y)

# Save the figure to a file
plt.savefig("line_plot.png")  # Saves in the current directory

plt.show()
```
###### Use `plt.savefig('filename.png')` to save the plot and use it **before** `plt.show()`
