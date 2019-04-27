# 队列 tf.FIFOQueue
参考地址：https://blog.csdn.net/akadiao/article/details/78552037

FIFOQueue类基于基类QueueBase．QueueBase主要包含入列（enqueue）和出列（dequeue）两个操作．enqueue操作返回计算图中的一个Operation节点，dequeue操作返回一个Tensor值．Tensor在创建时同样只是一个定义，需要放在Session中运行才能获得真正的数值
