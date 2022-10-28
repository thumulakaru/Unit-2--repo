# Quiz 19
## Part a
### Solution
```.py
def get_l3tt3r(msg:str):
    # Defining the special characters
    key_dict = {"a": "4", "e": "3", "i": "1", "o": "0", " ": "_"}
    # Defining the output variable of the function
    out = ""
    for i in range(len(msg)):
        temp = msg[i]
        # Selecting the characters inside the string
        if msg[i].lower() in key_dict.keys():
            temp = (key_dict.get(msg[i].lower()))
        out += temp
    return out


# Testing all given inputs
Tests = ["Hello World", "Why did I choose CS?", "Remember the Figure Caption?"]
for i in range(3):
    out = get_l3tt3r(Tests[i])
    print(f"{i+1}. {out}")
```

### Tests
![](https://github.com/thumulakaru/Unit-2--repo/blob/main/Quizzes/Quiz_019_Tests.png)

## Part b
### Circuit
![](https://github.com/thumulakaru/Unit-2--repo/blob/main/Quizzes/Quiz_019_Boolean_Circuit.jpg)
