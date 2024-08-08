# sicp hw01

<!--more-->

[阅读](https://www.composingprograms.com/) 1.1～1.5 节，回答下面 4 个问题。


## 问题

### Q1
Python 的 operator 模块，包含了 add sub 作为内置算术运算符。
```python
def a_plus_abs_b(a, b): 
    """Return a+abs(b), but without calling abs.

    >>> a_plus_abs_b(2, 3)
    5
    >>> a_plus_abs_b(2, -3)
    5
    >>> a_plus_abs_b(-1, 4)
    3
    >>> a_plus_abs_b(-1, -4)
    3
    """
    if b < 0:
        f = _____
    else:
        f = _____
    return f(a, b)
```

- `python3 ok --local -q a_plus_abs_b` 测试
- `python3 ok --local -q a_plus_abs_b_syntax_check` 除填空外，没有多余的修改

一开始俺想复杂了，用了 lambda 表达式， `f = lambda a, b: a - b`，后来发现给了 `sub`，`f = sub`。

### Q2
以三个正数作为参数，返回两个最小数的平方和。函数主体仅使用一行。
```python
def two_of_three(i, j, k):
    """Return m*m + n*n, where m and n are the two smallest members of the
    positive numbers i, j, and k.

    >>> two_of_three(1, 2, 3)
    5
    >>> two_of_three(5, 3, 1)
    10
    >>> two_of_three(10, 2, 8)
    68
    >>> two_of_three(5, 5, 5)
    50
    """
    return _____
```

- `python3 ok --local -q two_of_three` 测试
- `python3 ok --local -q two_of_three_syntax_check` 格式检查，是不是只用了一行

同样，开始想复杂了，用 `max` `min` 反复去求第二小的数，思路应该是三个数平方，减去最大值的平方。
不得不说一句，函数声明下面的功能描述够清晰的啊。

### Q3
求一个整数的最大真因子（除了自身以外的因子，叫做真因子）。
```python
def largest_factor(n):
    """Return the largest factor of n that is smaller than n.

    >>> largest_factor(15) # factors are 1, 3, 5
    5
    >>> largest_factor(80) # factors are 1, 2, 4, 5, 8, 10, 16, 20, 40
    40
    >>> largest_factor(13) # factor is 1 since 13 is prime
    1
    """
    "*** YOUR CODE HERE ***"
```

- `python3 ok --local -q largest_factor`

### Q4
冰雹序列：
1. 选择一个正整数n作为开始。
2. 如果n是偶数，则除以 2。
3. 如果n是奇数，则乘以 3 并加 1。
4. 继续此过程直到n为 1。

```python
def hailstone(n):
    """Print the hailstone sequence starting at n and return its
    length.

    >>> a = hailstone(10)
    10
    5
    16
    8
    4
    2
    1
    >>> a
    7
    >>> b = hailstone(1)
    1
    >>> b
    1
    """
    "*** YOUR CODE HERE ***"
```
- `python3 ok --local -q hailstone`

## 打分

- `python3 ok --local --score`

```
Point breakdown
    a_plus_abs_b: 1.0/1
    a_plus_abs_b_syntax_check: 1.0/1
    two_of_three: 1.0/1
    two_of_three_syntax_check: 1.0/1
    largest_factor: 1.0/1
    hailstone: 1.0/1

Score:
    Total: 6.0
```

这里俺再感慨一句，这个作业评分机制，对学习者真的友善。

[代码](https://github.com/cunfus/course/blob/main/sicp/hw/hw01.py)
