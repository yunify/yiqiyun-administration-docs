---
title: "StartCaches"
description: 
draft: false
---



启动一台或多台缓存服务。

**Request Parameters**

| Parameter name | Type | Description | Required |
| --- | --- | --- | --- |
| caches.n | String | 缓存服务ID | Yes |
| zone | String | 区域 ID，注意要小写 | Yes |

[_公共参数_](../../../parameters/)

**Response Elements**

| Name | Type | Description |
| --- | --- | --- |
| action | String | 响应动作 |
| job_id | String | 执行任务的 Job ID |
| ret_code | Integer | 执行成功与否，0 表示成功，其他值则为错误代码 |

**Example**

_Example Request_:

```
https://api.yiqiyun.net.cn/iaas/?action=StartCaches
&caches.1=c-55dwkqew
&zone=zw2
&COMMON_PARAMS
```

_Example Response_:

```
{
  "action":"StartCachesResponse",
  "job_id":"j-1234abcd",
  "ret_code":0
}
```
