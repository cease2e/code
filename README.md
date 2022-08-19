# code

记录一些刷过的题目

## 语言细微差异

xxx | C | C++ | JavaScript | Python | Go | Ruby |
--- | - | --- | ---------- | ------ | -- | ---- |
结尾分号 | 使用 | 使用 | 使用 | 不使用 | 不使用 | 不使用 |
获取数组长度 | sizeof(array) | array.size() | array.length | len(array) | len(array) | array.size |
定义变量 | 需指明类型 | 需指明类型 | 不需指明类型(let x = 0) | 不需指明类型 | := 直接定义 | 不需指明类型 |
向下取整 | int 自动 | int 自动 | Math.floor(x/y) | // | 自动 | 自动 |
注释 | // /**/ | // /**/ | // /**/ | # ''' """ | // /**/ | # =begin =end |
函数结尾 | 无 | 有 | 有 | 无 | 无 | 无 |
一维数组 | int* result = (int *)malloc(numsSize * sizeof(int)); | vector<int> result(nums.size(), 0); | let result = new Array(nums.length).fill(0); | result = [-1] * len(nums) | result := make([]int, n) | result = Array.new(n) |
三元运算符 | 有 | 有 | 有 | 无 | 无 | 有

* C++ 中 `sizeof(array)` 是用来求对象所占内存空间的大小。

## 记录

* 数组问题减小时间复杂度
  * 双指针(索引)
  * 创建一个新数组存储中间值，二分查找
