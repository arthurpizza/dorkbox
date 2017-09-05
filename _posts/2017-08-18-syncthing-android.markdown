---
title: Syncthing and Android
layout: post
---
![Writing this post in Writeily](/images/writeily.png){:.alignright width="256"}In spite of the annoyance of my friends, girlfriend, and anyone else I collaborate with I've been trying to reduce my dependence on Google. I've been minimally effective at this. One of the biggest perks of using Google products is the integration with both the mobile and web.

I can work on a project on my phone, move to the computer, and pick up where I left off. To do this gives Google full unbridled access to your projects. If those projects are important then it makes sense to keep them as secure as possible.

### Alternative Solution

There is an awesome open source writing application for Android called [Writeily] that uses Markdown. It works really well and because it saves to a native Markdown format it's perfect for going between VIM and Gedit as needed.

I like working in Markdown. Part of the joy I get from running this site with Jekyll is the incredible power that Markdown affords. For all my day to day documents I write in Markdown. If I need a PDF or a Docx I can just generate one from my Markdown with [Pandoc].

The last piece of the puzzle is [Syncthing]. When I first started using Syncthing for Android it was a total battery killer but it looks like they've really got the Android version under control in that department.

### Setting it up

By default Writeily makes a folder in your SD card partition.

```
/sdcard/writeily/
```

Using Syncthing I connected it to a folder on my desktop.

```
~/Documents/Writeily/
```

When I feel like busting out a document (Like this post I'm writing on both my Android phone and my computer) I just edit wherever I am. It syncs almost instantaneously.

For me this work really good.

### Limitations

Collabritive editing is not baked into this solution. Theoretically you could do collaborative editing using git but that would not be real time, plus no one I know uses Markdown for everyday documents. Yet.

Right now using git on mobile is less than steller. There is also [Prose](https://n0pe.org/2017/08/02/prose/) that would allow you to edit git projects on mobile but at time of writing that only works with Github. Not everyone wants there project on display.

I am one of those weirdos that has [Termux] on my phone with ssh and git. Though akward, I can even copy my markdown document into my `_posts` folder and push a new post to my site through Termux. It's not perfect but it works in a pinch.

[Writeily]: https://github.com/plafue/writeily-pro
{:target="_blank"}

[Pandoc]: http://pandoc.org/
{:target="_blank"}

[Syncthing]: https://syncthing.net/
{:target="_blank"}

[Termux]: https://termux.com/
{:target="_blank"}
