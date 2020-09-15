# HashSet 类

## 简介

* 基于 HashMap 实现，底层采用 HashMap 来保存元素
* 实现 Set 接口
* 仅存放对象
* 使用对象来计算 hashcode 值
* 线程不安全

```底层代码
public class HashSet<E> extends AbstractSet<E> implements Set<E>, Cloneable, Serializable ｛
    private transient HashMap<E, Object> map;
｝
```
