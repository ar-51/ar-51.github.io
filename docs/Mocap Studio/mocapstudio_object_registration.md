---
layout: default
title: Mocap-Studio - Registering Tracked Objects
parent: Mocap Studio
nav_order: 7
description: "Explains how to register and track a physical object in Mocap Studio using custom FBX models and marker-based detection."
---

# Mocap-Studio – Registering Tracked Objects
{: .no_toc }

Use Mocap Studio to register real-world objects and track them as interactive objects inside the scene.
{: .fs-6 .fw-300 }

---
## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

<iframe width="560" height="315" src="https://www.youtube.com/embed/A4Ohy-8WYOI" frameborder="0" allowfullscreen></iframe>


## Introduction
This guide explains how to register a real-world object in Mocap Studio using object detection and a custom 3D model.
Once registered, the object becomes a tracked entity that can be moved, rotated, and interacted with in real time.

The example used in this guide is a **wooden chair** tracked using markers.

## Prerequisites
* Camera colors and markers are already configured correctly.
* Stable markers are clearly detected in 3D space.
* Markers are placed on the real object.

![Markers placed on the object](/assets/images/mocap_studio_object_registration/0.place_marker_on_object.png)

* The object is placed near the center of the capture volume.
* Marker balls within **1 meter** from the object’s center are considered valid.

## Adding a New Tracked Object
### Open Object Detection
1. Open **Mocap Studio**
2. Click **Object Detection**
3. Select **Add Track Object**

![Add tracked object menu](/assets/images/mocap_studio_object_registration/1.menu_add_object.png)

## Importing a Custom Model
Mocap Studio includes several built-in object models, but custom models can also be used.

### Import FBX
1. Select **Import FBX**

![Select import FBX](/assets/images/mocap_studio_object_registration/2.select_import_fbx.png)

2. Choose the FBX file from disk

![FBX file selection](/assets/images/mocap_studio_object_registration/3.file_selection_screen.png)

3. The model may appear **extremely large**

![Chair with incorrect scale](/assets/images/mocap_studio_object_registration/4.chair_wrong_scale.png)

This usually means the model was authored in **centimeters instead of meters**.

### Important
Do **not** use the scale controls inside Mocap Studio to fix this.

![Do not scale in Mocap Studio](/assets/images/mocap_studio_object_registration/5.do not use scale from menu.png)
{: .warning }

## Fixing Scale in Blender
1. Open the FBX in **Blender**
2. Select the model
3. Change scale from `1` → `0.1`
4. Export the FBX again

![Use Blender to rescale](/assets/images/mocap_studio_object_registration/6.use_blender_to_rescale.png)

## Re-importing the Corrected Model
Re-import the corrected FBX into Mocap Studio.  
The model should now appear at the correct size.

## Aligning the Model
### Move and Rotate
Use the **manipulator** to position and rotate the model.

![Move and rotate with manipulator](/assets/images/mocap_studio_object_registration/7.use_manipulator to move_and_rotate.png)

### Camera Overlay Alignment
1. Double-click the camera feed to enable overlay view
2. Use it to precisely match the real object

![Camera overlay view](/assets/images/mocap_studio_object_registration/8.double_click_for_camera_overlay_to_find_correct_manipulation.png)

![Chair aligned with overlay](/assets/images/mocap_studio_object_registration/9.chair_from_camera_overlay.png)

## Registering the Object
1. Rename the object

![Rename object](/assets/images/mocap_studio_object_registration/10.rename_object.png)

2. Click **Apply**

![Save and apply](/assets/images/mocap_studio_object_registration/11.save_and_apply.png)

The object is now registered.

## Using the Tracked Object
Once registered:
* The object becomes part of the virtual scene
* Any movement or rotation of the real object is mirrored

![Tracked chair movement](/assets/images/mocap_studio_object_registration/11.move_the_chair.gif)

## Removing an Object
If the result is not satisfactory, the object can be deleted and re-registered at any time.

![delete_object](/assets/images/mocap_studio_object_registration/12.delete_object.png)
