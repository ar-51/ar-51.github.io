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


## Follow the "New Project" instructions from the quest website
Follow the instruction from the [quest website](https://developer.oculus.com/documentation/unreal/unreal-quick-start-guide-quest/)  to get setup up your project

## Ensure that your project is compatiable with the android guidelines
Follow the instruction from the [unreal android guidelines](https://docs.unrealengine.com/5.0/en-US/how-to-set-up-android-sdk-and-ndk-for-your-unreal-engine-development-environment/)  to get setup up your project


## Download and extract Meta Unreal Plugins into the Plugins folder

Download Meta's plugin from [meta unreal plugin] (https://developer.oculus.com/downloads/package/unreal-engine-5-integration/). Extract the plugin into the project "Plugins" folder and restart unreal editor.

## Try to deploy a simple level to your headset

Try and build the project and deploy it to your headset.

## Download and extract AR51 Unreal Plugins into the Plugins folder
Your plugins folder should look like this ![plugin_folder](/assets/images/unreal_plugin_folder.png)
Restart the editor to enable the plugin.

## Create a new level
File -> New Level -> Basic

## Be sure to set the visablity of the plugins to True
In the Content Browser window. Select settings and enable "Show Plugin Content"

## Drag the AR51 SDK into the current level
From the "Content Browser" windows, select Plugins -> AR51 SDK Content -> Blueprints and drag "AR51SDK_Blueprint" into the level. 

## In AR51 Blueprint, select "Oculus Quest" as the platform type
Edit the AR51 Buleprint. Under general you should see a field "Platform" please select "Oculus Quest"  ![select_platform_type](/assets/images/unreal_select_plaform_type.png)


## Make sure you have enabled Meta's Hand support
In the project settings under the Meta XR plugin section choose the following ![hand_support](/assets/images/unreal_enable_meta_hand_support.png):
* "Hand Tracking Support"  should be "Controllers and Hands" or "Hands Only"
* "Hand Tracking Version"  works better with V2.


## Be sure to enable "Developer runtime features" on the oculus PC app
Without enabling this option you might not be able to move your hands on a tethered app and also in "VR preview" mode
{: .warning }

Open the "Oculus" PC application.
Under Settings -> Beta, enable "Developer runtime features".
![enable_developer_option_on_oculus_pc_app](/assets/images/enable_developer_on_quest_pc_app.png)

## Hit Play 
Make sure that AR51's system is running on the same local network as your device.
{: .warning }

You should see character move live ![character_waving](/assets/images/unreal_character_waving.png).

## On your first run, perform device calibration
You should now perform [device calibration]({% link docs/System Calibration/Device_calibration.md %})  so that the character would position on your body.


