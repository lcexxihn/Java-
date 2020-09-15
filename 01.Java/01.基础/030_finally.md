# finally

## finally 语句不执行的情况

1. try语句没有被执行到，如在try语句之前就返回了，这样finally语句就不会执行，这也说明了finally语句被执行的必要而非充分条件是：相应的try语句一定被执行到。

2. 在try块中有 `System.exit(0);` 这样的语句，`System.exit(0);` 是终止Java虚拟机JVM的，连JVM都停止了，所有都结束了，当然finally语句也不会被执行到。

## finally 执行

1. finally语句，在return语句执行之后，return返回之前执行。

2. finally块中的return语句，会覆盖try块中的return。
