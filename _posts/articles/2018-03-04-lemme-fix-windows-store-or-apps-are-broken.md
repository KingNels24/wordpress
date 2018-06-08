---
layout: post
title: Lemme Fix: Windows Store or Apps are broken
date: 2018-03-04 00:02
author: nvinside
comments: true
categories: [apps, Windows 10, Windows Store]
---
Sometimes especially on Windows Insider Builds the Windows Store is broken or the pre-installed apps are not functional and you going to search for a fix and in this quick guide I provide several ways how you can fix the Windows Store/Apps problems very easy.

<img class="alignnone size-full wp-image-3211" src="https://chefkochblog.files.wordpress.com/2018/03/windows-broken-apps.jpg" alt="Windows broken Apps" width="1684" height="960" />

<!--more-->

<h2>Fix broken Windows Store</h2>

<h3>0x80240013 &amp; 0x80131500</h3>

This error is an result of outdated apps or a mismatch between the Account and the Store application, there is no real solution for it yet. In most of the cases Microsoft fixes this problem itself in the background and the error simply dissapears after some hours/days. The 0x80131500 problem is explicit a Microsoft Server issue, just try it again after 1 hour and then mash F5.

<h3>0x80073CF0</h3>

This problem is a result of a broken <b>SoftwareDistribution</b> folder, something is missing or borked. The easiest solution IO found so far to deal with this problem is to delete the content of C:\Windows\SoftwareDistribution.

<h3>0x80072EFD</h3>

This error means you have to unblock the App/Store with the integrated or external Firewall, so there is no Internet connection.

<h3>0x80070057</h3>

This is caused by some AV products, ensure you disable it (temporarily) or exclude/whitelist the Store if it really won't work at all.

<h3>0x80248014</h3>

This error means that the Store is restricted via gpedit.msc.

<code>HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\WindowsStore</code>

<code>RemoveWindowsStore</code>

<ul>
    <li>1 = Windows Store is locked</li>
    <li>0 = Windows Store is unlocked</li>
</ul>

<h3>Windows Store doesn't start with more than once User Account</h3>

<img class=" size-full wp-image-3214 aligncenter" src="https://chefkochblog.files.wordpress.com/2018/03/lock.jpg" alt="Lock" width="569" height="438" />

<a class="external text" href="https://support.microsoft.com/en-us/kb/3092053" target="_blank" rel="nofollow noreferrer noopener">KB3092053</a> (cssemerg70008.diagcab) provides a fix for this. There is also an <a class="external text" href="https://support.microsoft.com/de-de/instantanswers/69e76f90-d54c-44cf-9851-c2d1542790db/run-the-troubleshooter-for-windows-apps" target="_blank" rel="nofollow noreferrer noopener">Appsdiagnostic10.diagcab</a> file which tries to solve some Windows Store issue.

<h3>Resetting the Windows Store</h3>

[caption id="attachment_3212" align="aligncenter" width="600"]<img class=" size-full wp-image-3212 aligncenter" src="https://chefkochblog.files.wordpress.com/2018/03/reset-microsoft-store.png" alt="reset-microsoft-store" width="600" height="364" /> Can be found under "Apps &amp; features" - 'Store' - 'Advance Options'.[/caption]

This will permanently delete the app’s data on this device, including your preferences and sign-in details”. After your confirmed this message you fully reset the Windows Store and the apps back to the default.

<h3>Check your date &amp; clock</h3>

Sounds ridiculous? It is, but sometimes checking the clock and the date might already solve some issue.

<h3>Repair the Windows Store via Command Prompt</h3>

<img class=" size-full wp-image-3213 aligncenter" src="https://chefkochblog.files.wordpress.com/2018/03/windows-10-store-cmd.jpg" alt="Windows 10 Store CMD" width="719" height="307" />

<code>PowerShell -ExecutionPolicy Unrestricted -Command "&amp; {$manifest = (Get-AppxPackage Microsoft.WindowsStore).InstallLocation + '\AppxManifest.xml' ; Add-AppxPackage -DisableDevelopmentMode -Register $manifest}"</code>

or

<code>powershell -ExecutionPolicy Unrestricted Add-AppxPackage -DisableDevelopmentMode -Register $Env:SystemRoot\WinStore\AppxManifest.XML</code>

These are the two commands which you could try, keep in mind to start the CMD with adminstrative privileges.

<h3>Windows Stores opens and closes itself after 1 second</h3>

Navigate to <b>C:\Users\yourAccount\AppData\Local\Packages\Microsoft.WindowsStore_<i>8wekyb1d9bbwe</i>\LocalCache</b> and remove the content. Keep in mind that the numbers after Microsoft.WindowsStore_xxxxx are random generated and can look different for you.

If this method fails because it tells you that you can't access the LocalCache folder, just rename it to LocalCacheOld and create another LocalCache folder manually.

<h3>PowerShell Method</h3>

<ol>
    <li>Download the <a class="external text" href="http://go.microsoft.com/fwlink/?LinkId=619547" target="_blank" rel="nofollow noreferrer noopener">Reinstall-preinstalledApps.zip</a>.</li>
    <li>Extract it on the eg. Desktop</li>
    <li>Open PowerShell (right click on Start-Menu Orb/Button - PowerShell (Admin)</li>
    <li>Type in "<code>Set-ExecutionPolicy Unrestricted</code><b>"</b>and confirm it with<b> Y</b>. This basically allows you to install scripts without digital signature.</li>
    <li>Navigate to your extracted files on the Desktop which included several scripts</li>
    <li>Type in<code>.\reinstall-preinstalledApps.ps1</code></li>
    <li>This will reinstall all Apps</li>
    <li>last step is to reset the ExecutionPolicy back to normal due security reasons "<code>Set-ExecutionPolicy AllSigned</code><b>" </b>and confirm it again with <b>Y</b>.</li>
    <li>That's it.</li>
</ol>

Another Method is:

<ul>
    <li><code>set-ExecutionPolicy RemoteSigned</code></li>
    <li><code>Get-AppXPackage -AllUsers | Foreach {Add-AppxPackage -DisableDevelopmentMode -Register "$($_.InstallLocation)\AppxManifest.xml"}</code></li>
</ul>

<h3>Repair the broken Store via DISM</h3>

We starting the CMD (Command Prompt) again with administrative privileges and then we going to using the following command:

<p style="text-align:center;"><code>dism /online /cleanup-image /startcomponentcleanup</code></p>

<h2>Repair/Reinstall broken Apps</h2>

Same steps like the 'PowerShell Method' above but you replace step 6 with the app you want to repair/reinstall.

<span style="text-decoration:underline;">Examples</span>:

<ul>
    <li>.\reinstall-preinstalledApps.ps1 *Microsoft.Office.OneNote*</li>
    <li>.\reinstall-preinstalledApps.ps1 *Microsoft.People*</li>
    <li>.\reinstall-preinstalledApps.ps1 *Microsoft.SkypeApp*</li>
    <li>.\reinstall-preinstalledApps.ps1 *Microsoft.WindowsCalculator*</li>
    <li>.\reinstall-preinstalledApps.ps1 *Microsoft.WindowsCamera*</li>
    <li>.\reinstall-preinstalledApps.ps1 *Microsoft.WindowsMaps*</li>
    <li>.\reinstall-preinstalledApps.ps1 *Microsoft.WindowsSoundRecorder*</li>
    <li>.\reinstall-preinstalledApps.ps1 *Microsoft.XboxApp*</li>
</ul>

You can do this for every app you want to bring back or repair.

<h2>General System issue</h2>

You always can try to <code>sfc /scannow</code> via CMD to solve some common problems. It's worth a try. Also <b>wsreset.exe </b>might help to delete the Windows Store Cache, sometimes it can help (just execute it and the cache gets deleted in the background).
