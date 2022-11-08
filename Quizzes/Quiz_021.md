# Quiz 21

## Part A
### Solution
```.py
def get_truth():
    out = []
    # Printing title
    print(f"| A | B | C | AB + not B + not CB |")

    for i in range(8):
        a_value_temp = i//4
        b_value_temp = (i % 4)//2
        c_value_temp = i % 2
        out_value = (a_value_temp and b_value_temp) or not(b_value_temp) or not(b_value_temp and c_value_temp)
        out.append(f"| {a_value_temp} | {b_value_temp} | {c_value_temp} | {(str(int(out_value))).center(20)}|")
    return out


display = get_truth()
print(*display, sep="\n")
```

### Tests
![](https://github.com/thumulakaru/Unit-2--repo/blob/main/Quizzes/Quiz_021_Tests.png)
**Figure 1:** Tests

## Part B
### Truth table
![](https://github.com/thumulakaru/Unit-2--repo/blob/main/Quizzes/Quiz_021_Truth_Table.jpg)

**Figure 2:** Truth table solution

### Boolean Circuit
![](https://github.com/thumulakaru/Unit-2--repo/blob/main/Quizzes/Quiz_021_Boolean_Circuit.jpg)

**Figure 3:** Boolean circuit solution
