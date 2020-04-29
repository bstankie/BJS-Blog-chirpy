---
layout: post
title: Ubuntu Error-VMLinuz Not Found
date: 2020-04-28 8:55:00 -0500
categories: [tutorial]
tags: [linux]
---
![VMLinuz File Not Found](/assets/img/post_images/VMLinuzFileNotFound.jpg)


# Installing Ubuntu on AMD Ryzen: VMLinuz Error

## Background

Three years ago my son was ready to make the leap to a dedicated gaming rig. I told him we were going to do this 'old school' and build our own rigs like we 'used to do in the olden days'. His eyes rolled when I regailed him with stories of going to the comptuer swap meets where we would walk down aisles of vendors and you would buy your components from different vendors. They were good times. I told him about when I bought my first rig in 1987 and I was deciding between a 20 and 40 MB hard drive (yes you read that right MB) and I was balking at the 40MB drive because, 'What in the world would I do with 40MB?'. For those of you that are two young to know, back then the biggest files that you would put on your rig were probably MS Word files. Putting photos on your rig (music wasn't even a thought) was something that we knew was coming so I decided to be prepared and buy the 40 MB hard drive.

![Old School Build](/assets/img/post_images/NickBuild.jpg)


Anyhow, I digress. When my son and I bought our rigs in 2017 the AMD Ryzen chips were just released and the performance reviews were amazing. I did some research, talked with my son about it and we decided to go for it. 

I love my rig (*Phoenix*). The only downside that I have experinced was that the Linux distros really weren't up-to-date for the Ryzen chips. Our rigs were primarily for gaming so the Ubuntu operating system really was not a priority. However, with the COVID19 stay-at-home initiative, I've had more time (like many of us) to improve my home life so I decided to finally go back and make *Phoenix* a dual-boot machine. I ran into a couple small glitches and I thought that I would share the solution (and regail you with my story).

## *Phoenix* configuration

|Item	| Version|
|---	|---	|
|[Ubuntu](https://ubuntu.com/)	| 20.04 LTS |
|[Rufus](https://rufus.ie/)	|3.10|  
|[Pendrive](https://www.pendrivelinux.com/universal-usb-installer-easy-as-1-2-3/)|1.9.9.0|  
|CPU|[AMD RYZEN 7 1700](https://www.newegg.com/amd-ryzen-7-1700/p/N82E16819113428?Item=N82E16819113428)|
|Memory | [Corsair DDR Memory](https://www.newegg.com/corsair-16gb-288-pin-ddr4-sdram/p/N82E16820233863?Item=N82E16820233863)
|Motherboard|[ASRock X370 Taichi AM4 AMD](https://www.newegg.com/asrock-x370-taichi/p/N82E16813157757?Item=N82E16813157757)


### USB Boot Drive Not Detected

The first issue that I had was that the USB Boot Drive was not being recognized and it was going directly to Windows 10. To overcome this I simply had the USB drive connected to my rig and went into the BIOS using the F2 key during bootup. I was then able to re-order the bootable drives on *Phoenix*.

![Boot Drive Order](/assets/img/post_images/BootDriveOrder.jpg)


### \/casper\/vmlinuz Not Found

I built a bootable USB thumb drive using [Rufus](https://rufus.ie/) as [suggested](https://ubuntu.com/tutorials/tutorial-create-a-usb-stick-on-windows#2-requirements) by [Ubuntu](https://ubuntu.com). 

![Rufus](/assets/img/post_images/UbuntuInstallRufus.png)

When I was able to get *Phoenix* to recognize the USB d.pngrive I thought that I was home free. Then I got an error `/casper/vmlinuz: file not found`. "Huh?!". Sure enough there was no `vmlinuz` file in the `/casper` directory. I tried re-dowloading the IOS and loading it again, and had the same issue. 

![Rufus](/assets/img/post_images/NoVMLinuzFile.jpg)


**Solution**: I downloaded the [Pendrive](https://www.pendrivelinux.com/universal-usb-installer-easy-as-1-2-3/) USB installer. When I mounted the ISO, I could now see the `vmlinuz' file and everything worked fine.
