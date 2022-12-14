---
layout: default
title: Oculus Quest
parent: New Unity Project
nav_order: 2
---

# Set up a New Unity Oculus Quest Project
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

<iframe width="560" height="315" src="https://www.youtube.com/embed/vr3xzahvIB0" frameborder="0" allowfullscreen></iframe>

## Follow the "New Project" instructions from the quest website
Follow the instruction from the [quest website](https://developer.oculus.com/documentation/unity/unity-gs-overview/)  to get setup up your project

## Drag the SDK prefab into the scene

From Assets/AR51.Unity.SDK/Prefabs drag the AR51.Unity.SDK prefab into the scene.

## Select the target platform
In the "Service Manager" component select "Oculus Quest" as the platform of your choice.

## Select the hand provider
Select "Oculus Quest" as the hand provider in the "Service Manager" component.

## Set the world pivot
The system automatically maps between the coordinate system of the every quest to a common coordinate system.
This enables a shared experience where multiple players share the same world.

In order for the players to experience the same place, every object that the player can interact with needs to mapped as well.

Create a new Game Object and add the "World Anchor Constraint" component.
Place all game objects that the player interact with as child objects of this new object.

## Build and the deploy the app to the Oculus Quest
Build the project and deploy it your devices.

By default the application will reside under "Unknown Sources" in the quest apps menu.

