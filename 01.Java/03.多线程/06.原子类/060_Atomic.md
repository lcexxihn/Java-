# Atomic 原子类

> 操作是不可中断的

## java.util.concurrent 包中的原子类

### 基本类型

* AtomicBoolean：布尔型原子类
* AtomicInteger：整形原子类
* AtomicLong：长整型原子类

### 引用类型

* AtomicReference：引用类型原子类
* AtomicStampedReference：原子更新带有版本号的引用类型。该类将整数值与引用关联起来，可用于解决原子的更新数据和数据的版本号，可以解决使用 CAS 进行原子更新时可能出现的 ABA 问题。
* AtomicMarkableReference：

### 数组类型

* AtomicIntegerArray：整形数组原子类
* AtomicLongArray：长整形数组原子类
* AtomicReferenceArray：引用类型数组原子类

### 对象的属性修改类型

* AtomicIntegerFieldUpdater：原子更新整形字段的更新器
* AtomicLongFieldUpdater：原子更新长整形字段的更新器
