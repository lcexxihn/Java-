# redis 和 memcached 的区别

## 区别

1. redis 支持更丰富的数据类型（支持更复杂的应用场景）

2. redis 支持数据持久化

3. 集群模式：redis 目前是原生支持 cluster 模式的；memcached 没有原生的集群模式，需要依靠客户端来实现往集群中分片写入数据

4. redis 使用单线程的多路 IO 复用模型；memcached 是多线程，非阻塞 IO 复用的网络模型
