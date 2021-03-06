---
title: 0. 也许你需要做的准备
date: 2022-03-21
---

在学习 Python 之前，你需要一个可以运行 Python 的环境，这里推荐你使用一台桌面电脑——而不是手机来学习 Python。

阅读 [附录 1：Python 的安装与环境调试](/preparation/install-python) 来安装 Python 及其所需的环境。

<!--more-->

在前言中我们提到，Python 程序是由**源代码**（`source code`）组成的，这是一种特殊的以 `.py` 结尾的文本文件，编程就是通过编辑这些源代码来实现的。

既然是文本文件，那么它其实可以使用任何你想要的编辑器来编辑，比如 Windows 记事本等，不过本指南将使用 Python 自带的 IDLE 来编辑源代码。IDLE 是 Python 所内置的开发与学习环境。

在 Windows 上，你可以通过在开始菜单中找到 Python 文件夹内的 IDLE 项来启动 IDLE，它看起来是这样的：

![开始菜单中的 IDLE](https://mapp.alicdn.com/1647766026656vaBAEvnewLGiix6.png)

点击 IDLE，你会看到 IDLE 的解释器窗口：

![IDLE 的解释器窗口](https://mapp.alicdn.com/1647766168027tEXVxxddkdyhmGv.png)

这个交互式解释器窗口主要有两大部分：上面的菜单栏和下面的 Python Shell，你可以看到 Python Shell 里已经有了一些东西，可能类似于上图中的

````Python 3.10.3 (tags/v3.10.3:a342a49, Mar 16 2022, 13:07:40) [MSC v.1929 64 bit (AMD64)] on win32
Type "help", "copyright", "credits" or "license()" for more information.```
这个是 Python Shell 的提示语，它会显示你当前的 Python 版本，编译信息等。

提示语的下方则是一个 Python Shell 的提示符：`>>>` 你可以通过在提示符后面输入任意的语句、表达式或者代码来进行测试。

如在 Python Shell 中直接输入

```python Python Shell
>>> print("Hello, world!")
````

<article class="message is-warning">
  <div class="message-body">
    注意，请关闭输入法或者全程使用英文模式，本指南的所有代码都是在关闭输入法的情况下输入的，因为 Python 代码中的中文标点会导致错误。
  </div>
</article>

此时按下回车，你会看到输出结果：

![运行结果](https://mapp.alicdn.com/1647766916267HJKf0RsGJSUF9EO.png)

这就是交互式解释器的基本功能了。

IDEL 有两种主要的窗口类型：交互式解释器窗口和编辑器窗口。其中编辑器窗口可以同时打开多个。

点击上方菜单栏的 `File` 项，你会看到下面的菜单，选择 `New File`来打开一个新的编辑器窗口：

![新建文件菜单](https://mapp.alicdn.com/1647767147148NF1wCLTn5DaXOnV.png)

![IDLE 的编辑器窗口](https://mapp.alicdn.com/1647767217768rxcCLhkvoyDgfOq.png)

你会发现，编辑器的窗口初始内容要比解释器简单的多，只有菜单栏和空空如也的编辑区域，我们之后的大部分编辑都是在这个编辑区域进行的。
在解释器中直接打开编辑器窗口，实际上是创建了一个未保存的 Python 文件，标题的 `untitled` 则表明这个文件是未保存的。

此时，如果你想保存这个文件，可以点击菜单栏的 `File` 项，然后选择 `Save`，这样你就可以保存你的文件了。（当然，如果你使用 `Ctrl + S` 快捷键保存肯定更快）

需要注意的是，这里没有解释器窗口那些 `>>>` 提示符号，因为这些符号并不是程序源代码的组成部分。解释器窗口通过这些提示符号，提示我们当前是在解释器窗口工作，并且解释器在等待你的输入。但是当我们在编辑一个独立的文件时，就不需要这些提示符号了。

这里，如果将文件保存到桌面，并命名为 `helloworld`，那么标题就会变成这个样子：

![保存文件](https://mapp.alicdn.com/1647768523169ZjqSWnMWl8P0SLr.png)

![已保存到桌面](https://mapp.alicdn.com/1647768582561YZWBlNrjJH3ONkL.png)

同时桌面也会出现一个新的 Python 文件。

你可以在编辑器窗口中编辑你的 Python 代码，然后点击菜单栏中的 `Run` - `Run Module` （或者使用快捷键 `F5`），运行你的代码。

假如我们还是输入了之前的 `helloworld`：

```python helloworld.py
print("Hello, world!")
```

> 按下 `F5` 运行代码，可能会出现一个提示：
> ![保存提示](https://mapp.alicdn.com/1647768931094n7pAYKW1txhKI0c.png)
> 意思是源代码必须保存后才能运行，问你是否要保存，选择是即可。

此时，运行结果会在之前的解释器窗口中显示：

![之前的解释器窗口](https://mapp.alicdn.com/16477693442460heQHSy8KeWRYhz.png)

如果你关闭了之前的解释器窗口，IDLE 会新建一个解释器窗口来显示运行结果，其中 `============ RESTART: C:\Users\Administrator\Desktop\helloworld.py ===========` 表示这是来自桌面的 `helloworld.py` 文件的运行结果。

如果同样输出了 `Hello, world!`，那么代表你成功了！
