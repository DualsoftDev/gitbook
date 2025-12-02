# 이력 분석

### ✅ 기능 설명

\*\*이력 분석(HISTORY ANALYSIS)\*\*은 시스템 전체에서 발생한 이벤트나 상태 변화의 이력을\
**시간 순서대로 시각화하여 이상 동작 추적 및 오류 패턴 분석에 활용**할 수 있는 기능입니다.

* 오류 발생 구간을 **타임라인 형태로 시각화**
* TAG 상태 변화 이력 기반으로 **정확한 원인 추적 및 반복 이상 진단** 가능

<figure><img src="../../../../.gitbook/assets/image (128).png" alt=""><figcaption></figcaption></figure>

***

### 🛠 주요 기능 특징

<table><thead><tr><th width="243.3333740234375" align="center">항목</th><th align="center">설명</th></tr></thead><tbody><tr><td align="center">🔍 집중 오류 구간 식별</td><td align="center">시간 축 기반 시각화로 <strong>특정 시간대의 오류 밀집 구간</strong> 식별 가능</td></tr><tr><td align="center">🔎 상태 변화 추적</td><td align="center">TAG 이름, 발생 시작 시각, 상태 값(True/False) 확인 가능</td></tr><tr><td align="center">🧠 조건 기반 검색</td><td align="center">특정 TAG, 오류 유형, 장비 조건 등 <strong>다양한 필터 검색</strong> 기능 지원</td></tr><tr><td align="center">⬇️ 데이터 내보내기</td><td align="center">전체 이벤트 이력 데이터 Export 가능 (CSV, Excel 등)</td></tr></tbody></table>

***

### 📊 화면 구성 예시 (이미지 기준)

* **좌측**: 메뉴 및 필터 조건
* **중앙**: 시간 축 기반 이벤트 상태 변화 시각화 (막대 또는 블록으로 표시)
* **우측**: 이벤트 로그 목록 (Tag Name, 시간, 상태값 등 표시)

***

### 📝 활용 예

<table><thead><tr><th width="250" align="center">활용 목적</th><th align="center">설명</th></tr></thead><tbody><tr><td align="center">⏱ 오류 시점 추적</td><td align="center">특정 오류가 언제, 어떤 장비에서 발생했는지 정밀 추적 가능</td></tr><tr><td align="center">🔁 반복 패턴 진단</td><td align="center">동일 TAG에서 반복적으로 발생하는 <strong>이상 시나리오</strong> 조기 탐지</td></tr><tr><td align="center">🧩 복합 문제 원인 규명</td><td align="center">한 시간대 여러 오류 발생 여부를 분석해 <strong>상관 관계 파악</strong></td></tr><tr><td align="center">🛠 장비 상태 확인</td><td align="center">장비별 상태 변화, 동작 실패 여부 등을 이력 기반으로 확인</td></tr></tbody></table>

***

### 💡 실무 TIP

* 오류 추적 시 **“Contains” 필터**로 오류 유형 키워드 검색 (예: `_errorWork`)
* `Export` 기능으로 기간별 로그 백업 또는 품질 이슈 보고서 작성
* “정지 분석” 또는 “공정 분석” 화면과 병행 사용하면 **이력 → 원인 → 개선** 흐름 구성 가능
