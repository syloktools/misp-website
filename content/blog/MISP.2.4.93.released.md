---
title: MISP 2.4.93 released (aka ATT&CK integration)
date: 2018-06-27
layout: post
banner: /img/blog/misp-small.png
---

A new version of MISP [2.4.93](https://github.com/MISP/MISP/tree/v2.4.93) has been released including a much improved and tightly integrated [MITRE ATT&CK](https://attack.mitre.org) interface, a new event locking functionality, initial support for a multilingual interface, various fixes including a security fix ([CVE-2018-12649](https://cve.circl.lu/cve/CVE-2018-12649)).

MITRE ATT&CK offers an excellent, efficient and very complete framework to describe adversarial tactics and techniques, which MISP now directly incorporates as a way to contextualise the information contained within (at the event and attribute levels) and to share the contextualised data with your partners. We have been supporting the use of the ATT&CK framework via the [misp-galaxy](/galaxy.html) from the early beginning but we quickly realised the limitations of using this technique in MISP. So we decided to improve the user-interface by having the ATT&CK matrix directly accessible in MISP in order to be able to more intuitively attach techniques and tactics to MISP data following a method that is more universally linked to ATT&CK. The global statistics were also extended in order to get a quick overview of techniques used.

<div class="myvideo">
   <video  style="display:block; width:100%; height:auto;" autoplay controls loop="loop">
        <source src="{{ site.baseurl }}/img/video/attack.webm"  type="video/webm"  />
   </video>
</div>

A new functionality has been introduced called the event lock which shows users if another user is editing the event they're viewing (same organisation only).

STIX 2 export now includes PE binaries and better support for MISP objects.

STIX 1 import has been significantly improved in regards to its capabilities when importing AIS/US-CERT STIX files that include specific relationships for malware samples.

A new functionality has been added to allow the toggling of the UI language of the MISP interface (part of the ongoing [internationalization effort](https://github.com/MISP/misp-book/tree/master/translation)) .

[CVE-2018-12649](https://cve.circl.lu/cve/CVE-2018-12649) has been fixed, which allowed attackers to bypass the brute force protection via PUT requests.

Many bug fixes (including some to the install guides) and minor features including impfuzzy validation.

The full change log is available [here](https://www.misp.software/Changelog.txt). [PyMISP change log](https://www.misp.software/PyMISP-Changelog.txt) is also available.

A huge thanks to all the [contributors](/contributors) who helped us improve the software and also all the participants in MISP trainings giving us a bunch of interesting feedback for improvements.

MISP [galaxy](/galaxy.pdf), [objects](/objects.pdf) and [taxonomies](/taxonomies.pdf) were notably extended by many contributors. These are also included by default in MISP. Don't forget to do a `git submodule update` and update galaxies, objects and taxonomies via the UI.

Don't forget that the MISP Threat Intelligence Summit 0x4 will take place the Monday 15th October 2018 before hack.lu 2018. A [Call-for-Papers is open](https://cfp.hack.lu/misp0x4/) for the MISP Threat Intelligence Summit 0x4. We would be glad to see users, contributors or organisations actively using MISP or/and threat intelligence to share their experiences and presentation to the CfP.
