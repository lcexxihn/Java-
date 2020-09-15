# Znode

## 简介

* 在分布式中，节点是指 **组成集群的每一台机器**
* 在 ZooKeeper 中，节点分为两类：
  * **机器节点**（构成集群的机器）
  * **数据节点**（Znode，数据模型中的数据单元）

在 ZooKeeper 中，node 可以分为 **持久节点** 和 **临时节点**

* 持久节点：一旦被创建，除非主动移除，否则这个 Znode 将一直保存在 ZooKeeper 上。

* 临时节点：生命周期和客户端会话绑定，一旦客户端会话失效，那么这个客户端创建的所有临时节点都会被移除。

## SEQUENTIAL

ZooKeeper 允许用户为每个节点添加一个特殊的属性：SEQUENTIAL。

节点被创建时，ZooKeeper 会自动在节点名后面追加一个整型的自增数字（由父节点维护）。

## Stat

ZooKeeper 的每个 Znode 上都会存储数据，对应于每个 Znode，ZooKeeper 都会为其维护一个叫作 Stat 的数据结构

Stat 中记录了 Znode 的三个数据版本：

* version（当前 Znode 的版本）
* cversion（当前 Znode 的子节点版本）
* aversion（当前 Znode 的ACL版本）

## Data
