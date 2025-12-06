---
title: How to install Windows 11 on Proxmox
date: 2025-10-20 12:00 PM
categories: [Proxmox]
tags: [proxmox, windows 11]
---

This post will provide you with a step-by-step guide on how to install Windows 11 on Proxmox. When installing Windows 11 on Proxmox, you'll need the VirtIO drivers. You should also keep in mind the minimum system requirements for Windows 11. The system requirements for Windows 11 can be found on Microsoft's official website [here](https://www.microsoft.com/en-us/windows/windows-11-specifications){:target="_blank"}.

## Step 1: Download Windows 11 and VirtIO drivers ISO images

1\. Download the Windows 11 ISO from [https://www.microsoft.com/en-us/software-download/windows11](https://www.microsoft.com/en-us/software-download/windows11){:target="_blank"}.

![Windows 11 download page](https://res.cloudinary.com/do8uy1fxa/image/upload/v1760719268/windows-11-download-page_rgjelh.png)

2\. Download the VirtIO drivers ISO from [https://pve.proxmox.com/wiki/Windows_VirtIO_Drivers](https://pve.proxmox.com/wiki/Windows_VirtIO_Drivers){:target="_blank"} by clicking on **download the most recent** under the **Installation** section.

![VirtIO drivers download page](https://res.cloudinary.com/do8uy1fxa/image/upload/v1760719226/virtio-drivers-download-page_aks5ot.png)

## Step 2: Upload ISO images to Proxmox

1\. Upload the Windows 11 and VirtIO drivers ISO images to Proxmox by clicking the node > local storage > ISO Images > Upload.

![Proxmox ISO image upload window](https://res.cloudinary.com/do8uy1fxa/image/upload/v1760719208/upload-iso-images_p3h1be.png)

## Step 3: Create Windows 11 VM

1\. To create a new VM in the Proxmox dashboard, select the appropriate node and click on **Create VM** in the top right corner.

2\. On the **General** tab, assign the virtual machine a VM ID (you can leave it as default if you want) and a name.

![Proxmox create virtual machine window General tab](https://res.cloudinary.com/do8uy1fxa/image/upload/v1760718666/create-windows-11-vm-1_i9xwfg.png)

3\. On the **OS** tab, select the Windows 11 ISO from the **ISO image** dropdown menu. Next, under **Guest OS**, select **Microsoft Windows** for **Type** and **11/2022/2025** for **Version**. Finally, check the box for **Add additional drive for VirtIO drivers** and select the VirtIO drivers ISO from the **ISO image** dropdown menu.

![Proxmox create virtual machine window OS tab](https://res.cloudinary.com/do8uy1fxa/image/upload/v1760718681/create-windows-11-vm-2_vdxw0p.png)

4\. On the **System** tab, check the box for **Add TPM**, then select the appropriate storage location for **TPM Storage** and select **v2.0** for **Version**. Lastly, make sure **OVMF (UEFI)** is selected for **BIOS**.

![Proxmox create virtual machine window System tab](https://res.cloudinary.com/do8uy1fxa/image/upload/v1760718693/create-windows-11-vm-3_gw5yop.png)

5\. For the **Disks** tab, choose a disk size under **Disk size (GiB)**. Keep in mind that Windows 11 requires a minimum of 64GB of storage space.

![Proxmox create virtual machine window Disks tab](https://res.cloudinary.com/do8uy1fxa/image/upload/v1760718709/create-windows-11-vm-4_s7m0hv.png)

6\. On the **CPU** tab, assign the desired number of cores. Keep in mind that Windows 11 requires a minimum of 2 cores.

![Proxmox create virtual machine window CPU tab](https://res.cloudinary.com/do8uy1fxa/image/upload/v1760718721/create-windows-11-vm-5_dx5zkj.png)

7\. For the **Memory** tab, assign the desired amount of RAM. Keep in mind that Windows 11 requires a minimum of 4GB of RAM.

![Proxmox create virtual machine window Memory tab](https://res.cloudinary.com/do8uy1fxa/image/upload/v1760718735/create-windows-11-vm-6_o6drop.png)

8\. You can leave everything as default on the **Network** tab.

![Proxmox create virtual machine window Network tab](https://res.cloudinary.com/do8uy1fxa/image/upload/v1760718749/create-windows-11-vm-7_ypl8lj.png)

9\. After reviewing everything on the **Confirm** tab, click **Finish**.

![Proxmox create virtual machine window Confirm tab](https://res.cloudinary.com/do8uy1fxa/image/upload/v1760718762/create-windows-11-vm-8_z58n9x.png)

## Step 4: Install Windows 11

1\. Start the Windows 11 VM by selecting it on the sidebar, selecting **Console**, and clicking **Start Now**.

![Proxmox dashboard showing the Windows 11 VM console](https://res.cloudinary.com/do8uy1fxa/image/upload/v1760719188/start-windows-11-vm_yxvime.png)

2\. Select your language.

![Windows 11 installation Select language settings screen](https://res.cloudinary.com/do8uy1fxa/image/upload/v1760718837/install-windows-11-1_ba7itq.png)

3\. Select your keyboard.

![Windows 11 installation Select keyboard settings screen](https://res.cloudinary.com/do8uy1fxa/image/upload/v1760718856/install-windows-11-2_pd0vcl.png)

4\. Select **Install Windows 11**, and check the box for **I agree everything will be deleted including files, apps, and settings**.

![Windows 11 installation Select setup option screen](https://res.cloudinary.com/do8uy1fxa/image/upload/v1760718873/install-windows-11-3_obapcj.png)

5\. Enter your product key or select **I don't have a product key** if you don't have one.

![Windows 11 installation Product key screen](https://res.cloudinary.com/do8uy1fxa/image/upload/v1760718891/install-windows-11-4_ejhd5a.png)

6\. Select the edition you want to install.

![Windows 11 installation Select Image screen](https://res.cloudinary.com/do8uy1fxa/image/upload/v1760718908/install-windows-11-5_us3nod.png)

7\. Click **Accept**.

![Windows 11 installation Applicable notices and license terms screen](https://res.cloudinary.com/do8uy1fxa/image/upload/v1760718927/install-windows-11-6_uhnhd4.png)

8\. Click **Load Driver**.

![Windows 11 installation Select location to install Windows 11 screen](https://res.cloudinary.com/do8uy1fxa/image/upload/v1760718947/install-windows-11-7_d8jt2l.png)

9\. Click on **Browse**, then select This PC > CD Drive (D:) virtio-win-0.1.285 > amd64 > w11, and click **OK**.

![Windows 11 installation Install driver to show hardware screen](https://res.cloudinary.com/do8uy1fxa/image/upload/v1760718966/install-windows-11-8_iu8fdg.png)

10\. Highlight the **Red Hat VirtIO SCSI pass-through controller** driver and click **Install**.

![Windows 11 installation Install driver to show hardware screen with driver highlighted](https://res.cloudinary.com/do8uy1fxa/image/upload/v1760718987/install-windows-11-9_snnnyi.png)

11\. Highlight the Disk and click **Next**.

![Windows 11 installation Select location to install Windows 11 screen with Disk highlighted](https://res.cloudinary.com/do8uy1fxa/image/upload/v1760719006/install-windows-11-10_pb7mib.png)

12\. Click **Install**.

![Windows 11 installation Ready to install screen](https://res.cloudinary.com/do8uy1fxa/image/upload/v1760719026/install-windows-11-11_xoy6wl.png)

13\. After the installation is complete, you'll see this screen. Then, select your country or region.

![Windows 11 installation Is this the right country or region? screen](https://res.cloudinary.com/do8uy1fxa/image/upload/v1760719044/install-windows-11-12_u9yste.png)

14\. Select your keyboard layout.

![Windows 11 installation Is this the right keyboard layout or input method? screen](https://res.cloudinary.com/do8uy1fxa/image/upload/v1760719062/install-windows-11-13_zaf2bj.png)

15\. Next, you can add a second keyboard layout or select **Skip**.

![Windows 11 installation Want to add a second keyboard layout? screen](https://res.cloudinary.com/do8uy1fxa/image/upload/v1760719083/install-windows-11-14_yn6tpu.png)

16\. On the **Let's connect you to a network** screen, press `Shift + F10` on your keyboard to open a command prompt. In the command prompt, type `start ms-cxh:localonly` and press enter. This command will cause a pop-up window to appear that will allow you to create a local user account so you don't have to sign in with a Microsoft account.

![Windows 11 installation Let's connect you to a network screen with command prompt window](https://res.cloudinary.com/do8uy1fxa/image/upload/v1760719102/install-windows-11-15_vg0wo6.png)

17\. In the pop-up window, enter the information to create a local user account.

![Windows 11 installation Microsoft account Create a user for this PC pop-up window](https://res.cloudinary.com/do8uy1fxa/image/upload/v1760719122/install-windows-11-16_yxbc1z.png)

18\. Choose your privacy settings.

![Windows 11 installation Choose privacy settings for your device screen](https://res.cloudinary.com/do8uy1fxa/image/upload/v1760719141/install-windows-11-17_ivpesu.png)

19\. The installation and setup is now complete.

![Screenshot of Windows 11 desktop](https://res.cloudinary.com/do8uy1fxa/image/upload/v1760719246/windows-11-desktop_hc7kol.png)

## Step 5: Post-installation configuration

1\. The next step is to update drivers to enable internet access. To do this, right-click the Windows 11 Start menu icon and select **Device Manager**.

![Windows 11 desktop with Device Manager open](https://res.cloudinary.com/do8uy1fxa/image/upload/v1760718776/device-manager_uewz6b.png)

2\. Navigate to **Other devices**, right-click **Ethernet Controller**, and select **Update Driver**. Next, select **Browse my computer for drivers**. On the next page, click **Browse**, and navigate to CD Drive (D:) virtio-win-0.1.285 > NetKVM > w11 > amd64. Finally, click OK > Next, then close the window.

![Windows 11 desktop with Device Manager Browse for drivers window open](https://res.cloudinary.com/do8uy1fxa/image/upload/v1760718819/device-manager-update-drivers_kudwku.png)

3\. The **Red Hat VirtIO Ethernet Adapter** should appear under **Network adapters** in Device Manager.

![Windows 11 desktop with Device Manager open and Network adapters highlighted](https://res.cloudinary.com/do8uy1fxa/image/upload/v1760718802/device-manager-network-adapters_iwlflc.png)

4\. You should now have internet access.

![Windows 11 desktop with Microsoft Edge open showing google.com](https://res.cloudinary.com/do8uy1fxa/image/upload/v1760719163/internet-connection-test_sbl6r9.png)

5\. Finally, check Windows Update for any needed updates.

![Windows 11 desktop with Windows Update open](https://res.cloudinary.com/do8uy1fxa/image/upload/v1760718651/check-windows-update_dwdxgr.png)