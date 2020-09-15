# MyISAM 和 InnoDB 区别

MyISAM 是 MySQ 的默认数据库引擎（5.5版之前）。虽然性能极佳，而且提供了大量的特性，包括全文索引、压缩、空间函数等，但 MyISAM 不支持事务和行级锁，而且最大的缺陷就是崩溃后无法安全恢复。不过，5.5版本之后，MySQL 引入了 InnoDB（事务性数据库引擎），5.5版本后默认的存储引擎为InnoDB。

## MyISAM

* 只有表级锁（table-level locking）

* 不支持事务

  强调的是性能，每次查询具有原子性，其执行数度比InnoDB类型更快，但是不提供事务支持。

* 不支持外键

* 不支持MVCC

## InnoDB

* 支持行级锁（row-level locking）和表级锁，默认为行级锁

* 支持事务

  具有事务(commit)、回滚(rollback)和崩溃修复能力(crash recovery capabilities)的事务安全(transaction-safe (ACID compliant))型表。

* 支持外键

* 支持MVCC

应对高并发事务，MVCC 比单纯的加锁更高效；MVCC 只在 `READ COMMITTED` 和 `REPEATABLE READ` 两个隔离级别下工作；MVCC 可以使用 `乐观(optimistic)锁` 和 `悲观(pessimistic)锁` 来实现；各数据库中MVCC实现并不统一。
