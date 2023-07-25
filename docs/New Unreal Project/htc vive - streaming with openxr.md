---
layout: default
title: Vive - Streaming With OpenXR
parent: New Unreal Project
nav_order: 4
---

# Set up a New Unreal Vive OpenXR-SDK Project
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---


## Follow the "New Project" instructions from the Vive OpenXR website
Follow the instruction from the [HTC website](https://developer.vive.com/resources/openxr/openxr-pcvr/overview/)  to get setup up your project

Make Sure to install **"Vive Business Streaming"** and **"SteamVR"**
{: .warning }

## Ensure that your project is compatiable with the htc hand tracking guidelines
Follow the instruction from the [vive unreal hand tracking guidelines](https://developer.vive.com/resources/openxr/openxr-pcvr/tutorials/unreal-engine/integrate-hand-tracking-data-your-hand-model/)  to get setup up your project


## Enable OpenXR and OpenXRHandTracking plugins

In unreal engine under plugins make sure that the openXR and that the openXRHandTracking is checked.

## Make sure that you PC streaming is working correctly
On your pc open both SteamVR and Vive Business Streaming apps.

## In Vive Business Streaming make sure "Hand Tracking" is checked
Open the settings in the ["Vive Business Streaming"](https://developer.vive.com/resources/openxr/openxr-pcvr/tutorials/set-up-vbs-for-focus-3/) app.
Under "Input" make sure "Hand tracking" checkbox is checked. ![plugin_folder](/assets/images/vive_streaming_hand_tracking.png)

Hand Tracking must be enabled on VBS inorder to track finger motion.
{: .warning }

## In SteamVR, make sure that openXR backend is set to SteamVR.
Open SteamVR settings.
Under "OpenXR" make sure that your current OpenXR Runtime is set to SteamVR.

## Try to deploy a simple level to your headset

Try and build the project and deploy it to your headset.

## Download and extract AR51 Unreal-SDK Plugin and AR51 OpenXR Plugins into the Plugins folder
Your plugins folder should look like this ![plugin_folder](/assets/images/unreal_plugin_folder_openXR.png)

Restart the editor to enable the plugins.

## Create a new level
File -> New Level -> Basic

## Be sure to set the visablity of the plugins to True
In the Content Browser window. Select settings and enable "Show Plugin Content"

## Drag the AR51 SDK Blueprint into the current level
From the "Content Browser" windows, select Plugins -> AR51 SDK Content -> Blueprints and drag "AR51SDK_Blueprint" into the level. 

## Drag the AR51 OpenXR-related Blueprints into the current level
From the "Content Browser" windows, select Plugins -> AR51SDK_OPENXR Content -> Blueprints and drag: "VRPawn", "OpenXrBoundary Adapter_BP" and "OpenXrHands Adapter_BP" into the level. 

## Make sure your VrPawn object uses "stage tracking"
Either create a new VRPawn object (using [these instructions](https://hub.vive.com/storage/docs/en-us/UnrealPlugin/VRPawn.html)) or edit the provided VRPawn Blueprint.
Make sure that your tracking space is set to Stage ![tracking_set_to_stage](/assets/images/unreal_vrpawn_tracking_origin_set_to_stage.png)

If you do not set the tracking mode to stage, the skeleton will not appear on your body after once you restart the VR application.
{: .warning }

## In AR51 Blueprint, select "HtcVive" as the platform type
From the Details pannel, Under general you should see a field "Platform" please select "Oculus Quest"  ![select_platform_type](/assets/images/unreal_select_plaform_type_wave.png)

## In a tethered deployment - enable "Start in VR"
Before deploying to a tethered application (PC VR app), be sure that you project is set to start in VR.
In Unreal engine, under "Project Settings" -> "Project Description" enable "Start in VR".

![enable_start_in_VR](/assets/images/unreal_engine_start_in_VR.png)


## Hit Play 
Make sure that AR51's system is running on the same local network as your device.
{: .warning }

You should see character move live ![character_waving](/assets/images/unreal_character_waving.png).

## On your first run, perform device calibration
You should now perform [device calibration]({% link docs/System Calibration/Device_calibration.md %})  so that the character would position on your body.


