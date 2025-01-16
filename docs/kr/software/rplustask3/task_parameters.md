---
layout: archive
lang: kr
ref: task_parameters
read_time: true
share: true
author_profile: false
permalink: /docs/kr/software/rplustask3/task_parameters/
sidebar:
  title: R+ Task 3.0
  nav: "rplustask3"
product_group: rplustask3
page_number: 4
---

<style>body {counter-reset: h1 4 !important;}</style>

# [태스크 파라미터](#태스크-파라미터)

R+ Task 3.0에서 사용하는 파라미터를 설명합니다. 각 장치에 따라 사용할 수 있는 파라미터를 분류하여 설명합니다. 자세한 사용법은 각 항목의 설명과 예제 코드를 참고하세요.

## [제어기 장치](#제어기-장치)

### [주변 장치](#주변-장치)

#### [포트 닉네임](#포트-닉네임)

제어기의 주변장치 포트에 연결되는 장치의 별명을 지정할 수 있습니다.

![](/assets/images/sw/rplus_task3_kr/port_nickname_01.png)  

아래는 포트 닉네임이 적용된 예제입니다.  

![](/assets/images/sw/rplus_task3_kr/port_nickname_02.png)  
![](/assets/images/sw/rplus_task3_kr/port_nickname_03.png)

#### 감속모터
- 제어기에 연결된 감속모터를 제어하기 위해 사용합니다.
- 제어기마다 연결할 수 있는 장치가 다릅니다. 제어기 호환표를 참고하세요. [제어기 호환표]
- 방향 : CW(Clock Wise : 시계 방향), CCW(Counter Clock Wise : 반시계 방향)
- 출력 : 값 범위는 0~1023이며, 0일 때 정지, 1023일 때 100% 출력으로 설정됩니다.  
  ![](/assets/images/sw/rplus_task3_kr/task3_070.png)

- 아래는 감속 모터를 제어하는 예제입니다.  
  ![](/assets/images/sw/rplus_task3_kr/task3_071.png)

- 아래는 감속 모터를 사용하여 로봇을 전진 시키는 예제입니다.  
  ![](/assets/images/sw/rplus_task3_kr/task3_072.png)

#### 서보모터 속도/위치

- 제어기에 연결된 서보모터를 제어하기 위해 사용합니다.
- 제어기마다 연결할 수 있는 장치가 다릅니다. 제어기 호환표를 참고하세요. [제어기 호환표]
- 서보모터 동작모드 : 속도모드와 관절모드를 선택할 수 있습니다.  
  ![](/assets/images/sw/rplus_task3_kr/servo_mode_selection.png)

- 속도모드 : 서보모터의 이동속도를 설정할 수 있습니다.  
  ![](/assets/images/sw/rplus_task3_kr/task3_073.png)

- 관절모드 : 서보모터의 위치를 설정할 수 있습니다.  
  ![](/assets/images/sw/rplus_task3_kr/task3_074.png)

- 아래는 서보모터를 바퀴형태로 제어하는 예제입니다.  
  ![](/assets/images/sw/rplus_task3_kr/servo_velocity.png)

- 아래는 서보모터를 관절형태로 제어하는 예제입니다.  
  ![](/assets/images/sw/rplus_task3_kr/servo_joint.png)

- CM-550은 서보모터를 속도모드와 관절모드로 선택해서 사용할 수 있습니다. 그러므로 다른 제어기와 같이 동작모드에 속도모드 또는 관절모드를 지정해줄 필요없이 바로 사용 가능합니다.  
  ![](/assets/images/sw/rplus_task3_kr/cm550_servo_selection.png)  
  ![](/assets/images/sw/rplus_task3_kr/cm550_servo_ex.png)


#### LED 모듈

- 제어기에 연결된 LED 모듈을 제어하기 위해 사용합니다.
- 제어기마다 연결할 수 있는 장치가 다릅니다. 제어기 호환표를 참고하세요. [제어기 호환표]
- LED 모듈의 오른쪽 LED와 왼쪽 LED를 켜거나 끌 수 있습니다.  
  ![](/assets/images/sw/rplus_task3_kr/task3_077.png)

- 아래는 LED 모듈을 제어하는 예제입니다.  
  ![](/assets/images/sw/rplus_task3_kr/task3_078.png)

#### 여러가지 센서

제어기에 연결된 여러 센서를 제어하기 위해 사용합니다. 제어기마다 연결할 수 있는 장치가 다릅니다. 제어기 호환표를 참고하세요. [제어기 호환표]

##### 접촉센서
접촉센서의 접촉 여부를 읽어오기 위해 사용합니다. (True일 때 접촉됨, False일 때 접촉되지 않음)
- [접촉 센서 부품 정보]
- 아래는 접촉 센서를 사용한 예제입니다.  
  ![](/assets/images/sw/rplus_task3_kr/task3_079.png)

##### 적외선 센서
물체와의 거리를 읽어오기 위해 사용합니다. (값 범위 0 ~ 1023, 값이 0에 가까울수록 물체와의 거리가 멉니다.)
- [적외선 센서 부품 정보]
- 아래는 적외선 센서를 사용한 예제입니다.  
  ![](/assets/images/sw/rplus_task3_kr/task3_080.png)

##### 절대 거리 센서
물체와의 거리를 읽어오기 위해 사용합니다.  (값 범위 0~ 1023, 값이 0에 가까울수록 물체와의 거리가 멉니다.)
- [절대 거리 센서 부품 정보]
- 아래는 절대 거리 센서를 사용한 예제입니다.  
  ![](/assets/images/sw/rplus_task3_kr/task3_081.png)

##### 컬러 센서
물체의 색상을 읽어오기 위해 사용합니다.
- 컬러 센서가 감지하는 색은 아래와 같습니다.  
  ![](/assets/images/sw/rplus_task3_kr/task3_082.png)

- [컬러 센서 부품 정보]
- 아래는 컬러 센서를 사용한 예제입니다.  
  ![](/assets/images/sw/rplus_task3_kr/task3_083.png)

##### 자석 센서
자석이나 물체의 자력을 읽어오기 위해 사용합니다. (True일 때 자석이 감지됨, False일 때 자석이 감지되지 않음)
- [자석 센서 부품 정보]
- 아래는 자석 센서를 사용한 예제입니다.  
  ![](/assets/images/sw/rplus_task3_kr/task3_084.png)

##### 온도 센서
물체의 온도를 읽어오기 위해 사용합니다. (온도 범위 : -20~120&deg;C)
- [온도 센서 부품 정보]
- 아래는 온도 센서를 사용한 예제입니다.  
  ![](/assets/images/sw/rplus_task3_kr/task3_085.png)

##### 동작감지 센서
물체의 움직임을 감지하기 위해 사용합니다.
- [동작감지 센서 부품 정보]
- 아래는 동작감지 센서를 사용한 예제입니다.  
  ![](/assets/images/sw/rplus_task3_kr/task3_086.png)

##### 온습도 센서
물체의 온도와 습도를 읽어오기 위해 사용합니다. (온도 범위 : -20~120&deg;C, 습도 범위 : 0~100%)
- [온습도 센서 부품 정보]
- 아래는 온습도 센서를 사용한 예제입니다.

  ![](/assets/images/sw/rplus_task3_kr/task3_087.png)

##### 조도 센서
장소의 밝기를 감지하기 위해 사용합니다. (값 범위 0~ 1023, 값이 0에 가까울수록 주위가 어둡습니다.)
- [조도 센서 부품 정보]
- 아래는 조도 센서를 사용한 예제입니다.  
  ![](/assets/images/sw/rplus_task3_kr/task3_088.png)

##### 사용자 장치
사용자가 제작한 센서의 값을 읽어오거나 쓸 때 사용합니다.
- [사용자 센서 제작]
- 아래는 사용자 장치를 사용한 예제입니다.  
  ![](/assets/images/sw/rplus_task3_kr/task3_089.png)

### [모션 제어](#모션-제어)
제어기에 다운로드된 모션을 실행하기 위한 파라미터입니다.
- 특정 제어기에서만 사용할 수 있습니다.  
  (지원 제어기 : [CM-200], [CM-5], [CM-510], [CM-530], [CM-550], [CM-700], [OpenCM 9.04])

#### 모션 호출 번호
해당 호출 번호의 모션이 실행됩니다.
- 모션 호출 번호에 지정된 이름을 확인할수 있습니다.
- 모션이 실행되는 도중이라면 현재 실행 중인 모션 번호를 읽어올 수 있습니다.  
  ![](/assets/images/sw/rplus_task3_kr/motion_control_namelist.png)  
- 아래는 모션 호출 번호를 이용한 예제입니다.  
  ![](/assets/images/sw/rplus_task3_kr/task3_090.png)  
  - 모션 호출 번호가 **0** 일 경우, 모션 정지 유닛을 실행하여 모션을 정지합니다.  
  - 모션 호출 번호가 **-1** 일 경우, 현재 유닛에서 모션을 정지합니다.
  - 모션 호출 번호가 **-2** 일 경우, 실행중인 키-프레임에서 모션을 정지합니다.  ([CM-550] 지원.)  
  - 모션 호출 번호가 **-3** 일 경우, 즉각 모션을 정지합니다. ([CM-550] 지원.)  

키프레임, 모션유닛, 모션에 대한 정보는 [모션 프로그래밍](/docs/kr/software/rplustask3/motion_programming/#모션-프로그래밍)을 참조하세요.
{: .notice}

#### 모션 연결

현재 모션 이후, 실행될 모션을 지정합니다. 현재 모션과 다음 실행 모션을 자연스럽게 연결할 수 있습니다.

![Motion_Link](/assets/images/sw/rplus_task3_kr/Motion_Next_Page_kr.png)

#### 모션 상태
모션이 실행되고 있으면 True, 모션이 실행되고 있지 않으면 False값을 반환합니다.
- 아래는 모션 상태를 이용하여 모션이 종료될 때까지 대기하는 예제입니다.  
  ![](/assets/images/sw/rplus_task3_kr/task3_091.png)

#### 관절 오프셋
모션이 실행될 때 -255~255 값을 모든 관절에 더해줍니다.  
관절 오프셋이 -50이고 모션 데이터의 위치 값이 300 -> 400 -> 500으로 설정된 경우라면, 250 -> 350 -> 450으로 변경되어 실행됩니다.
- 아래는 특정 관절에 오프셋 값을 적용하는 예제입니다.  
  ![](/assets/images/sw/rplus_task3_kr/task3_092.png)

- 아래는 특정 관절에 모션 데이터 값의 영향을 받지 않도록 설정하는 예제입니다.  
  ![](/assets/images/sw/rplus_task3_kr/task3_093.png)

#### 관절 LED 자동 켜기
모션이 실행되는 동안 다이나믹셀의 LED를 켜거나 끌 수 있습니다. (True일 때 RGB LED 사용, False일 때 RGB LED 사용안함)  
해당 기능은 OpenCM 9.04에서만 지원합니다.
- 아래는 모션 실행 시 “관절 LED 자동 켜기” 기능을 활용하는 예제입니다.  
  ![](/assets/images/sw/rplus_task3_kr/task3_094.png)

- 아래는 제어기에 저장된 모션을 실행하는 예제입니다. 리모컨 버튼 눌림에 따라 해당하는 모션이 실행됩니다.  
  ![](/assets/images/sw/rplus_task3_kr/task3_095.png)

### [내장 센서](#내장-센서)
제어기에 내장된 각종 센서를 사용할 수 있습니다.

#### 시작 버튼 눌림 횟수
최초 제어기를 켤 때 연속적으로 시작버튼을 누른 횟수를 읽어올 때 사용합니다. 시작 버튼 눌림 횟수의 값의 범위는 0 ~ 255 입니다.
- 지원 제어기 : [CM-5], [CM-50], [CM-100A], [CM-150], [CM-200], [CM-510], [CM-530], [CM-700], [OpenCM 7.0], [OpenCM 9.04]
- 아래는 시작 버튼 눌림 횟수를 사용하는 예제입니다.  
  ![](/assets/images/sw/rplus_task3_kr/task3_099.png)

#### 제어기 버튼 / 버튼
제어기의 버튼 상태를 읽어올 때 사용합니다. 제어기에 따라 사용할 수 있는 버튼이 달라집니다.
- 지원 제어기 : [CM-5], [CM-50], [CM-100A], [CM-150], [CM-200], [CM-510], [CM-530], [CM-700], [OpenCM 7.0], [OpenCM 9.04]
- 아래는 CM-5, CM-510, CM-530 제어기의 버튼을 사용하는 예제입니다.  
  ![](/assets/images/sw/rplus_task3_kr/task3_100.png)

- 아래는 OpenCM9.04의 버튼을 사용하는 예제입니다.  
  ![](/assets/images/sw/rplus_task3_kr/task3_101.png)

#### 컨트롤러 버튼 릴리즈 이벤트
CM-550 제어기의 시작버튼이 눌렸다가 떨어질 때 1(True)이 되며, 값을 읽으면 0(False)으로 리셋됩니다.

#### 버튼 눌림 시간
CM-550 제어기의 버튼을 누르고 있으면 버튼 눌림 시간이 ms 단위로 증가합니다.

#### 버튼 눌림 1초 타이머
CM-550 제어기의 버튼을 누르고 있으면 버튼 눌림 시간이 1초 단위로 증가합니다.

#### 최종 소리 감지 횟수
제어기에 내장된 마이크를 사용하여 일정 수준 이상의 큰 소리가 날 경우 1회씩 카운트하는 기능입니다. 대표적인 예로 박수 소리를 카운트하여 로봇을 동작시킬 때 많이 사용합니다.  
감지된 소리 횟수를 누적하여 카운트합니다. 초기화가 필요한 경우 0값을 직접 입력해야 합니다.  
제어기마다 지원하는 센서의 종류가 다릅니다. 각 제어기의 매뉴얼을 참고하세요.
- 지원 제어기 : [CM-5], [CM-50], [CM-100A], [CM-150], [CM-200], [CM-510], [CM-530], [CM-550], [CM-700], [OpenCM 7.0], [OpenCM 9.04]
- 아래는 최종 소리감지 횟수를 이용한 예제입니다.  
  ![](/assets/images/sw/rplus_task3_kr/task3_096.png)

#### 실시간 소리 감지 횟수
제어기에 내장된 마이크를 사용하여 일정 수준 이상의 큰 소리가 날 경우 1회씩 카운트하는 기능입니다. 대표적인 예로 박수 소리를 카운트하여 로봇을 동작시킬 때 많이 사용합니다.  
실시간으로 감지된 소리 횟수를 카운트합니다. 0.8초간 소리가 입력되지 않으면 0으로 초기화 됩니다.
- 아래는 실시간 소리감지 횟수를 이용한 예제입니다.  
  ![](/assets/images/sw/rplus_task3_kr/task3_097.png)

#### 적외선 센서
- 제어기에 내장된 적외선 센서 값을 읽어오기 위해 사용합니다.
- 적외선 센서의 값 범위는 0 ~ 1,023 입니다. 물체와의 거리가 가까울수록 큰 값을 가지며, 거리가 멀수록 작은 값을 가집니다.
- 제어기마다 내장된 센서의 종류가 다릅니다. 각 제어기의 매뉴얼을 참고하세요.
  - 지원 제어기 : [CM-5], [CM-50], [CM-100A], [CM-150], [CM-200]

- 아래는 제어기의 적외선 센서 값을 사용하는 예제입니다.  
  ![](/assets/images/sw/rplus_task3_kr/task3_098.png)

##### 왼쪽 적외선 센서
제어기 왼쪽 하단에 위치한 적외선 센서의 값을 읽어올 때 사용합니다.

##### 중앙 적외선 센서
제어기 전면 중앙에 위치한 적외선 센서의 값을 읽어올 때 사용합니다.

##### 오른쪽 적외선 센서
제어기 오른쪽 하단에 위치한 적외선 센서의 값을 읽어올 때 사용합니다.

#### 현재 입력 전압
제어기에 입력되는 전압을 읽어오기 위해 사용합니다.

#### 제어기 온도
CM-550 제어기의 현재 온도를 측정하기 위해 사용합니다.

#### 제어기 IMU 방향
CM-550 제어기의 장착 상태에 따라 제어기에 내장된 IMU 센서의 방향을 설정해 주어야 합니다.
제어기를 세워서 사용하거나 눕혀서 사용할 경우에 따라 아래와 같이 설정합니다.

|   제어기 장착 상태   | 설정값 |
|:--------------------:|:------:|
| 수직으로 세워서 장착 |   0    |
| 수평으로 눕혀서 장착 |   1    |

#### Roll X / Pitch Y / Yaw Z
CM-550 제어기에 내장된 IMU 센서의 Roll / Pitch / Yaw 축 데이터를 읽어올 때 사용합니다. (단위 : 0.01&deg;)

#### Gyro X / Y / Z
CM-550 제어기에 내장된 IMU 센서의 자이로 X / Y / Z 축 데이터를 읽어올 때 사용합니다. (단위 : 0.01&deg;/s)

#### Accel X / Y / Z
CM-550 제어기에 내장된 IMU 센서의 가속도계 X / Y / Z 축 데이터를 읽어올 때 사용합니다. (단위 : 0.001G)

### [버저](#버저)

#### 버저 종류 / 버저 울림 시간

- 제어기에 내장된 버저를 통해 음계나 멜로디를 연주할 때 사용합니다.
- 버저 울림 시간을 먼저 설정한 후 버저 종류를 설정해야 설정에 맞게 소리가 납니다.
- 아래는 버저 종류를 설정하는 그림입니다.  
  ![](/assets/images/sw/rplus_task3_kr/task3_102.png)

- 아래는 제어기의 음계를 연주하는 예제입니다. 음계 연주 시 “버저 울림 시간”을 0~5초로 설정할 수 있습니다.  
  ![](/assets/images/sw/rplus_task3_kr/task3_103.png)

- 아래는 제어기의 멜로디를 연주하는 예제입니다. 멜로디 연주 시 “버저 울림 시간”을 멜로디 연주 시간(특수 멜로디 연주)으로 설정해야 합니다.  
  ![](/assets/images/sw/rplus_task3_kr/task3_104.png)

### [리모컨](#리모컨)

#### 받은 무선 데이터, 보낼 무선 데이터 / 무선 ID / RC-100채널

- 제어기에 연결된 무선 통신 모듈(블루투스, 적외선, 지그비)을 통해 외부와 데이터를 주고 받는 파라미터입니다.
- 일반적으로 RC-100, 스마트폰 가상 리모컨으로 로봇을 조종할 때 사용되며, 그 외에 사용자가 만든 임의의 SW와 통신을 위해 사용될 수 있습니다.
- 주고 받는 데이터의 값 범위는 0~65535로 제한됩니다. (2bytes)
- 받은 무선 데이터 : 제어기가 외부로부터 데이터를 전달받을 때 사용합니다.  
  ![](/assets/images/sw/rplus_task3_kr/task3_105.png)

##### 보낼 무선 데이터
제어기가 외부로 데이터를 내보낼 때 사용합니다.  
![](/assets/images/sw/rplus_task3_kr/task3_106.png)

##### 새 무선 데이터 도착
제어기에 외부로부터 데이터가 전달되었을 때 값이 True가 됩니다.  
![](/assets/images/sw/rplus_task3_kr/task3_107.png)

##### 내 로봇 무선 ID
지그비를 사용할 때 지그비 ID를 확인합니다.  
![](/assets/images/sw/rplus_task3_kr/task3_108.png)

##### 상대로봇 무선 ID
지그비를 사용할 때 패어링할 지그비의 ID를 설정합니다.  
![](/assets/images/sw/rplus_task3_kr/task3_109.png)

##### RC-100 채널
적외선 수신기를 사용할 때 채널 값을 설정합니다. (값이 255일경우 블루투스/지그비 모드로 동작합니다.)  
![](/assets/images/sw/rplus_task3_kr/task3_110.png)

- 아래는 제어기에서 받은 무선 데이터를 처리하는 예제입니다.
  
  ![](/assets/images/sw/rplus_task3_kr/task3_111.png)

- 아래는 제어기가 외부로 데이터를 내보내는 예제입니다.
  
  ![](/assets/images/sw/rplus_task3_kr/task3_112.png)


### [타이머](#타이머)
- 타이머와 정밀 타이머는 제어기에 자동으로 카운트 다운 되는 타이머의 값을 설정할 때 사용합니다.

#### 타이머
제어기에 자동으로 카운트 다운 되는 타이머의 값을 사용할 때 설정합니다. 타이머의 값 범위는 0~255이며, 단위는 0.128초 입니다.  
- 아래는 타이머를 사용하여 약 1초(1.024초)만큼 대기하는 예제입니다.

  ![](/assets/images/sw/rplus_task3_kr/task3_113.png)

#### 정밀 타이머
타이머와 같은 기능을 하며 시간을 더 정밀하게 카운트 합니다. 정밀 타이머의 값 범위는 0 ~ 65,535이며, 단위는 0.001초 입니다.  
- 아래는 정밀 타이머를 사용하여 정확히 1초(1.000초)만큼 대기하는 예제입니다.
 
  ![](/assets/images/sw/rplus_task3_kr/task3_114.png)

#### 딜레이
CM-550에서는 타이머와 조건대기가 결합된 딜레이 기능을 사용할수 있습니다.  
![](/assets/images/sw/rplus_task3_kr/cm550_delay_01.png)  
![](/assets/images/sw/rplus_task3_kr/cm550_delay_02.png)  

- 아래 태스크 코드 중 우측의 코드는 CM-550에서 딜레이를 간단하게 사용할 수 있는 예시입니다.  
  ![](/assets/images/sw/rplus_task3_kr/cm550_delay_03.png)

#### 자동꺼짐 타이머
제어기의 절전 모드 기능을 사용할 때 설정합니다.
- '자동꺼짐 타이머'의 실제 값은 0 ~ 255 사이의 숫자를 사용합니다.
- 숫자 1 은 시간 값 1분을 의미합니다.
- 제어기 작동 시 '자동꺼짐 타이머'의 기본 설정 값은 5분 입니다.
- 대부분의 제어기에서 자동꺼짐 타이머 값을 0분으로 설정하면 자동꺼짐 기능이 동작하지 않습니다 (OpenCM7.0은 60분으로 설정됨).
- 자동꺼짐 타이머의 남은 시간은 항상 '분' 단위로 읽혀집니다. 즉, 50초가 남아 있어도 1분으로 읽혀집니다.
- 자동꺼짐 타이머의 설정은 아래 표와 같으며, 타이머를 사용하지 않는 경우 배터리가 방전될 위험이 있으니 주의하시기 바랍니다.

|  설정값  |       OpenCM7.0의 타이머 시간       |      기타 제어기의 타이머 시간      |
|:--------:|:-----------------------------------:|:-----------------------------------:|
|    0     |                60분                 | 타이머 사용안함(배터리 방전에 주의) |
|  1 ∼ 60  |              1 ∼ 60분               |              1 ∼ 60분               |
| 61 ∼ 254 |                60분                 |              61 ∼254분              |
|   255    | 타이머 사용안함(배터리 방전에 주의) |                255분                |

**주의**: OpenCM7.0은 설정값이 다르므로 주의하시기 바랍니다.
{: .notice--warning}

- 아래는 자동꺼짐 타이머를 이용하여 제어기의 절전 모드를 설정하는 예제입니다. 5분내에 새 무선 데이터가 도착하면 자동꺼짐 타이머 값을 다시 초기화합니다.

  ![](/assets/images/sw/rplus_task3_kr/task3_115.png)


### [제어기: 기타](#제어기-기타)

#### 임의의 숫자
0 ~ 255 범위에서 임의의 숫자(Random Value)를 생성합니다.  
값을 설정하여 최대값의 범위를 조절할 수 있습니다.
- 아래는 임의의 숫자를 사용하여 임의의 모션을 실행하는 예제입니다. 0 ~ 15까지의 임의의 숫자를 생성하여 해당 모션을 실행합니다.  
  ![](/assets/images/sw/rplus_task3_kr/task3_116.png)

#### 내장 LED
제어기의 내장 LED(Aux LED)를 제어하기 위해 사용합니다.
- 아래는 내장 LED를 사용하는 예제입니다. 0.512초 간격으로 내장 LED를 켜고 끕니다.  
  ![](/assets/images/sw/rplus_task3_kr/task3_117.png)

#### 화면 출력
태스크 코드의 결과값을 터미널 창에서 확인하고 싶을 때 사용합니다.

#### 화면 출력 후 줄바꿈
태스크 코드의 결과값을 터미널 창에서 확인하고 싶을 때 사용합니다. 출력 후 자동으로 다음 줄로 변경됩니다.  
- 아래는 “화면 출력”과 “화면 출력 후 줄바꿈”을 사용하여 센서 값을 출력하는 예제입니다.  
  ![](/assets/images/sw/rplus_task3_kr/task3_118.png)  
  ![](/assets/images/sw/rplus_task3_kr/task3_119.png)

### [제어기: 직접 입력](#제어기-직접-입력)

- 제어기의 특정 주소에 직접 접근하여 읽기와 쓰기 작업을 진행할 수 있습니다.
- 사용자가 지정한 주소를 Byte(1바이트), Word(2바이트), DWord(4바이트) 단위로 선택하여 읽거나 씁니다.
- 각 제어기 매뉴얼 내의 컨트롤 테이블을 참고하세요.

## [다이나믹셀 장치](#다이나믹셀-장치)

다이나믹셀 액츄에이터의 컨트롤 테이블 값을 읽거나 쓰기 위한 파라미터 입니다. 자세한 정보는 다이나믹셀의 컨트롤 테이블을 참고하세요.

### [다이나믹셀](#다이나믹셀)

- DX / RX / AX 시리즈에서 사용 가능한 파라미터  
  토크 켜기 / 끄기, LED, CW margin / CCW margin, CW slope / CCW slope, 목표 위치, 이동 속도, 토크 한계, 현재 위치, 현재 속도, 현재 하중, 현재 전압, 현재 온도, 움직임 유무,
- MX 시리즈에서 사용 가능한 파라미터  
  토크 켜기 / 끄기, LED, PID gain, 목표 위치, 이동 속도, 토크 한계, 현재 위치, 현재 속도, 현재 하중, 현재 전압, 현재 온도, 움직임 유무
- X 시리즈에서 사용 가능한 파라미터(XL 라인업은 일부 파라미터 미적용)  
  토크 켜기 / 끄기, LED, PID gain, 목표 위치, 목표 속도, 목표 전류, 목표 PWM, 프로파일 가속도, 프로파일 속도, 토크 한계, 현재 위치, 현재 속도, 현재 전류, 현재 PWM, 현재 하중, 현재 전압, 현재 온도, 움직임 유무

#### 작동 모드
다이나믹셀의 동작 모드를 설정합니다. 자세한 내용은 다이나믹셀의 Operating Mode를 참고하세요.  
![](/assets/images/sw/rplus_task3_kr/task3_216.png)

#### 토크 켜기 / 끄기
다이나믹셀의 토크를 켜거나 끄기 위해 사용합니다. True일 때 토크 켜짐, False일 때 토크 꺼짐으로 동작합니다.  
- 아래는 제어기의 버튼을 누르면 ID가 1인 다이나믹셀의 토크를 켜는 예제입니다.  
  ![](/assets/images/sw/rplus_task3_kr/task3_120.png)

#### LED
다이나믹셀의 LED를 켜거나 끄기 위해 사용합니다. True일 때 LED 켜짐, False일 때 LED 꺼짐으로 동작합니다.

#### CW margin / CCW margin
다이나믹셀의 Margin 설정값을 읽어오거나 설정하기 위해 사용합니다. 값 범위는 0~ 254이며 가급적 기본값(1)을 바꾸지 않는 것이 좋습니다.  
자세한 설명은 해당 다이나믹셀의 컨트롤 테이블을 참고하세요.

#### CW slope / CCW slope
다이나믹셀의 Slope 설정값을 읽어오거나 설정하기 위해 사용합니다. 총 7단계로 설정가능하며 아래 표에 따라 대표값이 설정됩니다.  
자세한 설명은 해당 다이나믹셀의 컨트롤 테이블을 참고하세요.

| 단계 |       Data 값       | Data 대표 값 |
|:----:|:-------------------:|:------------:|
|  1   | 0 (0x00) ~ 3(0x03)  |   2 (0x02)   |
|  2   |  4(0x04) ~ 7(0x07)  |   4 (0x04)   |
|  3   |  8(0x08)~15(0x0F)   |   8 (0x08)   |
|  4   |  16(0x10)~31(0x1F)  |  16 (0x10)   |
|  5   |  32(0x20)~63(0x3F)  |  32 (0x20)   |
|  6   | 64(0x40)~127(0x7F)  |  64 (0x40)   |
|  7   | 128(0x80)~254(0xFE) |  128 (0x80)  |

#### PID Gains
다이나믹셀의 PID 설정값을 읽어오거나 설정하기 위해 사용합니다.  
P gain은 Proportional Gain으로 작은 값일수록 유격이 커지고, 목표위치 근처에서의 출력정도가 약해집니다.  
I gain은 Integral Gain 이며, D gain은 Derivative Gain 입니다.

#### 목표 위치
다이나믹셀의 목표 위치값을 읽어오거나 설정하기 위해 사용합니다.  
- 아래 그림과 같이 `모터 위치 값` 컨트롤을 사용하여 각도 위치를 설정할 수 있습니다.  
  ![](/assets/images/sw/rplus_task3_kr/task3_121.png)

#### 목표 속도
다이나믹셀의 이동 속도를 읽어오거나 설정하기 위해 사용합니다.  
- 아래 그림과 같이 `모터 제어 값` 컨트롤을 사용하여 회전 방향과 출력 값을 설정할 수 있습니다.  
  ![](/assets/images/sw/rplus_task3_kr/task3_122.png)

#### 프로파일 가속도
다이나믹셀-X 시리즈에서 프로파일의 가속도를 설정합니다. 자세한 내용은 X 시리즈의 [Profile Acceleration(108)](/docs/kr/dxl/x/xm430-w210/#profile-acceleration)을 참고하세요.  
![](/assets/images/sw/rplus_task3_kr/task3_214.png)

#### 프로파일 속도
다이나믹셀-X 시리즈가 Position Control 또는 Extended Position Control 모드일 때 프로파일의 최대 속도를 설정합니다. 자세한 내용은 X 시리즈의 [Profile Velocity(112)](/docs/kr/dxl/x/xm430-w210/#profile-velocity)을 참고하세요.  
![](/assets/images/sw/rplus_task3_kr/task3_215.png)

#### 목표 전류 / 토크
다이나믹셀의 전류 / 토크 한계를 설정하기 위해 사용합니다.  
![](/assets/images/sw/rplus_task3_kr/task3_207.png)

#### 현재 위치
다이나믹셀의 현재 위치를 읽어오기 위해 사용합니다.  
![](/assets/images/sw/rplus_task3_kr/task3_208.png)

#### 현재 속도
다이나믹셀의 현재 속도를 읽어오기 위해 사용합니다.  
![](/assets/images/sw/rplus_task3_kr/task3_209.png)

#### 현재 하중
다이나믹셀의 출력축이 받고있는 하중값과 하중의 방향을 읽어오기 위해 사용합니다.  
![](/assets/images/sw/rplus_task3_kr/task3_210.png)

#### 현재 입력 전압
다이나믹셀의 내부 전압을 읽어오기 위해 사용합니다.  
![](/assets/images/sw/rplus_task3_kr/task3_211.png)

#### 현재 온도
다이나믹셀의 내부 온도를 읽어오기 위해 사용합니다.  
![](/assets/images/sw/rplus_task3_kr/task3_212.png)

#### 움직임 유무
다이나믹셀의 움직임 유무를 읽어오기 위해 사용합니다. True일 때 움직이는 상태, False일 때 움직이지 않는 상태를 나타냅니다.  
![](/assets/images/sw/rplus_task3_kr/task3_213.png)

### [SyncWrite](#syncwrite)

CM-550 제어기를 사용할 경우 [프로토콜 2.0 - SyncWrite](/docs/kr/dxl/protocol2/#sync-write) 명령어를 사용할 수 있습니다.

#### SyncWrite Command

SyncWrite 명령어를 사용합니다. 아래와 같이 지정된 파라미터에 따른 동작을 합니다.

| 파라미터 |          동작           |                          예시                           |
|:--------:|:-----------------------:|:-------------------------------------------------------:|
|    0     | SyncWrite 패킷 시작하기 | ![](/assets/images/sw/rplus_task3_kr/sync_write_01.png) |
|    1     | SyncWrite 패킷 입력하기 | ![](/assets/images/sw/rplus_task3_kr/sync_write_02.png) |
|    2     | SyncWrite 패킷 전송하기 | ![](/assets/images/sw/rplus_task3_kr/sync_write_03.png) |

#### SyncWrite Address

데이터가 전송될 주소를 나타냅니다.

![](/assets/images/sw/rplus_task3_kr/sync_write_04.png)  
> 데이터가 전송될 시작주소를 116번지로 설정합니다.

#### SyncWrite Length

전송될 데이터의 길이를 나타냅니다.

![](/assets/images/sw/rplus_task3_kr/sync_write_05.png)  
> 전송될 데이터의 길이를 4바이트로 설정합니다.

#### SyncWrite ID

데이터가 적용될 ID를 나타냅니다.

![](/assets/images/sw/rplus_task3_kr/sync_write_06.png)  
> 데이터를 수신받을 다이나믹셀의 ID를 2로 설정합니다.

#### SyncWrite Data

전송될 데이터를 나타냅니다.

![](/assets/images/sw/rplus_task3_kr/sync_write_07.png)  
> 10진수 값 2048을 전송할 데이터로 설정합니다.

#### SyncWrite 사용 예

다음은 SyncWrite 명령어를 이용해서 다이나믹셀 ID 2번과 3번의 116번 주소에 각각 2048의 값을 전달하는 방법입니다.

![](/assets/images/sw/rplus_task3_kr/sync_write_example.png)

### [적외선 어레이 센서](#적외선-어레이-센서)

- 적외선 센서 값 (1~7번) : 적외선 센서 어레이의 적외선 센서 값을 읽어오기 위해 사용합니다. 벽이나 물체의 표면 색, 질감에 따라 측정값에 차이가 생길 수 있으며, 해당 센서는 0~5cm 이내에서 사용하도록 최적화 되었습니다.
- 적외선 감지 기준 값 (1~7번) : 적외선 센서 어레이가 흰색/검정색을 판단하는 기준 값입니다.

|                  | 검은색 감지 유무 | LED |
|:----------------:|:----------------:|:---:|
| 센서값 <= 기준값 |    해당 BIT 1    | ON  |
| 센서값 > 기준값  |    해당 BIT 0    | OFF |

- 버저 종류 : 적외선 센서 어레이의 버저 종류를 설정하기 위해 사용합니다.
- 버저 울림 시간 : 적외선 센서 어레이의 버저 사용시 소리가 지속될 시간을 설정하는데 사용합니다. 저 울림 시간을 먼저 설정한 후 버저 종류를 설정해야 설정에 맞게 소리가 납니다.
- 감지 기준 값 자동 설정 : 검정색 감지 기준값 자동 찾기의 시작과 마침을 결정하는데 사용합니다. 자세한 사용법은 아래 예제를 참고하세요.
- 적외선 물체 감지 유무 : 적외선 센서 어레이에 물체가 감지되었는지를 읽어오기 위해 사용합니다.

| 2 진수 값 | 10 진수 값 |        검은색 감지 유무        |
|:---------:|:----------:|:------------------------------:|
|  0000001  |     1      | 1번 적외선 센서에 검은 색 감지 |
|  0000010  |     2      | 2번 적외선 센서에 검은 색 감지 |
|  0000100  |     4      | 3번 적외선 센서에 검은 색 감지 |
|  0001000  |     8      | 4번 적외선 센서에 검은 색 감지 |
|  0010000  |     16     | 5번 적외선 센서에 검은 색 감지 |
|  0100000  |     32     | 6번 적외선 센서에 검은 색 감지 |
|  1000000  |     64     | 7번 적외선 센서에 검은 색 감지 |

아래 그림과 같이 그림을 보며 값을 체크할 수 있습니다.

![](/assets/images/sw/rplus_task3_kr/task3_123.png)

### [다이나믹셀 장치: 직접 입력](#다이나믹셀-장치-직접-입력)

- 다이나믹셀 등의 외부 장치의 주소를 직접 접근하여 읽기와 쓰기 작업을 진행할 수 있습니다.
- 사용자가 지정한 주소를 Byte(1바이트), Word(2바이트), DWord(4바이트) 단위로 선택하여 읽거나 씁니다.
- 각 다이나믹셀 매뉴얼 내의 컨트롤 테이블을 참고하세요.  
![](/assets/images/sw/rplus_task3_kr/task3_217.png)

## [스마트 장치](#스마트-장치)

제어기와 블루투스로 연결된 앱(R+ Smart, R+ IoT, R+ ENGINEER)의 컨트롤 테이블 값을 읽거나 쓰기 위한 파라미터 입니다.

### [카메라](#카메라)

스마트 기기의 카메라 기능을 사용하기 위한 파라미터입니다.

#### 카메라 선택
스마트 기기에 내장된 카메라 중 사용할 카메라를 선택합니다. 아래 예제는 후면 카메라와 전면 카메라를 번갈아 선택하는 예제입니다.  
![](/assets/images/sw/rplus_task3_kr/task3_124.png)  
![](/assets/images/sw/rplus_task3_kr/task3_125.png)

#### 카메라 확대
스마트 기기의 카메라를 확대할 때 사용합니다 (값의 범위는 0~255 입니다).  
아래는 카메라를 1.024초에 한번씩 확대하는 예제입니다.  
![](/assets/images/sw/rplus_task3_kr/task3_126.png)  
![](/assets/images/sw/rplus_task3_kr/task3_127.png)![](/assets/images/sw/rplus_task3_kr/task3_128.png)

#### 카메라 센서
스마트 기기의 카메라를 센서모드로 동작시키기 위해 사용합니다.  
![](/assets/images/sw/rplus_task3_kr/task3_129.png)

**참고**: 카메라 센서의 자세한 사용법은 [비전](#비전)을 참고하세요.
{: .notice}

#### 사진 촬영
스마트 기기의 카메라로 사진을 촬영할 때 사용합니다. (True일 때 촬영, False일 때 촬영정지)  
아래는 스마트 기기의 후면 카메라를 이용하여 사진을 촬영하는 예제입니다.  
![](/assets/images/sw/rplus_task3_kr/task3_130.png)  
![](/assets/images/sw/rplus_task3_kr/task3_131.png)

### [비전](#비전)

스마트 기기의 카메라를 “카메라 센서”로 설정시 사용하는 파라미터입니다.

#### 감지된 색상
“카메라 센서”의 “색상 감지 모드”를 사용하는 경우, 화면 가운데 부분에 표시되는 색상을 확인하기 위해 사용합니다.  
아래는 감지된 색상 값을 사용하는 예제입니다.  
![](/assets/images/sw/rplus_task3_kr/task3_132.png)

#### 감지할 라인 색상
“카메라 센서”의 “라인 감지 모드”를 사용하는 경우, 감지할 라인의 색상을 설정하기 위해 사용합니다.

#### 라인 감지 영역
“카메라 센서”의 “라인 감지 모드”를 사용하는 경우, 감지된 라인의 위치를 확인하기 위해 사용합니다.  
아래는 녹색 라인이 감지되면 해당 라인에 빨간색 원을 표시하는 예제입니다.  
![](/assets/images/sw/rplus_task3_kr/task3_133.png)  
![](/assets/images/sw/rplus_task3_kr/task3_134.png)

#### 얼굴 감지 영역
“카메라 센서”의 “얼굴 감지 모드”를 사용하는 경우, 감지된 얼굴의 위치를 확인하기 위해 사용합니다.  
아래는 얼굴이 감지되면 해당 위치에 빨간색 원을 표시하는 예제입니다.  
![](/assets/images/sw/rplus_task3_kr/task3_135.png)  
![](/assets/images/sw/rplus_task3_kr/task3_136.png)

#### 동작 감지 영역
“카메라 센서”의 “동작 감지 모드”를 사용하는 경우, 감지된 동작의 위치를 확인하기 위해 사용합니다.  
아래는 동작이 감지되면 해당 위치에 빨간색 원을 표시하는 예제입니다.  
![](/assets/images/sw/rplus_task3_kr/task3_137.png)  
![](/assets/images/sw/rplus_task3_kr/task3_138.png)

### [표시](#표시)

스마트 기기의 화면에 배경, 그림, 도형, 문자, 숫자를 표시하기 위해 사용합니다.

#### 화면 회전
스마트 기기의 화면 방향을 설정할 때 사용합니다.  
아래는 스마트 기기의 화면 방향을 1.024초마다 번갈아 변경하는 예제입니다.  
![](/assets/images/sw/rplus_task3_kr/task3_139.png)  
![](/assets/images/sw/rplus_task3_kr/task3_140.png)![](/assets/images/sw/rplus_task3_kr/task3_141.png)

#### 배경 표시
스마트 기기의 화면에 그림 배경을 설정할 때 사용합니다.(스마트 기기 앱에 미리 등록해놓은 배경만 사용할 수 있습니다.)  
아래는 스마트 기기의 그림 배경을 아이템1로 설정하는 예제입니다.  
![](/assets/images/sw/rplus_task3_kr/task3_142.png)  
![](/assets/images/sw/rplus_task3_kr/task3_143.png)

#### 그림 표시
스마트 기기의 화면에 그림을 배치할 때 사용합니다.(스마트 기기 앱에 미리 등록해놓은 그림만 사용할 수 있습니다.)  
아래는 스마트 기기의 위치2,3과 위치 4,3에 그림을 표시하는 예제입니다.  
![](/assets/images/sw/rplus_task3_kr/task3_144.png)  
![](/assets/images/sw/rplus_task3_kr/task3_145.png)

#### 감지된 얼굴 그림 표시
“카메라 센서”의 “얼굴 감지 모드”를 사용할 경우, 감지된 얼굴에 덮어씌울 그림을 설정할 때 사용합니다. (스마트 기기 앱에 미리 등록해놓은 그림만 사용할 수 있습니다.)  
아래는 스마트 기기의 카메라를 이용하여 얼굴을 감지한 후 감지된 얼굴 위에 그림을 표시하는 예제입니다.  
![](/assets/images/sw/rplus_task3_kr/task3_146.png)  
![](/assets/images/sw/rplus_task3_kr/task3_147.png)

#### 도형 표시
스마트 기기의 화면에 도형을 배치할 때 사용합니다. (1 : 원, 2 : 사각형, 3 : 삼각형)  
아래는 위치3,3에 파란색 원형과 회색 삼각형을 번갈아 표시하는 예제입니다.  
![](/assets/images/sw/rplus_task3_kr/task3_148.png)  
![](/assets/images/sw/rplus_task3_kr/task3_149.png)![](/assets/images/sw/rplus_task3_kr/task3_150.png)

#### 문자 표시
스마트 기기의 화면에 문자를 배치할 때 사용합니다. (스마트 기기 앱에 미리 등록해놓은 문자만 사용할 수 있습니다.)  
아래는 위치1,3~5,3에 차례로 문자를 표시했다가 지우는 예제입니다.  
![](/assets/images/sw/rplus_task3_kr/task3_151.png)  
![](/assets/images/sw/rplus_task3_kr/task3_152.png)
![](/assets/images/sw/rplus_task3_kr/task3_153.png)
![](/assets/images/sw/rplus_task3_kr/task3_154.png)
![](/assets/images/sw/rplus_task3_kr/task3_155.png)

#### 숫자 표시
스마트 기기의 화면에 숫자를 배치할 때 사용합니다. (별도의 문자 등록 없이 0~255 사이의 숫자를 사용할 수 있습니다.)  
아래는 위치3,3에 숫자를 증가하며 표시하는 예제입니다.  
![](/assets/images/sw/rplus_task3_kr/task3_156.png)  
![](/assets/images/sw/rplus_task3_kr/task3_157.png)![](/assets/images/sw/rplus_task3_kr/task3_158.png)

### [멀티미디어](#멀티미디어)

스마트 기기의 화면과 스피커를 사용하여 영상을 출력하거나, 소리를 출력하기 위해 사용합니다.

#### 문자음성 자동변환(TTS)
스마트 기기의 문자음성 자동변환 서비스를 활용할 때 사용합니다. (스마트 기기 앱에 미리 등록해놓은 문자만 사용할 수 있습니다.)  
아래는 문자아이템2, 문자아이템3을 번갈아 음성으로 변환하여 출력하는 예제입니다.  
![](/assets/images/sw/rplus_task3_kr/task3_159.png)

#### 악기 연주
스마트 기기로 악기 소리를 낼 때 사용합니다.  
아래는 어쿠스틱 피아노로 도, 레, 미를 반복해서 출력하는 예제입니다.  
![](/assets/images/sw/rplus_task3_kr/task3_160.png)

#### 오디오 재생
스마트 기기의 오디오 파일을 재생할 때 사용합니다.  
오디오 재생1과 오디오 재생2는 독립적으로 동작합니다. (스마트 기기 앱에 미리 등록해놓은 오디오 파일만 사용할 수 있습니다.)

#### 볼륨
스마트 기기의 사운드 볼륨을 설정할 때 사용합니다.  
값 범위는 0~255이며, 값이 클수록 볼륨이 커집니다. 기기에 따라 값의 범위가 다를 수 있습니다.  
아래는 오디오 재생1, 오디오 재생2, 볼륨을 이용하여 스마트 기기의 음원을 재생하는 예제입니다.  
![](/assets/images/sw/rplus_task3_kr/task3_161.png)

#### 동영상 재생
스마트 기기의 동영상 파일을 재생할 때 사용합니다. (스마트 기기 앱에 미리 등록해놓은 동영상만 사용할 수 있습니다.)

#### 동영상 일시정지
스마트 기기에서 동영상 파일이 재생되고 있을 때 일시 정지하기 위해 사용합니다.  
아래는 동영상 재생과 동영상 일시정지를 사용하여 화면을 터치하고 있는 동안 동영상 재생을 일시정지하는 예제입니다.  
![](/assets/images/sw/rplus_task3_kr/task3_162.png)

### [센서](#센서)

스마트 기기에 내장된 여러 가지 센서를 활용하기 위해 사용합니다.

#### 흔들림 센서
스마트 기기의 흔들림 센서를 활용하기 위해 사용합니다. 스마트 기기의 흔들림 정도에 따라 0~255사이 값이 출력됩니다.  
아래는 스마트 기기의 흔들림 정도를 읽어 값이 80이상일 때 화면에 표시한 도형의 색상을 바꾸는 예제입니다.  
![](/assets/images/sw/rplus_task3_kr/task3_163.png)  
![](/assets/images/sw/rplus_task3_kr/task3_164.png)![](/assets/images/sw/rplus_task3_kr/task3_165.png)

#### 기울기 센서
스마트 기기의 기울기 센서를 활용하기 위해 사용합니다. (왼쪽), (오른쪽), (위쪽), (아래쪽)의 기울기를 각각 0~90도로 출력됩니다.  
아래는 스마트 기기의 기울기에 따라 화면에 기울어진 방향에 원을 표시하는 예제입니다.  
![](/assets/images/sw/rplus_task3_kr/task3_166.png)  
![](/assets/images/sw/rplus_task3_kr/task3_167.png)![](/assets/images/sw/rplus_task3_kr/task3_168.png)![](/assets/images/sw/rplus_task3_kr/task3_169.png)

#### 조도 센서
스마트 기기의 조도 센서를 활용하기 위해 사용합니다. 주위 밝기에 따라 0~65535의 값이 출력됩니다. 기기에 따라 값의 범위가 다를 수 있습니다.  
아래는 조도를 측정하여 주위가 어두우면 회색 원을, 주위가 밝으면 흰색 원을 화면에 표시하는 예제입니다.  
![](/assets/images/sw/rplus_task3_kr/task3_170.png)  
![](/assets/images/sw/rplus_task3_kr/task3_171.png)![](/assets/images/sw/rplus_task3_kr/task3_172.png)

#### 자기장 센서
스마트 기기의 자기장 센서를 활용하기 위해 사용합니다. 주위 자기장에 따라 0~65535의 값이 출력됩니다.  
아래는 스마트 기기 주위의 자기장을 측정하여 값을 화면에 표시하는 예제입니다.  
![](/assets/images/sw/rplus_task3_kr/task3_173.png)  
![](/assets/images/sw/rplus_task3_kr/task3_174.png)![](/assets/images/sw/rplus_task3_kr/task3_175.png)

#### 방향 센서
스마트 기기의 방향 센서를 활용하기 위해 사용합니다. 방향에 따라 각도 단위로 0~359 사이의 값을 출력합니다. (0:북, 90:동, 180:남, 270:서)  
아래는 스마트 기기의 방향 값을 10으로 나누어 화면에 표시하는 예제입니다.  
![](/assets/images/sw/rplus_task3_kr/task3_176.png)  
![](/assets/images/sw/rplus_task3_kr/task3_177.png)

#### 소음 센서
스마트 기기의 소음 센서를 활용하기 위해 사용합니다. 소음에 따라 dB 단위로 0~255 사이의 값을 출력합니다.  
아래는 소음의 크기에 따라 도형을 표시하는 예제입니다.  
![](/assets/images/sw/rplus_task3_kr/task3_178.png)  
![](/assets/images/sw/rplus_task3_kr/task3_179.png)![](/assets/images/sw/rplus_task3_kr/task3_180.png)

#### 음성 인식
스마트 기기의 음성 인식 기능을 켜거나 끄기 위해 사용합니다. True일 때 “음성 인식 시작”, False일 때 “음성 인식 정지”로 동작합니다.  

#### 음성 인식 결과
“음성 인식”기능을 사용할 때, 인식된 결과를 확인하기 위해 사용합니다.  
인식된 결과가 숫자로 표시됩니다. 0일 때 “결과값 없음”, 1~199일 때 해당 문자아이템과 일치.  
아래는 음성 인식과 음성 인식 결과를 사용하여 화면을 터치했을 때 음성을 인식하여 인식된 결과를 화면 중앙에 표시하는 예제입니다.  
![](/assets/images/sw/rplus_task3_kr/task3_181.png)  
![](/assets/images/sw/rplus_task3_kr/task3_182.png)![](/assets/images/sw/rplus_task3_kr/task3_183.png)

#### 터치 위치
스마트 기기의 화면 터치 위치를 활용하기 위해 사용합니다. 터치 위치1은 첫 번째로 터치된 손가락을 의미하며 터치 위치2는 두 번째로 터치된 손가락을 의미합니다.  
아래는 터치한 위치에 도형을 표시하는 예제입니다.  
![](/assets/images/sw/rplus_task3_kr/task3_184.png)  
![](/assets/images/sw/rplus_task3_kr/task3_185.png)![](/assets/images/sw/rplus_task3_kr/task3_186.png)

#### 제스처 인식
스마트 기기의 제스처 인식 기능을 활용하기 위해 사용합니다.  
아래는 제스처를 인식하여 해당 제스처의 번호를 화면에 출력하는 예제입니다.  
![](/assets/images/sw/rplus_task3_kr/task3_187.png)  
![](/assets/images/sw/rplus_task3_kr/task3_188.png)![](/assets/images/sw/rplus_task3_kr/task3_189.png)

### [스마트 장치: 기타](#스마트-장치-기타)
스마트 기기의 부가 기능을 활용하기 위해 사용합니다.

#### 디버그 정보 표시
스마트 기기의 주요기능들의 값을 화면에 표시하여 확인하기 위해 사용합니다.  
하위 비트(우측)부터 1로 설정 시 다음의 정보를 스마트 기기의 화면에 표시할 수 있습니다.

|  비트(Bit)  | 정보                                             |
|:-----------:|:-------------------------------------------------|
| 1번째 비트  | 비전 관련 위치, 색상 표시 (정수 입력 시 : 1)     |
| 2번째 비트  | 흔들림 값 표시 (정수 입력 시 : 2)                |
| 3번째 비트  | 기울기 상하좌우 값 표시 (정수 입력 시 : 4)       |
| 4번째 비트  | 조도 값 표시 (정수 입력 시 : 8)                  |
| 5번째 비트  | 자기장 값 표시 (정수 입력 시 : 16)               |
| 6번째 비트  | 방향 값 표시 (정수 입력 시 : 32)                 |
| 7번째 비트  | 소음 값 표시 (정수 입력 시 : 64)                 |
| 8번째 비트  | 터치 위치 1, 2값 표시 (정수 입력 시 : 128)       |
| 9번째 비트  | 음성입력 결과 값 표시 (정수 입력 시 : 256)       |
| 10번째 비트 | SMS 관련 전화번호, 내용 표시(정수 입력 시 : 512) |

아래는 디버그 정보 표시 기능을 이용하는 예제입니다.  
![](/assets/images/sw/rplus_task3_kr/task3_190.png)  
![](/assets/images/sw/rplus_task3_kr/task3_191.png)

#### 화면 출력
태스크 코드에서 특정 값을 눈으로 확인하고 싶을 때 사용합니다. (스마트 앱 화면에 표시됩니다.)

#### 화면 출력 후 줄바꿈
태스크 코드에서 특정 값을 눈으로 확인하고 싶을 때 사용합니다. 출력 후 자동으로 다음 줄로 변경됩니다. (스마트 앱 화면에 표시됩니다.)  
아래는 스마트 기기의 화면출력 예제입니다.  
![](/assets/images/sw/rplus_task3_kr/task3_192.png)

#### 스마트 타이머
스마트 기기의 타이머를 설정하기 위해 사용합니다.

#### 진동 시간
스마트 기기의 진동 기능을 켤 때 사용합니다.

#### 진동 상태
스마트 기기가 현재 진동 중인지 확인하기 위해 사용합니다.  
아래는 스마트 타이머와 진동 시간을 이용하여 10초마다 1초 진동하는 예제입니다.  
![](/assets/images/sw/rplus_task3_kr/task3_193.png)

#### 현재 시간
스마트 기기로부터 현재시간을 읽어오기 위해 사용합니다.  
아래는 현재시간을 화면에 표시하는 예제입니다.  
![](/assets/images/sw/rplus_task3_kr/task3_194.png)  
![](/assets/images/sw/rplus_task3_kr/task3_195.png)

#### 플래시 LED
스마트 기기의 카메라 플래시 LED를 켜거나 끄기 위해 사용합니다.  
아래는 조도센서로 주위 밝기를 측정하여 어두우면 플래시 LED를 켜는 예제입니다.  
![](/assets/images/sw/rplus_task3_kr/task3_196.png)

#### 앱 실행하기
스마트 기기에 설치된 앱을 실행하기 위해 사용합니다.  
아래는 화면을 터치하면 등록된 앱을 실행하는 예제입니다.  
![](/assets/images/sw/rplus_task3_kr/task3_197.png)

#### E-Mail 기능
촬영한 사진이나 동영상을 E-Mail로 발송하기 위해 사용합니다.

#### E-Mail 전송 상태
현재 E-Mail이 전송 중인지 확인하기 위해 사용합니다.  
아래는 E-Mail 전송 기능과 E-Mail 전송 상태를 사용하여 촬영된 사진을 메일로 보내는 예제입니다.  
![](/assets/images/sw/rplus_task3_kr/task3_202.png)

#### 화면 넓이 / 화면 높이
스마트 기기 화면의 넓이와 높이를 읽기 위해 사용합니다.

### [사용자 데이터](#사용자-데이터)
스마트 기기의 특정 주소영역에 사용자의 데이터를 읽거나 쓸 수 있습니다.  

### [스마트 장치: 직접 입력](#스마트-장치-직접-입력)

- 스마트 기기의 주소를 직접 접근하여 읽기와 쓰기 작업을 진행할 수 있습니다.
- 사용자가 지정한 주소를 Byte 또는 Word, DWord 단위로 선택하여 읽거나 씁니다.
- 제품과 함께 사용되는 앱의 컨트롤 테이블을 참고하세요. [R+ Smart 컨트롤 테이블]

## [공통](#공통)

모든 장치에서 사용할 수 있는 기본적인 변수와 상수입니다.

### [변수](#변수)

- 프로그램 내부의 저장공간으로 여러 가지 데이터를 저장하거나 읽을 수 있습니다.
- 숫자를 기억하고 있어야 하는 경우나 공통된 값을 한꺼번에 변경해야 하는 경우 변수를 사용하면 유용합니다.
- 아래는 변수를 사용하는 예제입니다.

![](/assets/images/sw/rplus_task3_kr/task3_203.png)

### [숫자](#숫자)

- 프로그램 내부에서 숫자를 직접 입력해야 하는 경우 사용합니다.
- 대체로 조건절에서 값을 비교할 때 사용합니다.
- 값 범위는 -2,147,483,648 ~ 4,294,967,295 입니다.

![](/assets/images/sw/rplus_task3_kr/task3_204.png)

### [참/거짓](#참거짓)

- 프로그램 내부에서 참 / 거짓(True / False)를 직접 입력해야 하는 경우 사용합니다.
- 대체로 조건절에서 상태를 비교할 때 사용합니다.
- 값 범위는 0~1 입니다. False일 때 0, True일 때 1.

![](/assets/images/sw/rplus_task3_kr/task3_205.png)

### [2진수 숫자](#2진수-숫자)

- 프로그램 내부에서 숫자를 직접 입력해야 하는 경우 사용합니다.
- 대체로 비트 연산을 해야한 경우 사용되며, 2진수로 표기됩니다.
- 값 범위는 0 ~ 4,294,967,295 입니다. (Hex : 00 00 00 00 ~ FF FF FF FF)  
![](/assets/images/sw/rplus_task3_kr/task3_206.png)

### [모터 모드](#모터-모드)
SM-10 서보모터의 속도모드, 관절모드를 전환할 경우 사용합니다.  
![](/assets/images/sw/rplus_task3_kr/task3_219.png)

## [모션 목록](#모션-목록)
모션 예제가 열려있는 경우 해당 예제의 모션 목록이 여기에 나타납니다.  
모션 예제가 열려있지 않은 경우 이 항목은 메뉴에 표시되지 않습니다.  
![](/assets/images/sw/rplus_task3_kr/task3_218.png)

[제어기 호환표]: /docs/kr/parts/controller/controller_compatibility/
[접촉 센서 부품 정보]: /docs/kr/parts/sensor/ts-10/
[적외선 센서 부품 정보]: /docs/kr/parts/sensor/irss-10/
[컬러 센서 부품 정보]: /docs/kr/parts/sensor/cs-10/
[자석 센서 부품 정보]: /docs/kr/parts/sensor/mgss-10/
[온도 센서 부품 정보]: /docs/kr/parts/sensor/tps-10/
[절대 거리 센서 부품 정보]: /docs/kr/parts/sensor/dms-80/
[조도 센서 부품 정보]: /docs/kr/parts/sensor/cds-10/
[온습도 센서 부품 정보]: /docs/kr/parts/sensor/tms-10/
[동작감지 센서 부품 정보]: /docs/kr/parts/sensor/pir-10/
[사용자 센서 제작]: /docs/kr/edu/bioloid/premium/#사용자-센서-제작
[CM-50]: /docs/kr/parts/controller/cm-100/
[CM-100A]: /docs/kr/parts/controller/cm-100/
[CM-150]: /docs/kr/parts/controller/cm-150/
[CM-200]: /docs/kr/parts/controller/cm-200/
[CM-5]: /docs/kr/parts/controller/cm-5/
[CM-510]: /docs/kr/parts/controller/cm-510/
[CM-530]: /docs/kr/parts/controller/cm-530/
[CM-550]: /docs/kr/parts/controller/cm-550/
[CM-700]: /docs/kr/parts/controller/cm-700/
[OpenCM 7.0]: /docs/kr/parts/controller/opencm7/
[R+ Smart 컨트롤 테이블]: /docs/kr/software/mobile_app/rplussmart/#r-smart-control-table
[ROBOTIS DREAM]: /docs/kr/edu/dream/dream1-1/
[ROBOTIS SMART]: /docs/kr/edu/smart/smart1-1/
[ROBOTIS STEM]: /docs/kr/edu/bioloid/stem/
[ROBOTIS PREMIUM]: /docs/kr/edu/bioloid/premium/
[ROBOTIS GP]: /docs/kr/edu/bioloid/gp/
[ROBOTIS MINI]: /docs/kr/edu/mini/
[OpenCM 9.04]: /docs/kr/parts/controller/opencm904/
[BT-110]: /docs/kr/parts/communication/bt-110/
[BT-210]: /docs/kr/parts/communication/bt-210/
[BT-410]: /docs/kr/parts/communication/bt-410/
[제어기펌웨어 업데이트]: /docs/kr/software/rplus2/manager/getting_started/#펌웨어-업데이트
