---
layout: default
title: Ubuntu Installation
nav_order: 3
---

# Installing Ubuntu with Pre-Configured AR51 Mocap Unleash

{: .no_toc }

This guide covers installing the Ubuntu OS with AR51 Moca Unleash software already pre-installed and configured.
{: .fs-6 .fw-300 }

---
## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}


## Prerequisites
Make sure you have the pre-configured Ubuntu installation file downloaded.

## Prepare for Installation
1. Connect the computer to the internet to download updates during the installation process.
2. Ensure you have a USB drive or other media to install Ubuntu.
3. If you do not have a usb-install:
   - Download our custom ubuntu 22 ISO from our files server.
   - Use a sofware like [etcher](https://etcher.balena.io/) to burn the ISO to a usb flash-drive.

## Start the Installation Process
1. Boot your computer from the installation media. Then, choose "Try or Install Ubuntu"
![install 1 - choose try or install.png](/assets/images/installation/install%201%20-%20choose%20try%20or%20install.png)
2. Once the installation loads, choose "Install AR51".
![install 2 - choose install.png](/assets/images/installation/install%202%20-%20choose%20install.png)

## Configure Installation Options
1. When prompted, select "Install Ubuntu."
2. Connect to the internet when asked so it can download updates.
3. On the top left corner you should see a network icon. Make sure the computer is connected to the network before continue to the next step.
![install 3 - make sure the network is connected.png](/assets/images/installation/install%203%20-%20make%20sure%20the%20network%20is%20connected.png)
If the computer is not connected to the internet, it will not be able to get recent updates. And some functionality may be hindered. 
{: .warning }

4. Make sure both "Download updates" and "Install third-party software..." options are checked. This ensures that necessary drivers and codecs are installed.
![install 4 - choose both download and third party graphics.png](/assets/images/installation/install%204%20-%20choose%20both%20download%20and%20third%20party%20graphics.png)

## Complete the Installation
1. Follow the remaining prompts to complete the installation process.
![install 5 - progress bar.png](/assets/images/installation/install%205%20-%20progress%20bar.png)
2. Once the installation finishes, the computer will prompt a restart request. Approve it, and remove the ubuntu installation disk when prompted. 
![install 7 - on first login enter the password.png](/assets/images/installation/install%207%20-%20on%20first%20login%20enter%20the%20password.png)

## First Login
1. After the system boots, enter your user name and password to login.
2. Once logged-in, you should see a terminal window. Enter your password to complete the installation process.

## Configure the Network Interfaces
1. You should set the ip, and subnet of all the network interfaces that are connected to the cameras.
2. First, open network interface settings by clicking on the network icon on the top left corner.
   ![install 8 - enter network configuration.png](/assets/images/installation/install%208%20-%20enter%20network%20configuration.png)
3. You will need to edit all interfaces that point to each camera (only once if you use a switch)
   ![install 9 - edit each network interface.png](/assets/images/installation/install%209%20-%20edit%20each%20network%20interface.png)
4. For each interface perform these two steps:
5. On the "identity" tag, set the MTU to 9000
      ![install 10 - set the MTU.png](/assets/images/installation/install%2010%20-%20set%20the%20MTU.png)
6. On the IPV4 tag configure the IP and the subnet for each interface.
      ![install 11 - set the ip and subnet.png](/assets/images/installation/install%2011%20-%20set%20the%20ip%20and%20subnet.png)

7. The network configure can vary depending on the site constrains. Usually we recommend the following convention:
   The ip of the interface should be 169.254.X.1 where X is a running interface ID. The subnet should be 255.255.255.0

Do not configure a default gateway for these cameras. The camera should be in a closed loop/closed network.
{: .warning }

In most cases the interface that is connected to the internet (external network) should not be set.

If you change the network interface that is pointing outside it may disable your internet connection.
{: .warning }

8. Once completed, to apply the changes disable and enable the interface.

## Set the license key and provide the machine signature
1. Open Mocap Unleashed app from the desktop icon "Start AR51..." .
![install - Start AR51.png](/assets/images/installation/install%20-%20Start%20AR51.png)
2. Open the settings tab, and enter the provided license key,
![install 12 - enter license.png](/assets/images/installation/install%2012%20-%20enter%20license.png)

If you did not receive a license key, contact AR51 staff.
{: .warning }

3. The system should now prompt the "machine fingerprint", report the fingerprint to AR51 staff.
Each license is looked per machine. If you re-install the computer it might change the fingerprint.
{: .warning }

If the fingerprint does change, contact AR51 staff to re-activate your machine.
![install 13 - fingerprint warning.png](/assets/images/installation/install%2013%20-%20fingerprint%20warning.png)

## Provide Remote Access for Testing
1. We recommend using AnyDesk for remote access.
2. Provide the AnyDesk access code to your support representative.

## Done
Your pre-configured AR51 Ubuntu installation is complete. 
