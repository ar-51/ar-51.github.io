---
layout: default
title: Configuring fs.com Switch for 100G Connection
parent: Network Setup
nav_order: 2
---

# Configure fs.com Switch
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Goal

The goal of the steps below is to configure the switch so it will be able to upload **100G** to your server using the **SFP28 interface**.

## Steps Before Using the Switch

### Step 1: Connect the Fiber Optic Cable

- Connect the fiber optic cable to the **server** and to **port 25 or 26** in your switch.

### Step 2: Connect a Laptop for Configuration

- Use an **ethernet cable** to connect your laptop directly to the switch.
- The switch has a port marked **MGT (management)**. Connect the cable there and to your laptop.
- Once configuration is done, this cable can be disconnected.
![Management Port Screenshot](/assets/images/network setup/configure_the_switch/switch_managment_port.png)

### Step 3: Set Laptop IP Address

- By default, the switch uses IP **192.168.1.1**.
- Set your laptop LAN IP to the same range (e.g., **192.168.1.10**).

### Step 4: Access the Web Management Interface

- Open a browser and navigate to **192.168.1.1**.
- You should see the **web-based management system** of the switch.

### Step 5: Login to Web Interface

- Use the following credentials:
  - **User:** admin
  - **Password:** admin

![web_login_screen.png](/assets/images/network setup/configure_the_switch/web_login_screen.png)

---

## Switch Configuration via Terminal

### Step 6: Open a Terminal

- On the **server**: open a terminal.
- On your **laptop**: open **PuTTY** (or another SSH client).
- Connect to the switch:
  ```bash
  ssh admin@192.168.1.1
  ```
- Password: **admin**

![ssh.png](/assets/images/network setup/configure_the_switch/ssh.png)

### Step 7: Identify the 100G Interfaces

- The switch has two **100G interfaces**: port **25** and port **26**.

### Step 8: Configure Ports via SSH

Run the following commands:

```bash
configure terminal

interface eth-0-25
shutdown
no shutdown
speed 100g
duplex full 
fec rs
exit

interface eth-0-26
shutdown
no shutdown
speed 100g
duplex full 
fec rs
exit

write memory
reload
```

- Press **Enter** to confirm the reboot.

---

## Verification

- After reboot, login again to the **web interface**.
- Ports should show a **color change**, indicating successful connection.

![port_display.png](/assets/images/network setup/configure_the_switch/port_display.png)

---

## Summary

By following these steps, you can configure the **fs.com switch** to support **100G connectivity** on your server using the **SFP28 interface**.
