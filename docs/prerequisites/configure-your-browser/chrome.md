---
title: Chrome
page_title: Configure Chrome for Test Studio Automation
description: "Configure Chrome to use for testing with Test Studio. Prerequisites for testing against Chrome with Test Studio. Install Chrome extension for Test Studio testing."
position: 1
---

# Configuring Chrome for Test Studio Automation 

This document describes the steps to enable Chrome browser for test recording and execution.

## 1. Enable Chrome for Automation

In __Test Studio release 2022 R1__ (v.2022.1.xx) you can choose how to record and execute tests with Chrome browser. In this version it can be enabled for automation with or without the Progress Test Studio Extension. The setting how Chrome will be used is set on project level, which means that you can use both options at the same time depending on the project you work from.

### Enable Chrome for Automation with Extension

By default each Test Studio project is set to use Chrome with the extension. So, if this is the option you want to use, you need to install the latest <a href="https://chrome.google.com/webstore/detail/progress-test-studio-exte/gegcllkonmciadpdldechnepmjildoan" target="_blank">__Progress Telerik Test Studio Extension__</a> from the Chrome Web Store.

### Enable Chrome for Automation without Extension

If you choose to use Chrome for recording and execution without additional extension, you need to __change a setting in the Test Studio project__. The <a href="/features/project-settings/overview" target="_blank">project setting</a> is listed under the __Browsers__ tab and is named __Use browser extension__ (it is enabled by default). __Uncheck the checkbox__ and Test Studio will __start the Chrome browser for this project without using the extensions__ even if this is installed.

![Disable UseBrowserExtension](/img/prerequisites/browser-config/disable-extension.png)

## 2. Browser Calibration

To ensure a flawless and consistent automation process, there are a few browser settings that we need to apply. We call this **browser calibration** and have implemented a feature to <a href="/features/project-settings/browsers" target="_blank">**automatically calibrate the browser**</a> out of the box. No manual interaction is required.<br><br>

> __Important__
> <br>
> <br>
> <p>If your Chrome browser has an active <strong>Google Apps session</strong> (for example, you are logged into GMail), automatic calibration will not work as expected. To use automatic configuration, log out of your Google account first.</p><p></p>
<p></p>

> __Tip__
> <br>
> <br>
> You can check all settings applied from the calibration in the <a href="#Manual_Configuration">Manual Configuration</a> section below (click the + sign to expand it).<br><br>

<p><hr></p>
<p></p>
<p></p>

<p class="trigger"><a name="Extension_Install" style="color:black; text-decoration: none;";> Extension Install Procedure <span id="d" style="color:#28a1e2";> + </span></a></p>

<div class="toggle_container">
<div class="block">

<hr/>
<br>


1.&nbsp; When you start recording against Chrome, but the Progress extension is not installed, the browser will load the recording start page and will try to load the extension. The recorder will search for the extension for the period that is defined in the *ClientReady* Timeout (the default is 60 seconds).<br><br>

<img src="/img/general-information/configure-your-browser/chrome/fig14.png" alt="Wait For Extension"><br><br>

2.&nbsp; If the Progress extension doesn't load within the timeout period, a link to the Web Store will be displayed to install the extension.<br><br>

<img src="/img/general-information/configure-your-browser/chrome/fig10.png" alt="Get Extension"><br><br>

3.&nbsp; By clicking on <strong>Get It Free From Chrome Web Store</strong>, you will be redirected to the Progress extension in the Web Store.<br><br>

<img src="/img/general-information/configure-your-browser/chrome/fig11.png" alt="Extension In Store"><br><br>

4.&nbsp; By clicking the <strong>Add to Chrome</strong> button, the extension will be added after confirmation. <br><br>

<img src="/img/general-information/configure-your-browser/chrome/fig12.png" alt="Add Extension Confirmation"><br><br>

5.&nbsp; Click on the icon located to the right of the address bar to find the extension's version. <br><br>

<img src="/img/general-information/configure-your-browser/chrome/fig13.png" alt="Extension Version"><br><br>

<hr/>

</div>
</div>
<p></p>
<p></p>
<p></p>

<p class="trigger"><a name="Manual_Configuration" style="color:black; text-decoration: none;";> Manual Configuration <span id="d" style="color:#28a1e2";> + </span></a></p>

<div class="toggle_container">
<div class="block">

<hr/>
<br>

Follow the steps below to manually configure Chrome for web automation with Test Studio.

<h3>Enable Extensions</h3>

1.&nbsp; Click on <img src="/img/general-information/configure-your-browser/chrome/fig1.png" alt="chrome settings button"> located in the upper right corner of the browser. Then select <strong>More tools > Extensions</strong>.<br><br>

2.&nbsp; Ensure that the <strong>Progress Test Studio Extension</strong> is enabled.<br><br>

<img src="/img/general-information/configure-your-browser/chrome/fig2.png" alt="Extensions"><br><br>

<h3>Zoom Level Set to 100%</h3>

1.&nbsp; Click on <img src="/img/general-information/configure-your-browser/chrome/fig1.png" alt="chrome settings button"> in the upper right corner.<br><br>

2.&nbsp; Use the plus (+) and minus (-) buttons next to <strong>Zoom</strong> to set it to 100% (or use the keyboard shortcut: Ctrl + 0).<br><br> 

<img src="/img/general-information/configure-your-browser/chrome/fig3.png" alt="Zoom"><br><br>

<h3>Enable File Downloads</h3>

1.&nbsp; Click on <img src="/img/general-information/configure-your-browser/chrome/fig1.png" alt="chrome settings button"> in the upper right corner.<br><br>

2.&nbsp; Select <strong>Settings</strong> from the drop-down menu.<br><br>

3.&nbsp; Scroll to the bottom and click <strong>Advanced</strong>.<br><br>

4.&nbsp; Locate the <strong>Downloads</strong> section.<br><br>

5.&nbsp; Enable <strong>Ask where to save each file before downloading</strong>.<br><br>

<img src="/img/general-information/configure-your-browser/chrome/fig4.png" alt="Downloads"><br><br>

<h3>Disable Pop-up Blocker</h3>

1.&nbsp; Click on <img src="/img/general-information/configure-your-browser/chrome/fig1.png" alt="chrome settings button"> in the upper right corner.<br><br>

2.&nbsp; Select <strong>Settings</strong> from the drop-down menu.<br><br>

3.&nbsp; Scroll to the bottom and click <strong>Advanced</strong>.<br><br>

4.&nbsp; Locate the <strong>Privacy and security</strong> section.<br><br>

5.&nbsp; Click <strong>Content Settings</strong>.<br><br>

<img src="/img/general-information/configure-your-browser/chrome/fig5.png" alt="Pop up blocker"><br><br>

6.&nbsp; Under <strong>Popups</strong> section enable <strong>Allowed</strong>.<br><br>

<img src="/img/general-information/configure-your-browser/chrome/fig6.png" alt="Pop up blocker"><br><br>

<h3>Allow All Sites to Run JavaScript</h3>

1.&nbsp; Click on <img src="/img/general-information/configure-your-browser/chrome/fig1.png" alt="chrome settings button"> in the upper right corner.<br><br>

2.&nbsp; Select <strong>Settings</strong> from the drop-down menu.<br> <br>

3.&nbsp; Scroll to the bottom and click <strong>Advanced</strong>.<br> <br>

4.&nbsp; Locate the <strong>Privacy and security</strong> section. <br> <br>

5.&nbsp; Click <strong>Content Settings</strong>.<br><br>

6.&nbsp; Under <strong>JavaScript</strong> enable <strong>Allowed</strong>.<br><br>

<img src="/img/general-information/configure-your-browser/chrome/fig7.png" alt="Allow JavaScript"><br><br>

<h3>Unblock Third-Party Cookies and Site Data</h3>

1.&nbsp; Click on <img src="/img/general-information/configure-your-browser/chrome/fig1.png" alt="chrome settings button"> in the upper right corner <strong>Settings > Advanced > Privacy and security > Content Settings > Cookies </strong>.<br><br>

2.&nbsp; Enable <strong>Allow sites to save and read cookie data (recommended)</strong>.<br><br>

3.&nbsp; Disable <strong>Block third-party cookies</strong>.<br><br>

<img src="/img/general-information/configure-your-browser/chrome/fig8.png" alt="Allow Cookies"><br><br>

<h3>Allow all Sites to Download Multiple Files Automatically</h3>

1.&nbsp; Click on <img src="/img/general-information/configure-your-browser/chrome/fig1.png" alt="chrome settings button"> in the upper right corner <strong>> Settings > Advanced > Privacy and security > Content Settings</strong>.<br> <br>

2.&nbsp; Under <strong>Automatic Downloads</strong> section enable <strong>Allow all sites to download multiple files automatically</strong> .<br><br>

<img src="/img/general-information/configure-your-browser/chrome/fig9.png" alt="Automatic Download"><br><br>

<h3>Allow All Sites to Open PDF Files Externally</h3>

1.&nbsp; Click on <img src="/img/general-information/configure-your-browser/chrome/fig1.png" alt="chrome settings button"> in the upper right corner <strong>> Settings > Privacy and security > Content Settings > Additional content settings</strong>.<br> <br>

2.&nbsp; Under <strong>PDF documents</strong> section enable <strong>Download PDF files instead of automatically opening them in Chrome</strong> .<br><br>

<img src="/img/general-information/configure-your-browser/chrome/fig20.png" alt="Download PDF enabled"><br><br>

<h3>Disable Web Security</h3>

<p>1. Open the default Chrome user data folder under your Windows account - "C:\Users\[WindowsUser]\AppData\Local\Google\Chrome\User Data\Default" and locate the <strong>Preferences</strong> file.</p>

<p>2. Open it with a text editor and search for "webkit". If there is no such preference in the file, add the following at the bottom of the file:</p>

<style>
.code {
  background-color: #FFFFFF;
  text-align: left;
  text-indent: 50px;
  color: #000000;
}
</style>

<div class="code">
    <p>"webkit":{"webprefs":{"web_security_enabled":false}}</p>
</div>

<p>If the "webkit" preference already exists in the <strong>Preferences</strong> file and has any value in the "webprefs", you can add the web security as follows:</p>

<div class="code">
    <p>Existing values listed in the file:</p>
    <p>"webkit":{"webprefs":{"minimum_font_size":6}}</p>
    <p>The file after adding the web security:</p>
    <p>"webkit":{"webprefs":{"minimum_font_size":6, "web_security_enabled":false}}</p>
</div>

<hr/>

</div>
</div>

<h3>See also:</h3>

* <a href="/troubleshooting-guide/browser-inconsistencies-tg/extensions-disabled-in-chrome" target="_blank">Chrome Extensions Disabled or Missing</a>

<script>
window.addEventListener('DOMContentLoaded', function () {
$(".toggle_container").hide();
    
    $("p.trigger").click(function(e){
        e.preventDefault();
        $(this).toggleClass("active").next().slideToggle("normal");
		$(this).find('#d').text(function (i, oldText) {
        return $.trim(oldText) == '+' ? '-' : '+';
		});
		
    });
    });
</script>
