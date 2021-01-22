---
title: "Dosbox and Touhou"
date: 2021-01-22T04:20:59-06:00
tags:
- dosbox
- touhou
categories:
- retro
- emulation
draft: false
---
I bet most of you don't know that the default install of Dosbox is way out of date. There are plenty more custom builds that use the latest Dosbox code. While I'm a fan of RetroArch, my favorite SVN build so happens to be Dosbox-X. This build contains one unique feature that I deem that I need... and that's NEC PC-98 Emulation.

The PC-98 was the line of personal computers made by NEC in the 80s to 90s. This machine itself was the home of many a doujin game - both clean and sexy. The most popular of which happens to be the first five Touhou games. Unfortunately, these games aren't quite available in the US. However, if you can get your hands on the images, the following instructions can help set up a DOSBox you can play both DOS and PC-98 titles on.

## Get Dosbox-X

It's an Open Source project. You can find it by clicking [here](https://github.com/joncampbell123/dosbox-x/releases). You're going to want to get both the installer and the zipped version for Windows.

## Extract and Install DOSBox-X
Exactly as it says on the tin. In the installed directory, you're going to find a file named "FREECG98.BMP". This file contains the glyphs used in PC-98 mode and are hand crafted by the developer, as the official set is not legal to distribute online. Move this file into your unzipped version of DOSBox.

## Prepare your Disk Images
Unzip them into a folder or something.

## Copy and edit the dosbox.conf file
Put the file with your disk images. There are some lines you will need to edit. The first is what I believe to be line 119. This line should be set to pc98. At the bottom, feel free to set the disk image mounting here, like so.

```
[autoexec]
imgmount c "P:\ath\to\th01.hdi"
boot -l c:
```

## Mash go
In a command prompt, change to your Dosbox unzipped directory and run the following:
`dosbox-x.exe -conf P:\ath\to\th01.conf`

It'll load up and begin running the game, complete with a full set of glyphs. You can uninstall the installed version by now.
