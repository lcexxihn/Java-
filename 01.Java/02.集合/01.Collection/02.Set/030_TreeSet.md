# TreeSet 类

## 简介

* 基于 TreeMap 实现
* 实现 NavigableSet（继承SortedSet）接口，能够把保存的记录根据键排序
* 线程不安全

```源码
源码：

public class TreeSet<E> extends AbstractSet<E> implements NavigableSet<E>, Cloneable, Serializable {
    private transient NavigableMap<E, Object> m;
}
```
