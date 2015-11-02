---
author: Bilal Syed Hussain
description: Control iTunes from the command line.
info: Control iTunes from the command line; over 30 commands including play/pause, mute/unmute, playlist and play random album.
draft: false
github: Bilalh/Shell-Tunes
title: ShellTunes
type: code
num: 20
languages:
    - Shell
aliases:
    - /projects/shell-tunes
---

Control iTunes from the command line, over **30** commands including play/pause, mute/unmute, playlist and play random album. Also includes scripts for getting data from Ttunes.

Usage
-----
Usage: `itunes.sh <option>`


Install
-------
* Put the scripts in your `$PATH`
* See below for bash completion.

Options
-------

	Usage: itunes.sh <option>
	Options: (short)
	 (s) status          : Shows iTunes' status, and track info
	 (y) play            : Start playing.
	 (a) pause           : Pause iTunes.
	 (p) playpause       : Start playing / Pauses.

	 (n) next            : Go to the next track.
	 (b) prev            : Go to the previous track.
	 (r) rewind          : Rewinds the current track.

	 (m)                 : Toggles Mute iTunes' volume.
	     mute            : Mute iTunes' volume.
	     unmute          : Unmute iTunes' volume.
	 (v) vol up          : Increase iTunes' volume by 10%
	 (v) vol down        : Increase iTunes' volume by 10%
	 (v) vol #           : Set iTunes' volume to # [0-100]

	 (@) search        {string} : Search for songs in each field (results playlist must exist)
	 (@) search [type] {string} : Search for songs by type
	                            : Types are album, artist, composer
	                            : comment, genre, grouping, name and year
	 ($)               {string} : Searching for songs using name, album and comment as fields

	 (l) playlist        : List all the playlists
	 (l) playlist {name} : Plays the specified playlist
	 (c) current         : List the songs of the current playlist

	 (d) random          : Plays a random album
	 (f) shuffle         : Toggles shuffle
	 (f) shuffle on      : Turns shuffle on
	 (f) shuffle off     : Turns shuffle off

	 (e) repeat all      : Set repeat to all
	 (e) repeat one      : Set repeat to on
	 (e) repeat off      : Set repeat to off


	 [0-5]              : Set the current song rating
	 (6) 4.5            : Set the current song rating to 4½ stars

	 (t) stop           : Stop iTunes.
	 (q) quit           : Quit iTunes.


Bash Completion
--------------
* Add this to your `.bash_profile` or `.bashrc`

```bash
function i(){
	itunes.sh "$@"
}

function _ilist(){
	itunes.sh commands
}

function _icomp(){
	local curw
	COMPREPLY=()
	curw=${COMP_WORDS[COMP_CWORD]}
	COMPREPLY=($(compgen -W '`_ilist`' -- $curw))
	return 0
}

#  Completion for itunes.sh
shopt -s progcomp
complete -F _icomp i
```
