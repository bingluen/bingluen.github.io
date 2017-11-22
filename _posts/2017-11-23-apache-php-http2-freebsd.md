---
layout: post
title:  "Apache 2.4 + PHP 7 Support HTTP/2 on FreeBSD"
date:   2017-11-23
excerpt: "NCTU-SA106"
post: true
tag:
- Apache
- php
- HTTP2
- FreeBSD
comments: true
---

## 結論

先說結論，Apache 對於 HTTP/2 支援有非常嚴重的地雷。

## Key

- Apache 預設使用 mpm_prefork -> 此模組不支援 HTTP/2 所需使用的 mod_http2
- mod_php 需要 perfork -> 因此不支援 HTTP/2

- 改用 mpm_worker 或 mpm_event 
- 改以 php-fpm 啟動 php

## 心得

去Ｏ的＃＃％＃＊＄＆＃＄＆，Apache 還是回歸塵土吧┻━┻︵╰(‵□′)╯︵┻━┻

Nginx、Caddy 好棒棒٩(˃̶͈̀௰˂̶͈́)و
