# ZooKeeper 集群角色

ZooKeeper 集群中的所有机器通过一个 Leader 选举过程来选定一台称为 “Leader” 的机器。

Leader 既可以为客户端提供写服务又能提供读服务。

Follower 和 Observer 只能提供读服务。

## Leader 领导者

* 事务请求的唯一调度者和处理者，保证集群事务处理的顺序性
* 集群内部各服务器的调度者

## Learner 学习者

Follower 跟随者

* 处理客户端非事务请求，转发事务请求给 Leader
* 参与事务请求 Proposal 的投票
* 参与 Leader 选举的投票

Observer 观察者

* Follower 和 Observer 唯一的区别在于 Observer 不参与 Leader 的选举过程，也不参与写操作的“过半写成功”策略，因此 Observer 机器可以在不影响写性能的情况下提升集群的读性能。

## Client 客户端

通过与集群中的某一台机器建立 TCP 连接来使用服务，客户端使用这个 TCP 链接来发送请求、获取结果、获取监听事件以及发送心跳包。
