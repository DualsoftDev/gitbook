# 공정 상태

### ✅ 기능 설명

**공정 상태(Process Status)** 기능은 설비 및 생산 라인의 **운영 상태를 실시간 시각적으로 확인**할 수 있도록 지원합니다.\
각 설비의 구성 요소 상태를 다양한 방식으로 확인할 수 있으며, 장애 발생 시 **즉각적인 대응**이 가능하게 도와줍니다.

<figure><img src="../../../../.gitbook/assets/image (132).png" alt=""><figcaption></figcaption></figure>

***

### 🛠 주요 기능 특징

<table><thead><tr><th width="215.333251953125" align="center">항목</th><th align="center" valign="top">설명</th></tr></thead><tbody><tr><td align="center">🔁 시각화 보기 전환</td><td align="center" valign="top">상태 정보를 <strong>Kanban / Default / List</strong> 형태로 자유롭게 전환하여 확인</td></tr><tr><td align="center">🧩 구성 요소 상태 시각화</td><td align="center" valign="top">설비 구성요소(예: 로봇, 실린더 등)의 동작 상태 및 위치를 <strong>블록 단위로 표현</strong></td></tr><tr><td align="center">📌 설비 위치 기반 분류</td><td align="center" valign="top"><strong>라인 구성 순서</strong> 또는 <strong>공정 구역별로 그룹화</strong>하여 전체 흐름 파악 가능</td></tr><tr><td align="center">🧠 장애 시 빠른 인지</td><td align="center" valign="top">이상 발생 시 시각적 경고 제공 → <strong>즉시 원인 파악 및 조치 유도</strong></td></tr></tbody></table>

***

### 🖥 화면 구성 설명 (이미지 기준)

* 상단: `SHUTTLE`, `S301`, `S302` 등의 스테이션 단위 구역
* 중단: 각 스테이션별 요소(예: `DoubleCylinder`, `HOOK`, `Welding` 등) 상태 박스
* 왼쪽 드롭다운 메뉴: 보기 모드 전환 (`Kanban`, `Default`, `List`)
* 상태 박스: 각 요소 동작 가능 여부, 오류 여부, 실시간 상태를 색상 및 텍스트로 표시

***

### 🎯 활용 예

<table><thead><tr><th width="195.3333740234375" align="center">활용 목적</th><th align="center">설명</th></tr></thead><tbody><tr><td align="center">🔍 설비 실시간 점검</td><td align="center">현장의 <strong>장비 상태를 원격에서 실시간 시각적으로 점검</strong> 가능</td></tr><tr><td align="center">🧠 병목/과부하 확인</td><td align="center"><strong>병목이 발생한 라인 또는 멈춘 설비</strong>를 빠르게 식별</td></tr><tr><td align="center">🛠 초동 대응 지원</td><td align="center"><strong>이상 발생 즉시 상태 변화 확인 → 원인 추론 → 현장 조치 유도</strong></td></tr><tr><td align="center">🧩 공정 구성 검토</td><td align="center">전체 라인의 장비 구성 및 위치를 파악하고, <strong>공정 설계 기준 검토에 활용</strong></td></tr></tbody></table>

***

### 💡 실무 TIP

* **Kanban 보기**: 카드 스타일로 가독성 높고, 운영자에게 직관적
* **List 보기**: 설비 목록을 빠르게 필터링할 때 유용
* **Default 보기**: 기본 그룹 구조에 따른 전체 보기
* 이상 상태는 빨간색 또는 경고 아이콘으로 강조되며, 클릭 시 세부 내역 조회 가능
