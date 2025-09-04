---
layout: default
title:  Add a new Character to AR51’s Unreal SDK
parent: Unreal Plugin
nav_order: 7
---

#  Add a new Character to AR51’s Unreal SDK
{: .no_toc }

Setting up a new character for AR-51 in Unreal Engine.
{: .fs-6 .fw-300 }


---
## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}


This document provides a step-by-step guide to setting up a new character forAR-51 in Unreal Engine. 
<iframe width="560" height="315" src="https://www.youtube.com/embed/ky_is3ye2sk" frameborder="0" allowfullscreen></iframe>


# Prerequisites
* Ensure Unreal Engine is installed.
* Confirm that AR-51 SDK plugin is available and activated.


# Creating a new blueprint for the character
## Create a new Blueprint class

1. Make a new folder for the character inside the content folder.
2. **Create a new Blueprint class**: right-click on the folder and select **"Create Blueprint Class"**. 
![1.Create_a_new_blueprint_class.png](/assets/images/Unreal_Engine_Add_ a_new_Character/1.Create_a_new_blueprint_class.png)
3. From the options provided, choose the **"Actor"** class. 
![2.Choose_the_actor_class.png](/assets/images/Unreal_Engine_Add_ a_new_Character/2.Choose_the_actor_class.png)


## Add AR51Character component to the new blueprint class
1. Double-click on the newly created Blueprint to open it in the Blueprint Editor.
2. Add the AR51 Character component to your blueprint by clicking Add in the Component tab. 
   Then, search for and select the **AR51Character** component.
![3.Add_a_AR51Character_component.png](/assets/images/Unreal_Engine_Add_ a_new_Character/3.Add_a_AR51Character_component.png)

## Setting the Skeletal Mesh
1. Navigate to the Details tab.
2. Locate the Skeletal Mesh option.
3. Choose the desired mesh from the available options.
![4.Select_skeletal_mesh.png](/assets/images/Unreal_Engine_Add_ a_new_Character/4.Select_skeletal_mesh.png)

## Custom Joint mapping
### Create a Custom joint mapping file
If necessary, create a custom mapping file. This file maps the joint names of your custom mesh to the joint names of the Unreal default character.
You can begin by copying and then editing the default mapping file.
![5.Edit_mapping_file.png](/assets/images/Unreal_Engine_Add_ a_new_Character/5.Edit_mapping_file.png)


### Setting the Mapping file
1. Navigate to the Details tab.
2. Locate the Mapping option.
3. Choose the desired mapping from the available options.
![6.Select_mapping_file.png](/assets/images/Unreal_Engine_Add_ a_new_Character/6.Select_mapping_file.png)

# Add a New Character to the AR51SDK Skeleton Consumer
Now that we have a new character available we need to make it available to the AR51SDK
1. Locate the **AR51SDK** blueprint within your level.
2. Navigate to the Details tab and find the **SkeletonConsumer** Component.
3. Under **"Character Blueprints"** create a new entry in the array if necessary, or replace an existing entry with the newly created character blueprint.
4. Rearrange the order of the characters in the array by dragging the array entries. This changes the loading order. 
Entry 0 defines the default character loaded by the SDK.
{: .warning }

![7.Add_to_SkeletonConsumer.png](/assets/images/Unreal_Engine_Add_ a_new_Character/7.Add_to_SkeletonConsumer.png)

# Play and test
1. Press **Play** to start the scene.
2. The game should instantiate your new character when the system detects a new person.


# Conclusion
You've successfully added your character to the AR-51 SDK. 
For any issues, revisit the steps and ensure all settings are correct. Thank you for following this guide.
