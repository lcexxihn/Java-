# Executor 和 Executors 的区别

* Executors 工具类的不同方法按照我们的需求创建了不同的线程池，来满足业务的需求。
* Executor 接口对象能执行我们的线程任务。
* ExecutorService 接口继承了 Executor 接口并进行了扩展，提供了更多的方法我们能获得任务执行的状态并且可以获取任务的返回值。
* 使用 ThreadPoolExecutor 可以创建自定义线程池。
* Future 表示异步计算的结果，他提供了检查计算是否完成的方法，以等待计算的完成，并可以使用 get()方法获取计算的结果。
