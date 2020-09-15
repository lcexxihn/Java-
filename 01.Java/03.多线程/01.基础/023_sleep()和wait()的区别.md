# sleep() 和 wait() 的区别

* sleep() 方法

  1. 属于 Thread 类中的静态方法
  2. 可在任意位置调用
  3. 不会释放锁
  4. 会自动唤醒
  5. 必须捕获异常（InterruptedException）

* wait() 方法

  1. 属于 Object 类中的方法
  2. 只能在 synchronized 块或方法中调用
  3. 线程会释放锁，并进入该对象的等待池中（等待池中的线程不会去竞争该对象的锁）
  4. 不会自动唤醒，需要通过调用 Object 类中的 notify()、notifyAll() 方法唤醒等待的线程；或者可以使用 wait(long timeout) 超时后线程会自动苏醒
  5. 不需要捕获异常
