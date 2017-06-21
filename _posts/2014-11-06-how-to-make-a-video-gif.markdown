---
layout: post
tags: video editing
date: 2014-11-06 09:30
title: 'How to Make a Video "GIF"'
published: true
slug: how-to-make-a-video-gif
---

![](/images/make-a-video-gif.jpg)

It seems to be all the rage these days.

A video “gif” is a silent video embedded to a site in loop mode. I guess the audio is an optional thing but most go without it.

## Step One: Prepare the video file

Use your favorite video editor to trim your video down to just a few seconds. To be an awesome looping “gif”, try your best to make it look seamless. I used kdenlive but almost any modern video editor will work. Render it out to either mp4 (h264) or webm (vp8) or both if you’d like to keep compatibility.

## Step Two: The Code

It’s pretty easy. This even works on WordPress.

```
<video autoplay="autoplay" loop="loop" width="480" height="480">
  <source src="loop.webm" type="video/webm" />
</video>
```

If you want to add support for h264.

```
<video autoplay="autoplay" loop="loop" width="480" height="480">
  <source src="loop.webm" type="video/webm" />
  <source src="loop.mp4" type="video/mp4" />
</video>
```

## Enjoy your creation!

Now obviously I don’t expect everyones to be as awesome as mine but I’m sure you’ll figure it out.
