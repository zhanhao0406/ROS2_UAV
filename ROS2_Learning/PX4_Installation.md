# ROS2 - PX4

* Official Web: https://docs.px4.io/main/en/ros2/user_guide

## 1. ROS 2 Install (done)
* See **System_(Re)install_Steps.md**

## 2. PX4 Install

```bash
cd
git clone https://github.com/PX4/PX4-Autopilot.git --recursive
bash ./PX4-Autopilot/Tools/setup/ubuntu.sh
# Error happend here. libgbm-dev depends version error.
# Cannot solve, the current solution is 1. install PX4, 2. then install ROS2


cd PX4-Autopilot/
make px4_sitl
```


