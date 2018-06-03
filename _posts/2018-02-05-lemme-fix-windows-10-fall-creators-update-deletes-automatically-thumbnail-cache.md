---
layout: post
title: Lemme fix: Windows 10 Fall Creators Update deletes automatically thumbnail cache
date: 2018-02-05 18:31
author: nvinside
comments: true
categories: [Lemme fix, Tips and Tricks, Windows 10]
---
Since Windows 10 Fall Creators Update the thumbnail cache automatically gets deleted, this can be annoying and it creates unnecessary write cycles on your SSD which decrease the lifespan, it's not a drama but it's simply an unwanted behavior because the Explorer is forced to re-create the thumbnails again and again after each reboot.

<img class="alignnone size-full wp-image-2624" src="https://chefkochblog.files.wordpress.com/2018/02/silentcleanup.png" alt="SilentCleanup" width="1398" height="866" />

<!--more-->

<h2>What is causing the issue?</h2>

Windows own SilentCleanup task triggers the Disk Cleanup tool which then deletes the thumbnail cache. The Automatic Maintenance task can delete e.g. %TMP% folder, check your HDD among other things.

The thumbnail cache for each user is stored as separate .db file located under:

<p style="text-align:center;"><code>%LocalAppData%\Microsoft\Windows\Explorer</code></p>

<h2>Disabling it</h2>

You should not delete the entire task because it's too useful, instead disabling this specific behavior is enough.

<code>REGEDIT4
</code><code>HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\VolumeCaches\Thumbnail Cache</code>

;On 64-bit systems only
<code>HKLM\SOFTWARE\WOW6432Node\Microsoft\Windows\CurrentVersion\Explorer\VolumeCaches\Thumbnail Cache</code>

Create or change the following value:
<strong><code>Autorun</code></strong> (DWORD)
0 = <strong><code>Prevent</code></strong>
1 = <strong><code>Allow</code></strong>

<h3>Finished example</h3>

<code>Windows Registry Editor Version 5.00</code>

<code>[HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\Windows\CurrentVersion\Explorer\VolumeCaches\Thumbnail Cache]
"Autorun"=dword:00000000</code>

<h2>Final words</h2>

Most tools disabling everything, in this case maybe the Automatic Maintenance process, this is not needed and not a good idea, changing this little toggle is simply enough and does the trick.

Why MS implemented this is a little beyond me, in my opinion this should be set by default as opt-in option because I see no reason why someone really want to delete the thumbnail cache each reboot, most people just disable the creation of thumbnails in general when they don't like them.
