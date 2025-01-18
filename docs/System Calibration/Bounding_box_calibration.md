---
layout: default
title: Defining the Active Area - Bounding Box Calibration
parent: System Calibration
nav_order: 2
---

# Define Your Active Region Using Bounding-Box Calibration in Mocap Studio
{: .no_toc }

Bounding box calibration is used to define the capture area within which motion is recorded. This ensures that the system focuses on a specific space, optimizing performance and accuracy by ignoring irrelevant movements outside this area. 
{: .fs-6 .fw-300 }

It is crucial for scenarios where space is limited or where multiple activities occur simultaneously.
{: .fs-6 .fw-300 }

---
## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

## Open Mocap Studio and Locate the Bound Properties
On a laptop that is connected to the same network as the system, open Mocap Studio.
Ensure your computer (laptop or desktop) is connected to the same local network as the system, open Mocap Studio.

If the computer is not in the same network, it will not be able to connect to the system.
{: .warning }

In Mocap Studio, scroll down in the properties panel on the right side and find the section called "Bounds".

![mocap studio](/assets/images/4.3BoundingBoxCalibration/1bounding_box_location.png)

## Show the current bounds
Click on "Show Bounds" to display the current bounds.
![mocap studio selection menu](/assets/images/4.3BoundingBoxCalibration/2bounding_box_example.png)

## Set the center and the dimensions
This step focuses the bounding box on the desired area, ignoring movements outside the box.

Set the center and dimensions (width, height, depth in meters) of the bounding box ("cage") to define the capture area (e.g., 2x2x3 meters). 

You can set the bounds in two ways:
1. By writing the numerical values inside the panel.
2. By dragging the bounds manually using the left mouse button, in the main panel.
![mocap studio set bounds](/assets/images/4.3BoundingBoxCalibration/3set_center_and_dimensions.png)
	* **SHIFT + mouse** :To move wall symetrically. 
	* **CTRL + mouse** : To make the increments as multiplication of 10cm.
	* You can only drag the bounding wall that is facing you.
If you are not able to drag your desired bounding box wall, try rotating the camera so this wall is closest to you.
{: .warning }

## Send the bounding box to the server
Sending the bounding box data to the server saves the current bounds setting on the server.
When bounds are saved on the server, they effect all the devices that will connect to the server.
This make it the "de-facto" system bounds.

To send the bounds to the server:
1. Navigate to the File menu at the top left
2. Select "Calibration" from the dropdown
3. Click "Save bounds on server."

By default, bounds are not sent to the server.
This means that you can open multiple "mocap studio" instances. On the same computer or on a different computer, each can have a unique "active region".
This for example, can be used when multiple people share a system and wish to record on the same time, but each want to record just his movement.

![mocap studio save bounds on server](/assets/images/4.3BoundingBoxCalibration/4save_bounds_on_server.png)

## Validate by moving in and out of the bounded region
Check that when a person steps out of the target area, their avatar disappears. This confirms the bounding box is correctly set.

![mocap studio bounds validate](/assets/images/4.3BoundingBoxCalibration/5bound_validate.gif)

Note: A person who moves outside of the bounding box is no longer captured.
{: .warning }

