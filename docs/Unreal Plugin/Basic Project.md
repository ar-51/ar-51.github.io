---
layout: default
title: Basic Project
parent: Unreal Plugin
nav_order: 1
description: "Step-by-step guide to creating a new Unreal project and integrating the AR51 SDK, including plugin setup, level creation, and real-time character visualization."
---

# Set up a New Unreal Project
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Download and extract AR51 Unreal Plugins into the Plugins folder
Your plugins folder should look like this: ![plugin_folder](/assets/images/unreal_plugin_folder_clean.png)

Restart the editor to enable the plugin.

## Create a new level
File -> New Level -> Basic

## Be sure to set the visibility of the plugins to True
In the Content Browser window. Select settings and enable "Show Plugin Content"

## Drag the AR51 SDK into the current level
From the "Content Browser" windows, select Plugins -> AR51 SDK Content -> Blueprints and drag "AR51SDK_Blueprint" into the level. 

## Hit Play 
Make sure that AR51's system is running on the same local network as your device.
{: .warning }

You should see the character move in realtime. ![character_waving](/assets/images/unreal_character_waving.png)
