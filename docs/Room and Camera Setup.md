---
layout: default
title: Room & Camera Setup 
nav_order: 2
---

# Room & Camera Setup 
{: .no_toc }

This document contains best-practice instructions regarding how to position the cameras
{: .fs-6 .fw-300 }



---
## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}



## Pointers
AR51's Mocap Unleashed system is a multi-camera optical system. 
As an optical system, the system achieves the best result when the room is well lit 
and when the person is not occluded.
To extract the correct pose, two cameras which can see the subject are sufficient.
However, as more cameras observe a body part, the accuracy increases.
This becomes even more critical in challenging scenarios when occlusions occur 
(occlusions by another person, self-made occlusions, or by objects).

## Best practice 
### The room should be well-lit with diffused light
Since this is an optical system, a good camera feed of the viewing area is required.
The system works best when the room is well-lit.
It is also preferable to use diffused lighting and not spotlighting. 
Spot lighting can cause dead areas in the image due to over-exposure from reflective surfaces.

### Cover your area of interest
There are no theoretical constraints on how to place the cameras in the scene.
This means that if there is a certain area in which you know that there will be more occlusion or that you require better accuracy, you can place more cameras in this specific area. 

### Position the cameras around the room to get a decent coverage

For a standard system of 6m by 6m, we recommend:
* Using **8 cameras**.
* Camera height should be between **2.5m to 3m**.
* Place **2 cameras at each corner**.
* Place each camera approximately **0.5 meter from the corner**.
![camera_position](/assets/images/camera_position.png)


### Minimize the capture of dead space
* The camera should look into the distance but not capture too much of the ceiling.
* Try not to point to the ceiling or straight down to the floor. 

### Reduce camera tilt - level the cameras
Try to make the camera as level as much as possible. 
The system works best when the cameras are not tilted.

### Place the camera so they get diverse viewing angles
There is no benefit in placing the camera in the same spot and pointing them in the same direction.
This will cause redundant information and the system will not benefit from it.


## Use Live-Feed from OMS to get a live feedback
Open the oms, and press on a camera - this will show a live feed.

### Use Live-Feed to tune the position & orientation
You can then position the camera using the live feed. 
Once you are satisfied with the position and the orientation of the camera, lock the camera grip.
![oms_camera_feed](/assets/images/oms_camera_feed.png)

### Use the HQ option to view the image in full resolution
To view the image in full resolution, open the oms and press on HQ (top right corner). 
Then, to open a camera, press on the camera icon in the bottom row.
This will show a high-quality live feed (But low fps). 

![oms_HQ](/assets/images/oms_HQ.png)

You can use the high-quality feed to tune the focus dial until the image looks sharp.

### Tune the focus dial on the cameras
Sharper images result in a better-quality capture.
To change the focus of the camera, release the outer-most lock on the camera lens and rotate the dial until the image is sharp.
![oms_HQ](/assets/images/lens.png)





