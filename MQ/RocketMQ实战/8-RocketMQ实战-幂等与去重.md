# 8-RocketMQ实战-幂等与去重

[TOC]

## 8.1 基本概念

### 幂等性

- 一个幂等操作的特点是其任意多次执行所产生的影响均与一次执行的影响相同。
- 在MQ中broker不可避免的会发送重复的数据,到我们的consumer,consumer必须要保证处理的消息是唯一的.

## 8.2 如何去重

- 去重原则
    1. 幂等性
    2. 业务去重
- 去重策略
    1. 去重表机制
    2. 业务拼接去重(指纹码,唯一流水号)
- 高并发去重
    1. redis去重(需要有补偿策略)