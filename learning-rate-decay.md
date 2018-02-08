title: Learning Rate Decay
data: 2018/2/8
catogories:
- training
tags:
- underfitting
---

# Learning Rate Decay

> tensorflow version: 1.5
> last update: 2018/2/8

## 1. Definition

**学习率衰减** (Learning Rate Decay) 是指在训练模型时，随着训练的时间或者步骤的延长，逐步降低训练速率的一种算法。

在**梯度下降** (Gradient Descent) 算法中，逐步降低学习率能使模型拟合程度更高，对于一些训练出现难以拟合的情况下，可以试用该方法。

## 2. Methods

### 2.1. 指数型衰减 eponential_decay

#### math

$$\begin{aligned}
decayedLearningRate = d\alpha\\
learningRate = \alpha\\
globalStep = n\\
decaySteps = m\\
decayRate = \gamma\\
\end{aligned}$$

对于学习速度进行指数型衰减

$$
d\alpha = {\alpha}*{\gamma^{n/m}}
$$

`n`随着训练的步骤递增，衰减指数随着`n`递增而递增，学习率逐渐降低。

#### Implementation

>tf.train.exponential_decay [link](https://tensorflow.google.cn/api_docs/python/tf/train/exponential_decay)

```python
# 初始学习率
starter_learning_rate = 0.1
# global step每次训练递增1
global_step = tf.Variable(0, trainable=False)
# 衰减步数
decay_steps = 1000
# 衰减率
decay_rate = 0.9
learning_rate = tf.train.exponential_decay(
    starter_learning_rate,
    global_step,
    decay_steps,
    decay_rate,
    staircase=True)
# Passing global_step to minimize() will increment it at each step.
train = (
    tf.train.GradientDescentOptimizer(learning_rate)
    .minimize(loss, global_step=global_step)
)
```