# 병목공정 분석

### ✅ 기능 설명

**병목공정 분석**은 설비별 작업시간(이동 시간)과 대기시간을 분석하여,\
생산 라인 내 **병목 지점을 정량적으로 시각화**하는 기능입니다.

* 설비가 작업을 **얼마나 오래 수행했는지** (Moving Time)
* **얼마나 오랫동안 대기했는지** (Waiting Time)를 구분하여
* 병목 현상이 발생하는 구간을 쉽게 파악할 수 있습니다.

<figure><img src="../../../../.gitbook/assets/image (125).png" alt=""><figcaption></figcaption></figure>

***

### 🛠 주요 특징

<table><thead><tr><th width="352" align="center">항목</th><th align="center">설명</th></tr></thead><tbody><tr><td align="center">정렬 기준</td><td align="center">병목 순위 또는 정지 시간 순으로 자동 정렬</td></tr><tr><td align="center">색상 표현</td><td align="center"></td></tr><tr><td align="center"> 🔷 파란색: <strong>설비 이동 시간</strong> (Moving Time)</td><td align="center"></td></tr><tr><td align="center"> 🟧 주황색: <strong>설비 대기 시간</strong> (Waiting Time)</td><td align="center"></td></tr><tr><td align="center">시각적 집중 표시</td><td align="center">병목지점은 <strong>대기시간이 긴 구간에서 명확히 표현됨</strong></td></tr><tr><td align="center">통계 지표</td><td align="center">AVG (평균), STD (표준편차), Times (횟수) 등 시계열 데이터 포함</td></tr></tbody></table>

***

### 📈 화면 구성 예시 (이미지 기준)

* 좌측: 설비별 작업 항목 리스트 (`S301.RBT1`, `SHUTTLE.CAR`, `OP_A.CAR` 등)
* 우측: 시간 기반 이동/대기 그래프 (파란/주황 막대 시각화)
* 수치: 각 설비의 평균 이동 시간 / 대기 시간 / 반복 횟수 등 표시

***

### 💡 활용 예

<table><thead><tr><th width="201.3333740234375" align="center">활용 시나리오</th><th align="center">효과</th></tr></thead><tbody><tr><td align="center">🔁 반복 병목 추적</td><td align="center">특정 설비나 위치에서 반복 발생하는 병목 구간 자동 인지</td></tr><tr><td align="center">🛠 설비 재배치 제안</td><td align="center">병목 구간을 기준으로 <strong>설비 순서 최적화</strong> 및 <strong>로직 변경</strong> 제안 가능</td></tr><tr><td align="center">📊 공정 개선 방향 도출</td><td align="center">병목 해소 후 흐름 재분석으로 <strong>전체 라인 효율 개선</strong> 도출</td></tr><tr><td align="center">🧠 병목 원인 파악</td><td align="center">대기시간 과다 발생 시 주변 조건 (센서, 로봇 대기, I/O 신호)와 연계 분석</td></tr></tbody></table>

***

### 🔧 실무 팁

* 정지 시간 기준 정렬 시 **가장 병목이 심한 설비**부터 우선 분석
* 함께 제공되는 **사이클 타임, 이력 분석**과 병행 분석 시 정확도 상승
* **자동 보고서 생성 기능** 사용 시 병목 Top-N 리스트 자동 출력 가능
