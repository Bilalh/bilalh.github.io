---
author: Bilal Syed Hussain
date: 2011-12-20T17:37:31Z
modified: 2015-11-01T01:15:27Z
description: MPlayer OSX Extend release
draft: false
tags:
- MPlayer
title: MPlayer OSX Extended Release 1
topics:
- release
type: post
aliases:
 - /2011/12/20/mplayer-osx-extended/
---


A new binary of [MPlayer OSX Extended]({{< path "mplayer-osx-extended/" >}} "MPlayer OSX Extended") has been released  

[Download Link](https://github.com/downloads/Bilalh/MPlayer-OSX-Extended/MPlayer%20OSX%20Extended.zip "MPlayer OSX Extended Binary")

[GitHub Repository](https://github.com/Bilalh/MPlayer-OSX-Extended "MPlayer OSX Extended GitHub Repository")

New Features
--------

### File Types Information ###

I added type information about movies as shown below. This gives the user more info when looking at video/audio  files in Finder.
![Filetypes]({{< path "media/code/MPlayer-OSX-Extended/Filetypes.png" >}})


### Media Keys ###
Support for media keys (F7, F8, F9) on Apple keyboards has been added.

| Key              | Function         |
|:-----------------|:-----------------|
| PlayPause (F8)   | Plays/Pauses     |
| Rewind(F7)       | Skip to Previous |
| Fast forward(F9) | Skip to Next     |


### Keyboard ###
All of MPlayer keyboard shortcuts have been added, a list of keyboard shortcuts is in the help and can be viewed [here]( {{< ref "mplayer-keybindings.md" >}} "Complete List of keyboard shortcuts").


### Help ###
I am (re)wrote most of the help

### Next Episode ###
A menu item (Play Next Episode) that plays the next episode based on the currently playing file has been added and is bound to  ⌘E. This works for most formats of naming including

* File Name 01
* File\_Name\_1
* File Name Episode 1

### Icons ###

Icons for all the file types have been added, below are a sample the rest can seen [here](https://github.com/Bilalh/MPlayer-OSX-Extended/tree/build/extras/File%20Type%20Icons "Complete set of icons").


### Video Icons ###
![Video Icons]({{< path "media/code/MPlayer-OSX-Extended/Video.png" >}})

### Audio Icons ###
![Audio Icons]({{< path "media/code/MPlayer-OSX-Extended/Audio.png" >}})

### Subtitles Icons ###
![Subtitles Icons]({{< path "media/code/MPlayer-OSX-Extended/Subtitles.png" >}})

### Binary Icon ###
![Binary Icon]({{< path "media/code/MPlayer-OSX-Extended/Binary.png" >}})
