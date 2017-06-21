---
layout: post
tags: linux security passwords
date: 2014-05-03 09:30
title: "Passwords with APG"
published: true
slug: passwords-with-apg
---
I believe APG stands for Automatic Password Generator. I’m not 100% sure but I believe it’s installed in the Default of Ubuntu and Debain Linux. If not you can always just run:

```
sudo apt-get install apg
```

By default it will generate 6 passwords.

```
apg
```
```
KayRoowlUv8 (Kay-Roowl-Uv-EIGHT)
```
```
yeibfigsOis6 (yeib-figs-Ois-SIX)
```
```
wofJect6 (wof-Ject-SIX)
```
```
UzCyibShycs4 (Uz-Cyib-Shycs-FOUR)
```
```
Vafkarag9 (Vaf-kar-ag-NINE)
```

This includes the verbal pronunciation of the password by default.

I like to run the command:

```
apg -m 16
```

This will give you a minimum character count of 16. Personally I like to store my passwords in a spreadsheet. Weather you want local files or cloud based spreadsheets from Google or Microsoft is up to your discression.

**UPDATE FROM 2015**

Recently I've begun using

```
apg -n 12 -a 1 -MNCl -m 16
```

This makes a 16 character password that is easily copy and pasted but still very powerful. To save time you can script this.
