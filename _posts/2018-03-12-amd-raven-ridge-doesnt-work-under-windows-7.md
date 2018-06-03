---
layout: post
title: AMD: Raven Ridge doesn't work under Windows 7
date: 2018-03-12 10:24
author: nvinside
comments: true
categories: [AMD, Raven Ridge, Windows 7]
---
AMD is dropping the support for older operating systems like Windows XP, Vista and now Windows 7. You still could't 'cheat' you way around this with other newer CPU's because it was a driver 'problem' but this is now over.

[caption id="attachment_3584" align="alignnone" width="2040"]<img class="alignnone size-full wp-image-3584" src="https://chefkochblog.files.wordpress.com/2018/03/amd-raven-ridge.jpg" alt="AMD Raven Ridge" width="2040" height="967" /> AMD Raven Ridge. Picture Source Wccftech[/caption]

<!--more-->

<h2>Not the OS is to blame this time, the BIOS is</h2>

Previously you could boot a newer CPU with manipulated drivers in eg. Windows 7 this seems over now because a <a href="https://www.reddit.com/r/Amd/comments/83l53s/raven_ridge_windows_7_psa/" target="_blank" rel="noopener">Reddit user reports that the culprit is now the BIOS</a>. The reaosn here seems the implementation of <a class="has-tooltip js-tooltip" href="https://en.wikipedia.org/wiki/Advanced_Configuration_and_Power_Interface" target="_blank" rel="noopener">Advanced Configuration and Power Interface (ACPI)</a> feature, this has changed and won't allow you to boot the CPU under Windows 7. If you use a decided GPU instead of the APU, this will not change and boot.

<h2>No Updates for new CPU's on older Operating Systems</h2>

Microsoft checks the CPU during the Windows Update which means you won't get specific updates when you CPU/OS doesn't match the requirements. You could <a href="https://github.com/zeffy/wufuc" target="_blank" rel="noopener">patch your way around this</a>, but that is not possible when the BIOS doesn't support the missing ACPI table.

<h2>Windows 7 support until 2020</h2>

The thing is that Windows 7 gets official supported until 2020 but since 2015 the OS is in another  'extended' phase which means you only receive security and bugfixes but not feature updates anymore. These feature updates would be required in order to support newer CPU features and energy profiles.

<h2>Conclusion</h2>

The real problem I see here is that Windows 7 official gets supported until 2020 and theoretically all new CPU's must be supported (in my opinion) and I get the point that people are upset because it's now fully blocked within the BIOS. A solution would be a BIOS and Windows update but AMD and Microsoft don't want it and that's the whole point here. On the other side, who is going to buy a new CPU and cripples it with Windows 7 - ah right the spying ... sure. Makes me laugh - btw when you paid your CPU do you used PayPal? I ask because you revealed more with PayPal and externals than using Windows 10 cause <a href="https://www.paypal.com/ie/webapps/mpp/ua/third-parties-list" target="_blank" rel="noopener">PayPal is sharing your data with others</a>.

Just upgrade your god damn it OS .. <em>JESUS</em>! <img class="alignnone size-full wp-image-3528" src="https://chefkochblog.files.wordpress.com/2018/03/getting-stoned.gif" alt="getting-stoned" width="31" height="27" />

<h3><span style="text-decoration:underline;">Source</span></h3>

<ul>
    <li>Raven Ridge Windows 7 PSA (<a href="https://www.reddit.com/r/Amd/comments/83l53s/raven_ridge_windows_7_psa/" target="_blank" rel="noopener">reddit.com/r/Amd</a>)</li>
</ul>
