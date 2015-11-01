---
author: Bilal Syed Hussain
description: Contributions to MPlayer OSX Extended
info: MPlayer OSX Extended is a video player leveraging the power of the MPlayer and FFmpeg. I have contributed icons and some features to the project and up to data binaries.
draft: false
github: Bilalh/MPlayer-OSX-Extended
title: MPlayer OSX Extended
type: code
num: 100
languages:
    - C
    - Icons
aliases:
    - projects/mplayer-osx-extended/
---


This page contains some of my contributions to the MPlayer OSX Extended project


File Types Information
----------------------
I added type information about movies as shown below. This gives the user more info when looking at video/audio files in Finder.
![Filetypes]({{< path "media/code/MPlayer-OSX-Extended/Filetypes.png" >}})


### Media Keys ###
Support for media keys (F7, F8, F9) on Apple keyboards has been added.

| Key              | Function         |
|:-----------------|:-----------------|
| PlayPause (F8)   | Plays/Pauses     |
| Rewind(F7)       | Skip to Previous |
| Fast forward(F9) | Skip to Next     |

Next Episode
------------
Added a menu item (Play Next Episode) that plays the next episode based on the currently playing file. This is bound to  ⌘E

Help
----
I am (re)wrote most of the help.

Icons
-----
I made all the filetype icons for the project (34 in total), below are a sample the rest can seen [here](https://github.com/Bilalh/MPlayer-OSX-Extended/tree/build/extras/File%20Type%20Icons "Complete set of icons").

### Video Icons ###
![Video Icons]({{< path "media/code/MPlayer-OSX-Extended/Video.png" >}})

### Audio Icons ###
![Audio Icons]({{< path "media/code/MPlayer-OSX-Extended/Audio.png" >}})

### Subtitles Icons ###
![Subtitles Icons]({{< path "media/code/MPlayer-OSX-Extended/Subtitles.png" >}})

### Binary Icon ###
![Binary Icon]({{< path "media/code/MPlayer-OSX-Extended/Binary.png" >}})
