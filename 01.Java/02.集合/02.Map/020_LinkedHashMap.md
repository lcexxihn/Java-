# LinkedHashMap

## 简介

* LinkedHashMap 是 HashMap 的一个子类
* 保存了记录的插入顺序，可以根据插入顺序排序；也可以在构造时带参数，按照应用次数排序

```源码
源码：

public class LinkedHashMap<K, V> extends HashMap<K, V> implements Map<K, V> {
    transient Entry<K, V> head;
    transient Entry<K, V> tail;
}
```
