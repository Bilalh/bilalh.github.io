---
author: Bilal Syed Hussain
date: 2012-04-22T22:01:23Z
modified: 2015-11-01T01:16:22Z
description: Pipe output from a command line tool to a text editor on OS X
draft: false
tags:
- osx
title: Pipe output from command line tools to a text editor
topics:
- scripting
type: post
---

A useful feature is to pipe the result of a command such as `ls` to a text editor. This can be done by using:

```
	ls | open -f
```


Using the `-a` flag for `open`  makes this even more useful allowing you to specify the application to open the output in e.g to open in TextMate use:

```
	ls | open -f -a Textmate
```
