---
layout: default
title: Mocap-Studio - Entity Identification
parent: Mocap Studio
nav_order: 5
description: "Guide to using Mocap Studio’s entity identification system to register, label, rename, and manage persistent identities across tracking sessions."
---

# Mocap-Studio - As a System Emulator
{: .no_toc }

Use Mocap-Studio to administer the entity identification.
{: .fs-6 .fw-300 }



---
## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}


# Identification System in Mocap Studio

This guide explains how to use the **Identification** feature in AR 51's Mocap Studio. It covers how to register entities, view their persistent labels, and edit or forget entity identities using the main menu or the context menu.

---
<iframe width="560" height="315" src="https://www.youtube.com/embed/61HklDkK35I" frameborder="0" allowfullscreen></iframe>

## Prerequisites
Make sure that "enable reid" option is enabled in the server settings.
![Enable_ReId](/assets/images/entity_id/enable_reid_server.png)
## Starting the Entity Registration Process

To begin entity registration, open the main menu and select:

**Identification → Start Registration**

During this phase, all individuals who need persistent identification should be present in the capture space and look toward the AR 51 cameras as much as possible.

For better visualization, enable the **Detection Identifier** overlay (Shortcut: `8`, or via `View → Detection Identifier`).

![Identification Menu Item](/assets/images/entity_id/Identification%20Menu%20Item.png)

Once registered, entity labels will appear:
- **Blue**: Tracking (skeleton) ID (valid only inside the capture area)
- **Green**: Persistent Entity ID (remains even if the person exits and re-enters the space)

![EntityId and Display Name Labels](/assets/images/entity_id/EntityId%20and%20Display%20Name%20Labels.png)

---

## Editing Entity Display Name
Use can provide a display name for each persistant id.
This can provide an easier way to recognize the identified person.
This entity ID along with the display name is also shared and distributed to all clients (i.e. unreal-engine, unity).

### Option 1: Using Context Menu

1. Right-click on a tracked character in the viewport.
2. Click **Rename Entity Display Name**.

![Edit Display Name and Forget Entity Context Menu](/assets/images/entity_id/Edit%20Display%20Name%20Context%20Menu.png)

3. A dialog will prompt you to type a new display name.

![Edit Display Name DIalog](/assets/images/entity_id/Edit%20Display%20Name%20DIalog.png)

---

### Option 2: Using Main Menu

1. Navigate to: **Identification → Set Display Name**
2. Choose the entity you want to rename.

![Choose Entity for Editing its Display Name](/assets/images/entity_id/Choose%20Entity%20for%20Editing%20its%20Display%20Name.png)

---

## Removing an Entity

### Option 1: Using Context Menu

1. Right-click the character in the viewport.
2. Select **Forget Entity**.

![Edit Display Name and Forget Entity Context Menu](/assets/images/entity_id/Forget%20Entity%20Context%20Menu.png)

3. Confirm the action in the dialog:

![Forget Entity DIalog](/assets/images/entity_id/Forget%20Entity%20DIalog.png)

---

### Option 2: Using Main Menu

1. Navigate to: **Identification → Forget Entity**
2. Select the entity to delete.

![Forget Entity Menu Item](/assets/images/entity_id/Forget%20Entity%20Menu%20Item.png)

---

## Remove All Entities

To delete all saved entities:

1. Navigate to: **Identification → Forget All Entities**
2. Confirm the irreversible action in the dialog:

![Forget All Dialog](/assets/images/entity_id/Forget%20All%20Dialog.png)

---

## Notes

- Registration must be performed with all necessary individuals present and facing the cameras.
- Labels provide a reliable way to confirm identification in real time.
- The system ensures that each entity retains their identity across multiple tracking sessions.

**Do not register the same person twice.** Try to provide a single registration for each person. When a person has more than one registered entity, identification will not provide a coherent output.
{: .warning }
