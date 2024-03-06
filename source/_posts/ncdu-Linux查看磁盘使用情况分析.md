---
title: 使用 ncdu 分析 Linux 磁盘使用情况
date: 2023-12-25 22:22:04
tags:
  - linux
  - 文件
---

Linux 下有时你可能会发现硬盘空间不足，而想要深入了解哪个目录占用的空间最多。在解决这个问题时，一个强大的工具是 <a href="https://dev.yorhel.nl/ncdu">ncdu</a>，该工具可通过各个发行版的包管理器直接安装。我这里使用 Debian 系的 apt 包管理器进行安装。

首先，使用以下命令安装 ncdu：

```bash
sudo apt install ncdu
```

安装完成后，你可以直接在需要查看的目录运行 ncdu 命令，以便进行磁盘使用情况的详细分析：

```bash
ncdu <options> <directory>
```

此命令将提供一个直观的终端界面，显示目录中各文件和子目录的大小，帮助你迅速定位空间占用较大的部分。
![](https://img.katr.top/2023/12/80c85dc6ecf2db07d20e3278b80b2029.png)
