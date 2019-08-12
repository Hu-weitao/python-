# About  \_\_name\_\_



在程序中我们经常会看到：

```python
if __name__ == '__main__':
    pass
```



这条语句的作用是什么呢？ `__name__`到底表示什么呢？



`__name__` 是python中的一个魔法变量。它表示当前模块的名字。但如果当前模块是执行模块则该模块的 `__name__ = __main__`。



例如：

此时`__name__` 所在的模块为执行的模块，所以`__name__` 为 `__main__` 。

```python
manage.py

print(__name__)

---------------
输出：__main__
```



此时执行模块为`__init__.py` ，所以`__name__` 为它所在的模块名。

```python
__init__.py

import manage

--------------
输出：manage
```



所以现在我们就可以理解第一段代码的作用了。`if __name__ == '__main__'` 表示，只有当前模块为执行模块时，才执行if条件下的代码块，否则不执行。