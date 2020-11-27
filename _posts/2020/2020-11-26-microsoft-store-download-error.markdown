---
layout: post
title:  "Microsoft Store Download Error 0x80070001"
date:   2020-11-26 00:00:00 +0000
categories: 
---

On a Windows 10 computer, when I tried downloading an app from Microsoft Store to a non-C:\ drive, I received an error with the code `0x80070001`.  The following steps resolved the issue for me:

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