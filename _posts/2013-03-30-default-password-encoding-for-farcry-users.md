---
layout: post
title:  "Default Password Encoding for FarCry Users"
date:   2013-03-30
author: "geoff-bowers"
tags: security
---

In FarCry Core 6.2 we have switched to hashing user passwords by default.  This means the plain text paswords you may have seen in your usertable are now encrypted; prefixed with something like ```$2a$10$```.

<!--more-->

The prefix indicates which hashing algorithm was used. There are a few choices available in the webtop *Security Config*. FarCry uses that prefix to determine whether a user's password is still in plaintext and needs to be updated. That check is automatic when a user logs in, but you can kick of a full database update using the handy script provided.

We changed the default password encoding in 6.2 because storing passwords in plain text creates an opportunity for unauthorised hackers to get the passwords of every user on the system. The frequency of incidents of hackers stealing stored passwords of online systems have been increasing over the years. Storing passwords as secure hashes means that even if hackers steal the hashes it will take time for them to discover the original passwords; this time can be used to reset everyone's passwords so that the stolen hashes become (mostly) useless.

It's possible that password theft by hackers is not a major concern for your system, but we wanted to provide a secure default for 6.2. If you want to return to the old behaviour, go to the *Security Config* under the webtop and change the Password hashing algorithm to 'No hashing'. The stored passwords will then revert back to plain passwords as each user logs in successfully, or as their passwords are reset. 

Secure password hashes are not easily reversible, so no password downgrade tool is available.

We performed extensive testing of the password hashing code to make sure changing the algorithm wouldn't lock users out of the system. The login code detects the storage format of the user's password and uses it to do the password check. This is why the stored passwords are only upgraded automatically on successful logins and resets: it's the only time the system knows for sure what the user's actual password is.

Our best advice for users who keep forgetting their passwords is to tell them to write their passwords down. This idea may sound crazy, but is in fact [recommended by a number of security experts](http://news.cnet.com/Microsoft-security-guru-Jot-down-your-passwords/2100-7355_3-5716590.html) It's important though that written passwords be unique for the system and not reused across multiple systems.

Enjoy!