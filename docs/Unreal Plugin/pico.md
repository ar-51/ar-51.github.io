---
layout: default
title:  Using AR51’s PicoXR Plugin
parent: Unreal Plugin
nav_order: 8
---

#  Using AR51’s PicoXR Plugin
{: .no_toc }

How to setup AR-51's PicoXR plugin for Unreal Engine.
{: .fs-6 .fw-300 }


---
## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}


This document provides a step-by-step guide on setting up AR-51's PicoXR Plugin in Unreal Engine. 

# Prerequisites
Ensure Unreal Engine is installed.
Confirm that AR-51 SDK and PicoXR plugins are available and activated.



# Download and Install the Plugins
## Download the AR51 Plugins
1. In your browser, navigate to **AR Files Storage** [https://files.ar-51.com](https://files.ar-51.com/) 
2. Download the **”AR51 Unreal SDK”** plugin. 
3. Download the **'AR 51 SDK_Live Link'** plugin.
![1.download_live_link.png](/assets/images/pico_unreal/1.download_live_link.png)

## Download PicoXR Plugin
1. Download the [**PicoXR** Unreal plugin](https://developer.picoxr.com/resources/#sdk).

## Install the Plugin
**Project-Specific Installation:**
1. Navigate to your Unreal Engine project's root directory.
2. If a **Plugins** folder does not exist, create one.
![2.UE_plugins_folder.png](/assets/images/pico_unreal/2.UE_plugins_folder.png)
3. Extract the content of the downloaded plugins into the Plugins folder.
4. The Plugins folder should contains the three plugins: **AR51SDK**, **AR51SDK_PICO**, **PicoXR**
![2.picoPlugins.png](/assets/images/pico_unreal/2.picoPlugins.png)

## Activating the Plugins
1. Open Unreal Engine and your project.
2. Go to **Edit > Plugins**.
3. In the Plugins window, use the search bar to find **'Live Link'** and **'AR 51 SDK_PICO.'**
4. Ensure both **AR51 SDK_PICO** and **AR51 SDK** are enabled by checking their respective boxes.
![3.UE_plugins_window.png](/assets/images/pico_unreal/3.UE_plugins_window.png)

## Disable OpenXR plugins
1. Open Unreal Engine and your project.
2. Go to **Edit > Plugins**.
3. In the Plugins window, use the search bar to find **'openXR'**.
4. Ensure all **openXR** and **AR51 SDK** are enabled by checking their respective boxes.
![3.UE_plugins_window.png](/assets/images/pico_unreal/3.UE_plugins_disable_openxr.png)

# Unreal Project Settings

## Make sure the project is set using the [PICO development guidelines](https://developer.picoxr.com/document/unreal/configure-the-project/) 

## Disable Mobile HDR
1. Go to the top menu and select **Edit**.
2. Choose **Project Setings** .
3. Under Engine - Rendering submenu VR find the option for "Mobile HDR" and disable it.
![4.disable_mobile_hdr.png](/assets/images/pico_unreal/4.disable_mobile_hdr.png)

## Add Support for Vulkan and OpenGl
1. Go to the top menu and select **Edit**.
2. Choose **Project Setings** .
3. Under **Android** - "**build**" submenu, add support for Vulkan and OpenGl.
![11.vulcan_and_opengl.png](/assets/images/pico_unreal/11.vulcan_and_opengl.png)

## Enable fullscreen in Kitkat
1. Go to the top menu and select **Edit**.
2. Choose **Project Setings** .
3. Under **Android** - "**build**" submenu, add support for Vulkan and OpenGl.
![10.fullscreen_android.awebp](/assets/images/pico_unreal/10.fullscreen_android.awebp)

## Enable hands as a valid VR controller
1. Go to the top menu and select **Edit**.
2. Choose **Project Setings** .
3. On the left table of content select Plugins and then PICOXR Settings
4. Under HandTRacking Support, make sure either "Controllers and Hands" or "Hands Only" are selected.
![5.enable_hands.png](/assets/images/pico_unreal/5.enable_hands.png)

## In a tethered deployment - enable “Start in VR”
Before deploying to a tethered application (PC VR app), be sure that you project is set to start in VR. In Unreal-Engine, under “Project Settings” -> “Project Description” enable “Start in VR”.
![enable_start_in_VR](/assets/images/unreal_engine_start_in_VR.png)

# Set the New Level
## Create a New Unreal Level
1. On the menu press on "File" => "New Level..."
2. Select your desired level from the templates
![5.new_level.png](/assets/images/pico_unreal/5.new_level.png)

## Drag the AR51SDK blueprint into the current Level and zero it's transform
1. In the Content Brwoser, navigate to Plugins/AR51SDK Content.
![6.ar51sdk_blueprint.png](/assets/images/pico_unreal/6.ar51sdk_blueprint.png)
2. Drag the **AR51SDK_Blueprint** into current level
3. Zero the transform of AR51SDK_Blueprint


## Drag the neccessery blueprints into the current Level and zero it's transform
1. In the Content Brwoser, navigate to Plugins/AR51SDK_PICO Content.
![6.PicoXR_pawn.png](/assets/images/pico_unreal/6.picoXR_pawn.png)

2. Drag the **BP_PICO_XR_Pawn** into current level
3. Zero the transform of BP_PICO_XR_Pawn
4. Drag the **PicoXRHandsAdapter_BP** into current level
5. Zero the transform of PicoXRHandsAdapter_BP
6. Drag the **PicoBoundaryAdapter_BP** into current level
7. Zero the transform of PicoBoundaryAdapter_BP
8. Your current level should now contain all three blueprints
![7.currentMap.png](/assets/images/pico_unreal/7.currentMap.png)

## Make sure your VrPawn object uses “stage tracking”
Edit the provided VRPawn Blueprint. Make sure that your tracking space is set to “Stage”
![8.set_stage_mode.png](/assets/images/pico_unreal/8.set_stage_mode.png)


# Hit Play 
Make sure that AR51's system is running on the same local network as your device.
{: .warning }

You should see the character move in realtime ![character_waving](/assets/images/unreal_character_waving.png).

## On your first run, perform device calibration
You should now perform [device calibration]({% link docs/System Calibration/Device_calibration.md %})  so that the character would position on your body.
