---
author: Bilal Syed Hussain
date: 2011-10-15T22:37:32Z
modified: 2015-11-02T00:02:13Z
description: bash prompt including git status and metadata
draft: true
tags:
- git
title: git bash prompt and aliases
topics:
- tools
type: post
---


You can get git to shown information such as which branch you are on by using the following:

```bash
export PS1='\u$(__git_ps1 "@%s") \$ '
```

This would be as displayed as `User@master $ `.  You can also get git to shown even more metadata by using the following.

```bash
export GIT_PS1_SHOWDIRTYSTATE=true
export GIT_PS1_SHOWUNTRACKEDFILES=true
export GIT_PS1_SHOWSTASHSTATE=true
```

* `GIT_PS1_SHOWDIRTYSTATE` adds a `*` at the end if the branch has been changed e.g `User@master * $ `
* `GIT_PS1_SHOWUNTRACKEDFILES` adds a `%` at end if the branch has untracked files e.g `User@master % $ `
* `GIT_PS1_SHOWSTASHSTATE` shows a `$` if the stash contains anything.
* `+` at the end means that there are changed to be committed.

For a full colour prompt use

```bash
export PS1='\[$(tput setaf 3)\]\u\[$(tput sgr0)$(tput setaf 5)\]\[$(tput sgr0)$(tput setaf 2)\]$(__git_ps1 " [%s]") \[$(tput sgr0)\]$ '
```

which shows `bilalh [mediakeys] $` but in colour

This has been tested with `git version 1.7.3.4` but should work with 1.6.5+ and requires git `bash_completion`, see [git bash completion](https://github.com/markgandolfo/git-bash-completion "git bash_completion") if you don't have it.
