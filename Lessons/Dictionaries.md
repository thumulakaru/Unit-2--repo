# Dictionaries
This lesson was conducted to teach how dictionaries work and how to use them in a practical situation
## Code
```.py
import random
import matplotlib.pyplot as plt


# Dictionaries
sensor = {"name": "sensor_x1",
          "type": "Temperature",
          "readings": []}

for i in range(100):
    a = random.randint(0, 100)
    sensor["readings"].append(a)

sensor["samples"] = []
for i in range(100):
    sensor["samples"].append(i)

plt.plot(sensor["samples"], sensor["readings"])
plt.show()
```

## Date
Friday, 18th November 2022
