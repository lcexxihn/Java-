# Error 与 Exception

## Error

Error 是非程序异常，即程序不能捕获的异常，一般是编译或者系统性的错误，如 OutOfMemorry 内存溢出异常等。

## Exception

Exception 是程序异常，由程序内部产生。

Exception 又分为运行时异常、非运行时异常。

* 运行时异常

  运行时异常的特点是Java编译器不会检查它。

  常见的运行时异常如 NullPointException、ArrayIndexOutOfBoundsException 等。

* 非运行时异常（受检查异常）

  非运行时异常是程序必须进行处理的异常，捕获或者抛出，如果不处理程序就不能编译通过。

  如常见的 IOException、ClassNotFoundException 等。
