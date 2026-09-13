# 안성식

C#·C++ 기반 Windows 응용프로그램과 Unity·Unreal Engine 실시간 콘텐츠를 개발합니다. 장비·영상·웹캠 입력을 처리해 사용자 화면, 아바타와 외부 시스템으로 연결하는 기능을 구현해 왔습니다.

## 주요 프로젝트

### Unity

#### Virtual Avatar Studio · 1인 개발

웹캠 프레임을 Unity Sentis로 추론해 얼굴·상체 데이터를 생성하고, VRM 본·표정 반영부터 KlakSpout·OBS 출력까지 연결한 Windows 실시간 콘텐츠 애플리케이션입니다.

- 포즈 검출기의 GPU 출력 대기 구조를 변경해 추론 갱신 평균을 9 FPS에서 16 FPS로 높이고 렌더 평균 60 FPS 유지
- VRM 0.x·1.0 등록과 교체, 캐시·중복 방지, 캘리브레이션과 자원 수명주기 처리
- [GitHub 저장소](https://github.com/AnSeongSik-UE/Virtual-Avatar-Studio) · [Windows 최신 릴리즈](https://github.com/AnSeongSik-UE/Virtual-Avatar-Studio/releases/latest)

### Unreal Engine

#### Virtual Production Pipeline · 1인 개발

웹캠의 MediaPipe 얼굴·포즈 추론을 Binary UDP로 Unreal Engine 5.8 C++ Runtime Plugin에 전달해 VRoid 표정·머리·양쪽 상완을 구동하고, 아바타와 배경만 Spout로 송출하는 Windows 실시간 콘텐츠 앱입니다.

- VPTP 스키마 3 패킷 검증, 최신 프레임 처리와 추적 소실 복귀 구현
- ShowOnly HDR 캡처와 GPU 합성으로 배경 제거·크로마 키 및 1280×720 Spout 출력
- Python 테스트 33/33, Unreal 자동화 테스트 28/28, Windows 배포본 검사 26 PASS·0 FAIL
- [GitHub 저장소](https://github.com/AnSeongSik-UE/Virtual-Production-Pipeline-UE5.8) · [Windows 최신 릴리즈](https://github.com/AnSeongSik-UE/Virtual-Production-Pipeline-UE5.8/releases/latest)

#### TouchNPop · 4인 팀 프로젝트

Unreal Engine 5와 ARCore를 사용한 Android AR 두더지잡기 프로젝트입니다.

- 선택한 AR 평면의 캐릭터 생성·재선택, 생성 제한·재시도 구현
- Unreal SaveGame 기반 최고 기록 저장·로드와 기존 터치·UI 흐름 통합
- [GitHub 저장소](https://github.com/AnSeongSik-UE/TouchNPop)

## Windows 응용프로그램 개발

- C++·Qt: 조이패드 입력을 모터 제어 명령으로 변환하는 프로그램
- C++·MFC: 9채널 RTSP 영상의 CUDA 디코딩·화면 표시와 FFmpeg NVENC 녹화
- C#·WinForms: Serial·UDP·FEnet 장비 데이터 수신·변환 및 외부 시스템 연동
- [Windows 장비 연동 프로젝트 상세 보기](https://app.notion.com/p/Windows-3c0521c4b7758133802fe1d42fc5a322)

## Python·PyQt 응용프로그램

- [face-recognition](https://github.com/AnSeongSik-UE/face-recognition) — OpenCV 웹캠 프레임의 인식 상태·촬영 효과 합성 및 PyQt 설정 흐름
- [order-pdf-workflow](https://github.com/AnSeongSik-UE/order-pdf-workflow) — QThread 기반 PDF 일괄 다운로드, 일시정지·이어받기·재시도
- [shopping-rank-monitor](https://github.com/AnSeongSik-UE/shopping-rank-monitor) — 상품 순위 수집·SQLite 저장과 Telegram 예약 알림
