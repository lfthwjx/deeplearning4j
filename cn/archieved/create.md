---
title: 创建深度学习网络
layout: cn-default
---

# 创建深度学习网络

## 单线程

单线程和多线程深度学习网络仅仅是指两种分配任务负担的方式，而真正的差异存在于单网络和多网络的深度学习系统之间，以及随机和非随机生成式模型之间。

单网络学习系统仅由两个层组成，结构就像[翻线戏](https://en.wikipedia.org/wiki/File:Cat's_cradle_soldier's_bed.png)一样。多网络系统则将双层网络相互连接形成很长的链条，各自相当于一个子网络。 

### 连续受限玻尔兹曼机

受限玻尔兹曼机由二进制神经元组成，这些神经元的激活状态只有零和一两种值。连续受限玻尔兹曼机可以接受十进制数。区别仅此而已。 

### 参数

### 输入

### 降噪自动编码器

自动编码器是一种用于降维的神经网络，这也就是说，它可以用于特征选择和提取。隐藏层数量多于输入的自动编码器有可能会学习[恒等函数](https://en.wikipedia.org/wiki/Identity_function)（输出直接等于输入的函数），进而变得无用。 

降噪自动编码器是基本自动编码器的一种扩展，是加入了随机因素的自动编码器。降噪自动编码器采用对输入进行随机污染（即引入噪声）的方式来减少学习恒等函数的风险，自动编码器必须将污染后的输入重构，或称降噪。 
<!---
### 参数

### 输入

### 初始化降噪自动编码器

单线程降噪自动编码器很容易设置。 

要创建编码器，只需要将[CLASS]类的对象实例化。

编码器创建代码块TK

接下来为编码器创建一个定型数据集。为了方便从视觉上理解，下列代码中包含的是一个简易的二维数据集。（大型项目的定型数据集规模显然会更大。）

定型集创建代码块TK

现在编码器已经实例化，定型数据集也已创建完毕，可以开始定型网络了。 

编码器定型代码块TK

您可以对已定型的网络输入非结构化数据并检查输出，以此来测试网络的表现。 

多线程降噪自动编码器的代码块如下：

创建编码器：

编码器创建代码块TK

创建定型数据集：

定型集创建代码块TK

编码器定型：

编码器定型代码块TK