# find()函数

```C++
template<class InputIterator, class T>

  InputIterator find ( InputIterator first, InputIterator last, const T& value )
  {
	for ( ;first!=last; first++) if ( *first==value ) break;
    return first;
  }
```



#### 返回区间[first,end)中第一个值等于value的元素的位置。

#### 如果没有找到匹配元素，则返回end。

#### 复杂度：线性复杂度。最多比较次数是：元素的总个数。

###     程序实例：

#### 下面的程序在int类型的vector中搜寻元素5和12，如果搜索到，就返回其位置,否则输出提示信息。

#### ！！注意find不属于vector的成员，而存在于算法中，应加上#include<algorithm> :

```c++
	#include <vector>
	#include <algorithm>
	#include <iostream>
 
	using namespace std;
 
	int main()
	{
		vector<int> intVec;
 
		INSERT_ELEMENTS(intVec,1,9);
 
		vector<int>::iterator pos;
		pos = find(intVec.begin(),intVec.end(),5);
 
		if(pos != intVec.end())
			cout << "The value 5 exists,and its position is " <<
			distance(intVec.begin(),pos) + 1 << endl;
		else
			cout << "The value 4 not found!" << endl;
 
		pos = find(intVec.begin(),intVec.end(),12);
 
		if(pos != intVec.end())
			cout << "The value 12 exists,and its position is " <<
			distance(intVec.begin(),pos) + 1 << endl;
		else
			cout << "The value 12 not found!" << endl;
	}
```

