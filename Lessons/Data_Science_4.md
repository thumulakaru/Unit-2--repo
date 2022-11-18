# Data science
This lesson was directed to teach how to make two graphs and also more importantly how to get and insert error lines.
## Code
```.py
import matplotlib.pyplot as plt
import numpy as np

plt.style.use("dark_background")

h = [57.0, 56.0, 57.0, 56.0, 55.0, 55.0, 54.0, 54.0, 54.0, 53.0, 53.0, 54.0, 53.0, 53.0, 52.0, 52.0, 51.0, 51.0, 51.0]
low = [53.0, 54.0, 54.0, 52.0, 54.0, 51.0, 53.0, 53.0, 50.0, 51.0, 52.0, 53.0, 49.0, 50.0, 50.0, 49.0, 50.0, 47.0, 50.0]
high = [58.0, 60.0, 61.0, 57.0, 56.0, 58.0, 58.0, 57.0, 56.0, 55.0, 54.0, 57.0, 54.0, 56.0, 53.0, 56.0, 53.0, 55.0,
        52.0]
samples = []

# Step 1 visualise data
for i in range(len(h)):
    samples.append(i)

# step 2: Splitting the view
fig = plt.figure(figsize=(8, 4))
plt.subplot(1, 2, 1)
plt.plot(samples, h, color="#caf0f8")
plt.plot(samples, low, color="#415a77")
plt.plot(samples, high, color="#9b2226")

# Step 3: Analyse the data
mean = []
standard_dev = []
for i in range(len(h)):
    data = [h[i], low[i], high[i]]
    mean.append(np.mean(data))
    standard_dev.append(np.std(data))

plt.subplot(1, 2, 2)
plt.fill_between(samples, high, low, alpha=.5, linewidth=0, color="#90e0ef")
plt.errorbar(samples, mean, standard_dev, fmt='o')

plt.show()
```

## Date
Thursday, 17th November 2022
