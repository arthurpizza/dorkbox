---
layout: post
tags: linux commandline
date: 2012-02-24 09:30
title: "Auto-complete in Ubuntu 12.10"
published: true
slug: auto-complete-in-ubuntu-12-10
---
For some unknown (and possibly criminally dumb) reason one of the Linux desktops strongest features are horrifyingly stunted.  I'm talking about auto-complete in Bash.  Fortunately there is a quick and easy fix to un-Canonical the system.

Simply uncomment the following in /etc/bash.bashrc as SuperUser or Root:

![God, Why?](/images/why_god_why.png)

I'm not entirely sure if it will look exactly the same on your system.  This was the GNOME Remix of 12.10.  Now as this tragedy of bad decision making has been fixed I wonder if anyone knows how this could be switched off by default.  In what world is this a feature that nobody want?

**UPDATE**

I've tested it out on Xubuntu and this fix appears to be universal.
