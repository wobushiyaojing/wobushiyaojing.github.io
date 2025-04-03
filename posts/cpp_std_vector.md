# C++ std::vector 使用指南

std::vector是C++标准模板库(STL)中最常用的容器之一，它提供了动态数组的功能。

## 基本用法

```cpp
#include <vector>
using namespace std;

// 创建vector
vector<int> nums;

// 初始化vector
vector<int> nums2 = {1, 2, 3};
```

## 常用操作

### 添加元素
```cpp
nums.push_back(10);  // 在末尾添加元素
nums.insert(nums.begin(), 5);  // 在开头插入元素
```

### 访问元素
```cpp
int first = nums[0];  // 通过下标访问
int first2 = nums.at(0);  // 使用at()方法
```

### 删除元素
```cpp
nums.pop_back();  // 删除最后一个元素
nums.erase(nums.begin());  // 删除第一个元素
```

### 其他操作
```cpp
int size = nums.size();  // 获取元素数量
bool empty = nums.empty();  // 判断是否为空
nums.clear();  // 清空vector
```

## 性能特点

- 随机访问：O(1)
- 末尾插入/删除：O(1) 平均
- 中间插入/删除：O(n)

## 最佳实践

1. 预分配空间：如果知道元素数量，使用reserve()提高性能
2. 使用emplace_back代替push_back避免临时对象
3. 遍历时尽量使用迭代器或范围for循环

[返回首页](/)
