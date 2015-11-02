---
author: Bilal Syed Hussain
date: 2015-10-31T16:46:31Z
modified: 2015-11-02T00:17:41Z
description: Pretty printing a .csv file to get nicely aligned output on the command line.
draft: false
tags:
- shell
- text processing
title: Viewing .csv files on the command line
topics:
- scripting
type: post
---

It can be convenient to view a `.csv` file from the command line, when using SSH connection for example.  A basic version with no dependencies is as follows:

```bash
function see_csv(){
    column -s, -t <"$1" | less --shift 2  -SN
}
```

with example output:

```
1 seq    run_no  kind        iterations  timeout
2 12001  1       undirected  64          600
3 12002  1       nsample     64          600
```

To handle blank fields we can use `sed` to add extra spaces for use with `column`:

```bash
function see_csv(){
    cat "$1" | sed 's/,,/, ,/g;s/,,/, ,/g' | column -s, -t | less --shift 2 -SN
}
```

If the `.csv` has many columns, you change the `less` options to the following:

```bash
function see_csv(){
    cat "$1" | sed 's/,,/, ,/g;s/,,/, ,/g' | column -s, -t | less -SN -Xs
}
```
So that the columns that can fit on the screen are printed, for convenience.   

```
❯ see_csv experiment.csv
      1 seq    run_no  kind        iterations param timeout  
      2 16001  1       undirected  64               38400            
      3 16002  1       nsample     64               38400            
      4 16003  1       undirected  64               38400            

~/Desktop/Results/
❯

~/Desktop/Results/
❯
```

To access any addition columns use the arrow keys, this will cause the screen to be redrawn.
