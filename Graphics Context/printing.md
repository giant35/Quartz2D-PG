## 获取打印图形上下文
macOS cocoa 应用程序 通过定制 NSView 子类实现打印。
打印时会调用 view.print:方法。
然后创建打印用的图形上下文然后调用 view.drawRect: 方法。
应用程序可以使用跟屏幕绘图同样的绘制代码绘图到打印机。
也可以定制 drawRect: 调用图片打印（译者：不懂 It can also customize the drawRect: call to an image to the printer that is different from the one sent to the screen.）。

Cocoa更多打印信息请参考 [Printing Programming Guide for Mac](https://developer.apple.com/library/content/documentation/Cocoa/Conceptual/Printing/osxp_aboutprinting/osxp_aboutprt.html#//apple_ref/doc/uid/10000083i)
