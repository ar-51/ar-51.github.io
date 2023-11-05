---
layout: default
title: Hardware Requirments and Specifications 
nav_order: 9 
---

# Hardware Specifications for MoCap Unleashed 
{: .no_toc }

This document contains hardware specification of recommanded hardware to run Mocap-Unleashed
{: .fs-6 .fw-300 }



---
## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}



## Mocap Unleashed process 8 parallel streams Gige cameras 
Mocap Unleashed is a markerless motion capture solution that utilizes RGB-based cameras, along with advanced deep-learning and computer-vision algorithms to generate real-time output. 
Our GigE-cameras collectively produce between 4.7 Gigapixels to 8.7 Gigapixels of data per second, which is then processed by the GPUs. 
As a result, the computation demands substantial resources.


The PC hardware specifications of AR 51's Mocap Unleashed system have been rigorously tested. 
It is important to note that compromising the quality of any components may lead to a decrease in the system's performance and speed.

## Specs: 
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
| Motherboard        | [ASUS ROG STRIX Z790-E GAMING WIFI](https://rog.asus.com/motherboards/rog-strix/rog-strix-z790-e-gaming-wifi-model/)   <br> [Asus Prime-x670-p](https://www.asus.com/motherboards-components/motherboards/prime/prime-x670-p/techspec/)                     | Requirements:  <br> - PCI-e 4 for **RTX 4090** <br> - **2x** PCI-e slots for a card (transmits 6GB/s each, **PCIe4 x 4mode** - a minimum for each slo      |
| Memory (RAM)       | Corsair DDR 5 64G (32x2) 5200                       | Minimum speed: 4000                                                                |
| Storage (HDD)      | SSD 1.0TB                                           | 512GB should also suffice.                                                         |
| GPU (RTX 4090)     | Gigabyte RTX 4090 GV-N4090GAMING OC-24GD            | When not using water cooling 4090 cards can be bulky. <br> **Ensure the motherboard has space for two additional PCIe network cards.**           |
| 2 PCI-e Netw cards | LR-LINK PCI-e v4.0 x8 Quad Ports 4 SFP28 25G Intel E810 <br>      +8 SFTP RJ45 connectors           |[Link to a verified supplier](https://www.alibaba.com/product-detail/LR-LINK-PCI-Express-v4-0_1600768840919.html?spm=a2756.order-detail-ta-ta-b.0.0.62332fc2jmW6qL)  <br> [Link to a verified supplier](https://www.alibaba.com/product-detail/LR-LINK-LRXP0010-Y3ATR-10Gb-SFP_1600768803659.html?spm=a2756.order-detail-ta-ta-b.0.0.62332fc2jmW6qL) |



## Calibration Sphere
The sphere used for calibration should emit **a strong white light** at least 1800 Lumen.  

[Link to a verified supplier](https://www.amazon.de/-/en/Trango-Garden-Diameter-Outdoor-Lighting/dp/B00J1OL9IS/ref=sr_1_12?crid=2IMCIF6JZFXY6&keywords=gartenleuchte+kugel+40+cm&qid=1674556426&sprefix=garden+light+ball+40+cm%2Caps%2C141&sr=8-12)