---
author: Bilal Syed Hussain
date: 2011-09-09T20:36:06Z
description: description
draft: false
tags:
- git
title: Git Delete Last Commit
topics:
- tools
type: post
---


If you have committed files that you shouldn't have (e.g passwords, keys) you can use the following to delete the last commit provided the commit has not been pushed.

```bash
git reset --hard HEAD~1
```

`HEAD~1` means the pervious commit, you can also use the SHA-1 of a commit to **delete** all commits back to that commit.  

>   Note that `--hard` gets rid of **any** changes from the selected commit(s). Use `--soft` to leave the files as `changes to be committed`.

If you have pushed the commit then you can either do

```
git revert HEAD
```

which creates a **new** commit that getrid of the changes in the last commit but the data is still present in the history of the repository.

Even if you tried to do `git push --force` after you deleted the commit from your copy the data will exist in people locals copies until they pull the latest changes. This Also makes merging a lot more diffcuent
