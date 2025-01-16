---
layout: archive
lang: kr
ref: rh_p12_rna_gazebo
read_time: true
share: true
author_profile: false
permalink: /docs/kr/platform/rh_p12_rna/gazebo/
sidebar:
  title: RH-P12-RN(A)
  nav: "rh_p12_rna"
product_group: rh_p12_rna
page_number: 3
---

<style>body {counter-reset: h1 6 !important;}</style>

# [Gazebo Simulation](gazebo-simulation)

## [Gazebo 설치](#gazebo-설치)
ROS-Gazebo 패키지를 설치.

### Gazebo with ROS
- Reference : [Gazebo Tutorials](http://gazebosim.org/tutorials?cat=connect_ros)

### RH-P12-RN 패키지 설치
RH-P12-RN(A) 의 Gazebo 패키지를 받기 위해 아래의 명령어를 입력하세요.

```
$ cd catkin_ws/src
$ git clone https://github.com/ROBOTIS-GIT/RH-P12-RN-A
```

### 추가 설치
ros-kinetic-desktop-full 로 ROS 를 설치했다면 다음 패키지들을 설치하세요.

```
$ sudo apt install ros-kinetic-ros-control
$ sudo apt install ros-kinetic-ros-controllers
$ sudo apt install ros-kinetic-gazebo-ros-control
```

## [시뮬레이터 실행](시뮬레이터-실행)
Gazebo 시뮬레이터를 설정하고 실행하는 방법

### 권장사항
Gazebo 를 제어 프로그램과 같은 PC 에서 실행할 경우 realtime factor 가 떨어질 수 있으므로, Gazebo 는 별도의 PC 를 이용할 것을 권장합니다.

### 실행 방법
Gazebo 에서 RH-P12-RN(A) 를 불러오기 위한 명령

```
$ roslaunch rh_p12_rn_a_gazebo rh_p12_rn_a_gazebo.launch
```

Gazebo 의 Play 버튼을 누르세요. 

![](/assets/images/platform/rh_p12_rn/gazebo_play_button.png)  

움직임을 확인하기 위해 터미널을 열고 아래의 명령을 입력하세요.  

- 손가락을 열린 상태로 보내는 명령

  ```
  $ rostopic pub -1 /rh_p12_rn_a/rh_p12_rn_a_position/command std_msgs/Float64 "data: 0.0"
  ```

- 손가락을 닫힌 상태로 보내는 명령

  ```
  $ rostopic pub -1 /rh_p12_rn_a/rh_p12_rn_a_position/command std_msgs/Float64 "data: 1.1"
  ```
