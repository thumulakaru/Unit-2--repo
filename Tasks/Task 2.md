# System Diagram Binary Counter
## Python code
```.py
from pyfirmata import Arduino
import time

board = Arduino('/dev/cu.usbserial-120')
print("Board is ready")

while True:  
  for i in range(8):
      board.digital[12].write(i//4)
      time.sleep(1)
      board.digital[5].write((i%4)//2)
      time.sleep(1)
      board.digital[9].write(i%2)
      time.sleep(1)
```

## Arduino output
[Link for the video](https://drive.google.com/file/d/1f_uqRTZztHHKePOmN2UyAHlGDSkFtJRf/view?usp=share_link)
