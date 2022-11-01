# Quiz 20
## Part a
### Solution
```.py
def get_truth():
    out = []
    # Printing title
    print(f"| A | B | C |")

    for i in range(8):
        a_value_temp = i//4
        b_value_temp = (i % 4)//2
        c_value_temp = i % 2
        out.append(f"| {a_value_temp} | {b_value_temp} | {c_value_temp} |")
    return out


display = get_truth()
# Printing the list of outputs properly 
print(*display, sep="\n")

```
### Tests
![](https://github.com/thumulakaru/Unit-2--repo/blob/main/Quizzes/Quiz_020_Tests.png)

## Part b
### Boolean Circuit
![](https://github.com/thumulakaru/Unit-2--repo/blob/main/Quizzes/Quiz_020_Boolean_Circuit.jpg)

### Truth Table
![](https://github.com/thumulakaru/Unit-2--repo/blob/main/Quizzes/Quiz_020_Truth_Table.jpg)
