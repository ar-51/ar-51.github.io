---
layout: default
title: HTC Vive
parent: Unity Plugin
nav_order: 3
---

# Set up a New Unity HTC Vive Project
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Import the Vive to the Package Manager
In the project settings add Vive to Package Manager.
* Name: Vive
* URL: https://npm-registry.vive.com
* Scope: com.htc.upm


![vive_package_url](/assets/images/Add_vive_to package_manager.png)

## Install the Vive Essence Package
Open Window -> Package Manager and install "Vive Wave XR Plugin - Essence".
It will install the necessary dependencies

![install_wave_essence](/assets/images/install_wave_essence.png)

## Select the main camera object and convert it to XR-Rig
Right-click the main camera and select XR -> Convert Main Camera To XR Rig

![convert_to_xr_rig](/assets/images/convert_main_camera_to_XR_rig.png)

## Reset the XR-rig transform and set tracking to Floor
Reset the XR-rig transform. Place zero in the offset. And, set "Tracking Mode" to "Floor".

![tracking_mode_floor](/assets/images/Set_XR_rig_to_Floor_and_Y_offset_to_zero.png)

## Enable Wave-XR in player settings
In player settings, under XR Plugin Management on the Android Tab, choose WaveXR.

![choose_waveXR](/assets/images/choose_waveXR.png)

## Enable Natural Hand in Wave XR Settings
In the player setting, under WaveXRSettings, enable the "Enable Natural Hand" checkbox.

![enable_hand](/assets/images/enable_hand_tracking.png)

## Add the hand manager to the scene
From the wave menu, select GameObject -> "Add hand manager to the scene"

![choose_waveXR](/assets/images/add_hand_managerr.png)

## Drag AR-51 prefab into the scene
From Assets/AR51.Unity.SDK/Prefabs drag the AR51.Unity.SDK prefab into the scene.

## Select the platform and hand-provider
In the "Service Manager" component (under the newly created ar-51 object), set the platform and Hand Provider.

Choose HTC Focus 3 (or HTC Vive if you are using a tethered headset such as the Vive-Pro).
Choose HTC_Wave under HandProvider.

![choose_waveXR](/assets/images/Select_HTC_focus3_and_HTC_Wave_in_platform.png)

![choose_waveXR](/assets/images/Select_HTC_focus3_and_HTC_Wave_in_platform2.png)

## Set the world pivot
The system automatically maps the coordinate system of every quest to a common coordinate system.
This enables a shared experience where multiple players share the same world.

In order for the players to experience the same place, every object that the player can interact with needs to be mapped as well.

Create a new Game Object and add the "World Anchor Constraint" component.
Place all game objects that the player interacts with as child objects of this new object.

## Build and deploy the app to the HTC device
Build the project and deploy it on your devices.
