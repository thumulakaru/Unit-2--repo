# Quiz 18
## Solution
```.py
from math import ceil

# Using mathematics
def number_Matches_math(l:int,s:int):
    out = ceil((l/(s/100)) / 5)
    out = f"{out} Matches"
    return out


print("Math method")
print(number_Matches_math(100, 100))
print(number_Matches_math(250, 110))
print(number_Matches_math(500, 150))
print(number_Matches_math(12345, 123))

# Using algorithm


def number_matches_algo(l:int, s:int):
    l_in_cm = l * 100
    num_matches = 0
    while l_in_cm > 0:
        l_in_cm -= (s * 5)
        num_matches += 1
    num_matches = f"{num_matches} Matches"
    return num_matches


print(f"\nAlgorithmic method")
print(number_matches_algo(100, 100))
print(number_matches_algo(250, 110))
print(number_matches_algo(500, 150))
print(number_matches_algo(12345, 123))
```

## Tests
![](https://github.com/thumulakaru/Unit-2--repo/blob/main/Quizzes/Quiz_018_Tests.png)

## Boolean Algebra(HL)
### Question
out = ABC+(A+B+C)+not(notA notB notC)

### Answer
![](https://github.com/thumulakaru/Unit-2--repo/blob/main/Quizzes/Quiz_018_Truth_Table.jpg)
