---
layout: post
title: Mozilla: Guiding principles for Shield Studies
date: 2018-01-31 20:42
author: nvinside
comments: true
categories: [Browser, Firefox, Mozilla]
---
Mozilla explains the latest disaster, the Mr. ROBOT story and there showing some more details, their <a href="https://dxr.mozilla.org/mozilla-central/source/toolkit/components/telemetry/docs/internals/preferences.rst">latest documentation</a> reveals a bit more what's going on in such opt-in studies. Looking Glass was released as a system add-on to Firefox which meant that users saw the add-on appear in the browser's add-on manager without them initiating the installation - to avoid the next shitstorm there now stronger rules.

<img class="alignnone size-full wp-image-2475" src="https://chefkochblog.files.wordpress.com/2018/01/mozilla-looking-glass-featured.png" alt="mozilla-looking-glass-featured" width="800" height="450" />

<!--more-->

Mozilla create a new set of principles for Shield studies so that something like Looking Glass won't happen again which includes the following:

<ul>
    <li>All Shield studies must answer specific questions.</li>
    <li>All Shield studies must be named accurately. - Same names are still confusing anyway.</li>
    <li>Shield studies will always respect user privacy.</li>
    <li>All Shield studies adhere to the "scientific method for answering complex questions".</li>
    <li>All Shield studies require a Product Hypothesis Doc which outlines the research question the study is trying to answer.</li>
</ul>

<h2>How to opt-out?</h2>

Untick all checkboxes at <strong>about:preferences#privacy-reports</strong> and you’re opted-out of these. Alternative you can work with about:config:

<ul>
    <li>app.shield.optoutstudies.enabled = false</li>
    <li>extensions.shield-recipe-client.api_url = “” (empty string)</li>
    <li>extensions.shield-recipe-client.enabled = false</li>
</ul>

The toggles are documented <a href="https://dxr.mozilla.org/mozilla-central/source/toolkit/components/telemetry/docs/internals/preferences.rst">here</a>.

<h2>Mozilla lost some trust and it's hard to earn some back</h2>

Quantum is such a nice Browser but Mozilla lost a lot of trust with such stupid studies and tests, I'm not a fan of such things or if they really want to test stuff like that they should implement it only in nightly builds and not into ESR/stable builds with specific details and documentation - That's, in my opinion, the only way however, Mozilla already changed this and by default since FF 57+ all Telemetry in all stable builds are opt-in except the 'security' related telemetry like eg. certificate checks or their own opt-in/opt-out malware/blacklist to avoid phishing and other threats.

I think this Looking Glass thing was not a study, but a game. It was advertising Firefox to Mr. Robot fans, not the other way around, as the add-on was completely inactive unless the user did something particular as prompted by one of Mr. Robot’s episodes. But anyway that was scary and people reported it was enabled by default, while others said it wasn't - still not what I like to see from Mozilla.

<h2>Final words</h2>

We all need to learn a lot each day when it comes to private data and even the big ones making some mistakes here and then, the thing is that the responsability is huge and when someone should take you seriously on your promises you must provide a good documentation and source code so that this can be checked, Mozilla did this since day one and that's the reason I still think it's a good Browser and a good community, we just - like all of us - need to be more careful on which data we collect and what data we submit into the internet.

<h4><span style="text-decoration:underline;">Source</span></h4>

<ul>
    <li>
<p class="entry-title">Retrospective: Looking Glass (<a href="https://blog.mozilla.org/firefox/retrospective-looking-glass/">blog.mozilla.com</a>)</p>
</li>
    <li>
<p id="section_0">Firefox/Shield/Shield Studies (<a href="https://wiki.mozilla.org/Firefox/Shield/Shield_Studies">wiki.mozilla.org</a>)</p>
</li>
</ul>
