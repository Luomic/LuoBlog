---
title: Linux基础命令与Python的基础
published: 2026-10-22
pinned: true
description: 学习ctf
image: https://jetpackcompose.cn/assets/images/demo4-541a9b9ed26bef86e75b05fbeecc51f6.gif
tags:
  - CTF
category: CTF
series: 笔记
seriesOrder: 1
---
> 近日开始学习CTF，记录学习路上的一些方法或者是一些Writeup

# Linux与命令

在PowerShell中安装WSL即可获得其内置的Linux子系统（仅针对Windows 10/11 系统）

## 基础命令：

| 命令    | 作用           | 示例                | 输出                 |
| ----- | ------------ | ----------------- | ------------------ |
| `pwd` | 查看当前进程目录     | `pwd`             | `/home/luomic`     |
| `cd`  | 切换工作目录       | `cd /mnt/c/user/` | C盘                 |
| `ls`  | 列出当前目录下的所有文件 | `ls -a`           | xxx.txt  basic.zip |

### `cd` 的参数：


| 参数     | 含义       |
| ------ | -------- |
| `cd -` | 返回上一次的目录 |
| `cd ~` | 返回home目录 |
| `cd /` | 返回根目录    |

### `ls` 的参数


| 参数   | 含义                |
| ---- | ----------------- |
| `-a` | 列出目录下所有文件         |
| `-l` | 列出文件详细属性（可读、可写）   |
| `-A` | 列出非隐藏文件           |
| `-h` | 列出文件大小            |
| `-t` | 按修改时间排序（最新）       |
| `-r` | 与`-t`相反，最新修改的在最尾端 |
| `-R` | 递归出子目录            |

![](images/ls.png)

