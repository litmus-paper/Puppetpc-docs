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
1. **Download the Installer:** Go to the PuppetPC website and download the [Windows installer](https://api.puppetpc.com/manage/static/release/puppetpc-windows-amd64.exe).
2. **Run the Installer:** Locate the downloaded `.exe` file and double-click to start the installation.
3. **Verify Installation:** A terminal window should open indicating that PuppetPC is running. Keep the terminal window open to maintain the connection.
4. **Control Interface:** The control interface will open in the default web browser.

## Installation on Linux on PC
1. **Open Terminal:** Open your terminal.
2. **Download and Install:** 
```
curl https://api.puppetpc.com/manage/static/release/puppetpc_16-1_amd64.deb --output puppetpc_16-1_amd64.deb && sudo dpkg -i puppetpc_16-1_amd64.deb
```
3. **Verify Installation:** 
```
systemctl status puppetpc
```

## Installation on Raspberry Pi (RPI)
1. **Open Terminal on RPI:** 
2. **Download and Install:** 
- For RPI 32 bit:
```
curl https://api.puppetpc.com/manage/static/release/puppetpc_16-1_armhf.deb --output puppetpc_16-1_armhf.deb && sudo dpkg -i puppetpc_16-1_armhf.deb
```
- For RPI 64 bit:
```
curl https://api.puppetpc.com/manage/static/release/puppetpc_16-1_arm64.deb --output puppetpc_9.2_arm64.deb && sudo dpkg -i puppetpc_16-1_arm64.deb
```
3. **Verify Installation:**
```
systemctl status puppetpc
```

## Installation on NVIDIA Jetson
1. **Open Terminal on Jetson:** 
2. **Download and Install:** 
```
curl https://api.puppetpc.com/manage/static/release/puppetpc_16-1_arm64.deb --output puppetpc_9.2_arm64.deb && sudo dpkg -i puppetpc_16-1_arm64.deb
```
3. **Verify Installation:** 
```
systemctl status puppetpc
```

## Post-Installation Steps
1. **Configuration:** Configure PuppetPC as needed for your specific use case.
2. **Test the Connection:** Ensure that PuppetPC is functioning correctly by establishing a test connection.

## Troubleshooting
- Ensure your system meets all prerequisites.
- Review installation steps for accuracy.
- For specific error messages or issues, consult the PuppetPC support forum or help center.

For more detailed instructions and support, visit the [PuppetPC official website](https://www.puppetpc.com).