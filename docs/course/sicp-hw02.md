
# sicp hw02

<!--more-->

[阅读](https://www.composingprograms.com/) 1.6～1.7 节，回答下面 4 个问题。

## 问题

### Q1

- `python3 ok --local -q product`

### Q2

- `python3 ok --local -q accumulate`
- `python3 ok --local -q summation_using_accumulate`
- `python3 ok --local -q product_using_accumulate`

### Q3

- `python3 ok --local -q make_repeater`

### Q4

- `python3 ok --local -q digit_distance`

### Q5

- `python3 ok --local -q interleaved_sum`

花了一个小时，回过头去看 recording 中下面的基础案例，这种 A 中返回了 B，B 中再次返回了 A 的递归，它将一些值存储在了栈帧中，显得有点绕。
```py
def print_sum(x):
    print(x)
    def next_sum(y):
        return print_sum(x + y)
    return next_sum
```
再回到 `interleaved_sum` 这一题，想通就比较好写了，伪代码写完一次通过。

### Q6

- `python3 ok --local -q count_coins`

卡住了，


## 打分

- `python3 ok --local --score`

```

```

[代码]()
