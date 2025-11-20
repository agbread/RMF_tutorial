# Open-RMF Tutorial

이 저장소는 Open-RMF를 처음 접하는 사용자를 위해 제작한 **튜토리얼 자료 모음**입니다.  
튜토리얼 영상과 슬라이드(PPT)를 보면서, 직접 데모를 실행하고 환경을 만들고, 태스크를 생성해보는 것을 목표로 합니다.

- 튜토리얼 영상: (YouTube 링크) https://www.youtube.com/playlist?list=PLjPJoa4-dGtbBEgE7Ge4zIC7xLcqfqPHH
- 튜토리얼 슬라이드 및 관련 자료(Google Drive):  
  https://drive.google.com/drive/folders/1QP4yWc97Mng6ip67Si4_xFa7CCRSI0wG?usp=drive_link
- 데모 코드 및 월드: [agbread/rmf_demos](https://github.com/agbread/rmf_demos)

---

## 튜토리얼에서 다루는 내용

튜토리얼은 크게 다음 네 가지 흐름으로 구성됩니다.

1. **RMF 데모 소개**
   - `rmf_demos`에서 제공하는 기본 데모(Hotel, Office, Clinic, Campus, Manufacturing & Logistics 등)를 개괄적으로 소개
   - 이 포크에서 추가한 **RCI Lab World**를 포함하여,
   - 여러 로봇 플릿, 엘리베이터(lift), 도어(door)가 어떻게 Open-RMF를 통해 조정되는지 시나리오 중심으로 설명

2. **Traffic Editor로 환경 제작하기**
   - Traffic Editor 기본 UI 및 개념 소개
   - 층(floor) 추가, 벽/문/리프트 배치 방법
   - waypoint, charger, docking, lift door 등 RMF에서 사용하는 오브젝트 배치 및 속성 설정
   - 작성한 building map을 이용하여
     - Gazebo Classic용 world 파일 생성
     - 층별 nav_graph(.yaml) 생성
   - 생성된 결과를 `rmf_demos` 패키지 구조에 통합하는 방법

3. **Task 생성 및 실행 방법**
   - `rmf_demos_tasks`를 이용한 **CLI 기반 task 생성**
     - loop(patrol) task
     - delivery task
     - clean task
   - task 상태를 RViz schedule visualizer로 확인하는 방법
   - 각 task가 실제 데모 월드에서 어떤 로봇 동작으로 나타나는지 시연

4. **RMF Panel 및 Web 연동**
   - [rmf-panel](https://github.com/open-rmf/rmf-panel-js) 소개
     - 단일 Task 제출
     - Task 목록(JSON) 로드 후 일괄 제출
   - 튜토리얼에서 사용하는 panel 설정 방법
     - `server_uri` 인자 설정 예시
     - `task_state_updates`를 이용해 웹에서 task/로봇 상태를 모니터링하는 방법
   - [rmf-web](https://github.com/open-rmf/rmf-web)과의 차이 및 언제 어떤 것을 사용할지에 대한 간단한 가이드

---

## 자료 다운로드

튜토리얼에서 사용하는 슬라이드 및 부가 자료는 Google Drive 폴더에 정리되어 있습니다.

- **튜토리얼 슬라이드(PPT) 및 관련 파일**  
  https://drive.google.com/drive/folders/1QP4yWc97Mng6ip67Si4_xFa7CCRSI0wG?usp=drive_link  

해당 폴더에는 다음과 같은 자료가 포함될 수 있습니다.

- 튜토리얼 본문 슬라이드 (PPTX / PDF)
- Traffic Editor 예제 프로젝트 파일
- 예시 task JSON (`*.json`)
- 기타 실습에 필요한 참고 파일

---

## 사전 준비 환경

튜토리얼은 다음 환경을 기준으로 제작되었습니다.

- **Ubuntu 22.04**
- **ROS 2 Humble**
- **Gazebo Classic 11**
- Open-RMF Humble 바이너리 패키지 (`ros-humble-rmf-dev`)
- 튜토리얼에서 사용하는 데모 코드:
  - [agbread/rmf_demos](https://github.com/agbread/rmf_demos)

Open-RMF/RMF Demos 설치 및 workspace 구성 방법은  
`agbread/rmf_demos` 저장소의 README에 정리되어 있으니, 먼저 해당 내용을 따라 환경을 준비하는 것을 권장합니다.
