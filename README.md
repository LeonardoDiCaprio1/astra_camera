# 简介:camera:

用于Orbbec 3D相机的ROS驱动程序。

## 安装

这个安装包主要介绍ROS Noetic版本。

1. 鱼香ros
- 选择第一个选项一键安装安装ROS，在选择安装国内镜像源并清理第三方源，安装ROS1 Noetic版本，最后选择桌面版。
```
wget http://fishros.com/install -O fishros && . fishros 
```

2. 安装相关依赖
```
sudo apt-get update
sudo apt-get install libuvc-dev
sudo apt install ros-noetic-rgbd-launch
```
3. 操作过程
```
mkdir -p ~/astra_ws/src && cd ~/catkin_ws/
git clone https://github.com/LeonardoDiCaprio1/astra_ws_camera.git
cd ..
catkin_make
source devel/setup.bash
roscd astra_camera/
chmod 777 scripts/create_udev_rules
./scripts/create_udev_rules
sudo service udev restart
```
4.执行过程
```
cd astra_ws 
source devel/setup.bash
roslaunch astra_camera astra.launch
```
- 新建窗口
```
sudo apt update
sudo apt install ros-noetic-rqt-image-view
rqt_image_view
```
