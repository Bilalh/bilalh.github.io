---
author: Bilal Syed Hussain
date: 2012-05-18T13:48:44Z
description: MPlayer OSX Extend release 2
draft: false
tags:
- MPlayer
title: MPlayer OSX Extended Release 2
topics:
- release
type: post
---

This is build contains all the features in the [previous build]({{<  ref "mplayer-osx-extended1.md" >}}) with a few new additions.


[Download Link](https://github.com/downloads/Bilalh/MPlayer-OSX-Extended/MPlayer%20OSX%20Extended%20rev15-test1-build%202.zip "MPlayer OSX Extended Binary")

[GitHub Repository](https://github.com/Bilalh/MPlayer-OSX-Extended "MPlayer OSX Extended GitHub Repository")

New Features
------------

### Proxy Icons ###

I Added a Proxy Icon when a file is playing, which  is invoke by clicking on the icon in the menu bar, this brings up the menu shown below which allows the user to open the folder the movie is placed in.

![Proxy Icon]({{< path "media/posts/MPlayer-OSX-Extended/proxy_icon.png" >}})

### Next Episode ###

A menu item (Play Next Episode) that plays the next episode based on the currently playing file was added in previous build and was bound to ⌘E. This works for most formats of naming including

    File Name 01
    File_Name_1
    File Name Episode 1

This build added an extra option to play the next episode automatically, saving the user  from clicking on the `Play Next Episode` menu item each time.

![Next Menu]({{< path "media/posts/mplayerosx/next_menu.png" >}})

Compatibility
-------------

Nearly all of he features have been merged in the main repository, meaning that will no compatibility issues in the future.

Other Improvements
------------------
This build also contains other features to improve the image quality.
