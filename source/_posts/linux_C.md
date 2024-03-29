---
title: 编译运行 C/C++
date: 2023-03-08 14:36:12
tags: [技术分享,linux,C,C++]
categories: [技术分享,linux]
---

#### 编译并运行

以下内容参考你们的那个 word 文件的[Linux 常用工具及命令](https://blog.csdn.net/sillyxue/article/details/83382909)

当没有了宇宙第一 IDE Visual Studio 后，没有万能的`ctrl + F5`，可能你甚至不会编译运行你的程序？甚至什么是编译都不知道。首先让我们来走进编译，走进编译器。
<!-- more -->
##### Gcc：编译器

linux 下程序的执行就是告诉操作系统程序文件在哪个路径下。gcc 是一个编译工具，将我们所写的 C 语言程序编程成为机器可识别的语言程序。

windows 下和 Linux 下的二进制接口不同，程序不能互相运行，因为 ABI 不同。ABI 应用程序二进制接口是一个所有处理二进制的程序（包括编译器、汇编器、链接器和语言运行库支持）都会使用的接口。

##### G++：编译器

以下内容参考自[g++的基本使用](https://blog.csdn.net/chengqiuming/article/details/88410794)。g++是 GNU 组织推出的 C++编译器。它不但可以用来编译传统的 C++程序，也可以用来编译现代 C++，比如 C++11/14 等。

g++的用法和 gcc 类似，编译 C++的时候比 gcc 更简单，因为它会自动链接到 C++标准库，而不像 gcc 需要手工指定。

g++编译程序的内部过程和 gcc 一样，也要经过 4 个阶段：预处理、编译、汇编和链接。

##### 基本语法格式

```bash
g++ [选项] 准备编译的文件 [选项] [目标文件]
```

##### 编译

```bash
g++ hello_world.cpp -o hello
```

可以看到当前目录下有一个`hello`文件，而且颜色是绿色，表示可执行文件。

##### 运行

```bash
 ./hello
```

即可看到屏幕打印出了 Hello World

![输出结果](https://tsunaou.github.io/linux_guide/images/7.png)

实际 gcc/g++的使用有更多细节，由于本教程只是一个入门教程，这里不多赘述。
