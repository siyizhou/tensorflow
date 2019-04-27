# 队列 tf.FIFOQueue
## 是TF队列和缓存机制的实现
参考地址1：https://blog.csdn.net/akadiao/article/details/78552037 <br>
参考地址2：https://blog.csdn.net/fegang2002/article/details/82949863 <br>
参考地址3：https://www.jianshu.com/p/d063804fb272 <br>

FIFOQueue类基于基类QueueBase．QueueBase主要包含入列（enqueue）和出列（dequeue）两个操作．enqueue操作返回计算图中的一个Operation节点，dequeue操作返回一个Tensor值．Tensor在创建时同样只是一个定义，需要放在Session中运行才能获得真正的数值

## 好处
TF实现了一个队列来支持异步操作，EnQueue可以阻塞直到队列中的空间足够；DeQueue也可以阻塞直到队列中一系列的要求得到满足。队列有两个典型应用：
1.读入数据，数据在队列中，这样可以达到数据处理和数据载入的并行<br>
2.梯度的累加，让梯度存储在队列中，直到队列中的梯度积累到一定的数值，这样可以达到多个mini-batch组成一个大的batch<br>
3.句子的聚合，对LSTM中的输入句子按长度来进行聚合，统一计算以提高效率<br>
