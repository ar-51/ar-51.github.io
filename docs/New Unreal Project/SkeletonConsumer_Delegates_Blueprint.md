---
layout: default
title:  SkeletonConsumer - Multicast Delegate Reference
parent: New Unreal Project
nav_order: 10
---

# SkeletonConsumer - Multicast Delegate Reference
{: .no_toc }

Outline all **Multicast Delegates** (BlueprintAssignable events) exposed by the `USkeletonConsumer`
{: .fs-6 .fw-300 }


---
## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

This document outlines all **Multicast Delegates** (BlueprintAssignable events) exposed by the `USkeletonConsumer` component in the AR 51 Unreal SDK.

These events allow developers to hook into key lifecycle updates of tracked persons and manage real-time mocap interactions.

---

## Person Tracking Events

### `OnPersonDetected`
Triggered when a new person is detected in the capture area for the first time.

```cpp
UPROPERTY(BlueprintAssignable, Category = "Events")
FOnPersonDetected OnPersonDetected;
```

- **Parameter**: `FString PersonId`
- **Use Case**: Initialize logic or UI feedback when a new participant enters the stage.

---

### `OnPersonUpdated`
Fired when skeleton data for a tracked person is updated.

```cpp
UPROPERTY(BlueprintAssignable, Category = "Events")
FOnPersonUpdated OnPersonUpdated;
```

- **Parameter**: `FString PersonId`
- **Use Case**: Use for visual feedback or real-time analytics during motion.

---

### `OnPersonTrackingLost`
Broadcast when tracking is lost for a currently tracked person.

```cpp
UPROPERTY(BlueprintAssignable, Category = "Events")
FOnPersonTrackingLost OnPersonTrackingLost;
```

- **Parameter**: `FString PersonId`

---

### `OnPersonTrackingRecovered`
Fired when tracking is regained after a previous loss.

```cpp
UPROPERTY(BlueprintAssignable, Category = "Events")
FOnPersonTrackingRecovered OnPersonTrackingRecovered;
```

- **Parameter**: `FString PersonId`

---

### `OnPersonDestroyed`
Broadcast when a person is fully removed from the system (prolonged tracking loss).

```cpp
UPROPERTY(BlueprintAssignable, Category = "Events")
FOnPersonDestroyed OnPersonDestroyed;
```

- **Parameter**: `FString PersonId`

---

## Active Person Management

### `OnActivePersonChanged`
Called when the person closest to the headset changes.

```cpp
UPROPERTY(BlueprintAssignable, Category = "Events")
FOnActivePersonChanged OnActivePersonChanged;
```

- **Parameter**: `FString PersonId` (empty string if no one is active)

---

## Component Lifecycle Events

### `OnComponentActivated`
Triggered when this component is activated.

```cpp
UPROPERTY(BlueprintAssignable, Category = "Events")
FOnComponentActivated OnComponentActivated;
```

---

### `OnComponentDeactivated`
Triggered when this component is deactivated.

```cpp
UPROPERTY(BlueprintAssignable, Category = "Events")
FOnComponentDeactivated OnComponentDeactivated;
```

---

## Editor Screenshots

### Details Panel View
This screenshot shows the assignable events in the **Details Panel** of a Blueprint.

![SkeletonConsumer Events](/assets/images/SkeletonConsumer_Multicast_Delegate_Reference/SkeletonConsumerDetailsPanelEvents.png)

---

### Blueprint Binding Example
An example Blueprint setup using **BeginPlay** to bind to `OnPersonDetected`.

![OnPersonDetected Binding](/assets/images/SkeletonConsumer_Multicast_Delegate_Reference/OnPersonDetectedBlueprint.png)


---

## Notes
- Binding should typically occur in `BeginPlay`, and unbinding (if needed) in `EndPlay`.
- Always validate `PersonId` before using it.
- Use these events to integrate with your gameplay, UI, analytics, or telemetry.

---

For full documentation, visit the [AR 51 Dev Portal](https://docs.ar-51.com/).
