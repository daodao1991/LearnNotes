# max_element()和min_element()

#### 利用algorithm算法库里的max_element和min_element可以得到vector的最大最小值，配合distance函数可以得到最大值的位置，其结果返回的是迭代器

#### 当vector中有多个最小最大值时，位置取的是第一个

```c++
#include<vector>
#include<algorithm>
#include<iostream>
 
using namespace std;
 
int main(){
    vector<int> vec = {1,4,2,5,2,7,9,3,9};
    
    auto max = max_element(vec.begin(), vec.end());
    cout << *max << " " << distance(vec.begin(), max) << endl;
 
    auto min = min_element(vec.begin(), vec.end());
    cout << *min << " " << distance(vec.begin(), min) << endl;
 
    return 0;
}
```

#### 输出结果：

#### 9  6

#### 1  0