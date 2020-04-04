---
layout: post
title:  "PhantomX Robot Setup"
date:   2020-04-02 4:19:00 -0600
categories: [Tutorial]
tags: [Robotics]
---

# Overview

[PhantomX Pincher Robot Arm](https://www.trossenrobotics.com/p/PhantomX-Pincher-Robot-Arm.aspx)

## Instruction issues

* The [Arbotix Getting Started Guide](https://learn.trossenrobotics.com/arbotix/7-arbotix-quick-start-guide)worked fine.
    * Insert Dynamixel-Robopus-Not-Correct.jpg (Not correct)
    * Does not recognize the port.
    * Run these [dynamixel instructions](https://learn.trossenrobotics.com/index.php/getting-started-with-the-arbotix/1-using-the-tr-dynamixel-servo-tool#&panel1-1)
    * Follow the [Trossen Getting Started Overview](https://learn.trossenrobotics.com/) guide
    * Insert Dynamixel-ID-Guide.jpg
## dynaManager Problems

* Use [dynaManager Version 1.2 with Java](https://github.com/Interbotix/dynaManager/releases/tag/1.2) [zip File](https://github.com/Interbotix/dynaManager/releases/download/1.2/dynaManager_windows_with_java.zip)
* Could not get version 1.3 working [dynaManager Version 1.3](https://github.com/Interbotix/dynaManager/releases/tag/1.3)

```
ControlP5 2.0.4 infos, comments, questions at http://www.sojamo.de/libraries/controlP5
Exception in thread "Animation Thread" java.lang.UnsatisfiedLinkError: jssc.SerialNativeInterface.getSerialPortNames()[Ljava/lang/String;
        at jssc.SerialNativeInterface.getSerialPortNames(Native Method)
        at jssc.SerialPortList.getWindowsPortNames(SerialPortList.java:309)
        at jssc.SerialPortList.getPortNames(SerialPortList.java:298)
        at jssc.SerialPortList.getPortNames(SerialPortList.java:182)
        at processing.serial.Serial.list(Unknown Source)
        at dynaManager.setup(dynaManager.java:375)
        at processing.core.PApplet.handleDraw(PApplet.java:2359)
        at processing.core.PGraphicsJava2D.requestDraw(PGraphicsJava2D.java:240)
        at processing.core.PApplet.run(PApplet.java:2254)
        at java.lang.Thread.run(Unknown Source)
```

[Dynamixel Servo Tool](https://learn.trossenrobotics.com/index.php/getting-started-with-the-arbotix/1-using-the-tr-dynamixel-servo-tool#&panel1-1)

[Setting DYNAMIXEL AX and MX Series Firmware, ID, and BAUD with ROBOPLUS 1.0](https://learn.trossenrobotics.com/projects/194-setting-dynamixel-ax-and-mx-series-firmware-id-and-baud-with-roboplus-1-0.html)

## Servo Build

* [Nut Insertion YouTube.com](https://youtu.be/o0JtXuj7HmA) video is useful, but my experience was that they didn't 'snap' into place. The Nuts were still not aligned. I used the driver to push them down from the opposite side of the nut (see images).
* Recommend using another tool. Seemed to 'round' the edges of my drive tool doing this. Should have known better.

[Image of nut not aligned]
[Image of using the driver to set nut]

* Use supplied allan wrench to do a 'finish tightening'

* [Step 2.4](https://learn.trossenrobotics.com/16-interbotix/robot-arms/pincher-robot-arm/163-phantomx-pincher-robot-arm-assembly-guide.html) doesn't mention bolts for the 30mm standoff. The parts list also mentions only 4 M3x8 bolts. I think that it should be 8. 4 for the 10mm standoff and 4 for the 30mm standoff.

[Step 2.4 Incorrect](Step-2-Bolts-Incorrect.jpb)


