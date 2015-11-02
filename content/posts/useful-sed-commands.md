---
author: Bilal Syed Hussain
date: 2011-10-09T17:20:59Z
modified: 2015-11-01T01:17:04Z
description: Useful sed commands for text processing
draft: false
tags:
- shell
title: Useful sed commands
topics:
- Scripting
type: post
aliases:
 - /2011/10/09/using-sed/
---


### Delete nth line inplace ###
```
sed -i .tmp '<n>d' <filename>
```

### Get the nth line ###
```
sed '<n>q;d' <filename>
```    

### Delete the first 10 lines of a file ###
```
sed '1,10d'
```

### Delete lines matching pattern ###
```
 sed '/pattern/d'
```
