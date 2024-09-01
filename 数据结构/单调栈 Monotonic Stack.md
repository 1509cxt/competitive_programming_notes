# 如何入门单调栈
直接进入模板题，读题，学习题解即可。
[P5788 【模板】单调栈 - 洛谷](https://www.luogu.com.cn/problem/P5788)

或者看看[算法学习笔记(67): 单调栈 - 知乎 (zhihu.com)](https://zhuanlan.zhihu.com/p/346536592)

# 单调栈是干啥的

##   O(n) 解决数组的**NGE问题**（Next Greater Element）
给长度为n的数组a，单调栈可以离线地O(n)求出第i个元素之前（之后）第一个大于（小于、大于等于、小于等于）该元素的元素的下标f(i)。

对于“之前”的问题，这个问题甚至可以【在线】对每个元素求解。

### 实现
例：求每个数后第1个大于它的数

```cpp
stack<int> s; //栈s存的是元素的下标，越栈底 存的下标对应的元素值越大

for(int i=n-1;i>=0;i--) //从后往前看
{
	while(!s.empty() && a[s.top()] <= a[i]) s.pop();
	//弹出小于等于当前数的那些栈顶，只留下严格大于当前数的
	
	f[i]= s.empty() ? -1 : s.top();
	//存储答案，栈空的话意味着没有严格大于当前数，栈非空的话 栈顶就是第一个严格大于当前数的下标
	
	s.push(i); //存好答案再把当前元素的下标压进栈
}
```

# 练习题
## 还是模板题
[P1901 发射站 - 洛谷](https://www.luogu.com.cn/problem/P1901)

[739. 每日温度 - 力扣](https://leetcode.cn/problems/daily-temperatures/description/)

[496. 下一个更大元素 I - 力扣（LeetCode）](https://leetcode.cn/problems/next-greater-element-i/description/)

## 几乎是模板题
[503. 下一个更大元素 II - 力扣（LeetCode）](https://leetcode.cn/problems/next-greater-element-ii/description/)

[901. 股票价格跨度 - 力扣（LeetCode）](https://leetcode.cn/problems/online-stock-span/description/)

## 只会单调栈就能做的练习题
[42. 接雨水 - 力扣（LeetCode）](https://leetcode.cn/problems/trapping-rain-water/description/)

