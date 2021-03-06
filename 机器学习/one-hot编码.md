## one-hot编码

### 什么是one-hot编码

one-hot编码，又称一位有效编码，主要是采用N位状态寄存器来对N个状态进行编码，在任意时候只有一位有效，是分类变量作为二进制向量的表示。

> one-hot编码是将类别变量转换为机器学习算法易于利用的一种形式的过程。

### 为什么要使用one-hot编码

one-hot编码进行数据的分类更准确，许多机器学习算法无法直接用于数据分类，数据的类别必须转换成数字。

### 例子1

这里有一个迷你数据集：

![](https://raw.githubusercontent.com/HurleyJames/ImageHosting/master/v2-5169c7bde2fa839aca7377a5080a5ca0_hd.jpg)

其中，类别值是分配给数据集中条目的数值编号。比如，如果我们在数据集中新加入一个公司，那么我们会给这家公司一个新类别值4。当独特的条目增加时，类别值将成比例增加。w

在上面的表格中，类别值从1开始，更符合日常生活中的习惯。实际项目中，类别值从0开始（因为大多数计算机系统计数），所以，如果有N个类别，类别值为0至N-1。

将以上数据集进行one-hot编码后，得到的表如下：

![](https://raw.githubusercontent.com/HurleyJames/ImageHosting/master/v2-e5e6c2b72a4a07b8b7e056ba68667488_hd.jpg)

### 例子2

* N=2

    例如性别特征：["男", "女"]

    男：10

    女：01

* N=3

    例如国家特征：["美国", "英国", "日本"]

    美国：100

    英国：010

    日本：001

* N=4

    例如运动特征：["游泳", "足球", "篮球", "羽毛球"]

    游泳：1000

    足球：0100

    篮球：0010

    羽毛球：0001

所以，当一个样本为["男","美国","足球"]时，完整的特征数字化结果为：

[1, 0, 1, 0, 0, 0, 1, 0, 0]











