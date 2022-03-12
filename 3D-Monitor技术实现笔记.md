# 3D-Monitor技术实现笔记



## 技术方案参考

我们需要的是real time face detection的工具

OpenCV能满足：[Real-time Face detection | Face Mask Detection using OpenCV](https://www.mygreatlearning.com/blog/real-time-face-detection/)

[mtcnn](https://github.com/ipazc/mtcnn) face detection implementation for TensorFlow, as a PIP package.

[机器视觉（4）-- 云台人脸追踪_Techblog of HaoWANG ...](https://blog.csdn.net/hhaowang/article/details/88064497)



## OpenCV软件实现

**非常详细！！！**

PC环境为：Windows 11 64位专业工作站版 21H2，AMD Ryzen 9 5950X 16-Core Processor 3.40 GHz，Nvidia 3090 GPU，64G RAM。

编程环境：

[Python 3.10.2](https://www.python.org/ftp/python/3.10.2/python-3.10.2-amd64.exe)，安装时记得勾选Add Python3.10 to PATH

[TensorFlow](https://www.tensorflow.org/?hl=zh-cn) 2.8.0 参考指南：[安装TensorFlow](https://www.tensorflow.org/install?hl=zh-cn)，必要时安[TensorFlow Docker 映像](https://hub.docker.com/r/tensorflow/tensorflow/)是设置 [GPU 支持](https://www.tensorflow.org/install/gpu?hl=zh-cn)的最简单方法