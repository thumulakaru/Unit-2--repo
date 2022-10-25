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
    for word in words:
        for char in word:
            if char == " ":
                spaces += 1

    for i in new_words:
        for letters in i:
            letter_count += 1
    average = letter_count/(len(new_words)+spaces)
    average = round(average, 1)
    return average


print(avarageLength())
```

## Tests
![](https://github.com/thumulakaru/Unit-2--repo/blob/main/Quizzes/Screen%20Shot%202022-10-25%20at%2014.01.23.png)
