# Quiz 27
## Programming
### Solution
```.py
import matplotlib.pyplot as plt
import numpy as np

sensorA = [16, 24, 24, 9, 23, 26, 26, 23, 25, 14]
sensorB = [2, 19, 25, 10, 11, 24, 17, 7, 24, 17]
sensorC = [15, 11, 24, 21, 6, 2, 18, 27, 1, 16]

samples = []

for i in range(len(sensorA)):
    samples.append(i)

fig = plt.figure(figsize=(8, 4))

plt.subplot(1, 2, 1)
plt.plot(samples, sensorA, color="#caf0f8")
plt.plot(samples, sensorB, color="#415a77")
plt.plot(samples, sensorC, color="#9b2226")

mean = []
standard_dev = []
max_v = []
min_v = []

for i in range(len(sensorA)):
    data = [sensorA[i], sensorB[i], sensorC[i]]
    mean.append(np.mean(data))
    standard_dev.append(np.std(data))
    max_v.append(max(data))
    min_v.append(min(data))

plt.subplot(1, 2, 2)
plt.fill_between(samples, max_v, min_v, alpha=.5, linewidth=0, color="#90e0ef")
plt.errorbar(samples, mean, standard_dev, fmt='o')
plt.show()
```


### Tests
![](https://github.com/thumulakaru/Unit-2--repo/blob/main/Quizzes/Quiz_027_Tests.png)

**Fig.1:** Tests for the solution

## Colour code
### Answer
![](https://github.com/thumulakaru/Unit-2--repo/blob/main/Quizzes/Quiz_027_Colour_Question.jpg)

**Fig.2:** Answer for the colour code question
