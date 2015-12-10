---
layout: post
title: "FarCry Repos Now On Github"
date:   2013-07-11
author: "geoff-bowers"
tags: documentation
---

We're moving FarCry version control repos to Github from SVN. While all plugins and related code bases have been moved, the `core` is still in a state of transition; we're still committing to SVN and syncing changes into Github.

<!--more-->

Daemonite Dennis (@boomerangfish) has been running `git-svn scripts` to sync FarCry Core commits from SVN to GitHub. The sync process is scheduled to run every 15 minutes, all day every day. You no longer need worry about waiting long for core updates on SVN to show up on:

- <http://github.com/farcrycore>

If you've been using SVN checkouts of `core` for your FarCry sites, now is a good time to think about replacing it with a Git clone. The simplest and safest way is to shut down your FarCry site, delete/rename the old core, git clone the new core, checkout the right tag/branch and restart the site.

You can find the FarCry Core Framework GitHub project at:

- <https://github.com/farcrycore/core>

The [Daemonites](http://www.daemon.com.au/) have been sharpening their Git skills lately on various other projects, and soon the core committers will be ready to work directly against Git. We haven't set a date for ending updates to SVN, but it will be before October 15 as that's when Atlassian will be shutting down their SVN service.

So its Github all the way, we just can't accept pull requests on `core` for a little while yet.

**UPDATE: Send your PULL REQUESTS!  We're GitHub all the way.**

