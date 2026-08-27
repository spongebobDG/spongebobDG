# 김대건 | ROS 2 Robot Systems Software Engineer

실제 로봇에서 **센서·통신·제어 문제를 로그와 측정값으로 좁히고, 안전 계층과 재현 가능한 검증으로 마무리**합니다.

> ROBOTIS 휴머노이드 시스템 소프트웨어 엔지니어 지원 · 신입<br>
> ROS 2 · 실기기 통합 · 안전 제어 · 임베디드

[지원 포트폴리오 허브](https://github.com/spongebobDG/robotics-software-portfolio) · [대표 프로젝트](https://github.com/spongebobDG/turtlebot-fleet-ops) · [ROBOTIS 직무 매핑](https://github.com/spongebobDG/robotics-software-portfolio/blob/main/applications/robotis-humanoid-system-sw.md)

## Recruiter Quick Scan

| 근거 | 확인할 수 있는 역량 |
|---|---|
| 통신 단절 후 **0.301–0.305초** 내 정지, 자동 재개 없음 | 실 로봇 안전 제어와 실패 상태 검증 |
| **600초 · 11 loops · fault 0** 순찰 | ROS 2·Nav2 장시간 실기기 운영 |
| LiDAR 무수신 원인을 **9단계**로 추적해 TX 이탈 복구 | Linux·UART·ROS 2 계층형 디버깅 |
| KCC 2026 제1저자, **174KB LSTM → 약 10KB 1D-CNN** 설계 전환 | MCU 제약을 고려한 임베디드 AI |
| Dobot 실기기 **64.7초** 픽앤플레이스, 단위 테스트 12개 | 비전 좌표 보정과 fail-fast 로봇 동작 |

## Featured Projects

### 1. [TurtleBot Fleet Ops](https://github.com/spongebobDG/turtlebot-fleet-ops) · 개인 · 우수상

TurtleBot3 Burger 한 대의 bringup부터 센서 복구, SLAM, Nav2, 웹 관제, 공간정책, 안전 정지와 로컬 로그 진단까지 연결한 ROS 2 실기기 시스템입니다.

- `/scan` publisher는 있지만 데이터가 없던 문제를 토픽 → 프로세스 → 포트 → 원시 UART → 배선 순으로 추적
- deadman·Gateway·Zenoh 단절 후 최종 속도 0과 미재무장 정책을 실측
- 대구가톨릭대학교 인공지능 부트캠프 PBL 우수상, 2026-08-27

`ROS 2 Humble` `TurtleBot3` `Nav2` `TF2` `OpenCR` `Linux` `Python` `C++`

### 2. [Camping Safe Guard](https://github.com/spongebobDG/Camping-Safe-Guard) · 4인 팀장 · KCC 2026

ESP32·MQ-9·DHT11 센서 노드와 ESP32-C3 웨어러블 수신기를 연결한 일산화탄소 조기 경보 캡스톤입니다.

- 시스템 설계, 모델 경량화, 펌웨어, ESP-NOW, 회로와 3D 프린팅 케이스 제작 주도
- 제1저자로 논문 심사를 통과하고 한국컴퓨터종합학술대회(KCC 2026) 포스터 세션 발표
- AI 추론과 PPM 구간 규칙을 분리한 하이브리드 안전 판단

`ESP32` `TinyML` `TensorFlow Lite Micro` `ESP-NOW` `Embedded C++` `Sensors`

### 3. [Dobot Vision Sorter](https://github.com/spongebobDG/dobot-vision-sorter) · 개인

YOLOv8 인스턴스 세그멘테이션부터 카메라-로봇 좌표 보정, 작업영역 검증과 Dobot 픽앤플레이스까지 연결했습니다.

- 보정에 사용하지 않은 좌표로 homography를 검증하고 기준 미달 파일은 로드 거부
- 범위 밖 목표를 경계값으로 바꾸지 않고 원본 명령 자체를 거부
- 데이터 누수와 과거 좌표 재사용 등 프로토타입 문제 7개를 감사하고 수정

`Python` `OpenCV` `YOLOv8` `Homography` `Dobot` `GitHub Actions`

### 4. [Industrial Robot Arm Vision](https://github.com/spongebobDG/aip_robotarm_vision) · 개인

Raspberry Pi가 비전·기구학·FSM을, ESP32가 4축 서보의 50 Hz 로컬 모션 루프와 watchdog을 담당하는 분산 로봇암입니다.

- 명령 중단 1.5초 후 hold, 8초 후 자동 relax
- 4축 조그 5분 18초, telemetry 1,581건, 1초 이상 gap 0건
- FK→IK round-trip 오차 0.00°, 도달 불가능 목표 reject

`Raspberry Pi` `ESP32` `MQTT` `UART` `OpenCV` `Kinematics` `Watchdog`

### 5. [AIP Swarm](https://github.com/spongebobDG/aip-swarm-portfolio) · 5인 팀

산업 감시를 가정한 다차량 ROS 2 관제 프로젝트입니다. 카메라·열화상 연동, 웹 관제, 서브차량 구동 흐름을 담당했습니다.

- 직접 수행·공동 수행·팀 시스템을 [기여 case study](https://github.com/spongebobDG/aip-swarm-case-study)에 구분
- Docker simulation에서 3대 상태·지도·pose와 supervisor/simulation 56 tests 검증
- 실차 3대 동시 장시간 군집 주행은 미검증으로 명시

`ROS 2` `FastAPI` `WebSocket` `Computer Vision` `Docker` `Team Project`

## Core Stack

- **Robot software:** ROS 2 Humble, Nav2, SLAM Toolbox, AMCL, TF2, rclpy, rclcpp
- **Real hardware:** TurtleBot3 Burger, OpenCR, LDS-02, Dobot Magician Lite, Raspberry Pi 4, ESP32
- **Embedded:** UART, MQTT, ESP-NOW, PWM servo, watchdog, TensorFlow Lite Micro
- **Perception:** OpenCV, camera calibration, homography, RGB–thermal alignment, YOLOv8 segmentation
- **Operations:** Ubuntu 22.04, Docker, FastAPI, WebSocket, GitHub Actions

## Evidence and Scope Policy

1. 실기기, 시뮬레이션, mock 결과를 서로 바꿔 표현하지 않습니다.
2. 수치는 코드·로그·영상 또는 문서에서 확인할 수 있을 때만 사용합니다.
3. 팀 프로젝트는 본인 수행, 공동 수행과 팀 시스템을 구분합니다.
4. 구현한 것과 아직 검증하지 못한 것을 같은 완료 상태로 표시하지 않습니다.

## Current Learning Focus

OpenCR을 통해 DYNAMIXEL을 운용했지만 **DYNAMIXEL SDK 직접 제어와 `ros2_control` hardware interface 구현은 아직 실기기 검증 전**입니다. 프로토콜 2.0, Control Table, Sync Write/Bulk Read와 `SystemInterface` lifecycle을 학습하고 있으며, 검증 결과가 생긴 뒤에만 보유 역량으로 표시하겠습니다.

## How I Work

- 기능보다 먼저 데이터와 제어가 끊기는 계층을 찾습니다.
- 상위 판단이 틀리거나 통신이 끊겼을 때를 대비해 하위 안전 계층을 둡니다.
- 성공 장면뿐 아니라 실패 원인, 수정 전후와 남은 한계를 기록합니다.

<details>
<summary>이전 프로필 내용 보존</summary>

# 김대건 | ROS 2 Robot Systems Software Developer

ROS 2 기반 로봇 시스템을 실제 하드웨어에서 통합하고, 센서·통신·제어 문제를 로그와 측정값으로 분석합니다.

> I build and debug ROS 2 robot systems across hardware integration, safe motion, perception, and fleet operations.

## Focus

- ROS 2 시스템 소프트웨어와 Linux 디버깅
- TurtleBot3·OpenCR·LiDAR 실기기 통합
- watchdog, deadman, e-stop 기반 안전 제어
- RGB·열화상 비전과 로봇팔 추적

## Featured Projects

### 1. [TurtleBot Fleet Ops](https://github.com/spongebobDG/turtlebot-fleet-ops)

TurtleBot3 Burger 한 대의 bringup부터 Nav2, 웹 관제, 안전 정지, 작업·장애 복구까지 연결한 ROS 2 실기기 프로젝트입니다.

- LDS-02 TX 연결 문제를 원시 UART로 추적해 `/scan` 복구
- deadman·Gateway·Zenoh 단절 후 0.301–0.305초 내 최종 정지 및 미재개 검증
- 600초 실기기 순찰 11 loops, fault 0

`ROS 2 Humble` `TurtleBot3` `Nav2` `OpenCR` `Linux` `Python` `C++`

### 2. [AIP Swarm Contribution Case Study](https://github.com/spongebobDG/aip-swarm-case-study)

ROS 2 군집 순찰 팀 프로젝트에서 맡은 카메라 비전, 웹 관제, 서브 차량 구동을 본인·공동·팀 시스템으로 구분해 정리했습니다.

- 팀 전체 결과를 개인 성과로 표시하지 않는 contribution matrix
- 카메라/인식 결과와 중앙 관제의 인터페이스
- 서브 차량 구동과 ROS 2 namespace 통합 경험

`ROS 2` `Computer Vision` `Web Monitoring` `Team Project`

### 3. [Industrial Robot Arm Vision](https://github.com/spongebobDG/aip_robotarm_vision)

Raspberry Pi가 비전·기구학·FSM을 담당하고 ESP32가 4축 서보를 50 Hz로 제어하는 분산 감시 로봇암입니다.

- MQTT 명령 중단 후 8초 자동 relax 검증
- RGB 640×480 약 23 FPS 및 RGB–열화상 affine calibration
- FK/IK round-trip 0.00°와 도달 불가능 목표 reject

`Raspberry Pi` `ESP32` `MQTT` `Computer Vision` `Python` `C++`

### 4. [Camping Safe Guard](https://github.com/spongebobDG/Camping-Safe-Guard)

ESP32, MQ-9, DHT11과 TinyML을 활용한 캠핑 안전 캡스톤 프로젝트입니다. KCC 학술대회 논문 심사를 통과하고 poster session에서 발표했습니다.

`ESP32` `TinyML` `Embedded` `Sensors` `TensorFlow Lite Micro`

### 5. [ROS2 RobotOps Dashboard](https://github.com/spongebobDG/ros2-robotops-dashboard)

합성·mock ROS 2 로그와 로봇 상태를 이용해 장애 진단, 웹 관제, MLflow·Prometheus 운영 구조를 재현한 보조 프로젝트입니다.

`FastAPI` `WebSocket` `MLflow` `Prometheus` `Docker`

## Portfolio Hub

프로젝트별 문제 정의, 정확한 기여 범위, 검증 결과와 지원 직무 매핑은 [robotics-software-portfolio](https://github.com/spongebobDG/robotics-software-portfolio)에 정리했습니다.

## Core Skills

- **Robot Software:** ROS 2 Humble, Nav2, TF2, rclpy, lifecycle/task control
- **Hardware:** TurtleBot3 Burger, OpenCR, LDS-02, Raspberry Pi, ESP32
- **Languages:** Python, C++, JavaScript
- **Vision:** OpenCV, RGB/thermal calibration, tracking
- **Operations:** GitHub Actions, Docker Compose, FastAPI, Prometheus

## Current Gap and Next Step

DYNAMIXEL SDK와 `ros2_control` hardware interface를 직접 구현·검증하는 TurtleBot3 실기기 프로젝트를 다음 대표작으로 준비합니다. 팀 프로젝트에서 접한 기술을 개인 기여로 소급하지 않고, 직접 만든 코드와 실험 결과가 완성된 뒤에만 프로필에 추가합니다.

## How I Work

1. 로그와 관찰값으로 문제 범위를 나눕니다.
2. 자동 테스트와 실기기 검증의 역할을 구분합니다.
3. 수정 전후를 수치와 재현 절차로 비교합니다.
4. 팀 프로젝트에서는 본인 기여와 팀 시스템의 경계를 명확히 표시합니다.

</details>
