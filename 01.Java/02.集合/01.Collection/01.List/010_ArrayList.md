# ArrayList 类

## 简介

* 底层采用数组实现
* 默认构造方法创建一个空数组
* 第一次添加元素，扩展容量为10；之后的扩充算法：原来数组大小+原来数组的一半
* 对元素进行查找，效率非常高
* 可以在集合中存储任意类型的数据
* 线程不安全

```底层源码
源码：

public class ArrayList<E> extends AbstractList<E> implements List<E>, RandomAccess, Cloneable, Serializable {
    transient Object[] elementData;
}
```

## 线程不安全

* 对 ArrayList 的操作一般分为两个步骤，改变位置(size)和操作元素(e)。
* 这个过程在多线程的环境下是不能保证具有原子性的，因此 ArrayList 在多线程的环境下是线程不安全的。

```注
注：
原子性 操作是不可中断的，要么全部执行成功，要么全部执行失败
```

## ArrayList优缺点

* 优点：

  因为其底层是 Object 数组，所以修改和查询效率高。

  可自动扩容(1.5倍)。

* 缺点：

  插入和删除效率不高。

  线程不安全。
