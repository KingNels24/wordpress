---
layout: post
title: Lenovo: Current version of Software Fingerprint Manager Pro is insecure
date: 2018-01-29 13:06
author: nvinside
comments: true
categories: [Lenovo, Security, Software]
---
Lenovo just confirmed that their own Software Fingerprint Manager is insecure, <a href="https://support.lenovo.com/nl/en/product_security/len-15999">according to their own Blog post</a>, the Fingerprint Manager stores some biometric data on the device. It seems that all recent Windows versions are affected, Win 7 and 8.1 - Windows 10 is not affected. Windows 10 is not affected because it comes with another integrated solution called 'Windows Hello'. Jackson Turaisamy originally discovered this hole.

&nbsp;

[caption id="attachment_2372" align="alignnone" width="670"]<img class="alignnone size-full wp-image-2372" src="https://chefkochblog.files.wordpress.com/2018/01/lenovo-security-threat-670x335.jpg" alt="lenovo-security-threat-670x335" width="670" height="335" /> Picture: <a href="https://cdn.makeuseof.com/wp-content/uploads/2016/05/lenovo-security-threat-670x335.jpg">makeuseof.com</a>[/caption]

&nbsp;

<!--more-->

<h2>Affected ThinkPads and Desktops</h2>

<ul>
    <li>ThinkPad L560</li>
    <li>ThinkPad P40 Yoga, P50s</li>
    <li>ThinkPad T440, T440p, T440s, T450, T450s, T460, T540p, T550, T560</li>
    <li>ThinkPad W540, W541, W550s</li>
    <li>ThinkPad X1 Carbon (Type 20A7, 20A8), X1 Carbon (Type 20BS, 20BT)</li>
    <li>ThinkPad X240, X240s, X250, X260</li>
    <li>ThinkPad Yoga 14 (20FY), Yoga 460</li>
    <li>ThinkCentre M73, M73z, M78, M79, M83, M93, M93p, M93z</li>
    <li>ThinkStation E32, P300, P500, P700, P900</li>
</ul>

https://youtu.be/JRA34PzvANg

<h2>Update your Software</h2>

Lenovo gives the advice to install the update v8.01.87 or newer which can be found <a href="https://pcsupport.lenovo.com/nl/en/downloads/ds034486">here</a>.

<h2>Final words</h2>

Lenovo should a little bit worry about their reputation because this isn't the first time that they have a security problem, of course, it's not as big as the huge <a href="https://en.wikipedia.org/wiki/Superfish">Superfish</a> leak but it'd maybe time to fire someone and replace him with a more competent person which takes security more serious. Such big 'fishes' are not every day on your hook.

It always surprises me, not that there are holes moreover that this only gets some attention if it affects multiple systems and devices. I wonder how the software gets tested these days, seems no one cares more about the quality because an update is always possible, but that this also costs time, bandwidth and Co. is something which people seems to ignore very quickly.

<h4><span style="text-decoration:underline;">Resource</span></h4>

<ul>
    <li>Hard-coded Password Lets Attackers Bypass Lenovo's Fingerprint Scanner (<a href="https://thehackernews.com/2018/01/lenovo-fingerprint.html" target="_blank" rel="noopener">thehackernews.com</a>)</li>
</ul>
