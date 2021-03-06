## 内存管理：对象所有权
Quartz 使用 Core Foundation 引用计数内存管理模型。
创建时对象引用计数为1。
当获取(retain)对象时可以调用相关方法增加引用计数，释放(release)对象时调用方法减少引用计数。
引用计数减少到0时，对象被释放。
这个模型能安全引用其它对象。

需要记住一些简单的规则：
* 如果创建或复制出一个对象，你拥有此对象所以不用后需要释放它。一般来说方法名中包含"Create" 或 "Copy" 就表示不用时需要释放它。否则会产生内存泄漏。
* 如果不是创建或复制出的对象，你没有拥有对象所以不需要释放它。对象会由它自己的拥有者释放。
* 如果你没拥有对象但你要用它，你需要获取对象用完后释放。可以使用Quartz 2D 一些方法获取释放对象。如：使用 CGColorSpaceRetain 获取 CGColorSpaceRef 对象，使用 CGColorSpaceRelease 不用时释放对象。也可以使用 Core Foundation 函数 CFRetain 与 CFRelease ，要小心不要传递 NULL 给这些函数。
