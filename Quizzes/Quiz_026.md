# Quiz 26
## Programming
### Solution
```.py
import matplotlib.pyplot as plt
import numpy as np


h = [57.0, 56.0, 57.0, 56.0, 55.0, 55.0, 54.0, 54.0, 54.0, 53.0,
     53.0, 54.0, 53.0, 53.0, 52.0, 52.0, 51.0, 51.0, 51.0, 50.0,
     50.0, 49.0, 50.0, 49.0, 49.0, 48.0, 49.0, 49.0, 48.0, 48.0, 48.0, 49.0]
samples = []

for i in range(len(h)):
    samples.append(i)

plt.plot(samples, h, linestyle="none", marker="v")
m, b = np.polyfit(samples, h, 1)

x_values = []
y_values = []

for i in [1, 30]:
    x_values.append(i)
    H_model = m * i + b
    y_values.append(H_model)
plt.plot(x_values, y_values)
plt.xlabel("Sample")
plt.ylabel("Relative humidity")

plt.show()
```


### Tests
![](https://github.com/thumulakaru/Unit-2--repo/blob/main/Quizzes/Quiz_026_Tests.png)

**Fig.1:** Tests for the solution

## Colour code question
### Answer
![](https://github.com/thumulakaru/Unit-2--repo/blob/main/Quizzes/Quiz_026_Colour_Question.jpg)

**Fig.2:** Answer for the colour code question
