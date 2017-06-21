---
layout: post
tags: tech linux
date: 2014-04-12 09:30
title: "Manual control for Logitech c920 in Ubuntu"
published: true
slug: manual-control-for-logitech-c920-in-ubuntu
---
I recently bought a Logitech c920 and I decided to show everyone how to get the best usage out of it in Ubuntu 14.04. I recently found out that Cheese records videos again. Because of the level of integration with PulseAudio this makes Cheese the best tool for recording video directly from the web cam and gives you the flexibility of having Pulse at your disposal.

The best part about this camera is that it’s essentially plug and play. No fussing around with drivers or modules. In low light it handles like a boss though you might want to get into manual mode to get any kind of quality picture out of it at that point. The best way that I’ve found is to run guvcview in control mode.

```
guvcview -o
```

This let’s control the focus and exposure manually. That level of control can add a lot to your videos. For those who don’t know, WebM is an open video format that is compliant with the HTML5 specification.

This webcam is almost flawless. It works in Skype, Google Hangout, and even in YouTube for direct upload without breaking a sweat. It clips easily to any monitor and even has a tripod mount on the bottom. I also tested it in ChromeOS on my Chromebook and it worked just as smoothly there. In my humble opinion there is no better webcam for Linux.

[Amazon has a full spec list and better images than I took for those who are curious.](http://www.amazon.com/gp/product/B006JH8T3S?ie=UTF8&camp=213733&creative=393185&creativeASIN=B006JH8T3S&linkCode=shr&tag=arthursucks-20&qid=1397314316&sr=8-1&keywords=logitech+c920)
