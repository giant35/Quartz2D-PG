### 支持的像素格式

表2-1 汇总了位图上下文支持的像素格式、相关的颜色空间及可用操作系统。
像素格式由 每像素位数(bpp)及每分量位数(bpc)指定。
表中也包括了代码要用到的对应像素格式常量。
每种位图格式信息参考[CGImage Reference](https://developer.apple.com/reference/coregraphics/cgimage)

表2-1 位图支持的像素格式

|CS|Pixel format and bitmap information constant|Availability|
|:---|
|Null | 8 bpp, 8 bpc, kCGImageAlphaOnly | Mac OS X, iOS |
|Gray |8 bpp, 8 bpc,kCGImageAlphaNone|Mac OS X, iOS|
|Gray|8 bpp, 8 bpc,kCGImageAlphaOnly|Mac OS X, iOS|
|Gray|16 bpp, 16 bpc, kCGImageAlphaNone|Mac OS X|
|Gray|32 bpp, 32 bpc, kCGImageAlphaNone,kCGBitmapFloatComponents|Mac OS X|
|RGB|16 bpp, 5 bpc, kCGImageAlphaNoneSkipFirst|Mac OS X, iOS|
|RGB|32 bpp, 8 bpc, kCGImageAlphaNoneSkipFirst|Mac OS X, iOS|
|RGB|32 bpp, 8 bpc, kCGImageAlphaNoneSkipLast|Mac OS X, iOS|
|RGB|32 bpp, 8 bpc, kCGImageAlphaPremultipliedFirst|Mac OS X, iOS|
|RGB|32 bpp, 8 bpc, kCGImageAlphaPremultipliedLast|Mac OS X, iOS|
|RGB|64 bpp, 16 bpc, kCGImageAlphaPremultipliedLast|Mac OS X|
|RGB|64 bpp, 16 bpc, kCGImageAlphaNoneSkipLast|Mac OS X|
|RGB|128 bpp, 32 bpc, kCGImageAlphaNoneSkipLast kCGBitmapFloatComponents|Mac OS X|
|RGB|128 bpp, 32 bpc, kCGImageAlphaPremultipliedLast  ，kCGBitmapFloatComponents|Mac OS X|
|CMYK|32 bpp, 8 bpc, kCGImageAlphaNone|Mac OS X|
|CMYK|64 bpp, 16 bpc, kCGImageAlphaNone|Mac OS X|
|CMYK|128 bpp, 32 bpc, kCGImageAlphaNone ，kCGBitmapFloatComponents|Mac OS X|
