# JoyceHTML5
HTML5学习

###2016/5/18
1.NetBeans新建HTML5项目

2.标签a的属性
  href
  download

3.HTML5全局属性
  class

###2016/5/19
1.添加mp4文件 播放成功
  video标签
  controls属性:向用户显示控件
  autoplay属性:自动播放视频
  height属性:视频的高度
  width属性:视频的宽度
  loop属性:视频自动重拨
  preload属性:视频加载方式,预加载/点击加载
  src属性:视频文件路径,绝对路径:指向另一个站点;相对路径:指向网址内的文件

2.控制video的播放
  从初始HTML跳转到另一个画面

  getElementsByTagName根据标签名获取控件成功
  getElementsById根据控件id获取控件失败

  控制video的播放/暂停/播放画面大小成功

  getElementsById根据控件id获取控件失败的原因:
  画面加载实在<body></body>之前执行,此时此时id="myVideo"对应的控件,还没有加载进去.
  解决办法:画面加载顺序是:先加载<head>，再加载<body>,所以把script标签中的内容,即javascript,写在body标签之前,head之内就可以了
  
  3.点击文本，改变文本文言
  注意：
  <h1 onclick="this.innerHTML='谢谢!'">请点击该文本</h1>
  一定要注意，不能有遗漏符号，否则代码无效
  
  http://www.w3school.com.cn/html5/html_5_draganddrop.asp
  将图片拖放至矩形

####2016/05/20
1.图片在矩形中拖放
  来回拖放成功，但是由于未注明要拖放图片的id，画面上的图片，draggable属性为true的，都可以进行来回拖放
  
#####画布
1.canvas标签 画布，需注意要声明style属性，否则画布没有边框，看不出来

2.绘制线条的起点用moveTo表示，每增加一个lineTo，增加一个节点

3.绘制圆

cxt.arc(100,100,30,0,Math.PI*2,true); 括号内第一个和第二个参数,代表圆心坐标.第三个参数是圆的半径.第四个参数代表圆周起始位置.0 PI就是起始位置.沿顺时针路线,分别是0.5 PI（正下方）,1 PI和1.5 PI（正上方）,为画饼图提供了扇形范围的依据.第五个参数是弧长Math.PI*2就是整个圆,Math.PI是半圆.第六个参数是一个布尔值,true是顺时针false是顺时针.
 
4.绘制渐变矩形

注意：渐变矩形只能给定两个颜色，否则绘制失败

5.把图片放到画布上

注意：需要写清楚图片路径

6.绘制矩形 填充颜色

注意：此部分代码要写到body标签内，否则无效