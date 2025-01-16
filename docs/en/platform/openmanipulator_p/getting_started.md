---
layout: archive
lang: en
ref: openmanipulator_p_getting_started
read_time: true
share: true
author_profile: false
permalink: /docs/en/platform/openmanipulator_p/getting_started/
sidebar:
  title: "OpenMANIPULATOR-P"
  nav: "openmanipulator_p"
product_group: openmanipulator_p
page_number: 3
---

<style>body {counter-reset: h1 2 !important;}</style>

# [Getting Started](#getting-started)

## [Safety Information](#safety-information)

- Allow sufficient workspace prior to setup by clearing objects in the arm’s vicinity.
- Always ensure the Manipulator is properly fixed to the base plate prior to operations; otherwise arm movements can cause damage and physical injury.
- Supply power to the Manipulator after making sure all cables are properly connected. While powered on do not touch the cables as it may cause erroneous operations or/and damage.
- When handling the Manipulator do so carefully as not to have your fingers stuck in the frames.
- If the Manipulator operates erroneously quickly cut off power by turning the power supply off.
- While the Manipulator is in operation keep out of its workspace; ensure no objects enter the workspace during operations.

{% capture manipulator_danger_01 %}
`DANGER`

Information appearing in a DANGER concerns the protection of personnel from the immediate and imminent hazards that, if not avoided, will result in immediate, serious personal injury or loss of life in addition to equipment damage.
- Keep away from the robot while its moving.
- Do not touch with the robot with wet hands.
- Turn off power of the robot whenever robot is problematic.
{% endcapture %}

<div class="notice--danger">{{ manipulator_danger_01 | markdownify }}</div>


{% capture manipulator_warning_01 %}
`WARNING`

Information appearing in a WARNING concerns the protection of personnel and equipment from potential hazards that can result in personal injury or loss of life in addition to equipment damage.
- Setup robot in an environment low on dust and humidity.
- The robot must always be attached to the based when powered on.
- The robot wiring must be checked prior to powering on.
- The robot connection to power supplly must be check prior to powering on.
- Do not change wiring on Robotis Manipulator while powered on.
{% endcapture %}

<div class="notice--warning">{{ manipulator_warning_01 | markdownify }}</div>

{% capture manipulator_caution_01 %}
`CAUTION`

Information appearing in a CAUTION concerns the protection of personnel and equipment, software, and data from hazards that can result in minor personal injury or equipment damage.
- Keep robot’s workspace clear of object.
- Ensure wiring is not tangled up on every joint.
- Make sure U2D2 and PC does not interfere with the robot’s moving
{% endcapture %}

<div class="notice--warning">{{ manipulator_caution_01 | markdownify }}</div>

## [Package Contents](#package-contents)

|              Item              | Quantity |
|:------------------------------:|:--------:|
|           RM-P60-RNH           |    1     |
|        Manipulator Case        |    1     |
|              U2D2              |    1     |
|    Extra cable set(4P, 2P)     |    1     |
|           4P Ext Hub           |    2     |
| Screw set (WB M2.5 and others) |    1     |

### Optional Parts

|                                              Item                                              | Quantity |
|:----------------------------------------------------------------------------------------------:|:--------:|
|                            [Gripper](/docs/en/platform/rh_p12_rna/)                            |    1     |
| [Base Plate Frame](http://www.robotis-shop-en.com/?act=shop_en.goods_view&GS=2538&GC=GD070002) |    1     |

## [Setup](#setup)

### Wiring

![](/assets/images/platform/openmanipulator_p/wiring.png)

- The diagram above illustrates joints 1~6 connected in daisy-chain (serial) configuration with 4P Cable.
- Joint 1 (labeled as “1st”) connects to U2D2 via 4P Cable.
- U2D2 connects to PC via USB hub.
- DYNAMIXEL-P is powered from a a power supply via power expansion hub.
- Joints 5 and 6 (model: PH42-020-S300-R) are not separately powered; instead power comes from the same 4P Cable.

### Power Supply
The OpenMANIPULATOR-P requires 24V for operations. Ensure the power supply is capable of supplying 24V and 15A or higher.

### Connector Information
The 4P Cable connects the OpenMANIPULATOR-P and U2D2.     
The power cable supplies power to the OpenMANIPULATOR-P.

{% include en/dxl/p/jst_485_pro_plus.md %}

### U2D2
[U2D2](/docs/en/parts/interface/u2d2/) is a small size USB communication converter that enables to control and operate DYNAMIXEL with PC. Connect the [U2D2](/docs/en/parts/interface/u2d2/) to the PC via USB hub.

![](/assets/images/platform/openmanipulator_p/u2d2.png)

### Goal Position Values with Respect to Rotation

- Goal Position value determines the rotational position of DYNAMIXEL-P.

|              Model Name              |                                                                   Relationship between angle(deg) and position value                                                                   |
|:------------------------------------:|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------:|
| PH54-200-S500-R<br />PH54-100-S500-R | -180 ~ 180 (deg) → -501923 ~ 501923<br />![](/assets/images/platform/openmanipulator_p/h54p_goal_position.png)<br />![](/assets/images/platform/openmanipulator_p/h54p_goal_angle.png) |
|           PH42-020-S300-R            | -180 ~ 180 (deg) → -303750 ~ 303750<br />![](/assets/images/platform/openmanipulator_p/h42p_goal_position.png)<br />![](/assets/images/platform/openmanipulator_p/h42p_goal_angle.png) |
