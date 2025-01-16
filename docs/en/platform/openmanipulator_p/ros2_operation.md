---
layout: archive
lang: en
ref: ros2_openmanipulator_p_ros_operation
read_time: true
share: true
author_profile: false
permalink: /docs/en/platform/openmanipulator_p/ros2_operation/
sidebar:
  title: "OpenMANIPULATOR-P"
  nav: "openmanipulator_p"
product_group: openmanipulator_p
page_number: 14
---

<style>body {counter-reset: h1 13 !important;}</style>

# [[ROS 2] Operation](#ros-operation)

## [GUI Program](#gui-program)

`GUI Program` for `ROS 2 Dashing Diademata` will be released soon!  
{: .notice}

## [Teleoperation](#teleoperation)
{% capture notice_01 %}
**NOTE**:
- The test is done on `ROS 2 Dashing Diademata` installed in `Ubuntu 18.04`.
- Make sure ROS dependencies are installed before performing these instructions. - [Install ROS 2 Packages](/docs/en/platform/openmanipulator_p/ros2_setup/#install-ros-2-packages).
- Make sure to run the [OpenMANIPULATOR-P controller](/docs/en/platform/openmanipulator_p/ros2_controller_package/#launch-controller) instructions before use of the instruction
{% endcapture %}
<div class="notice--info">{{ notice_01 | markdownify }}</div>

### [Keyboard](#keyboard)

**TIP**: Terminal can be found with the Ubuntu search icon on the top left corner of the screen. Shortcut key for Terminal is `Ctrl`+`Alt`+`t`.
{: .notice--success}

Launch `open_manipulator_p_teleop_keyboard` node for simple teleoperation test using the keyboard.  


``` bash
$ ros2 run open_manipulator_p_teleop open_manipulator_p_teleop_keyboard
```
If the node is successfully launched, the following instruction will appear in the terminal window.  

```
---------------------------------
Control Your OpenManipulator-P!
---------------------------------
w : increase x axis in task space
s : decrease x axis in task space
a : increase y axis in task space
d : decrease y axis in task space
z : increase z axis in task space
x : decrease z axis in task space

r : increase joint 1 angle
f : decrease joint 1 angle
t : increase joint 2 angle
g : decrease joint 2 angle
y : increase joint 3 angle
h : decrease joint 3 angle
u : increase joint 4 angle
j : decrease joint 4 angle
i : increase joint 5 angle
k : decrease joint 5 angle
o : increase joint 6 angle
l : decrease joint 6 angle
v : gripper open
b : gripper close
       
1 : init pose
2 : home pose
       
q to quit
-------------------------------------------------------------------------------
Present Joint Angle J1: 0.000 J2: 0.000 J3: 0.000 J4: 0.000 J5: 0.000 J6: 0.000
Present Kinematics Position X: 0.000 Y: 0.000 Z: 0.000
-------------------------------------------------------------------------------

```

### [PS4 Joystick](#ps4-joystick)

Install packages for teleoperation using PS4 joystick.

``` bash
$ sudo pip install ds4drv
```

Connect PS4 joystick to the PC via Bluetooth using the following command

``` bash
$ sudo ds4drv
```

Enter pairing mode with PS4 by pressing and holding Playstation button + share button for 10 sec. If the light on PS4 turns blue, enter the following commands in terminal and control OpenMANIPULATOR-P.

``` bash
$ ros2 run joy joy_node
$ ros2 run open_manipulator_p_teleop open_manipulator_p_teleop_joystick
```

### [XBOX 360 Joystick](#xbox-360-joystick)

Install packages for teleoperation using XBOX 360 joystick.

Connect XBOX 360 joystick to the PC with Wireless Adapter or USB cable, and launch teleoperation packages for XBOX 360 joystick.

``` bash
$ ros2 run joy joy_node
$ ros2 run open_manipulator_p_teleop open_manipulator_p_teleop_joystick
```


[OpenCR]: /docs/en/parts/controller/opencr10/
[OpenCR Manual]: /docs/en/parts/controller/opencr10/
[rc100]: /docs/en/parts/communication/rc-100/
[bt410]: /docs/en/parts/communication/bt-410/

[open_manipulator_p_msgs/GetJointPosition]: /docs/en/popup/open_manipulator_p_msgs_GetJointPosition/
[open_manipulator_p_msgs/GetKinematicsPose]: /docs/en/popup/open_manipulator_p_msgs_GetKinematicsPose/
[open_manipulator_p_msgs/SetJointPosition]: /docs/en/popup/open_manipulator_p_msgs_SetJointPosition/
[open_manipulator_p_msgs/SetKinematicsPose]: /docs/en/popup/open_manipulator_p_msgs_SetKinematicsPose/
[open_manipulator_p_msgs/SetActuatorState]: /docs/en/popup/open_manipulator_p_msgs_SetActuatorState/
[open_manipulator_p_msgs/SetDrawingTrajectory]: /docs/en/popup/open_manipulator_p_msgs_SetDrawingTrajectory/
[sensor_msgs/JointState]: /docs/en/popup/sensor_msgs_JointState_msg/
[_open_manipulator_p_msgs/KinematicsPose]: /docs/en/popup/_open_manipulator_p_msgs_KinematicsPose/
[_open_manipulator_p_msgs/OpenManipulatorState]: /docs/en/popup/_open_manipulator_p_msgs_OpenManipulatorState/
[std_msgs::String]: /docs/en/popup/std_msgs_string/
[task space]: /docs/en/popup/_open_manipulator_p_coordinates/
[joint space]: /docs/en/popup/_open_manipulator_p_coordinates/
[std_msgs/String]: /docs/en/popup/std_msgs_string/
[std_msgs/Float64]: /docs/en/popup/std_msgs_float64_msg/
[geometry_msgs/Pose]: /docs/en/popup/geometry_msgs_Pose_msg/
[robotis_controller_msgs/StatusMsg]: /docs/en/popup/StatusMsg.msg/
[manipulator_manipulation_module_msgs/JointPose]: /docs/en/popup/JointPose.msg/
[manipulator_manipulation_module_msgs/KinematicsPose]: /docs/en/popup/KinematicsPose.msg/
[manipulator_manipulation_module_msgs/GetJointPose]: /docs/en/popup/GetJointPose.srv/
[manipulator_manipulation_module_msgs/GetKinematicsPose]: /docs/en/popup/GetKinematicsPose.srv/
