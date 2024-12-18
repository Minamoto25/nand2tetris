# 计算机系统要素-从零开始构建现代计算机（nand2tetris）
这本书主要讲解了计算机原理（1-5章）、编译原理（6-11章）、操作系统相关知识（12章）。不要看内容这么多，其实这本书的内容非常通俗易懂，翻译也很给力。每一章背后都有对应的练习，需要你手写代码去完成，堪称理论与实践结合的经典。

这里引用一下书里的内容简介，大家可以感受一下。
>本书通过展现简单但功能强大的计算机系统之构建过程，为读者呈现了一幅完整、严格的计算机应用科学大图景。本书作者认为，理解计算机工作原理的最好方法就是亲自动手，从零开始构建计算机系统。
通过12个章节和项目来引领读者从头开始，本书逐步地构建一个基本的硬件平台和现代软件阶层体系。在这个过程中，读者能够获得关于硬件体系结构、操作系统、编程语言、编译器、数据结构、算法以及软件工程的详实知识。通过这种逐步构造的方法，本书揭示了计算机科学知识中的重要成分，并展示其它课程中所介绍的理论和应用技术如何融入这幅全局大图景当中去。
<br>全书基于“先抽象再实现”的阐述模式，每一章都介绍一个关键的硬件或软件抽象，一种实现方式以及一个实际的项目。完成这些项目所必要的计算机科学知识在本书中都有涵盖，只要求读者具备程序设计经验。本书配套的支持网站提供了书中描述的用于构建所有硬件和软件系统所必需的工具和资料，以及用于12个项目的200个测试程序。<br>
全书内容广泛、涉猎全面，适合计算机及相关专业本科生、研究生、技术开发人员、教师以及技术爱好者参考和学习。

而且，这本书的门槛非常低，只要你能熟练运用一门编程语言即可。

本书从与非门开始教你一步步构建一个完整的计算机（1-5章）；从第 6 章开始一直到第 11 章，需要完成三个编译器（汇编编译器、VM 编译器、Jack 语言编译器）；最后一章则需要完成操作系统部分功能。

如果你完成了本书所有的项目，则会获得以下成就：
* 构建出一台计算机（在模拟器上运行） 
* 实现一门语言和相应的语言标准库
* 实现一个简单的编译器

其他的编译原理书籍，在你学完后，可能还是不知道如何下手去实现一个编译器。

但这本书不一样，它是**手把手教你一步一步的实现一个编译器**。

## 其他语言版本答案
本书的第 6 - 11 章实验需要使用高级语言来实现，本仓库使用的是 JavaScript 语言。但仍然有许多开发者，他们熟悉的语言不是 JavaScript。因此，我添加了一些用其他语言实现的版本链接，方便大家学习。
* [Java](https://github.com/AllenWrong/nand2tetris)
* [C++](https://github.com/FusionBolt/The-Elements-of-Computer-Systems-Project)
* [Python](https://github.com/xrahoo/nand2tetris-python)

## 配套资料
* [全套工具下载](https://github.com/woai3c/teocs-exercises/blob/master/nand2tetris.zip)
* [本书作者制作的教学视频课程](https://www.coursera.org/learn/build-a-computer/home/welcome)
* [官网](https://www.nand2tetris.org/)

书籍请加 QQ 群 **39014053**，在群文件里下载。
### 注意
我上传的只有答案，测试用例和工具已经压缩放在仓库里，名字是 **nand2tetris.zip**，下载源码后请自行解压。

有问题欢迎提 [issues](https://github.com/woai3c/nand2tetris/issues)，也可以选择加入 QQ 交流群 **39014053**，有问题随时提问。

## 问题
* [windows 下无法打开 `.bat` 文件](https://github.com/woai3c/nand2tetris/tree/master/09)

## 内容简介
在完成所有项目后，可以跑一下软件提供的测试用例，感受一下计算机的奇妙之处：

![](https://p6-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/d040649df3bb4cd28b7b90a9f857fe4e~tplv-k3u1fbpfcp-zoom-1.image)

![](https://p9-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/e5820185fae84ac389f457d5df08f2c8~tplv-k3u1fbpfcp-zoom-1.image)

![](https://p6-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/ae42f59db6714190a9a2b8c13741d0c2~tplv-k3u1fbpfcp-zoom-1.image)

## 硬件平台

### 1.布尔逻辑
介绍了各种基础逻辑门,并且所有门都是基于nand门实现的
* and  and16
* dmux  dmux4way  dmux8way
* mux  mux16  mux4way16  mux8way16
* not  not16
* or  or16  or8way
* xor

### 2.布尔运算
* 二进制数
* 二进制加法
* 半加器
* 全加器
* 加法器
* 增量器
* ALU

### 3.时序逻辑
#### 组合芯片
* 布尔芯片
* 算术芯片

#### 时序芯片
时序芯片基于大量的DFF门
* 时钟 
* 触发器 
* 寄存器 
* 内存
* 计数器


### 4.机器语言
* A指令
* C指令
* 寻址方式：直接寻址、立即寻址、间接寻址

### 5.计算机体系结构
* 内存
* CPU
* 寄存器
* 输入输出

## 软件阶层体系
6. 汇编编译器
7. 虚拟机I：堆栈运算
8. 虚拟机II：程序控制
9. 高级语言
10. 编译器I：语法分析
11. 编译器II：代码生成
12. 操作系统

## License
MIT
## 赞助
如果你觉得本项目对你的帮助很大，可以请作者喝一杯奶茶🎁😉。

![](https://github.com/woai3c/nand2tetris/blob/master/img/wx.jpg)
![](https://github.com/woai3c/nand2tetris/blob/master/img/zfb.jpg)
