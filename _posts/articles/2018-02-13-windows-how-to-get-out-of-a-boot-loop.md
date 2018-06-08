---
layout: post
title: Windows: How to get out of a Boot Loop
date: 2018-02-13 08:43
author: nvinside
comments: true
categories: [boot loop, tutorial, Tutorials, Windows]
---
There might be situations when you're stuck in a boot loop in Windows 7 or later, e.g. if you recently installed a Windows Update or if you tried to revert your Windows version to a newer or older state. So the following tutorial might help you one day if you're stuck in the loop.

<img class="alignnone size-full wp-image-2833" src="https://chefkochblog.files.wordpress.com/2018/02/endless-reboot-loop-windows-10-fix1.png" alt="endless-reboot-loop-windows-10-fix(1)" width="715" height="437" />

<!--more-->

Boot into Windows Recovery Environment by pressing F8, Shift+F8, F11, F12. In case none of these options are working, just check-out this guide over <a href="https://www.tenforums.com/tutorials/22455-enable-disable-f8-advanced-boot-options-windows-10-a.html" target="_blank" rel="noopener">here</a>.

<img class="alignnone size-full wp-image-2834" src="https://chefkochblog.files.wordpress.com/2018/02/windowsbootmanager.png" alt="WindowsBootManager" width="1021" height="766" />

Start or force to restart your computer two or three times. If you see the Launch Startup Repair option, choose it, and then optionally press Cancel to cancel the Startup Repair, and then click “View advanced options […].”

<img class="alignnone size-full wp-image-2835" src="https://chefkochblog.files.wordpress.com/2018/02/startupsettings.png" alt="StartupSettings" width="1020" height="763" />

In most cases hammering the F8 key during the boot brings this screen ^^ up which gives you already a lot of options. First try to use the startup repair option, which might already fix your problem but if that fails, you can use the Advance Startup settings which brings you to the 'Launch recovery environment' screen.

<img class="alignnone size-full wp-image-2836" src="https://chefkochblog.files.wordpress.com/2018/02/launchrecoveryenvironment.png" alt="LaunchRecoveryEnvironment" width="1023" height="767" />

Navigate within the Windows Recovery Environment until you find Command Prompt and click it to open a command prompt and type in the following to get out of the boot loop:

<p style="text-align:center;"><code>dism /image:d:\ /cleanup-image /revertpendingactions</code></p>

This brings you out of the loop and, in case you see an error, replace the d: with another drive, in our example it uses d because Windows is installed on c: (default).

There is also an official Microsoft related article to this issue which you can find <a href="https://blogs.technet.microsoft.com/joscon/2009/10/15/getting-out-of-a-no-boot-situation-after-installing-updates-on-windows-7-2008r2/" target="_blank" rel="noopener">here</a>.

<h2>Closing Words</h2>

Microsoft usually brings everything that you need in order to repair or fix Windows, sadly the documentation is a bit lacking, most people are not aware of the possibilities of dism. This should, in my opinion, be improved since it's a powerful utility.
