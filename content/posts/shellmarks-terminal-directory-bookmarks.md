---
author: Bilal Syed Hussain
date: 2012-01-14T00:57:33Z
modified: 2015-11-01T21:50:39Z
description: Shellmarks is a shell script that allows you to save and jump to commonly used directories
draft: false
tags:
- shell
title: Shellmarks - terminal directory bookmarks
topics:
- scripting
type: post
aliases:
  - /2012/01/14/enchanted-bashmarks-terminal-directory-bookmarks/
---


[shellmarks]( {{< path "shellmarks" >}} "shellmarks project page") is a shell script that allows you to save and jump to commonly used directories.

Usage Example
-------------

```
$ cd /var/www/
$ s web
$ cd /usr/local/bin/
$ s localbin
$ l
    web          /var/www/
    localbin     /usr/local/bin/
$ g web<tab>
$ g web          # cd to /var/www/
$ o web     	 # Open in Finder if on a mac
```


Extra Features
--------------
* if no bookmark name is specified the default directory is used instead  ($HOME unless changed)

```
cd ~/projects
s
g              # g now defaults to ~/projects
```


* Commands can be placed after the bookmark  
```
$ g web ls     # cd to ~/home/projects/www/ then executes ls
~/var/www/
index.html
site.css
$
```

* cd like features

```
g -   # does cd -
g ..  # does cd ..
g /   # does cd /
```


### Mac Specific Features ###
* `o` command which opens the specified bookmark in Finder
* `t` command which opens the specified bookmark in a new Terminal tab.

```
y web          # opens ~/home/projects/www/  in a new tab
cd javascript
y              # opens ~/home/projects/www/javascript in a new tab

o              # opens ~/home/projects/www/javascript in Finder
```


Install
-------
1. git clone git://github.com/Bilalh/shellmarks.git
2. make install
3. `source ~/.local/bin/shellmarks.sh` from within your `~.bash_profile` or `~/.bashrc`

OR

download [https://raw.githubusercontent.com/Bilalh/shellmarks/master/shellmarks.sh](https://raw.githubusercontent.com/Bilalh/shellmarks/master/shellmarks.sh) and source it from within your `~.bash_profile` or `~/.bashrc`


More Information
---------------
See the [project page]( {{< path "shellmarks" >}} "shellmarks project page")  for information.  
