---
layout: post
title: "FarCry 7.0: Shiny progress with 'Seedy Nelly'"
date:   2013-08-13
author: "geoff-bowers"
tags: release
---

Work on "Shiny" (FarCry 7.0) has been progressing well, however, we're a bit behind schedule. The alpha release for Shiny is available; it's stable enough for development but missing a couple of major features. You can track progress via commits (https://github.com/farcrycore/core/commits/trunk).  

We got sidetracked by a client, and the development of an awesome CDN feature.  You can now deploy all images and file assets directly to the CDN of your choice. FarCry supports FTP, S3 and local file storage by default, and can build plugins for other CDN APIs (we have commercial support for Limelight already).

<!--more-->

CDN support (codename: "Seedy Nelly") was originally earmarked for 7.1 but has now been [released as FarCry 6.3](https://github.com/farcrycore/core/tree/p630) Seedy Nelly has already been rolled into the "Shiny" alpha build.

**So what's on the horizon for FarCry 7.0?**

- a complete overhaul of the webtop UI; its completely rebuilt, redesigned, and "pluggable" (you can build plugins to replace the webtop design completely)
- new site overview tree; high performance backbone.js and the UI greatly simplified 
- multi-file upload support; through the browser, FTP, Dropbox or any other way of getting files into a folder on the server
- an incredible asynchronous queue -- `Core` can manage a whole series of asynchronous threads for processing images, statistics, or anything else you need to "offline" for users
- archive, restore, undelete and undo 
- upgraded form tool library; including tinyMCE 4.x and themes for widgets

At this stage all the heavy lifting is done.  We just need a window to clean up all the UI changes, remaster the webtop menus, and squash bugs.  This is finicky work -- may be a few more weeks before the beta is good to go.

If you've been considering a Commercial License (starting at $5,000USD) this is the time -- every purchase really makes a huge difference, and gives [the Daemonite team](http://www.daemon.com.au/) time to focus on perfecting the next release.
