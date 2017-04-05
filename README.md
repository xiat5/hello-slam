ORB－SLAM的优点：

  1.Tracking的平均时间约为20ms每帧，基本可以达到实时追踪（i5－5200，2.2GHz）。
  
  2.丢帧以后回到原来的场景，很容易就可以找回来。
  
  3.定位的稳定性较好，姿态流畅，没有跳变。
  
  4.在简单背景下，可以有效地追踪目标物体。
  
ORB－SLAM的缺点：

  5.旋转时比较容易丢帧，特别是pure rotation。
  
  6.地图中的点云很稀疏，完全不能看出任何结构。
  
  7.加载地图需要一定时间（10秒左右，通过二进制词典可以加速，DBoW2的作者似乎是为了兼容性放弃了二进制）。
  
  8.初始化时最好保持低速运动，对准特征和几何纹理丰富的物体。
  
  9.作者为了增强系统的鲁棒性，在很多地方采用了多重判断，引入了N多参数。不同场景下的应用可能需要花一些时间理解和调整这些参数。
  
  10.随着SLAM时间的增长，如何控制图的结构和优化的规模，仍是现在SLAM有待解决的一个问题。
  

摘自

  https://www.zhihu.com/question/42050992/answer/93630213
  
  http://www.cnblogs.com/luyb/p/5240168.html
