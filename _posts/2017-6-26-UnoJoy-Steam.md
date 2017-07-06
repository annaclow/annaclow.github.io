---
layout: post
title: UnoJoy & Steam & Collaborative Play!
---

[Unojoy](https://github.com/AlanChatham/UnoJoy) allows you to turn your arduino (i'm using an Uno as we were given them in Physical Computing) into a USB controller, which as it turns out works with steam !!

<iframe width="560" height="315" src="https://www.youtube.com/embed/FqfR1u44Pnk?ecver=1" frameborder="0" allowfullscreen></iframe>
First you upload code which allows the arduino pins to act as different buttons of the controller;The way the arduino interacts as a controller is through sending different pins 0, as they are all pulled up, to show which button/joystick is being used. 

```java
//when pin 8 is connected to ground the arduino registers the controller input
 controllerData.dpadUpOn = !digitalRead(8);
```

But! You have to update the firmware on your arduino, which is done through:
1. Installing DFU  programming software
2. Bridge the reset pin & ground pin on the Ardunio which resets ATmega16U2 chip
3. Use UnoJoy's shell script to reprogram the Arduino

Then it's recognised as a controller by your computer !! Thanks Alan Chatham!!

![altText](https://annaclow.github.io/blogImages/SteamUnoJoy.png)

This video has been super useful is calibrating some of the paramaters, building soon!!
<iframe width="560" height="315" src="https://www.youtube.com/embed/GrO8ZmxbOyI?ecver=1" frameborder="0" allowfullscreen></iframe>
