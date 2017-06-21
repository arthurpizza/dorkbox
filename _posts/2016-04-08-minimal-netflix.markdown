---
layout: post
tags: blog
date: 2016-04-08 10:00
title: "Minimal Netflix"
published: true
slug: minimal-netflix
---

I like Netflix. It's literally the main reason I install Chrome browser on my system. Even with the [looming price increase] it's still a very good value. Chances are if you're reading this you're already a fan as well.

![Working Hard](/images/netflix.png)

So I sometimes like to watch videos while surfing reddit or doing work. So a lot of the time I like to have a little window on the bottom right of my screen. With my go-to video player, [mpv], it's easy. However Chrome has all these tabs and stuff that ruin the experience.

The solution is my new favorite command:

```
google-chrome-stable --app=http://netflix.com
```

This opens only the page you want in app mode. It's nice. I like to alias it with:

```
alias netflix='google-chrome-stable --app=http://netflix.com &'
```

I'm not sure if it really uses less resources but it feels snappier. It's a simple way to load only what you want or need. Now I just need to find a way to do this on ChromeOS.

[looming price increase]: http://www.businessinsider.com/netflix-will-increase-prices-in-may-2016-4
[mpv]: https://mpv.io/
