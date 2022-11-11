# Quiz 23
## Part A
### Solution
```.py
import random
random.seed(1234)

def produce(n: int, m: int, s: int):
    c1 = "x"
    c2 = "y"
    x_list = []
    y_list = []
    for i in range(n):
        x = random.randint(0, 100)
        y = round(x ** (1/2*((m/s)**2)), 2)
        x_list.append(x)
        y_list.append(y)
    return x_list, y_list


data_x, data_y = produce(n=10, m=5, s=2)

from matplotlib import pyplot as plt

plt.plot(data_x, data_y, color ='r', marker = "o")
plt.xlabel("x")
plt.ylabel("$y = x^{1/2(m/a)^2}$")

plt.show()
```
### Tests
![](https://github.com/thumulakaru/Unit-2--repo/blob/main/Quizzes/Quiz_023_Tests.png)
## Part B
### Truth Table

| A | B | A+B | A(A+B) |
|:-:|:-:|:---:|:------:|
| 0 | 0 |  0  |    0   |
| 0 | 1 |  1  |    0   |
| 1 | 0 |  1  |    1   |
| 1 | 1 |  1  |    1   |
