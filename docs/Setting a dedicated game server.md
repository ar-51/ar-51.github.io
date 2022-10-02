---
layout: default
title: Stream 3D objects to the OMS as overlay
nav_order: 4
---


# Stream 3D objects to the OMS as overlay
{: .no_toc }

The system can stream 3D content as an overlay from any of the cameras in the scene.
This can be viewed from the OMS web interface.
{: .fs-6 .fw-300 }



---
## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}


<iframe width="560" height="315" src="https://www.youtube.com/embed/hOzdWpYH_m4" frameborder="0" allowfullscreen></iframe>


## Prerequisites
Make sure the SDK is in the scene (drag the prefab).

There should be a single dedicated game server (DGS) in the network.


## Set Unity as DGS 
Set the Platform as a PC. Tick on the "Is Dedicated Game Server" box. inside the "Service Manager" component.

## Enable Unity to run in the background
By default unity projects are paused when the are not the active window.
Since this is not a preferred behavior for a server, the "run in background" option should be enabled.

Project Settings -> Player tick the checkbox for "Run In Background".

## Only game object in the "Water" layer are streamed

By default all game objects which belong to the "Water" layer are streamed.

If you wish the other object (beside the characters) are streamed to the OMS, make sure they are in the "Water" layer.

You can select which layers are rendered and shown in the OMS.

In the Unity SDK. Under the "Render Service" component, you can choose which layers should be rendered.
If you wish to change the layers which are rendered, change the values in the "render Camera Culling Mask" field.

## Open the OMS web-gui and enable the hologram view for the camera
Open the OMS web application. Click on a camera to view the feed in the web-gui.

You can enable the holograms by clicking on the button which is above the upper-right corner of the camera feed.

