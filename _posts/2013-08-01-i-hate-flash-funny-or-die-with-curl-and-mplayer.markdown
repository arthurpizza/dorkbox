---
layout: post
tags: tech funny linux
date: 2013-08-01 09:30
title: "I hate flash : Funny or Die with Curl and Mplayer"
published: true
slug: i-hate-flash-funny-or-die-with-curl-and-mplayer
---
![](/images/funny_or_die_mplayer.jpg)

I did a post earlier this week about [watching YouTube videos with Mplayer](/2013/06/watching-youtube-from-terminal/) and I found that comedy site Funny or Die also also has high definition videos that can be played in mplayer.

For this video I’ll be using the Cheese & Chong read the Bible video.  It’s pretty funny.  We need to make sure “curl” is added from the repository.

```
curl http://www.funnyordie.com/videos/7e64d0be37/cheech-chong-read-the-bible | grep mp4
```

This will push out a lot of data but only the lines with “mp4″ in them.  The line we’re looking for is:

```
http://vo.fod4.com/v/7e64d0be37/v110.mp4
```

Above it you’ll also see a list of video bitrates:

```
110,200,400,600,1200,1800,2500
```

By changing the number to the proper bitrate you can get the better quality video.

All that’s left is to load it into mplayer.

```
mplayer http://vo.fod4.com/v/7e64d0be37/v2500.mp4
```

No need for flash.
