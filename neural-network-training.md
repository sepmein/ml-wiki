# Neural Network Training

## The Easy Fact

### 梯度下降算法 Gradient Descent

## The Hard Fact
训练前，通常需要定义许多“**超参数**”，而这些超参数定义了可能的模型搜索空间。

例如:

1. 神经网络模型架构

包括：**层数**，**每层神经元数**

2. 训练参数

包括：学习率（α, Learning Rate）， 是否使用随时间或训练步骤衰减的学习率（Learning Rate Decay）

3. 正则化

包括：是否使用L1或L2正则化，及使用时的β值；是否使用 Layer Normarlization；是否使用Dropout

4. 随机化

使用何种随机化算法来初始化模型。

### Solutions
1. Traditional

随机设置与手动搜索。

通常，在初始状态下，根据研究人员经验随即预设模型参数，随后根据模型训练结果随即或手动调整训练参数，选择最好的其中一组参数作为最终模型。

2. Traditional+

集群搜索。
在计算资源足够的情况下，随机生成多个模型，同时进行并行训练，根据训练的结果，挑选表现最好的一个模型，然后将该模型的参数作为最终模型。

优点： 实现较为简单。

缺点： 浪费大量的计算资源。对于模型较大的很难训练。

3. PBT population based training

是一种集群搜索的进化。该算法在集群搜索的基础上，集训的训练单元可以根据其他单元的训练结果调整自我参数，在某种程度上实现集群“进化”，在计算开销较小的情况下，快速找到最优设置。

https://arxiv.org/abs/1711.09846

## Thoughts
Can AI read papers?