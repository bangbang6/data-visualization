### 1.canvas

**所有操作都在 ctx 上进行 及**canvas 实例 ctx = canvas.getContext('2d')

**api**

ctx.fillstyle 形状内部填充色

ctx.fillrect 绘制矩形

绘制线段

ctx.beginPath() //开始绘制路径

ctx.lineWidth //宽度

ctx.strokeStyle //线条填充色

ctx.moveTo //设置起点

ctx.lineTo //绘制点终点

//持续调用 ctx.lineTo 可以绘制连续多条线段。

ctx.stroke() //**绘制线段 ** 这个才会真正的绘图

再次调用 ctx.beginPath 可以结束上次线段绘制 免得线段和下次画矩形的线连起来

**一般连续绘制上次的重点就是这次的起点** 除非用 Moveto 去改变起点

**一般 lineTo 都不会画线只是一个坐标变化知道线怎么画 调用完 stroke() 这个才是画线**

**fillStyle**一般是形状内部里的填充色

**strokeStyle**是画形状的线条的填充色

ctx.arc() //设置圆心坐标和半径和开始角度和结束角度

ctx.fill() //填充圆形等形状

ctx.stroke() //绘制圆形等的线段
ctx.clearRect() //清除画布

**一定搞清楚绘图属性和绘图 api**

属性是不会画出东西来的

fillstyle lineWidth strokeStyle moveTo strokeStyle arc

绘图 api 才会绘图出来

fillrect beginPath stroke fill

canvas 图片放缩会模糊 svg 不会 所以 svg 适合需要放大缩小的情况比如图标

svg 是 dom 开销比 canvas 多 在动画时候会卡顿

three.js webgl 都是在 canvas 上封装的三维图像的库

zrender 是封装了 canvas 和 svg 又是 echarts 的底层调用库
原图 2000*2000 canvas 画图 1024*1024 **是不会只取图片部分的** 而是会对图片进行等比压缩到这个大小达到图片压缩效果。
ctx.drawImage(1024,1024,img) 之前一直以为只取一部分导致主要部分丢失 **真实含义是**将大图绘制到 1024\*1024 大小的画布里
