---
layout: default
title: Camera Calibration
parent: System Calibration
nav_order: 1
---

# Camera Calibration 
{: .no_toc }

Before activating the system, the system needs to be calibrated.
{: .fs-6 .fw-300 }

The calibration has two steps:
{: .fs-6 .fw-300 }
1. Calibration board detection.
2. Lit calibration sphere detection.
{: .fs-6 .fw-300 }



---
## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

## Open the AR51 management system in a browser
Using the web interface you can monitor the system and activated the calibration process.

![oms](/assets/images/oms.png)

## Camera check
Check that all cameras appear and that the feed from each camera works.
{: .warning }

Use can use the feed to check that all cameras are pointing to the capture area. \
And, that there is good coverage of the area.

Poor coverage can lead to poor capture quality.
{: .warning }

## Place the provided calibration board
Place the provided calibration board in the middle of the capture area and make sure that is fully visible by as many cameras as possible.

## Start the camera calibration

### Open at least one camera feed
The feed from the camera should reflect the various stages in the calibration process.

### Click on the “Start Cam Calibration” button
Once the calibration board detection is completed the images in the camera feed will turn darker.

![start camera calibration](/assets/images/start_camera_calibration.png)

### Switch on the calibration sphere
Once the feed goes dark, switch on the provided calibration sphere.

Make sure your light bulb emits a strong white light. Using yellow, warm light can result with a bad calibration score.
{: .warning }

### Move around the room holding the calibration sphere
Do not run while holding the sphere.\
 Make sure you move around the entire capture area.\
 Try to vary the height of the calibration sphere.\
 Variation in height means a better quality.
{: .warning }

Use the progress bar in the management system to monitor the progress of the calibration.

## Monitor the progress in Mocap Studio

You can use “Mocap Studio” to view the movement of the ball in 3D

Once the calibration is completed you can view the 3D avatars in “Mocap Studio”.
