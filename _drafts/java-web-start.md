---
layout: post
title: Java Web Start
categories: tech-issues
---

##Background

Java Web Start was introduced in 2001 to allow applications to be launched through browsers or directly via the Java Network Launching Protocol (JNLP).

Java Web Start Applications do not run inside the browser like Applets but still run in a restricted environment. Those restrictions can be removed by signing the applications with a trusted certificated. This has been encouraged since Java 7 update 21 to lower risks for desktop users and it has been re-inforced in follow-up updates.
Two security changes to enhance authentication and authorization for Web Start (and Applets) were introduced back in January 2014 with Java 7 update 51.

As of Java 7 update 51
Rich Internet Applications must contain two things:
1. Code signatures from a trusted authority.
2. Manifest Attributes:
   i. Permissions (required) indicating if the application should run within the sandbox or it requires full-permissions.
   ii. Codebase (recommended): location of the hosted code.

Due to vulnerabilities affecting Java plugins, users are now frequently recommended to disable Java, at least, in their favorite browser. Since 2013, browsers like Firefox, Google chrome just to mention a few have started to block plugins by default.
The US Department of Homeland Security has been recommended since 2013 to disable Java in Web browsers unless it is absolutely necessary to run it.

##What does it mean for desktop administrators?

To deploy Java Web Start, you first need to get familiar with [Deployment Rule Sets](https://blogs.oracle.com/java-platform-group/entry/introducing_deployment_rule_sets).
Administrators can then create a list of known-safe applications and manage compatibility between
different versions of Java on the system.
Each browser will have their own set of dialogs and control mechanisms

Conclusion
It is getting harder and harder to distribute Java Web Start applications for developers and/or administrators.


##What about Browser support?

The Java plug-in for web browsers relies on the cross platform plugin architecture [NPAPI](https://en.wikipedia.org/wiki/NPAPI), architecture supported by all major web browsers for the past 10 years.
In version 45 (released Sept 2015), Google's Chrome has dropped support for [NPAPI plugins like Java](https://support.google.com/chrome/answer/6213033).
This means that you can't enable Java in Google Chrome 45 (or later).
Firefox, Internet Explorer and Safari still continue to support it but for how long?

During our testing we are increasingly encountering unpredictable issues, across all platforms, with various combinations of browsers, browser versions, Java versions and Java Web Start.

##OMERO and Java Web Start

For the past few years, the Java Desktop clients could be distributed as Java Web Start Applications. The feature was requested by several institutions. But due to the steady increase of issues,
we have concluded that continuing to support the use of Java Web Start for distribution of the OMERO Desktop clients is unsustainable.

In recently released versions of OMERO, we made significant effort to unify the OMERO Desktop and Web clients.
With new import options available via, for example, dropbox or in-place, more features like ROI support being worked on in the Web client and the drop of Java support in web browser by Google, we feel that it is time to deprecate the distribution of our Desktop clients as Java Web Start applications.
We will stop releasing them from OMERO version 5.2.


