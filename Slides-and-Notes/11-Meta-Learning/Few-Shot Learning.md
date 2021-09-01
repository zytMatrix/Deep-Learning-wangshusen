

## 0x1、Few-Shot Learning

<img src="https://cdn.jsdelivr.net/gh/zytMatrix/images/posts/20210901104201.png" style="zoom: 50%;" />

**Few-Shot Learning** 回答的问题是给定一个Query（图片），它和**Support Set**中哪个元素（图片）相似。

## 0x2、Few-Shot Learning and Meta Learning

* Few-shot learning is a kind of meta learning
* Meta learning: learn to learn

<img src="https://cdn.jsdelivr.net/gh/zytMatrix/images/posts/20210901104519.png" style="zoom:50%;" />

**Meta Learning** 学习的是如何学习。

以上图为例子，一个小孩子去水族馆，遇见一只不认识的动物。但去水族馆之前他已经拥有的学习能力是：给定他一把动物卡片，他能从中找出和现在这只不认识动物最像的那张图片，从而知道它的名字是：水獭。

## 0x3、Supervised Learning vs. Few-Shot Learning

<img src="https://cdn.jsdelivr.net/gh/zytMatrix/images/posts/20210901105040.png" style="zoom:50%;" />

### 1. 监督学习

* 测试集中的数据在训练时并未见过，但属于训练集中数据的某一类（上图右侧测试集的哈士奇属于左侧训练集的哈士奇类）

<img src="https://cdn.jsdelivr.net/gh/zytMatrix/images/posts/20210901105305.png" style="zoom:50%;" />

### 2. Few-Shot Learning

* Query中的样本训练时从未见过，且不属于训练集中已知的类别

### 3. Support Set

<img src="https://cdn.jsdelivr.net/gh/zytMatrix/images/posts/20210901105528.png" style="zoom:50%;" />

* k-way：support集合中有k类
* n-shot：每一类有n个样本

<img src="https://cdn.jsdelivr.net/gh/zytMatrix/images/posts/20210901105717.png" style="zoom:50%;" />

如上图所示，**Support Set**中的样本一共有4类，每一类有2个样本。

<img src="https://cdn.jsdelivr.net/gh/zytMatrix/images/posts/20210901105814.png" style="zoom:50%;" />

<img src="https://cdn.jsdelivr.net/gh/zytMatrix/images/posts/20210901105903.png" style="zoom:50%;" />

如上所示，**Support Set**中类别越多，最后的精度会下降。回到之前的例子，如果小孩在在卡片集中看到的动物越多，那最终错误识别动物的概率越大。

<img src="https://cdn.jsdelivr.net/gh/zytMatrix/images/posts/20210901110057.png" style="zoom:50%;" />

<img src="https://cdn.jsdelivr.net/gh/zytMatrix/images/posts/20210901110122.png" style="zoom:50%;" />

如上所示，**Support Set**中每个类中的样本数目越多，最后的精度会越高。因为，每一类中的样本越多，可以从不同的角度反映本类的特征，有助于更好的识别。

## 0x4、 Basic Idea

<img src="https://cdn.jsdelivr.net/gh/zytMatrix/images/posts/20210901110359.png" style="zoom:50%;" />

Few-Shot Learning的主要流程：

* 从大量训练样本中学习到一个相似度函数
* 使用该相似度函数来进行预测：
    * 与query与support set中的每个样本进行比较
    * 返回相似度最高的那个样本

<img src="https://cdn.jsdelivr.net/gh/zytMatrix/images/posts/20210901110547.png" style="zoom:50%;" />

如上所以，query与support set中水獭相似度最高，所以query大概率是水獭。

## 0x5、DataSets

### Omniglot

* Official website: https://github.com/brendenlake/omniglot/
* TensorFlow: https://www.tensorflow.org/datasets/catalog/omniglot

<img src="https://cdn.jsdelivr.net/gh/zytMatrix/images/posts/20210901110745.png" style="zoom:50%;" />

### Mini-ImageNet

<img src="https://cdn.jsdelivr.net/gh/zytMatrix/images/posts/20210901110823.png" style="zoom: 38%;" />

