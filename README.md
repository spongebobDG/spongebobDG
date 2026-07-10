# 김대건 | Robotics & AI Software Developer

ROS 2 기반 로봇 소프트웨어와 컴퓨터 비전, 로봇 운영 자동화에 관심을 두고 개발하고 있습니다.  
단순히 기능을 구현하는 데서 끝내지 않고, **실시간 제어 안정성·장애 진단·재현 가능한 배포 환경**까지 함께 고민합니다.

## Core Skills

- **Robotics:** ROS 2 Humble, TurtleBot3, Nav2, TF2, MQTT
- **AI / Vision:** Python, OpenCV, YOLOv8, scikit-learn
- **Backend / MLOps:** FastAPI, WebSocket, MLflow, Prometheus, Grafana
- **Infrastructure:** Docker, Docker Compose, GitHub Actions, WSL2
- **Embedded:** Raspberry Pi, ESP32, Arduino, PlatformIO

## Featured Projects

### 1. [ROS2 RobotOps Dashboard](https://github.com/spongebobDG/ros2-robotops-dashboard)

다중 로봇의 상태를 실시간으로 관제하고 ROS 2 장애 로그를 자동 분류하는 운영 대시보드입니다.

- FastAPI와 WebSocket을 이용한 로봇 5대 실시간 상태 관제
- TF-IDF + Logistic Regression 기반 ROS 2 장애 로그 10종 분류
- MLflow 모델 버전 관리, Prometheus/Grafana 운영 지표 구성
- Docker Compose 기반 재현 환경과 GitHub Actions CI 구성
- 실제 로봇 없이 전체 흐름을 시연할 수 있는 mock ROS 2 데이터 생성기 포함

`ROS 2` `FastAPI` `WebSocket` `scikit-learn` `MLflow` `Docker`

---

### 2. [TurtleBot3 AI Vision](https://github.com/spongebobDG/TurtleBot3_AI_Vision)

YOLOv8으로 목표물을 인식하고 TurtleBot3 Burger가 실시간으로 추적하는 프로젝트입니다.

- ROS 2 이미지 QoS를 `KEEP_LAST`, `depth=1`로 조정해 누적 프레임 지연 개선
- 속도 명령 토픽의 제어권 충돌을 분석해 로봇 떨림 현상 해결
- 일시적인 인식 실패 시 지수 감쇠를 적용해 급정거 완화
- 거리 오차 기반 P 제어와 최소·최대 속도 제한 적용

`ROS 2 Humble` `TurtleBot3` `YOLOv8` `OpenCV` `Python`

---

### 3. [Industrial Robot Arm Vision](https://github.com/spongebobDG/aip_robotarm_vision)

RGB·열화상 비전을 활용하는 4축 산업용 감시 로봇암 프로젝트입니다.

- Raspberry Pi 4에서 비전·AI·상태 머신을 처리하는 분산 구조 설계
- ESP32의 50Hz 실시간 서보 제어와 Wi-Fi/MQTT 통신 구현
- 서보 제한값 캘리브레이션 도구와 통신 단절 안전정지 구조 설계
- 역기구학과 RGB·열화상 융합을 단계적으로 확장할 수 있는 모듈 구성

`Raspberry Pi` `ESP32` `MQTT` `PlatformIO` `Python` `Computer Vision`

## Other Work

| Repository | Focus |
|---|---|
| [Camping Safe Guard](https://github.com/spongebobDG/Camping-Safe-Guard) | Arduino·센서·TinyML 기반 캠핑 안전 시스템 실험 |
| [camping_bot](https://github.com/spongebobDG/camping_bot) | ROS 2 패키지와 임베디드 제어 연동 |
| [ROS2 Study](https://github.com/spongebobDG/ROS2_Study) | ROS 2 노드·서비스·액션·비전 학습 기록 |
| [DeepThinkCar RC](https://github.com/spongebobDG/DeepThinkCar-RC) | OpenCV 차선 인식과 RC카 모터 제어 실험 |
| [robot_arm_project_v2](https://github.com/spongebobDG/robot_arm_project_v2) | 카메라 및 로봇암 캘리브레이션 실험 |
| [TIL](https://github.com/spongebobDG/TIL) | 개발 과정에서 배운 내용과 문제 해결 기록 |

## How I Work

1. 재현 가능한 환경과 실행 절차를 먼저 정리합니다.
2. 로그와 증상을 기반으로 문제의 원인을 분리합니다.
3. 수정 전후 동작을 테스트와 측정값으로 확인합니다.
4. 다른 개발자가 이어받을 수 있도록 설계 의도와 트러블슈팅을 문서화합니다.

## Current Focus

- 실제 ROS 2 로봇과 관제 대시보드 연결
- RGB·열화상 센서 융합과 로봇암 추적
- 로봇 장애 데이터 수집 및 진단 모델 고도화

---

프로젝트에 관한 질문이나 피드백은 각 저장소의 Issue를 통해 남겨주세요.
