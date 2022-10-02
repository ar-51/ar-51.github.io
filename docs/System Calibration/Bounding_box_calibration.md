---
layout: default
title: Bounding Box Calibration
parent: System Calibration
nav_order: 2
---

# Bounding-Box Calibration in Mocap Studio
{: .no_toc }

Bounding box calibration is used to set the capture area.
{: .fs-6 .fw-300 }

A person who moves outside of the bounding box is not longer captured.
{: .fs-6 .fw-300 }

---
## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

## Open Mocap Studio
On a laptop that is connected to the same network as the system, open Mocap Studio.

If the laptop is not in the same network it will not be able to connect to the system.
{: .warning }

![mocap studio](/assets/images/mocap_studio.png)


## Set the center and the dimensions
In Mocap Studio, set the center and the dimensions of the bounding box (width, height, depth).

You can show the bounding box by activating "Show Bounds".
![mocap studio selection menu](/assets/images/mocap_studio_selection_menu.png)

## Send the bounding box to the server
From the file menu press: “Calibration” -> “Send bounds to server”

![mocap studio file menu](/assets/images/mocap_studio_file_menu.png)

## Validate
Check that when a player steps out of the target area his avatar disappears.
