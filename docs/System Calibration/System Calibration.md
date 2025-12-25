---
layout: default
title: System Calibration
nav_order: 4
has_children: true
permalink: /docs/System Calibration
description: "Overview of AR51’s complete system calibration workflow, including camera calibration, bounding-box setup, VR device alignment, and LED-stage synchronization to ensure accurate multi-device tracking."
---

# System Calibration
Before using the AR51 system, you must complete camera and device calibration to ensure accurate motion capture and synchronized coordinates across all devices. The calibration process includes three main stages:
* Camera Calibration. 
* Define the Bounding box. 
* Device Calibration (VR-Headset Calibration).
{: .fs-6 .fw-300 }

## Camera Calibration
The first step involves setting up and calibrating the cameras to ensure they accurately capture and interpret the physical space. It includes:
* Calibration board detection
* Lit calibration sphere detection
![6.calib_sphere_path.gif](/assets/images/camera_calibration/6.calib_sphere_path.gif)

## Bounding Box Calibration
Next, we will set up the bounding box to define the capture area boundaries. Properly setting up the bounding box ensures that the system accurately interprets the spatial limits within which the performance will be captured. This step focuses on:
* Setting the center and dimensions of the bounding box
* Sending the bounding box data to the server
* Validating the bounding box calibration
![mocap studio bounds validate](/assets/images/4.3BoundingBoxCalibration/5bound_validate.gif)


## VR Device Calibration
Here, we will calibrate the VR devices to ensure they are synchronized and functioning correctly within the capture environment. This includes:
* Ensuring all devices agree on a common coordinate system
* Moving and positioning your hands within the VR environment for accurate tracking

![mocap studio bounds validate](/assets/images/device_calibration/device_calibration_showroom.png)

## LED Stage Synchronization
Here, we will sync between an LED stage coordinate system and AR51's coordinate system by projecting the checkerboard pattern onto the LED floor.

![calibration board on stage.png](/assets/images/led_sync/calibration board on stage.png)  

