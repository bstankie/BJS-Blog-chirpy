---
layout: post
title: PhantomX Robot Build
date: 2020-04-02 4:19:00 -0600
categories: [tutorial]
tags: [robotics]
seo:
  date_modified: 2020-04-05 11:29:41 -0500
---

# Overview

Recently I purchased the [PhantomX Pincher Robot Arm](https://www.trossenrobotics.com/p/PhantomX-Pincher-Robot-Arm.aspx) and began the build process. Below are some notes and 'gotchas' that I'd like to pass along to others.

## Starting State

![Starting Parts](/assets/img/post_images/PhantomX-Build/StartingParts.jpg)
Parts for the [PhantomX Pincher Robot Arm](https://www.trossenrobotics.com/p/PhantomX-Pincher-Robot-Arm.aspx). I marked the servos with white marker to make identifying the servos much easier. I would recommend something like this.

## Finished State

![Starting Parts](/assets/img/post_images/PhantomX-Build/FinishedPhanomXRobot.jpg)

## Experience

The build is a bit challenging. If building an [Ikea Bed](https://www.ikea.com/us/en/p/brimnes-bed-frame-with-storage-headboard-black-luroey-s79129608/) has a difficulty value of 5 (good clear instructions),  rebuilding a carburetor is a 10 (no real instructions and figuring it out as you go) and getting started on a Mac is a 1 (just press the power button), I would say that this is about a 7. Doable but the instructions can be a little bit tricky. To that end below are some things that I learned during the build that should help anyone who might be considering building the robot (including the future me).

## Review

* For roughly $400 this is a great flexible *desktop robot*. 
* The Dynamixel servos are a great thing to have. 
* [Trossen Robotics](https://www.trossenrobotics.com/) were really supportive. I purchased this during the COVID19 Quarantine period of 2020 and when initially delivered there were parts missing (check the parts list). 
  * I sent them a picture of the parts that I had and requested replacement parts and they sent them no questions.
  * Unfortunately, they had a skeleton crew due to COVID19 and not all of the replacement parts came. During this time grace was needed. They then shipped the remaining part overnight. Thank you Trossen!
* From the robot quality and build I would build this robot again (especially now that I have the help tips below). I am eager to see how the programming goes and I plan on doing a separate blog on that experience.


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

The parts list for Step #3 has changed. Specifically the *Arm Spacer* are no longer 8 stacked pieces but instead its a single 3D printed part (see below).

![Spacers Product List](/assets/img/post_images/PhantomX-Build/SpacersProdList.jpg) 

'Arm Spacers' listed in the product list and product build

![Spacers Product List](/assets/img/post_images/PhantomX-Build/SpacersNew.jpg) 
New 3D printed 'Arm Spacers'.

