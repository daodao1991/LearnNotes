# random模块用来生成随机数

### Python中的random模块用于生成随机数

#### 下面具体介绍random模块的功能：

###### 1.random.random()

#### #用于生成一个0到1的

#### 随机浮点数：0<= n < 1.0

```python
>>>import random
>>>random.random()
0.6847304212841228
```

###### 2.random.uniform(a,b)

#### \#用于生成一个指定范围内的随机符点数，两个参数其中一个是上限，一个是下限。如果a > b，则生成的随机数n: b <= n <= a。如果 a <b，则 a <= n <= b。

```python
>>>import random
>>>print(random.uniform(1,10))
4.117561971893286
>>>print(random.uniform(10,1))
6.175271435965824
```



###### 3.random.randint(a, b)

#### #用于生成一个指定范围内的整数.其中参数a是下限，参数b是上限，生成的随机数n: a <= n <= b

```python
>>>import random
>>>print(random.randint(1,10))
6
```

###### 4.random.randrange([start], stop[, step])

#### #从指定范围内，按指定基数递增的集合中 获取一个随机数。

#### random.randrange(10, 30, 2)，结果相当于从[10, 12, 14, 16, ... 26, 28]序列中获取一个随机数。random.randrange(10, 30, 2)在结果上与 random.choice(range(10, 30, 2) 等效。

```python
>>>import random
>>>print(random.randrange(10,30,2))
24
```

###### 5.random.choice(sequence)

#### \#参数sequence表示一个有序类型。从序列中获取一个随机元素.sequence在python不是一种特定的类型，而是泛指一系列的类型。list, tuple, 字符串都属于sequence。

```python
>>>import random
>>>lst = ['python','C','C++','javascript']
>>>str = ('python is ok')
>>>print(random.choice(lst))
o
>>>print(random.choice(str1))
C++
```



###### 6.random.shuffle(x[, random])

#### \#用于将一个列表中的元素打乱,即将列表内的元素随机排列。

```python
>>>import random
>>>lst = [1,2,3,4,5]
>>>random.shuffle(lst)  #注意改变了原来的序列，没有返回值
>>>lst
[3, 1, 5, 4, 2]
```



###### 7.random.sample(sequence, k)

#### #从指定序列中随机获取指定长度的片断并随机排列。sample函数不会修改原有序列。

```python
>>>import random 
>>>lst = [1,2,3,4,5]
>>>print(random.sample(lst,2))
[1, 4]
>>>print(lst)
[1, 2, 3, 4, 5]
```

