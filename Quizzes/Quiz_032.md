# Quiz 32
## Part A
### Solution
```.py
import requests
import matplotlib.pyplot as plt

req = requests.get("http://192.168.6.142/readings")
data = req.json()
readings = data["readings"][0]
T_9 = []
T_10 = []
samples = []
T_9_smooth = []
T_10_smooth = []
samples_smooth = []
y = []
diff = []
num_samples_per_hour = 12

for r in readings:
    if r["sensor_id"] == 9:
        T_9.append(r["value"])
    if r["sensor_id"] == 10:
        T_10.append(r["value"])

for i in range(0, len(T_10), num_samples_per_hour):
    t_hour_9 = T_9[i:i+num_samples_per_hour]
    T_9_smooth.append(sum(t_hour_9)/len(t_hour_9))
    t_hour_10 = T_10[i:i+num_samples_per_hour]
    T_10_smooth.append(sum(t_hour_10)/len(t_hour_10))
    samples_smooth.append(i)

for t in range(len(T_9_smooth)):
    print(t)
    y.append(T_9_smooth[t] - T_10_smooth[t])
    diff.append(t)

plt.subplot(3, 1, 1)
plt.plot(samples_smooth, T_9_smooth, color="red")
plt.title("Sensor 9")

plt.subplot(3, 1, 2)
plt.plot(samples_smooth, T_10_smooth, color="green")
plt.title("Sensor 10")

plt.subplot(3, 1, 3)
plt.plot(diff, y)
plt.title("Differences", color = "blue")

plt.show()
```
### Tests
![]()

## Part B
### Answer
The 3 main operators used in boolean logic are 

**1. AND**

**2. OR**

**3. NOT**.
