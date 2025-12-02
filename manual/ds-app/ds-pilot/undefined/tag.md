# TAG 모니터링

### ✅ 기능 개요

**TAG 모니터링**은 설비/공정에서 사용하는 신호(TAG)의 **현재 상태, 변화 이력, 계층 구조**를\
**실시간으로 확인**할 수 있는 기능입니다.\
주요 제어 신호, 인터락 상태, 센서 반응 등을 **구조적/계층적으로 추적**하여\
문제 발생 시 빠른 원인 분석과 현장 대응이 가능합니다.

<figure><img src="../../../../.gitbook/assets/image (131).png" alt=""><figcaption></figcaption></figure>

***

### 🛠 주요 기능 설명

#### 1️⃣ 실시간 상태 보기

* 현재 모든 TAG의 상태를 **True/False 또는 수치 형태**로 표시
* 주기적으로 자동 갱신되어 실시간 모니터링 가능

#### 2️⃣ 계층 구조 기반 정렬

* **설비별, 공정별, 기능별 그룹화** 지원
* 복잡한 자동화 시스템에서 **중요 신호만 필터링해서 집중 추적 가능**

#### 3️⃣ TAG 변화 추적

* 신호가 언제 변경되었는지 시간 기준 로그 가능
* **True → False**, 또는 수치 변화 기반의 이벤트 감지 가능

#### 4️⃣ 인터락/이상 조건 감시

* 인터락 관련 TAG 감시로 **조건 미충족 원인 추적**
* 특정 TAG 상태가 고정되거나 비정상일 경우 **빠르게 진단 가능**

***

### 📊 화면 구성 예시 (이미지 기반)

<table><thead><tr><th width="194.66668701171875" align="center">영역</th><th align="center">설명</th></tr></thead><tbody><tr><td align="center">좌측 영역</td><td align="center">공정별 TAG 이름 리스트 (예: <code>OP_CAR_A_ON1</code>, <code>POSILOCK.RET</code>)</td></tr><tr><td align="center">우측 값 영역</td><td align="center">각 TAG의 현재 상태 (<code>True/False</code>, <code>N/A</code>, <code>수치 값</code>)</td></tr><tr><td align="center">상단 코드 뷰</td><td align="center">디지털 모델 또는 자동화 조건에 사용되는 TAG 흐름 참조용 구조 표시 (<code>FLOW</code>, <code>JOB</code> 등)</td></tr></tbody></table>

***

### 🎯 활용 예

<table><thead><tr><th width="226.66668701171875" align="center">시나리오</th><th align="center">설명</th></tr></thead><tbody><tr><td align="center">🔍 신호 반응 오류 확인</td><td align="center">특정 장비가 작동하지 않을 때, 관련 TAG가 <strong>정상 신호를 보내는지 확인</strong></td></tr><tr><td align="center">🧠 인터락 해제 여부 진단</td><td align="center">장비가 작동 불가할 때, <strong>인터락 조건 미충족 여부 판단</strong></td></tr><tr><td align="center">🔁 TAG 로그 기반 문제 재현</td><td align="center">장애 재현 시 해당 TAG 변화 이력을 기반으로 <strong>이상 조건 재현</strong></td></tr><tr><td align="center">🧪 자동화 로직 테스트</td><td align="center">제어 조건에 맞는 TAG가 정상적으로 반응하는지 확인하여 <strong>로직 검증</strong></td></tr></tbody></table>

***

### 📌 실무 팁

* 검색창 또는 필터 기능을 통해 **관심 TAG만 집중적으로 확인** 가능
* TAG 이름 패턴으로 조건 검색 (예: `*_ERROR`, `*_COMP`, `*_START`)
* “이상 이력관리” 및 “CCTV 영상”과 연계해 TAG 변화와 실제 현장 상황 비교 가능
