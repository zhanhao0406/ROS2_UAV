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
