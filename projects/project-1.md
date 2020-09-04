---
layout: project
type: project
image: images/arm.png
title: RobotArm
permalink: projects/robotarm
# All dates must be YYYY-MM-DD format!
date: 2019-12-9
labels:
  - Robotics
  - Raspberry Pi
  - Python
summary: Basic robot arm
---

<div class="ui small rounded images">
  <img class="ui image" src="../images/micromouse-robot.png">
  <img class="ui image" src="../images/micromouse-robot-2.jpg">
  <img class="ui image" src="../images/micromouse.jpg">
  <img class="ui image" src="../images/micromouse-circuit.png">
</div>
This is a robotic arm a group and I have developed for computer architecture. We were supposed to hook it up to some joysticks so it could be controlled that way, but it didn't turn out the way it should, mainly because the joysticks were not being detected.

Here is some code that illustrates how we read values from the line sensors:
```js
30
byte ADCRead(byte ch)
31
{
    word value;
    ADC1SC1 = ch;
    while (ADC1SC1_COCO != 1)
    {   // wait until ADC conversion is completed   
    }
    return ADC1RL;  // lower 8-bit value out of 10-bit data from the ADC
}
```
