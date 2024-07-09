---
layout: default
title: Oculus Quest
parent: New Unreal Project
nav_order: 2
---

# Set up a New Unreal Oculus Quest Project
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---


## Follow the "New Project" instructions from the Quest website
Follow the instructions from the [quest website](https://developer.oculus.com/documentation/unreal/unreal-quick-start-guide-quest/)  to set up your project

Remember to disable **Support OpenGL ES3.2** under Android ->Build. Quest projects will not work with that option ticked. Make sure to run the test under **"Meta XR Performance Window"** and select Mobile as your target platform. Also Remember to package the project for oculus using the "Package for Meta Quest devices" option.
{: .warning }

## Ensure that your project is compatible with the Android guidelines
Follow the instructions from the [unreal android guidelines](https://docs.unrealengine.com/5.0/en-US/how-to-set-up-android-sdk-and-ndk-for-your-unreal-engine-development-environment/)  to get setup up your project

## Download and extract Meta Unreal Plugins into the Plugins folder

Download Meta's plugin from [meta unreal plugin](https://developer.oculus.com/downloads/package/unreal-engine-5-integration/). Extract the plugin into the project "Plugins" folder and restart the Unreal editor.

## Try to use "Meta XR Performance Window" to set the project with the recommanded settings
It is recommanded to use "Meta XR Performance Window" and follow their suggestions.
![meta_performance_window](/assets/images/unreal_meta_performance_window.png)

## Remember to check the "Package for Meta Quest Devices" option.
When you package your quest device do not forget to tick the "Package for Meta Quest Devices".
Under **"Android" -> "Advanced APK Packaging" -> "Package for Meta Quest Devices"**
![package_for_quest](/assets/images/unreal_package_for_meta_quest_devices.png)

If you see that your project opens as a "window" application inside the quest,
it is a good indication that you forgot to check this box.
{: .warning }

## Try to deploy a simple level to your headset
Try and build the project and deploy it to your headset.

## Download and extract AR51 Unreal Plugins into the Plugins folder
Your plugins folder should look like this:
![plugin_folder](/assets/images/unreal_plugin_folder_quest.png)
Restart the editor to enable the plugin.

## Create a new level
File -> New Level -> Basic

## Be sure to set the visibility of the plugins to True
In the Content Browser window. Select settings and enable "Show Plugin Content"

## Drag the AR51 SDK into the current level
From the "Content Browser" windows, select Plugins -> AR51 SDK Content -> Blueprints and drag "AR51SDK_Blueprint" into the level. 

## Drag the AR51 Oculus-dependent Blueprints into the current level
From the "Content Browser" windows, select Plugins -> AR51SDK_OCULUS Content -> Blueprints and drag: "OculusQuestBoundaryAdapter_BP", "OculusQuestHandsAdapter_BP" and "VRPawn" into the level. 

## Make sure your VrPawn object uses "stage tracking"
Either create a new VRPawn object (using [these instructions](https://hub.vive.com/storage/docs/en-us/UnrealPlugin/VRPawn.html)) or edit the provided VRPawn Blueprint.
Make sure that your tracking space is set to “Stage” ![tracking_set_to_stage](/assets/images/unreal_vrpawn_tracking_origin_set_to_stage.png)

## In AR51 Blueprint, select "Oculus Quest" as the platform type
From the Details panel, under “General” you should see a field "Platform". Please select "Oculus Quest"  ![select_platform_type](/assets/images/unreal_select_plaform_type.png)


## Make sure you have enabled Meta's Hand support
In the project settings under the Meta XR plugin section choose the following: ![hand_support](/assets/images/unreal_enable_meta_hand_support.png):
* "Hand Tracking Support"  should be "Controllers and Hands" or "Hands Only"
* "Hand Tracking Version"  works better with V2.


## Be sure to enable "Developer runtime features" on the “Oculus PC app”
Without enabling this option you might not be able to move your hands on a tethered app and also in "VR preview" mode
{: .warning }

Open the "Oculus" PC application.
Under Settings -> Beta, enable "Developer runtime features".
![enable_developer_option_on_oculus_pc_app](/assets/images/enable_developer_on_quest_pc_app.png)

## In a tethered deployment - enable "Start in VR"
Before deploying to a tethered application (PC VR app), be sure that you project is set to start in VR.
In Unreal-Engine, under "Project Settings" -> "Project Description" enable "Start in VR".

![enable_start_in_VR](/assets/images/unreal_engine_start_in_VR.png)


## Hit Play 
Make sure that AR51's system is running on the same local network as your device.
{: .warning }

You should see the character move in realtime ![character_waving](/assets/images/unreal_character_waving.png).

## On your first run, perform device calibration
You should now perform [device calibration]({% link docs/System Calibration/Device_calibration.md %})  so that the character would position on your body.
