### iOS 中绘图到图形上下文

iOS app 中绘图到屏幕上，你需要设置 UIView 对象并重载 drawRect: 方法进行绘制。
当 view 可见或刷新时 view.drawRect: 方法会调用。
当调用你重载掉的 view.drawRect 方法前 view 会自动配置绘图环境让你可以直接绘画。
配置绘图环境的一部分就是创建适合的图形上下文(CGContextRef)。
你可以在 drawRect: 方法中调用 UIKit 函数 UIGraphicsGetCurrentContext 获取到图形上下文。

UIKit 与 Quartz 默认坐标系不一样。UIKit 中坐标原点在左上角，y坐标从上往下增长。
UIView 会修正 Quartz 图形上下文的 CTM （y坐标乘-1）让图形上下文的坐标与 UIKit 一致，都是y坐标从上往下增长。
更多修正坐标系相关信息参考[Quartz 2D 坐标系](../Overview/Coordinate.md)。

UIView 对象详细描述信息参考[View Programming Guide for iOS](https://developer.apple.com/library/content/documentation/WindowsViews/Conceptual/ViewPG_iPhoneOS/Introduction/Introduction.html#//apple_ref/doc/uid/TP40009503)。
