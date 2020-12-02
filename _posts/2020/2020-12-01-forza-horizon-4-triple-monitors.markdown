---
layout: post
title:  "Forza Horizon 4 Triple Monitors"
date:   2020-12-01 00:00:00 +0000
categories: 
---

I bought Forza Horizon 4 on sale for $16.99 from NewEgg and the Ultimate Add-Ons Bundle for $19.99 from Microsoft store.  I set up the game up to play on my PC.  Since I have three monitors, I wanted to try playing the game on all three.  Fortunately [somebody else has already found a way](https://www.reddit.com/r/forza/comments/bwm6kb/tutorial_how_to_run_fh4_on_triple_monitors/).

## 1 Figure out the resolution of your monitors combined
If your monitors do not have the same resolutions, I recommend setting the height to the smallest vertical resolution, and setting the width to the sum of your horizontal resolutions.  

For example, my main, center monitor was 2560x1440.  My side monitors were both 1920x1200.  So the resolution that I would use was `height=1200`, `width=6400`, if I wanted to use my "full" resolution.  However my current GPU (GTX 760) was not powerful enough to run the game at that resolution.  I opted to try it at 720p.  Multiply both height and width by 0.6 and we get `height=720`, `width=3840`.

## 2 Find the game's config file
By default, the game config file should be here.  Note the file has no extension.
```
C:\Users\[YourUsername]\AppData\Local\Packages\Microsoft.SunriseBaseGame_8wekyb3d8bbwe\TempState\scratch\User_PCLocalStorageDirectory\ConnectedStorage\ForzaUserConfigSelections\UserConfigSelections
```

## 3 Edit the config file
You can open the file using any text editor software (e.g. Notepad).  Set the values for `ResolutionHeight` and `ResolutionWidth` to the numbers we calculated in step 1.  Set the value for `Fullscreen` to 0.  Then save the file.

Example:
```
<ResolutionWidth value="3840"/>
<ResolutionHeight value="720"/>
<Fullscreen value="0"/>
```

## 4 Launch the game
The game should launch in windowed mode.  Note that it might be maximized.  You will have to manually resize the window to stretch across all three monitors.  Hide the Windows Taskbar if you want to.


## 5 Edit HUD
When you first play with really wide resolution, the HUD will be on the far ends of the monitors.  You can adjust their location as needed.
- Go to game's  "Setting"
- "HUD and GamePlay"
- Scroll down and adjust "HUD Safe Frame Horizontal" to your liking.

## 6 Adjust Video Settings
Now that you are playing at a much higher resolution, if your computer is not powerful enough, you might need to lower some of the video settings to get a good framerate.

There are some nuances when setting the game up this way.  You can read up on these from the [original post](https://www.reddit.com/r/forza/comments/bwm6kb/tutorial_how_to_run_fh4_on_triple_monitors/) by u/Chew-Magna.