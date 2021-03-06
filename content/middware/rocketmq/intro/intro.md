---
title: "什么是消息队列 RocketMQ"
description: 
draft: false
enableToc: false
keyword: 
---

[Apache RocketMQ](https://rocketmq.apache.org/)是一个基于[Apache 2.0 协议](https://github.com/apache/rocketmq/blob/master/LICENSE)开源的分布式消息和流数据平台，具有低延时、高吞吐、可审计、可几乎无限水平扩展等优点。

RocketMQ 和其他流行的消息系统之间的对比，请查阅[RocketMQ官网](https://rocketmq.apache.org/docs/motivation/#rocketmq-vs-activemq-vs-kafka)。

RocketMQ 通过云应用的形式在 AppCenter 部署，具有如下特性:

- 开箱即用
- 支持横向与纵向在线伸缩
- 支持高可用部署，无单点失败
- 系统自动运维，降低企业使用成本
- 提供了[监控告警](/monitor_service/cloudsat/)功能更好的管理集群
- 可通过网页控制台[RocketMQ Console](https://rocketmq-1.gitbook.io/rocketmq-connector/rocketmq-connect/rocketmq-console)对集群进行可视化管理
- 自`RocketMQ 4.7.1 - YiQiYiun 1.1.0`版本开始，新增日志自助获取机制，详情请查阅**文末[FAQ](/middware/rocketmq/faq/how_get_log/)部分**