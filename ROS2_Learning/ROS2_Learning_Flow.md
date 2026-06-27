🧩 1) ROS2 基础通信（必须掌握）

这是最核心的，你每天都会用。

✔ 必须会
① Node（C++）
创建节点
spin / executor

② Topic（pub/sub）

你至少要会：

发布：
/cmd_vel（或自定义）
/trajectory
订阅：
/odom
/imu
/pointcloud（可选）

👉 你要做到：

自己写一个 node，发控制指令 + 收状态

③ Message类型

必须熟悉：

geometry_msgs::Pose
geometry_msgs::Twist
nav_msgs::Odometry
sensor_msgs::Imu

👉 你不用背，但要：

看到就知道怎么用

---

🧠 2) 控制链路（你系统的命脉）

✔ 你必须搞懂这一条链：
Your Node → ROS2 Topic → PX4 bridge → PX4 controller → UAV
✔ 你需要掌握：
① Offboard control
setpoint publishing（位置/速度）
控制频率（>20Hz）
② 状态反馈
UAV位置（odom）
UAV姿态

👉 你要做到：

“我发一个轨迹 → 飞机真的按这个飞”

---

🧭 3) TF坐标系统（90%的人卡这里）
✔ 必须理解：
坐标系关系：
map → odom → base_link → sensor
✔ 你要会：
查 TF tree
转换坐标
知道：
轨迹在哪个坐标系？
目标点在哪个坐标系？

👉 你的任务（绕树飞）本质是：

在 map frame 生成轨迹，在 base_link 执行

---

🧪 4) Launch系统（必须会）
✔ 你要会：
启动多个 node
参数传递
namespace（可选）

👉 你的系统至少会有：

- controller node
- planner node
- perception node
- px4 bridge

---

⚙️ 5) Action（强烈建议掌握）
✔ 用在哪？

你的任务是：

“飞到树 → 绕树 → 完成 → 下一个”

这就是典型：

长时间任务控制

✔ 你要会：
定义 action
client / server

👉 举例：

Action: ExecuteSpiralTrajectory
Goal: tree_position
Feedback: progress
Result: success/failure

---

🧱 6) 参数系统（实用）
✔ 你要会：
声明参数
动态调整

👉 用在：

轨迹半径
下降速度
安全距离

---

🌍 7) 常用工具（强烈建议）
✔ 必须会用：
① RViz2
看轨迹
看点云
看TF
② rqt_graph
看系统连接
③ ros2 topic
echo / list / hz

👉 你调试90%时间都在用这些

---

🧠 8) 你“可以不急着学”的东西（帮你省时间）

这些很多教程会讲，但你现在可以跳过：

❌ lifecycle node（后期再说）
❌ component node（优化才用）
❌ DDS原理（没必要）
❌ MoveIt（机械臂专用）

🔥 最关键：你需要实现的“最小系统”

如果你把下面这个做出来，你已经超过80%的博士生初期水平：
```
✔ Minimal UAV System
[Trajectory Generator Node]  ← 你写（核心）
        ↓
[Control Node]              ← 你写
        ↓
[PX4 Offboard]
        ↓
[UAV]

+ RViz visualization
+ TF system
🎯 你当前最优执行顺序（直接照做）
```

---

* Step 1（1–2天）
写 ROS2 C++ node
发布一个固定位置 setpoint

* Step 2（2–3天）
UAV 起飞 + 悬停 + 移动

* Step 3（3–5天）
写 trajectory（circle / spiral）

* Step 4（1周）
RViz 可视化轨迹
加简单 obstacle（可选）


✅ 一句话总结

你现在只需要掌握：

ROS2 = 通信工具 + 系统组织工具

你真正的目标不是“学ROS2”，而是：

用ROS2把你的 trajectory planning 跑起来
