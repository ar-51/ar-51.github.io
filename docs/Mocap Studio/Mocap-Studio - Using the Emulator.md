---
layout: default
title: Mocap-Studio - Using the Emulator
parent: Mocap Studio
nav_order: 3
---

# Mocap-Studio - As a System Emulator
{: .no_toc }

Use Mocap-Studio to record the movement of the people inside the scene.
{: .fs-6 .fw-300 }



---
## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}


<iframe width="560" height="315" src="https://www.youtube.com/embed/HKpiEfGotZ8?si=tR-lHhPAk3t_ZBug" frameborder="0" allowfullscreen></iframe>

## Introduction
This guide provides detailed instructions on how to use the AR-51 Mocap Studio as an Emulator.
In this mode of operations, Mocap Studio mimics the behaviour of a live system.
This making it perfect for development team to developer their application that interacts with AR51 sdk.
The guide covers starting mocap studio, activating OMS and CVS, and loading animation files.

## Prerequisites
* Make sure Mocap Studio is installed on a computer.
* Make sure you have a GR51 motion file available [running recording](/assets/gr51/running_take001_2023-10-19_17-16-32_2023-10-19_17-16-47.gr51), [clapping recording](/assets/gr51/Bclapping003_2023-10-19_13-56-23_2023-10-19_13-56-32.gr51).
* Ensure that the client computer is connected to the same network as the Mocap Studio.
When mocap studio is not in the same local network it will fail to communicate with AR51's mocap server.
{: .warning }


## Starting the Mocap Studio Emulator
### Launch Mocap Studio:
1. Open the Mocap Studio application.
2. Put the application in full-screen mode for better visibility.

### Locate Indicators
On the top right corner, you will see two indicators: 
1. *OMS (Operating Management System)*: Detects components within the local network.
2. *CVS (Computer Vision Service)*: Streams skeleton information and object detection.
![1.connectivity.png](/assets/images/record_with_mocap_studio/1.connectivity.png)

### Ensure OMS is Active
* If the OMS indicator is green, it means OMS is already active
* If it not is gray, double-click the icon. A prompt will notify you to start a new OMS. Select "Yes" to activate it.

### Ensure the CVS is Active
1. Make sure that the CVS in indicator is gray
![1.connectivity.png](/assets/images/record_with_mocap_studio/1.connectivity.png)

2. Double-click the CVS icon.
3. Confirm by clicking "OK" to start a new CVS instance.
If the indicator is already green, this means that another computer is currently the active CVS. You should find the second CVS and close it before activating a new CVS.
{: .warning }

### Loading a pre-recorded animation 
Open a new Mocap Studio and Load a File:
1. Click the file import button.
![1.connectivity.png](/assets/images/record_with_mocap_studio/1.connectivity.png)

2. The system should open a new window.
3. Locate your pre-recorded file (*.gr51) and load it.
4. You should see a process bar for the loading process
5. Once loaded you should see an animation playing inside Mocap Studio

## Emulator is Active. Check status on another client 
<iframe width="560" height="315" src="https://www.youtube.com/embed/EDgn7kPi5Rw?si=n-yRnJSeP_Jw6086" frameborder="0" allowfullscreen></iframe>

* At this point "Mocap Studio" is acting as a system emulator. 
* At this mode, it is sending skeleton to all other client that are connected to the same local network.
* To view the mocap broadcast, you can use another client.
* The client can be the same machine or a different one.
* Here is a partial list of supported clients:
  1. Another Mocap Studio
  2. Unity3D Editor with AR51 SDK. 
  3. A compiled program that was created with Unity and AR51 SDK (i.e. oculus quest sdk)
  4. Unreal Engine with AR51 SDK.
  5. A C++ client that is running AR51 SDK.

![1.connectivity.png](/assets/images/record_with_mocap_studio/1.connectivity.png)

## Controlling the Emulator
### Changing the content that is being broadcast
You can choose a different pre-recorded animation to change the content.
Note, any change in the emulator's content is propagated to all other clients in the network.

### Scrub Through the Animation
Use the time slider to navigate through the recorded animation.

### Recording Panel, Playback and Export
1. You can use Mocap-Studio Record function to record a subset of original animation file.
![1.connectivity.png](/assets/images/record_with_mocap_studio/1.connectivity.png)

2. After you recorded the original gr51 again you should see a second animation on the animation panel
3. This new animation should have the export icon enabled (not grayed out).
4. You can press on the export icon to export the animation.
