# Quiz 30
## Part A
### Solution
```.py
import matplotlib.pyplot as plt
import numpy as np

h = [57.0, 56.0, 57.0, 56.0, 55.0, 55.0, 54.0, 54.0, 54.0, 53.0, 53.0, 54.0, 53.0, 53.0, 52.0, 52.0, 51.0, 51.0, 51.0]
low = [53.0, 54.0, 54.0, 52.0, 54.0, 51.0, 53.0, 53.0, 50.0, 51.0, 52.0, 53.0, 49.0, 50.0, 50.0, 49.0, 50.0, 47.0, 50.0]
high = [58.0, 60.0, 61.0, 57.0, 56.0, 58.0, 58.0, 57.0, 56.0, 55.0, 54.0, 57.0, 54.0, 56.0, 53.0, 56.0, 53.0, 55.0, 52.0]

window = 4
overlap = 2
samples = []
samples_h = []

# Calculating the high mean and low for values given in the window with the overlap of 50%
for i in range(len(h)):
    samples.append(i)

samples_low = []
samples_high = []
samples_smooth = []

# Smoothing the data
for i in range(0, len(h), window//2):
    samples_smooth.append(i)
    values = h[i:i+window]
    samples_h.append(np.mean(values))


# Plotting the graph
fig = plt.figure(figsize=(4, 8))
plt.subplot(3, 1, 1)
plt.plot(samples, h)
plt.subplot(3, 1, 2)
plt.plot(samples_smooth, samples_h)

plt.show()
```
### Tests
![](https://github.com/thumulakaru/Unit-2--repo/blob/main/Quizzes/Quiz_030_Tests.png)

**Fig.1** The tests for the solution of part A

## Part B

### Solution
The interent was invented on 1983 January 1st.
“A Brief History of the Internet.” A Brief of History of the Interent,
https://www.usg.edu/galileo/skills/unit07/internet07_02.phtml#:~:text=January%201%2C%201983%20is%20considered,Protocol%20(TCP%2FIP). 

