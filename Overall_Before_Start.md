# ROS2_UAV

要做的不是“考试型C++”，而是机器人研究型C++  
博士期间真正会天天面对的是：
* 能不能 改别人代码
* 能不能 debug
* 能不能 把一个模块接进系统
* 能不能 让程序在真实机器/仿真里跑起来

`倒着学：从“我要写什么程序”反推我需要什么 C++`
---

<mark>这是你一个月内必须吃透的：</mark>  
1. C++ 基础（工程版）   
* if / for / while
* std::vector / std::map
* struct / class
* 引用 &
* 指针（会用，不深究）
* const
* 构造函数 / 成员函数
* #include / .h + .cpp
* cmake 基本语法
❗不学模板元编程，不学奇技淫巧

---
2. ROS2 C++ 核心
这是你真正的命门：
* rclcpp::Node
* publisher / subscriber
* callback
* msg / srv
* 参数 server
* launch 文件
* colcon build
* package.xml / CMakeLists.txt
你博士第一年 80% 的痛苦都在这。

---
3. “看代码 + 改代码”的能力
比写新代码更重要：
* 会 grep / ripgrep
* 会用 gdb / printf
* 会顺着函数调用往下追
能找到「这个变量是从哪来的」

---
<mark>第 1 周：找回“手感”</mark>

目标：不怕终端、不怕编译报错  
配好 Ubuntu + ROS2

跑官方 demo

自己写：

* 一个 talker
* 一个 listener

* 每天至少 写代码 ≥ 2 小时
* 哪怕只是改变量名、加日志。

<mark>第 2 周：C++ + ROS2 结合</mark>

目标：能“写而不是抄”

写一个小节点：

订阅里程计

发布一个虚拟轨迹

理解：  
* callback 在哪
* 数据怎么流
* 手改 CMakeLists.txt（很重要）

<mark>第 3 周：贴近你未来方向</mark>  
目标：和导师方向挂钩，减轻心理压力

找一个：
* outdoor mapping
* SLAM / planning ROS2 package

不要求完全看懂  
只做一件事：
👉 加 log + 改一个参数 + 跑起来

<mark>第 4 周：工程自信建立</mark>  
目标：“我不是废物，我只是新”  
从头写一个：  

ROS2 C++ package

能：  
* build
* run
* debug

写一页笔记：

我现在会什么

我哪里还不熟

这对你进组心态非常重要。
