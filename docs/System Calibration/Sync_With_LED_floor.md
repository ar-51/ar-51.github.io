---
layout: default
title: LED Stage Synchronization
parent: System Calibration
nav_order: 5
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

![led_stage_example.png](/assets/images/led_sync/led_stage_example.png)  

---

## Projecting the Checkerboard
To sync AR-51 coordinates with the LED stage:  
CalibrationBoard With Colors.png
1. Project the provided checkerboard image onto the LED floor.  
   - [Download the checkerboard image](/assets/images/led_sync/CalibrationBoard With Colors.png)   
   - The small mark at the center of the checkerboard indicates the AR-51 origin.  

2. AR-51 uses a **right-hand coordinate system** where **Y is up**.  

![checkerboard_projection.png](/assets/images/led_sync/CalibrationBoard With Colors_origin_highlighted.png)  

---

## Rescaling the Checkerboard
- You may rescale the checkerboard, but it must be **uniform** so that each square remains a square.  
- In the AR-51 server settings:  
  - Navigate to:  
    `Camera Calibration Settings` → `Checker Board Settings` → **Aruco Board Square Size Meters**  
  - Enter the real-world size of a checker square (in meters).  

![aruco_settings.png](/assets/images/led_sync/aruco_settings.png)  

---

## Handling Coordinate Offsets
If the LED coordinate system is not centered on the stage (e.g., origin is in the upper-right corner), you can adjust using:  
- `Camera Calibration Settings` → **Calibration Checkerboard Offset**  
- Set the offset values so AR-51 matches the LED system’s origin.  

![coordinate_offset.png](/assets/images/led_sync/coordinate_offset.png)  

---

