# multi-sensor fusion and dynamic-aware autonomous navigation for fully-actuated UAVs in outdoor autonomous weed cutting mission

---
```bash
[Sensing Layer]
  RGB / stereo / IMU / GPS
        ↓
[State Estimation / Fusion]
  pose + map + uncertainty
        ↓
[Perception]
  weed / tree / obstacle geometry
        ↓
[Task-aware Planner]   ← ⭐核心论文点
  (weed cutting trajectory generation)
        ↓
[Dynamic-aware Local Planner]
  (avoid + tracking + replanning)
        ↓
[Full-actuation Controller]
```
---


## (1) multi-sensor fusion

* RGB / stereo / depth
* IMU + GPS
* possibly LiDAR

👉 目标不是SLAM本身，而是：  
为 navigation + task execution 提供可靠状态估计

---

## (2) dynamic-aware navigation

* wind / drift
* moving obstacles（人、动物、树枝）
* perception uncertainty  

👉 本质是：  
uncertainty-aware / disturbance-aware trajectory planning

---
## (3) fully-actuated UAVs

* full 6-DoF control
* lateral motion without yaw coupling
* better manipulation-like motion  

👉 这意味着：  
轨迹可以更“自由”，不是传统“前进+转向”

---
## (4) autonomous weed cutting mission

这个是 application layer：

* forestry / wilding pine / weed cutting
* structured interaction task（绕树/贴近目标）

👉 本质是：  
navigation + task execution coupled planning problem

---



