---
icon: bring-forward
---

# 모델링

## 📘 DS 모델링 규칙 매뉴얼

***

### 1️⃣ 도형 배치 및 중첩 규칙

#### 📍 일반 규칙

* **제목 슬라이드 제외**:\
  도형은 반드시 **제목 슬라이드를 제외한 장표**에만 배치
* 사각형(work)은 타원(action)을 포함할 수 있음

***

#### 🔲 사각형 (Work 도형)

<table><thead><tr><th width="292" align="center">항목</th><th align="center">규칙</th></tr></thead><tbody><tr><td align="center">중첩 허용</td><td align="center">O (타원만 포함 가능)</td></tr><tr><td align="center">내부 포함 방식</td><td align="center"><strong>사각형 내부에 완전히 포함</strong>되어야 함</td></tr><tr><td align="center">사각형 내부에 사각형 중첩</td><td align="center">❌ <strong>금지</strong></td></tr></tbody></table>

***

#### ⭕ 타원 (Action 도형)

|    항목   |             규칙            |
| :-----: | :-----------------------: |
|  중첩 허용  |     ❌ 불가 (다른 도형 포함 불가)    |
|    위치   |  **사각형 내부 또는 외부**에 위치 가능  |
| 외부 위치 시 | **조건 감시 용도**로 사용됨 (출력 없음) |

***

#### 📄 로드 도형 (Load)

* 반드시 **슬라이드 최외곽**에 위치해야 함
* 중첩 불가
* **연결선 불가** (Edge 연결하면 오류)

***

#### ◆ 연산 도형 (Condition)

* 반드시 **슬라이드 최외곽**에 위치
* 중첩 불가
* **입력선 없음**, **출력선은 사각형으로 연결**

***

### 2️⃣ 연결(Edge) 규칙

> 도형 간의 흐름(제어 순서)을 표현하는 **연결선 생성 시 준수사항**입니다.

#### 📌 일반 연결 조건

<table><thead><tr><th width="252" align="center">항목</th><th align="center">규칙</th></tr></thead><tbody><tr><td align="center">연결 유효성</td><td align="center">도형 이동 시 <strong>연결선도 함께 이동해야 연결된 것으로 간주</strong></td></tr><tr><td align="center">연결선 경로</td><td align="center"><strong>사각형을 뚫고 지나가면 안 됨</strong> (내부-외부 분리 유지)</td></tr></tbody></table>

***

#### 🔄 사각형 내부 연결

* 사각형 내부의 Action 간 연결은 허용
* 단, **DAG(Directed Acyclic Graph)** 구조를 유지해야 함
  * **순환(Cycle)** 금지!

***

#### 🌐 사각형 외부 연결

* 외부 도형(예: Work ↔ Work, Work ↔ Interface 등)의 연결은 **Cycle 허용**

***

#### ⚠️ 특수 도형의 연결 제한

<table><thead><tr><th width="270" align="center">도형</th><th align="center">연결 규칙</th></tr></thead><tbody><tr><td align="center"><strong>로드 (Load)</strong></td><td align="center">연결선 금지 ❌</td></tr><tr><td align="center"><strong>연산 (Condition)</strong></td><td align="center">입력선 ❌, 출력선은 사각형에 연결</td></tr><tr><td align="center"><strong>명령 (Action)</strong></td><td align="center">출력선 ❌, 입력선만 허용 (예: 트리거 발생 지점)</td></tr></tbody></table>

***

### 3️⃣ 명명 규칙 (Naming Rules)

> 도형 이름, 장치 이름, API 이름 등 모든 요소의 명명 방식은 아래 규칙을 따릅니다.

#### ✅ 허용 형식

<table><thead><tr><th width="277" align="center">조건</th><th align="center">설명</th></tr></thead><tbody><tr><td align="center">시작 문자</td><td align="center">반드시 영문 알파벳(a<del>z, A</del>Z)로 시작</td></tr><tr><td align="center">구성 문자</td><td align="center"><strong>알파벳, 숫자, 밑줄(<code>_</code>)</strong> 사용 가능</td></tr><tr><td align="center">구분자</td><td align="center"><strong><code>.</code>(dot)</strong> 사용 가능 (DS 언어 내 구분자)</td></tr><tr><td align="center">밑줄</td><td align="center"><strong>연속 밑줄(<code>__</code>) 금지</strong></td></tr></tbody></table>

***

#### ❌ 금지 사항

* 공백 문자 포함 불가
* 특수 문자(`!@#$%^&*()-+=~` 등) 사용 금지
* 숫자로 시작하는 이름 금지
* 중복된 이름 사용 금지

***

#### 🧭 주소 영역 규칙

* 주소 값은 **대상 PLC 플랫폼의 규격에 맞게 작성**
  * 예: LS XGI의 경우 `%Q0.0`, `%I1.0` 등 사용
* 장비별 IO Mapping 시, 올바른 주소와 장치명이 1:1 대응돼야 함

***

### 🔔 요약표

<table><thead><tr><th width="216" align="center">항목</th><th align="center">규칙 요약</th></tr></thead><tbody><tr><td align="center">도형 중첩</td><td align="center">사각형 내부에 <strong>타원만 포함 가능</strong>, 사각형 내부끼리는 중첩 ❌</td></tr><tr><td align="center">도형 위치</td><td align="center">Load/Condition 도형은 슬라이드 최외곽에 위치</td></tr><tr><td align="center">연결 구성</td><td align="center">사각형 내부: DAG 구조 유지<br>외부: Cycle 허용</td></tr><tr><td align="center">연결선 유효성</td><td align="center">도형 이동 시 연결선 따라 움직여야 유효 연결</td></tr><tr><td align="center">명명 규칙</td><td align="center">알파벳 시작, 특수문자 ❌, 연속 밑줄 ❌, <code>.</code> 구분자 사용 가능</td></tr><tr><td align="center">IO 주소</td><td align="center">PLC 플랫폼에 맞는 형식 적용 필요</td></tr></tbody></table>
