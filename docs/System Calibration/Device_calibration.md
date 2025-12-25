---
layout: default
title: Device Calibration
parent: System Calibration
nav_order: 3
description: "Step-by-step guide to calibrate an AR51 VR device so all devices share a common coordinate system."
---

# Device Calibration 
{: .no_toc }

Each VR device initially uses its own coordinate origin. Device calibration aligns those coordinates to the server’s global coordinate system so all clients agree on position and orientation.
{: .fs-6 .fw-300 }



---
## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}
## Locate the server IP 
To perform device calibration you need to enter the web-based management system of the server.

You can find the ip on the server’s GUI top left corner.
![1.finding_oms_ip.png](/assets/images/device_calibration/1.finding_oms_ip.png)

Note that the ip displayed in the image "192.168.0.197" is probably different from yours.
{: .warning }

## Open the AR51 Management System in a Browser
Enter the IP of the server in your browser.
Using the web interface, you can monitor the system and activate the calibration process.
![2.open_browser.png](/assets/images/device_calibration/2.open_browser.png)

## Inside VR: Open an application on a device that has the AR51 SDK
In Oculus Quest, "Developer apps" are usually located under “unknown sources” inside the oculus quest
![3.unkown_sources_quest.gif](/assets/images/device_calibration/3.unkown_sources_quest.gif)

Once the app is open on the device, you should see the device on the devices panel.

## Select your device on the AR51’s web-based management system and start calibration
1. Select the device you wish to calibrate from the device panel.
2. You should see a blue box that indicates that the device was selected.
3. Press the **“Device Calibration”** button in the management system.

![4.device_calibration_selected.png](/assets/images/device_calibration/4.device_calibration_selected.png)


## Calibrate the device

### While in the VR application, lift both your hands so they are fully visible to the device’s cameras
The VR device should see your hands.
It is best if your hands are in front, between chest and head high.
![5.device_calibration_hands.gif](/assets/images/device_calibration/5.device_calibration_hands.gif)

### Move slowly across the capture area while moving your hands

Do not wave your hands too fast. Move them at a relaxed speed. \
Moving too fast can produce poor calibration quality.
{: .warning }

![6.device_calibration_screen.gif](/assets/images/device_calibration/6.device_calibration_screen.gif)

### Character should "snap" onto your body (in VR)
You should see the character “snap” into place after a short while. 
This does not mean the calibration is over. 
You should still move around the capture area to improve the calibration.
![7.device_calibration_within_quest.gif](/assets/images/device_calibration/7.device_calibration_within_quest.gif)

