# 概览

Quartz 2D 是给iOS及 macOS 非内核应用程序使用的二维绘画引擎。你可以使用Quartz 2D API 绘制路径、绘制透明、阴影、透明层、颜色管理、反锯齿渲染、PDF 文档生产、访问PDF 元数据。Quartz 2D 会尽量利用图形硬件设备的威力。

在 macOS 中 ，Quartz 2D 也可以跟其它的图形图像技术一起使用（像：Core Image、Core Video、OpenGL、QuickTime）。如：可以从 QuickTime 用 GraphicsImportCreateCGImage 函数导入图形然后在Quartz中创建图像。
[Quartz2D 与Core Image 之间数据传输](https://developer.apple.com/library/content/documentation/GraphicsImaging/Conceptual/drawingwithquartz2d/dq_data_mgr/dq_data_mgr.html#//apple_ref/doc/uid/TP30001066-CH216-BAJHEBHE) 说明了如何提供图片给Core Image ，哪些框架支持图像处理。

iOS中类似，Quartz 2D 也可以跟 Core Animationi 、OpenGL ES 及 UIKit 类一起使用
