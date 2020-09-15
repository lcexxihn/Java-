# String

## String 和 StringBuilder、StringBuffer 的区别

* String 是只读字符串，字符串内容是不能被改变的。
* StringBuffer / StringBuilder 类表示的字符串对象可以直接进行修改。
* StringBuilder 是 Java5 中引入的，它和 StringBuffer 的方法完全相同，区别在于它是在单线程环境下使用的，因为它的所有方面都没有被 synchronized 修饰（非同步），因此它的效率也比 StringBuffer 要高。

## 请说出下面程序的输出

```2
String s1 = "Programming";
String s2 = new String("Programming");
String s3 = "Program";
String s4 = "ming";
String s5 = "Program" + "ming";
String s6 = s3 + s4;
System.out.println(s1 == s2); // false
System.out.println(s1 == s5); // true
System.out.println(s1 == s6); // false
System.out.println(s1 == s6.intern()); // true
System.out.println(s2 == s2.intern()); // false
```

## intern()方法

* 用来返回常量池中的某字符串，如果常量池中已经存在该字符串，则直接返回常量池中该对象的引用。
* 否则，在常量池中加入该对象，然后 返回引用。

```intern
String.class

public native String intern();
```

## 如何将字符串反转

使用 StringBuilder 或者 StringBuffer 的 reverse() 方法。
