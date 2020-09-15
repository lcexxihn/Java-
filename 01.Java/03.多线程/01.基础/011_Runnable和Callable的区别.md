# Runnable和Callable的区别

都是接口

* Runnable

    run() 方法，没有返回值

* Callable

    call() 方法，返回泛型

    和 Future、FutureTask 配合可以用来获取异步执行的结果。

源码：

```Runnable
@FunctionalInterface
public interface Runnable {
    public abstract void run();
}
```

```Callable
@FunctionalInterface
public interface Callable<V> {
    V call() throws Exception;
}
```
