# 知识点摘要
> 记录平时工作学习中的知识点,以备面试复习之用
## React知识点
## 算法
1. 冒泡排序
2. 快速排序
## 内容
### 冒泡排序
> 两层循环数组,比较当前元素和下一个元素,如果当前元素比下一个元素大,向上冒泡.

> 优化:当一次循环没有发生冒泡,说明已经排序完成,停止循环.

> ![冒泡排序](https://raw.githubusercontent.com/JakeXu/excerpts/master/images/%E5%86%92%E6%B3%A1%E6%8E%92%E5%BA%8F.gif)
##### 代码
```javascript
Array.prototype.bubble_sort = function () {
    var i, j, temp
    for (i = 0; i < this.length - 1; i++)
        for (j = 0; j < this.length - 1 - i; j++)
            if (this[j] > this[j + 1]) {
                temp = this[j]
                this[j] = this[j + 1]
                this[j + 1] = temp
            }
    return this
}
var num = [22, 34, 3, 32, 82, 55, 89, 50, 37, 5, 64, 35, 9, 70]
num.bubble_sort()
for (var i = 0; i < num.length; i++)
    document.body.innerHTML += num[i] + ' '
```
##### 复杂度
> 1. 最坏时间复杂度: O(n^2)
> 2. 最优时间复杂度: O(n)
> 3. 平均时间复杂度: O(n^2)
> 4. 最坏空间复杂度: 总共O(n)，需要辅助空间O(1)
##### 稳定性
>稳定
##### 参考
> 1. [wiki(冒泡排序)](https://zh.wikipedia.org/wiki/%E5%86%92%E6%B3%A1%E6%8E%92%E5%BA%8F)
