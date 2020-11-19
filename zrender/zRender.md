## zrender

echarts的渲染引擎  支持canvas svg 等

需要引入zrender的库 自带zrender对象

zr = zrender.init(dom) //初始化对象

zr.add()来在canvas里面图形

shape style和canvas的api一样

let rect = new zrender.Rect({shape:{},style:{}})来绘制矩形

let line = new zrender.Polyline() //来绘制线段

let circle = new zrender.Circle() //绘制圆形

想深入学习 zrender 的同学可以参考[官方案例](https://ecomfe.github.io/zrender-doc/public/examples/animation.html)，源码可以在 [zrender-docs](https://github.com/ecomfe/zrender-doc/tree/master/public/examples) 中找到