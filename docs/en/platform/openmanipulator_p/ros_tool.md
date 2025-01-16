---
layout: archive
lang: en
ref: openmanipulator_p_ros_tools
read_time: true
share: true
author_profile: false
permalink: /docs/en/platform/openmanipulator_p/ros_tools/
sidebar:
  title: "OpenMANIPULATOR-P"
  nav: "openmanipulator_p"
product_group: openmanipulator_p
page_number: 8
---

<style>body {counter-reset: h1 7 !important;}</style>

# [[ROS] Tools](#ros-tools)

## [RH-P12-RN Gripper](#rh-p12-rn-gripper)

### [Parts List](#parts-list)

|                     | Part Name           | Quantity |
|:--------------------|:--------------------|:--------:|
| **Necessary Parts** | OpenMANIPULATOR-P   |    1     |
|                     | RH-P12-RN (Gripper) |    1     |
| **Chassis Parts**   | FRP42_A110K         |    1     |
| **Cables**          | CABLE_4P_180MM      |    1     |
| **Miscellaneous**   | WB_M3X08_NYLOK_K    |    12    |


![](/assets/images/platform/openmanipulator_p/open_manipulator_gripper_assembly_01.png)

### [Assembly Manual](#assembly-manual)

1. Fix FRP42_A110K to the tip of OpenMANIPUALTOR-P with eight WB_M3X08_NYLOK_K screws.
 
    ![](/assets/images/platform/openmanipulator_p/open_manipulator_gripper_assembly_02.png)

2. Assemble RH-P12-RN Gripper on fixed frame(FRP42_A110K) and tighten four WB_M3X08_NYLOK_K screws.
  
    ![](/assets/images/platform/openmanipulator_p/open_manipulator_gripper_assembly_03.png)
    
    **NOTE** : There are two more holes on the other side for screws.
    {: .notice--info}

3. Connect OpenMANIPULATOR-P and RH-P12-RN with CABLE_4P_180MM Cable.

    ![](/assets/images/platform/openmanipulator_p/open_manipulator_gripper_assembly_04.png)

### [Operation](#operation)

{% capture notice_01 %}
**NOTE** :  
- The test is done on `ROS Kinetic Kame` installed in `Ubuntu 16.04`.
- The test is done on `ROS Melodic Morenia`installed in `Ubuntu 18.04`.
- Make sure ROS dependencies are installed before performing these instructions - [Install ROS Packages](/docs/en/platform/openmanipulator_p/ros_setup/#install-ros-packages)
- Make sure to run the [OpenMANIPULATOR-P controller](/docs/en/platform/openmanipulator_p/ros_controller_package/#launch-controller) instructions before running the instruction below
{% endcapture %}
<div class="notice--info">{{ notice_01 | markdownify }}</div>

Please, open the Terminal then run **roscore** along with following command.  

```bash
$ roscore
```
 
After running **roscore**, open another Terminal then write the following commands in Terminal.  

```bash
$ roslaunch open_manipulator_p_controller open_manipulator_p_controller.launch with_gripper:=true
```

#### [GUI Program](#gui-program)

Launch `open_manipulator_p_control_gui node`. This program shows the status of and allows users to control OpenMANIPULATOR-P.

```bash
$ roslaunch open_manipulator_p_control_gui open_manipulator_p_control_gui.launch with_gripper:=true
```

To controll OpenMANIPULATOR-P with RH-P12-RN (Gripper), click the `Timer Start` button.  

![](/assets/images/platform/openmanipulator_p/open_manipulator_gripper_operation_01.png)


To activate RH-P12-RN (Gripper), Click the `Gripper open` button.


![](/assets/images/platform/openmanipulator_p/open_manipulator_gripper_operation_02.png)


- [GUI Program e-Manual](/docs/en/platform/openmanipulator_p/ros_operation/#ros-operation)  

#### [Teleoperation](#teleoperation)

**Keyboard**  

```bash
$ roslaunch open_manipulator_p_teleop open_manipulator_p_teleop_keyboard.launch with_gripper:=true
```

**PS4 & XBOX 360 Joystick**  
You can do Teleoperation with a joystic.

```bash
$ export ROS_NAMESPACE=open_manipulator_p
$ roslaunch teleop_twist_joy teleop.launch
$ roslaunch open_manipulator_p_teleop open_manipulator_p_teleop_joystick.launch with_gripper:=true
```

- [Teleoperation e-Manual](/docs/en/platform/openmanipulator_p/ros_operation/#teleoperation)

#### [MoveIt!](#moveit)

```bash 
$ roslaunch open_manipulator_p_controllers joint_trajectory_controller.launch sim:=false with_gripper:=true
```
- [MoveIt! e-Manual](/docs/en/platform/openmanipulator_p/ros_operation/#moveit)

### [Simulation](#simulation)

{% capture notice_02 %}
**NOTE** :  
- The test is done on `ROS Kinetic Kame` installed in `Ubuntu 16.04`.
- The test is done on `ROS Melodic Morenia`installed in `Ubuntu 18.04`.
- Make sure ROS dependencies are installed before performing these instructions - [Install ROS Packages](/docs/en/platform/openmanipulator_p/ros_setup/#install-ros-packages)
{% endcapture %}
<div class="notice--info">{{ notice_02 | markdownify }}</div>

#### [Launch Gazebo](#launch-gazebo)

Load OpenManipulator-PRO on Gazebo simulator

```bash
$ roslaunch open_manipulator_p_gazebo open_manipulator_p_gazebo.launch with_gripper:=true
```

- [Launch Gazebo e-Manual](/docs/en/platform/openmanipulator_p/ros_simulation/#launch-gazebo)

#### [Controller for Gazebo](#controller-for-gazebo)

Launch the open_manipulator_p_controller for gazebo simulation.

```bash
$ roslaunch open_manipulator_p_controller open_manipulator_p_controller.launch use_platform:=false with_gripper:=true
```
- [Controller for Gazebo e-Manual](/docs/en/platform/openmanipulator_p/ros_simulation/#controller-for-gazebo)
