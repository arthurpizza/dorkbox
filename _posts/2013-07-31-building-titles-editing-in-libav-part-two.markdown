---
layout: post
tags: tech linux commandline
date: 2013-07-31 09:30
title: "Building Titles (Editing in LibAV part two!)"
published: true
slug: building-titles-editing-in-libav-part-two
---

One of the biggest challenges with making a video in LibAV/FFmpeg is the lack of title cards.  Using the GIMP (or ImageMagick) you can make some very awesome title cards and convert them into a static video clip to be mixed in with your other clips.

If you rememeber the camera shot clips at 1080p 24fps h264.  We encoded the clips to 720p 24fps with Mpeg2Video.  An older video format, but gives us the advantage of using the “cat” command.

![New Image in GIMP](/images/title-new-image.png)

In the GIMP all you have to remember is to match the resolution.  Everything else will be done with LibAV.  Here is the image I made for this blog:

![Test Title](/images/title-test.png)

When we make this clip there are two things to keep in mind.  First, if there is no audio in this clip the following video clips’ audio will be offset.  Second, if the AV sync is off on this clip it was also effect the following clips.  This clip will be exactly 4 seconds.  Let’s make some noise… er silence:

```
avconv -ar 48000 -ac 2 -f s16le -i /dev/zero -t 4 temp.wav
```

```
lame -b 256 temp.wav temp.mp3
```

This will convert solid zeros to pcm making a blank (quiet) track of 4 seconds with the same bitrate of the other clips.

```
avconv -loop 1 -i title.png -r 23.976
```

```
-vcodec mpeg2video -vb 20M -t 4 tempvid.mpg
```

The “loop” command is what duplicates the single frame into 24 fps.  Also note the “-t 4″ again.  We now how a video and audio clip of the same length.  I think you can see where we go from here.

```
avconv -i tempvid.mpg -i temp.mp3
```

```
-vcodec copy -acodec copy title.mpg
```

Now when you cat this clip with the others it will merge perfectly.

**PROTIP!**

If you have ImageMagick installed you can build a simple title image with this command:

```
convert -size 1280×720 xc:black -font Ubuntu -pointsize 64 -fill white -draw “text 150,600 ‘Sample Text'” temp.png
```

It doesn’t look as good as the GIMP and I haven’t figured out a good way to center the text yet, but it works in a pinch.  Perhaps someone better at ImageMagick can help out with that.
