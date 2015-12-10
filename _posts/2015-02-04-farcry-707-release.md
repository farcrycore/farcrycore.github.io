---
layout: post
title: "FarCry 7.0 Maintenance Releases"
date:   2015-02-04
author: "geoff-bowers"
tags: release
---

We've been quiet on the blog front but maintenance on the `p700` branch continues apace.

<!--more-->

https://github.com/farcrycore/core/releases

Couple of recent fixes have patched a number of longstanding bugbears:

## iPad support
A strange iFrame scrolling behaviour was blocking any sort of meaningful use of the webtop using an iPad.  Clever little CSS trick and the webtop is "fire all boosters" for iPad.

## Object Admin Improvements; ie webtop grids
"clear filter" now resets pagination under the advanced filter options and the quick filter now behaves properly with pagination.

## Login Performance
Turns out we've been archiving `dmProfile` records on login.  Arggh.  Turns out this is a slow process ;) Archive is a standard process for the framework on object change for content items, but its not needed when the `lastloggedin` field changes.

Note that we still have a high work factor for `bcrypt` password encryption that could have an impact on high volume login scenarios.

## 7.0.7 Release

```
[FC-2932] - Webtop navigation permissions not combining properly for users with multiple roles
[FC-2933] - Role Content Type Security alert() on every click
```

## 7.0.6 Release

```
[FC-2916] - add support for publicfiles/privatefiles locations in bulk upload
[FC-2917] - wrong struct key used in s3.cfc
[FC-2918] - when restireve file from s3, special character in path got normalized
[FC-2921] - file.cfc onSecuirityChange refers to wrong location variable
[FC-2922] - iframe scrolling support for iPad
[FC-2923] - dmProfile records should not be "archived" on login
[FC-2925] - fix caching issue in webtop edit profile form
[FC-2926] - Railo S3 path issue with special characters
[FC-2929] - Fix potential reflected XSS in tray webskins
[FC-2930] - objectadmin advanced "clear filter" should also reset pagination
[FC-2931] - objectadmin quick filter pagination loses search term
```

**Remember the general policy for maintenance releases is that you should be able to update and restart the application -- no schema changes or code breaking updates.**

Update now!