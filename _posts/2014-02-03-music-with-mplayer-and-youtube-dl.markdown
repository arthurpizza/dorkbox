---
layout: post
tags: linux commandline youtube-dl
date: 2014-02-03 09:30
title: "Music with mplayer and youtube-dl"
published: true
slug: music-with-mplayer-and-youtube-dl
---

Last year [I wrote about my adoration for youtube-dl](/2013/06/watching-youtube-from-terminal/) and how it was awesome for streaming youtube videos without flash or even a web browser.

Since I wrote that post youtube has changed the way in how content is streamed. They have adopted DASH an adaptive steaming protocol that should make streaming more efficient on mobile data connections.

An awesome side effect of this new streaming protocol is the separation of the audio and video streams.

Using the combo of youtube-dl and mplayer you can now take advantage of the numerous full albums on youtube.

To play David Bowie’s Hunky Dory:

```
mplayer $(youtube-dl -f 140 -g http://youtu.be/YQTENuQYgjM)
```

Though the legal ramifications of all this music steaming is undetermined it’s safe to say that Google’s rumored streaming service might cover the licensing.

Until then, happy listening.
