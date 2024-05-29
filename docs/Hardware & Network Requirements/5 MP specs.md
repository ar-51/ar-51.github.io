---
layout: default
title: 5MP Camera System
parent: Hardware & Network Requirements
nav_order: 2
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

## PC Specification

Make sure the **motherboard can support both two network cards and the GPU**: <br> * Make sure there are **free slots for 2 pcie extenstion**.  4090/4080 cards are bulky the do not use  water-cooling. <br> * The 2 additional PCIeslots should support a minimum of   **PCIe3 x 4 mode**
{: .warning }


| Component          | Example Type                                        | Information                                                                        |
|--------------------|-----------------------------------------------------|------------------------------------------------------------------------------------|
| CPU                | Intel Core i9 13900K / 1700 Tray                    | The CPU should a minimum of  **20 pcie lanes ** to support network cards and the GPU.         |
| Motherboard        | [Gigabyte Z790 AORUS ELITE AX](https://www.gigabyte.com/Motherboard/Z790-AORUS-ELITE-AX-rev-10/sp#sp)                        | Requirements:  <br> - PCI-e 4 for **RTX 4090**  <br>                - **2x** PCI-e slots for Ethernet extension cards (3GByte/s each, **PCIe3 x 4 mode**)                                     |
| Memory (RAM)       | DDR5 64GB (32x2) 5200 Corsair                       | Minimum speed: 4000                                                                |
| Storage (HDD)      | SSD 1.0TB                                           | 512GB should also suffice.                                                         |
| GPU (RTX 4080)     | Gigabyte RTX 4080                                   | When not using water cooling 4090 cards can be bulky. <br> **Ensure the motherboard has space for two additional PCIe network cards.**           |
| Water Cooling      | Corsair iCUE H150i RGB PRO XT Liquid CPU Cooler     | 4090 without water cooling is very bulky and does not leave space for the 2 pcie cards|
| 2x PCI-e Netw cards | [Intel x710-t4 PCI-Express x8 10Gbe RJ45](https://www.alibaba.com/product-detail/Intel-x710-t4-PCI-Express-x8_62473433376.html?spm=a2756.order-detail-ta-ta-b.0.0.72712fc29ZCC0S)  <br> Quad-port 5G **POE+** Framer Grabber [Amazon](https://www.amazon.com/LRES1052PT/dp/B0D3DMK47T?ref_=ast_sto_dp) [Alibaba] (https://www.alibaba.com/product-detail/LR-LINK-PCIe-3-0-x4_1601150383177.html?spm=a2756.trade-list-buyer.0.0.152876e9tMz8iX)          | 2x PCIe network cards with 4x ports (5Gbps each, RJ45 or SFP+).                        |

