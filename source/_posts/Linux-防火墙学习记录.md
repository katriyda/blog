---
title: Linux 防火墙学习记录
date: 2024-03-12 19:38:10
tags:
  - Linux
  - 防火墙
---

iptables 命令参数

![Iptables参数](https://img.katr.top/2024/03/abba339ea8b6f7be46add643ae8cf87e.png)

iptables 上面规则的优先级最高，所以可以使用 -I 参数加在头部。

也可以使用 -A 参数添加一个在尾部兜底的规则。

```bash
# INPUT规则链默认策略改为拒绝
iptables -P INPUT DROP
```

```bash
# INPUT规则链设置环回地址放行
iptables -I INPUT -i lo -j ACCEPT
```

```bash
# INPUT规则链删除第一个规则
iptables -D INPUT 1
```

```bash
# 永久保存当前的iptables规则
iptables-save
```
