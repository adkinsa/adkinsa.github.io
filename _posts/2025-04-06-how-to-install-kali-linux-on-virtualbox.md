---
title: How to install Kali Linux on VirtualBox
date: 2025-04-06 9:00 PM
categories: [Linux]
tags: [linux]
---

I recently installed Kali Linux on VirtualBox to use as an attack machine for completing rooms on [TryHackMe](https://tryhackme.com/){:target="_blank"}. So, I decided to write a step-by-step walkthrough of the installation process. In this post, I will walk you through the steps to obtain the Kali Linux ISO and install Kali Linux on VirtualBox.

Before getting started, make sure that virtualization is enabled in your computer's BIOS.

## Step 1: Download and install VirtualBox

Download and install VirtualBox from [https://www.virtualbox.org/wiki/Downloads](https://www.virtualbox.org/wiki/Downloads){:target="_blank"}.

## Step 2: Download Kali Linux ISO

1\. Go to [https://www.kali.org/](https://www.kali.org/){:target="_blank"}.

![Screenshot of kali.org](https://res.cloudinary.com/do8uy1fxa/image/upload/v1743871841/kali.org_ooae21.png)

2\. Click on "**GET KALI**" and then choose "**Installer Images**".

![Screenshot of kali.org's get kali page](https://res.cloudinary.com/do8uy1fxa/image/upload/v1743871857/kali.org-get-kali_uxbdad.png)

3\. On the Installer Images page, choose "**x86_64**" and click on the blue down arrow to download.

## Step 3: Create a new virtual machine in VirtualBox

1\. Open VirtualBox and click on the "**New**" button.

![VirtualBox interface](https://res.cloudinary.com/do8uy1fxa/image/upload/v1743872381/virtualbox-interface_o5gks9.png)

2\. Give the machine a name and select the Kali Linux ISO that you downloaded.

![VirtualBox create virtual machine window showing machine name and ISO image](https://res.cloudinary.com/do8uy1fxa/image/upload/v1743872518/virtualbox-new-machine_jpogrw.png)

3\. Allocate RAM and CPU cores to the machine. In this example, I allocated 4GB of RAM and 1 CPU core to the machine, but you can adjust this based on your host machine's resources.

![VirtualBox create virtual machine window showing RAM and CPU cores](https://res.cloudinary.com/do8uy1fxa/image/upload/v1743872544/virtualbox-select-ram-and-cpu_p9up9g.png)

4\. Create a Virtual Hard Disk. In this example, I allocated 50GB of space to the Virtual Hard Disk, but you can assign more if you want to.

![VirtualBox create virtual machine window showing Virtual Hard Disk](https://res.cloudinary.com/do8uy1fxa/image/upload/v1743872358/virtualbox-create-vhd_xxipj2.png)

5\. Review the machine summary and click finish.

![VirtualBox create virtual machine window showing machine summary](https://res.cloudinary.com/do8uy1fxa/image/upload/v1743872493/virtualbox-machine-summary_sxtgpk.png)

## Step 4: Configure virtual machine settings

1\. Click on the "**Settings**" button at the top of the window.

![VirtualBox interface showing Kali Linux machine](https://res.cloudinary.com/do8uy1fxa/image/upload/v1743872403/virtualbox-interface-showing-new-kali-machine_mgbmkl.png)

2\. On the "**General**" tab, click on "**Advanced**" and change the Shared Clipboard to Bidirectional. This allows you to copy/paste between the host operating system and the virtual machine.

![VirtualBox settings window with the general advanced tab selected](https://res.cloudinary.com/do8uy1fxa/image/upload/v1743872469/virtualbox-kali-linux-machine-settings-general_j69jyn.png)

3\. Navigate to the "**Display**" tab and move the Video Memory slider to the maximum 128MB.

![VirtualBox settings window with the display tab selected](https://res.cloudinary.com/do8uy1fxa/image/upload/v1743872426/virtualbox-kali-linux-machine-settings-display_qk0bxz.png)

## Step 5: Install Kali Linux

1\. Start the virtual machine by clicking on the "**Start**" button.

2\. On the Kali Linux installer menu, choose "**Graphical Install**" and press enter.

![Kali Linux installer menu](https://res.cloudinary.com/do8uy1fxa/image/upload/v1743871910/kali-linux-install-1_yptnxi.png)

3\. Select your language.

![Kali Linux installer select a language](https://res.cloudinary.com/do8uy1fxa/image/upload/v1743871928/kali-linux-install-2_auglmw.png)

4\. Select your location.

![Kali Linux installer select your location](https://res.cloudinary.com/do8uy1fxa/image/upload/v1743871942/kali-linux-install-3_nu2c3v.png)

5\. Choose your keyboard.

![Kali Linux install configure the keyboard](https://res.cloudinary.com/do8uy1fxa/image/upload/v1743871957/kali-linux-install-4_buenr0.png)

6\. Choose a hostname for the device.

![Kali Linux install configure the network - hostname](https://res.cloudinary.com/do8uy1fxa/image/upload/v1743871973/kali-linux-install-5_fzn1vy.png)

7\. For the domain name, you can leave it blank.

![Kali Linux install configure the network - domain name](https://res.cloudinary.com/do8uy1fxa/image/upload/v1743871987/kali-linux-install-6_zuxurm.png)

8\. Enter the full name for the new user.

![Kali Linux install set up users and passwords - full name for the new user](https://res.cloudinary.com/do8uy1fxa/image/upload/v1743872008/kali-linux-install-7_o0icy3.png)

9\. Choose a username for your account.

![Kali Linux install set up users and passwords - username for your account](https://res.cloudinary.com/do8uy1fxa/image/upload/v1743872027/kali-linux-install-8_bkyext.png)

10\. Set an account password.

![Kali Linux install set up users and passwords - choose a password for the new user](https://res.cloudinary.com/do8uy1fxa/image/upload/v1743872045/kali-linux-install-9_pfglei.png)

11\. Select your time zone.

![Kali Linux install configure the clock](https://res.cloudinary.com/do8uy1fxa/image/upload/v1743872064/kali-linux-install-10_vsvfyg.png)

12\. For the partitioning method, choose "**Guided - use entire disk**".

![Kali Linux install partition disks - partitioning method](https://res.cloudinary.com/do8uy1fxa/image/upload/v1743872083/kali-linux-install-11_pvfkt5.png)

13\. Select the disk to partition.

![Kali Linux install partition disks - select disk to partition](https://res.cloudinary.com/do8uy1fxa/image/upload/v1743872108/kali-linux-install-12_bjk7ql.png)

14\. For the partitioning scheme, choose "**All files in one partition (recommended for new users)**".

![Kali Linux install partition disks - partitioning scheme](https://res.cloudinary.com/do8uy1fxa/image/upload/v1743872129/kali-linux-install-13_kbnbiw.png)

15\. Select "**Finish partitioning and write changes to disk**".

![Kali Linux install partition disks - overview of partitions](https://res.cloudinary.com/do8uy1fxa/image/upload/v1743872150/kali-linux-install-14_umjrig.png)

16\. Choose "**Yes**" to write the changes to disks.

![Kali Linux install partition disks - write the changes to disks](https://res.cloudinary.com/do8uy1fxa/image/upload/v1743872170/kali-linux-install-15_yiq8qy.png)

17\. For the software selection, leave the selections as default.

![Kali Linux install software selection](https://res.cloudinary.com/do8uy1fxa/image/upload/v1743872233/kali-linux-install-16_qhtomt.png)

18\. Choose "**Yes**" to install the GRUB boot loader.

![Kali Linux install - install the GRUB boot loader to your primary drive](https://res.cloudinary.com/do8uy1fxa/image/upload/v1743872257/kali-linux-install-17_fzgqfv.png)

19\. Select the device to install the GRUB boot loader.

![Kali Linux install - install the GRUB boot loader - device for boot loader installation](https://res.cloudinary.com/do8uy1fxa/image/upload/v1743872281/kali-linux-install-18_jixg1v.png)

20\. Once the installation is finished, click Continue to reboot.

![Kali Linux install finish the installation](https://res.cloudinary.com/do8uy1fxa/image/upload/v1743872301/kali-linux-install-19_ipt7jh.png)

21\. Enter your username and password to login.

![Kali Linux login page](https://res.cloudinary.com/do8uy1fxa/image/upload/v1743872325/kali-linux-login_qhwxgz.png)

22\. You've now successfully installed Kali Linux on VirtualBox.

![Kali Linux desktop](https://res.cloudinary.com/do8uy1fxa/image/upload/v1743871874/kali-linux-desktop_qnygrl.png)