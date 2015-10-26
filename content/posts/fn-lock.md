---
author: Bilal Syed Hussain
date: 2011-08-29T00:30:16Z
description: description
draft: false
keywords:
- Applescript
- OSX
tags:
 - Applescript
 - Utilities
 - Scripting
title: fn lock
topics:
- topic 1
type: post
---

The below script toggles the function keys on a mac's keyboards, between the media keys and the standard functions keys.

The script is most useful in either the script menu, which is done by placing the script in the `/Library/Scripts/` or using by setting a keyboard shortcut using  Alfred/Quicksilver.


```applescript
tell application "System Preferences"
	set current pane to pane "com.apple.preference.keyboard"
end tell


tell application "System Events"
	if UI elements enabled then
		tell application process "System Preferences"
			get properties
			click radio button "Keyboard" of tab group 1 of window "Keyboard"
			click checkbox "Use all F1, F2, etc. keys as standard function keys" ¬
				of tab group 1 of window "Keyboard"

		end tell

	else
		tell application "System Preferences"
			activate
			set current pane ¬
				to pane "com.apple.preference.universalaccess"
			display dialog ¬
				"UI element scripting is not enabled. Check \"Enable access for assistive devices\""
		end tell
	end if
end tell

tell application "System Preferences"
	quit
end tell
```

