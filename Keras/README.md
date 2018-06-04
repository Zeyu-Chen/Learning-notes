# Keras Learning Notes

Author: Zeyu

### 文档:

[Keras中文文档- keras.io](https://keras.io/zh/)  
[Keras中文文档 - readthedocs.io](http://keras-cn.readthedocs.io/en/latest/)

## Keras安装（Tensorflow Backend）

Date: 2018.06.04

参考：[Keras安装和配置指南（Windows）](http://keras-cn.readthedocs.io/en/latest/for_beginners/keras_windows/)

1. Anaconda（Python 3.6, 64-Bit）
	[Download Anaconda](https://www.anaconda.com/download/)  
	[Anaconda指令](https://blog.csdn.net/fyuanfena/article/details/52080270)

2. CUDA
	目前，Tensorflow最新版仅支持CUDA 9.0，下载Windows x86_64 exe(local)版本。  
	[CUDA 9.0](https://developer.nvidia.com/cuda-90-download-archive)

3. CuDNN
	下载[CuDNN 7.0 for CUDA 9.0](https://developer.nvidia.com/rdp/cudnn-archive)  
	解压名为cuda的文件夹，将bin、include、lib内的文件复制到安装CUDA地址下的对应文件夹

4. Tensorflow
	参考：  
	[在 Windows 上安装 TensorFlow](https://www.tensorflow.org/install/install_windows)  

		# GPU版本
		pip install --upgrade tensorflow-gpu

		# CPU版本
		pip install --upgrade tensorflow

	测试：

		import tensorflow as tf
		hello = tf.constant('Hello, TensorFlow!')
		sess = tf.Session()
		print(sess.run(hello))
	
	若输出：

		Hello, TensorFlow!

	则安装成功。

5. Keras  

		pip install keras -U --pre

	测试：
  
		import keras

	若输出：
  
		Using Tensorflow backend.
		......

	则安装成功。


## Keras可视化

参考：[可视化 Visualization](https://keras.io/zh/visualization/)  
>Keras可视化函数依赖**Pydot**和**Graphviz**。

###Pydot安装

	pip install pydot
或  

	conda install pydot


###Graphviz安装（Windows）

- [Download Graphviz](http://www.graphviz.org/download/)
- 将Graphviz安装目录下的bin文件添加到环境变量
- 重启