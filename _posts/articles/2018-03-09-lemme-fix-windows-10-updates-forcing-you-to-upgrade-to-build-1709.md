---
layout: post
title: Lemme Fix: Windows 10 updates forcing you to upgrade to Build 1709
date: 2018-03-09 13:12
author: nvinside
comments: true
categories: [forced upgrade, Lemme fix, Windows 10]
---
Several pages reporting that Microsoft is forcing you to upgrade Windows 1703 (or an older build) to Build 1709. Several KB's are the cause here, because Microsoft added a <b>UpdateOrchestrator </b>&amp; <b>UpdateAssistant </b>to the Windows Tasks Scheduler. It's definitely wrong that this has something to do with telemetry related settings because these two tasks are there no matter which telemetry option you set (basic, advance,...) and there not only <a href="https://support.microsoft.com/en-us/help/4023814/some-versions-of-windows-10-display-a-notification-to-install-the-late" target="_blank" rel="noopener">KB4023814</a> + KB4023057 related, several other KB's also managing this.

<img class=" size-full wp-image-2844 aligncenter" src="https://chefkochblog.files.wordpress.com/2018/02/windows-10-finger-e1478083389681.jpg" alt="Windows performance" width="640" height="427" />

<!--more-->

<h2>Is Microsoft forcing you to upgrade?</h2>

The tasks are created to make it easier to offer upgrades but the <b>UpdateOrchestrator task </b>might have some problems which overriding some settings, so you systems <a href="https://support.microsoft.com/en-us/help/4023814/some-versions-of-windows-10-display-a-notification-to-install-the-late" target="_blank" rel="noopener">wrongly gets the upgrade notification</a> no matter what. I already informed Microsoft about this several weeks ago.

<blockquote>If you're currently running Windows 10 Version 1507, Version 1511, Version 1607 or Version 1703, you can expect to receive a notification that states that your device has to have the latest security updates installed. Windows Update will then try to update your device. When you receive the update notification, click Update now to update your device.

This update is also offered directly to Windows Update Client for some devices that have not installed the most recent updates.

Windows 10 Version 1507 and Version 1511 are currently at "end of service". This means that devices that are running these operating systems no longer receive the monthly security and quality updates that contain protection from the latest security threats. To continue receiving security and quality updates, Microsoft recommends that you update the system to the latest Windows version, Windows 10 Version 1709. Windows 10 version 1607 and version 1703 are not yet at "end of service". However, they must be updated to the latest versions of Windows 10 to ensure protection from the latest security threats.

<hr />
<p class="x-hidden-focus">Microsoft is aware that this notification was incorrectly delivered to some Windows 10 Version 1703 devices that had a user-defined feature update deferral period configured. Microsoft mitigated this issue on March 8, 2018.</p>
<p class="">Users who were affected by this issue and who upgraded to Windows 10 Version 1709 can revert to an earlier version within 10 days of the upgrade. To do this, open <strong>Settings</strong> &gt; <strong>Update &amp; Security</strong> &gt; <strong>Recovery</strong>, and then select <strong>Get started</strong> under <strong class="">Go back to the previous version of windows 10</strong>.</p>


<hr />

<em>Microsoft</em></blockquote>

Microsoft already responded in the <a href="https://support.microsoft.com/en-us/help/4023814/some-versions-of-windows-10-display-a-notification-to-install-the-late" target="_blank" rel="nofollow noopener">KB4023814</a> to the issue and offered a workaround for this. The problem is fixed with the <a href="https://chefkochblog.wordpress.com/2018/03/13/microsoft-security-updates-march-2018-edition/" target="_blank" rel="noopener">Security Patchday from March</a>.

<h2>Workarounds</h2>

<h3>Disabling the tasks fixes the problem</h3>

If you control panel -&gt; Programs and Features panel lists an entry called "Upgrade Advisor to Windows 10" just uninstall it, in additional you can also disable the tasks - you not need to delete it it's not necessary.

<ul>
    <li>Open taskschd.msc and navigate to the following paths:</li>
    <li>Task Scheduler Library\Microsoft\Windows\<b>UpdateOrchestrator\UpdateAssistant</b></li>
    <li>Task Scheduler Library\Microsoft\Windows\<b>UpdateOrchestrator\UpdateAssistantCalendarRun</b></li>
</ul>

<img class="alignnone size-full wp-image-3428" src="https://chefkochblog.files.wordpress.com/2018/03/task-scheduler.png" alt="Task Scheduler" width="1050" height="642" />

You also can check if the C:\WINDOWS\UpdateAssistant folder is empty or not, if not, delete it's content.

<h2>Rollback</h2>

You can use the setting under Settings &gt; Update &amp; Security &gt; Recovery, or restore a backup image if you have one to rollback to a previous Windows Build. In case you deleted the windows.old folder you might be out of luck in that case only an image helps.

<h2>Some people don't have the tasks why?</h2>

If you're already on Build 1709 or you used some 'privacy' tools you might not see such entries because there deleted or not existent it's also depending what was set via Group Policy Editor (gpedit.msc).

<h2>Final Words</h2>

The original intent behind this is to provide you with an upgrade if you really need it, sadly it can wrongly install the upgrade for you which is not the expected behavior. It could be a problem with the Update Assistant or on purpose to avoid that you run into a build which is end of life (and there not [yet]).

Some people saying this is due security threats which is not incorrect because you should upgrade in order to stay secure especially Windows Defender got several improvements but it's unclear what Microsoft really mean by that forcing the user to install the upgrade without the change to react or block this is not the best way in my opinion.

<h2><span style="color:#ff0000;">Update</span></h2>

The problem was meanwhile fixed by Microsoft itself. There now aware of the issue and you not need to apply the workaround, however it could help to clean the folders anyway to avoid fugue update issue.

Uninstall the KB and ensure you catch the latest update, which addresses the issue.
