# System Diagram Binary Counter
# Task 2

## System Diagram
![](https://github.com/thumulakaru/Unit-2--repo/blob/main/Tasks/Task2_System_Diagram.jpeg)


## Prompt
To build the circuit below using Arduino and create the program in Python to control the LED.
*Fig.1* **System Diagram**

## Code Structure(Forever) 
```.py
# 2022-11-08 Task 2

# Binary counter to LEDs on Arduinos
from my_lib import validate_1_to_n_input
import time
from pyfirmata import Arduino

board = Arduino('/dev/cu.usbserial-10')
print("Board is ready")

while True:
    i = validate_1_to_n_input(input("Enter a number: "), 7)
    board.digital[12].write(0)
    board.digital[5].write(0)
    board.digital[9].write(0)
    board.digital[12].write(i // 4)
    board.digital[5].write((i % 4) // 2)
    board.digital[9].write(i % 2)
    time.sleep(1)
```

## Code Structure(User Input) 
```.py
# 2022-11-08 Task 2

# Binary counter to LEDs on Arduinos
from my_lib import validate_1_to_n_input
import time
from pyfirmata import Arduino

board = Arduino('/dev/cu.usbserial-10')
print("Board is ready")

while True:
    i = validate_1_to_n_input(input("Enter a number: "), 7)
    board.digital[12].write(0)
    board.digital[5].write(0)
    board.digital[9].write(0)
    board.digital[12].write(i // 4)
    board.digital[5].write((i % 4) // 2)
    board.digital[9].write(i % 2)
    time.sleep(1)
```

## Evidence
![](https://github.com/thumulakaru/Unit-2--repo/blob/main/Tasks/Task2_Evidence.jpeg)
*Fig.2* **Photo of the build**

As we can see in figure 2, there is an arduino. There are three wires going out from the arduino to the breadboard and a single wire from the breadboard to
the arduino. The arduino 5,9,12 ports are connected to LEDs on the breadboard. In between the LED and the wire from the ports there are resistors.

## Video

[Click here for the video](https://drive.google.com/file/d/1f_uqRTZztHHKePOmN2UyAHlGDSkFtJRf/view?usp=share_link)

*Link.1* **Video of the first program**

As we can see in the video the LEDs light up according to the binary notations of 0 to 7 and after it displays 7 it again starts over and do the same
procedure infinite times.

[Click here for the video](https://drive.google.com/file/d/1WceipQ8BIo40XUUcdxqDOk5iFVU0khUV/view?usp=share_link)

*Link.2* **Video of the second program**

As we can see in the video the LEDs light up according to the number that the user enters. If the user enters a number lower than 0 or higher than 7 the
program would ask the user for another input. If the user enter a set of characters including letters and symbols the program would again ask the user for
another valid input. When the user enters a number between 0 and 7(0 and 7 included) the bulbs display that number in binary notation until another valid
input is entered by the user.

## Citations
[1] Pinzon, Ruben. “System Diagram Binary Counter.” System Diagram Binary Counter, 8 Nov. 2022, docs.google.com/presentation/d/1sgshVux_DLBBhZKoKJrq9l79a9B_2aTzmdnAtdFDHhc/edit#slide=id.p.
