---
title: "参数介绍"
description: 本小节主要介绍 ClickHouse 常用配置项。 
keyword: 常用配置项,数据仓库,ClickHouse
weight: 10
collapsible: false
draft: false
---



在 AppCenter 集群管理控制台，支持对 ClickHouse 常用配置参数的管理。

本小节主要介绍 AppCenter 中各 ClickHouse 不可修改配置参数的含义。

## 参数说明

| <span style="display:inline-block;width:80px">参数</span> | <span style="display:inline-block;width:120px">取值范围</span> | <span style="display:inline-block;width:420px">参数说明</span> |
| :-------------------------------------------------------- | :----------------------------------------------------------- | :----------------------------------------------------------- |
| 用户名                                                    | -                                                            | 表示新创建数据库用户账号名。<ul><li>默认为 `default`。</li><li>创建集群后，ClickHouse 1.1.9及以上版本支持修改。</li></ul> |
| 密码                                                      | -                                                            | 表示新创建时设置的账号密码。<br>创建集群后，ClickHouse 1.1.9及以上版本支持修改。 |
| 副本数量                                                  | 1～3                                                         | 表示集群当前副本数量。<br>集群创建后不可修改。               |
| HTTP 端口                                                 | 0～65535                                                     | 表示 HTTP 端口号码。 <ul><li>默认为 `8123`。</li><li>集群创建后不可修改。</li></ul> |
| 允许访问网络列表                                          | 0~65535                                                      | 表示所有允许访问的网络列表，由分号分割的列表。<ul> <li>默认为 `::/0`，表示允许所有网络可访问。</li><li>创建集群后，ClickHouse 1.1.9及以上版本支持修改。</li></ul> |
| max_concurrent_queries                                    | -1，128～1024                                                | 表示同时处理请求的最大数量。 <br>- 默认值为-1，表示根据集群初始化 CPU 值动态设定最大请求数。 <br>- CPU 值｜最大请求数默认关系： 1C｜128，2C｜256，4C｜512，8C｜1024, 16C｜1024，32C｜1024。<span style="display: block; background-color: #D8ECDE; padding: 10px 24px; margin: 10px 0; border-left: 3px solid #00a971;"><b>说明</b>: <li>该参数修改后，数据库将重启。</li></span> |
| max_partitions_per_insert_block                           | 100～10000                                                   | 表示单个插入块中的最大分区数。 <br>- 默认值为100。 <span style="display: block; background-color: #D8ECDE; padding: 10px 24px; margin: 10px 0; border-left: 3px solid #00a971;"><b>说明</b>: <li>不建议设置过大，参数值过大可能影响数据库性能。</li></span> |
