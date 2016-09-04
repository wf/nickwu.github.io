---
title: Tomgrok - 快捷构建自己的代码查询库
date: 2016-09-04 07:37:32
categories: tools
tags: [bash, tools, efficiency]
---
用过 LXR 可能了解到在 Linux Kernel 上使用交叉索引查询有多么的方便。现在有一个工具 [Tomgrok][] 能方便快捷的管理自己的代码库，构建交叉索引查询。

引自：[Tomgrok][]
> Tomgrok 是基于对 OpenGrok 和 Apache Tomcat 包装的一套脚本，致力于打造方便易用的源代码库，以提供对源代码进行 Web 式交叉索引查询。开箱即用，使用简单命令就能配置好 Apache Tomcat + OpenGrok，而无需对他们进行过多了解。OpenGrok 基本支持现在大部分语言，如 C、C++、Java、Javascript 等，具体详见：OpenGrok Supported Languages and Formats。

用法很简单，不需要了解 OpenGrok，直接通过 create 创建一个 Context（Webapp），再用 link 或 copy 将各个项目加进来，然后用 index 更新索引，用 tomgrok startup 启动 Web 服务即可。具体使用方法，请查看[Tomgrok][]。

自已可以建一些分类，比如将一些小的项目放到一个 Context，大的项目可以单独放。

[Tomgrok]: <https://github.com/wongdao/tomgrok> "Tomgrok Github"
