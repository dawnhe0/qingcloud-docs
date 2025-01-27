---
title: "创建告警策略"
draft: false
collapsible: false
weight: 10
---

SD-WAN 为您提供监控数据的告警服务，您可以通过创建指标告警策略或者事件告警策略来定义告警系统如何检查监控数据，并在监控数据满足告警策略时发送报警通知。

对重要监控指标或者事件创建告警策略后，您即可在第一时间得知指标数据或者事件发生异常，并迅速处理故障。

## 创建指标告警策略

1. 登录 QingCloud 管理控制台。

2. 选择**产品与服务** > **SD-WAN（新版）** > **SD-WAN（新版）**，进入**概览**页面。

   <img src="../../../_images/qs_cloud_network.png" style="zoom:50%;" />

3. 在左侧导航栏中，点击**告警设置**，进入**告警设置** > **指标告警**页面。

   ![](../../../_images/um_alarm_list.png)

4. 点击**创建告警策略**，进入**创建告警策略**页面。

   <img src="../../../_images/um_alarm_indicator_create.png" style="zoom:50%;" />

5. 配置相关告警参数，如下表所示。

   | 参数     | 参数说明                                                     |
   | -------- | ------------------------------------------------------------ |
   | 策略名称 | 告警策略的名称。                                             |
   | 告警对象 | 您可以选择全部对象。                                         |
   | 告警类型 | 选择**指标告警**。                                           |
   | 监控周期 | 在下拉列表中，选择监控周期的时间。                           |
   | 告警规则 | 请根据实际情况选择告警规则。<br />若需要添加多个规则，您可以点击**添加规则**，添加更多的规则。<br />最多支持添加 20 条规则。 |
   | 触发条件 | 请根据实际情况设置触发条件。                                 |
   | 告警级别 | 设置高级级别为**高**、**中**、**低**。                       |
   | 发送通知 | 您可以开启或者关闭发送通知。开启发送通知后，当触发告警后，添加到**通知列表**中相关人员将会收到告警通知。 |
   | 通知列表 | 通知列表用于保存接收通知的联系方式。若没有通知列表，您可以点击**新建通知列表**，添加新的通知列表。 |
   | 通知方式 | 您可以选择全部、邮件、短信、微信或者 webhook 中的一种通知方式，或者选择多种通知方式。 |
   | 通知时间 | 选择通知的时间。                                             |

6. 点击**创建**，完成指标告警策略的创建操作。

   告警策略创建完成后，您可以在告警列表中查看告警状态，默认为**开启**。

## 创建事件告警策略

1. 登录 QingCloud 管理控制台。

2. 选择**产品与服务** > **SD-WAN** > **SD-WAN**，进入**概览**页面。

   <img src="../../../_images/qs_cloud_network.png" style="zoom:50%;" />

3. 在左侧导航栏中，点击**告警设置**，进入**告警设置** > **指标告警**页面。

   ![](../../../_images/um_alarm_list.png)

4. 点击**创建告警策略**，进入**创建告警策略**页面。

   <img src="../../../_images/um_alarm_event_create.png" style="zoom:50%;" />

5. 配置相关告警参数，如下表所示。

   | 参数     | 参数说明                                                     |
   | -------- | ------------------------------------------------------------ |
   | 策略名称 | 告警策略的名称。                                             |
   | 告警对象 | 您可以选择**全部对象**或**部分对象**。当选择部分对象时，可选择其中某个业务组或者多个接入点。 |
   | 告警类型 | 选择**事件告警**。                                           |
   | 监控周期 | 在下拉列表中，选择监控周期的时间。                           |
   | 告警规则 | 请根据实际情况选择告警规则。<br />若需要添加多个规则，您可以点击**添加规则**，添加更多的规则。<br />最多支持添加 20 条规则。 |
   | 触发条件 | 请根据实际情况设置触发条件。您可以选择为**立即触发**或者**累计触发**。 |
   | 告警级别 | 设置高级级别为**高**、**中**、**低**。                       |
   | 发送通知 | 您可以开启或者关闭发送通知。开启发送通知后，当触发告警后，添加到**通知列表**中相关人员将会收到告警通知。 |
   | 通知列表 | 通知列表用于保存接收通知的联系方式。若没有通知列表，您可以点击**新建通知列表**，添加新的通知列表。 |
   | 通知方式 | 您可以选择全部、邮件、短信、微信或者 webhook 中的一种通知方式，或者选择多种通知方式。 |
   | 通知时间 | 选择通知的时间。                                             |

6. 点击**创建**，完成事件告警策略的创建操作。

   告警策略创建完成后，您可以在告警列表中查看告警状态，默认为**开启**。

## 相关操作

### 开启/关闭告警策略

1. 进入告警设置的**指标告警/事件告警**页面。
2. 在待开启/关闭策略所在行，点击**开启/关闭**，开启/关闭告警策略。

### 修改告警策略

1. 进入告警设置的**指标告警/事件告警**页面。

2. 在待修改策略所在行，点击**修改**，弹出**修改策略**窗口。

   <img src="../../../_images/um_alarm_modify_policy.png" style="zoom:50%;" />

3. 根据需要修改策略后，点击**确定修改**，完成策略修改操作。

### 禁用告警策略

禁用规则后将不能收到告警通知，请谨慎操作。

1. 进入告警设置的**指标告警/事件告警**页面。

2. 点击待禁用策略名称，进入策略详细信息页面。

   ![](../../../_images/um_alarm_policy_details.png)

3. 点击**禁用**，弹出**禁用策略**窗口。

   <img src="../../../_images/um_alarm_policy_disabled.png" style="zoom:50%;" />

4. 点击**确定**，完成策略禁用操作。

### 删除告警策略

删除规则后将不能恢复，请谨慎操作。

1. 进入告警设置的**指标告警/事件告警**页面。

2. 在待删除策略所在行，点击**删除**，弹出**删除策略**窗口。

   <img src="../../../_images/um_alarm_policy_del.png" style="zoom:50%;" />

3. 点击**确定**，完成策略删除操作。
