---
title: "对象存储"
date: 2020-11-25
draft: false
weight: 1
---

对象存储是面向海量非结构化数据的通用数据存储平台，为用户或企业提供安全可靠、低成本的云端存储服务。作为企业的数据存储和流转中心，用户可通过浏览器、HTTP RESTful API 、S3 API 、 SDK 和 FTP 等方式高效存取和管理文件，从而支撑企业丰富的上层业务和数据分析系统使用。

## 产品优势

**高可靠：** 对象存储具备跨地域的多数据中心服务能力，并支持数据的跨区复制，提供数据异地容灾功能。

**低成本：** 对象存储成本低廉，无需采购、部署和运维，可按量付费。并且支持用户通过存储分层及对象生命周期管理，将成本降至更低。

**无限水平扩展：**
  - 对象存储可无限水平扩展。当存储容量水平扩展时，相应的数据存取性能也能得到线性的提升。
  - 对象存储可承载无限存储空间。即，用户的 Bucket 容量可无限扩展。

**网络加速：**
  - 存储于对象存储内的数据，可通过 YiQiYun CDN 服务加速与分发，有效降低访问延迟、提升下载速度。
  - 存储于  对象存储内的数据，可与同区域内 YiQiYun IaaS 使用内网传输数据。
  - 对象存储支持断点续传。

**安全：**
  - 多租户间 100% 网络隔离，使用性能优异的防火墙及 DDoS 防护为用户提供全方位的防护服务。
  - 完善的访问控制；支持客户端及服务端数据加密；数据传输支持 SSL 协议，使您在团队协作中依旧能保持数据不泄露，不被轻易篡改。

**灵活易用：**
  - 对象存储可存储任意类型、任意数量、任意大小的文件。
  - 对象存储通过存储分层及对象生命周期管理，可覆盖用户的各种业务场景下的存储需求。
  - 对象存储提供 HTTP RESTful API 接口，及主流语言的 SDK 包，兼容 AWS S3 API，并提供详尽的 API 文档说明。
  - 对象存储与青云 YiQiYun 大数据平台无缝集成，为用户提供丰富的数据处理服务。

## 基本概念
### Object
对象，是对象存储中储存的基本数据单元，也是用户操作的基本数据单元。每个 Object 的访问地址有两种风格，详情可参考 [访问域名](#Endpoint)。

### Object Key
对象名称。其格式为：`<bucket_name>/<dir_name>/<object_name>`。如：`test_bucekt/test.mp3`，`test_bucekt/personal/test.mp3`。

### Bucket
用户创建的存储桶。用于存储用户上传的各种对象。

### Global
对象存储服务的全局管理服务。

### Zone
区域。和YiQiYun一样，对象存储服务支持多区域部署。用户可以在不同区域创建 Bucket。目前，对象存储开放的区域如下表所示：

| Name      | Zone ID | Domain Name |
|----------:|---------|-|
| 公共服务域 | zw |zw.obs.yiqiyun.sd.cegn.cn |
| 互联网域 | zw1 | zw1.obs.yiqiyun.sd.cegn.cn |

### Service
对象存储的顶层命令空间。在该命名空间下，每一个用户可以创建多个 Bucket。

### Endpoint

访问域名，每个 Object 的访问地址有如下两种风格:

- Virtual-host Style: `https://<bucket-name>.<zone-id>.obs.yiqiyun.sd.cegn.cn/<object-name>`
- Path Style: `https://<zone-id>.obs.yiqiyun.sd.cegn.cn/<bucket-name>/<object-name>`

其中 `<zone-id>` 代表 Bucket 创建时选择的区域。


## 服务等级协议

对象存储承诺数据持久性不低于 99.99999999%，服务可用性不低于99.99%。





