# TreeMap

## 简介

* 红黑树（自平衡的排序二叉树）
* 实现 NavigableMap（继承SortedMap）接口，能够把保存的记录根据键排序
* 线程不安全

```源码
源码：

public class TreeMap<K, V> extends AbstractMap<K, V> implements NavigableMap<K, V>, Cloneable, Serializable {
    private transient NavigableMap<K, V> descendingMap;
}
```

## 根据键排序

* 能够把保存的记录根据键排序
* 默认是按键值的升序排序，也可以指定排序的比较器
* 当用 Iterator 遍历 TreeMap 时，得到的记录是排过序的

在使用 TreeMap 时，key 必须实现 Comparable 接口或者在构造 TreeMap 传入自定义的 Comparator，否则会在运行时抛出java.lang.ClassCastException类型的异常。
