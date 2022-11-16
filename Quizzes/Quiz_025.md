# Quiz 25
## Coding
### Solution
```.py
import matplotlib.pyplot as plt

x_list = []
y_list = []

for i in range(-100, 100, 1):
    x_list.append(i/10)
    y_list.append(abs(i/10))

plt.plot(x_list, y_list)
plt.show()
```

### Tests
![](https://github.com/thumulakaru/Unit-2--repo/blob/main/Quizzes/Quiz_025_Tests.png)
**Fig.1:** Tests for the solution

## Part A
FFA5 = (15x16x16x16)+(15x16x16)+(15x16)+(5x1)
     = 65445
