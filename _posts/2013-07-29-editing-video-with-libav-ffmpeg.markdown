---
layout: post
tags: tech linux commandline
date: 2013-07-29 09:30
title: "Editing Video with LibAV / FFmpeg"
published: true
slug: editing-video-with-libav-ffmpeg
---

For a few weeks the Cthulhu has been out of commision.  I’ve been working on an old beat up Acer Aspire 5100 lately.  Even though the computer has a PassMark of 750 it feels more like a 75…  I’ve had some netbooks that could just crush this machine in terms of performance.  To paraphrase the old statement: the best computer is the one you have.

Chrome has really helped with the over all sluggishness of doing things online.  I will always have a special spot in my heart for Firefox, but the Fox is just too much beast for this machine.  GIMP and Ardour seem to work fantastically and the only area I’m left without many options is video editing.

Kdenlive will install, but it’s almost unusable.  What do I have left? [LibAV](http://libav.org/).

Let’s talk about the process for a second.  This is not video editing in the advanced way that Kdenlive or Openshot can give you, but more like a HD version of Kino that is powered by commandline.  There are no overlays and everything is basically one-video-one-audio-track only.  I’m sure using something like ImageMagick you could add titles, but that is for another tutorial.  Here are the 3 major steps.

1. Use LibAV to encode the videos using the in point time and out point time.

2. Use the cat command to merge them all together.

When I first started doing editing this way I learned I was limited by what codecs I can use.  Fear not, the Mpeg2 video standard looks amazing at 20 MB/s.  Within a MPG container you can use the cat command and it will merge the files effortlessly.
The camera I shoot with makes clips that are 1080p 24 fps.  This is just too much for my computer.  Let’s convert to 720p at 24 fps.  With the appropriate time stamps making clip01.mpg would probably look like this.

```
avconv -y -i video.mov -s 1280×720 -vcodec mpeg2video -vb 20M -acodec libmp3lame -ab 256k -ss 00:01:27.060 -t 8.849 clip01.mpg
```

The red marks the tags and example times of this clip.  “-ss” is when the time when the video will start encoding and “-t” is for how long.  In this example the clip is only going to be 8.849 seconds long.  I’d suggest making a shell script to automate this process, it can take a few minutes for LibAV to navigate to the start point in the clip before it starts rendering.  Also the rendering can take some time, especially if you decide to use the full 1080p format.

After all the clips have been rendered you can losslessly merge them together:

```
cat clip01.mpg clip02.mpg clip03.mpg > fullvideo.mpg
```

This part only takes a moment but the video is completed.  Next chapter: Titles!

Big shout out to [Kris Occhipinti](http://www.youtube.com/playlist?list=PLcUid3OP_4OWC-GJ6KfHK7dIK_yRKKn0e) for the original tutorials.
