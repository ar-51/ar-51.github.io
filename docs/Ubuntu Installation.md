---
layout: default
title: Ubuntu Installation
nav_order: 3
---

# Installing Ubuntu with Pre-Configured AR51 Mocap Unleash

{: .no_toc }

This guide explains how to install the Ubuntu OS with the AR51 Mocap Unleash software pre-installed and configured.
{: .fs-6 .fw-300 }

---
## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}


## Prerequisites
Downloading the Pre-Configured Ubuntu Installation File
1. Access the AR51 Files Page:
2. Open your web browser and go to [https://files.ar-51.com](https://files.ar-51.com)
3. Locate the Ubuntu Installation File.
![install download ubuntu-ar51](/assets/images/installation/ubunut_on_website.png)
4. Click the download link for the installation file and save it to your computer.


## Prepare for Installation
### Create a Bootable USB Drive:
Use a sofware like [etcher](https://etcher.balena.io/) to burn the ISO to a usb flash-drive.

### Ensure you have a USB drive or other media 
Make sure you have a USB drive or another medium available for installing Ubuntu

### Make sure the computer is connected to the internet
Ensure the computer is connected to the internet to download updates during the installation process.


## Start the Installation Process
### Step-by-Step Guide:
1. Insert the USB drive or installation media into the computer.
2. Boot your computer from the installation media.
3. Once the system boots from the media, select "Try or Install Ubuntu"
![install 1 - choose try or install.png](/assets/images/installation/install%201%20-%20choose%20try%20or%20install.png)
4. When the installation screen appears, select "Install AR51".
![install 2 - choose install.png](/assets/images/installation/install%202%20-%20choose%20install.png)

## Configure Installation Options
1. When prompted, select "Install Ubuntu."
2. Choose Your Preferred Language
![install 2 - choose lang.png](/assets/images/installation/choose_lang.png)
3. Connect to the internet when prompted to allow Ubuntu to download updates.
4. In the top-left corner, you should see a network icon. Ensure the computer is connected to the network before proceeding to the next step.
![install 3 - make sure the network is connected.png](/assets/images/installation/install%203%20-%20make%20sure%20the%20network%20is%20connected.png)

 If the computer is not connected to the internet, it will be unable to download updates, which may affect system functionality.
{: .warning }
5. Check both "Download updates" and "Install third-party software..." to ensure the necessary drivers and codecs are installed.
![install 4 - choose both download and third party graphics.png](/assets/images/installation/install%204%20-%20choose%20both%20download%20and%20third%20party%20graphics.png)
6. Choose the appropriate installation type based on your setup:
    1. If using a clean disk, select "Erase disk and install Ubuntu."
    2. If creating a custom partition, select "Something else" and configure your partitions accordingly.
![install 5 - choose disk install type](/assets/images/installation/install_type.png)
7. Select your location to set the time zone and click "Continue."
![install 6 - choose time zone](/assets/images/installation/time_zone.png)
8. Enter your name, computer name, and create a secure password. Then, click "Continue."
![install 6 - choose time zone](/assets/images/installation/user.png)

## Complete the Installation
1. Follow the on-screen prompts to complete the installation process.
![install 5 - progress bar.png](/assets/images/installation/install%205%20-%20progress%20bar.png)
2. Once the installation is finished, the system will prompt you to restart. Approve the restart and remove the installation media when prompted. 
![install 7 - on first login enter the password.png](/assets/images/installation/install%207%20-%20on%20first%20login%20enter%20the%20password.png)

## First Login
1. After the system boots, enter your username and password to log in.
2. Once logged in, a terminal window should appear. Enter your password when prompted to complete the installation process.
3. When this process is done, you should see a change to the user wallpaper.

## Configure the Network Interfaces
1. Set the IP address and subnet for **all** network interfaces connected to the cameras.
2. First, open the network interface settings by clicking on the network icon in the top-left corner.
   ![install 8 - enter network configuration.png](/assets/images/installation/install%208%20-%20enter%20network%20configuration.png)
3. Edit **all** interfaces that connect to cameras (only once if using a switch).
   ![install 9 - edit each network interface.png](/assets/images/installation/install%209%20-%20edit%20each%20network%20interface.png)
4. For each interface, complete the following steps:
5. Under the **"Identity"** tab, set the **MTU** to **9000**.
      ![install 10 - set the MTU.png](/assets/images/installation/install%2010%20-%20set%20the%20MTU.png)
6. Under the **"IPv4"** tab, configure the IP **Address** and **Netmask**.
      ![install 11 - set the ip and subnet.png](/assets/images/installation/install%2011%20-%20set%20the%20ip%20and%20subnet.png)

7. Network configuration may vary based on site constraints. We generally recommend the following convention:
   * The IP address should follow the format **169.254.X.1**, where **X** is a unique interface ID.
   * The subnet should be **255.255.255.0** .

**Do not** configure a default gateway for these cameras. The cameras should be in a closed-loop/isolated network.
{: .warning }

In most cases, the interface connected to the internet (external network) should remain unconfigured.

Changing the network interface connected to the internet may disrupt your connection.
{: .warning }

8. Once completed, **disable and re-enable** all network interfaces to make the changes take into effect.
![restart_network_interface.png](/assets/images/installation/restart_network_interface.png)


## Set the license key and provide the machine signature
1. Open the **Mocap Unleashed** application using the desktop icon **"Start AR51..."** .
![install - Start AR51.png](/assets/images/installation/install%20-%20Start%20AR51.png)
2. Navigate to the Settings tab and enter the provided license key.
![install 12 - enter license.png](/assets/images/installation/install%2012%20-%20enter%20license.png)

If you did not receive a license key, contact AR51 support.
{: .warning }

3. The system will display a **"Machine Fingerprint"**. Share this fingerprint with AR51 support.

Each license is locked to a specific machine. If you reinstall the operating system, the fingerprint may change.
{: .warning }

 If the fingerprint changes, contact AR51 support to reactivate your machine. 

 ![install 13 - fingerprint warning.png](/assets/images/installation/install%2013%20-%20fingerprint%20warning.png)

## Provide Remote Access for Testing
1. We recommend using **AnyDesk** for remote access.
2. Provide the **AnyDesk access-code** to your support representative.

## Done
Your pre-configured AR51 Ubuntu installation is complete. 
