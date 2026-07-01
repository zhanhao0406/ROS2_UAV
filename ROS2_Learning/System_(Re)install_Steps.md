# Steps for reinstall system
Ubuntu 22.04.5 LTS, jammy;   
ROS2 Version: humble;   
Gazebo Version: harmonic (Not Gazebo(11)-Classic !!!)

### Delete previous system.
* delete the previous system under Window's disk manager.
* remove EFI "ubuntu" boot folder.

## Reinstall
* Use startup USB to install.
* Search how to allocate disk.
* install

## KeyPoints.
```bash
sudo apt update
sudo apt upgrade
```

## Graphic Card Driver.
* By default it only display: Integrated Graphics. + Code of GPU.
```bash
sudo apt install ubuntu-drivers-common
sudo apt update && sudo apt upgrade
sudo reboot now
```
```bash
lspci | grep -E 'VGA|3D controller'
ubuntu-drivers devices  #look for the recommended one.

# May face prob for this. 1. Click 'ok', create password. 
sudo apt install nvidia-driver-XXXXXXXX -y

# Reboot and prob: 2. Enroll MOK, 3. Continue, 4. Yes, 5. password, 6. Reboot.
sudo reboot now
```

```
# Check Current Graphic State
prime-select query
# on-demand : hybrid mod.

# IF WANT TO CHANGE
# sudo prime-select nvidia # GPU only "RECOMMAND"
# sudo prime-select intel  # Integrated GPU
# sudo prime-select on-demand #hybrid mode
# sudo reboot now # After Any Changes Made. 

```

* Go settings and check again.

## ROS2 Installation.
```bash
wget http://fishros.com/install -O fishros && . fishros

# Check ROS version. # echo $ROS_DISTRO
```

**ROS2 Work Environment Settings**

```bash
# 1. Tool: Git.
sudo apt install git
# Example: # git clone https://github.com/LINKSSSSSSS.git

# 2. IDE: VSCode.
# Find VSCode download (sudo dpkg -i xxxxxx)
# Then install PlugIn such as: 1. Python, 2. C/C++, 3. CMake, 4. vscode-icons, 5. ROS, 6. msg language support, 7. URDF, 8. intelli code, 9. markdown all in one, 

# 3. Tool: python3-pip
sudo apt install python3-pip
# Install ROS environment dependencies
sudo pip3 install rosdep
sudo rosdep init
rosdep update
# Then back to the working_space_root, to install required rosdeps for the work_space only.
rosdep install -i --from-path src --rosdistro humble -y

# 4. Tool: complation tool called "colcon"
sudo apt install python3-colcon-ros
# Go to workspace. then: # colcon build

# 5. Active the workspace. Soucre.
# source ~/ws/install/local_setup.sh   # one time only
# OR
# sudo gedit ~/.bashrc
# source ~/ws/install/local_setup.sh
# soucre ~/.bashrc

```

## Gazebo Sim (NEW GAZEBO) installation.
* Visit link: https://gazebosim.org/docs/harmonic/install_ubuntu/

* Ignore if there is WARNING (NO solution yet (for me)): ```libEGL warning: egl: failed to create dri2 screen```.

---

#### Chinese Language Install.
* Go settings, and find Language.
* Install
* Restart, then select Intelligent PinYin


#### Other helpful softwares
* Find Chrome download (sudo dpkg -i xxxxxx)
* Terminator software. ```sudo apt install terminator```



