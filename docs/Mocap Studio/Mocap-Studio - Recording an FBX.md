---
layout: default
title: Mocap-Studio - Recording an FBX
parent: Mocap Studio
nav_order: 2
---

# Mocap-Studio - Recording an FBX
{: .no_toc }

Use Mocap-Studio to record the movement of the people inside the scene.
{: .fs-6 .fw-300 }



---
## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}


<iframe width="560" height="315" src="https://www.youtube.com/embed/5m-6Mp5ea3c" frameborder="0" allowfullscreen></iframe>

## Introduction
This document provides a step-by-step guide on how to use mocap studio to:
1. Record an animation
2. Visualize the recorded data
3. Export it as an FBX file 

Follow the instructions below to ensure a successful recording, visualization, and export process.

## Prerequisites
* Make sure Mocap Studio is installed on a computer.
* Ensure the computer is connected to the same network as the Mocap system.

When mocap studio is not in the same local network it will fail to comunicate with AR51's mocap server.
{: .warning }


## Open Mocap Studio and Check for Connectivity
### Launch Mocap Studio:
1. Open the Mocap Studio application.
2. In the upper right corner, ensure that the two indicators are green. This signals that Mocap Studio has found both the management unit (CVS) and the Mocap System (CVS) in its local network.
![1.connectivity.png](/assets/images/record_with_mocap_studio/1.connectivity.png)

## Record the animation 
### Start Recording:
1. Click on the “record” button located in the bottom right corner to begin the recording.
![2. Click on record.png](/assets/images/record_with_mocap_studio/2. Click on record.png)
2. Provide a name for the current session.
![3.Provide_a_name](/assets/images/record_with_mocap_studio/3.Provide_a_name.png)

### Perform Animation:
1. Move into the camera's range to make your character visible on the screen.
2. You can change the view port angle by pressing "Alt" and draging with the mouse left button.
3. Perform the desired animation.

### Stop Recording:
Click again on the record button to stop the current recording session.
![4.Stop_recording.png](/assets/images/record_with_mocap_studio/4.Stop_recording.png)

## Rename the Recording
1. Access the Captures List by locating the new recording file in the captures list
2. To rename the capture, Click on the rename option and enter a descriptive name for the recording. For example, name it "tutorial." 
![5.Rename_recording.png](/assets/images/record_with_mocap_studio/5.Rename_recording.png)

## Export the Recording
Click on the export button. Choose a folder. Choose the file format (i.e. FBX).

![6.Export_button.png](/assets/images/record_with_mocap_studio/6.Export_button.png)
Click "Save" to complete the export.

## Done
You can open the animation in a 3D program of your choice (i.e. Maya, Blender).
