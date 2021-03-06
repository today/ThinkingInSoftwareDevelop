流是程序输入或输出的一个连续的字节序列，设备(例如鼠标、键盘、磁盘、屏幕、调制解调器和打印机)的输入和输出都是用流来处理的。在C语言中，所有的流均以文件的形式出现----不一定是物理磁盘文件，还可以是对应于某个输入／输出源的逻辑文件。C语言提供了5种标准的流，你的程序在任何时候都可以使用它们，并且不必打开或关闭它们。以下列出了这5种标准的流。
------------------------------------------------
    名称          描  述            例  子
------------------------------------------------
    stdin        标准输入           键盘
    stdout       标准输出            屏幕
    stderr       标准错误            屏幕
    stdprn       标准打印机          LPT1端口
    stdaux       标准串行设备        COM1端口
------------------------------------------------
需要注意的是，stdprn和stdaux并不总是预先定义好的，因为LPT1和COM1端口在某些操作系统中是没有意义的，而stdin，stdout和stderr总是预先定义好的。此外，stdin并不一定来自键盘，stdout也并不一定显示在屏幕上，它们都可以重定向到磁盘文件或其它设备上。
同样的，在操作系统层面，所有的设备也都被封装成文件的形式，应用程序使用类似操作文件的 API 来操作各种设备。