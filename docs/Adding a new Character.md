---
layout: default
title: Adding a new Character
nav_order: 5
---

# Adding a new Character 
{: .no_toc }

The system support any type of Unity compatible Humanoid Character.
{: .fs-6 .fw-300 }



---
## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}


<iframe width="560" height="315" src="https://www.youtube.com/embed/WfF9q_2Mztc" frameborder="0" allowfullscreen></iframe>


## Prerequisites
Make sure the sdk is in the scene (drag the prefab).
And that the unity project is set up correctly [New Unity Project]({% link docs/New Unity Project/New Unity Project.md %}).


## Set prefab a Humanoid
Open the character fbx in the inspector and change the "Animation Type" to "Humanoid" and click Apply.

## Verify the joints are set up correctly

Click "Configure" and make sure that all the unity joints are correctly mapped

## Verify each finger has a tip GameObject

Make sure the finger has a tip game object.

If the fingers do not contain a tip game object, the model will not work correctly
{: .warning }

## Add the component "AR51 Character" to the character prefab
Back in Unity - edit the prefab and add the component "AR51 Character"

The system automatically maps the correct bones in the hierarchy. You can validate this by expanding the bones group in the inspector.

## Added the prefab to the "Character Prefabs" list inside "Skeleton Consumer"
Select the AR51.Unity.SDK game object. 
In the inspector open the component named "Skeleton Consumer". And, add the newly created prefab to the "Character Prefabs" list. 



