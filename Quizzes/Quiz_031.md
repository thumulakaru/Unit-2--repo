# Quiz 31
## Part A
### Solution
```.py
import requests
import matplotlib.pyplot as plt
import numpy as np
import json

url = "http://192.168.6.142/readings"
data = requests.get(url)
jdata = data.json()
sensor_data = (jdata["readings"][0])

# Get temperature
temperature = []
for element in sensor_data:
    if element["sensor_id"] == 1:
        temperature.append(element["value"])
temp_afternoon_mon = temperature[610:800]
x_afternoon_mon = []
for i in range(len(temp_afternoon_mon)):
    x_afternoon_mon.append(i)

plt.scatter(x_afternoon_mon, temp_afternoon_mon)
# linear model
m, b = np.polyfit(x_afternoon_mon, temp_afternoon_mon, 1)
x_line = [0, len(temp_afternoon_mon)]
y_line = []
for i in x_line:
    y_line.append(m*i+b)
plt.plot(x_line, y_line, "black")
plt.text(70, 20, f"Linear Equation: y = {m:.4f}x + {b:.4f}", fontsize=6)
# Quadratic model
a1, a2, a3 = np.polyfit(x_afternoon_mon, temp_afternoon_mon, 2)
y_model_quad = []
for i in x_afternoon_mon:
    y_model_quad.append(a1 * (i ** 2) + a2 * i + a3)

plt.plot(x_afternoon_mon, y_model_quad, "orange")
plt.text(30, 25, f"Quadratic Equation: y = {a1:.3f}x^2 + {a2:.2f}x + {a3:.2f}", fontsize=6)
plt.show()
```
### Tests
![](https://github.com/thumulakaru/Unit-2--repo/blob/main/Quizzes/Quiz_031_Tests.png)

**Fig.1** Tests for quiz 30 programming question
