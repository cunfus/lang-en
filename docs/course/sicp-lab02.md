# sicp lab02

<!--more-->


## 问题

### Q1

- `python3 ok --local -q short-circuit -u`

开始弄错了不少，
```py
not None        -> True
True and 13     -> 13
(1 + 1) and 1   -> 1
3 and ""        -> ''
print(3) and "" -> 3 ''
"zero" and ""   -> ''
```
短路求值，俺是知道的，除此之外，在 Python 里，
- None 在布尔上下文中，被视为 False
- 字符串在布尔上下文中，被视为 True
- and 左右两侧都为 True 时，返回右侧的值（不同于 C）

### Q2

- `python3 ok --local -q hof-wwpd -u`

### Q3

- `python3 ok --local -q lambda -u`

```
>>> print_lambda = lambda z: print(z)
>>> print_lambda
? Function
-- OK! --

>>> one_thousand = print_lambda(1000)
? 1000
-- OK! --

>>> one_thousand
? 1000
-- Not quite. Try again! --

? Nothing
-- OK! --
```

### Q4

- `python3 ok --local -q composite_identity`

### Q5

- `python3 ok --local -q count_cond`

### Q6

在 [pythontutor](https://pythontutor.com/cp/composingprograms.html#mode=edit) 中验证画的环境图对不对

```py
n = 7

def f(x):
    n = 8
    return x + 1

def g(x):
    n = 9
    def h():
        return x + 1
    return h

def f(f, x):
    return f(x + n)

f = f(g, n)
g = (lambda y: y())(f)
```

没画对，`f = f(g, n)` 还好， `g = (lambda y: y())(f)` 表示定义了一个函数，接受参数 y, 执行 y()，而这个参数是上一步计算的 f。

### Q7

- `python3 ok --local -q multiple`

### Q8

- `python3 ok --local -q cycle`


## 打分

- `python3 ok --local --score`

```
Point breakdown
    Lambda the Free: 0.0/0
    The Truth Will Prevail: 0.0/0
    Higher Order Functions: 0.0/0
    count_cond: 1.0/1
    composite_identity: 1.0/1

Score:
    Total: 2.0
```

[代码](https://github.com/cunfus/course/blob/main/sicp/lab/lab02.py)
