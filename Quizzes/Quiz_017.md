# Quiz 17
## Solution
```.py
def avarageLength(words = ["Hello", "main"]):
    new_words = []
    letter_count = 0
    spaces = 0

    for element in words:
        temp1 = element.replace(" ", "")
        new_words.append(temp1)

    for i in new_words:
        for letters in i:
            letter_count += 1
    average = letter_count/(len(new_words)+spaces)
    return average


print(avarageLength())
```

## Tests
![](https://github.com/thumulakaru/Unit-2--repo/blob/main/Quizzes/Quiz_017_Tests.png)
