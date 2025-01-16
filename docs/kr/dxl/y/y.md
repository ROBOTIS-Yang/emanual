---
layout: archive
lang: kr
ref: dxl_y
permalink: /docs/kr/dxl/y/
sidebar:
  title: 다이나믹셀-Y
  nav: "dynamixel_y"
---

![](/assets/images/dxl/y/y_series_product.png)

DYNAMIXEL-Y is ROBOTIS’ industrialized premium robot actuator solution for full scale Robots

# [제품 라인업](#제품-라인업)

![](/assets/images/dxl/y/model_numbering_kr.png)

![](/assets/images/dxl/y/y_productline.png)

> 다이나믹셀-Y 시리즈 라인업

**Features**
- High Performance Frameless motor
- Multi-turn Absolute Encoder
- Integrated Electric Brake for Safety
- Integrated Dynamixel Drive(DYD)
- Compact & Simple Design with Hollow Shaft
- Dynamic Motor Controller

![](/assets/images/dxl/y/y_type.png)

![](/assets/images/dxl/y/y_exploded_view.png)

# [주요 사양](#주요-사양)

## [YM070](#ym070)

|       모델명        | 크기 [mm]   | 무게 [g] | 기어비 [R]  | 정격 토크 [N.m]  | 최대 토크 [N.m] | 동작 전압 [V]  | 해상도 [pulse/rev]  |         구성          |
| :-----------------: | :--------: | :------: | :--------: | :-------------: | :-------------: | :-----------: | :----------------: | :-------------------: |
| [YM070-210-M001-RH] | Ø70 x 50.9 |   340    |     -      |      0.32       |      0.64       |      24       |      524,288       |         Motor         |
| [YM070-210-B001-RH] | Ø70 x 71.0 |   530    |     -      |      0.32       |      0.64       |      24       |      524,288       |     Motor, Brake      |
| [YM070-210-R051-RH] | Ø70 x 71.1 |   790    |    51:1    |       8.2       |      16.3       |      24       |     26,738,688     |    Motor, Reducer     |
| [YM070-210-R099-RH] | Ø70 x 71.1 |   790    |    99:1    |      14.6       |      31.7       |      24       |     51,904,512     |    Motor, Reducer     |
| [YM070-210-A051-RH] | Ø70 x 91.2 |   980    |    51:1    |       8.2       |      16.3       |      24       |     26,738,688     | Motor, Reducer, Brake |
| [YM070-210-A099-RH] | Ø70 x 91.2 |   980    |    99:1    |      14.6       |      31.7       |      24       |     51,904,512     | Motor, Reducer, Brake |

## [YM080](#ym080)

|       모델명        |  크기 [mm]   | 무게 [g] | 기어비 [R]  | 정격 토크 [N.m]  | 최대 토크 [N.m] | 동작 전압 [V]  | 해상도 [pulse/rev]  |         구성          |
| :-----------------: | :---------: | :------: | :--------: | :-------------: | :-------------: | :-----------: | :----------------: | :-------------------: |
| [YM080-230-M001-RH] | Ø80 x 54.1  |   530    |     -      |      0.62       |      1.24       |      24       |      524,288       |         Motor         |
| [YM080-230-B001-RH] | Ø80 x 76.1  |   890    |     -      |      0.62       |      1.24       |      24       |      524,288       |     Motor, Brake      |
| [YM080-230-R051-RH] | Ø80 x 78.1  |  1,200   |    51:1    |      15.8       |      31.6       |      24       |     26,738,688     |    Motor, Reducer     |
| [YM080-230-R099-RH] | Ø80 x 78.1  |  1,200   |    99:1    |      26.0       |      61.4       |      24       |     51,904,512     |    Motor, Reducer     |
| [YM080-230-A051-RH] | Ø80 x 100.1 |  1,550   |    51:1    |      15.8       |      31.6       |      24       |     26,738,688     | Motor, Reducer, Brake |
| [YM080-230-A099-RH] | Ø80 x 100.1 |  1,550   |    99:1    |      26.0       |      61.4       |      24       |     51,904,512     | Motor, Reducer, Brake |

# [통신 회로](#통신-회로)

## [UART 연결 회로도](#uart-연결-회로도)

Main Controller를 직접 제작하여 다이나믹셀-Y를 제어하기 위해서는 Main Controller UART의 신호를 RS485 type으로 변환시켜 주어야 합니다. 다음은 권장 회로도 입니다.

![](/assets/images/dxl/y/uart_connection.PNG)

**참고**: 위 회로는 5V 전원을 사용하는 MCU를 사용하거나 IO가 5V tolerant한 경우 사용 가능합니다. 그 외의 경우, Level Shifter를 사용하세요.
{: .notice}

다이나믹셀 전용 제어기에는 위의 회로가 내장되어 있습니다. 위의 회로도에서 TTL Level의 TxD와 RxD는 TX_Enable_5V의 Level에 따라 다음과 같이 Data 신호의 방향이 결정됩니다.
- TX_Enable_5V =High인 경우: TxD의 신호가 D+, D-로 출력
- TX_Enable_5V =Low인 경우: D+, D-의 신호가 RxD로 입력

## [케이블 연결](#케이블-연결)
DYNAMIXEL-Y 커넥터의 핀 배열은 아래 그림과 같습니다.

![](/assets/images/dxl/y/70_connect_cable_1.png)

![](/assets/images/dxl/y/70_connect_cable_2.png)


**경고**: 배선 시에는 핀 배열이 틀리지 않도록 각별히 주의하십시오. 올바르게 연결되지 않을 경우 다이나믹셀의 심각한 손상을 초래할 수 있습니다.
{: .notice--warning}

[YM070-210-M001-RH]: /docs/kr/dxl/y/ym070-210-m001-rh/
[YM070-210-B001-RH]: /docs/kr/dxl/y/ym070-210-b001-rh/
[YM070-210-R051-RH]: /docs/kr/dxl/y/ym070-210-r051-rh/
[YM070-210-R099-RH]: /docs/kr/dxl/y/ym070-210-r099-rh/
[YM070-210-A051-RH]: /docs/kr/dxl/y/ym070-210-a051-rh/
[YM070-210-A099-RH]: /docs/kr/dxl/y/ym070-210-a099-rh/
[YM080-230-M001-RH]: /docs/kr/dxl/y/ym080-230-m001-rh/
[YM080-230-B001-RH]: /docs/kr/dxl/y/ym080-230-b001-rh/
[YM080-230-R051-RH]: /docs/kr/dxl/y/ym080-230-r051-rh/
[YM080-230-R099-RH]: /docs/kr/dxl/y/ym080-230-r099-rh/
[YM080-230-A051-RH]: /docs/kr/dxl/y/ym080-230-a051-rh/
[YM080-230-A099-RH]: /docs/kr/dxl/y/ym080-230-a099-rh/