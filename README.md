## Hi, I'm happiness-cheng

CS student focused on **high-performance C++ infrastructure** and **real-time data systems**.

### Featured Projects

#### [event_collector](https://github.com/happiness-cheng/event_collector) — 高并发 TCP 事件采集服务
> 单机峰值 **480K+ QPS** · **1.44 亿事件**生产验证 · Azure 云端部署 · 8 小时零崩溃

`C++17` `Boost.Asio` `Protobuf` `Kafka` `ClickHouse` `Redis` `Prometheus`

- 自定义 TCP 协议（4 字节长度前缀 + Protobuf）
- 分布式限流（Redis Lua 脚本）
- 降级模式（Redis/Kafka/ClickHouse 均可选）
- C epoll 客户端压测：**318K QPS**，500 并发，0% 丢包

#### [event_stream_engine](https://github.com/happiness-cheng/event_stream_engine) — 实时事件流处理引擎
> **2,473 万事件**生产验证 · Quality Pipeline 四阶段过滤 · Lambda 架构分流 · 99.2% 成功率

`C++17` `gRPC` `Kafka` `Redis Streams` `ClickHouse`

- Quality Pipeline：去重 → Watermark 纠偏 → HMAC-SHA256 反伪造 → GeoIP 补全
- Lambda 热/冷分流：Redis Streams（实时）+ ClickHouse（离线）
- 熔断器（CLOSED → OPEN → HALF_OPEN）
- 一致性哈希多租户路由

---

**Tech Stack:** C++17 · Boost.Asio · gRPC · Protobuf · Kafka · Redis · ClickHouse · Docker · Prometheus
