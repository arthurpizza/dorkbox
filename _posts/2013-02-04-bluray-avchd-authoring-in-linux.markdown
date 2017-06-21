---
layout: post
tags: howto linux video
date: 2013-02-04 09:30
title: "Bluray / AVCHD authoring in Linux"
published: true
slug: bluray-avchd-authoring-in-linux
---
![Bluray / AVCHD authoring in Linux](/images/1280px-Blu-ray_HD_DVD.JPG)

There is a blog post from '[If Jesus was Irish](http://irishjesus.wordpress.com/2010/10/17/blu-ray-movie-authoring-in-linux/)' that attempts to tackle the Bluray / AVCHD mastering process under Linux.  The two formats are near identical.  The only difference really seems to be the disc type and bitrate of the video.  The good news?  It can be done (or so they say).  The bad news, it requires closed source applications.

Let's start by pretending you've edited your masterpiece in Kdenlive or Openshot and rendered it to an uncompressed or high quality format.  (I'm particularly fond of DNxHD  at 220 Mbit/s which is fully supported by libav/ffmpeg.)  Let's also pretend your content is industry standardized like 1920x1080 at 24fps.

What's next?  According to [x264bluray.com](http://www.x264bluray.com/) you need to encode the video into a compatible format.  I usually make AVCHDs because I don't own a Bluray burner.  The x264 bitrate is usually around 6 to 8 Mbit/s.  This looks surprisingly clean and clear.  For the audio you can use Aften to make a surround sound ac3 file or just PCM file for stereo.

Now we use our first bit of proprietary software.  [TsMuxer](http://www.videohelp.com/tools/tsMuxeR) is a muxing tool for building the file structure of your disc.

![tsMuxer](/images/tsmuxer.png)

Make sure the level on the 264 is 4.1.  This helps with compatibly.  Doesn't seem to make too much difference if you choose AVCHD or Bluray but I assume AVCHD will make help with compatibility.

The next application you need is a no-longer-supported or for sale application.  Nero 4 Linux.  I had an old disc of Nero 4 for Windows that someone gave me and I was able to use that serial number.  (I did a quick test and it seems that the serial number is easily found online also.)

![Nero for Linux Formats](/images/nero4_01.png)

When Nero launches you want to make a DVD-ROM with the UDF version set to 2.50.  The Linux udftools that can make and build a UDF image lacks the ability to build higher than 2.1.  After that drop your Bluray / AVCHD structure into the disc and burn away.

![Nero for Linux UDF](/images/nero4_02.png)

That should essentially be it.  The disc will not play in a standard DVD player but should work on most Bluray players.  One could use this for playing downloaded content but I would not suggest it.

**Disclosure:** I haven't had a chance to test this techique but I hear it works great on most Bluray players and even the PS3.  We will find out this week when my film Expendables 3 get played at my Theater.

**UPDATE!:** Found that the Movie theater Bluray players are not AVCHD compatible. However a well made 480p DVD looks pretty fantastic on the big screen. My boss made a standard DVD and it looked great. Also, the AVCHD video used in this tutorial worked on all of my girlfriends Bluray players flawlessly.
