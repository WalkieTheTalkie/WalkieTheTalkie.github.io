
---
2
layout: project
3
type: project
4
image: images/arm.png
5
title: RobotArm
6
permalink: projects/robotarm
7
# All dates must be YYYY-MM-DD format!
8
date: 2019-12-9
9
labels:
10
  - Robotics
11
  - Raspberry Pi
12
  - Python
13
summary: Basic robot arm
14
---
15
​
16
<div class="ui small rounded images">
17
  <img class="ui image" src="../images/micromouse-robot.png">
18
  <img class="ui image" src="../images/micromouse-robot-2.jpg">
19
  <img class="ui image" src="../images/micromouse.jpg">
20
  <img class="ui image" src="../images/micromouse-circuit.png">
21
</div>
22
​
23
This is a robotic arm a group and I have developed for computer architecture. We were supposed to hook it up to some joysticks so it could be controlled that way, but it didn't turn out the way it should, mainly because the joysticks were not being detected.
26
​
27
Here is some code that illustrates how we read values from the line sensors:
28
​
29
```js
30
byte ADCRead(byte ch)
31
{
32
    word value;
33
    ADC1SC1 = ch;
34
    while (ADC1SC1_COCO != 1)
35
    {   // wait until ADC conversion is completed   
36
    }
37
    return ADC1RL;  // lower 8-bit value out of 10-bit data from the ADC
38
}
39
```
