---
layout: post
title:  "PhantomX Robot Build"
date:   2020-04-02 4:19:00 -0600
categories: [Tutorial]
tags: [Robotics]
---

# Overview

Recently I purchased the [PhantomX Pincher Robot Arm](https://www.trossenrobotics.com/p/PhantomX-Pincher-Robot-Arm.aspx) and began the build process. Below are some notes and 'gotchas' that I'd like to pass along to others.

## Experience

The build is a bit challenging. If building an Ikea desk or bed is a 5,  rebuilding a carburetor is a 10 and getting started on a Mac is a 1, I would say that this is about a 6.5. Challenging, but you'll have to be careful and there are some 'tricky' parts to the instructions. Below are some things that I learned during the build. This is my 'pay it forward' for all of the internet help that I've received over the years.

# Instructions

* The [Arbotix Getting Started Guide](https://learn.trossenrobotics.com/arbotix/7-arbotix-quick-start-guide) worked fine.

## Roboplus Issues

* Last item in the [Arbotix Getting Started Guide](https://learn.trossenrobotics.com/arbotix/7-arbotix-quick-start-guide) that takes you to the next steps seems inaccurate.

![RoboPlus Not Correct](/assets/img/post_images/PhantomX-Build/Dynamixel-Robopus-Not-Correct.jpg)

* **Behavior**: When running the DYnamixel RoboPlus I could not get it to recognize the port. 
    * Does not recognize the port.
    * Run the [dynamixel instructions](https://learn.trossenrobotics.com/index.php/getting-started-with-the-arbotix/1-using-the-tr-dynamixel-servo-tool#&panel1-1)

* Seems that this is accurately described in the  [Trossen Getting Started Overview](https://learn.trossenrobotics.com/) guide
![](/assets/img/post_images/PhantomX-Build/Dynamixel-ID-Guide.jpg)

## Dynamixel Istructions
* Ran into an issue when running version 1.3
* **Behavior**: Could not get version 1.3 working [dynaManager Version 1.3](https://github.com/Interbotix/dynaManager/releases/tag/1.3).
* Submitted a github [issue ticket](https://github.com/Interbotix/dynaManager/issues/2)

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

* **Solution**: You should run the [dynaManager Version 1.2 with Java](https://github.com/Interbotix/dynaManager/releases/tag/1.2). Here is the [zip File](https://github.com/Interbotix/dynaManager/releases/download/1.2/dynaManager_windows_with_java.zip)


    
    * Error when running: 



## dynaManager Problems





[Dynamixel Servo Tool](https://learn.trossenrobotics.com/index.php/getting-started-with-the-arbotix/1-using-the-tr-dynamixel-servo-tool#&panel1-1)

[Setting DYNAMIXEL AX and MX Series Firmware, ID, and BAUD with ROBOPLUS 1.0](https://learn.trossenrobotics.com/projects/194-setting-dynamixel-ax-and-mx-series-firmware-id-and-baud-with-roboplus-1-0.html)

# Robot Build

## Step 1
* [Nut Insertion YouTube.com](https://youtu.be/o0JtXuj7HmA) video is useful, but my experience was that they didn't 'snap' into place. The Nuts were still not aligned. I used the driver to push them down from the opposite side of the nut (see images).
![Nuts Misaligned](/assets/img/post_images/PhantomX-Build/Misaligned-Nuts.jpg)


* Recommend using another tool. Seemed to 'round' the edges of my drive tool doing this. Should have known better. 
* Able to use supplied allen wrench to do a 'finish tightening' (thank you [Trossen Robotics](https://www.trossenrobotics.com)!)
![Align Nuts](/assets/img/post_images/PhantomX-Build/Align-Nuts.jpg)


## Step 2

* [Step 2.4](https://learn.trossenrobotics.com/16-interbotix/robot-arms/pincher-robot-arm/163-phantomx-pincher-robot-arm-assembly-guide.html) doesn't list bolts for the 15mm + 30mm standoff. Should include 8x M3*10 Bolts


![Step 2 Bolts List](/assets/img/post_images/PhantomX-Build/Step-2-Bolts-Incorrect.jpg)

## Step 3

* Only 1 Metal F4 Bracket sent (not 2).
* No spacers
* No F3 Brackets

![Starting Parts](/assets/img/post_images/PhantomX-Build/StartingParts.jpg)

![Current State](/assets/img/post_images/PhantomX-Build/CurrentState.jpg)