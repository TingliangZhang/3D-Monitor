# 3D-Monitor
3D显示效果

https://lookingglassfactory.com/

多人，怎么做到的。



决定直接用摄像头，摄像头提取人脸位置（最好是3D位置），放到Unity接口里面映射摄像头位置



## 新提案

壁画、版画

可变、有版权库、立体艺术、立体NFT艺术终端

图像分割制作终端

https://www.boe.com/CustomerProducts/BOEiGalleryS3





## 想法来源

[Box](https://youtu.be/lX6JcybgDFo)

通过机械臂+屏+相机的映射来做

如果把相机变成人眼做实时mapping呢？



找相关产品找到一个吹牛的推送：[离屏空间悬浮裸眼3D光场显示](https://mp.weixin.qq.com/s?__biz=MjM5OTg4ODIxNA==&mid=2662496414&idx=1&sn=07e6dc1f97c2a9a88b058adc160550a8)

然而最想要的显示屏已经有产品了：[Spatial Reality Display](https://www.sony.com/electronics/spatial-reality-display/elf-sr1)

和我想到解决方案一毛一样：柱面镜+全息膜+眼动。

所以能不能去掉全息膜，做一个让人感觉像是屏幕后面有东西呢？

用Realsense加上视角和景深，追踪人眼在空间中的位置呢？



## Realsense相关

软件

Intel® RealSense™ SDK 2.0 (v2.44.0)

https://github.com/IntelRealSense/librealsense/releases

Viewer可以用来看输出的效果，SDK里面包含Viewer和Quality Tool



## 摄像头获取头部位置

[openpose](https://github.com/CMU-Perceptual-Computing-Lab/openpose)

安装opencv-python

```shell
pip3 install opencv-python
```

跑exe Demo失败

```sh
PS C:\Users\ztl20\Downloads\openpose> bin\OpenPoseDemo.exe --face --hand
Starting OpenPose demo...
Configuring OpenPose...
Starting thread(s)...
Auto-detecting camera index... Detected and opened camera 0.
Auto-detecting all available GPUs... Detected 1 GPU(s), using 1 of them starting at GPU 0.
F0506 16:29:05.468179 19928 syncedmem.cpp:71] Check failed: error == cudaSuccess (2 vs. 0)  out of memory
*** Check failure stack trace: ***
```

显卡内存报错，估计是到集显上面了

https://blog.csdn.net/qq_44001342/article/details/105900378

还是要重新build



Unity的插件

https://github.com/CMU-Perceptual-Computing-Lab/openpose_unity_plugin



## 基本原理

视错觉，最好包括角度和景深。

图形得好好设计，为了观感更好。

接口工作量估计不小



## 软件方案

Unity或UE游戏引擎

可能需要仔细考虑怎么映射

https://docs.unity3d.com/Manual/class-Camera.html



## 硬件方案一

1080p摄像头 + 投影

追踪头部位置



## 硬件方案二

Realsense D435i + 32寸4k 60Hz面板 + UR机械臂（最多可以有两组）

可以做眼动，即捕捉看的方向

https://eyeware.tech/gazesense/

暂时还是放弃机械臂，工作量太大了。



