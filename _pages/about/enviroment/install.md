---
layout: page
title: 软件下载与安装
permalink: /about/environment/install
---



#### apt

- 下载软件前先`apt update`一下
- 为了避免下载错，先看一下软件包是否存在，以及其型号
  - 用`apt search <package>`看一下软件包是否存在
  - 用`apt show <package>`看一下软件包的具体信息

#### 用wget下载和安装

- 安装包的选择大多需要知道操作系统内核和指令集架构，可以通过`uname -a`获取

##### 软件列表

- anaconda：https://repo.anaconda.com/archive/