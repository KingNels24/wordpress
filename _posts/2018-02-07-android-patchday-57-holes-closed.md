---
layout: post
title: Android Patchday: 57 holes closed
date: 2018-02-07 17:01
author: nvinside
comments: true
categories: [Android, Android Patchday]
---
6 critical holes got a fix, the Media Framework got yet again fixes (like every patchday since 2015) among nVidia and Qualcomm patches. Pixel owner can download a 'fixed' <a href="https://developers.google.com/android/ota" target="_blank" rel="noopener">OTA image</a>, which solves a huge issue with the latest patchday.

[caption id="attachment_2682" align="alignnone" width="700"]<img class="alignnone size-full wp-image-2682" src="https://chefkochblog.files.wordpress.com/2018/02/android1-71cb45c4a86f9f17.png" alt="android1-71cb45c4a86f9f17" width="700" height="393" /> Picture: <a href="https://heise.cloudimg.io/width/700/q75.png-lossy-75.webp-lossy-75.foil1/_www-heise-de_/imgs/18/2/3/6/6/2/0/0/android1-71cb45c4a86f9f17.png" target="_blank" rel="noopener">heise.de</a>[/caption]

<!--more-->

The complete changelog is available <a href="https://source.android.com/security/bulletin/2018-02-01" target="_blank" rel="noopener">here</a>, every Android version beginning from Android 5.1.1 are supported. 28 patches overall which including 57 holes in total.

<h2>Media Framework</h2>

<table>
<tbody>
<tr>
<th>CVE</th>
<th>References</th>
<th>Type</th>
<th>Severity</th>
<th>Updated AOSP versions</th>
</tr>
<tr>
<td>CVE-2017-13228</td>
<td>A-69478425</td>
<td>RCE</td>
<td>Critical</td>
<td>6.0, 6.0.1, 7.0, 7.1.1, 7.1.2, 8.0, 8.1</td>
</tr>
<tr>
<td>CVE-2017-13231</td>
<td>A-67962232</td>
<td>EoP</td>
<td>High</td>
<td>8.0, 8.1</td>
</tr>
<tr>
<td>CVE-2017-13232</td>
<td>A-68953950</td>
<td>ID</td>
<td>High</td>
<td>5.1.1, 6.0, 6.0.1, 7.0, 7.1.1, 7.1.2, 8.0, 8.1</td>
</tr>
<tr>
<td rowspan="2">CVE-2017-13230</td>
<td rowspan="2">A-65483665</td>
<td>DoS</td>
<td>High</td>
<td>7.0, 7.1.1, 7.1.2, 8.0, 8.1</td>
</tr>
<tr>
<td>RCE</td>
<td>Critical</td>
<td>5.1.1, 6.0, 6.0.1</td>
</tr>
<tr>
<td>CVE-2017-13233</td>
<td>A-62851602</td>
<td>DoS</td>
<td>High</td>
<td>5.1.1, 6.0, 6.0.1, 7.0, 7.1.1, 7.1.2, 8.0, 8.1</td>
</tr>
<tr>
<td>CVE-2017-13234</td>
<td>A-68159767</td>
<td>DoS</td>
<td>High</td>
<td>5.1.1, 6.0, 6.0.1, 7.0, 7.1.1, 7.1.2, 8.0, 8.1</td>
</tr>
</tbody>
</table>

<h2>System</h2>

<div class="devsite-table-wrapper">
<table><colgroup> <col width="17%" /> <col width="19%" /> <col width="9%" /> <col width="14%" /> <col width="39%" /> </colgroup>
<tbody>
<tr>
<th>CVE</th>
<th>References</th>
<th>Type</th>
<th>Severity</th>
<th>Updated AOSP versions</th>
</tr>
<tr>
<td>CVE-2017-13236</td>
<td>A-68217699</td>
<td>EoP</td>
<td>Moderate</td>
<td>8.0, 8.1</td>
</tr>
</tbody>
</table>
</div>

<h2 id="htc-components">HTC components</h2>

<div class="devsite-table-wrapper">
<table><colgroup> <col width="17%" /> <col width="19%" /> <col width="9%" /> <col width="14%" /> <col width="39%" /> </colgroup>
<tbody>
<tr>
<th>CVE</th>
<th>References</th>
<th>Type</th>
<th>Severity</th>
<th>Component</th>
</tr>
<tr>
<td>CVE-2017-13238</td>
<td>A-64610940<a href="https://source.android.com/security/bulletin/2018-02-01#asterisk">*</a></td>
<td>ID</td>
<td>High</td>
<td>Bootloader</td>
</tr>
<tr>
<td>CVE-2017-13247</td>
<td>A-71486645<a href="https://source.android.com/security/bulletin/2018-02-01#asterisk">*</a></td>
<td>EoP</td>
<td>Moderate</td>
<td>Bootloader</td>
</tr>
</tbody>
</table>
</div>

<h2 id="kernel-components">Kernel components</h2>

<div class="devsite-table-wrapper">
<table><colgroup> <col width="17%" /> <col width="19%" /> <col width="9%" /> <col width="14%" /> <col width="39%" /> </colgroup>
<tbody>
<tr>
<th>CVE</th>
<th>References</th>
<th>Type</th>
<th>Severity</th>
<th>Component</th>
</tr>
<tr>
<td>CVE-2017-15265</td>
<td>A-67900971
<a href="https://git.kernel.org/pub/scm/linux/kernel/git/stable/linux-stable.git/commit/sound/?h=v4.4.103&amp;id=23709ae9b61429502fcd4686e7a97333f3b3544a"> Upstream kernel</a></td>
<td>EoP</td>
<td>High</td>
<td>ALSA</td>
</tr>
<tr>
<td>CVE-2015-9016</td>
<td>A-63083046
<a href="https://github.com/torvalds/linux/commit/0048b4837affd153897ed1222283492070027aa9"> Upstream kernel</a></td>
<td>EoP</td>
<td>High</td>
<td>Multi-queue block IO</td>
</tr>
<tr>
<td>CVE-2017-17770</td>
<td>A-65853158<a href="https://source.android.com/security/bulletin/2018-02-01#asterisk">*</a></td>
<td>EoP</td>
<td>High</td>
<td>Kernel</td>
</tr>
</tbody>
</table>
</div>

<h2 id="nvidia-components">NVIDIA components</h2>

<div class="devsite-table-wrapper">
<table><colgroup> <col width="17%" /> <col width="19%" /> <col width="9%" /> <col width="14%" /> <col width="39%" /> </colgroup>
<tbody>
<tr>
<th>CVE</th>
<th>References</th>
<th>Type</th>
<th>Severity</th>
<th>Component</th>
</tr>
<tr>
<td>CVE-2017-6279</td>
<td>A-65023166<a href="https://source.android.com/security/bulletin/2018-02-01#asterisk">*</a>
N-CVE-2017-6279</td>
<td>EoP</td>
<td>High</td>
<td>Media framework</td>
</tr>
<tr>
<td>CVE-2017-6258</td>
<td>A-38027496<a href="https://source.android.com/security/bulletin/2018-02-01#asterisk">*</a>
N-CVE-2017-6258</td>
<td>EoP</td>
<td>High</td>
<td>Media framework</td>
</tr>
</tbody>
</table>
</div>

<h2 id="qualcomm-components">Qualcomm components</h2>

<div class="devsite-table-wrapper">
<table><colgroup> <col width="17%" /> <col width="19%" /> <col width="9%" /> <col width="14%" /> <col width="39%" /> </colgroup>
<tbody>
<tr>
<th>CVE</th>
<th>References</th>
<th>Type</th>
<th>Severity</th>
<th>Component</th>
</tr>
<tr>
<td>CVE-2017-15817</td>
<td>A-68992394
<a href="https://source.codeaurora.org/quic/la/platform/vendor/qcom-opensource/wlan/prima/commit/?id=8ba78e506e5002cdae525dd544dbf1df0ccce1ef"> QC-CR#2076603 [2]</a> [<a href="https://source.codeaurora.org/quic/la/platform/vendor/qcom-opensource/wlan/prima/commit/?id=fe43c2b64ac81199de17efc258e95546cb0546f1"> 2</a>]</td>
<td>RCE</td>
<td>Critical</td>
<td>WLan</td>
</tr>
<tr>
<td>CVE-2017-17760</td>
<td>A-68992416
<a href="https://source.codeaurora.org/quic/la/platform/vendor/qcom-opensource/wlan/qcacld-2.0/commit/?id=71331327ac389bff7d5af2707c4325e5b7949013"> QC-CR#2082544 [2]</a> [<a href="https://source.codeaurora.org/quic/la/platform/vendor/qcom-opensource/wlan/qcacld-2.0/commit/?id=a6afff2717791ceb281354833d4489123ae62605"> 2</a>]</td>
<td>RCE</td>
<td>Critical</td>
<td>WLan</td>
</tr>
<tr>
<td>CVE-2017-11041</td>
<td>A-35269676<a href="https://source.android.com/security/bulletin/2018-02-01#asterisk">*</a>
QC-CR#2053101</td>
<td>EoP</td>
<td>High</td>
<td>Media framework</td>
</tr>
<tr>
<td>CVE-2017-17767</td>
<td>A-64750179<a href="https://source.android.com/security/bulletin/2018-02-01#asterisk">*</a>
QC-CR#2115779</td>
<td>EoP</td>
<td>High</td>
<td>Media framework</td>
</tr>
<tr>
<td>CVE-2017-17765</td>
<td>A-68992445
<a href="https://source.codeaurora.org/quic/la/platform/vendor/qcom-opensource/wlan/qcacld-3.0/commit/?id=66e561b0c7fff54e8cacd87d2b7d9bb3eef4f13b"> QC-CR#2115112</a></td>
<td>EoP</td>
<td>High</td>
<td>WLan</td>
</tr>
<tr>
<td>CVE-2017-17762</td>
<td>A-68992439
<a href="https://source.codeaurora.org/quic/la/platform/vendor/qcom-opensource/wlan/qcacld-3.0/commit/?id=41ee23cd0972ef2ed47dd76eb7cd44a0268e4f9f"> QC-CR#2114426</a></td>
<td>EoP</td>
<td>High</td>
<td>WLan</td>
</tr>
<tr>
<td>CVE-2017-14884</td>
<td>A-68992429
<a href="https://source.codeaurora.org/quic/la/platform/vendor/qcom-opensource/wlan/qcacld-2.0/commit/?id=0ce15ef4075719a82858b7324690be7011cab832"> QC-CR#2113052</a></td>
<td>EoP</td>
<td>High</td>
<td>WLan</td>
</tr>
<tr>
<td>CVE-2017-15829</td>
<td>A-68992397
<a href="https://source.codeaurora.org/quic/la/kernel/msm-4.4/commit/?id=c1b60e554e158bfcf6932ed2c543c309236e0f79"> QC-CR#2097917</a></td>
<td>EoP</td>
<td>High</td>
<td>Graphics_Linux</td>
</tr>
<tr>
<td>CVE-2017-15820</td>
<td>A-68992396
<a href="https://source.codeaurora.org/quic/la/kernel/msm-4.4/commit/?id=7599c5b7d87248b4772d6c4b70ccb922704c8095"> QC-CR#2093377</a></td>
<td>EoP</td>
<td>High</td>
<td>Graphics_Linux</td>
</tr>
<tr>
<td>CVE-2017-17764</td>
<td>A-68992443
<a href="https://source.codeaurora.org/quic/la/platform/vendor/qcom-opensource/wlan/qcacld-3.0/commit/?id=f451565c052a0322565225515f46be677c0d1b18"> QC-CR#2114789</a></td>
<td>EoP</td>
<td>High</td>
<td>WLan</td>
</tr>
<tr>
<td>CVE-2017-17761</td>
<td>A-68992434
<a href="https://source.codeaurora.org/quic/la/platform/vendor/qcom-opensource/wlan/qcacld-3.0/commit/?id=13e3a516935a0dd90a7bc39e51c30c1592c548b7"> QC-CR#2114187</a></td>
<td>EoP</td>
<td>High</td>
<td>WLan</td>
</tr>
</tbody>
</table>
</div>

<h2 id="qualcomm-closed-source-components">Qualcomm closed-source components</h2>

<div class="devsite-table-wrapper">
<table><colgroup> <col width="17%" /> <col width="19%" /> <col width="9%" /> <col width="14%" /> <col width="39%" /> </colgroup>
<tbody>
<tr>
<th>CVE</th>
<th>References</th>
<th>Type</th>
<th>Severity</th>
<th>Component</th>
</tr>
<tr>
<td>CVE-2017-14910</td>
<td>A-62212114<a href="https://source.android.com/security/bulletin/2018-02-01#asterisk">*</a></td>
<td>N/A</td>
<td>High</td>
<td>Closed-source component</td>
</tr>
</tbody>
</table>
</div>

<h2>Conclusion</h2>

There is nothing much to mention this patchday, it's a typically patchday, the components which regularly getting patches like nVidia, Qualcomm and the media framework are vulnerable since several years.

&nbsp;
