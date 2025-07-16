#
# Chapter 6: Subplots 

<br>
<br>

### What are Subplots?
Subplots allow you to **display multiple plots in a single figure**. This is useful when you want to compare different plots side by side or show different aspects of your data together.

<br>
<br>

## Basic Syntax:
```bash
import matplotlib.pyplot as plt

fig, ax = plt.subplots(nrows=1, ncols=2)  # 1 row, 2 columns
```

<br>

#### Layout Options
| Parameter | Description                        |
| --------- | ---------------------------------- |
| `nrows`   | Number of rows                     |
| `ncols`   | Number of columns                  |
| `figsize` | Size of the figure (width, height) |
| `sharex`  | Share x-axis across subplots       |
| `sharey`  | Share y-axis across subplots       |

<br>
<br>

## Examples

<br>

### A. 1x2 Grid (Horizontal)
```bash
fig, ax = plt.subplots(1, 2, figsize=(10, 4))

ax[0].plot([1, 2, 3], [1, 4, 9])
ax[0].set_title('Plot 1')

ax[1].plot([1, 2, 3], [2, 5, 8])
ax[1].set_title('Plot 2')

plt.show()
```
###### Remember: In case of subplots, `plt.title()` will not work. Instead of that, `ax[i].set_title` must be used. <br> Similarly, `ax[i].set_xlabel()`, `ax[i].set_ylabel()`should be used
<img width="1458" height="484" alt="image" src="https://github.com/user-attachments/assets/dd909c0a-11c8-4b06-a29a-3f6075319904" />


<br>
<br>


### B. 2x2 Grid and Adding colors, Markers, Styles etc.
```bash
fig, ax = plt.subplots(2, 2, figsize=(8, 6))

ax[0, 0].bar([1, 2, 3], [3, 6, 9], color='red')
ax[0, 1].scatter([1, 2, 3], [8, 6, 7], color='green', marker='+')
ax[1, 0].plot([1, 2, 3], [2, 5, 7], color='orange', linestyle='--')
ax[1, 1].hist([1, 1, 2, 3, 3, 3, 4], color='yellow', edgecolor='red', alpha=0.5)

plt.show()
```
<img width="1457" height="657" alt="image" src="https://github.com/user-attachments/assets/f62118e8-c419-4ba2-a575-723cabb02dc5" />


<br>
<br>


### C. Sharing Axes Between Subplots
```bash
fig, ax = plt.subplots(2, 1, sharex=True, figsize=(6, 6))

ax[0].plot([1, 2, 3], [1, 4, 9])
ax[1].plot([1, 2, 3], [2, 5, 7])

ax[0].set_title("Shared X-axis")

plt.show()
```
<img width="1456" height="681" alt="image" src="https://github.com/user-attachments/assets/adbfe38c-1d29-48a7-b6a3-51059af55307" />


