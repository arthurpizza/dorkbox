---
layout: post
tags: blog
date: 2016-02-28 10:00
title: "Starbucks Wifi and Tor"
published: true
slug: starbucks-wifi-and-tor
---

I like wifi access points that are relatively accessible and free. I really love the fact that the Los Angeles library and the Long Beach Library both have free, uncensored wifi. This is how it should be. Any publicly funded areas should have wifi for the community.

In most of the United States it's become common for both McDonald's and Starbucks to offer free wifi to all their patrons as well. Originally it was AT&T or Google Wifi but a new Starbucks opened near my house that has a Starbucks branded wifi connection. The first thing I noticed was it was drastically slower than the wifi offered by Google. The second thing I noticed was that port 22 was blocked.

Now a few blocks over there is an older Starbucks that has both a faster Internet and one where I have no problem remotely logging into my Noodlebox at home. However tonight, I just ordered my drink and I was really enjoying the location and the raw energy from the people in this lively setting. What to do?

### Onions are a geeks best friend

The tools I generally use are:

* tor
* torsocks
* ssh
* sshuttle (optional)

You can fire up a terminal or (tmux pane) and run the tor command. It's gonna to connect slowly because you're gonna be limited by the slow Starbucks internet.

In a new terminal getting connected is as easy as:

```
torsocks ssh username@host
```

Everything should connect just like normal.

To add succurity to your starbucks surfing you can also run:

```
torsocks sshuttle username@host
```

And you entire wireless stack will be networked through tor into your remote server.

### Free as in Wifi, not free as in Coffee

Starbucks access to the internet is awesome. Especially for those who need it, but if you do anything other than Facebook it might be a pain. Having an awesome toolkit of networking tools is almost completely necessary to get any real work done.
