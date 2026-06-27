# Workflow Pipeline

## 起飞与定位
GPS / VIO / SLAM 初始化
UAV稳定悬停
定位误差收敛

## 环境感知（研究核心之一）
* wilding pine detection（目标识别）
* tree instance segmentation
* 3D reconstruction / depth estimation
* terrain + obstacle mapping

👉 这里可能涉及：
* ORB-SLAM2 / VINS-Fusion
* 深度网络检测（YOLO / segmentation）
* 点云地图

## 任务规划（核心研究点）

“锥形砍树导航”本质是：  
conical / cylindrical 3D coverage + sequential access planning  

包含：
* 从上往下（top-down access planning）
* 或从下往上（bottom-up trunk access）
* 生成一个绕树的3D轨迹（spiral / cone / layered descent/ascent）

## 局部轨迹规划 + 避障
* dynamic obstacle avoidance
* real-time replanning
* safe corridor tracking

👉 这里就是：

* MPC / optimization / sampling-based planning
* ESDF / voxel map

## 执行层（飞行控制）
* trajectory tracking
* velocity / position control
* PX4 offboard mode

## 任务闭环（砍完之后）
* tree marked as processed
* map update
* next target selection







