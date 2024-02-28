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

<h3>All Downloads</h3>
<ul class="list-group">
    <li class="list-group-item">Windows: <a href="/downloads/windows/package.exe">Download .exe</a></li>
    <li class="list-group-item">MacOS: <a href="/downloads/macos/package.dmg">Download .dmg</a></li>
    <li class="list-group-item">Linux: <a href="/downloads/linux/package.tar.gz">Download .tar.gz</a></li>
    <!-- Add more OS-specific downloads as needed -->
</ul>

<script>
document.addEventListener('DOMContentLoaded', function() {
    var os = "Unknown OS";
    var downloadLink = "";
    var downloadText = "";
    var guideLink = "/docs/installation.html";

    if (navigator.appVersion.indexOf("Win") != -1) { os = "Windows"; downloadLink = "/downloads/windows/package.exe"; downloadText = "Download for Windows"; }
    if (navigator.appVersion.indexOf("Mac") != -1) { os = "MacOS"; downloadLink = "/downloads/macos/package.dmg"; downloadText = "Download for MacOS"; }
    if (navigator.appVersion.indexOf("X11") != -1 || navigator.appVersion.indexOf("Linux") != -1) { os = "Linux"; downloadLink = "/downloads/linux/package.tar.gz"; downloadText = "Download for Linux"; }

    var suggestedDownloadCard = document.getElementById('suggestedDownload');
    suggestedDownloadCard.innerHTML = `
        <div class="card-body">
            <h2 class="card-title">Suggested Download for ${os}</h5>
            <br>
            <a href="${downloadLink}" class="btn btn-primary">${downloadText}</a>
            <p class="card-text"><a href="${guideLink}">View Installation Guide</a></p> <!-- Link to the installation guide -->
        </div>
    `;
});
</script>


