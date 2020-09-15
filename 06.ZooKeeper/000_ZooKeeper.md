# ZooKeeper

## 简介

分布式协调服务

* ZooKeeper 底层其实只提供了两个功能：

  * 管理（读取/存储）用户程序提交的数据
  * 为用户程序提供数据节点监听服务

* ZooKeeper 本身就是一个分布式程序（只要半数以上节点存活，ZooKeeper 就能正常服务）

## 功能

ZooKeeper 是一个典型的 **分布式数据一致性解决方案**，分布式应用程序可以基于 ZooKeeper 实现：

* 数据发布/订阅
* 负载均衡
* 命名服务
* 分布式协调/通知
* 集群管理
* Master 选举
* 分布式锁
* 分布式队列

## 特点

* **顺序一致性：**

  从同一客户端发起的事务请求，最终将会严格地按照顺序被应用到 ZooKeeper 中去。

* **原子性：**

  所有事务请求的处理结果在整个集群中所有机器上的应用情况是一致的，也就是说，要么整个集群中所有的机器都成功应用了某一个事务，要么都没有应用。

* **单一系统映像：**

  无论客户端连到哪一个 ZooKeeper 服务器上，其看到的服务端数据模型都是一致的。

* **可靠性：**

  一旦一次更改请求被应用，更改的结果就会被持久化，直到被下一次更改覆盖。

## 顺序访问

对于来自客户端的每个更新请求，ZooKeeper 都会分配一个全局唯一的递增编号（时间戳 —— zxid，ZooKeeper Transaction Id），这个编号反应了所有事务操作的先后顺序，应用程序可以使用 ZooKeeper 这个特性来实现更高层次的同步原语。

## 高性能

在 **"读"** 多于 **"写"** 的应用程序中尤其地高性能，因为 **"写"** 会导致所有的服务器间同步状态。

客户端的读请求可以被集群中的任意一台机器处理，如果读请求在节点上注册了监听器，这个监听器也是由所连接的 ZooKeeper 机器来处理。

对于写请求，这些请求会同时发给其他 ZooKeeper 机器并且达成一致后，请求才会返回成功。

因此，随着 ZooKeeper 的集群机器增多，读请求的吞吐会提高但是写请求的吞吐会下降。