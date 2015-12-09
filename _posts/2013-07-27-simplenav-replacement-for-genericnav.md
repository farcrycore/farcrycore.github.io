---
layout: post
title: "simpleNav replacement for genericNav"
date:   2013-07-27
author: "geoff-bowers"
categories: development
---

We've been encountering a few issues with single threading of "Query of Queries" on the Railo engine affecting performance on high traffic sites. This lead [Daemonite Justin](https://github.com/justincarter) (@justincarter) to refactor the common `<skin:genericNav>` tag as it uses a few QofQ.

<!--more-->

We've added the new `<skin:simpleNav>` to core (in branch p630+). It differs from `<skin:genericNav>` in a few ways:
 
- No query of queries
- No permission checks
- No "aLink" display style (this probably should have been a separate tag anyway...)
- All HTML tag names that are outputted are configurable
- You can actually [read the code](https://github.com/farcrycore/core/blob/p630/tags/webskin/simpleNav.cfm), and its less than half the number of lines!
 
At this time it's not intended as a full blown `<skin:genericNav>` replacement - but it could be if we add back permission checks since the attributes are largely the same. Either that or we could plan on using it going forward and just deprecate `<skin:genericNav>`.
 
We're using `<skin:simpleNav>` in a number of production sites, and the CPU usage has been noticeably lower.