---
layout: post
title: "FarCry COAPI Helicopter View"
date:   2015-12-11
author: "geoff-bowers"
tags: development
---

![COAPI MVC](/images/coapi-mvc-diagram.png)

The FarCry framework is based on a variation of the classic Model-View-Controller pattern. The COAPI (or Content Object API) is a high level name for the MVC engine inside FarCry. Without getting bogged down in the details of the framework, its good to have a high level or "helicopter" view of how things work under the hood. We expand on these themes gradually as you go through the [FarCry developer course][1].

<!--more-->

> ok, so the developer course is getting a bit long in the tooth. might be something to tackle in the christmas break. @modius 

Requests from users are processed by FarCry's built-in "smart controller" which automatically determines wiring based on the URL convention or the friendly URL sub-system. The COAPI always ends up calling a principal content type (a special type of class) that manages how we interact with the model and view. When thinking of views (or webskins) its important to realise that they are always executed in the context of a specific content type.

It's not at all important for developers to understand how the COAPI works, but hey, for those that want the details we're adding some advanced info boxes to the course where relevant. If you have more specific questions let me know -- always looking at ways to make the developer documentation clearer.

_h/t plumbing the archives for this post from late 2011_

[1]:    https://farcry.jira.com/wiki/display/FCDEV60/Book+of+FarCry