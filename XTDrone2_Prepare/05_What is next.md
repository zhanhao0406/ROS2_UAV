# GAZEBO 和 QGC 通讯成功后，What's nest?

L1. 我怎么用程序控制飞机？   
    （发什么话题 / 发什么命令）

L2. PX4 里现在有哪些节点？各自干嘛？   
    （uORB / MAVLink / EKF / 控制器）

L3. Gazebo 里 UAV 是怎么被“拼出来”的？   
    （模型 + 传感器 + 插件）

L4. 自主导航算法要订阅 / 发布哪些话题？   
    （位姿 / 地图 / 目标点）

L5. 像 ego-planner 这种代码   
    是怎么“插进 PX4 控制链路”的？

L6. 我怎么把这整条链   
    从仿真搬到真机？

---

<details> 
<summary><mark> 所有的步骤，五个阶段，我应该按顺序怎么做？ </mark></summary>
Phase 1：最小控制闭环（你现在就该做的）

🎯 目标：

你亲手写一个程序
让飞机：解锁 → 起飞 → 悬停 → 降落

哪怕只有 50 行 Python。

你会在这一步搞清楚：

offboard 是什么

MAVLink / ROS2 是什么关系

PX4 接收的“控制量”长什么样

---
Phase 2：PX4 里到底有哪些“黑箱模块”？

🎯 目标：

你能说清楚这 5 个节点各自干嘛：

ekf2

mc_pos_control

mc_att_control

commander

mavlink

而且你知道：

谁订阅什么

谁发布什么

---
Phase 3：Gazebo 不是仿真器，而是“传感器工厂”

🎯 目标：

你知道 Gazebo：

生成了哪些传感器数据

通过什么插件喂给 PX4

你能给 UAV：

加一个 fake 相机

加一个 fake depth

改一个 IMU 噪声

---
Phase 4：ego-planner 这种东西到底干了什么？

🎯 目标：

你能用一句话概括：

ego-planner =
一个订阅位姿 + 地图，
输出期望轨迹的 ROS 节点。

然后你知道：

它发的是：

position？

velocity？

trajectory？

PX4 是通过 offboard 吃它的输出的。

---
Phase 5：你自己的算法

🎯 目标：

用你最熟的方式
（比如你之前搞 RGB-D / 轨迹分析那一套）

替换 ego-planner

保留 PX4 的控制器不动

</details> 

---

Phase 1: 
