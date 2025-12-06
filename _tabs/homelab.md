---
icon: fa-solid fa-computer
order: 4
---

This is an overview of my current homelab setup. Having a homelab allows me to learn about new technologies and practice building my skillset. One of my goals this year is to take my homelab to the next level and I'm currently working on implementing new technologies and hardware. I will update this page as I continue to make changes and add new things to my homelab.

## DeskPi RackMate T1

This is my DeskPi RackMate T1 10 inch mini server rack. Here's a quick rundown of the rack from top to bottom. At the top I added a patch panel and am using Monoprice SlimRun Cat6A patch cables (0.5ft and 1ft). Shelf 1 has an 8 port managed switch. Shelf 2 is an SBC shelf with a mounted Raspberry Pi 5 and 2.5" SATA SSD. Shelf 3 has a Beelink Mini PC. Finally, at the very bottom is a travel router.

![DeskPi RackMate T1](https://res.cloudinary.com/do8uy1fxa/image/upload/v1758930613/deskpi-rackmate-t1_pztgap.jpg)

## Hardware

Here is a detailed list of all my homelab hardware:
* GL.iNet GL-MT3000 Beryl AX Travel Router
* TP-Link TL-SG108e 8-Port Gigabit Managed Switch
* Beelink Mini S13 Mini PC
* Raspberry Pi 5 (8GB RAM)
* KingSpec 256GB 2.5" SATA 3 SSD
 
## VirtualBox

I currently use VirtualBox for all of my virtual machine needs. This lets me experiment with running different operating systems and learn about new technologies in a sandboxed environment. As of right now, my VirtualBox environment consists of several Linux VMs, as well as an Active Directory environment made up of a Windows Server 2019 domain controller and 2 Windows 10 client machines.

Virtual Machines:
* Windows Server 2019
* Windows 10 x 2
* Ubuntu 24.04
* Linux Mint 22
* Kali Linux

![Screenshot of virtual machine list in VirtualBox](https://res.cloudinary.com/do8uy1fxa/image/upload/v1746547923/virtualbox-homelab_m7ya3b.png)