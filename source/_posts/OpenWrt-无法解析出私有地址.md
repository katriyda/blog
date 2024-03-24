---
title: OpenWrt 无法解析出私有地址
date: 2024-03-24 10:50:44
tags:
  - OpenWrt
  - DNS
---

因为需要解析出一个私有地址，发现怎么都解析不出来，猜测可能是 OpenWrt 某些选项影响了，果然在 DHCP/DNS 下找到了`重绑定保护`这个选项，可以去掉，也可以在下面的域名白名单里面添加需要解析的域名，然后就可以解析了。
![](https://img.katr.top/2024/03/8b844e12fad171cf1febad10ae607da2.png)
