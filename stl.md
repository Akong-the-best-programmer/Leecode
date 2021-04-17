# 一.Vector

1.排序

```c++
include<algorithm>
sort(nums.begin(),nums.end());			   sort(nums.begin(),nums.end(),greater<int>());  //大到小
```

2.判断是否已经排序  

```c++
include<algorithm>
is_sorted(A.begin(),A.end());   //小到大
is_sorted(A.rbegin(),A.rend());  //如果A大到小，同样目的

```

3.可以自定义结构体

4.定义含n个动态向量的向量 vector<int>[n]

```c++
vector<int>[n]temp;
//将0，1，2存储到temp[1]这个向量中
for(int i=0;i<3;i++) temp[1].push_back(i); 
//访问
int a=temp[1][2];
```

5.判断两个vector是否相等

```c++
vector<int>a,b;
if(a==b) cout<<"yes!!";
```



# 二.Map

1.map的建立

```c++
#include<map>
map<int, int>temp;
map<string, int>temp2;
```

2.map插入 数值

```c++
temp.insert(pair<int,int>(1,2));
temp.insert(pair<int, int>(2, 3));
temp2.insert(pair<string, int>("syk", 2));
```

3.map的索引

```c++
//1.按照key索引，直接索引处key对应的value
cout << temp[2]；
cout << temp2["syk"];
//2.利用迭代器来索引
map<int, int>::iterator iter;
iter = temp.begin();
cout<<iter->first<<iter->second;
```

3.map的删除

```c++
temp.erase(iter);
```

4.map的查找(按照key值查找)

```c++
if (temp.find(3) != temp.end())
		cout << "find it!!" << endl;
if (temp2.find("syk") != temp2.end())
		cout << "find it too!!";
```

5.map中key对应value值的修改

```c++
temp[2]=16;  //用key索引处value后直接赋值修改
temp2["syk"]=123；
```



## 1.Map的例题

1.Leecode T350[两个数组的交集](https://leetcode-cn.com/problems/intersection-of-two-arrays-ii/solution/liang-ge-shu-zu-de-jiao-ji-ii-by-leetcode-solution/)



# 三.Queue

## 1.priority_queue

[c++优先队列(priority_queue)用法详解](https://blog.csdn.net/weixin_36888577/article/details/79937886?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522161398429416780274167292%2522%252C%2522scm%2522%253A%252220140713.130102334..%2522%257D&request_id=161398429416780274167292&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~sobaiduend~default-1-79937886.pc_search_result_hbase_insert&utm_term=priority_queue)

## 2.queue非常规用法

1.pair队列

```c++
 queue<pair<TreeNode *, int> > que;
 que.emplace(root, 1);     //只有emplace才能使pair类型入队
```



# 四.Set

## 1.Set的例题

**1.Leecode T874 [行走的机器人](https://leetcode-cn.com/problems/walking-robot-simulation/solution/mo-ni-xing-zou-ji-qi-ren-by-leetcode/)**

## 2.Set易错点

1.用unorder_set.insert(value)插入相同的值只保留一个



# 五.String

1.排序    sort(nums.begin(),nums.end());

​			   sort(nums.begin(),nums.end(),greater<char>());  //大到小

2. 比较是否相同 str1.compare(str2) //相同返回0

3.迭代器 iterator

```c++
string::iterator iter=s.begin();
```

4. s.end()所指的位置为末尾元素后面一个位置

5.string中添加元素

```c++
string s;
s+='a';
s+='c';
cout<<s;
```

