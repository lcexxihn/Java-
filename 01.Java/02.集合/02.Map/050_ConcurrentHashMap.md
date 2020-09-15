# ConcurrentHashMap

* 线程安全

  采用 CAS 和 synchronized 来保证并发安全。

  synchronized 只锁定当前链表或红黑二叉树的根节点，这样只要 hash 不冲突，就不会产生并发，效率又提升N倍。

  ```JDK1.7
  JDK1.8 摒弃了 Segment 的概念

  在 JDK1.7 的时候，ConcurrentHashMap（分段锁）对整个桶数组进行了分割分段(Segment)，每一把锁只锁容器其中一部分数据，多线程访问容器里不同数据段的数据，就不会存在锁竞争，提高并发访问率。
  ```

* 底层采用 Node数组+链表/红黑二叉树 实现

  ```JDK1.7
  JDK1.7
  底层采用 分段的数组+链表 实现
  ```
