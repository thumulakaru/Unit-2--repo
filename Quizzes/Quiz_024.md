# Quiz 24
## Part A
### Solution
```.py
from matplotlib import pyplot as plt


change = 0.2
x_out = []
y_out = []
for i in range(-100, 102, 2):
    x = i/10
    x_out.append(x)
    y = 2*((x+5)**2)
    y_out.append(y)
plt.plot(x_out, y_out)
plt.xlabel("x")
plt.ylabel("$y = 2(x+5)^2$")
plt.show()
```
### Tests
![](https://github.com/thumulakaru/Unit-2--repo/blob/main/Quizzes/Quiz_024_Tests.png)
**Fig. 1** Tests of Quiz 24 part A

## Part B
### Boolean cricuit
![](https://github.com/thumulakaru/Unit-2--repo/blob/main/Quizzes/Quiz_024_Boolean_Circuit.jpg)
