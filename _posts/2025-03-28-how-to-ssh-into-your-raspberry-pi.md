---
title: How to SSH into your Raspberry Pi
date: 2025-03-28 11:00 PM
categories: [Raspberry Pi]
tags: [raspberry pi, ssh]
---

SSH is a network protocol used to establish a secure remote connection between two devices. This is useful because it lets you remotely access and control your Raspberry Pi without needing a monitor, keyboard, or mouse. In this post, I will walk you through the steps on how to SSH into your Raspberry Pi.

## Step 1: Enable SSH
The first step is to enable SSH. This can be done using the Raspberry Pi Imager or on the Raspberry Pi.

### Enable SSH using the Raspberry Pi Imager
1\. Open the Raspberry Pi Imager.

2\. Choose your device, operating system, and storage, then click next.

![Raspberry Pi Imager interface](https://res.cloudinary.com/do8uy1fxa/image/upload/v1743007314/raspberry-pi-imager-interface_fo8itn.png)

3\. Click **Edit Settings** on the pop-up menu.

![Raspberry Pi Imager Use OS customization? pop-up window](https://res.cloudinary.com/do8uy1fxa/image/upload/v1743007248/raspberry-pi-imager-apply-customization_sz2ttc.png)

4\. On the General tab, fill out the relevant fields.

![Raspberry Pi Imager OS customization window with General tab selected](https://res.cloudinary.com/do8uy1fxa/image/upload/v1743007271/raspberry-pi-imager-customization-general_lnxjr2.png)

5\. Navigate to the Services tab and select **Enable SSH**.

![Raspberry Pi Imager OS customization window with Services tab selected](https://res.cloudinary.com/do8uy1fxa/image/upload/v1743007293/raspberry-pi-imager-customization-services_rcikee.png)

### Enable SSH on the Raspberry Pi
1\. On the Raspberry Pi desktop, go to the main menu and select Preferences > Raspberry Pi Configuration.

2\. Navigate to the Interfaces tab and enable SSH.

![Raspberry Pi Configuration menu with SSH enabled](https://res.cloudinary.com/do8uy1fxa/image/upload/v1743007094/pi-os-configuration-window-ssh-enabled_vjp7yj.png)

## Step 2: Find the Raspberry Pi's IP Address
You can find out your Raspberry Pi's IP Address by using one of the following methods: 

1\. Running the command `ifconfig` on the Raspberry Pi.

or

2\. Pinging the Raspberry Pi using its hostname by running the command `ping [hostname]`.

![Pinging Raspberry Pi using hostname](https://res.cloudinary.com/do8uy1fxa/image/upload/v1743007075/command-prompt-ping-raspberry-pi_m1j0cc.png)

## Step 3: SSH into Raspberry Pi
We're now ready to SSH into the Raspberry Pi.

### SSH into Raspberry Pi on Mac/Linux
On Mac or Linux, open a terminal and run the command: 

`ssh [username]@[hostname]`

or 

`ssh [username]@[ip address]`

### SSH into Raspberry Pi on Windows
On Windows you will need an SSH client. In this example we will be using Putty.

1\. Download Putty from [putty.org](https://www.putty.org/){:target="_blank"}.

![Screenshot of putty.org](https://res.cloudinary.com/do8uy1fxa/image/upload/v1743007131/putty.org-screenshot_iwwbyq.png)

2\. Open Putty.

3\. Enter the Raspberry Pi's hostname or IP Address, make sure the connection type is set to SSH, then click open.

![Putty connection interface](https://res.cloudinary.com/do8uy1fxa/image/upload/v1743007152/putty-connection-interface_d5ivet.png)

4\. You may receive a warning about the server's host key not being cached. Click yes.

5\. Enter the username and password for your Raspberry Pi and press enter.

![Entering Raspberry Pi's credentials in Putty terminal](https://res.cloudinary.com/do8uy1fxa/image/upload/v1743007187/putty-terminal-login_h1orev.png)

6\. You should now be logged into your Raspberry Pi.

![Putty terminal logged into Raspberry Pi as user Pi](https://res.cloudinary.com/do8uy1fxa/image/upload/v1743007221/putty-terminal-ssh-connection-established_gdkxfe.png)

7\. Once you're done, you can close the session by typing `exit`.