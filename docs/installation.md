---
layout: default
title: Installation
nav_order: 4
---

# PuppetPC Installation Manual
{: .no_toc }

This guide provides step-by-step instructions for installing PuppetPC on your system.
{: .fs-6 .fw-300 }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Prerequisites
Before beginning the installation process, ensure that your system meets the following requirements:
- A stable internet connection.
- Administrative access to your computer.

## Installation on Windows
1. **Download the Installer:** Visit the PuppetPC website and download the [Windows installer](https://api.puppetpc.com/manage/static/release/puppetpc-windows-amd64.exe).
2. **Run the Installer:** Find the downloaded `.exe` file and double-click it to initiate the installation.
3. **Verify Installation:** A terminal window will open, indicating PuppetPC is operational. Keep this terminal window open to sustain the connection.
4. **Control Interface:** The control interface will launch in your default web browser.

## Installation on Linux (PC)
1. **Open Terminal:** Launch your terminal.
2. **Download and Install:** Use the following command to download and install PuppetPC:
```
curl https://api.puppetpc.com/manage/static/release/puppetpc_48.0.0-1_amd64.deb --output puppetpc_48.0.0-1_amd64.deb && sudo dpkg -i puppetpc_48.0.0-1_amd64.deb
```
3. **Verify Installation:** Confirm PuppetPC is running correctly:
```
systemctl status puppetpc
```

## Installation on Raspberry Pi (RPI)
1. **Open Terminal on RPI** 
2. **Download and Install:** Choose the command based on your RPI's architecture:
- For RPI running a 32-bit OS:
  ```
  curl https://api.puppetpc.com/manage/static/release/puppetpc_48.0.0-1_armhf.deb --output puppetpc_48.0.0-1_armhf.deb && sudo dpkg -i puppetpc_48.0.0-1_armhf.deb
  ```
- For RPI running a 64-bit OS:
  ```
  curl https://api.puppetpc.com/manage/static/release/puppetpc_48.0.0-1_arm64.deb --output puppetpc_48.0.0-1_arm64.deb && sudo dpkg -i puppetpc_48.0.0-1_arm64.deb
  ```
3. **Verify Installation:**
```
systemctl status puppetpc
```

## Installation on NVIDIA Jetson
1. **Open Terminal on Jetson** 
2. **Download and Install:** 
```
curl https://api.puppetpc.com/manage/static/release/puppetpc_48.0.0-1_arm64.deb --output puppetpc_48.0.0-1_arm64.deb && sudo dpkg -i puppetpc_48.0.0-1_arm64.deb
```
3. **Verify Installation:** 
```
systemctl status puppetpc
```

For support, visit the [PuppetPC official website](https://www.puppetpc.com).
