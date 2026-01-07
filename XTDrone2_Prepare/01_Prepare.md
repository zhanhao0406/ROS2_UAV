# 写在开始
流程为：
1. 首选传感器组合（感知模块到底怎么选，下视OpenCV + GPS粗定位 + <mark>IMU和视觉（还是）IMU和LiDAR</mark>）  
2. 优先 clone & run 现有方法，试运行demo。（XTDrone 2）  
3. Mapping显示  
4. 路径规划  
5. 飞控接口

---
参考链接：[XTDrone2](https://github.com/andy-zhuo-02/XTDrone2)   
参考文档：[语雀文档](https://www.yuque.com/xtdrone/xtdrone2/tutorial#)  

---
查看ros2 版本： `echo $ROS_DISTRO  #我的是：humble`  
查看ubuntu版本： `lsb_release -a  #我的是：Ubuntu 22.04.5 LTS，jammy`   

---
Gazebo 使用的不再是 Gazebo 9 或 11, 而是新一代 Gazebo Ignition： `sudo apt install ros-humble-ros-ign`   
教程中使用的配置为：  
|Ubuntu|仿真器|ROS发行版|PX4|
|:--|:--|:--|:--|
|Ubuntu24.04.1 LTS|Gazebo<br>Harmonic|ROS2 Jazzy|1.15.3|

我的使用配置为为老版本，需要重新装系统。  
查看 ""02_ReInstall.md""
