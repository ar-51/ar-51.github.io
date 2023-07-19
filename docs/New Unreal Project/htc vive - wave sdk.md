---
layout: default
title: Vive - Wave SDK
parent: New Unreal Project
nav_order: 3
---

# Set up a New Unreal Vive Wave-SDK Project
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---


## Follow the "New Project" instructions from the Vive Wave website
Follow the instruction from the [wave website](https://hub.vive.com/storage/docs/en-us/UnrealPlugin/UnrealPluginGettingStart.html)  to get setup up your project

Make Sure to disable "Support Vulkan" and enable "Support OpenGL ES3.1"
{: .warning }

## Ensure that your project is compatiable with the android guidelines
Follow the instruction from the [unreal android guidelines](https://docs.unrealengine.com/5.0/en-US/how-to-set-up-android-sdk-and-ndk-for-your-unreal-engine-development-environment/)  to get setup up your project


## Download and extract Wave Unreal Plugins into the Plugins folder

Download Meta's plugin from [wave unreal plugin] (https://developer.vive.com/resources/vive-wave/download/latest/). Extract the plugin into the project "Plugins" folder and restart unreal editor.

## Disable all other VR related plugins

Especially disable: **OpenXR**, **OculusVR** and **SteamVR** to prevent conflicts.

## Try to deploy a simple level to your headset

Try and build the project and deploy it to your headset.

## Download and extract AR51 Unreal-SDK Plugin and AR51 Wave Plugins into the Plugins folder
Your plugins folder should look like this ![plugin_folder](/assets/images/unreal_plugin_folder_wave.png)
Restart the editor to enable the plugins.

## Create a new level
File -> New Level -> Basic

## Be sure to set the visablity of the plugins to True
In the Content Browser window. Select settings and enable "Show Plugin Content"

## Drag the AR51 SDK Blueprint into the current level
From the "Content Browser" windows, select Plugins -> AR51 SDK Content -> Blueprints and drag "AR51SDK_Blueprint" into the level. 

## To enable hand tracking, drag the AR51 Wave-related Blueprints into the current level
From the "Content Browser" windows, select Plugins -> AR51SDK_WAVE Content -> Blueprints and drag: "VRPawn", "WaveBoundary Adapter_BP" and "WaveHands Adapter_BP" into the level. 

## Make sure your Pawn object uses "stage tracking"
Either create a new VRPawn object (using [these instructions](https://hub.vive.com/storage/docs/en-us/UnrealPlugin/VRPawn.html)) or edit the provided VRPawn Blueprint.
Make sure that your tracking space is set to Stage ![tracking_set_to_stage](/assets/images/unreal_vrpawn_tracking_origin_set_to_stage.png)


## In AR51 Blueprint, select "HtcVive" as the platform type
From the Details pannel, Under general you should see a field "Platform" please select "Oculus Quest"  ![select_platform_type](/assets/images/unreal_select_plaform_type_wave.png)


## Make sure you added WaveInputManager to the scene to enable Hand support
In the defails pannel of WaveInputManager under Hand, make sure to enable "Natural Hand" ![natural_hand](/assets/images/unreal_enable_wave_natural_hand.png):


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


