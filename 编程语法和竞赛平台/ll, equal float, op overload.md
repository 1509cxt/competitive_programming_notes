# long long

```cpp
typedef long long ll;
```

![[Pasted image 20240831172559.png]]
# float equality
```cpp
double equal(double a,double b){return abs(a-b)<1e-5;}
```

# overloaded operator
```cpp
struct node{
	int w,x;
	bool operator < (const node &foo) const{return w<foo.w;} //normal <
};
```
