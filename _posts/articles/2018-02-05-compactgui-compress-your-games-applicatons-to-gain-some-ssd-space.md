---
layout: post
title: CompactGUI: Compress your Games & Applicatons to gain some SSD space
date: 2018-02-05 20:08
author: nvinside
comments: true
categories: [CompactGUI, Software, Software Review]
---
CompactGUI is a must have tool for Windows and Gamers, that is for sure but it also can help the normal user to compress larger applications, the benefit is that you save a lot of storage and the application might load faster.

[caption id="attachment_2632" align="alignnone" width="1280"]<img class="alignnone size-full wp-image-2632" src="https://chefkochblog.files.wordpress.com/2018/02/compactgui.jpg" alt="CompactGUI" width="1280" height="655" /> Final Fantasy from 23 to under 1.2 GB compressed![/caption]

<!--more-->

<h2>CompactGUI</h2>

The program is free and open source, it's available on <a href="https://github.com/ImminentFate/CompactGUI" target="_blank" rel="noopener">GitHub</a>.

<img class="alignnone size-full wp-image-2633" src="https://chefkochblog.files.wordpress.com/2018/02/compactgui.png" alt="CompactGUI" width="1002" height="659" />

The GUI doesn't offer much, you select the folder and that's it, the entire magic is handled via a triggered command line parameter.

<img class=" size-full wp-image-2634 aligncenter" src="https://chefkochblog.files.wordpress.com/2018/02/compactgui-options.png" alt="CompactGUI Options" width="460" height="524" />

<h3>How does it work?</h3>

Basically it works with the Windows own compact option, an explanation is given <a href="https://technet.microsoft.com/en-us/library/cc976811.aspx" target="_blank" rel="noopener">here</a>. You also could <a href="https://www.windowscentral.com/how-reduce-windows-10-footprint-your-pc" target="_blank" rel="noopener">compact your entire OS</a>, but from my experience there is not really a benefit, maybe the SSD footprint but it also can create problems with some applications, so I suggest you start first with CompactGUI.

<h2>Benefits</h2>

<ul>
    <li>SSD space is not cheap, so go ahead and save some space.</li>
    <li>Faster loading speed because the application is faster to load due the efficient compressing algorithm.</li>
</ul>

What kind of gains can you expect from compacting folders and files within? This depends largely on the type of files - the developer compressed the Adobe Photoshop folder and cut its size in half by doing so and I was able to compress a recent Final Fantasy Version to under 1.2 GB, that's insane!

<h2>Final Words</h2>

Do you noticed that I not talked about the cons? Because there are no cons and the program works at least for me perfect, of course it's always possible that a game isn't compatible but it shouldn't be a big deal to do a backup or to re-install the game. Does it work with Steam and Origin Games too? Sure, it doesn't trigger any anti-cheat mechanism because it's only a compression and not any special voodoo.

Go ahead, show me your results.

<h2><span style="color:#ff0000;">Update</span></h2>

Windows reports the compressed file size using only a 32-bit unsigned integer, so whenever the end-result of compressing a single file is larger than 4GB (2^32 bytes = 4GB), the result wraps around and starts at 0 again. So when the compressed file ends up being 4.5GB big, it instead displays incorrectly as being only 0.5GB big (4.5GB - 4GB = 0.5GB).

<h3>What does it mean?</h3>

The developer needs to change the program to display the correct values, you still can get a solid compression but not over 100% or such ridiculous values, points out that I could save 9% on Final Fantasy. This is why FF XII seemed to compress from 29GB to just 1GB. The math here is 29GB - 4GB*7 = 1GB. However, the program is still not bad!
