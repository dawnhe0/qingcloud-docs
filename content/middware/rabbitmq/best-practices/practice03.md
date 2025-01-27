---
title: "Acknowledgements 和 Confirms"
description: Acknowledgements 和 Confirms 最佳实践
keyword: 云计算,大数据,消息队列,中间件,RabbitMQ
weight: 20
draft: false
---

在连接失败的情况下，传输中的消息可能会丢失，并且可能需要重新传输此类消息。

Acknowledgements 让服务器和客户机知道何时重新传输消息。客户机可以在收到消息时对其进行确认，也可以在客户机完全处理完消息后对其进行确认。Acknowledgement 具有性能影响，因此为了实现最快的吞吐量，应该禁用手动确认。
接收重要消息的消费应用程序在完成需要对其进行的任何操作之前不应确认消息，这样未处理的消息（工作进程崩溃、异常等）就不会丢失。
发布确认，也是一样的。如果发布者至少需要处理一次消息，服务器收到来自发布服务器的消息时会进行确认。发布确认也会影响性能。

## 未确认的消息

所有未确认的消息必须驻留在服务器上的 RAM 中。如果有太多未确认的消息，将耗尽内存。

您可以通过在客户端设置预取的消息数，限制未确认消息。
