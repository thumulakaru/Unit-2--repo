# Quiz 22
## Part A
### Solution
```.py
import random
random.seed(1234)


def produce(n: int, m: int, s: int):
    c1 = "x"
    c2 = "y"
    print(f"|{c1.center(6)}|{c2.center(10)}|")
    out = []
    for i in range(n):
        x = random.randint(0, 100)
        y = round(x ** (1/2*((m/s)**2)), 2)
        out.append(f"|{str(x).center(6)}|{str(y).center(10)}|")
    return out

display = produce(5, 3, 2)
# Printing the list of outputs properly
print(*display, sep="\n")
```

### Tests
![](https://github.com/thumulakaru/Unit-2--repo/blob/main/Quizzes/Quiz_022_Tests.png)

**Figure 1:** Tests for the quiz

## Part B
### Truth Table

| A | B | A+B | A(A+B) |
|:-:|:-:|:---:|:------:|
| 0 | 0 |  0  |    0   |
| 0 | 1 |  1  |    0   |
| 1 | 0 |  1  |    1   |
| 1 | 1 |  1  |    1   |
### Another way

A = A(A+B)
When A = 0, the output is always going to be 0 due to the AND logic between A and A+B. This means that no matter the B's value if A is 0 the output is always
0. Also if A = 1, the output is always going to be 1 because, A + B = 1 and A.(A+B) = A.(1) = 1. Therefore no matter what value B has it does not have an
effect on the output. Thus,

A = A(A+B) is true.
Therefore,
| A | B | Output(A) |
|:-:|:-:|:---------:|
| 0 | 0 |     0     |
| 0 | 1 |     0     |
| 1 | 0 |     1     |
| 1 | 1 |     1     |
