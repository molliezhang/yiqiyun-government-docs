---
title: "DeleteUserGroupMembers"
description: 
draft: false
---



删除用户组成员。

**Request Parameters**

| Parameter name | Type | Description | Required |
| --- | --- | --- | --- |
| user_group | String | 用户组 ID | Yes |
| users.n | String | 用户 ID | Yes |

[_公共参数_](../../../parameters/)

**Example**

_Example Request_

```
https://api.qingcloud.com/iaas/?action=DeleteUserGroupMembers
&user_group=ug-6zp387ak
&users.1=usr-iKf0yJEZ
&COMMON_PARAMS
```

_Example Response_:

```
{
  "action":"DeleteUserGroupMembersResponse",
  "user_group_id":"ug-6zp387ak",
  "user_ids":[
    "usr-iKf0yJEZ"
  ],
  "ret_code":0
}
```
