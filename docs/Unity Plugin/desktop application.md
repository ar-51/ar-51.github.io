---
layout: default
title: Desktop Application
parent: Unity Plugin
nav_order: 1
description: "Step-by-step guide for setting up a new Unity desktop project using the AR51 SDK, including installation, platform selection, hand provider setup, and running the scene."
---

# Set up a New Unity Desktop Project
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

<iframe width="560" height="315" src="https://www.youtube.com/embed/rsN7I83gimU" frameborder="0" allowfullscreen></iframe>

## Import the AR51 SDK Unity package
1. In Unity, choose Assets → Import Package → Custom Package…, and select the AR51 Unity SDK package. <br>
![1.Unity_import_custom_packages.png](/assets/images/unity_development/1.Unity_import_custom_packages.png)
2. Choose the ar51 Unity package from the file menu.  <br>
![2.file_menu.png](/assets/images/unity_development/2.file_menu.png)  <br>
3. You should see a progress bar when the package is loading.  <br>
![3.loading.png](/assets/images/unity_development/3.loading.png)  <br>
4. Choose all the assets in the package and click import.  <br>
![4.loading_all_assets.png](/assets/images/unity_development/4.loading_all_assets.png)

## Drag the SDK prefab into the scene
1. Locate the AR51.Unity.SDK prefab on the project menu. Under Assets/AR51.Unity.SDK/Prefabs  <br>
![5.ar51sdk_on_side_menu.png](/assets/images/unity_development/5.ar51sdk_on_side_menu.png)
2. Drag the AR51.Unity.SDK prefab into the scene.  <br>
![6.ar51sdk_in_the_scene.png](/assets/images/unity_development/6.ar51sdk_in_the_scene.png)

## Select the target platform
In the "Service Manager" component select the platform of your choice.  <br>
![7.target_platform.png](/assets/images/unity_development/7.target_platform.png)


## Select the hand provider
If you are using hands in your experience (i.e. Ultra leap) select the appropriate provider in the "Service Manager" component.

## Run the Unity Scene
Run the scene in Unity. 
You should be able to view a character that moves as you do.  <br>
![8.play.png](/assets/images/unity_development/8.play.png)
