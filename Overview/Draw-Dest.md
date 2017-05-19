## 绘图目标：图形上下文

图形上下文(Graphics Context) 是用于绘制图像输出到设备上的一些信息，API中对应(CGContext、CGContextRef)，输出设备如： PDF文件，位图、显示窗口。
图形上下文包括图形绘制参数及输出设备相关信息，还包括了所有要绘制的对象。

如图1-2 你可以认为图形上下文就是绘画目标。当你使用Quartz 绘制时，所有设备相关的特性都包含在你用的图形上下文中。换句话说，你可以简单的用同样的绘制炒作但是不同的图形上下文，画同一图像到不同的设备。你不需要为不同的设备做不同的操作，Quartz 会帮你搞定。（译者：就是说图形上下文就是各种不同输出设备的抽象）


图1-2 Quartz 绘制目标
![图1-2](https://developer.apple.com/library/content/documentation/GraphicsImaging/Conceptual/drawingwithquartz2d/Art/draw_destinations.gif)



你可以在应用中使用下列图形上下文：(TODO)
* 位图图形上下文
* PDF 图形上下文
* 窗口图形上下文 (window graphics context)
* 图层图形上下文(layer graphics context)
* 打印图形上下文 （macOS)
