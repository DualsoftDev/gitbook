# 공정 분석

### ✅ 기능 요약

**공정 분석(Process Analysis)** 기능은 각 설비의 **세부 동작별 운전 시간과 대기 시간**을 측정하여,\
공정의 병목 구간, 이상 현상, 효율 저하의 원인을 **시각적으로 비교 분석**할 수 있게 해주는 기능입니다.

* 설비별 동작 구간을 블록 단위로 표시
* 색상과 수치로 각 동작 시간의 상태 및 결과를 한눈에 표현

<figure><img src="../../../../.gitbook/assets/image (127).png" alt=""><figcaption></figcaption></figure>

***

### 🛠 주요 기능 특징

<table><thead><tr><th width="236.6666259765625" align="center">항목</th><th align="center">설명</th></tr></thead><tbody><tr><td align="center">🔍 운전/대기시간 비교</td><td align="center">공정 동작 단위별로 <strong>운전 시간 / 대기 시간</strong>을 구분하여 시각화</td></tr><tr><td align="center">🎨 색상 상태 구분</td><td align="center"></td></tr><tr><td align="center">  🔵 <strong>종료</strong></td><td align="center"></td></tr><tr><td align="center">  🟢 <strong>준비</strong></td><td align="center"></td></tr><tr><td align="center">  🟡 <strong>진행 중</strong></td><td align="center"></td></tr><tr><td align="center">  🔴 <strong>에러/이상</strong></td><td align="center"></td></tr><tr><td align="center">🧱 스테이션별 상세 보기</td><td align="center">설비(RBT, SHUTTLE 등) 내부의 <strong>세부 작업 별 시간 분석</strong> 가능</td></tr><tr><td align="center">🔧 필터링 기능</td><td align="center">특정 <strong>운전시간/대기시간/정지사유</strong> 기준으로 정렬 및 필터</td></tr><tr><td align="center">📊 시간 수치 표시</td><td align="center">블록 내부에 **운전시간(sec)**이 함께 표시되어 수치적 판단 가능</td></tr></tbody></table>

***

### 🖥 화면 구성 예시 (이미지 기준)

* 블록 하나: 특정 설비의 하나의 동작 (예: `RBT4.WELD`, `POSILOCK.RET`)
* 블록 색상: 상태(종료, 준비, 진행, 에러 등)를 표시
* 수치: 각 동작의 소요 시간 (예: 2.80 sec, 1.62 sec 등)
* 좌측 필터 메뉴: `운전시간`, `정지시간`, `이슈 발생 시간` 등 기준 선택 가능

***

### 📈 활용 예

<table><thead><tr><th width="218.6666259765625" align="center">활용 목적</th><th align="center">설명</th></tr></thead><tbody><tr><td align="center">🧠 병목 구간 파악</td><td align="center">특정 설비에서 <strong>작업 시간이 비정상적으로 긴 구간</strong> 탐색</td></tr><tr><td align="center">🛠 공정 최적화</td><td align="center">전체 흐름 중 <strong>과부하 설비</strong>를 기준으로 공정 개선 포인트 도출</td></tr><tr><td align="center">🔁 반복 이상 구간 탐색</td><td align="center">동일 설비에서 반복적으로 시간 이상이 발생하는 구간 식별</td></tr><tr><td align="center">🔎 시간 비교 진단</td><td align="center">같은 설비의 같은 동작이라도 사이클마다 시간이 다른 이유 파악 가능</td></tr></tbody></table>

***

### 💡 실무 TIP

* 병렬 설비의 성능 비교 시, **같은 동작(RBT1\~RBT4)의 시간 편차**를 정렬하여 비교
* 필터 메뉴에서 ‘정지시간’을 선택하면, **잠재적 이상 위치를 빠르게 확인 가능**
* 공정별 분석 결과는 `이력 분석` 탭과 함께 저장/보고서 출력 가능
