---
title: CanaKit Raspberry Pi 5 Starter Kit PRO
date: 2025-03-16 11:00 PM
categories: [Raspberry Pi]
tags: [raspberry pi]
---

In this post, I'm going to share my experience with the CanaKit Raspberry Pi 5 Starter Kit PRO and walk you through assembling the Raspberry Pi 5. I've decided to start experimenting more with homelabbing and thought that a Raspberry Pi would be a good starting point. Since this is my first Raspberry Pi, I decided to purchase a complete starter kit and go with the [CanaKit Raspberry Pi 5 Starter Kit PRO - Turbine Black (128GB Edition) (8GB RAM)](https://www.amazon.com/CanaKit-Raspberry-Starter-Kit-PRO/dp/B0CRSNCJ6Y/ref=sr_1_1?crid=20O4N95DO5U3&dib=eyJ2IjoiMSJ9.gER6ai2B6BUf_1KSPtGdIoWCTXoXY2rt7NNwgXOEScLQ-D8IWoMmKsSQXkVoIeIU1MPgldeXhRf3we6rg57sxfAz2zgx9vhDm6oTBLJ_043WJ4Bcj4wZaq0iiaITj3mtnCK3nN6v-znLQffk7UrJr6I1rcnPdzV0O14-P2CePYfar6opYUPdRir_dk-TrN_tOfJMn8O8G-ppyCqhUEPbHobGYAiI7KvWkswfaFIPpFs.CLQBa44bfPAD4LFH4J3_114pNHH-_7sVYOmi9Qd7Hgs&dib_tag=se&keywords=raspberry%2Bpi%2B5&qid=1742147970&sprefix=raspberry%2Bpi%2B5%2Caps%2C117&sr=8-1&th=1){:target="_blank"} on Amazon for $159. My plan is to utilize the Raspberry Pi as a homelab and to experiment with running different services.

## Starter Kit Contents

Here is a list of everything that is included in the starter kit:
* Raspberry Pi 5 board with 2.4Ghz 64-bit quad-core CPU (8GB RAM)
* 128GB Samsung MicroSD card (pre-loaded with Pi OS)
* USB MicroSD card reader
* Black case for Raspberry Pi 5
* Fan
* Heat Sink
* 45W USB C power supply
* 2 Micro HDMI to HDMI cables

![CanaKit Raspberry Pi 5 Starter Kit PRO contents](https://res.cloudinary.com/do8uy1fxa/image/upload/v1742057071/canakit-contents_u48wjc.jpg)

## Assembly

Assembling the Raspberry Pi 5 was simple and straightforward, and there is even a [setup guide](https://www.canakit.com/pi5-case){:target="_blank"} you can watch. I just assembled it on my own.

### Raspberry Pi 5 board

Here is a picture of the Raspberry Pi 5 board itself:

![Raspberry Pi 5 board](https://res.cloudinary.com/do8uy1fxa/image/upload/v1742057164/pi-5-board_tbzqdu.jpg)

### Step 1: Attach heat sink

The first step is to attach the heat sink. Remove the covers from the thermal pads on the bottom of the heatsink, align the heat sink with the chips on the Pi board, and press down firmly.

![Raspberry Pi 5 board with heat sink attached](https://res.cloudinary.com/do8uy1fxa/image/upload/v1742057230/pi-5-board-with-heatsink_ufwtfw.jpg)

### Step 2: Insert Pi board into bottom casing

Carefully insert the Raspberry Pi 5 board into the bottom casing.

![Raspberry Pi 5 board inserted into bottom casing](https://res.cloudinary.com/do8uy1fxa/image/upload/v1742057184/pi-5-board-in-bottom-casing_eym4ok.jpg)

### Step 3: Attach fan

Remove the cap from the fan connector on the Pi board and connect the fan cable.

![Raspberry Pi 5 board with fan attached](https://res.cloudinary.com/do8uy1fxa/image/upload/v1742057208/pi-5-board-with-fan-attached_em3nnx.jpg)

### Step 4: Connect middle casing

Connect the middle casing to the bottom casing.

![Raspberry Pi 5 with middle and bottom casing connected](https://res.cloudinary.com/do8uy1fxa/image/upload/v1742057253/pi-5-with-middle-casing-attached_poy4jv.jpg)

### Step 5: Attach fan to top casing

Attach the fan to the top casing with the design facing outward.

![Fan attached to top casing of Raspberry Pi 5 case](https://res.cloudinary.com/do8uy1fxa/image/upload/v1742057118/fan-attached-to-top-cover_zj2vd8.jpg)

### Step 6: Attach top casing

Attach the top casing to the Pi case to finish the assembly.

![Raspberry Pi 5 case fully assembled](https://res.cloudinary.com/do8uy1fxa/image/upload/v1742057141/pi-5-assembled_pjlzeb.jpg)

### Step 7: Insert MicroSD card

Insert the MicroSD card into the MicroSD card slot on the Raspberry Pi 5. The MicroSD card included in the kit comes pre-loaded with Pi OS. If your using another SD card, you can download the Raspberry Pi Imager from [raspberrypi.com/software](https://www.raspberrypi.com/software/){:target="_blank"} to create a bootable SD card.

![MicroSD card inserted into MicroSD card slot on Raspberry Pi 5](https://res.cloudinary.com/do8uy1fxa/image/upload/v1742142992/pi-os-microsd-card-inserted-into-pi-5-sd-card-slot_jksmtu.jpg)

### Step 8: Boot and Setup

Boot the Raspberry Pi 5 after connecting the 45W USB C power supply, micro HDMI cable, and any peripherals. Once you complete the desktop setup wizard, you'll be greeted with the Raspberry Pi OS desktop.

![Screenshot of Raspberry Pi OS desktop](https://res.cloudinary.com/do8uy1fxa/image/upload/v1742057280/pi-os-desktop_xz8feh.jpg)

Updates should have been applied during setup. However, you can make sure everything is updated by running the following commands:
```shell
sudo apt update
sudo apt full-upgrade
```
The Raspberry Pi 5 is now fully assembled and up and running.

Overall, I'm happy with the CanaKit Raspberry Pi 5 Starter Kit PRO. The starter kit came with everything needed to get started, and the Raspberry Pi 5 was easy to assemble. I'm excited to start experimenting with the Raspberry Pi 5 and I will provide future posts on some of the things I have done with it.