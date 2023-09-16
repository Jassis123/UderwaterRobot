# Underwater Robot Design

**项目描述：** 该项目针对水下机器人的应用进行软硬件的设计与开发。

主要包括：硬件框架、软件框架和应用开发。 

个人完全负责该型机器人软件框架的设计与开发，同时负责问题排查定位与调试。

以下仅作展示，**本项目暂时不开源。**

---

## 水下机器人展示

![](Robot.png)

## 封装测试流程

![Test flow.png](photos\Test%20flow.png)

## 系统软件框架设计

- NVIDIA系列板卡作为机载电脑，处理复杂的任务，如图像识别，运动规划等。

- STM32作为底层控制器，搭载ucosiii，方便应用开发，提高多任务的实时性。

![](System.png)

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

<img title="" src="file:///F:/MiniDesktop/Myproject/UnderwaterRobot/Yolo.png" alt="Yolo.png" width="249"><img title="" src="file:///F:/MiniDesktop/Myproject/UnderwaterRobot/grasp.gif" alt="" width="344">

![视觉避障反馈.png](photos\视觉避障反馈.png)

### 基于ROS机械臂遥操作

## ![](photos\Arm.gif)

## 实战

该机器人在水池、湖泊和海洋环境中进行了测试，实际效果良好，防水、控制等性能良好。

在2022参与全国水下机器人大赛并获奖。

![](photos\Lake%20test.jpg)
