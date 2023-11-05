---
layout: default
title: Hardware Requirments and Specifications 
nav_order: 12
---

# Hardware Specifications for MoCap Unleashed 
{: .no_toc }

This document outlines the recommended hardware specifications for running Mocap Unleashed
{: .fs-6 .fw-300 }



---
## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}



## Mocap Unleashed: Harnessing the Power of 8 Parallel GigE Cameras
Mocap Unleashed stands as a markerless motion capture solution, leveraging RGB-based cameras and cutting-edge deep-learning algorithms to deliver real-time motion capture results. Our system processes data from 8 parallel GigE cameras, collectively generating between 4.7 to 8.7 Gigapixels of data per second. This data is then meticulously handled by powerful GPUs. The substantial computational load demands high-end resources.

The hardware specifications of AR 51's Mocap Unleashed system have undergone rigorous testing. It's crucial to emphasize that any compromise in the quality of components could significantly impair the system's performance and speed.

## PC Specs: 
### 5MP camera system:


| Component          | Example Type                                        | Information                                                                        |
|--------------------|-----------------------------------------------------|------------------------------------------------------------------------------------|
| CPU                | Intel Core i9 13900K / 1700 Tray                    | The CPU should have enough **lanes** to support network cards and the GPU.         |
| Motherboard        | [Gigabyte Z790 AORUS ELITE AX](https://www.gigabyte.com/Motherboard/Z790-AORUS-ELITE-AX-rev-10/sp#sp)                        | Requirements:  <br> - PCI-e 4 for **RTX 4090**  <br>                - **2x** PCI-e slots for Ethernet extension cards (3GByte/s each, **PCIe3 x 4 mode**)                                     |
| Memory (RAM)       | DDR5 64GB (32x2) 5200 Corsair                       | Minimum speed: 4000                                                                |
| Storage (HDD)      | SSD 1.0TB                                           | 512GB should also suffice.                                                         |
| GPU (RTX 4090)     | Gigabyte RTX 4090 GV-N4090GAMING OC-24GD            | When not using water cooling 4090 cards can be bulky. <br> **Ensure the motherboard has space for two additional PCIe network cards.**           |
| 2 PCI-e Netw cards | Intel x710-t4 PCI-Express x8 10Gbe RJ45             | 2x PCIe network cards with 4x ports (10Gbps each, RJ45 or SFP+). <br>  [Link to a verified supplier](https://www.alibaba.com/product-detail/Intel-x710-t4-PCI-Express-x8_62473433376.html?spm=a2756.order-detail-ta-ta-b.0.0.72712fc29ZCC0S).                        |



### 9MP camera system:


| Component          | Example Type                                        | Information                                                                        |
|--------------------|-----------------------------------------------------|------------------------------------------------------------------------------------|
| CPU                | Intel Core i9 13900K / 1700 Tray                    | The CPU should have enough **lanes** to support network cards and the GPU.             |
| Motherboard        | 1. [ASUS ROG STRIX Z790-E GAMING WIFI](https://rog.asus.com/motherboards/rog-strix/rog-strix-z790-e-gaming-wifi-model/)   <br> 2. [Asus Prime-x670-p](https://www.asus.com/motherboards-components/motherboards/prime/prime-x670-p/techspec/)                     | Requirements:  <br> - PCI-e 4 for **RTX 4090** <br> - **2x** PCI-e slots for a card (transmits 6GB/s each, **PCIe4 x 4mode** - a minimum for each slo      |
| Water Cooling      | Corsair iCUE H150i RGB PRO XT Liquid CPU Cooler     | 4090 without water cooling is very bulky and does not leave space for the 2 pcie cards|
| Memory (RAM)       | Corsair DDR 5 64G (32x2) 5200                       | Minimum speed: 4000                                                                |
| Storage (HDD)      | SSD 1.0TB                                           | 512GB should also suffice.                                                         |
| GPU (RTX 4090)     | Gigabyte RTX 4090 GV-N4090GAMING OC-24GD            | When not using water cooling 4090 cards can be bulky. <br> **Ensure the motherboard has space for two additional PCIe network cards.**           |
| 2 PCI-e Netw cards | LR-LINK PCI-e v4.0 x8 Quad Ports 4 SFP28 25G Intel E810 <br>      +8 SFTP RJ45 connectors           |[Link to a verified supplier](https://www.alibaba.com/product-detail/LR-LINK-PCI-Express-v4-0_1600768840919.html?spm=a2756.order-detail-ta-ta-b.0.0.62332fc2jmW6qL)  <br> [Link to a verified supplier](https://www.alibaba.com/product-detail/LR-LINK-LRXP0010-Y3ATR-10Gb-SFP_1600768803659.html?spm=a2756.order-detail-ta-ta-b.0.0.62332fc2jmW6qL) |


### 1.3MP camera system:


| Component            | Example Type                            | Information                                                                                                      |
|----------------------|-----------------------------------------|------------------------------------------------------------------------------------------------------------------|
| CPU                  | Intel i7-13700F (or similar)            | The CPU should have enough lanes to handle network cards and GPU data transfer. |
| Motherboard          | | Requirements:<br> - PCI-e 4 that can handle RTX 4070 <br> - Alternative 1: 1x PCI-e  slots for 10Gige Ethernet extension cards (**PCIe3 x 4 mode**) <br> - Alternative 2: A motherboard with an extra 10G port. | 
| Memory (RAM)         | DDR5 64G (32x2) 5200 Corsair            | Minimum speed: 4000                                                                                              |
| Storage (HDD)        | SSD 1.0TB<br>512GB should also suffice. |                                                                                                                 |
| GPU - NVidia RTX4070 | Gigabyte RTX 4070                       | Any RTX 4070 will do. Make sure the board has room for the 10-Gige Ethernet card.                                |
| PCI-e Network cards  | TPlink - 10Gige card                    | For computers with fast USB (Thunderbolt or USB3.2 Gen2), a USB-to-10Gige connector can be used instead of the PCI network adapter.|
| Network Switch       | (Netgear MS510TXPP)[https://www.amazon.com/NETGEAR-Multi-Gigabit-Managed-Uplinks-MS510TXPP/dp/B075Q5T7NH?th=1] | The switch should have **8 1Gige connection and an uplink of 10Gige** to the PC. The camera port should also be sfp+ to provide **POE** (power-over-ethernet). |

* For computers equipped with high-speed USB interfaces like Thunderbolt or **USB 3.2 Gen2**, consider using a USB-to-10GigE adapter, (such as this)[https://www.sonnettech.com/product/solo10g-tb3/overview.html], as an alternative to the PCI-e network adapter.

## Calibration Sphere
The sphere used for calibration should emit **a strong white light** at least 1800 Lumen.  

[Link to a verified supplier](https://www.amazon.de/-/en/Trango-Garden-Diameter-Outdoor-Lighting/dp/B00J1OL9IS/ref=sr_1_12?crid=2IMCIF6JZFXY6&keywords=gartenleuchte+kugel+40+cm&qid=1674556426&sprefix=garden+light+ball+40+cm%2Caps%2C141&sr=8-12)