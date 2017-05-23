## 图形状态

Quartz 绘制操作的参数会保存到当前图形状态（current graphics state）。
图形状态会被其它绘制操作使用。
绘制操作依赖图形状态决定如何渲染到图形上下文。
例如：当你调用一个设置填充颜色的方法时，你修改的是当前图形状态中的值。
其它当前图形状态公用的值包括线宽(line width)、当前位置、文字字体大小。

图形上下文包含一个图形状态堆栈。
当 Quartz 创建一个图形上下文时这个图形状态堆栈是空的。
当保存图形状态时(译者：调用CGContextSaveGState)，Quartz 会保存一份当前图形状态副本到这个堆栈。
当恢复图形状态时（译者：调用CGContextRestoreGState），当前图形状态会被堆栈中弹出的最后一份图形状态替换。

CGContextSaveGState() 方法用于保存当前图形状态副本到图形状态堆栈。
CGContextRestoreGState() 方法用于从堆栈中弹出一份图形状态替换掉当前图形堆栈。

注意：图形状态不是当前绘画环境的所有东西，而是元素的状态。如：图形状态不包括当前路径，所以 CGContextSaveGState 时不会保存当前路径。图形状态会保存的参数如表1-1：

表1-1 图形状态保存的参数

|参数|参考章节|
| :--- | :--- |
|当前变换矩阵(Current transformation matrix (CTM)) | |
|裁减区域(Clipping area) | |
|线条：宽度、转折点、头(cap)、虚线(dash)、miter limit||
|Accuracy of curve estimation (flatness)||
|反锯齿设置(Anti-aliasing)||
|颜色：填充、画线 设置|
|透明度||
|Rendering intent||
|颜色空间：填充、画线设置||
|文本：字体、字体大小、字符间距、文本绘制模式||
|融合模式||
