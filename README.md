# 김재위 / Jaewi Kim


하드웨어와 소프트웨어가 만나는 지점에서 일합니다. 
<br/>레지스터를 직접 건드리는 임베디드 제어부터 ROS2 기반 멀티로봇 시스템, 딥러닝 모델 학습까지
<br/>한 시스템의 처음과 끝을 직접 붙여 봤습니다.

&nbsp;&nbsp;&nbsp;📨 Email: - jaewi.kim055@gmail.com<br/>
&nbsp;&nbsp;&nbsp;📝 Blog: [kimtortilla.tistory.com](https://kimtortilla.tistory.com/)<br/>

---

### About Me

| 기간 | 활동 | 주요 업무 |
| --- | --- | --- |
| 2025.12 ~ 2026.07 | **대한상공회의소 서울기술교육센터** | 로봇 AI SW 개발자 과정 |
| 2015.09 ~ 2022.04 | **University of British Columbia** | B.S. Human Kinetics 졸업 |

---

### 📂 Projects

### _현재 진행중_
#### [스콜피 - 5축 로봇팔과 3지 그리퍼를 장착한 층간이동 자율주행 로봇](https://github.com/cheeserust/Scorpy)
![ROS2:Jazzy](https://img.shields.io/badge/ROS2-Jazzy-blue?style=flat-square)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)
<br/> 직접 설계/제작한 로봇팔과 그리퍼를 장착하고 층간이동이 가능한 주행로봇
- **담당**: 층간 이동 구현(ArUco + solvePnP), 거리 추정 10 - 250cm 구간 오차 < 5%
- **성과**:
  - 층간 이동 구현
  - **통신 장애 디버깅**: 카메라 토픽 유실 → QoS 불일치 + 커널 UDP 버퍼 부족으로 **레이어별 진단**, `rmem_max` 증설 및 DDS 인터페이스 바인딩으로 해결
  - FSM 기반 상태 관리 (`WAIT_BOARD → BOARDING → RIDING → EXITING → DONE`) + Action Server 인터페이스 설계

---

#### [ROScue - 폭발물 탐색/해체 로봇](https://github.com/cheeserust/ROScue)
![ROS2:Jazzy](https://img.shields.io/badge/ROS2-Jazzy-blue?style=flat-square)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![YOLO](https://img.shields.io/badge/YOLO-00FFFF?style=flat-square&logo=yolo&logoColor=black)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)
![HuggingFace](https://img.shields.io/badge/-HuggingFace-3B4252?style=flat-square&logo=huggingface)
<br/> 세 대의 로봇과 두 대의 ROBOTIS OMX 로봇팔을 제어하여 폭발물을 탐색하고 ROBOTIS-OMX 로 해체하는 로봇 다중제어 시스템
- **담당**: 다중로봇 자율 주행 관제 시스템 아키텍쳐 설계
- **성과**: 
  - 무선 대역폭 제약을 아키텍쳐 재설계로 해결:
    - PC 중앙 집중 Nav2 → 각 터틀봇 온보드 Nav2 + 도메인 격리 + 도메인 브릿지
      - 

#### ⚾ [PitchType - AI 야구 동작 분석 시스템](https://github.com/Hanjiho0316/AI_Pitching_analysis_system)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![YOLO](https://img.shields.io/badge/YOLO-00FFFF?style=flat-square&logo=yolo&logoColor=black)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=flat-square&logo=tensorflow&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white)
<br/>YOLOv8n-Pose 기반 투구/타격 폼 분석 서비스
- **담당**: 데이터 전처리, 모델 최적화, 실험 설계
- **성과**:
  - 소량 데이터 (클래스당 30 - 50개)를  L2 · SpatialDropout1D · Label Smoothing · GAP · StratifiedKFold 5-fold 를 통해 대응
    - 정확도 ~95%
  - 데이터 파이프라인 마이그레이션: MediaPipe → YOLOv8n-pose 정량 비교 후 전환
  - **한국정보처리학회 ASK 2026 학술대회 논문 게재**

#### 🔥 [the-Photatos - STM32 화재진압 시스템](https://github.com/sangaje/the-Photatos)
![C](https://img.shields.io/badge/C-00599C?style=flat-square&logo=c&logoColor=white)
![C](https://img.shields.io/badge/-STM32-03234B?style=flat-square&logo=stmicroelectronics&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)
<br/>STM32F411 기반 자율 소화 로봇. 4채널 IR 센서 + 적응형 칼만 필터로 화염 방향을 추정하고 스테퍼/서보로 노즐을 자동 조준.

#### 🔧 [PLC_mini_Project](https://holistic-sock-964.notion.site/PLC-3007f8020a7280c882e4dad6cddd8cef?source=copy_link)<br/>
![PLC](https://camo.githubusercontent.com/92540e16c2a217f253227949e770bac73384e10bca19823d9ad201abe2902013/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f504c432d3334384133413f7374796c653d666f722d7468652d6261646765266c6f676f3d637075266c6f676f436f6c6f723d7768697465)
<br/>PLC 미니 프로젝트 → 소재별 자동/수동 적재 및 배출과 비상정지

---

### 🛠 Tech Stack

**Languages**

![C](https://img.shields.io/badge/C-00599C?style=flat-square&logo=c&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)

**Robotics / Embedded**

![ROS2](https://img.shields.io/badge/ROS2-22314E?style=flat-square&logo=ros&logoColor=white)
![STM32](https://img.shields.io/badge/STM32-03234B?style=flat-square&logo=stmicroelectronics&logoColor=white)
![Raspberry Pi](https://img.shields.io/badge/-RaspberryPi-C51A4A?style=flat-square&logo=Raspberry-Pi)

**AI / Vision**

![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=flat-square&logo=tensorflow&logoColor=white)
![YOLO](https://img.shields.io/badge/YOLO-00FFFF?style=flat-square&logo=yolo&logoColor=black)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white)

**Tools**

![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white)
![HuggingFace](https://img.shields.io/badge/-HuggingFace-3B4252?style=flat-square&logo=huggingface)

**OS**

![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)

