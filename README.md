# 안성식

## 소프트웨어 개발자

약 3년의 소프트웨어 개발 경험이 있습니다. 로보스텍에서 C++/C# 기반 Windows 프로그램의 장비 연동, 영상 처리, 네트워크 통신을 개발했으며, 프리랜서 기간에는 Python/PHP 개발과 Android 앱의 Google Play 업데이트 및 target SDK 대응을 수행했습니다.

이후 Unreal Engine과 Unity를 활용한 실시간 3D 클라이언트 개발로 경험을 확장하고 있습니다.

## C++/C# 실무

[Windows 장비 연동 개발 포트폴리오 보기](https://anseongsik-ue.github.io/windows-device-integration-portfolio/)

### ROV Camera System

ROV의 여러 RTSP 카메라 영상을 통합해 모니터링하고 녹화하는 C++/MFC 기반 Windows 프로그램입니다.

- 측면 8대와 후방 1대의 9채널 RTSP 영상 수신 및 표시
- CUDA 사용 가능 여부에 따라 GPU/CPU 디코딩 경로 선택
- 카메라 제어와 FFmpeg/NVENC 영상 녹화 경로 구현
- 프레임 타임아웃 감지 및 자동 재연결

### TunnelROVDataHub

ROV 운용 장비의 데이터를 수신하고 파싱해 화면, 로그 및 외부 운용 시스템에 전달하는 C#/WinForms 기반 Windows 프로그램입니다.

- GNSS/Altimeter는 Serial, Sonar/INS는 UDP, PLC/CableReel은 FEnet으로 수신 및 파싱
- 장비 데이터를 화면과 로그에 표시하고 외부 운용 시스템으로 전달
- 장비별 통신 상태와 수신 작업, 타이머, 연결 자원 관리

### Motor Control

조이패드 입력으로 모터를 제어하고 상태를 확인하는 C++/Qt 기반 Windows 프로그램입니다.

- 조이패드 입력을 모터 제어 명령으로 변환
- 모터 상태 수신 프로토콜을 구현하고 수신 데이터를 처리
- Motor 1/2의 RPM, 전류, 전압, 온도를 확인하는 모니터링 UI 추가

## 프리랜서 개발

### face-recognition

얼굴 및 표정 인식 결과에 맞춰 촬영 안내와 화면 효과를 제공하는 Python/PyQt 프로그램입니다.

- 촬영 전후 상태 이미지와 안내 가이드 표시
- 인식 상태에 따른 안내 표시 시점과 투명도, 하단 배너 투명도 조정
- 촬영 효과와 오디오 재생 흐름 적용 및 연속 촬영 오류 수정
- Windows 빌드의 SQLite 의존성 보완

[GitHub 저장소](https://github.com/AnSeongSik-UE/face-recognition)

### order-pdf-workflow

주문 PDF의 다운로드, 가공 및 저장 작업을 지원하는 Python/PyQt 프로그램입니다.

- PDF 다운로드를 QThread 작업으로 분리하고 저장 파일 확인으로 중복 다운로드 방지
- QMutex/QWaitCondition 기반 일시정지와 재개, 실패 시 재시도 처리
- 작업 중지 과정의 크래시와 멈춤 문제 수정

[GitHub 저장소](https://github.com/AnSeongSik-UE/order-pdf-workflow)

### shopping-rank-monitor

상품과 검색어의 순위를 조회해 기록하고 변동과 예약 공지를 Telegram으로 전달하는 Python/PyQt 도구입니다.

- 상품 정보의 SQLite 추가, 수정 및 삭제 흐름 구현
- Telegram 상품 등록과 삭제, 조회 주기 조정 및 예약 공지 처리
- Excel 기반 등록 상품 입력과 작성 양식 보완

[GitHub 저장소](https://github.com/AnSeongSik-UE/shopping-rank-monitor)

### PDA용 API 개발

재물조사 업무의 PDA 연동을 위한 개발 작업입니다.

- PHP로 PDA용 API 작성

### Open API를 이용하여 제작된 기존 프로그램 보강

기존 Open API 기반 주식 자동매수 프로그램의 기능을 보강한 Python 작업입니다.

- 기존 코드 분석과 거래내역 조회 및 표시 기능 보강
- 손절 및 익절 조건 처리 기능 추가

### Google Play 업데이트

Google Play에 등록된 기존 Android 앱을 요구사항에 맞춰 업데이트한 작업입니다.

- 요구 target SDK 문제를 해결하고 Google Play 업데이트 진행

## Unreal Engine

### Virtual Production Pipeline

MediaPipe의 얼굴과 포즈 추론 결과를 Binary UDP로 Unreal Engine 5.8 C++ Runtime Plugin에 전달해 VRoid에 반영하고 Spout2로 출력하는 1인 프로젝트입니다.

- Python과 Unreal Engine 사이 Binary UDP 패킷 검증 및 최신 프레임 기준 처리
- VRoid 표정, 머리, 양쪽 상완 반영과 추적 소실 시 중립 자세 복귀
- Spout2 출력 및 프로세스 실행 상태 확인과 시작 및 종료 관리
- 기능 목표와 문제를 직접 정의하고 OpenAI Codex를 활용해 구현과 문제 해결을 진행한 뒤 실제 환경에서 결과 검증

[GitHub 저장소](https://github.com/AnSeongSik-UE/Virtual-Production-Pipeline-UE5.8) / [Windows 최신 릴리즈](https://github.com/AnSeongSik-UE/Virtual-Production-Pipeline-UE5.8/releases/latest)

### TouchNPop

Unreal Engine 5의 Blueprint Only와 ARCore로 제작한 Android AR 두더지잡기 4인 팀 프로젝트입니다.

- AR Plane 자동 식별 및 감지된 평면 내부 무작위 위치에 캐릭터 Spawn
- SaveGame 기반 저장 기능 구현
- 팀 변경사항 병합

[GitHub 저장소](https://github.com/AnSeongSik-UE/TouchNPop)

## Unity

### Virtual Avatar Studio

웹캠의 얼굴과 상체 포즈를 Unity 6 Sentis로 추론해 VRM에 반영하고 Spout/OBS로 출력하는 1인 프로젝트입니다.

- 얼굴 및 상체 포즈 추론 결과를 VRM에 반영
- 추론 과정의 끊김을 줄이고 추론과 렌더링 처리 안정화
- VRM 0.x와 1.0 등록 및 교체, 중복 등록 방지와 캘리브레이션
- 웹캠, VRM, Spout, OBS의 전체 동작을 실제 환경에서 검증
- 기능 목표와 문제를 직접 정의하고 OpenAI Codex를 활용해 구현과 문제 해결을 진행한 뒤 실제 환경에서 결과 검증

[GitHub 저장소](https://github.com/AnSeongSik-UE/Virtual-Avatar-Studio) / [Windows 최신 릴리즈](https://github.com/AnSeongSik-UE/Virtual-Avatar-Studio/releases/latest)
