---
layout: post
title: Ubuntu Error-VMLinuz Not Found
date: 2020-04-28 8:55:00 -0500
categories: [tutorial]
tags: [linux]
seo:
  date_modified: 2020-05-05 10:10:19 -0500
---
![VMLinuz File Not Found](/assets/img/post_images/VMLinuzFileNotFound.jpg)


# Installing Ubuntu on AMD Ryzen: VMLinuz Error

# TL;DR

* Installation error `/casper/vmlinuz:file not found`
  * **Diagnosis**: Using Rufus boot drive builder for writing ISO didn't create vmlinuz file.
  * **Solution**: Used [Pendrive](https://www.pendrivelinux.com/universal-usb-installer-easy-as-1-2-3/) USB boot builder.
* Unable to get rig to recognize USB boot drive.
  * **Diagnosis** Boot drive order had hard drive before USB drive.
  * **Solution** During machine boot up go into machine BIOS (my machine it was by pressing F2 during boot up) and re-order the boot drive order in the BIOS.

## Background

Three years ago my son was ready to make the leap from my hand-me-down laptop to a full gaming rig. I told him we were going to do this 'old school' and build our own rigs like we 'used to do in the good ol' days'. His eyes rolled when I regailed him with stories of going to the comptuer swap meet where I would walk down aisles and aisles of vendors looking for the best price for a particular component. You could bargain with the vendors if you were willing to purchase multiple components. Those were good times. I told him about when I bought my first rig in 1987 and I how I was faced with an important decision--How large of a hard drive should I buy? I remember standing there trying to decide between a 20 and 40 MB hard drive (yes you read that right **MB**) and I was balking at the 40MB drive because, 'What in the world would I do with 40MBs?'. For those of you that are too young to remember, back then the biggest files that you would store on your hard drive were MS Word files at maybe 100k. Storing photos, music, and videos was not even possible--but people thought, 'Maybe one day'. So in an attempt to make my rig 'future proof' I opted for the 40MB hard drive. But I digress.

## 2017 Build

When my son and I bought our rig components in 2017 the [AMD Ryzen](https://www.amd.com/en/ryzen) chips were just released and the performance reviews were amazing. I did some research, talked with my son about them, he did his own research (amazing times) and we decided to take the calculated risk. When the components arrived, my son jumped right into the build and referenced [YouTube](https://youtube.com) whenever he had any questions. 'It's sort of like [Legos](https://www.lego.com) Dad. Each piece just fits.' I guess the small fortune that I spent on [Lego](https://www.lego.com) kits 'for him' was starting to pay off.

![Old School Build](/assets/img/post_images/NickBuild.jpg)

I love my rig (*Phoenix*). The only downside that I have experinced was that the Linux distros really weren't up-to-date for the Ryzen chips in 2017. Our rigs were primarily for gaming so the Ubuntu operating system really was not a priority. However, with the COVID19 stay-at-home initiative, I've had more time (like many of us) to improve my home life so I decided to finally go back and make *Phoenix* a dual-boot machine. I ran into a couple small glitches and I thought that I would share the solution (and regail you with my stories in the process).

## *Phoenix* configuration

|Item	| Version|
|---	|---	|
|[Ubuntu](https://ubuntu.com/)	| 20.04 LTS |
|[Rufus](https://rufus.ie/)	|3.10|  
|[Pendrive](https://www.pendrivelinux.com/universal-usb-installer-easy-as-1-2-3/)|1.9.9.0|  
|CPU|[AMD RYZEN 7 1700](https://www.newegg.com/amd-ryzen-7-1700/p/N82E16819113428?Item=N82E16819113428)|
|Memory | [Corsair DDR Memory](https://www.newegg.com/corsair-16gb-288-pin-ddr4-sdram/p/N82E16820233863?Item=N82E16820233863)
|Motherboard|[ASRock X370 Taichi AM4 AMD](https://www.newegg.com/asrock-x370-taichi/p/N82E16813157757?Item=N82E16813157757)

# Installation Issues

## USB Boot Drive Not Detected

The first issue that I had was that the USB Boot Drive was not being recognized and it was going directly to Windows 10. To overcome this I simply had the USB drive connected to my rig , restarted the machine and went into the BIOS by pressing the F2 key during bootup. I was then able to re-order the bootable drives on *Phoenix* (see image below). Placing the USB drive before my hard drives fixed the problem right away.

![Boot Drive Order](/assets/img/post_images/BootDriveOrder.jpg)


## /casper/vmlinuz: file not found

When I was able to get *Phoenix* to recognize the USB d.pngrive I thought that I was home free. Then I got an error `/casper/vmlinuz: file not found`. "Huh?!". I checked the folder and sure enough there was no `vmlinuz` file in the `/casper` directory. I tried re-dowloading the IOS and loading it again, and had the same issue. 

![Casper directory](/assets/img/post_images/NoVMLinuzFile.jpg)

I built a bootable USB thumb drive using [Rufus](https://rufus.ie/) as [suggested](https://ubuntu.com/tutorials/tutorial-create-a-usb-stick-on-windows#2-requirements) by [Ubuntu](https://ubuntu.com) (see image below). So I thought that it should work fine.

![Rufus](/assets/img/post_images/UbuntuInstallRufus.png)

I ran around the internet trying to find a solution. On an unrelated topic, someone did mention building the bootable USB with [Pendrive](https://www.pendrivelinux.com/universal-usb-installer-easy-as-1-2-3/). I then downloaded the [Pendrive](https://www.pendrivelinux.com/universal-usb-installer-easy-as-1-2-3/) USB installer. When I mounted the ISO the `vmlinuz' file was there and everything worked fine. I'm not sure what the issue is with [Rufus](https://rufus.ie/) as [suggested](https://ubuntu.com/tutorials/tutorial-create-a-usb-stick-on-windows#2-requirements) but I'm now working well in my new Ubuntu environment so I'm on to new adventures.
