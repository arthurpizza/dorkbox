---
layout: post
tags: blog commandline
date: 2015-10-01 09:30
title: "The Joy of Jekyll"
published: true
slug: joy-jekyll
---
![Jekyll](/images/jekyll.png)

Like many before me, I've ditched Wordpress and took the plunge into Jekyll. It was natural to use Jekyll after working with WordPress for so long. There are trade offs but I feel that Jekyll is a better platform for my creativity.

In the last year or so I've really thrown myself into using VIM. It's availble on my Apple PC at work, my Chromebook (With Crouton) and ofcourse my Linux box at home. (For Android I like [Turbo Editor](https://github.com/vmihalachi/turbo-editor).)

**VIM and Jekyll go great together**

## Hosting

To host a plain text website there are a million choices. My two favorites at this moment are [Surge.sh](http://surge.sh) and the very popular [Github](https://github.com). I ultimately went with Github because I can make updates with git. I like git.

## Cloudflare

[Cloudflare](https://www.cloudflare.com/) is a popular (and sometimes [controversial](https://scotthelme.co.uk/tls-conundrum-and-leaving-cloudflare/)) service. They act as a free CDN but also offer a lot of other awesome features. I use them for the free TLS. This adds a layer of encryption between the user and the domain but doesn't encrypt between the domain and the server. After thinking it through, I decided that a little security is better than zero security. Hopefully once the [Let's Encrypt](https://letsencrypt.org/) project takes over I can add full encryption from Github.

Most my dynamic sites will probably go this route with the exception of [ConsBEERacy](http://consbeeracy.com). ConsBEERacy is a podcast that I work on (I'm not one of the hosts, sorry. The hosts are really awesome and you should listen!) and it needs the WordPress framework.
