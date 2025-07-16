#
# Chapter 5: Pie Chart - Categorical vs Numerical 

<br>
<br>

A **pie chart** displays data in a circular graph, divided into slices to illustrate **proportions**. Matplotlib offers this via `plt.pie()`.

<br>

## Basic Pie Chart (`plt.pie(data= , labels= `)
```bash
import matplotlib.pyplot as plt

fruit_name = ['Apples', 'Bananas', 'Cherries', 'Dates']
sizes = [20, 30, 25, 25]

plt.pie(sizes, labels=fruit_name)
plt.show()
```
<img width="1462" height="483" alt="image" src="https://github.com/user-attachments/assets/d6eb127c-006e-49e8-91b7-f57b5986473b" />

<br>
<br>

## Adding values in `%` for each slice (`autopct= `)
```bash
import matplotlib.pyplot as plt

fruit_name = ['Apples', 'Bananas', 'Cherries', 'Dates']
sizes = [20, 30, 25, 25]

plt.pie(sizes, labels=fruit_name, autopct="%.1f%%")

plt.show()
```
<img width="1458" height="487" alt="image" src="https://github.com/user-attachments/assets/46b16c25-3523-417d-a7dc-c0904854576b" />

<br>
<br>

## Customizing Colours and Offsetting a Particular Slice (`explode= `)
```bash
labels = ['Python', 'C++', 'Ruby', 'Java']
sizes = [215, 130, 245, 210]
colors = ['gold', 'yellowgreen', 'lightcoral', 'lightskyblue']
explode = (0.1, 0, 0, 0)  # Explode 1st slice

plt.pie(sizes,
        explode=explode,
        labels=labels,
        colors=colors,
        autopct='%1.1f%%')

plt.title('Programming Language Popularity')
plt.axis('equal')  # Equal aspect ratio ensures the pie is a circle.

plt.show()
```

<img width="1459" height="528" alt="image" src="https://github.com/user-attachments/assets/095241d1-4bee-4cbb-ba92-633d53dab942" />

<br>
<br>

## Donut Chart
```bash
plt.pie(sizes, labels=labels, autopct='%1.1f%%')

# Draw circle
centre_circle = plt.Circle((0, 0), 0.50, fc='white')
fig = plt.gcf()
fig.gca().add_artist(centre_circle)

plt.axis('equal')
plt.title("Donut Chart")

plt.show()
```
<img width="1459" height="518" alt="image" src="https://github.com/user-attachments/assets/5358cf9c-98a8-4c6f-bc6a-9e2445e8c075" />


