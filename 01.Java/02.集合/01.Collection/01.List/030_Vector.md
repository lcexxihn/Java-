# Vector 类

* 底层采用数组实现
* 默认构造方法创建一个大小为10的数组
* 扩充的算法：当增量为0时，扩充为原来大小的2倍，当增量大于0时，扩充为原来大小+增量
* 线程安全，使用 synchronized

```底层源码
源码：

public class Vector<E> extends AbstractList<E> implements List<E>, RandomAccess, Cloneable, Serializable {
    protected Object[] elementData;
}
```
