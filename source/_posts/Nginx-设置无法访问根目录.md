---
title: "Nginx 设置无法访问根目录"
date: 2023-09-20 01:13:04
tags:
  - Nginx
  - Config
---

要求不能访问根目录，只能访问有路径的页面，并且强制要求访问根目录会跳转到 404 页面。

```nginx
    location / {
        if ($request_uri = '/') {
            return 404;
        }
        proxy_pass http://server/;
    }
```

<!-- ![洛天依](https://img.katr.tk/202309200147553.png) -->
<!-- ![洛天依](https://img.katr.tk/2023/12/31ed0c4a2fbf4541ec5eaae5bfcb0a97.png) -->

![洛天依](https://img.katr.top/2023/12/de4f7c49533fb7025e43d0fb2b56202c.webp)
