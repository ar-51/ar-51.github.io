---
layout: default
title: 9MP Camera System
parent: Hardware & Network Requirements
nav_order: 3
---

# Hardware Specifications for MoCap Unleashed - 9MP Camera system
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---


## Mocap Unleashed: Harnessing the Power of 8 Parallel 10GigE Cameras
Mocap Unleashed stands as a markerless motion capture solution, leveraging RGB-based cameras and cutting-edge deep-learning algorithms to deliver real-time motion capture results. Our system processes data from 8 parallel GigE cameras, collectively generating 8.7 Gigapixels of data per second. This data is then meticulously handled by powerful GPUs. The substantial computational load demands high-end resources.

The hardware specifications of AR 51's Mocap Unleashed system have undergone rigorous testing. It's crucial to emphasize that any compromise in the quality of components could significantly impair the system's performance and speed.


## PC Specification
Make sure the **motherboard can support both two network cards and the GPU**: <br> * Make sure there are **free slots for 2 pcie extenstion**.  4090/4080 cards are bulky the do not use water-cooling. <br> * The 2 additional PCIeslots should support a minimum of   **PCIe4 x 4 mode** <br> * Note that the extension example extension card uses  **PCI-e v4.0 x4** and also requrires these [SFP adapters](https://www.alibaba.com/product-detail/LR-LINK-LRXP0010-Y3ATR-10Gb-SFP_1600768803659.html?spm=a2756.order-detail-ta-ta-b.0.0.62332fc2jmW6qL) 
{: .warning }


| Component          | Example Type                                        | Information                                                                        |
|--------------------|-----------------------------------------------------|------------------------------------------------------------------------------------|
| CPU                | Intel Core i9 13900K / 1700 Tray                    | The CPU should have enough **lanes** to support network cards and the GPU. Should also support DDR5.             |
| Motherboard        | 1. [ASUS ROG STRIX Z790-E GAMING WIFI](https://rog.asus.com/motherboards/rog-strix/rog-strix-z790-e-gaming-wifi-model/)   <br> 2. [Asus Prime-x670-p](https://www.asus.com/motherboards-components/motherboards/prime/prime-x670-p/techspec/)                     | Requirements:  <br> - PCI-e 4 for **RTX 4090** <br> - **2x** PCI-e slots for a card (transmits 6GB/s each, **PCIe4 x 4mode** - a minimum for each slo      |
| Water Cooling      | Corsair iCUE H150i RGB PRO XT Liquid CPU Cooler     | 4090 without water cooling is very bulky and does not leave space for the 2 pcie cards|
| Memory (RAM)       | Corsair **DDR 5** 64G (32x2) 5600                       |                                                                 |
| Storage (HDD)      | SSD 1.0TB                                           | 512GB should also suffice.                                                         |
| GPU (RTX 4090)     | [AORUS GeForce RTX™ 4090 XTREME WATERFORCE 24G](https://www.gigabyte.com/Graphics-Card/GV-N4090AORUSX-W-24GD-rev-11#kf)            | To allow access to the other pcie slots, a watercooled 4090 varient is prefered. When not using water cooling 4090 cards can be bulky and block the other pcie slots. <br> **Ensure the motherboard has space for two additional PCIe network cards.**           |
| **2**x PCI-e Network cards | LR-LINK **PCI-e v4.0 x8 Quad Ports** 4 SFP28 (25G Intel E810)   [Amazon](https://www.amazon.com/Quad-Port-SFP28-Ethernet-Network-Adapter/dp/B0D2NFV4JV?ref_=ast_sto_dp), [Alibaba](https://www.alibaba.com/product-detail/LR-LINK-PCI-Express-v4-0_1600768840919.html?spm=a2756.order-detail-ta-ta-b.0.0.62332fc2jmW6qL) <br>
       **8** SFP+ RJ45 **80m** connectors (Efficent Power Consumption) [Amazon.com](https://www.amazon.com/dp/B0C1Z1W8PF?ref=ppx_yo2ov_dt_b_fed_asin_title&th=1),[Amazon.co.jp](https://www.amazon.co.jp/gp/product/B0BRKQNZJX/ref=ppx_yo_dt_b_asin_title_o00_s00?ie=UTF8&th=1) [fs.com](https://www.fs.com/products/154924.html?attribute=95101&id=3757118)           | **PCI-e v4.0** cards are required  | These type of connectors can get very hot. We recommend purchasing the 80m types of connectors since they have lower power consumption.

