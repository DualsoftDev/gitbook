# 이상 보기

### ✅ 기능 개요

\*\*이상 보기(Abnormality View)\*\*는 제조 공정 흐름의 정상/비정상 상태를 **진단 다이어그램(Diagnostics Diagram)** 형식으로 시각화하여,\
**전체 흐름의 이상 탐지 및 문제 추적**을 가능하게 하는 핵심 기능입니다.

* 방사형 구조를 활용하여 공정 단계별 동작을 한눈에 표현
* 색상 구분을 통해 현재 상태를 직관적으로 파악
* 반복되는 비정상 패턴이나 병목을 조기에 인지 가능

<figure><img src="../../../../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

### 🧭 주요 화면 구성

#### 🔵 진단 다이어그램 (Diagnostics Diagram)

* 중심 → 외곽 방향으로 공정 흐름 표현
* 각 섹터는 **설비 → 모듈 → 동작 항목** 계층을 의미
* 클릭 시 세부정보 탐색 가능

***

### 🎨 색상 코드 (우측 범례 기준)

|   색상   |    의미   |
| :----: | :-----: |
| 🔵 진파랑 | Flow 정상 |
| 🟦 하늘색 |    종료   |
|  🟨 노랑 |  준비 상태  |
|  🟩 연두 |   진행 중  |
|  🔴 빨강 |   비상정지  |
|  🟥 자홍 |   일시정지  |
|  ⚫ 회색  |    대기   |
| 🟥 진빨강 | 시간초과 이력 |

> ✅ 실제 이미지에서는 대부분 진파랑(정상), 연두(진행), 회색(대기), 노랑(준비), 간혹 빨강(이상정지)이 혼재되어 시각적으로 즉각 인지 가능

<div><figure><img src="../../../../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure> <figure><img src="https://dualsoft-2.gitbook.io/~gitbook/image?url=https%3A%2F%2F2569009332-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FggzSj7OzpTUPl71JfBtu%252Fuploads%252FS1Q2inYxCR9vxBDgdjfF%252F24.jpg%3Falt%3Dmedia%26token%3D95aba9bb-ff0a-4187-b7b2-19ccc2bbcb95&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=42853bfc&#x26;sv=2" alt="" width="563"><figcaption></figcaption></figure></div>

***

### 🔧 주요 기능 요약

<table><thead><tr><th width="372" align="center">기능</th><th align="center">설명</th></tr></thead><tbody><tr><td align="center">공정 상태 시각화</td><td align="center">전체 공정 흐름을 구조적 다이어그램으로 표현</td></tr><tr><td align="center">모듈별 동작 상태 분해</td><td align="center">세부 동작 항목 단위로 상태 추적 가능</td></tr><tr><td align="center">상태 진단</td><td align="center">비정상 흐름/대기/중단 지점 즉시 확인</td></tr><tr><td align="center">입력/출력 상태 포함</td><td align="center">I/O 조건이 반영된 진단 가능</td></tr></tbody></table>

***

### 📈 활용 예

|      활용 목적     |             설명            |
| :------------: | :-----------------------: |
| 🔍 공정 이상 조기 탐지 |     특정 설비 반복 중단 여부 추적     |
|   🛠 문제 원인 식별  | 종료 상태나 비상정지 위치 파악 후 원인 분석 |
|   📊 공정 흐름 개선  |  병목 지점 시각화 후 운영 개선 포인트 도출 |
|   🔁 반복 패턴 인지  |  특정 시간/라인에서의 반복 이상 흐름 탐지  |

***

### 💡 실무 TIP

* `Detail View = TRUE` 설정 시 하위 동작 항목까지 상세 표시됨
* 설비별로 구간을 클릭하면 하단 `공정 이력` 또는 `TAG 모니터링`과 연동 분석 가능
* ‘이력 분석’ 메뉴와 병행하여 **시간대별 이상 흐름 비교** 시 유용

***

### 📂 예시 해석 (이미지 기준)

* `S303.RBT1`\~`RBT4` : 대부분 정상(진파랑) → 정상 흐름
* `S305.HOOK.UP` : 빨강(비상정지) 발생 → 현장 점검 필요
* `CARTYPEMOVE.CAR_MOVE` : 회색(대기) 지속 → 병목 가능성
* `S302.STN` : 준비/진행 색상 반복 → 자동화 동기화 검토 필요
