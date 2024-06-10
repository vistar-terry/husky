# husky

官方 husky 源码基础上，添加了一些依赖库，不需要再安装。

感谢 husky 官方开源此项目。

官方项目链接：[https://github.com/husky/husky](https://github.com/husky/husky)

本项目链接：[https://github.com/vistar-terry/husky](https://github.com/vistar-terry/husky)

有不对的地方或其他疑问，欢迎提 [issues](https://github.com/vistar-terry/husky/issues)。



## 仓库目录说明

`HUSKY_README.md`：官方README

`README.md`：本项目README

`doc`：文档与学习笔记

`src`：源码



## 安装方法

### 1. 下载

```bash
git clone https://github.com/vistar-terry/husky.git
```

### 2. 编译

```bash
cd husky
catkin_make
```

### 3. 启动

启动一个简单的仿真界面

```bash
roslaunch husky_gazebo empty_world.launch
```

 

## husky 功能包说明

Clearpath Husky的通用ROS包，可用于模拟和真正的机器人操作：

 - husky_control : 控制配置
 - husky_description : 机器人模型
 - husky_msgs : 消息定义
 - husky_navigation : 导航配置和演示



Clearpath Husky的桌面ROS包，会引入图形化依赖

- hushy_viz：可视化（rviz）配置和bringup



Clearpath Husky的模拟器ROS包

- hushy_gazebo：gazebo对机器人的定义和扩展。



更详细见官方README：[HUSKY_README.md](./HUSKY_README.md)



## husky 依赖包

- fath_pivot_mount_description
- flir_camera_description
- interactive_marker_twist_server
- joy
- LMS1xx
- robot_localization
- teleop_twist_joy
- twist_mux
- velodyne_simulator





























