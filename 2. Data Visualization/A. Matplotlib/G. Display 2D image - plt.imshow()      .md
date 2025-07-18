#
# Chapter 7: Display 2D image

<br>
<br>

`plt.imshow()` is a function in `matplotlib.pyplot` used to display image-like data as a 2D image.<br>
It maps values of a matrix (NumPy array) to pixel intensities and renders it as an image using color mapping.

<br>

## Types of Arrays You Can Use
| Type            | Shape                | Description                            |
| --------------- | -------------------- | -------------------------------------- |
| Grayscale Image | 2D array (H × W)     | Each value = intensity                 |
| RGB Image       | 3D array (H × W × 3) | 3 channels: Red, Green, Blue           |
| RGBA Image      | 3D array (H × W × 4) | Red, Green, Blue, Alpha (transparency) |


<br>

## Examples

<br>

### 1. Grayscale Example
```python
import numpy as np
import matplotlib.pyplot as plt

data = np.random.rand(10, 10) * 100  # 2D grayscale matrix
plt.imshow(data, cmap='gray')
plt.colorbar()
plt.title('Grayscale Image')
plt.show()
```
<img width="1456" height="537" alt="image" src="https://github.com/user-attachments/assets/27b48bd0-aa6e-485a-a65e-a33eb4bf1a16" />

<br>
<br>

### RGB Image Example
```python
import matplotlib.pyplot as plt
import matplotlib.image as mpimg

img = mpimg.imread('image.jpg')

plt.imshow(img)

plt.axis('off')  # Hides axes
plt.title('RGB Image')

plt.show()
```
<img width="1464" height="504" alt="image" src="https://github.com/user-attachments/assets/20781d26-f813-49c4-b757-f74f722c50a2" />


<br>
<br>


### 3. Color Mapping Example
```python
data = np.random.rand(10, 10)

plt.imshow(data, cmap='viridis')
plt.colorbar()

plt.title('Heatmap with Viridis')

plt.show()
```
<img width="1464" height="559" alt="image" src="https://github.com/user-attachments/assets/21e111be-9d83-4f57-910d-98670319c1b3" />


<br>
<br>

### Saving the Output
```python
plt.imsave('output.png', data, cmap='hot')
```
**When to Use Which?**
| Situation                                   | Use                                                    |
| ------------------------------------------- | ------------------------------------------------------ |
| You want a simple grayscale output          | `plt.imsave('img.png', data)`                          |
| You want visual enhancement (like heatmaps) | `plt.imsave('img.png', data, cmap='hot')`              |
| You already have RGB data                   | Use `plt.imsave('img.png', rgb_data)` **without cmap** |


<br>
<br>

### Display vs Load
| Task                 | Function         |
| -------------------- | ---------------- |
| Load image           | `mpimg.imread()`<br> used for showing image file |
| Display NumPy matrix | `plt.imshow()`   |
| Showing the image    | `plt.show()`     |
| Save visualized data | `plt.imsave()`   |




