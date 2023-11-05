---
layout: default
title: 5MP camera system
parent: Hardware Specs
nav_order: 1
---

# Hardware Specifications for MoCap Unleashed - 5MP Camera system
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---


## Mocap Unleashed: Harnessing the Power of 8 Parallel 5GigE Cameras
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

