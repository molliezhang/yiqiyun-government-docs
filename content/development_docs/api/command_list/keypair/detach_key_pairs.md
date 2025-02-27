---
title: "DetachKeyPairs"
description: 
draft: false
---



将任意数量的密钥对从云服务器中卸载， 云服务器状态须为“运行中”（ running ）或“已关机”（ stopped ）。

**Request Parameters**

| Parameter name | Type | Description | Required |
| --- | --- | --- | --- |
| keypairs.n | String | 密钥 ID | Yes |
| instances.n | String | 云服务器 ID | Yes |
| zone | String | 区域 ID，注意要小写 | Yes |

[_公共参数_](../../../parameters/) **Response Elements**

| Name | Type | Description |
| --- | --- | --- |
| action | String | 响应动作 |
| job_id | String | 执行任务的 Job ID |
| ret_code | Integer | 执行成功与否，0 表示成功，其他值则为错误代码 |

**Example**

_Example Request_:

```
https://api.qingcloud.com/iaas/?action=DetachKeyPairs
&keypairs.1=kp-12djpg8q
&instances.1=i-12345678,
&zone=zw1b
&COMMON_PARAMS
```

_Example Response_:

```
{
  "action":"DetachKeyPairsResponse",
  "job_id":"j-bm6ym3r8",
  "ret_code":0
}
```
