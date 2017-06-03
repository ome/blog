---
layout: post
title: User survey for OME Files C++
categories: ome-files future-plans
---

## User survey

Are you an existing OME Files C++ user?  Or planning to use it in the
future?  Or simply considering the possibility of using it?  We would
like to know which operating systems and compilers you're using, or
planning to use, so that we can focus our efforts to support your
requirements.

At our recent [Annual Users
Meeting](http://www.openmicroscopy.org/site/community/minutes/meetings/12th-annual-users-meeting-2017),
we discussed some of these requirements with attendees in some of the
workshops and meetings, but we don't want anyone who didn't attend, or
who attended but didn't have a chance to discuss their requirements,
to miss out on the opportunity to do so.

We have created an [online
survey](https://goo.gl/forms/cCMqLc6eSwhcV2dP2) which asks several
questions about your requirements.  We would be very grateful if you
could take a few minutes to fill it out.

The survey will close on Monday the 19th of June.

## Existing operating system and compiler support

We put a lot of effort into making sure that OME Files C++ builds and
runs on the wide variety of operating systems, compilers and hardware
platforms which our users care about, plus some less common variants
to further improve the correctness and portability of our codebase.
Each system we officially support is backed by dedicated continuous
integration infrastructure, taking care of daily software builds as
well as the release builds for our release download pages.  However,
our resources (hardware and developer time) are not infinite, and we
need to ensure that our efforts are directed appropriately to
supporting the configurations which are actively in use, dropping old
configurations as they cease to be used, and adding new ones to keep
up to date with current development and user demand.

We are currently working to upgrade our continuous integration
infrastructure, in particular to move from an *ad hoc* collection of
manually managed machines running on bare metal or virtually with
VMware, to virtual machines provisioned and managed with OpenStack and
Ansible.  Supporting new platforms will be simpler and faster with the
new setup, and this will enable us to be more responsive to requests
for new configurations.

## Use of the survey data

There are several questions which we would like to answer to help
complete this infrastructure upgrade, which include:

  - Which Microsoft Visual Studio versions should we support?  Should
    we drop VS2013 support, or add VS2017 support?  What's in use
    right now, and expected in the future?
  - Which Linux distributions are used for development and deployment?
    Should we add or drop support for any particular distributions?
  - Which compilers are most commonly used?  What's the baseline set
    of features we should require?

Other questions include:

  - What are your existing and planned uses of OME Files?  Can we do
    anything specific to improve our support for these uses?
  - Can we improve what we offer for download on our release download
    page, or via other channels?

We would very much appreciate your input.  If we don't get any
feedback telling us that particular systems or compilers are required,
we'll assume that support for these is not actively required, and this
may result in support for these being dropped in the future, so please
do let us know what you need from us.


[Go to the survey](https://goo.gl/forms/cCMqLc6eSwhcV2dP2)