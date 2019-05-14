[//]: # (Image References)

[image1]: ./images/sample_dog_output.png "Sample Output"
[image2]: ./images/vgg16_model.png "VGG-16 Model Keras Layers"
[image3]: ./images/vgg16_model_draw.png "VGG16 Model Figure"


## 项目概述

在这一项目中，通过创建和训练卷积神经网络模型，给定一个狗的图像，算法将会识别并估计狗的品种，如果提供的图像是人，代码将会识别最相近的狗的品种。
该项目主要通过迁移学习的方法，使用预训练的 VGG-19 模型架构作为固定的图像特征提取器，模型准确率大于70%。代码可参考'dog_app_zh.ipynb'文件.

![Sample Output][image1]


## 项目指南

### 步骤

1. 克隆存储库并打开下载的文件夹。

 ```	
git clone https://github.com/udacity/MLND_CN_P4_Dog_Project.git
cd MLND_CN_P4_Dog_Project/
```

2. 下载[狗狗数据集](https://s3.cn-north-1.amazonaws.com.cn/static-documents/nd101/v4-dataset/dogImages.zip) ，并将数据集解压大存储库中，地点为`项目路径/dogImages`. 

3. 下载[人类数据集](https://s3.cn-north-1.amazonaws.com.cn/static-documents/nd101/v4-dataset/lfw.zip)。并将数据集解压大存储库中，位置为`项目路径/lfw `。

4. 为狗狗数据集下载 [VGG-16关键特征](https://s3.cn-north-1.amazonaws.com.cn/static-documents/nd101/v4-dataset/DogVGG16Data.npz) 并将其放置于存储库中，位置为`项目路径/bottleneck_features `。

5. 安装必要的 Python 依赖包


	对于 __Mac/OSX__：
	
	```bash
	conda env create -f requirements/dog-mac.yml
	source activate dog-project
	KERAS_BACKEND=tensorflow python -c "from keras import backend"
	```

	对于 __Windows__：
	
	```bash
	conda env create -f requirements/dog-windows.yml
	activate dog-project
	set KERAS_BACKEND=tensorflow
	python -c "from keras import backend"
	```
6. 打开 notebook

 ```
jupyter notebook dog_app.ipynb
```

__注意：__ 该项目属于Udacity深度学习开源项目，部分代码已给出，剩余代码自行完成。
