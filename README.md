# CircuitPython
This repository will actually serve as a aid to help you get started with your own template.  You should copy the raw form of this readme into your own, and use this template to write your own.  If you want to draw inspiration from other classmates, feel free to check [this directory of all students!](https://github.com/chssigma/Class_Accounts).
## Table of Contents
* [Table of Contents](#TableOfContents)
* [Hello_CircuitPython](#Hello_CircuitPython)
* [CircuitPython_Servo](#CircuitPython_Servo)
* [CircuitPython_LCD](#CircuitPython_LCD)
* [NextAssignmentGoesHere](#NextAssignment)
---

## Hello_CircuitPython

### Description & Code
Description goes here
First assignment was pretty okay, wasn't too diffucult or challenging 
Here's how you make code look like code:

```python
Code goes here
import board
import neopixel
import time

dot = neopixel.NeoPixel(board.NEOPIXEL, 1, brightness= 0.3)
while True:
    print("Make it blue!")
    dot.fill((0,0,255))
    time.sleep(.5)
    dot.fill((255, 255, 0))
    time.sleep(.5)
```


### Evidence
Pictures / Gifs of your work should go here.  You need to communicate what your thing does.

### Wiring
Make an account with your google ID at [tinkercad.com](https://www.tinkercad.com/learn/circuits), and use "TinkerCad Circuits to make a wiring diagram."  It's really easy!  
Then post an image here.   [here's a quick tutorial for all markdown code, like making links](https://guides.github.com/features/mastering-markdown/)

### Reflection
What went wrong / was challenging, how'd you figure it out, and what did you learn from that experience?  Your ultimate goal for the reflection is to pass on knowledge that will make this assignment better or easier for the next person.
Nothing really went wrong, it was fun and challenging.



## CircuitPython_Servo

### Description & Code
This assigment was actually challenging, didn't understand most of it but somehow did it. My servo doesn't move around or shake when i want it to.
```python
Code goes here
"""CircuitPython Essentials Servo continuous rotation servo example"""
import time
import board
import pwmio
from adafruit_motor import servo

# create a PWMOut object on Pin A2.
pwm = pwmio.PWMOut(board.A2, frequency=50)

# Create a servo object, my_servo.
my_servo = servo.ContinuousServo(pwm)

while True:
    print("forward")
    my_servo.throttle = 1.0
    time.sleep(2.0)
    print("stop")
    my_servo.throttle = 0.0
    time.sleep(2.0)
    print("reverse")
    my_servo.throttle = -1.0
    time.sleep(2.0)
    print("stop")
    my_servo.throttle = 0.0
    time.sleep(4.0)

```

### Evidence

### Wiring

### Reflection




## CircuitPython_LCD

### Description & Code
the color changes based on the distance, if your phone gets closer and further the colors change
```python
Code goes here
try:
    distance = sonar.distance
    print((distance))

    if distance < 5:
        r = 255
        g = 0
        b = 0
    elif distance > 5 and distance < 20:
        r = simpleio.map_range(distance, 5, 20, 255, 0)
        b = simpleio.map_range(distance, 5, 20, 0, 255)
        g = 0
        r = int(r)
        g = int(g)
        b = int(b)
    elif distance > 20 and distance < 35:
        r = 0
        b = simpleio.map_range(distance, 20, 35, 255, 0)
        g = simpleio.map_range(distance, 20, 35, 0, 255)
        r = int(r)
        g = int(g)
        b = int(b)
    elif distance > 35:
        r = 0
        b = 0
        g = 255
        r = int(r)
        g = int(g)
        b = int(b)
    print(r, g, b)
    time.sleep(0.05)

except RuntimeError:
    print("Retrying!")
    r = 0
    g = 0
    b = 255
    time.sleep(0.05)

print(r, g, b)
dot.fill((int(r), int(b), int(g)))
time.sleep(0.05)
```

### Evidence

### Wiring

### Reflection





## NextAssignment

### Description & Code

```python
Code goes here

```

### Evidence

### Wiring

### Reflection
