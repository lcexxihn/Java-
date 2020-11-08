# BIO、NIO、AIO 的区别

* BIO：Block IO 同步阻塞式 IO，数据的读取写入必须阻塞在一个线程内等待其完成。它的特点是模式简单使用方便，并发处理能力低。

* NIO：New IO 同步非阻塞 IO，是传统 IO 的升级，客户端和服务器端通过 Channel（通道）通讯，实现了多路复用。

* AIO：Asynchronous IO 是 NIO 的升级，也叫 NIO2，实现了异步非堵塞 IO ，异步 IO 的操作基于事件和回调机制。
