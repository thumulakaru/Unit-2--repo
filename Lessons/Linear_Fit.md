# Linear fit
## Description
This lesson covered how to make a straight line with variables that are not constant

## Code
```.py
import matplotlib.pyplot as plt
import numpy as np

x = [1, 2, 3, 1.5, 4, 2.5, 6, 4, 3, 5.5, 5, 2]
y = [3, 4, 8, 4.5, 10, 5, 15, 9, 5, 16, 13, 3]


m, b = np.polyfit(x, y, 1)
print(f"Linear equation is y ={m:.2f}x + {b:.2f}")

plt.scatter(x, y, color="b")
plt.xlabel("Displacement")
plt.ylabel("Time")
plt.title("Scatter plot of the data")

x_model = []
y_model = []
for i in [1, 6]:
    x_model.append(i)
    temp = m * i + b
    y_model.append(temp)

plt.plot(x_model, y_model)
plt.show()
```
## Date
Friday, 11th November 2022
