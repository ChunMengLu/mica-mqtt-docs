---
title: 保留消息
icon: inbox
order: 3
---

### MQTT 保留消息场景

- 例如，某设备定期发布自身 GPS 坐标，但对于订阅者而言，从它发起订阅到第一次收到数据可能需要几秒钟，也可能需要十几分钟甚至更多，这样并不友好。因此 MQTT 引入了保留消息。
- 而每当有订阅者建立订阅时，服务端就会查找是否存在匹配该订阅的保留消息，如果保留消息存在，就会立即转发给订阅者。
- 借助保留消息，新的订阅者能够立即获取最近的状态。