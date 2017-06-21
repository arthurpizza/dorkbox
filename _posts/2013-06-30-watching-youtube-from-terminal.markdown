---
layout: post
tags: life
date: 2013-06-30 09:30
title: "I hate flash : Watching youtube from terminal"
published: true
slug: watching-youtube-from-terminal
---

I hate flash.  It’s taking a very long time dying but it needs to die.  Sadly there are a lot of amazing websites that use it.  Fortunately I found a quick trick to watching youtube videos from the terminal.  This requires youtube-dl and mplayer.  Both should be in most major Linux distros repositories.

```
mplayer -fs $(youtube-dl -g -f 22 youtube.com/watch?v=3V35jvY0u7I)
```

The key tags are the “-g” that prints out the actual video location for mplayer and “-f 22″ is an optional tag for selecting the quality / codec  Without this tag it will load the highest quality video.  You can find a complete list of format tag numbers on the [YouTube Wikipedia page](https://en.wikipedia.org/wiki/YouTube#Quality_and_codecs).
