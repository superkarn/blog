---
layout: post
title:  "Microsoft Store Download Error 0x80070001"
date:   2020-11-26 00:00:00 +0000
categories: 
---

On a Windows 10 computer, when I tried downloading an app from Microsoft Store to a non-C:\ drive, I received an error with the code `0x80070001`.  After searching, I found this [post](https://gamefaqs.gamespot.com/boards/916373-pc/74384545) with the solution that worked for me.

1. Cancel the download
1. Redownload to C:\ drive
1. After the app has completed installation, move it to another drive
    1. Open "Windows Settings"
    1. Click "Apps"
    1. Find your app and click it
    1. Click "Move"
    1. Select the location
    1. Click "Move"
1. Once this is complete, you should be good to go

**Edited on 2020-12-13**  
I received the same error again when apps were trying to update. After more searching, I found this [post](https://www.reddit.com/r/XboxGamePassPC/comments/j3edas/error_code_0x80070141/g7nhkkf/) (which points to another [post](https://www.reddit.com/r/XboxGamePassPC/comments/io1ur4/heres_how_to_troubleshoot_if_you_have_problems/)) about editing the Registry. (Make sure to back up anything you plan on changing.) The gist is

 1. Open regedit
 1. Go to `Computer\HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Appx\PackageVolumes\`
 1. Look for the subkey that contains the drive your app was installed on
 1. Delete the subkey
 1. Reboot (optional?)