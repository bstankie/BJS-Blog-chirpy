---
layout: post
title: Ubuntu Error-VMLinuz Not Found
date: 2020-04-28 8:55:00 -0500
categories: [tutorial]
tags: [linux]
---


# Installing Ubuntu on AMD Ryzen: VMLinuz Error

## Background

X years ago my son was ready to make the leap to a dedicated gaming rig. I told him we were going to do this 'old school' and build our own rigs like we 'used to do'. His eyes rolled when I regailed him with stories of going to the comptuer swap meets where you would buy your hard drive from one vendor, your motherboard from another and you would go home and put it all together (or upgrade). They were good times. I still remember buying my first rig in 1987 and I was deciding between a 20 and 40 MB hard drive (yes you read that right) and I was balking at the 40MB drive because ('What in the world would I do with 40MB?'). Anyhow, I digress. The only downside was that the Linux distros really weren't up-to-date for the Ryzen chips. Our rigs were primarily for gaming so the Ubuntu operating system really was not a priority. However, with the COVID19 stay-at-home initiative, I've had more time (like many of us) to improve our home life so I decided to finally go back and make Phoenix (name of my rig) a dual-boot machine. I ran into a couple small glitches and I thought that I would share the solution (and regail you with my story).

## Installation Issues

|Item	| Version|
|---	|---	|
|[Ubuntu](https://ubuntu.com/)	| 20.04 LTS |
|[Rufus](https://rufus.ie/)	|3.10|  
|[Pendrive](https://www.pendrivelinux.com/universal-usb-installer-easy-as-1-2-3/)|1.9.9.0|  
|CPU|[AMD RYZEN 7 1700](https://www.newegg.com/amd-ryzen-7-1700/p/N82E16819113428?Item=N82E16819113428)|
|Memory | [Corsair DDR Memory](https://www.newegg.com/corsair-16gb-288-pin-ddr4-sdram/p/N82E16820233863?Item=N82E16820233863)
|Motherboard|[ASRock X370 Taichi AM4 AMD](https://www.newegg.com/asrock-x370-taichi/p/N82E16813157757?Item=N82E16813157757)

## Boot Drive

I built a bootable USB thumb drive using [Rufus](https://rufus.ie/) as [suggested](https://ubuntu.com/tutorials/tutorial-create-a-usb-stick-on-windows#2-requirements) by [Ubuntu](https://ubuntu.com). 

### USB Boot Drive Not Detected

The first issue that I had was that the USB Boot Drive was not being recognized and it was going directly to Windows 10. To overcome this I simply had the USB drive connected to my rig and went into the BIOS using the F2 key during bootup. I was then able to re-order the bootable drives on *Phoenix*.

### V/casper/vmlinuz Not Found

When I was able to get *Phoenix* to recognize the USB drive I thought that I was home free. Then I got an error `/casper/vmlinuz not found`. "Huh?!". Sure enough there was no `vmlinuz` file in the `/casper` directory. I tried re-dowloading and loading it again, and had the same issue. 

**Solution**: I downloaded the [Pendrive](https://www.pendrivelinux.com/universal-usb-installer-easy-as-1-2-3/) USB installer. When I mounted the ISO, I could now see the `vmlinuz' file and everything worked fine.

Rufus
'/casper/vmlinuz not found'

pen extracted okay.