# numpy.random.randn()与rand()的区别

#### 1.numpy.random.rand()

#### numpy.random.rand(d0,d1,…dn) ，以指定的形状创建一个数组，并在数组中加入在[0,1]之间均匀分布的随机样本。

```python
>>>import numpy
>>>numpy.random.rand(2,3)
array([[0.78971397, 0.88715429, 0.15207254],
       [0.49149149, 0.71052367, 0.05769726]])
```



#### 2.numpy.random.randn()

#### numpy.random.rand(d0,d1,…dn) ，以指定的形状创建一个数组，数组元素符合标准正态分布N(0,1) 

#### 若要获得一般正态分布N(mu,sigma*2)，则可用**sigma \* np.random.randn(…) + mu**进行表示 。

```python
>>>import numpy
>>>numpy.random.randn(2,3)
array([[ 1.39562871, -0.43103567, -0.75354335],
       [-1.35488738, -2.04843075, -1.59255058]])
```

