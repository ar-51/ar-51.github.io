---
layout: default
title: Using an Animation Blueprint
nav_order: 7
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


This tutorial will guide you through the process of importing an FBX file, creating a blueprint out of the character, editing it, and utilizing the Animation Blueprint in Unreal Engine.


## Prerequisites
Make sure the sdk is in the scene (drag the blueprint).
And that the unreal project is set-up correctly.


### Step 1: Import FBX

1. Open Unreal Engine.
2. In the **Content Browser**, click on **Import**.
3. Navigate to the location of your FBX file, select it, and click **Open**.
4. In the **FBX Import Options** window, adjust the settings as needed and click **Import**.

### Step 2: Create a Blueprint out of the Character

1. In the **Content Browser**, find the imported FBX character.
2. Right-click on the character and select **Create Blueprint**.
3. Choose a name and save location for the blueprint, then click **Create Blueprint**.

### Step 3: Edit the Blueprint

1. Double-click on the newly created blueprint to open it.
2. Edit the blueprint components and settings as needed.
3. Save and close the blueprint editor.

### Step 4: Add AR51Character

1. Drag the AR51Character class into the blueprint.
2. Select the AR51Character in the blueprint editor.

#### 4.a Set the Mesh

1. In the Details panel, locate the **Mesh** property.
2. Set it to the same mesh as the FBX character.

#### 4.b Set the NodeNameMapping

1. In the Details panel, locate the **NodeNameMapping** property.
2. Set it according to your specific nodenamemapping requirements.

### Step 5: Using the Animation Blueprint

If you want to use the Animation Blueprint, follow these steps:

#### 5.a Create an Animation Blueprint

1. In the **Content Browser**, right-click and navigate to **Animation** > **Animation Blueprint**.
2. Select the parent class and the FBX character that you want to create the animation blueprint for.
3. Name and save the new Animation Blueprint.

![animation_node](/assets/images/unreal_blueprint_with_animation_node.png)


#### 5.b Add AR51AnimGraphNode to the AnimGraph

1. Open the newly created Animation Blueprint.
2. In the **AnimGraph**, add the AR51AnimGraphNode.
3. Connect the AR51AnimGraphNode to the Final Pose.

![animation_graph](/assets/images/unreal_animation_graph.png)


#### 5.c Hide AR51Character in the Game

1. Select the AR51Character in the viewport or world outliner.
2. In the Details panel, change its visibility settings to hide it in the game.

![hide_in_game](/assets/images/unreal_hide_in_game.png)


## Conclusion

You have now successfully imported an FBX character, created a blueprint, edited it, and set up an Animation Blueprint in Unreal Engine. Feel free to explore more features and functionalities in Unreal Engine to enhance your game development skills.
