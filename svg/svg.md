### svg



canvas图片放缩会模糊 svg不会 所以svg适合需要放大缩小的情况比如图标和矢量图

svg是**dom** 开销比canvas多 在动画时候会卡顿

svg是dom编程 canvas是js的api编程 svg是一个一个dom可以选中



矩形是<rect style='

fill:red//填充色,

stroke-width:1px,

stroke:black//线段色'/>



线段<line>

x1,x2,y1,y2是起点和终点坐标

style = stroke:blue,stroke-width:2 //颜色和宽度



圆<circle>

cx,cy//圆心坐标

r 半径

stroke = green stroke-width=2

fill='red'

//fill 表示形状内部样式 stroke表示线条样式