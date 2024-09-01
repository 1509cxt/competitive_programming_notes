## pair
```cpp
pair<int,int> a1{1,2}, a2{2,1};

pair<int,int> tmp;
tmp.first=1;
tmp.second=-1;

pair<int,int> b2=make_pair(1,2);
```

## sort
O(n\*log(n))
```cpp
vector< pair<int,int> > arr_pair;
sort(arr_pair.begin(),arr_pair.end());
```

# linear container
## vector
.push_back(...) O(1)
.pop_back() O(1)
.begin() O(1)
.end() O(1)
.rbegin() O(1)
.rend() O(1)
.size() O(1)
```cpp
vector<int> v[1000]; 
v[1].push_back(1);
cout<<v[1][0]<<endl;
```
### unique 去重
```cpp
std::vector<int> vec = {1, 2, 2, 3, 4, 4, 4, 5}; 
// 先排序 
std::sort(vec.begin(), vec.end()); 
// 使用 std::unique 移除重复元素 
auto new_end = std::unique(vec.begin(), vec.end()); 
// 删除多余的元素, 代码执行后vec.end()会随之改变。
vec.erase(new_end, vec.end());
```

## queue
FIFO
.push(...) O(1)
.front() O(1)
.pop() O(1)
.empty() O(1) // EMPTY ->true
.size() O(1)
```cpp
queue<int> q;
for(int i=0;i<30;++i) q.push(i);
for(int i=0;i<30;++i){
    printf("%d ",q.front());
    q.pop();
}
```

## stack
LIFO
.push(...) O(1)
.top() O(1)
.pop() O(1)
.empty() O(1) // EMPTY ->true
.size() O(1)
```cpp
stack<int> s;
for(int i=0;i<30;++i) s.push(i);
for(int i=0;i<30;++i){
    printf("%d ",s.top());
    s.pop();
}
```

## unordered_map
The algorithm inside is hash.
unordered_map<key_type, value_type>中，keytype必须是不可变的（可以是string，不可以是数组、vector），value_type随意。
.insert(pair< , > ( , ) ) O(1)
.find(...) // ... in type of key O(1) //if it doesn't exist , it returns `.end()`
.erase() O(1)
.begin() O(1)
.end() O(1)
.rbegin() O(1)
.rend() O(1)
.size() O(1)
![[Pasted image 20240901171414.png]]

## unordered_set
The algorithm inside is hash.
.insert(...) O(1)
.find(...) // ... in type of key O(1)
.erase(...) O(1)
.begin() O(1)
.end() O(1)
.rbegin() O(1)
.rend() O(1)
.size() O(1)
.empty() O(1)
![[Pasted image 20240901171559.png]]
# non-linear container
## map
The data structure inside is red-black-tree.
.insert(pair< , > ( , ) ) O(log(size))
.find(...) // ... in type of key O(log(size)) //if it doesn't exist , it returns `.end()`
.erase() O(log(size))
.begin() O(1)
.end() O(1)
.rbegin() O(1)
.rend() O(1)
.size() O(1)
.empty() O(1)

## set
The algorithm inside is red-black-tree.
.insert(...) O(log(size))
.find(...) // ... in type of key O(log(size))
.erase(...) O(log(size))
.begin() O(1)
.end() O(1)
.rbegin() O(1)
.rend() O(1)
.size() O(1)
.empty() O(1)

# lower_bound( , , )
The algorithm inside is binary search.
O(log(size))
could be used in `map`, `set` , sorted `vector`, sorted array
![[Pasted image 20240901171943.png]]

# 练习题 
[49. 字母异位词分组 - 力扣（LeetCode）](https://leetcode.cn/problems/group-anagrams/description/)

[128. 最长连续序列 - 力扣（LeetCode）](https://leetcode.cn/problems/longest-consecutive-sequence/description/?envType=study-plan-v2&envId=top-100-liked)