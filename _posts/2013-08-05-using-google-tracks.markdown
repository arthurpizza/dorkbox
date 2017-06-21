---
layout: post
tags: life android opensource
date: 2013-08-05 09:30
title: "Using Google Tracks"
published: true
slug: using-google-tracks
---
<img class="alignright" width="300" src="/images/th/google-tracks.png">There was a time not long ago that I weighed almost 300lbs.  I’m not ashamed.  In fact I’m proud of the weight loss.  I’m still a fatty (always will be, being a fatty is all in your head!) but I’ve made a lot of progress.  At the time of writing this I’m down to 218lbs.  I still have quite a way to go.

One of the tools that made the weight loss easier was great software to help me track my progress.  I was using [Endomondo](http://www.endomondo.com/) for the longest time.  I actually bought the full version of the application when it went on sale for 25¢.  These days I’ve become quite annoyed with the service.  Besides constantly wanting me to spam my friends and upgrade to a monthly ‘service(?)’ the application keeps getting more and more bloated.  I’m officially breaking up with Endomondo.

Hello My Tracks!  The program limits itself to raw numbers.  It doesn’t calculate calories burned but will tell you the elevation, distance, time, and a whole slew of other data.  These numbers are for you to crunch.  I’ve stumbled upon a overly simplistic calculation of calories:

```
0.0(mph) x weight x time = calories
```

Using the data from the screen shot my last walk would calculate to:

```
0.027 x 218 x 81 = 476.766
```

Or 477 calories burned.  This system seems to be in the same ballpark to what Endomondo was giving me.  Because of all the variables calorie counting is not an exact science.  I can assume that part of the reason it was left out of My Tracks.  Perhaps you know of a better calculation?

The business model of Endomondo seems to be the biggest drawback.  My Tracks is an [open source application](http://code.google.com/p/mytracks/) that will probably keep growing in features.  With the addition of a flexable API it opens a lot of doors for integration with other applications.  For my personal needs My Tracks is a better all around fit.  If you’re looking for a solution that respects your user right give My Tracks a try.
