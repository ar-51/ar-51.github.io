---
layout: default
title: LED Stage Synchronization
parent: System Calibration
nav_order: 5
description: "Instructions for synchronizing AR51’s coordinate system with LED walls or floors by projecting a calibration checkerboard, adjusting scale, and applying coordinate offsets for cross-system alignment."
---

# LED Stage Synchronization
{: .no_toc }

Before presenting content on an LED stage with AR-51, you may want to synchronize AR-51’s coordinate system with the LED system.  
{: .fs-6 .fw-300 }

This ensures a consistent origin across sessions and allows direct alignment with LED walls or floors.  
{: .fs-6 .fw-300 }

---
## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Motivation
You want to present something on the LED stage and synchronize AR-51 with another system.  
Examples include:
- Use your body to control the content that is displayed on the LED wall/floor.  
- Ensuring the AR-51 origin is placed consistently in the same spot each time.  

![calibration board on stage.png](/assets/images/led_sync/calibration board on stage.png)  

---
## Using AR51's Aruco Style checkerboard pattern
### AR51 Server Settings
- In the AR-51 server settings:  
  - Navigate to:  
    `Camera Calibration Settings` → `Checker Board Settings` → **Calibration Method**  
  - Select **Charuco** from the dropdown menu.  
    ![server_settings_charuco.png](/assets/images/led_sync/server_settings_charuco.png)  
  - Save the server settings if you want this to persist.
### Projecting the Checkerboard
To sync AR-51 coordinates with the LED stage:  
1. Project the provided checkerboard image onto the LED floor.  
   - [Download the checkerboard image](/assets/images/led_sync/CalibrationBoard%20With%20Colors.zip)   
   - The small mark at the center of the checkerboard indicates the AR-51 origin.  

2. AR-51 uses a **right-hand coordinate system** where **Y is up**.  

![checkerboard_projection.png](/assets/images/led_sync/CalibrationBoard With Colors_origin_highlighted.png)  

---

## Using AprilTag Style checkerboard pattern
### AR51 Server Settings
- In the AR-51 server settings:  
  - Navigate to:  
    `Camera Calibration Settings` → `Checker Board Settings` → **`Calibration Method`**  
  - Select **AprilTags** from the dropdown menu.  
    ![server_settings_apriltags.png](/assets/images/led_sync/server_settings_apriltags.png)  
  - Save the server settings if you want this to persist.

### Projecting the Checkerboard
To sync AR-51 coordinates with the LED stage:  
1. Project the provided april tags image onto the LED floor.  
   - [Download the april tags checkerboard image](/assets/images/led_sync/AprilTagCalibrationBoard With Colors.zip)   
   - The center of the board is AR-51's system origin.  

2. AR-51 uses a **right-hand coordinate system** where **Y is up**.  

![apriltag_projection.png](/assets/images/led_sync/AprilTags_origin_highlighted.png)  

---

## Rescaling the Checkerboard
- Measure the a calibration square in the "real world"
When you measure your "real world" checkerboard square make sure to measure the entire square - **Not just the inner aruco area**. You can also measure the pattern from side to side and divide by the number of squares for better accuracy.
{: .warning }

| Standard Calibration Board                                                                 | AprilTags Calibration Board                                           |
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| ![aruco_settings.png](/assets/images/led_sync/CalibrationBoardSingleSquareHighlighted.png) | ![aruco_settings.png](/assets/images/led_sync/SquareSizeAprilTag.png) |


- You may rescale the checkerboard, but it must be **uniform** so that each square remains a square.  
- In the AR-51 server settings:  
  - Navigate to:  
    `Camera Calibration Settings` → `Checker Board Settings` → **`Aruco Board Square Size Meters`**  
  - Enter the real-world size of a checker square (in meters).  

When you measure your "real world" checkerboard square make sure to measure the entire square - **Not just the inner aruco area**. You can also measure the pattern from side to side and divide by the number of squares for better accuracy.
{: .warning }

![aruco_settings.png](/assets/images/led_sync/aruco_settings.png)  

---
## Handling Coordinate Offsets
If the LED coordinate system is not centered on the stage (e.g., origin is in the upper-right corner), you can adjust using:  
- `Camera Calibration Settings` → **Calibration Checkerboard Offset**  
- Set the offset values so AR-51 matches the LED system’s origin.  

![coordinate_offset.png](/assets/images/led_sync/coordinate_offset.png)  

---

