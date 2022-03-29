---
title: "登录镜像仓库"
description: 介绍如何通过 Docker Cli 登录到 Docker Hub。
draft: false
keyword: 云计算, Docker, 镜像仓库
weight: 8
---

您可以通过 Docker Cli 登录到 Docker Hub。

## 背景信息

公有云镜像仓库 (Docker Hub) 的访问域名是 `dockerhub.yiqiyun.net.cn`。

## 前提条件

- 已创建 公有云镜像仓库。
- 已获取登录用户名及密码。
- 已下载及安装 Docker，具体操作请参见 [Docker 官方文档](https://docs.docker.com/get-docker/)。

## 操作步骤

安装 Docker 后，在本地终端命令行，执行以下命令便可登录到镜像仓库。

```
docker login -u <username> -p <password> dockerhub.yiqiyun.net.cn
```

> **说明**：
>
> `<username>` 及 `<password>` 表示 Docker 的登录用户名及密码。

