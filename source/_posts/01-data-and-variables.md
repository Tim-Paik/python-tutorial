---
title: 1. 数据与变量
date: 2022-03-27
---

## 1.1 对象和变量

在 Python 中，所有的数据都是以**对象**（ `object` ）的形式存在的，**每个对象都有各自的编号、类型和值**。对象是 Python 中对数据的抽象，Python 程序中所有的数据都是由对象或对象之间的关系表示的。

<!--more-->

使用对象时，我们使用**名称**（ `name` ）来指代对象。名称是通过名称绑定操作（ `name binding` ）来引入的。

```python Python Shell
x = "Hello World"
```

上面代码就是一种名称绑定操作，我们称之为**赋值**（ `assign` ），它将名称（或者叫标识符）与 `Hello World` 这个字符串对象绑定在一起。这里的 `x` 是一个名称，就是指代的对象的值为 `Hello World` 的名称。

不过在日常编程中，因为这种说法过于繁复，所以我们将绑定了对象的名称称之为**变量**（ `variable` ）。变量实质上是名称和它所绑定的对象的组合，所以我们说的“变量名”是指变量的名称，而变量的类型和值是指变量所绑定的对象的类型和值。

可以简单理解为，**变量是一种命名的，具有具体类型和值的，可变的量**。

上面的赋值语句，用变量的方式来说，就是将 `Hello World` 赋给了变量 `x`。
这时，变量 `x` 的变量名为 `x`，类型为字符串，值为 `Hello World`。

### 1.1.1 变量的命名

在前面，我们使用了赋值语句，将字符串 `Hello World` 赋给了变量 `x`。实际上这并不是最好的做法，因为我们将变量名命名为 `x` 并不能代表什么含义，代码可读性并不高。Python 社区的一个重要的共识是，代码被阅读的次数比编写的次数多，所以提高代码的可读性、一致性是很重要的。其中，变量的命名就是一个重要的部分

在 Python3 中，有效的名称（或者在语法分析中叫做标识符的东西）可以由以下字符组成：

- 大写字母 `A` 到 `Z`
- 小写字母 `a` 到 `z`
- 数字 `0` 到 `9`
- 下划线 `_`
- 其他一些 Unicode 字符（我们以后再讲）

命名变量需要遵守的规则：

- 变量名称不能以数字开头
- 变量名称不能包含空格（使用下划线代替）
- 变量名称不能使用 Python 关键字和内置函数名（或者其他 Python 用于保留用途的名称）
- 注意，Python 中的变量名是**区分大小写**的！

> Python 中的保留字，或称**关键字**如下：
>
> ```text
> False      await      else       import     pass
> None       break      except     in         raise
> True       class      finally    is         return
> and        continue   for        lambda     try
> as         def        from       nonlocal   while
> assert     del        global     not        with
> async      elif       if         or         yield
> ```

不过需要注意的是，在这里并不建议你*直接*按照上面的规则来命名变量，因为这样的变量名会比较难以理解，并且不符合 Python 的命名习惯。
我们推荐使用下面的规则和习惯来命名变量：

- 变量名应该尽可能简单，尽量不要使用过于复杂的名称
- 变量名应该尽可能有含义、有描述性，尽量不要使用无意义的名称
- 变量名应该尽量避免缩写，不要通过删除单词中的字母来进行缩写
- 变量名绝大部分时候应该使用小写字母和下划线组成
- 变量名绝大部分时候应该由小写字母开头，下划线开头的名称有其特殊含义
- 不要使用单字符来作为变量（有些时候会有例外，例如循环中的迭代器名称，后面我们会讲道）
- 不要使用拼音啦，会显得很滑稽，~~而且中国人也不会懂~~

这些名称是好的：

```text
message user_name book first_name last_name qq_number
```

这些命名是差的：

```text
m u_name Book xing ln QQhao
```

这些命名是错误的：

```
1_name _ int not None
i am a variable
```

### 1.1.2 变量的使用

在代码中使用变量时，你大部分时候可以直接把变量做是它当前代表的值：

```python Python Shell
>>> welcome_message = "Welcome to Python!"
>>> print(welcome_message)
Welcome to Python!
```

可以看到，它会输出 `Welcome to Python!`。

你可以给它赋值其他值，比如：

```python Python Shell
>>> welcome_message = "Welcome!"
>>> print(welcome_message)
Welcome!
>>> welcome_message = "Welcome to the world of Python!"
>>> print(welcome_message)
Welcome to the world of Python!
```

在第三行输入中，我们将变量重新赋值为 `Welcome to the world of Python!`（实质上是名称 `x` 被重新绑定了一个新的字符串对象），这时，它会输出 `Welcome to the world of Python!`。

这意味着**变量的值是随着赋值的操作而变化的**。在代码中调用变量的时候，变量的值取决于它最近被赋值的那个值。

很多时候，其实对象并不可变，只是名称绑定了一个新的对象而已。这也是为什么变量都“可变”的原因。

## 1.2 字面值与数据类型

前面我们说过，Python 中的所有的数据都是由对象或对象间的关系来表示的。而对象又由编号、类型和值组成。其中，对象的类型决定了对象所支持的操作与行为，并定义了这个对象可能的取值。

接下来我们将会学习常用的数据类型，以及如何使用字面值来创建这种类型的对象。

### 1.2.1 空值 None