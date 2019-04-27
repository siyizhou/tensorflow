# tensorboard可视化，tf.summary相关
参考地址：https://www.cnblogs.com/lyc-seu/p/8647792.html <br>

tensorboard 作为一款可视化神器，可以说是学习tensorflow时模型训练以及参数可视化的法宝。<br>
而在训练过程中，主要用到了tf.summary()的各类方法，能够保存训练过程以及参数分布图并在tensorboard显示。<br>

### 相关函数：
#### 1.tf.summary.scalar：
用于展示Tensorflow中标量（scalar）监控数据随着迭代进行的变化趋势。比如：展示模型在训练batch上的正确率随着迭代进行的变化趋势。<br>

#### 2.tf.summary.histogram：
用于展示Tensorflow中张量分布监控数据随着迭代伦数的变化趋势。比如：神经网络参数取值分布随着迭代进行的变化趋势。

#### 3.tf.summary.image：
用于展示Tensorflow中使用的图片数据。这一栏一般用于可视化当前使用的训练/测试数据。

#### 4.tf.summary.audio：
用于展示Tensorflow中使用的音频数据。

