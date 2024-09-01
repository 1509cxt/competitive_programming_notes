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