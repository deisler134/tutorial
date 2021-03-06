# Windows10环境下安装TensorFlow-GPU版
## 环境
* 系统：Windows 10 Enterprise
* 版本：1703
* 处理器：Intel(R) Core(TM) i7-7700K CPU @ 4.20GHz
* 内存：16.0GB
* 类型：64位操作系统 64位处理器
* 显卡：索泰GTX1060 6G
## 注意事项
* 显卡支持CUDA；
* Python版本是3.5.0 64位及以上；
* 稳定的网络连接。
## 软件下载
* python3.6.2 64位：[官网下载](https://www.python.org/ftp/python/3.6.2/python-3.6.2-amd64.exe)，[百度网盘下载](https://pan.baidu.com/s/1eSPCAZ4)；
* CUDA8.0：[官网下载](https://developer.nvidia.com/compute/cuda/8.0/Prod2/local_installers/cuda_8.0.61_win10-exe)，[百度网盘下载](https://pan.baidu.com/s/1dFMqRap)；
* cuDNN6.0：[百度网盘下载](https://pan.baidu.com/s/1kV3hM1h)。
## 安装流程
#### 安装python
1. 从python官网下载[python 3.6.2 64位安装文件](https://www.python.org/ftp/python/3.6.2/python-3.6.2-amd64.exe)；
2. 双击`python-3.6.2-amd64.exe`安装python和pip；
3. 将python安装路径和pip安装路径添加到系统环境变量PATH中；
4. 验证安装：打开Command Prompt，输入`python`能够看到python版本号等信息，输入`pip`能看到pip提示信息，即安装成功。
#### 安装TensorFlow
1. 在Command Prompt中输入以下命令更新pip：
```console
python -m pip install -U pip
```
2. 在Command Prompt中输入以下命令通过pip安装tensorflow-gpu：
```console
pip install tensorflow-gpu
```
#### 安装CUDA
1. 从[NVIDIA官网](https://developer.nvidia.com/cuda-downloads)下载[CUDA8](https://developer.nvidia.com/compute/cuda/8.0/Prod2/local_installers/cuda_8.0.61_win10-exe)；
2. 双击`cuda_8.0.61_win10.exe`安装；
3. 验证安装：打开Command Prompt，输入`nvcc -V`能够看到版本信息即安装成功。
#### 安装cuDNN
1. 从[NVIDIA官网](https://developer.nvidia.com/cudnn)下载cuDNN6.0压缩包（因下载时需要登录，故在此不提供官网下载链接）；
2. 解压cuDNN6.0压缩包；
3. 将解压后得到的`bin`文件夹路径添加到系统环境变量PATH中。
## 验证安装
1. 打开Command Prompt启动python：
```console
python
```
2. 输入：
```console
>>> import tensorflow as tf
>>> hello = tf.constant('Hello, TensorFlow!')
>>> sess = tf.Session()
>>> sess.run(hello)
```
3. 若是成功安装了TensorFlow，则会输出：
```console
Hello, TensorFlow!
```
