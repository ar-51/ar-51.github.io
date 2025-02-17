---
layout: default
title:  Using AR51’s LiveLink Plugin
parent: New Unreal Project
nav_order: 6
---

#  Using AR51’s LiveLink Plugin
{: .no_toc }

Setting up Live Link for AR-51 in Unreal Engine.
{: .fs-6 .fw-300 }


---
## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}


This document provides a step-by-step guide to setting up Live Link for AR-51 in Unreal Engine. 
<iframe width="560" height="315" src="https://www.youtube.com/embed/aSO3yDgI0fE" frameborder="0" allowfullscreen></iframe>


# Prerequisites
Ensure Unreal Engine is installed.
Confirm that AR-51 SDK and Live Link plugins are available and activated.



# Download and Install the Plugins
## Download the Plugins
1. In your browser, navigate to **AR Files Storage** [https://files.ar-51.com](https://files.ar-51.com/) 
2. Download the **”AR51 Unreal SDK”** plugin. 
3. Download the **'AR 51 SDK_Live Link'** plugin.
![1.download_live_link.png](/assets/images/live_link_unreal/1.download_live_link.png)

## Install the Plugin
**Project-Specific Installation:**
1. Navigate to your Unreal Engine project's root directory.
2. If a **Plugins** folder does not exist, create one.
3. Extract the content of the downloaded plugins into the Plugins folder.

**Engine-Wide Installation:**
1. Navigate to the Unreal Engine installation directory (e.g., **C:\Program Files\Epic Games\UE_X.YY\Engine\Plugins\Marketplace\**).
2.  Extract the content of the downloaded plugins into this folder. 
    Note: Plugins installed here will be available for all projects using this Unreal Engine version.
    {: .warning }
![2.UE_plugins_folder.png](/assets/images/live_link_unreal/2.UE_plugins_folder.png)

## Activating the Plugins
1. Open Unreal Engine and your project.
2. Go to **Edit > Plugins**.
3. In the Plugins window, use the search bar to find **'Live Link'** and **'AR 51 SDK_Live Link.'**
4. Ensure both **AR51 SDK_Live Link** and **AR51 SDK** are enabled by checking their respective boxes.
![3.UE_plugins_window.png](/assets/images/live_link_unreal/3.UE_plugins_window.png)

# Opening Virtual Production

1. Go to the top menu and select **Window**.
2. Choose **Virtual Production** and then **Live Link**.
![4.virtual_production_live_link.png](/assets/images/live_link_unreal/4.virtual_production_live_link.png)

## Adding AR 51 Live Link Source

1. In the Live Link panel, click **Add Source**.
2. Select **AR51 Live Link** from the list.
![5.live_link_panel_add_source.png](/assets/images/live_link_unreal/5.live_link_panel_add_source.png)
3. The source type should appear as **AR51 Live Link** and will appear with the status: **Not Connected**.
![6.source_type_not_connected.png](/assets/images/live_link_unreal/6.source_type_not_connected.png)

## Adding Virtual Subject
1. Click **Add Source** again in the Live Link panel.
2. Select **Add Virtual Subject**.
3. Provide a name for your subject (e.g. AR51VirtualSubject).
4. Under the options, select **AR51LiveLinkSubject**.
5. Click **Add**.
![7.create_virtual_subject.png](/assets/images/live_link_unreal/7.create_virtual_subject.png)

# Creating a Live-Link Character using the Animation Blueprint
## Creating and Setting Up Blueprint
1. In the Content Browser, go to **Plugins > AR 51 SDK Content > Models > Unreal Default Character > Mesh**.
2. Locate the **SK_Mannequin skeletal mesh**.
3. Right-click on it, select **Create**, and then choose **Anim Blueprint**.
4. Name the new blueprint **AR 51 SDK Live Link Character**.
5. Move this blueprint to your project's Content folder.
![8.create_anim_blueprint.png](/assets/images/live_link_unreal/8.create_anim_blueprint.png)

## Configuring the Blueprint
1. Open the newly created blueprint.
2. In the blueprint editor, right-click on an empty space and search for **Live Link Pose**.
3. Add the **Live Link Pose** node.
4. Connect the **Input Pose** to the **Result Pose**.
5. In the **Live Link Subject Name** field, select **AR 51 Virtual Subject**.
6. Click **Compile** to save the changes.
![9.blueprint_input_pose.png](/assets/images/live_link_unreal/9.blueprint_input_pose.png)


# Testing the Setup
1. Drag and drop the **AR 51 SDK Live Link Character** blueprint into your level.
2. Reset its location to (0,0,0) to center it.
3. Drag and drop the **AR 51 SDK** blueprint into your level.
4. Reset its location to (0,0,0) to center it.
5. Press **Play** to start the scene.
6. Open the Live Link panel from **Window > Virtual Production > Live Link** if it's minimized.
7. Ensure that **AR 51 Live Link** in the subject name list shows as connected.
8. In the right-side attributes panel, ensure **Show Model** is enabled under **General**.
![10.live_link_show_model.png](/assets/images/live_link_unreal/10.live_link_show_model.png)


# Conclusion
You've successfully set up Live Link for AR-51 in Unreal Engine. For any issues, revisit the steps and ensure all settings are correct. Thank you for following this guide.
