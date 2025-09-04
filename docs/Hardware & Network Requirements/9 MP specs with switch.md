---
layout: default
title: Multi PC setup - 9MP Camera System
parent: Hardware & Network Requirements
nav_order: 2
---

# Hardware Specifications for MoCap Unleashed - 9MP Camera - Multi PC setup
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---


## Mocap Unleashed: Working with multiple PCs - Capturing a large area / Increased quality
Mocap Unleashed stands as a markerless motion capture solution, leveraging RGB-based cameras and cutting-edge deep-learning algorithms to deliver real-time motion capture results. 
Our system processes data from 8 parallel GigE cameras for each Server, collectively generating 8.7 Gigapixels per server of data per second. This data is then meticulously handled by powerful GPUs. The substantial computational load demands high-end resources.

The hardware specifications of AR 51's Mocap Unleashed system have undergone rigorous testing. It's crucial to emphasize that any compromise in the quality of components could significantly impair the system's performance and speed.

![1.Multi_PC_System_Diagram.jpg](/assets/images/Multi_PC_System_Diagram.jpg)

Using a network switch simplifies wiring by connecting multiple cameras locally, eliminating the need to run individual cables directly to the PC. 
The switch can be placed close to the cameras, linking back to the PC via a single fiber cable. 
**This approach is especially beneficial for multi-PC configurations.**


## PC Specification
Make sure the **motherboard can support a PCIe4 X8 network card and the GPU**: 
<br> * Make sure there is a **free slots for PCIe extension card**.  4090/5080 cards are bulky make sure they do not block other slots. 
<br> * make sure to **acquire two 100Gpbs QSFP28 modules** to the pca as well as for the switch  
{: .warning }


| Component                                                     | Example Type                                                                                                                                       | Information                                                                                                                                                                                                                                            |
|---------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CPU                                                           | Intel Core Ultra 265KF / Tray 1851                                                                                                                 | The CPU should have enough **lanes** to support network cards and the GPU. Should also support DDR5.                                                                                                                                                   |
| Motherboard                                                   | [APEX Z890 MAXIMUS ROG Asus](https://rog.asus.com/motherboards/rog-maximus/rog-maximus-z890-apex/spec/)                                            | Requirements:  <br> - PCI-e 4 for **RTX 4090** <br> - **1x** PCI-e slots for a card (transmits 6GB/s each, **PCIe4 x 8mode** - a minimum for each slot                                                                                                 |
| Cooling                                                       | Corsair Water Cooling H150 RGB 360mm Black                                                                                                         | 4090 without water cooling is very bulky and does not leave space for the 2 pcie cards                                                                                                                                                                 |
| Memory (RAM)                                                  | Corsair **DDR 5** 64G (32x2) 6400Gbps                                                                                                              | Minimum specs: DDR5 5600 MHz   - The system requires a fast memory to transfer these multiple 9MP images to the gpu fast enough                                                                                                                        |
| Storage (HDD)                                                 | M.2 SSD 1.0TB                                                                                                                                      | 512GB should also suffice.  <br> **Do Not Use Sata Harddrive** since it will take bandwith from the PCIe.   <br> Also, make sure to position this SSD on the dedicated **m.2-direct-to-CPU** slot on the motherboard                                   |
| GPU (RTX 4090)                                                | RTX 4090      /    RTX 5080                                                                                                                        | To allow access to the other pcie slots, a watercooled 4090 varient is prefered. When not using water cooling 4090 cards can be bulky and block the other pcie slots. <br> **Ensure the motherboard has space for two additional PCIe network cards.** |
| 10Gb Switch with 2 x 100Gb upload                             | FS.com a 10 Gigabit Ethernet Switch, with 2 x 100Gb QSFP28 Uplinks   [fs.com](https://www.fs.com/products/240831.html?attribute=105744&id=3844337) | The switch aggregates the data from the cameras and sends it to the PC. Per PC, the switch should have **8 10Gige connection and an uplink of 100Gige**.
| PCI-E card by Intel - E810-CAM2 100G Dual-Port QSFP28,        | **PCIe 4.0 x 8,** at the minimum because it needs to transfer 80Gbps   [fs.com](https://www.fs.com/products/141788.html?now_cid=4253)              | To transfer 8 10Gbps cameras using a single interface a PCIe4X8 is hard requirement. (PCIe4x8 max transfer is 128Gbps, where PCIE4x4 max transfer is 64Gbps)
| SFP module for the Switch                                     | [fs.com](https://www.fs.com/products/166442.html)                                                                                                  |                  
| SFP module for the PC                                         | [fs.com](https://www.fs.com/products/35182.html)                                                                                                   |                 
| Fiber Cable                                                   | [fs.com](https://www.fs.com/products/69009.html)                                                                                                   | 


