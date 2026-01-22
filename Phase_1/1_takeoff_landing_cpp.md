在 PX4 和 QGC 完成后；  

# 创建自己的工作空间，并最终茶创建自己的 一系列自定义 程序。

1. 创建工作空间：
```bash
mkdir -p ~/dev_ws/src
cd ~/ws_test_1/src

#安装依赖
sudo apt install -y python3-pip
sudo pip3 install rosdepc
sudo rosdepc init
rosdepc update
cd .. 
rosdepc install -i --from-path src --rosdistro jazzy -y

#编译工作空间
sudo apt install python3-colcon-ros
cd ~/ws_test_1/
colcon build

# 设置环境变量，可选每次手动，或直接写入 ~/.bashrc 中。
# 手动： source install/local_setup.sh
# 自动： echo " source ~/ws_test_1/install/local_setup.sh" >> ~/.bashrc
```

---
# 针对特定功能，创建功能包
公式为： ros2 pkg create --build-type <build-type> <package_name>      

2. 这里是 takeoff_landing 功能：   
```bash
# 创建功能包
cd ~/ws_test_1/src
ros2 pkg create --build-type ament_cmake takeoff_landing_cpp

# 编译功能包
cd ~/ws_test_1/src
colcon build
source install/local_setup.bash # 还得重新再 bash 一次
```

---
