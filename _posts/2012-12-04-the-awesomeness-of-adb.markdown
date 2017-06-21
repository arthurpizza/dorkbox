---
layout: post
tags: adb commandline android
date: 2012-12-04 09:30
title: "The awesomeness of ADB"
published: true
slug: the-awesomeness-of-adb
---

Installing [ADB](http://wiki.cyanogenmod.org/wiki/ADB) on any Ubuntu based system is as simple as adding the ‘[android-tools-adb](apt://android-tools-adb)‘ package. You can also add the package through the command line:

```
sudo apt-get install android-tools-adb
```

Once installed you should make sure your cellphone ‘Android Debugging’ is switched on. Then it’s as simple as:

```
sudo adb devices
```

This should find and mount your phone. This opens up a lot of awesome options like the ability to push and pull files from the phone. You can use:

```
adb shell
ls
```

To open a minimal shell window into your hardware. Here are some quick examples I use:

```
adb pull sdcard/downloads/happy.jpg ~/happy.jpg
adb push ~/Downloads/movie.mp4 sdcard/Movies/
```

When you’re done just a quick:

```
sudo adb kill-server
```

Unmounts the hardware. From what I can tell you can only use one device per session. However their might be much more advanced steps I’m missing. Hope this gets you started.