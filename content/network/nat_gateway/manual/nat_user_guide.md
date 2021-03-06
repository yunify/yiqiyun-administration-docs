---
title: "操作指南"
description: Test descrIPtion
draft: false
weight: 2
keyword: NAT网关, NAT
---

假设2 台云服务器位于私有网络的办公网络中，您可以通过配置实现云服务器共用 NAT 网关的公网 IP 访问互联网。

## 创建和配置 NAT 网关

### 创建 NAT 网关

登录管理控制台，在控制台导航栏中，选择 **VPC 网络** > **NAT 网关**。在 **NAT 网关**页面，点击**创建**按钮。

<img src="../../_images/create_natgw.png" style="zoom:50%;" />

根据性能的需求选择相应规格的 NAT 网关，选择部署方式，并可以在创建时选择需要绑定的公网 IP 和私有网络。

### 配置 NAT 网关

创建 NAT 网关后，您还可以右键点击您创建的 NAT 网关，将 NAT 网关绑定到新的公网 IP 和私有网络。

![](../../_images/modify_natgw.png)

### 查看 NAT 网关配置

第一步：点击 NAT 网关详情页面，可以看到 NAT 网关的详细信息。左侧为 NAT 网关的基本信息和网络信息，右侧主要显示与 NAT 网关绑定的私有网络和相关的路由表项，及防火墙信息和监控图表。

![](../../_images/details_natgw.png)

第二步：点击**创建和配置路由表或路由规则**，然后点击**添加路由**。对于**下一跳**选择，勾选**NAT网关**，然后点击**提交**。

<img src="../../_images/add_router_rule.png" style="zoom:50%;" />

添加好路由后，需要点击**应用修改**以生效。

![](../../_images/details_natgw_rt.png)

NAT 网关中的配置的私有网络云服务器可以共用 NAT 网关，`路由规则`决定私有网络利用NAT网关可以去访问哪些 IP 地址。



### 修改 NAT 防火墙

由于 NAT 网关与多个网络连接，所以在各个方向均可以设置单独的安全组，可以对网络流量进行更细粒度的安全管理。

在左下角的**网络**区域，点击![](../../_images/icon.png)，可以修改基础网络和公网安全组：

<img src="../../_images/modify_natgw_fw1.png" style="zoom:50%;" />


在**更多操作**中，可以修改 NAT 网关与单个私有网络的安全组：

![](../../_images/modify_natgw_fw2.png)


## 配置私有网络和路由规则

在配置完成私有网络以后，需要在私有网路的路由表中添加规则，决定私有网络内的云服务器可以访问哪些 IP 地址。

点击查看[私有网络路由配置详情](../../../vpc/manual/route_table)。

配置路由规则并应用修改后，即可测试云服务器与互联网的连通情况。

