---
layout: default
title: Device Calibration
parent: System Calibration
nav_order: 3
---

# Device Calibration 
{: .no_toc }

By default, every device has its own coordinate system.\
 By performing device calibration, all devices agree on a common coordinate system.
{: .fs-6 .fw-300 }



---
## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

## Open the AR51 Management System in a Browser
Using the system web interface, you can monitor the system and activate the calibration process.
Type the OMS/Server IP in the browser url. 
For example, if the server ip is 10.0.0.11 enter it and press Enter.
![device calibration - open browser.png](/assets/images/device%20calibration%20-%20open%20browser.png)

Using the web interface you can monitor the system and activated the calibration process.

![oms](/assets/images/oms.png)

### Open an application on a device that has the AR51 SDK 
Once the app is open on the device, you should see the device on the devices panel. 

## Select a device and start calibration
Select the device you wish to calibrate from the device panel. \
You should see a blue box that indicates that the device was selected.

Press the “Device Calibration” button in the management system.

![device calibration](/assets/images/device_calibration_selected.png)

## Calibrate the device

### While in the VR application, lift both your hands so they are fully visible to the device's cameras
The VR device should see your hands.
It is best if your hands are in front, between chest and head high.

### Move slowly across the capture area while moving your hands

Do not wave your hands too fast. Move them at a relaxed speed. \
Moving too fast can produce poor calibration quality.
{: .warning }

### Character should "snap" onto your body (in VR)
You should see the character “snap” into place after a short while. 
This does not mean the calibration is over. 
You should still move around the capture area to improve the calibration.

### You can monitor the progress in the management system
