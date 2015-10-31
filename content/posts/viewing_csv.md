---
author: Bilal Syed Hussain
date: 2015-10-27T18:59:52Z
description: description
draft: true
tags:
- shell
- text processing
title: Viewing .csv files on the command file
topics:
- tools
type: post
---

It can be convenient to view a `.csv` file from the command line, when using SSH connection for example.  A basic version with no dependencies is as  follows:

```bash
function see_csv(){
    column -s, -t <"$1" | less --shift 2  -S -N
}
```

with example output

```
1 seq    run_no  kind        iterations  timeout
2 12001  1       undirected  64          600
3 12002  1       nsample     64          600
```

To enhance the
