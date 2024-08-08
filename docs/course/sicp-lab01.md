# sicp lab01
<!--more-->

先在纸上写了所有问题的伪代码，调试几次通过，就不做过多记录了。

## 问题

### Q1

- `python3 ok --local -q control -u` 理解性测试

### Q2

- `python3 ok --local -q debugging-quiz -u` 关于 debug 的理解

这里记录了 ok 评分器的 debug 用法，
```
How do you prevent the ok autograder from interpreting print statements 
as output?

Print with 'DEBUG:' at the front of the outputted line.
---
What is the best way to open an interactive terminal to investigate 
a failing test for question sum_digits?

python3 ok --local -q sum_digits -i.
```

### Q3

- `python3 ok --local -q falling`


### Q4

- `python3 ok --local -q divisible_by_k`


### Q5

- `python3 ok --local -q sum_digits`


### Q6

填写教学大纲，俺是走读生，就不用填了:)。

### Q7

- `python3 ok --local -q if-statements -u` 理解性测试

### Q8

- `python3 ok --local -q double_eights`


## 打分

- `python3 ok --local --score` 查分数

```
Point breakdown
    Control: 0.0/0
    debugging-quiz: 0.0/0
    falling: 1.0/1
    divisible_by_k: 1.0/1
    sum_digits: 1.0/1

Score:
    Total: 3.0
```

[代码](https://github.com/cunfus/course/blob/main/sicp/lab/lab01.py)
