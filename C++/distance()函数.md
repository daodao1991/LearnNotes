# distance()函数

### 函数distance()用来处理两个迭代器之间的距离

#### 1.传回两个input迭代器pos1和pos2之间的距离；

#### 2.两个迭代器都必须指向同一个容器；

#### 3.对于random access迭代器，此函数仅仅只是传回pos2-pos1，因此具备常数复杂度；

#### 4.对于其他迭代器类型，distance()会不断递增pos1，直到抵达pos2为止，然后传回递增次数，也就是说其他类型的迭代器，distance()具备线性复杂度，所以对于non-random access迭代器，尽力避免使用此函数；

#### 5.如果需要更换容器型别和迭代器的型别，就应该使用distance()而不是operator-，但是存在对“non-random access迭代器”性能变差的问题，并且第一个迭代器绝对不能位于第二个迭代器之后，否则未定义行为；



## 代码示例：

### !!!可与find()结合使用，用于vector查找数据并返回索引

#### 同样需要加上头文件#include<algorithm>

```c++

#include<iostream>
#include<vector>
#include<algorithm>
#include<iterator>
 
 
using namespace std;
 
int main()
{
	vector<int> coll; 
 
	for(int i=-3;i<=9;i++)
	{
		coll.push_back(i);
	}
 
	vector<int>::iterator pos;
 
	pos=find(coll.begin(),coll.end(),5);
 
	if(pos!=coll.end())
	{
		cout<<"distance between begining and 5:"<<distance(coll.begin(),pos)<<endl;
	}
	else
	{
		cout<<"5 not found"<<endl;
	}
 
	system("pause");
	return 0;
}
```

