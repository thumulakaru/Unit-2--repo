# Quiz 29
## Part A
### Solution
```.py
def count_letters(my_dict, msg):
    temp_list = my_dict.keys()
    for i in msg:
        if i in temp_list:
            my_dict[i] += 1
    return my_dict


dic_1 = {"w": 0, "l": 0, "c": 0}
dic_2 = {"a": 0, "e": 0, "i": 0, "o": 0, "u": 0}
msg_1 = "hello world"
msg_2 = "Why did I choose CS?"

print(count_letters(dic_1, msg_1))
print(count_letters(dic_2, msg_2))
```
### Tests
![](https://github.com/thumulakaru/Unit-2--repo/blob/main/Quizzes/Quiz_029_Tests.png)

**Fig.1** Tests for the quiz 29 programming question

## Part B
### Answer
Since there are 6 bits the total number of colours that can be stored in the computer is,

2^6 = 64
