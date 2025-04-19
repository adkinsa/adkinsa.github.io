---
title: Installing CasaOS on my Raspberry Pi 5
date: 2025-04-18 10:00 PM
categories: [Raspberry Pi]
tags: [raspberry pi, casaos]
---

One of my goals for this year is to invest more time and effort into homelabbing and learning new technologies. These blog posts are a way for me to document my learning journey and share some of my knowledge and experience to help others on their own learning journeys. In some of my recent posts, I shared about the addition of my Raspberry Pi 5 to my homelab. With the Raspberry Pi all set up and running, the next thing I needed to do was figure out what I wanted to do with it.

After looking into various alternatives for self-hosting on the Raspberry Pi, I decided to give **CasaOS** a try. CasaOS is software that runs on top of your host operating system and provides a user-friendly interface for managing Docker applications. It also comes with a built-in app store with a bunch of applications to choose from, as well as an option to manually install applications using Docker images.

## Installing CasaOS
The first thing I did was go to the CasaOS website at [https://casaos.zimaspace.com/](https://casaos.zimaspace.com/){:target="_blank"}.

![Screenshot of casaos.zimaspace.com landing page](https://res.cloudinary.com/do8uy1fxa/image/upload/v1744852048/casaos-website_fs5gvz.png)

Next, I copied and pasted the curl command `curl -fsSL https://get.casaos.io | sudo bash` into the Raspberry Pi's terminal and ran the command.

![CasaOS installing in Raspberry Pi's terminal](https://res.cloudinary.com/do8uy1fxa/image/upload/v1744851981/casaos-install-in-terminal_r5beut.png)

Once the installation was complete, it showed that **CasaOS v0.4.15** was running at `http://192.168.0.33` which is the IP address of the Pi. Next, I opened up a browser and went to the address that was listed. I was then greeted with the CasaOS welcome page and prompted to create an account.

## CasaOS Dashboard
After logging in, I was greeted with the CasaOS dashboard.

![CasaOS dashboard after first login](https://res.cloudinary.com/do8uy1fxa/image/upload/v1744851946/casaos-dashboard_dnsqqh.png)

The dashboard has a very user-friendly interface. One of the nice features of the dashboard is that it displays status indicators for the system, storage, and network. The system status indicator is particularly useful because it shows the percentage of CPU and RAM utilization.

The app store has a variety of applications to choose from that cover a wide range of services and use cases.

![CasaOS app store](https://res.cloudinary.com/do8uy1fxa/image/upload/v1744851925/casaos-app-store_eoovvm.png)

In addition to the app store, it also has the option to manually install applications using Docker images.

![CasaOS manual app install interface](https://res.cloudinary.com/do8uy1fxa/image/upload/v1744852016/casaos-manual-app-install_csring.png)

Another added benefit is that the dashboard comes with a built-in terminal and logs.

![CasaOS logs interface](https://res.cloudinary.com/do8uy1fxa/image/upload/v1744852031/casaos-terminal-and-logs_d4tvfz.png)

## Conclusion
Overall, CasaOS was easy to install, and I'm impressed by its built-in features and the vast number of applications it has to offer in the app store. I'm excited to start experimenting with running different applications and services, and to put the Raspberry Pi to use in my homelab. This will also provide me with the opportunity to learn more about Docker and containerization. As I continue to experiment with CasaOS, I will provide future updates on some of the changes I have made and services I am running. 