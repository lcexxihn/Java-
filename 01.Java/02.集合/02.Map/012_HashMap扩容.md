# HashMap 扩容

## rehash

HashMap 在扩容时的一个步骤。

```链表环
JDK1.8之前，在并发的情况下可能会形成链表环。
```

## resize

1. HashMap 的容量是有限的，当经过多次元素插入，使得 HashMap 达到一个饱和度时，key 映射的位置发生冲突的几率会逐渐提高。

2. 这时候，HashMap 需要扩展它的长度，也就是时行 `resize`。

   * 影响 resize 的因素：

     * Gapacity（HashMap 当前长度）
     * LoadFactor（HashMap 负载因子，默认值为 0.75f）

   * 条件：HashMap.size >= Gapacity * LoadFactor

3. resize

   * 扩容

     创建一个新的空数组，长度是原数组的2倍。

   * rehash

     由于长度改变，需要重新计算 index
