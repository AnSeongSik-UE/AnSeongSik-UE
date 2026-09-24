# 안성식

## C++/C# 기반 실시간 응용 소프트웨어 개발자

약 3년의 응용 소프트웨어 개발 경험이 있습니다. 로보스텍에서는 C++·C# 기반 Windows 상용 프로그램으로 실시간 영상 처리, 네트워크 통신과 외부 장비 연동을 개발했으며, KAKIS 프리랜서 기간에는 Python·PHP 개발과 Android 앱의 Google Play 업데이트·target SDK 대응을 수행했습니다. 개인 프로젝트에서는 Unity·Unreal 기반 실시간 콘텐츠를 실제 웹캠·아바타·방송 환경에서 검증했습니다.

## C++/C# Windows 상용 실무

### ROV Camera System · C++ / MFC

- 9채널 RTSP 영상 수신·표시와 H.264 녹화
- CUDA 기반 GPU 디코딩과 FFmpeg NVENC 녹화
- 프레임 타임아웃 감지, 자동 재연결과 종료 시 영상 자원 정리

### TunnelROVDataHub · C# / WinForms

- GNSS·Sonar·INS·Altimeter·PLC 데이터를 Serial·UDP·FEnet으로 수신·파싱
- 장비 데이터를 화면·로그와 외부 운용 시스템으로 전달
- 장비별 통신 상태와 수신 작업·타이머·연결 자원 수명주기 관리

### 조이패드 모터 제어 · C++ / Qt

- 조이패드 입력을 모터 제어 명령으로 변환
- Motor 1/2 RPM·전류·전압·온도 상태를 실시간 모니터링하는 UI 기능 추가

[Windows 장비 연동 개발 포트폴리오 보기](https://anseongsik-ue.github.io/windows-device-integration-portfolio/)

## Unity / Unreal 개인 프로젝트

### Virtual Avatar Studio · 1인 프로젝트 · OpenAI Codex 활용

웹캠 입력을 Unity Sentis로 얼굴·상체 포즈 데이터로 변환해 VRM에 반영하고, KlakSpout을 통해 OBS로 출력하는 Windows 실시간 콘텐츠 앱입니다.

기능 목표와 문제 상황을 자연어로 정의하고 Codex에 코드 검토·원인 분석·수정을 요청했습니다. 수정 결과는 실제 웹캠·VRM·Spout·OBS 환경에서 직접 검증하고, 사용 과정에서 발견한 문제와 필요한 기능을 다시 정의해 반복 개선했습니다.

- 평균 9 FPS 수준의 끊김을 확인해 원인 분석·수정을 요청하고, 수정 후 추론 갱신 평균 약 16 FPS와 렌더 평균 60 FPS 유지를 직접 확인
- VRM 0.x·1.0 등록·교체, 캐시·중복 방지, 캘리브레이션과 종료 자원 해제를 실제 환경에서 검증
- [GitHub 저장소](https://github.com/AnSeongSik-UE/Virtual-Avatar-Studio) · [Windows 최신 릴리즈](https://github.com/AnSeongSik-UE/Virtual-Avatar-Studio/releases/latest)

### Virtual Production Pipeline · 1인 프로젝트 · OpenAI Codex 활용

MediaPipe 얼굴·포즈 추론 결과를 Binary UDP로 Unreal Engine 5.8 C++ Runtime Plugin에 전달해 VRoid 표정·머리·양쪽 상완에 반영하고, 아바타와 배경을 Spout2로 송출하는 Windows 실시간 콘텐츠 앱입니다.

기능 목표와 문제 상황을 자연어로 정의하고 Codex에 코드 검토·원인 분석·수정을 요청했습니다. 수정 결과는 실제 웹캠·VRM·Spout·OBS 환경에서 직접 검증하고, 사용 과정에서 발견한 문제와 필요한 기능을 다시 정의해 반복 개선했습니다.

- 프로젝트는 고정 구조 Binary UDP 패킷 검증, 최신 프레임 처리와 추적 소실 복귀 기능으로 구성
- VRoid 표정·머리·양쪽 상완 반영과 ShowOnly HDR 캡처·GPU 합성 기반 1280×720 Spout2 출력을 실제 환경에서 검증
- 통신·트래킹·UI/방송·프로세스 수명주기와 Windows 배포·종료까지 단계별 확인
- [GitHub 저장소](https://github.com/AnSeongSik-UE/Virtual-Production-Pipeline-UE5.8) · [Windows 최신 릴리즈](https://github.com/AnSeongSik-UE/Virtual-Production-Pipeline-UE5.8/releases/latest)

## Unreal Engine 팀 프로젝트

### TouchNPop · 4인 팀 프로젝트

Unreal Engine 5·Blueprint·ARCore를 사용한 Android AR 두더지잡기 프로젝트입니다.

- 담당: AR Plane 자동 식별과 감지된 평면 내부 무작위 위치 캐릭터 스폰
- 담당: SaveGame 기반 저장 기능과 팀 수정사항 병합
- [GitHub 저장소](https://github.com/AnSeongSik-UE/TouchNPop)

## 프리랜서·개인 프로젝트

- [face-recognition](https://github.com/AnSeongSik-UE/face-recognition) — OpenCV 웹캠 프레임의 인식 상태·촬영 효과 합성과 PyQt 설정 화면
- [order-pdf-workflow](https://github.com/AnSeongSik-UE/order-pdf-workflow) — PDF 일괄 다운로드·가공, 일시정지·이어받기·재시도
- [shopping-rank-monitor](https://github.com/AnSeongSik-UE/shopping-rank-monitor) — 상품 순위 수집·변동 감지, SQLite 저장과 Telegram 알림
- [inventory-pda-api](https://github.com/AnSeongSik-UE/inventory-pda-api) — PDA 재물조사 정보 조회와 스캔 결과 등록을 처리하는 PHP API
- [trading-workflow-enhancements](https://github.com/AnSeongSik-UE/trading-workflow-enhancements) — 일별 거래내역 조회·표시와 수익률 기준 손절·익절 처리
