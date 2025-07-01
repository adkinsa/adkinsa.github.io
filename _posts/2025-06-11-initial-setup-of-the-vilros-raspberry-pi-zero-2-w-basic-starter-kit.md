---
title: Initial setup of the Vilros Raspberry Pi Zero 2 W basic starter kit
date: 2025-06-11 9:00 PM
categories: [Raspberry Pi]
tags: [raspberry pi]
---

In a recent post I mentioned that I purchased the Vilros Raspberry Pi Zero 2 W basic starter kit. I purchased the [starter kit](https://www.amazon.com/Vilros-Raspberry-Incudes-HDMI-USB-Adapters/dp/B09M1PS35R/ref=sr_1_5?crid=14WXEOTDKOUA3&dib=eyJ2IjoiMSJ9.3BENuF2Ktu1UHOlVshSOQR65x4OX3ptA7XWs1dRUN9bQeTVmHuOYnaAwJcRE4n70YZzlUj_Ay0IaxqU2sPUffmhTH7DAg6Ud3rchltnlr78bJd5ANBwoTsoQpjvLPdvHfIXBAweNOFHGs2rQ7KVilSCsXK7IM1MzT52sP_ef4rZ8MjKr4myl4c_CwXmVrN6JUZBbIjHXfZWJWr8r6SDgWCG_AetHFQ88g98bB1uHMbo.qnFNE_FRkZpBvvIOF2V3rutSZ7M-l85SNfEXvGcxMvg&dib_tag=se&keywords=raspberry%2Bpi%2Bzero%2B2%2Bw&qid=1750350942&sprefix=raspberry%2Bpi%2Bzero%2B2%2Bw%2Caps%2C155&sr=8-5&th=1){: target="_blank"} on Amazon for $42, and it comes with just about everything needed to get started. I just got around to setting it up and wanted to share my experience with the initial setup process. In this post, I'll provide you with a quick overview of the starter kit and walk you through the steps I took to set up the Raspberry Pi Zero 2 W.

## Starter kit contents
Here's a list of everything that's included in the starter kit:
* Raspberry Pi Zero 2 W board
* Multi use case
* Micro USB power supply
* Micro USB to USB OTG adapter
* HDMI to mini HDMI adapter
* 40 pin header
* Camera module adapter cable
* Storage bag

![Vilros Raspberry Pi Zero 2 W basic starter kit contents on a table](https://res.cloudinary.com/do8uy1fxa/image/upload/v1749574282/vilros-raspberry-pi-zero-basic-starter-kit-contents_orsbsx.jpg)

## Setup
In this section, I'm going to walk you through the steps I took to set up the Raspberry Pi Zero 2 W.

### Step 1: Insert Pi board into bottom casing and apply thermal pad
First, I inserted the Pi board into the bottom casing and then applied the thermal pad to the CPU.

![Raspberry Pi Zero 2 W board in bottom casing on a table](https://res.cloudinary.com/do8uy1fxa/image/upload/v1749574210/raspberry-pi-zero-2-w-board-in-bottom-case_shsewd.jpg)

### Step 2: Attach top casing
Next, I attached the top part of the case and secured it in place with the screws on the bottom of the case.

![Raspberry Pi Zero 2 W with top and bottom casing attached on a table](https://res.cloudinary.com/do8uy1fxa/image/upload/v1749574193/raspberry-pi-zero-2-w-attach-top-case_o6exca.jpg)

### Step 3: Flash Raspberry Pi OS to Micro SD card
I then flashed Raspberry Pi OS to the Micro SD card using the Raspberry Pi Imager.

![Screenshot of Raspberry Pi Imager v1.9.4](https://res.cloudinary.com/do8uy1fxa/image/upload/v1749574177/raspberry-pi-imager-raspberry-pi-zero-2-w_gibwo4.png)

### Step 4: Insert Micro SD card
Once the Micro SD card was ready, I inserted it into the slot on the Pi board.

![Raspberry Pi Zero 2 W with Micro SD card inserted on a table](https://res.cloudinary.com/do8uy1fxa/image/upload/v1749574225/raspberry-pi-zero-2-w-insert-sd-card_iadvda.jpg)

### Step 5: Attach Micro SD card cover
Next, I attached the Micro SD card cover to the side of the case. 

![Raspberry Pi Zero 2 W case with Micro SD card cover attached on a table](https://res.cloudinary.com/do8uy1fxa/image/upload/v1749574264/raspberry-pi-zero-2-w-sd-card-cover_c7gds2.jpg)

### Step 6: Boot Raspberry Pi Zero 2 W
I then booted up the Raspberry Pi Zero 2 W and was greeted by the Raspberry Pi OS desktop.  

![Screenshot of Raspberry Pi OS desktop](https://res.cloudinary.com/do8uy1fxa/image/upload/v1749574247/raspberry-pi-zero-2-w-pi-os-desktop_gf5jgg.png)

### Step 7: Update system
Finally, I opened a terminal window and ran the following commands to update the system:
```shell
sudo apt update
sudo apt full-upgrade
```
The setup is now complete, and the Raspberry Pi Zero 2 W is up and running.

## Conclusion
All in all, I'm happy with the starter kit. It was a good value for the price and included everything needed to get started, except for a Micro SD card. Setting up the Raspberry Pi Zero 2 W was really simple and I'm looking forward to tinkering with it and seeing what it's capable of. My plan is to install Pi-hole on it and use it as a local DNS server in my homelab. So, that's what I'll be working on next.