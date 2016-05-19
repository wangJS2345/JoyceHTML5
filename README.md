# JoyceHTML5
HTML5学习

2016/5/18
1.NetBeans新建HTML5项目

2.标签a的属性
  href
  download

3.HTML5全局属性
  class

2016/5/18
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
  解决办法:画面加载顺序是:先加载<head>，再加载<body>,所以把<script>中的内容,即javascript,写在<body>之后,</html>之前就可以了