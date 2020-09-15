# equals

equals()方法必须满足：

```equals
自反性，x.equals(x)必须返回true
对称性，x.equals(y)返回true时，y.equals(x)也必须返回true
传递性，x.equals(y)和y.equals(z)都返回true时，x.equals(z)也必须返回true
一致性，当x和y引用的对象信息没有被修改时，多次调用x.equals(y)应该得到同样的返回值
而且对于任何非null值的引用x，x.equals(null)必须返回false
```

**1. 为什么重写equals()时必须重写hashCode()方法？**

> 如果两个对象相同，那么它们的hashCode值一定要相同；
反之，则不一定；
>
> 默认的hashCode()方法是根据对象的内存地址经哈希算法得来的。

源码：

```hashCode
Object.class

public native int hashCode();

public boolean equals(Object paramObject) ｛
    return this == paramObject;
｝
```
