# 정지 분석

### ✅ 기능 설명

\*\*정지 분석 (Sequence Flow Diagram)\*\*은 공정 설비 내 작업 순서를 시각적으로 표현하여,\
**공정 흐름의 연결 관계 및 진행 상황을 한눈에 파악할 수 있도록 지원하는 기능**입니다.

* 작업 간 연결 흐름을 선형적으로 표현
* 장비 간 작업 순서, 진행 상태, 지연 구간 등을 시각적으로 확인 가능

<figure><img src="../../../../.gitbook/assets/image (126).png" alt=""><figcaption></figcaption></figure>

***

### 🛠 주요 특징

<table><thead><tr><th width="213.333251953125" align="center">항목</th><th align="center">설명</th></tr></thead><tbody><tr><td align="center">📌 동작 연결 흐름 표현</td><td align="center">작업 간의 입력 → 처리 → 출력 관계를 선으로 표시</td></tr><tr><td align="center">📦 처리 상태 시각화</td><td align="center">완료 지점/종료 상태는 <strong>선 종료</strong>, 진행 중/준비 상태는 <strong>회색/노랑 표시</strong></td></tr><tr><td align="center">🔀 복합 흐름 대응</td><td align="center">조건 분기, 순차, 병렬 흐름 등 복잡한 작업 순서도 표현 가능</td></tr><tr><td align="center">📍 위치 기반 정지 파악</td><td align="center">정지 또는 병목이 발생한 지점을 정확히 추적 가능</td></tr></tbody></table>

***

### 🎨 상태 색상 예시 (이미지 기반)

<table><thead><tr><th width="283.333251953125" align="center">색상</th><th align="center">의미</th></tr></thead><tbody><tr><td align="center">회색</td><td align="center">준비 상태 또는 실행 대기</td></tr><tr><td align="center">노랑</td><td align="center">실행 진행 중</td></tr><tr><td align="center">녹색</td><td align="center">작업 완료 또는 종료 처리됨</td></tr><tr><td align="center">흐림</td><td align="center">연결된 다음 단계가 미진행 상태일 경우 흐림 효과</td></tr></tbody></table>

***

### 📈 활용 예

<table><thead><tr><th width="195.33331298828125" align="center">시나리오</th><th align="center">설명</th></tr></thead><tbody><tr><td align="center">🔍 공정 흐름 시각화</td><td align="center">장비 간 <strong>동작 순서</strong>를 시퀀스로 직관적으로 표현</td></tr><tr><td align="center">🛠 병목 위치 파악</td><td align="center">복잡한 조건 내에서 병목 또는 <strong>지연 지점</strong> 빠르게 확인</td></tr><tr><td align="center">🧠 동선 최적화 설계</td><td align="center">전체 작업의 흐름을 기반으로 <strong>최적 동작 설계안 도출</strong></td></tr><tr><td align="center">⏱ 동기 타이밍 조정</td><td align="center">특정 장비의 완료 시점과 다음 장비의 시작 시점 <strong>비동기 문제 식별</strong> 가능</td></tr></tbody></table>

***

### 💡 실무 TIP

* 장비명 또는 동작명을 클릭하면 관련 이력 확인 가능
* 이 기능은 “이상 보기”, “병목 분석” 기능과 함께 사용 시 더 높은 진단 효과
* 전체 공정의 ‘시간 흐름 기반 Gantt’와는 다르게 **구조적 흐름 기반** 진단에 적합
