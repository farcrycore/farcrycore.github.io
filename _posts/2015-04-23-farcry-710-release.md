---
layout: post
title: "FarCry Core 7.1 Release"
date:   2015-04-23
author: "geoff-bowers"
categories: release
---

The [FarCry Core 7.1 release](https://github.com/farcrycore/core/releases/tag/7.1.0) adds some cloud friendly improvements, particularly focussing on access to the application scope and some object broker refactoring. There are also many bug fixes and webtop performance tweaks that have been patched recently in 7.0.x maintenance releases.

Overall its a big "under the hood" update with little or no breaking changes.

<!--more-->

To update:

- stop the app
- replace `core` with the latest
- restart the application
- login to the webtop and deplpoy all COAPI changes
- rejoice!

https://github.com/farcrycore/core/releases/tag/7.1.0

### New Feature

```
[FC-2912] Track objects and types used to generate a page
[FC-2947] Reverse UUID formtool needs a hidden field to allow change event binding
[FC-2949] Detect database type from DSN during application startup
[FC-2950] Allow the Installer to detect DB type to assist with scripted deployments
[FC-2956] Richtext snippet support for TinyMCE FarCry Content Templates plugin
[FC-2958] Allow the boolean formtool to show labels inline next to the checkbox
[FC-2963] added attributes inline and r_html to cssInHead and jsInHead
```

### Improvement

```
[FC-2907] Move application scope caches into object broker
[FC-2910] Add CGI scope to dump utility
[FC-2913] JSON formatting of error "detail"
[FC-2919] Redirect after logout to remove 'logout=1' from url
[FC-2920] Add status argument to fapi.stream function
[FC-2935] Webtop header performance improvements
[FC-2936] Make farWorkflow configurable on content types, default to false
[FC-2937] Allow the tray to be turned on in the webtop
[FC-2938] Allow the webtop component to be extended in plugins/projects
[FC-2939] Allow the webtop header logo area to be overridden using a webskin
[FC-2940] Use the webtopHeaderLogo webskins on the webtop login page
[FC-2960] The sortableColumns attribute isn't being applied to custom columns
```

### Bug

```
[FC-2045] genericNav.cfm and displayStyle="aLink"
[FC-2923] dmProfile records should not be "archived" on login
[FC-2924] syntax error in assignCategories.cfm missing )
[FC-2925] fix caching issue in webtop edit profile form
[FC-2926] Railo S3 path issue with special characters
[FC-2929] Fix potential reflected XSS in tray webskins
[FC-2930] objectadmin advanced "clear filter" should also reset pagination
[FC-2931] objectadmin quick filter pagination loses search term
[FC-2932] Webtop navigation permissions not combining properly for users with multiple roles
[FC-2933] Role Content Type Security alert() on every click
[FC-2941] Property refresh for reverse UUID formtool in wizards returns a 404
[FC-2942] Clicking "Add" and then "Cancel" on reverse UUID formtool leaves blank records in DB
[FC-2943] Moving Rules in Containers errors on second attempt
[FC-2944] objectadmin quick search using a custom recordset throws an error
[FC-2945] Error during save/publish: "can't delete file" in s3.cfc removeCachedFile()
[FC-2946] UUID formtool throws JS error on clicking remove
[FC-2948] System Info webtop page throws [outputError] is undefined
[FC-2951] COAPI Overview shows some types extended from abstract types in the wrong location
[FC-2952] Using ftWatch on join.cfc formtools throws "argument stPackage required" error
[FC-2953] Invalid content types in URL should throw a 404 instead of 500
[FC-2954] Respect bSave="false" on array properties
[FC-2955] Country formtool dropdown "selected" state
[FC-2957] Formtools ftShowLabel attribute not working for wizards
[FC-2959] diff.cfc crashes when comparing an array in previous versions of an object where a typename has been removed
[FC-2961] ftClass not on all radio and checkbox formtool list inputs
[FC-2962] form.action attribute context sensitive default
[FC-2965] incorrect precision of cf_sql_float
[FC-2966] Bot detection by user agent is broken
[FC-2967] Add bingbot to list of default bot user agent strings
[FC-2968] Bot IP detection should check an array not a list
[FC-2969] Wrong URL path gets generated for S3 images when images are inserted via richtext formtool
[FC-2970] Richtext formtool ftLinkListFilterRelatedTypenames attribute should be ftLinkListFilterTypenames
[FC-2971] Remove id attribute on checkbox/radio elements in list formtool
[FC-2972] Set HTTP header charset parameter to UTF-8 for redirects
[FC-2973] Use property attribute instead of name on "inhead" meta elements
[FC-2974] File not found error when using "livecombine" CSS refresh
```
