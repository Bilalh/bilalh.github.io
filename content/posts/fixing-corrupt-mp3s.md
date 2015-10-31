---
author: Bilal Syed Hussain
date: 2011-12-24T16:33:17Z
modified: 2015-10-31T15-21-28Z
description: How to fix corrupt mp3 using mp3val on Mac or Linux
draft: false
tags:
- Audio
title: fixing corrupt mp3s
topics:
- guide
- tools
type: post
---

To fix a corrupt mp3 [mp3val](http://mp3val.sourceforge.net/) can be used.  The website provides binaries for Windows, and sources for other platforms including Linux and Mac OS X.

Installation
------------

**Update**: binaries for Mac OS X (tested on 10.6) [here]({{< path "files/mp3val" >}})

To install on a Mac either install it the easy way:

	brew install mp3val

or download the sources and then `cd` to the directory of sources and then do

	make -f Makefile.gcc

and then place the binaries in you `$PATH` e.g. `/usr/local/bin`


Usage
-----

To fix the corrupt mp3s use the following

	mp3val -f

which tells `mp3val` to fix the errors in the mp3s.  Shell wildcards can be used e.g.

	mp3val -f *.mp3

which will fix all mp3 in the current directory.

`mp3val` also keeps all the old tags as well, which is useful.
