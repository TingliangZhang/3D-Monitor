# 3D-Monitor
3D显示效果



想法来源：

[Box](https://youtu.be/lX6JcybgDFo)

通过机械臂+屏+相机的映射来做

如果把相机变成人眼做实时mapping呢？



找相关产品找到一个吹牛的推送：[离屏空间悬浮裸眼3D光场显示](https://mp.weixin.qq.com/s?__biz=MjM5OTg4ODIxNA==&mid=2662496414&idx=1&sn=07e6dc1f97c2a9a88b058adc160550a8)

然而最想要的显示屏已经有产品了：[Spatial Reality Display](https://www.sony.com/electronics/spatial-reality-display/elf-sr1)

和我想到解决方案一毛一样：柱面镜+全息膜+眼动。

所以能不能去掉全息膜，做一个让人感觉像是屏幕后面有东西呢？

用Realsense加上视角和景深，追踪人眼在空间中的位置呢？



Realsense相关

软件

Intel® RealSense™ SDK 2.0 (v2.44.0)

https://github.com/IntelRealSense/librealsense/releases

Viewer可以用来看输出的效果



## 基本原理

视错觉，包括

## 软件方案

Unity或UE游戏引擎

可能需要仔细考虑怎么映射

## 硬件方案一

1080p摄像头 + 投影

追踪头部位置

## 硬件方案二

Realsense D435i + 32寸4k 60Hz面板 + UR机械臂（最多可以有两组）

可以做眼动，即捕捉看的方向

https://eyeware.tech/gazesense/