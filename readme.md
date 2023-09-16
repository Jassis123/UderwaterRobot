# Underwater Robot Design

**项目描述：** 该项目针对水下机器人的应用进行软硬件的设计与开发。

主要包括：硬件框架、软件框架和应用开发。 

个人工作：个人完全负责该型机器人软件框架的设计与开发，同时负责问题排查定位与调试。

- 控制算法：编写双闭环PID控制算法；在NVIDIA上部署深度强化学习DDPG算法（Pytorch框架）。

- RTOS 开发：在 STM32F103 应用 UCOSIII，提高了多任务实时性，解决中断丢失等问题。

- 数据交互：上位机通信框架采用类 C/S 模型设计，以实现多端交互。具体建立了基于 TCP/IP 远程通信；IPC 进程间通信；另外，封装串口和摄像头设备接口，以共享资源。

- 图像处理/识别：OpenCV 图像去噪，部署 Yolov4-tiny 模型训练与检测，Fps 达 20+，反馈控制。

- 人机交互：采用 PyQT5 界面+Socket+多线程等技术编写上位机软件，实现算法参数调试、传感器数据显示和视频图像回传，同时编写游戏手柄遥操作机器人程序。

以下仅作展示，**本项目暂时不开源。**

---

## 水下机器人展示

![](photos\Robot.png)

## 封装测试流程

![Test flow.png](photos\Test%20flow.png)

## 系统软件框架设计

- NVIDIA系列板卡作为机载电脑，处理复杂的任务，如图像识别，运动规划等。

- STM32作为底层控制器，搭载ucosiii，方便应用开发，提高多任务的实时性。![](photos\System.png)

## 应用开发

### 上位机人机交互界面

- 视频传输

- 数据监控

- 急停开关

- 消息显示

- 在线参数调试

- 手柄遥操作控制

- 机械臂遥操作控制

![Interaction Interface.png](photos\Interaction%20Interface.gif)

### 基于yolov4-tiny模型训练的海产品识别

![](photos\Yolo.png)
![](photos\grasp.gif)

![视觉避障反馈.png](photos\视觉避障反馈.png)

### 基于ROS机械臂遥操作

## ![](photos\Arm.gif)

## 实战

该机器人在水池、湖泊和海洋环境中进行了测试，实际效果良好，防水、控制等性能良好。

在2022参与全国水下机器人大赛并获奖。

![](photos\Lake%20test.jpg)
