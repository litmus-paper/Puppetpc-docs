---
layout: page
title: Download
# permalink: /download/
nav_order: 2
---


<style>

    .card {
        background-color: #ffffff;
        margin-bottom: 20px;
        padding: 20px;
        border-radius: 8px;
        box-shadow: 0 2px 4px rgba(0,0,0,0.1);
        text-align: center; 
    }
    .card-highlight {
position: relative;
border: 2px solid transparent; /* Make the border transparent */
background: linear-gradient(#ffffff, #ffffff) padding-box, linear-gradient(#6f55d5, #5739ce) border-box;
box-shadow: 0 0 0 2px var(--border-gradient, linear-gradient(#6f55d5, #5739ce)) inset;
}
    .card-title {
        font-size: 24px;
        margin-bottom: 10px;
    }
    .card-text {
        font-size: 16px;
        margin-bottom: 20px;
    }
    .btn {
        display: inline-block;
        padding: 10px 20px;
        /* background-color: #007bff;
        color: #ffffff; */
        text-decoration: none;
        border-radius: 5px;
    }
    .list-group {
        list-style: none;
        padding: 0;
    }
    .list-group-item {
        background-color: #ffffff;
        margin-bottom: 10px;
        padding: 10px;
        border-radius: 5px;
    }
    .list-group-item a {
        text-decoration: none;
        /* color: #007bff; */
    }
</style>


<div class="card card-highlight" id="suggestedDownload">
    <!-- Suggested download card content will be inserted here by JavaScript -->
</div>

## All Downloads
### Windows
* [Download .exe](https://api.puppetpc.com/manage/static/release/puppetpc-windows-amd64.exe)

### Mac
* [Download for Mac OS amd64](https://api.puppetpc.com/manage/static/release/puppetpc-darwin-amd64)
* [Download for Mac OS arm64](https://api.puppetpc.com/manage/static/release/puppetpc-darwin-arm64)  

### Debian Linux
Use this for Ubuntu, Linux Mint, Raspbian, Kali Linux, and other Debian-based Linux distributions.  
* [Download for PC-based machines](https://api.puppetpc.com/manage/static/release/puppetpc_48.0.0-1_amd64.deb)  
* [Download for ARM64 devices, like Raspberry Pi 4 and NVIDIA Jetson](https://api.puppetpc.com/manage/static/release/puppetpc_48.0.0-1_arm64.deb) 
* [Download for ARM32 devices, like older Raspberry Pi models running a 32-bit OS](https://api.puppetpc.com/manage/static/release/puppetpc_48.0.0-1_armhf.deb)  

### Red Hat Linux
* [Download for PC-based machines](https://api.puppetpc.com/manage/static/release/puppetpc-48.0.0-2.x86_64.rpm)
* [Download for ARM64 devices](https://api.puppetpc.com/manage/static/release/puppetpc-48.0.0-2.arm64.rpm)
* [Download for ARM32 devices](https://api.puppetpc.com/manage/static/release/puppetpc-48.0.0-2.amdhf.rpm)

### Other Linux Distributions
Use the following executables for other Linux distributions like Arch Linux, Slackware, and Gentoo.
* [Download for PC-based machines](https://api.puppetpc.com/manage/static/release/puppetpc-linux-amd64)
* [Download for ARM64 devices](https://api.puppetpc.com/manage/static/release/puppetpc-linux-arm64)
* [Download for ARM32 devices](https://api.puppetpc.com/manage/static/release/puppetpc-linux-arm32)


<script>
document.addEventListener('DOMContentLoaded', function() {
    let os = "Windows";
    let downloadLink = "https://api.puppetpc.com/manage/static/release/puppetpc-windows-amd64.exe";
    let downloadText = "Download for Windows";
    let arch = "amd64";

    if (navigator.appVersion.indexOf("Win") !== -1) {
        os = "Windows";
        downloadLink = "https://api.puppetpc.com/manage/static/release/puppetpc-windows-amd64.exe";
        downloadText = "Download for Windows";
    } 
    else if (navigator.appVersion.indexOf("Mac") !== -1) {
        os = "MacOS";
        arch = navigator.userAgent.indexOf("arm64") !== -1 ? "arm64" : "amd64";
        downloadLink = `https://api.puppetpc.com/manage/static/release/puppetpc-darwin-${arch}`;
        downloadText = `Download for MacOS (${arch})`;
    } 
    else if (navigator.appVersion.indexOf("X11") !== -1 || navigator.appVersion.indexOf("Linux") !== -1) {
        os = "Linux";
        if (navigator.userAgent.indexOf("arm64") !== -1) {
            arch = "arm64";
            downloadLink = "https://api.puppetpc.com/manage/static/release/puppetpc_48.0.0-1_arm64.deb";
            downloadText = "Download for Linux (ARM64)";
        } 
        else if (navigator.userAgent.indexOf("armhf") !== -1) {
            arch = "armhf";
            downloadLink = "https://api.puppetpc.com/manage/static/release/puppetpc_48.0.0-1_armhf.deb";
            downloadText = "Download for Linux (ARM32)";
        } 
        else {
            arch = "amd64";
            downloadLink = "https://api.puppetpc.com/manage/static/release/puppetpc_48.0.0-1_amd64.deb";
            downloadText = "Download for Linux (AMD64)";
        }
    }

    var suggestedDownloadCard = document.getElementById('suggestedDownload');
    suggestedDownloadCard.innerHTML = `
        <div class="card-body">
            <h2 class="card-title">Suggested Download for ${os}</h2>
            <br>
            <a href="${downloadLink}" class="btn btn-primary">${downloadText}</a>
            <p class="card-text"><a href="installation.html">View Installation Guide</a></p>
        </div>
    `;
});
</script>


