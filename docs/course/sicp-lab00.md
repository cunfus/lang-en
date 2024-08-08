# sicp lab00

<!--more-->

由于俺是网上的旁听生，要使用这个 ok 自动评分器，需要加上 `--local`。
- `python ok --local -q python-basics -u` 解锁问题
- `python ok --local` 测试代码

此外，介绍了一些 Python 的命令行选项，
- `python lab00.py` 运行
- `python -i lab00.py` 交互式运行
- `python -m doctest lab00.py` 运行文件中的文档测试

doctest 的格式，在 `>>> ` 后面给出一个函数调用情况，下方是 return 的值。这个很适合用来验证算法。
```python
def twenty_twenty_four():
    """Come up with the most creative expression that evaluates to 2024
    using only numbers and the +, *, and - operators.

    >>> twenty_twenty_four()
    2024
    """
    return (1 + 2 + 3 + 4) * 5 * 6 * 7 - 8 * 9 - 4 
```
