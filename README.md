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
