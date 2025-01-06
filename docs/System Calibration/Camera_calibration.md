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

## Open the AR-51 Management System in a Browser
Using the web interface, you can monitor the system and activate the calibration process.

![oms](/assets/images/camera_calibration/1.oms.png)

## Camera check
Check if all the  cameras appear and if that the feed from each camera works.
{: .warning }

Ensure all cameras are pointing to the capture area and there is good coverage.

Poor coverage can lead to poor capture quality.
{: .warning }

You can use the feed to check that all cameras are pointing to the capture area. \
And, that there is good coverage of the area.

![2.camera_feed_check.png](/assets/images/camera_calibration/2.camera_feed_check.png)

## Place the provided calibration board
Place the provided calibration board in the middle of the capture area.\
Make sure the calibration board is fully visible to as many cameras as possible.
![3calibration_board_placement.png](/assets/images/camera_calibration/3calibration_board_placement.png)

## Start the camera calibration

### Open at least one camera feed
The feed from the camera should reflect the various stages in the calibration process.

### Click on the “Start Cam Calibration” button
1. Open Mocap Studio and navigate to the Calibration menu on the top left corner.
2. Select "Start Calibration" to activate the calibration process.

![4.start_cam_calibration.png](/assets/images/camera_calibration/4.start_cam_calibration.png)

Once the calibration board detection is completed, the images in the camera feed will turn darker.

### Switch on the calibration sphere
Once the feed goes dark, switch on the provided calibration sphere.

Make sure your light bulb emits **a strong white light (at least 1800 lumen)**. Using yellow, warm light can result with a bad calibration score.
{: .warning }
![5.calibration_sphere](/assets/images/camera_calibration/5.calibration_sphere.png)

### Move around the room holding the calibration sphere
1. Begin moving the calibration sphere around the room, covering as much ground as possible, including **varying heights and positions**. This helps in gathering a comprehensive set of data points.
2. Be thorough and systematic. Cover all areas of the room, including corners and elevated spots.
3. Frequently change the orientation of the calibration sphere to ensure diverse data points for better accuracy.

#### Important Tips:
1. Do not run while holding the sphere.
2. Ensure you move around the entire capture area.
3. Vary the height of the calibration sphere for better quality calibration.

## Monitor the progress in Mocap Studio

You can use “Mocap Studio” to view the movement of the ball in 3D. \
Use the progress bar in the management system to monitor the progress of the calibration.
![6.calib_sphere_path.gif](/assets/images/camera_calibration/6.calib_sphere_path.gif)
![7.cam_view.gif](/assets/images/camera_calibration/7.cam_view.gif)

## Validate in Mocap Studio
Once the calibration is completed, you can view the 3D avatars in “Mocap Studio”.
![8.calibration_done.png](/assets/images/camera_calibration/8.calibration_done.png)
