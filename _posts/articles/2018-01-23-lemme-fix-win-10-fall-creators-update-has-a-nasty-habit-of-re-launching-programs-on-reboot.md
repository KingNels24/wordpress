---
layout: post
title: Lemme fix: Win 10 Fall Creators Update has a nasty habit of re-launching programs on reboot
date: 2018-01-23 08:45
author: nvinside
comments: true
categories: [Lemme fix, Windows 10]
---
<a href="https://www.computerworld.com/article/3250485/microsoft-windows/win10-1709-s-most-irksome-feature-programs-come-back-from-the-dead.html" target="_blank" rel="noopener">Computerworld</a> reports that Windows 10 Fall Creators update automatically re-opens your applications on each reboot, I could confirm this on a fresh installed Win 10 on a test laptop.

<img class="alignnone size-full wp-image-2149" src="https://chefkochblog.files.wordpress.com/2018/01/win10s.jpg" alt="win10s" width="810" height="456" />

<!--more-->

In this little guide I give you a workaround until Microsoft changes it's mind and 'fix' their own mess, I still not understand why Microsoft made that decision but well we only can deal with what we get.

[caption id="attachment_2150" align="aligncenter" width="399"]<img class=" size-full wp-image-2150 aligncenter" src="https://chefkochblog.files.wordpress.com/2018/01/regedit.png" alt="regedit" width="399" height="206" /> Open <strong>regedit</strong>.[/caption]

Navigate to:

<p style="text-align:center;"><code>HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\RunOnce</code></p>

[caption id="attachment_2151" align="aligncenter" width="415"]<img class=" size-full wp-image-2151 aligncenter" src="https://chefkochblog.files.wordpress.com/2018/01/33.jpg" alt="33" width="415" height="322" /> Right click on this folder. And click "Permissions".[/caption]

[caption id="attachment_2152" align="aligncenter" width="363"]<img class=" size-full wp-image-2152 aligncenter" src="https://chefkochblog.files.wordpress.com/2018/01/54.png" alt="54" width="363" height="450" /> To change the permissions on the folder Left click on Disable Inheritance.[/caption]

[caption id="attachment_2153" align="alignnone" width="767"]<img class="alignnone size-full wp-image-2153" src="https://chefkochblog.files.wordpress.com/2018/01/fef7.png" alt="fef" width="767" height="520" /> Click on the <strong>“convert, inherited permissions into explicit permissions on this object”.</strong>[/caption]

[caption id="attachment_2154" align="aligncenter" width="522"]<img class=" size-full wp-image-2154 aligncenter" src="https://chefkochblog.files.wordpress.com/2018/01/fef8.png" alt="fef" width="522" height="277" /> Now you can change the permissions on the <strong>RunOnce</strong> folder.[/caption]

[caption id="attachment_2155" align="aligncenter" width="767"]<img class=" size-full wp-image-2155 aligncenter" src="https://chefkochblog.files.wordpress.com/2018/01/fef9.png" alt="fef" width="767" height="520" /> Make sure you remove the Full Control on each user and make them Read only.[/caption]

[caption id="attachment_2156" align="aligncenter" width="917"]<img class=" size-full wp-image-2156 aligncenter" src="https://chefkochblog.files.wordpress.com/2018/01/fef10.png" alt="fef" width="917" height="593" /> Untick '<strong>Full Control</strong>' and click <strong>OK</strong>.[/caption]

<img class=" size-full wp-image-2157 aligncenter" src="https://chefkochblog.files.wordpress.com/2018/01/untitled.png" alt="Untitled" width="767" height="520" />

This is the end result, ensure you did this for all users/accounts.
