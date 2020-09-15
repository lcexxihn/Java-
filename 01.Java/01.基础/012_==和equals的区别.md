# == 和 equals 的区别

## ==

基本类型：**值**是否相同

引用类型：**引用**是否相同

## equals

equals 本质上就是 ==，只不过 String 和 Integer 等重写了 equals 方法，把它变成了值比较。

源码：

```equals
Object.class

public boolean equals(Object obj) {
    return (this == obj);
}
```
