---
layout: post
title:  "Minecraft Missing Title Screen"
date:   2020-12-12 00:00:00 +0000
categories: 
---

Recently when I started Minecraft (Windows 10 edition), something was wrong with the title screen. The background was there, slowly rotating as before. The music was playing. But the usual buttons were missing (Play, Settings, Marketplace, Sign In, and Profile). The Minecraft title was missing. And the avatar was missing.

After searching the web, I came across this [Mojang Bug Report](https://bugs.mojang.com/browse/MCPE-109870). It appeared to be related to a recent Windows update, especially affecting users with AMD GPUs. Many people were reporting similar issues which started earlier this week. The solution worked for me:

1. Make sure you have the latest version of "AMD Radeon Settings" app. You can download it 1. [here](https://www.amd.com/en/support).
1. Open the "AMD Radeon Settings" app
1. Go to the "Gaming" section
1. Select Minecraft
1. Change the graphic profile to "Gaming"
1. Launch the game 

If this doesn’t work for you, try a few other suggestions on the [bug report page](https://bugs.mojang.com/browse/MCPE-109870).