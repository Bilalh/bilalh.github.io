---
author: Bilal Syed Hussain
date: 2011-10-15T22:37:32Z
modified: 2015-10-28T19:12Z
description: Shellmarks is a shell script that allows you to save and jump to commonly used directories
draft: true
tags:
- shell
title: Shellmarks - terminal directory bookmarks
topics:
- scripting
type: post
---


[Bashmarks](/projects/bashmarks "Bashmarks project page") is a shell script that allows you to save and jump to commonly used directories.

Usage Example
-------------

```shell
$ cd ~/home/projects/www/
$ s web
$ cd /usr/local/lib/
$ s locallib
$ l
web          /var/www/
locallib     /usr/local/lib/
$ g w<tab>
$ g web           # cd to ~/home/projects/www/
$ g l<tab>
$ g locallib      # cd to /usr/local/lib/

```


Extra Features
--------------
* if no bookmark name is specified the default directory is used instead  ($HOME unless changed)

```shell
cd ~/projects
s
g              # g now defaults to ~/projects
```


* Commands can be placed after the bookmark  
```shell
$ g web ls     # cd to ~/home/projects/www/ then executes ls
~/var/www/
index.html
site.css
$
```

* cd like features

```shell
g -   # does cd -
g ..  # does cd ..
g /   # does cd /
```


### Mac Specific Features ###
* `o` command which opens the specified bookmark in Finder
* `t` command which opens the specified bookmark in a new Terminal tab.

```shell
t web          # opens ~/home/projects/www/  in a new tab
cd javascript
t              # opens ~/home/projects/www/javascript in a new tab

o              # opens ~/home/projects/www/javascript in Finder
```


Install
-------
1. git clone git://github.com/Bilalh/bashmarks.git
2. make install
3. `source ~/.local/bin/bashmarks.sh` from within your `~.bash_profile` or `~/.bashrc`

OR

download [https://github.com/Bilalh/bashmarks/blob/master/bashmarks.sh](https://github.com/Bilalh/bashmarks/blob/master/bashmarks.sh) and source it from within your `~.bash_profile` or `~/.bashrc`


More Information
---------------
See the [Project Page](/projects/bashmarks "Bashmarks project page") for information.  
[GitHub Repository](https://github.com/Bilalh/bashmarks "Bashmarks GitHub Repository")
