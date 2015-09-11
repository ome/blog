---
layout: post
title: Java Web Start
categories: tech-issues
---

##Summary

This is the end, beautiful friend. This is the end.
##Background

Java Web Start was introduced in 2001 to allow applications to be launched through browsers or directly via the Java Network Launching Protocol (JNLP).

Java Web Start Applications do not run inside the browser like Applets but still run in a restricted environment. Those restrictions can be removed by signing the applications with a trusted certificate. This has been encouraged since Java 7 update 21 to reduce risks for desktop users and it has been reinforced in follow-up updates.
Two security changes to enhance authentication and authorization for Java Web Start (and Applets) were introduced back in January 2014 with Java 7 update 51.

As of Java 7 update 51
Rich Internet Applications must contain two things:
 1. Code signatures from a trusted authority.
 2. Manifest Attributes:
   1. Permissions (required) indicating if the application should run within the sandbox or it requires full-permissions.
   2. Codebase (recommended): location of the hosted code.

Due to vulnerabilities affecting Java plugins, security experts frequently recommend users to disable Java at least in their browser. Since 2013, Firefox, Google Chrome and other browsers have started to block plugins by default.

##What does it mean for desktop developers/administrators?

To deploy Java Web Start, one first needs to get familiar with [Deployment Rule Sets](https://blogs.oracle.com/java-platform-group/entry/introducing_deployment_rule_sets).
Administrators can then create a list of known-safe applications and manage compatibility between
different versions of Java on the system.
Each browser will have their own set of dialogs and control mechanisms.

It is getting harder and harder to distribute Java Web Start applications for developers and/or administrators.


##What about Browser support?

The Java plug-in for web browsers relies on the cross platform plugin architecture [NPAPI](https://en.wikipedia.org/wiki/NPAPI), which has been supported by all major web browsers for the past 10 years.
In version 45 (released Sept 2015), Google's Chrome has dropped support for [NPAPI plugins like Java](https://support.google.com/chrome/answer/6213033).
This means that you can't enable Java in Google Chrome 45 (or later).
Firefox, Internet Explorer and Safari still continue to support it but for how long?

During our testing we are increasingly encountering unpredictable issues, across all platforms, with various combinations of browsers, browser versions, Java versions and Java Web Start.

##OMERO and Java Web Start

For the past few years, the Java Desktop clients could be distributed as Java Web Start Applications. Such feature was requested by several institutions.
We totally acknowledge that it is a practical and still active way to distribute the applications across an institution. But, due to the steady increase of issues not under our control,
we have concluded that continuing to support the use of Java Web Start for distribution of the OMERO Desktop clients is unsustainable.

In recently released versions of OMERO, we made significant effort to unify the OMERO Desktop and Web clients.
With new import options available via, for example, OMERO.dropbox or in-place, more features like ROI support being worked on in the Web client and the drop of Java support in Web Browser by Google, we feel that it is time to deprecate the distribution of our Desktop clients as Java Web Start applications.
We will stop releasing them from OMERO version 5.2.


