# Redis 分布式锁

* 使用事务的 WATCH 命令
* 使用 SETNX 命令（只允许被一个程序占有，使用完调用 DEL 命令释放锁）

```SETNX
只有在 key 不存在时设置 key 的值
> SETNX key value
```

redis 分布式锁不能解决超时的问题，分布式锁有一个超时时间，程序的执行如果超出了锁的超时时间就会出现问题。

[参考](https://mp.weixin.qq.com/s?__biz=MjM5ODI5Njc2MA==&mid=2655825455&idx=1&sn=53e7043d76c0a39cf1b0d3be7a384ade&chksm=bd74e3f88a036aee104a1ec6001379d2238db2fde913b889b42138316e84ce9ed5e1ec271a10&mpshare=1&scene=1&srcid=&pass_ticket=ClR8gvFYBSjEqdmKbkRv3DDiFl24llL7GmzLG0VqhwWibafip2osNUEJPsuIGH7b#rd)
