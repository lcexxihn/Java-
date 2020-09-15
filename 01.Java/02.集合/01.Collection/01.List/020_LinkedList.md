# LinkedList 类

## 概述

* 基于双向链表
* 可以在任何位置进行高效地插入和移除操作
* 允许元素为 null
* 线程不安全

```底层源码
源码:

public class LinkedList<E> extends AbstractSequentialList<E> implements List<E>, Deque<E>, Cloneable, Serializable {
    transient Node<E> first;
    transient Node<E> last;
}

private static class Node<E> {
    E item;
    Node<E> next;
    Node<E> prev;
}
```

## 与 ArrayList 对比

* 优点：

  不需要扩容和预留空间，空间效率高

  增删效率高

* 缺点：

  随机访问时间效率低

  改查效率低
