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
释放链表节点内存 | free(tmp); | delete tmp; | none | none | none | none
读取结构体的项 | -> | -> | . | . | . | .
逻辑与 | && | && | && | and | && | &&
空 | NULL | NULL | NULL | None | nil | nil

* C++ 中 `sizeof(array)` 是用来求对象所占内存空间的大小。

### 二维数组

C

```c
int** generateMatrix(int n, int* returnSize, int** returnColumnSizes){
    // 返回的结果数组的大小
    *returnSize = n; // 行数
    *returnColumnSizes = (int*)malloc(sizeof(int) * n); // 列数
    // 返回结果数组 res
    int** res = (int**)malloc(sizeof(int*) * n);  // n 行
    int i;
    for(i = 0; i < n; i++) {
        res[i] = (int*)malloc(sizeof(int) * n);  // 每行 n 列
        (*returnColumnSizes)[i] = n; // 每列中元素个数
    }
    ...
    return res;
}
```

C++

``` C++
class Solution {
public:
    vector<vector<int>> generateMatrix(int n) {
        vector<vector<int>> res(n, vector<int>(n, 0)); // 定义二维数组
        ...
        return res;
    }
};
```

Javascript

``` javascript
var generateMatrix = function(n) {
    let res = new Array(n).fill(0).map(() => new Array(n).fill(0));
    ...
    return res;
};
```

Python3

``` python
class Solution:
    def generateMatrix(self, n: int) -> List[List[int]]:
        nums = [[0] * n for _ in range(n)]
        ...
        return nums
```

Go

``` go
func generateMatrix(n int) [][]int {
    matrix := make([][]int, n)
    ...
    return matrix
}
```

Ruby

``` ruby
def generate_matrix(n)
    res = Array.new(n) {Array.new(n, 0)} # 创建二维数组
    ...
    res
end
```

## 记录

* 数组问题减小时间复杂度
  * 双指针(索引)
  * 创建一个新数组存储中间值，二分查找
