# Numpy.random.randn()与rand()的区别

####1.numpy.random.rand()

####numpy.random.rand(d0,d1,…dn) ，以指定的形状创建一个数组，并在数组中加入在[0,1]之间均匀分布的随机样本。

![20170719094221011](C:\Users\Mr MaoDou\Desktop\20170719094221011.jpg)

#### **2.numpy.random.randn()** 

####numpy.random.rand(d0,d1,…dn) ，以指定的形状创建一个数组，数组元素符合标准正态分布N(0,1) 

####若要获得一般正态分布N(mu,sigma*2)，则可用**sigma \* np.random.randn(…) + mu**进行表示 。 ![20170719204112233](C:\Users\Mr MaoDou\Desktop\20170719204112233.jpg)

