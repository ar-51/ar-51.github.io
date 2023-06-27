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
Follow the instruction from the [unreal adnroid guidelines](https://docs.unrealengine.com/5.0/en-US/how-to-set-up-android-sdk-and-ndk-for-your-unreal-engine-development-environment/)  to get setup up your project


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

## Hit Play 
If AR51's system is running on the same local network as your device, you should see character move live ![character_waving](/assets/images/unreal_character_waving.png).


