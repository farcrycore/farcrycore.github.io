---
layout: post
title: "Friendly URLs on NGINX"
date:   2013-07-16
author: "geoff-bowers"
tags: development
---

[NGINX](http://nginx.org/) is fast becoming a popular web server for web apps. Daemonite Jason had a bit of a tinker getting FarCry Friendly URLs to work with the NGINX re-write module.

``` bash
# farcry test
# http://wiki.nginx.org/HttpCoreModule#try_files
server {
    listen       80;
    server_name  sowsew.local alias  www.sowsew.com;

    location / {
       root   C:\Users\Jason\workspace\sowsew\projects\sowsew\www;
       index  index.cfm index.html index.htm;

       proxy_pass          http://127.0.0.1:8888/;
       proxy_redirect      off;
       proxy_set_header    Host            $host;
       proxy_set_header    X-Real-IP       $remote_addr;
       proxy_set_header    X-Forwarded_For $proxy_add_x_forwarded_for;

       try_files $uri $uri/ @farcry;
    }
    location @farcry {
       rewrite ^/(.*)$  /index.cfm?furl=$1 last;
    }
    }
```

Enjoy!